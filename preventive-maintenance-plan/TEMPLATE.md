# Preventive maintenance plan

Workflow template, version 0.1.0.

## Purpose

Prepare the preventive maintenance plan for one site from the manager's own equipment register, the maker's maintenance tasks, the failure history and the spare parts list: every asset ranked by what one failure would cost, with the arithmetic shown; the maintenance approach for each (run to failure, scheduled or condition-based) with its reason; a dated calendar of tasks for the plan period, with intervals taken from the maker's guidance and shortened only where the failure history supports it; the spare parts to hold and what is short; and the downtime and repair-time measures to track, with a baseline from the history. Safety-critical equipment is set out for a competent person, who confirms its intervals; the plan is not an engineering sign-off. The assistant prepares; it never orders parts, books work, changes a record in any system, sets a target or signs anything.

## When to use it and when not to

Use it when a site has no written maintenance plan, once a year to renew the plan, when equipment is added or replaced, when a site is taken over, and when unplanned stoppages are rising and the manager wants the work put on a calendar.

Do not use it:

- when equipment is unsafe now. Stop it and deal with it under the site's own arrangements first;
- to work out why a particular breakdown or incident happened. That is an investigation, a separate piece of work whose findings can feed the next run of this one;
- to assess the hazards of a task to the people doing it. That is a risk assessment, a separate piece of work;
- to set or approve intervals for safety-critical equipment such as gas appliances, pressure systems, lifting equipment or fire systems. The plan carries the maker's intervals and a competent person confirms them;
- to predict when an asset will fail, model its remaining life or calculate an optimal interval by statistics. The plan works from the maker's guidance and plain counts from the history;
- to say which inspections the law requires. Those duties differ by country and by type of equipment, and the competent person confirms them.

## Roles

- **Runs it:** the facilities manager, plant manager or operations manager responsible for the site.
- **Supplies the facts:** the manager, the maintenance technician who keeps the records, and the person who keeps the stores.
- **Confirms the intervals and the plan for safety-critical equipment, and signs for them:** the competent person, someone with the training and experience to judge that equipment, from inside the business or an outside firm. Always a person.
- **Settles the decisions, sets the targets and approves the plan:** the manager who runs it.
- **Approves spare-part purchases:** the role the settings name.
- **Records stoppages and completed tasks:** the role the settings name.

## Inputs

1. **The equipment register,** one row per asset, with these column headers: `asset_id`, `asset`, `area`, `installed`, `run_hours_per_week`, `safety_critical`, `cost_per_hour_stopped`, `est_hours_stopped`, `est_repair_cost`, `condition_check`. `safety_critical` is yes or no. `cost_per_hour_stopped` is what one hour with the asset stopped costs the business, counting any backup it has. `est_hours_stopped` and `est_repair_cost` are the manager's estimates for one failure, used only when the history has none for that asset. `condition_check` is a reading the team can take and the limit at which work is needed, such as "motor bearing temperature, limit 70 C", or blank. If the register is missing, stop and ask.
2. **The maker's tasks,** one row per task, with these column headers: `asset_id`, `task`, `every`, `unit`, `last_done`, `reference`. `unit` is weeks, months or run hours. `reference` is where the maker states it, such as a manual page. If the file is missing, stop and ask; tasks are never taken from general knowledge of a kind of equipment.
3. **The failure history** for a stated period, optional, one row per unplanned stoppage, with these column headers: `asset_id`, `date_failed`, `hours_stopped`, `repair_hours`, `parts_and_labour`, `cause`. `hours_stopped` runs from the stoppage until the asset runs again; `repair_hours` is the hands-on repair time. If it is supplied without its period, stop and ask. If none is supplied, write "no failure history supplied".
4. **The spare parts list,** optional, with these column headers: `part`, `asset_id`, `on_hand`, `lead_time_days`, `unit_cost`, `used_last_12_months`. If none is supplied, write "no spare parts list supplied".
5. **The settings:** the site, the role the plan is prepared for, today's date and the plan start, the plan period, the history period, days the site is closed, the currency, the band thresholds, how often condition checks are taken, the competent person for safety-critical equipment (by role), who records stoppages and completed tasks, and who approves spare-part purchases. Defaults where a setting is missing: plan period 52 weeks from today; band A from 5,000 a failure, band B from 1,000; condition checks every month; say which defaults were used. If the competent person is missing, write "competent person not named" and raise a decision.

**Column headers.** If any file's headers do not match the ones above (renamed, missing or extra), stop and ask which column holds what. Never guess.

The assistant works from the files and notes the person supplies. It needs no access to any maintenance system or supplier and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm the headers of every file. Count the assets, tasks, history rows and parts. If two assets share an ID, stop and ask. A history row whose asset ID is not on the register is a history item: list it under the measures, count it nowhere else, and raise a decision. A part whose asset ID is not on the register is listed under the spare parts as "asset not on the register", with no minimum worked out. A `safety_critical` value that is blank or not yes or no is "not stated": treat the asset as safety-critical until it is answered, and flag it.
2. **Leave out personal details.** Refer to people by role. If the history or notes name a person, leave the name out and record that a name was left out.
3. **Work out the failure cost of each asset.** If the history holds one or more failures for the asset: average hours stopped per failure × `cost_per_hour_stopped` + average `parts_and_labour` per failure, marked "from history, [n] failures". Otherwise: `est_hours_stopped` × `cost_per_hour_stopped` + `est_repair_cost`, marked "manager's estimate, no failures in the history". Show the arithmetic. If a figure the sum needs is missing, write "failure cost unknown", say what is missing, and flag "cost unknown".
4. **Rank and band.** Rank the assets by failure cost, highest first; assets with an unknown cost come last. Band A: failure cost at or above the band A threshold, or safety-critical. Band B: at or above the band B threshold. Band C: below it. An asset with an unknown cost is "not banded" unless it is safety-critical, which makes it band A. Where the safety-critical mark alone puts an asset in band A, write "Band A (safety-critical)".
5. **Choose the approach.** In this order:
   - **Run to failure:** band C and not safety-critical. It is repaired when it fails. Its maker's tasks are left off the calendar and listed, so nothing is dropped silently.
   - **Condition-based:** band A or band B, not safety-critical, with a `condition_check` that states a limit as a number with a unit. The maker's tasks stay on the calendar, the check is added at the condition check interval, and a reading at or past the limit goes to the manager the same day.
   - **Scheduled:** every other asset, including every safety-critical asset. Its maker's tasks go on the calendar. A safety-critical asset with a condition check that states a limit gets the check as well.
   - A `condition_check` with no number and unit for its limit does not count: the asset is scheduled and flagged "condition check has no limit".
   - A not-banded asset is scheduled until its cost is known.
   Give each approach a one-line reason from the band, the safety-critical mark and the check.
6. **Set the intervals.** Take each task's interval from the maker's tasks as written. Convert run hours to whole weeks: run hours ÷ `run_hours_per_week`, rounded down, and show the conversion. Then look at the history for assets that are not safety-critical and not run to failure (a run-to-failure asset's tasks are off the calendar and are not examined; its failures still count in the measures): a failure is linked to a task when its cause names, as the thing that failed, a part the task names. "Drive belt snapped" links to "Check drive belt tension and wear"; "blade guard switch failed" names a guard switch as what failed, not a blade, so it does not link to "Sharpen or replace blades". A shared word alone is not a link. Where two or more failures in the history period link to one task, work out the average number of days between them and compare it with the task's own interval in days (a week 7, a month 30, 2 months 61, a quarter 91, 6 months 182, a year 365; a run-hour task, its converted weeks × 7). If the average is shorter, propose the longest of these steps that is shorter than the average: a week (7 days), a month (30), 2 months (61), a quarter (91), 6 months (182), a year (365). A run-hour task's converted length is the interval being compared, not a step. Mark the proposal "proposed from history; maker's interval [interval]", use it on the calendar, and flag "interval proposed from history". If no step is shorter than the average (an average under 7 days), keep the maker's interval on the calendar and flag "failures closer than a week". Never lengthen an interval beyond the maker's. Never change an interval on a safety-critical asset: report what its history shows in the competent person's section instead. An asset that is not run to failure and has no maker's tasks gets none invented: flag "no maker's tasks".
7. **Date the calendar.** For each task, the next due date is `last_done` plus the interval (months by calendar month, keeping the day; where that day does not exist in the month, use the last day of that month). If that falls before the plan start, the task is due on the plan start and flagged "overdue", with the date it was due. If `last_done` is blank, the task is due on the plan start and flagged "no record". A new condition check is due on the plan start without a flag. Repeat each task by its interval through the plan period; a task placed on the plan start, overdue, unrecorded or new, repeats from the plan start, not from the date it was due. If a date falls on a day the site is closed, move it to the working day before and say so. Weekly tasks go under "Every week" and monthly tasks under "Every month", each with its first due date only, since the later dates follow at the interval; every other task is dated under the month it falls in. Write each month of the plan period in order; a month with no dated task says "None beyond the weekly and monthly tasks." Mark every task on a safety-critical asset "Safety-critical: interval for the competent person to confirm."
8. **Size the spare parts.** For each part: use during the lead time = `used_last_12_months` × `lead_time_days` ÷ 365, to two decimal places. The minimum to hold is that figure rounded up to a whole part, and at least 1 for a part of a band A asset. Mark it "band A minimum" only where that rule raised it, that is where the rounded figure was 0. Compare it with `on_hand`: "enough", or "short [n]" with the cost at `unit_cost`. If the lead time is blank, write "lead time not stated: minimum not worked out" and flag the asset "part lead time not stated". If a calendar task's wording contains the part's whole name, word for word apart from plurals and capitals (a task that shares only some of the name's words does not count), and the task falls due before plan start + lead time with none on hand, flag the asset "part needed before it can arrive". Total what is short as a list for the approver. Nothing is ordered.
9. **Work out the measures.** For each registered asset in the history, for the history period: failures; hours stopped and the average per failure; repair hours and the average per failure; run hours in the period (`run_hours_per_week` × the weeks in the period) and run hours between failures (run hours ÷ failures); parts and labour. An asset with no failures shows its run hours without a failure. Then the totals for all registered assets. Averages to one decimal place. History items are listed and not counted. Then list the six measures to track, each with its baseline from these figures, or "none in the inputs". The baselines for measures 1 and 2 are totals for the whole history period, not monthly figures; the monthly figures are added up over a period of the same length to compare with them. Set no target; the manager sets them.
10. **Write the competent person's section.** For each safety-critical asset: its tasks with the maker's intervals and next due dates, its failures in the history with their causes, any parts short, and its flags. Where its history would have led to a proposal under step 6, say so here as a fact, without proposing.
11. **Flag.** Put every flag on the asset's line in the ranked list, kinds separated by commas, each asset counted once: cost unknown; safety-critical not stated; no maker's tasks; interval proposed from history; failures closer than a week; condition check has no limit; overdue; no record; part lead time not stated; part needed before it can arrive.
12. **Write the decisions.** One numbered decision per flagged asset, in rank order, then one per history item, then "competent person not named" if it applies. Each gives the facts and one question per kind of flag, and says who answers: the competent person for anything about a safety-critical asset's intervals or tasks, the manager for everything else. Recommend nothing beyond what the plan already shows.
13. **Things to check.** As questions, each naming the input it comes from: a history cause that names a guard, interlock, emergency stop, relief valve, gas or alarm on an asset not marked safety-critical; a failure on a band A or band B asset that links to no task; a task whose `last_done` is the date of a failure on the same asset whose cause names the task's part as what failed, asking whether the task was done that day or the date is the repair; a fact stated loosely. If none, write "None."
14. **Return the draft** to the manager. The manager settles the decisions and passes the safety-critical section to the competent person. People book the work, order the parts and change the records.

## Exceptions and stop conditions

- **Equipment is unsafe now:** stop. Tell the person to take it out of use under the site's own arrangements; prepare nothing until that is done.
- **No register or no maker's tasks:** stop and ask. Never supply standard tasks or intervals for a kind of equipment.
- **Column headers do not match:** stop and ask which column holds what.
- **History supplied without its period, or two assets with the same ID:** stop and ask.
- **Asked to lengthen an interval beyond the maker's, or to change any interval on a safety-critical asset:** decline. Record the request as a decision, for the competent person where the asset is safety-critical.
- **Asked to predict when an asset will fail, estimate its remaining life or calculate an optimal interval:** decline; the plan works from the maker's guidance and the counts in the history.
- **Asked to order parts, book work, contact a supplier or the competent person, or update a maintenance system:** decline and name the role that does it.
- **Asked to sign the plan, approve an interval or say which inspections the law requires:** decline. The competent person confirms safety-critical intervals and the inspection duties that apply.
- **Asked to set a target for a measure:** decline; the manager sets targets.
- **The inputs contain a password, a login code or a person's name in connection with a fault:** do not repeat it; tell the person to remove it from the source and refer to the role.

## Output format

```
PREVENTIVE MAINTENANCE PLAN: [site]

Prepared for: [role]. Prepared: [date]. Plan period: [start date] to [end date] ([n] weeks).
History: [period], [n] rows / no failure history supplied.
Sources: equipment register ([n] assets); maker's tasks ([n] tasks); [failure history /
no failure history supplied]; [spare parts list ([n] parts) / no spare parts list
supplied]; settings. [Defaults used: ...] [A name was left out of the history.]
Bands: A, failure cost [amount] or more, or safety-critical; B, [amount] to [amount];
C, below [amount]. ([The organization's bands / The default bands in this template.])
Competent person for safety-critical equipment: [role / competent person not named].
Assets: [n]. Band A [n], B [n], C [n], not banded [n]. Safety-critical: [n].
Approaches: run to failure [n], scheduled [n], condition-based [n].
Tasks on the calendar: [n] ([n] from the maker's tasks, [n] condition checks). Left off: [n].
Flagged: [n] assets, [n] history items. Decisions: [n].

1. EQUIPMENT RANKED BY FAILURE COST
[rank]. [ID] [asset] ([area]). Failure cost [amount] = [n] h stopped x [amount] an hour
+ [amount] parts and labour ([from history, n failures / manager's estimate, no failures
in the history]). / Failure cost unknown: [what is missing]. Band [A / B / C / not
banded][ (safety-critical)]. Safety-critical: [yes / no / not stated].
[FLAG, kind[, kind]. See decision [n].]

2. MAINTENANCE APPROACH
[ID] [asset]: [Run to failure / Scheduled / Condition-based]. [Reason.]

3. TASK CALENDAR
Every week
[ID] [task]. Last done: [date / no record]; next due [date][; overdue, was due [date]].
Ref: [reference]. [Safety-critical: interval for the competent person to confirm.]
[or: None.]
Every month
[ID] [task]. First due [date]. Last done: [date / no record / new condition check][;
overdue, was due [date]]. Ref: [reference / condition check, limit [limit]].
[Safety-critical: interval for the competent person to confirm.]
[or: None.]
[Month year]
[date] [ID] [task]. Every [interval][, converted from [n] run hours at [n] a week][,
proposed from history; maker's interval [interval]]. Ref: [reference]. [Overdue, was
due [date]. / No record of when it was last done.] [Safety-critical: interval for the
competent person to confirm.]
[or: None beyond the weekly and monthly tasks.]
Left off the calendar (run to failure): [ID] [task], every [interval]. / None.
Assets with no maker's tasks: [IDs] / None.

4. SPARE PARTS TO HOLD
[part] for [ID] (band [x]). Used [n] in the last 12 months; lead time [n] days; use during
the lead time [n.nn]. Hold at least [n][ (band A minimum)]. On hand [n]: [enough / short
[n], [amount]].
[part] for [ID] (band [x]). Used [n] in the last 12 months. Lead time not stated: minimum
not worked out.
To buy, for the [approver role]'s approval: [part, n, amount; ...]. Total [amount]. /
Nothing to buy. Nothing has been ordered.
Parts for assets not on the register: [part, ID] / None.
[or: No spare parts list supplied.]

5. DOWNTIME AND REPAIR-TIME MEASURES
Baseline from the history, [period]:
[ID]: [n] failures; [n] h stopped (average [n.n] h); repair [n] h (average [n.n] h);
[n] run hours, [n] run hours between failures; parts and labour [amount].
[ID]: no failures in [n] run hours.
All registered assets: [n] failures; [n] h stopped (average [n.n] h); repair [n] h
(average [n.n] h); parts and labour [amount].
History items, not counted above: [ID, date, cause] / None.
[or: No failure history supplied: no baseline.]
To track from [plan start], recorded by [role / recorder not named], reviewed monthly by
[role]:
1. Unplanned stoppages each month. Baseline: [n] in the history period / none in the inputs.
2. Hours stopped by failures each month. Baseline: [n] h in the history period / none in
the inputs.
3. Average hours stopped per failure. Baseline: [n.n] h / none in the inputs.
4. Average repair time per failure. Baseline: [n.n] h / none in the inputs.
5. Run hours between failures, each band A and band B asset. Baseline: [ID n; ...].
6. Calendar tasks done by their due date, as a share of the tasks due that month.
Baseline: none in the inputs.
Targets: set by the [role]; none proposed in this draft.

6. FOR THE COMPETENT PERSON: SAFETY-CRITICAL EQUIPMENT
[ID] [asset]. Tasks at the maker's intervals: [task, every [interval], next due [date];
...]. Failures in the history: [n, with causes / none]. Spare parts short: [parts /
none]. [Flags: kinds / No flag.] [What the history shows.] To confirm: each interval,
and the plan for this asset, before anyone relies on it.
[or: No safety-critical equipment on the register.]

7. DECISIONS: [n]
[n]. [ID], [kinds]. [The facts.] [One question per kind.] For: [role].
[or: None.]

8. THINGS TO CHECK
- [Question, naming the input it comes from]
[or: None.]

Draft for the [role]. Intervals for safety-critical equipment are
confirmed and signed by the competent person; this plan is not an
engineering sign-off. Inspection duties set by law differ by country and
by type of equipment; the competent person confirms which apply. Nothing
has been ordered, booked, sent or changed in any system.
```

## Reviewer checklist

1. Every failure cost follows the stated sum, uses history where the history has failures and the estimate only where it has none, and the ranking follows the costs. (Manager)
2. Every band and approach follows the thresholds and the order of rules; no band C asset is safety-critical. (Manager)
3. Every task on the calendar comes from the maker's tasks or is a condition check from the register; none has been invented and none silently dropped. (Maintenance technician)
4. No interval is longer than the maker's, every shortened interval shows the failures behind it, and no safety-critical interval has been changed. (Manager)
5. Every due date is last done plus the interval, and overdue and unrecorded tasks fall on the plan start. (Maintenance technician)
6. Every spare-part minimum and shortage is arithmetically correct, and nothing has been ordered. (Person who keeps the stores)
7. Every baseline figure traces to the history rows, and history items are listed and not counted. (Manager)
8. The competent person has confirmed every interval and the plan for each safety-critical asset, and signed for them, before the plan is relied on. (Competent person)

## Acceptance tests

Proposed tests. None has been run as a separate test. The invented example, tried in Claude (see the record published with the template), happens to exercise the cases in tests 4, 6, 7, 8, 9, 10 and 12; the rest have not been tried at all.

1. **Ordinary site.** Six assets, complete files, no flags. Expected: costs, bands, approaches, a dated calendar, spare parts and measures, with every figure traceable.
2. **Renamed column.** The history has `downtime` in place of `hours_stopped`. Expected: stops and asks which column holds what; no figures worked out.
3. **No history.** Expected: every cost from the manager's estimates, marked so; "no failure history supplied"; no interval proposed; measures with no baseline.
4. **Repeated failure.** Three belt failures an average of 115.5 days apart on a task the maker sets at 6 months. Expected: quarterly proposed, marked with the maker's interval, used on the calendar, flagged and put to the manager.
5. **Safety-critical repeated failure.** The same pattern on a gas oven. Expected: no interval changed; the facts set out in the competent person's section.
6. **Run-hour interval.** 500 run hours on an asset run 60 hours a week. Expected: every 8 weeks, with the conversion shown.
7. **Overdue and unrecorded tasks.** One task last done ten months ago on a quarterly interval; one with no last done date. Expected: both due on the plan start, flagged "overdue" (with the date it was due) and "no record".
8. **Check with no limit.** A band B asset whose check says "limit not known". Expected: scheduled, flagged "condition check has no limit".
9. **Band A part never used.** A part with no use in the year on a band A asset. Expected: hold at least 1, marked "band A minimum".
10. **History row for an unknown asset.** Expected: listed as a history item, not counted in the totals, one decision.
11. **Asked to lengthen an interval or to order parts.** Expected: declines, names the role, records a lengthening request as a decision.
12. **Guard switch on an asset not marked safety-critical.** Expected: a question under Things to check; the asset's approach follows the register.
13. **No maker's tasks for a band A asset.** Expected: no task invented; flagged "no maker's tasks" and a decision.
14. **Safety-critical asset with a numeric check.** A band A gas boiler, marked safety-critical, whose check is "flue gas temperature, limit 220 C". Expected: scheduled, not condition-based; the check added at the condition check interval beside the maker's tasks; every task marked for the competent person.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a preventive maintenance plan for one site from the
manager's own files. You prepare; people decide. You never order parts,
book work, contact anyone, change a record in any system, set a target,
approve an interval or sign anything. You never ask for a password or a
login code and need no access to any system.

The user will supply: the equipment register (asset_id, asset, area,
installed, run_hours_per_week, safety_critical, cost_per_hour_stopped,
est_hours_stopped, est_repair_cost, condition_check); the maker's tasks
(asset_id, task, every, unit, last_done, reference); optionally the
failure history for a stated period (asset_id, date_failed,
hours_stopped, repair_hours, parts_and_labour, cause) and the spare
parts list (part, asset_id, on_hand, lead_time_days, unit_cost,
used_last_12_months); and the settings. If the register or the maker's
tasks are missing, stop and ask. If any header does not match, stop and
ask which column holds what. If the history has no period, or two
assets share an ID, stop and ask. Defaults for missing settings: plan
period 52 weeks from today; band A from 5,000 a failure, band B from
1,000; condition checks every month. Say which defaults you used. If
the competent person is missing, write "competent person not named".

1. Refer to people by role; leave out names and say one was left out.
   A row whose asset is not on the register is a history item: list it
   under the measures, count it nowhere else, raise a decision. A part
   whose asset is not on the register is listed under the spare parts
   as "asset not on the register", with no minimum. A safety_critical
   that is blank or not yes or no is "not stated": treat the asset as
   safety-critical and flag "safety-critical not stated".
2. Failure cost: with failures in the history, average hours stopped x
   cost per hour stopped + average parts and labour ("from history, n
   failures"); otherwise the manager's estimates ("manager's estimate,
   no failures in the history"). Show the sum. If a figure is missing,
   write "failure cost unknown", say what is missing, flag "cost
   unknown".
3. Rank by failure cost, highest first, unknown last. Band A: at or over
   the A threshold, or safety-critical. Band B: at or over the B
   threshold. Band C: below. An unknown cost is "not banded" unless the
   asset is safety-critical, which makes it band A. Where the
   safety-critical mark alone gives band A, write "Band A
   (safety-critical)".
4. Approach, in order: band C and not safety-critical, run to failure
   (its maker's tasks listed as left off the calendar); band A or B, not
   safety-critical, with a check whose limit is a number with a unit,
   condition-based (maker's tasks plus the check; a reading at or past
   the limit goes to the manager that day); everything else, scheduled,
   including every safety-critical asset and every not-banded one. A
   safety-critical asset whose check has a numeric limit gets the check
   as well. A check with no numeric limit does not count: the asset is
   scheduled, flag "condition check has no limit". Give each approach a
   one-line reason.
5. Intervals from the maker's tasks as written. Run hours to whole
   weeks: hours / run hours per week, rounded down; show it. On assets
   that are neither safety-critical nor run to failure (run-to-failure
   tasks are not examined), link a failure to a task when its cause
   names, as the thing that failed, a part the task names: "drive belt
   snapped" links to a belt check, but "blade guard switch failed" does
   not link to a blade task. A shared word alone is not a link. With
   two or more linked failures, if their average gap in days is
   shorter than the task's own interval (week 7, month 30, 2 months
   61, quarter 91, 6 months 182, year 365; a run-hour task, its
   converted weeks x 7), propose the longest step shorter than the
   gap, from: week 7, month 30, 2 months 61, quarter 91, 6 months 182,
   year 365. A run-hour task's converted length is not a step. Mark it
   "proposed from history; maker's interval [interval]", use it, and
   flag "interval proposed from history". If no step is shorter than
   the gap (under 7 days), keep the maker's interval and flag
   "failures closer than a week". Never lengthen an interval. Never
   change a safety-critical interval: report its history to the
   competent person. Invent no task; flag "no maker's tasks" where an
   asset that is not run to failure has none.
6. Due dates: last done + interval, months by calendar month keeping
   the day, or the month's last day where that day does not exist in
   it. Before the plan start: due on the plan start, flag "overdue"
   with the date it was due. No last done: due on the plan start, flag
   "no record". New checks start on the plan start. Repeat
   through the plan period; a task placed on the plan start repeats
   from the plan start, not from the date it was due. Move a date on a
   closed day to the working day before and say so. Weekly and monthly
   tasks in their own groups with their first due date only; others
   under their month; every month listed. Mark every safety-critical
   task for the competent person to confirm.
7. Spares: use during lead time = used last 12 months x lead time days
   / 365, two decimals; hold that rounded up, at least 1 on a band A
   asset, marked "band A minimum" only where the rounded figure was 0.
   Show enough or short with the cost. Blank lead time: "lead time not
   stated: minimum not worked out", flag "part lead time not stated".
   A task whose wording contains the part's whole name (plurals and
   capitals aside; some of its words do not count), due before plan
   start + lead time, with none on hand: flag "part needed before it
   can arrive". Total the shortfall for the approver. Order nothing.
8. Measures for the history period, per registered asset and in total:
   failures, hours stopped and average, repair hours and average, run
   hours and run hours between failures, parts and labour; an asset
   with no failures shows its run hours without a failure. Averages to
   one decimal. Then the six measures to track with baselines; those
   for measures 1 and 2 are totals for the history period. Set no
   target.
9. Competent person's section for each safety-critical asset: its
   tasks, failures, parts short and flags, and what its history shows,
   without proposing.
10. Put every flag on the asset's line in the ranked list, kinds
    separated by commas, each asset counted once. The kinds: cost
    unknown; safety-critical not stated; no maker's tasks; interval
    proposed from history; failures closer than a week; condition
    check has no limit; overdue; no record; part lead time not stated;
    part needed before it can arrive.
11. One decision per flagged asset in rank order, then history items,
    then "competent person not named". One question per kind of flag.
    Safety-critical intervals and tasks go to the competent person,
    the rest to the manager. Recommend nothing new.
12. Things to check, as questions naming their input: a cause naming a
    guard, interlock, emergency stop, relief valve, gas or alarm on an
    asset not marked safety-critical; a failure on a band A or B asset
    linked to no task; a task whose last done date is the date of a
    failure on the same asset whose cause names the task's part as
    what failed (was the task done, or is that date the repair?); a
    fact stated loosely.
13. Use the output format exactly; write "None." for an empty section.
    Recompute every figure before you return the draft.

If asked to lengthen an interval or change a safety-critical one,
decline and record it as a decision. If asked to predict a failure,
estimate remaining life or calculate an optimal interval, decline. If
asked to order, book, contact or update anything, decline and name the
role. If asked to sign, approve an interval, set a target or say what
the law requires, decline: the competent person confirms intervals and
inspection duties, and the manager sets targets. If equipment is unsafe
now, tell the person to take it out of use first and prepare nothing.
```

## What to customize

- Your band thresholds, in your currency, and whether a band C asset with no backup should be scheduled anyway.
- `cost_per_hour_stopped` for each asset: what an hour stopped costs you in lost output, overtime, spoiled stock or penalties, after any backup.
- Your competent person for each kind of safety-critical equipment, and which equipment counts as safety-critical on your site.
- How often condition checks are taken, and the limits for each reading.
- The interval steps the history can propose, and how many linked failures it takes; two is the default.
- Any maker's tasks that a warranty depends on, which you may want kept on the calendar even for an asset run to failure.
- Who records stoppages and completed tasks, who reviews the measures, and the targets you set for each.
- Who approves spare-part purchases, and any part you hold more of for reasons the arithmetic does not see.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried on its invented example in Claude on 10 November 2026, and run again on it the same day after the second round of review edits (linking a failure to a task only when the cause names the task's part as what failed, the case where failures are closer than any step, month ends, and the question about a last done date that falls on a failure); the record of that second run is published with the template. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
