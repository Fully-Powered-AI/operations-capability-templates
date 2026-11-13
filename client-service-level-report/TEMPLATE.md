# Client service level report

Workflow template, version 0.1.0.

## Purpose

Prepare the service level report a client contract calls for, for one contract and one reporting period. Each service level in the contract's schedule is measured from the service records the business supplies, shown with its working and marked met, missed, no events or not measured this period. Every miss is explained by the records behind it, in the record's own cause note. The credits the contract states for each miss are listed for a person to confirm: worked out only where the contract gives a plain percentage of a named fee or a fixed amount, and otherwise quoted and located. Claimed exclusions, corrective actions and every open question sit beside them. The assistant prepares; it never decides what the contract means, whether an exclusion holds or whether a credit is owed, never offers, applies or invoices a credit, never sends the report to the client and never changes a record.

## When to use it and when not to

Use it at the end of each reporting period a client contract sets, usually monthly, once the period's records are closed and exported, and before the report is due to the client. Run it again after the service delivery manager has answered the questions, to produce the version that is approved and kept.

Do not use it:

- to set or change service levels, or to decide what a service level in the contract means. The service delivery manager sets out the schedule once, from the contract, and the commercial owner of the contract checks it; this workflow template reads that schedule and nothing else;
- for a general update on how the client's work is going, its dates and its open decisions. That is a client status update, a separate piece of work;
- for the status of an internal project, its workstreams and its blockers. That is a project status report;
- for the business's own internal measures, which no client contract sets. Those belong in an operations scorecard;
- to decide whether a credit is owed, to argue a dispute about the contract with the client, or to answer whether the business is in breach. Those questions go to the commercial owner of the contract, and to the business's lawyer if it has one;
- when the period's records have not been closed, or when the records were exported before the period ended.

## Roles

- **Runs it:** the service delivery manager, or the account manager or a service coordinator preparing it for them.
- **Sets out the service level schedule from the contract, and answers the questions:** the service delivery manager.
- **Checks the schedule against the contract, and settles what the contract means:** the commercial owner of the contract, as the business names it.
- **Confirms each exclusion claimed in the records:** the service delivery manager.
- **Confirms whether each credit applies and how much, before it is raised with the client:** the service delivery manager with the role named in the settings, such as the finance lead.
- **Owns each corrective action:** the role named on the action list.
- **Decides what the client receives, approves the report and sends it:** the account manager, or whoever the business names.

## Inputs

1. **The service level schedule,** one row per service level, written by the service delivery manager from the contract. Default column headers: `sl_id, service_level, type, target, better, measurement_period, service_minutes, excluded_reasons, credit_form, credit_value, credit_base, credit_terms, contract_ref`.
   - `type` is one of: `on-time` (a share of records done by their due time, such as responses, resolutions, deliveries or reports), `availability` (a share of service minutes without an outage), or `supplied` (a figure measured in another system and supplied as it stands, such as a satisfaction score).
   - `target` is a number: a percentage for `on-time` and `availability`, the measure's own unit for `supplied`. `better` is `higher` or `lower`; `on-time` and `availability` are always `higher`.
   - `measurement_period` is `month` or `quarter`.
   - `service_minutes`, for `availability` only, is `24x7` or blank. Blank means the settings give the service minutes for the period.
   - `excluded_reasons` lists, separated by semicolons, the reasons the contract allows a record or an outage to be left out of the count, in the schedule's own words, such as `awaiting client` or `planned maintenance`. Blank means none.
   - `credit_form` is `percent of fee`, `fixed amount`, `other` or `none`. `credit_value` is the percentage or the amount. `credit_base` names the fee a percentage is taken of, such as `monthly service fee`. `credit_terms` is the contract's credit wording, copied as written. `contract_ref` locates the service level in the contract, such as `Schedule 3, paragraph 2.1`.
   If there is no schedule, stop and ask for it; never read service levels out of the contract yourself. If a header does not match, stop, show the expected and the found headers, and ask which column is which. Two rows with the same `sl_id`: stop and ask.
2. **The service records** for the period: tickets, incidents, orders, deliveries or reports, one row each. Default column headers: `record_id, sl_id, opened, due, done, excluded_reason, cause_note`. `due` is the due time the business's own system set under the service level; `done` is when the thing the service level measures happened, blank if it has not. Times are written `YYYY-MM-DD HH:MM`. Needed when the schedule has an `on-time` service level. If missing, stop and ask. If a header does not match, stop and ask, as for the schedule.
3. **The outage log** for the period. Default column headers: `outage_id, sl_id, start, end, excluded_reason, cause_note`. Needed when the schedule has an `availability` service level; if missing, stop and ask. An outage with no `end` is still running: stop and ask for the time to count it to. If a header does not match, stop and ask.
4. **Supplied figures,** for `supplied` service levels. Default column headers: `sl_id, value, source, as_of`. If one is missing, mark that service level NOT MEASURED, write "figure not supplied" and ask for it.
5. **The action list:** corrective actions agreed for this contract. Default column headers: `action_id, sl_id, action, owner, due, status`. Status is the business's own, such as Open, In progress, Done or Closed. If missing, continue and write "action list not supplied" in the header and under Corrective actions.
6. **Last period's results,** from the previous report. Default column headers: `sl_id, period, result, status`, with the period written `YYYY-MM`. If missing, continue and write "not supplied" in each line's last-period slot.
7. **The settings:** the client and the contract, with the version or date of the schedule it was written from; the report period; the date and time the records were exported; today's date; the one time zone all times are in; the roles named under Roles; each fee a credit is taken of, with its amount and currency for the period; any cap on credits as the contract states it, with its reference; the service minutes for any `availability` service level whose `service_minutes` is blank; and the quarter ends, if the contract's quarters are not calendar quarters. If the period, the export time or the time zone is missing, stop and ask. If the export time is before the end of the period, stop: the records are not complete.

The assistant works only from what the person supplies. It needs no access to any system and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm the headers of every input against the defaults; on a mismatch, stop as set out under Inputs. Confirm every time can be read and is in the settings' time zone; if not, stop and ask. Two rows with the same `record_id` or `outage_id`: stop and ask which is right. A record whose `due` or `done` is earlier than its `opened`, or an outage whose `end` is earlier than its `start`: stop and ask. For each service level, check the row is complete for its type: a `target`; a `better`; for `availability`, service minutes from the schedule or the settings; for `percent of fee`, a `credit_value` and a `credit_base` the settings give an amount for. A service level whose row cannot be measured as written is marked NOT MEASURED, with the reason and a question.
2. **Decide what is measured this period.** A service level measured each month is measured in every report. A service level measured each quarter is measured only in the report whose period ends a quarter (calendar quarters unless the settings say otherwise); in any other report it is marked NOT MEASURED, "measured each quarter; due in the report for [month year]".
3. **Measure each on-time service level.** Take the records with its `sl_id` whose `due` falls inside the period; for a service level measured each quarter, inside the quarter, which means the records export must cover the whole quarter (if it covers only the report month, stop and ask). A record whose `due` falls after the period is left out and counted under Records left out; it belongs to a later report. A record with an `sl_id` the schedule does not list is left out, listed under Records left out, and gets a question. Of the records due in the period:
   - a record with an `excluded_reason` that appears in that service level's `excluded_reasons` is left out of the count and listed under Exclusions claimed, for the service delivery manager to confirm;
   - a record with an `excluded_reason` that does not appear in the list is counted as any other record, listed under Exclusions claimed as "not on the schedule's list; counted", and gets a question; if that record is missed, the same line gives its due time, its done time or "still open", how late it is and its `cause_note` as written, because no other section shows a missed record under a service level that is met;
   - a counted record is met when `done` is at or before `due`, and missed when `done` is after `due` or blank.
   The result is met records ÷ counted records × 100. With no counted records, mark the service level NO EVENTS; it is neither met nor missed.
4. **Measure each availability service level.** Service minutes are the days in the period × 1,440 when `service_minutes` is `24x7`, or the figure in the settings. Count only the minutes of each outage that fall inside the period; when an outage crosses the start or the end of the period, give the minutes inside it and the minutes left out. An outage whose `excluded_reason` appears in the service level's `excluded_reasons` is left out of the count and listed under Exclusions claimed; one whose reason is not on the list is counted, listed and gets a question. The result is (service minutes − counted outage minutes) ÷ service minutes × 100. The downtime the target allows is service minutes × (100 − target) ÷ 100.
5. **Take each supplied figure as it stands.** Show the value, its source and its date, and say it was supplied, not recomputed.
6. **Rate each service level.** Round an on-time result to one decimal place and an availability result to two. Compare the unrounded result with the target: when `better` is `higher`, MET at or above the target and MISSED below it; when `lower`, MET at or below and MISSED above. If rounding would show a missed result as equal to the target, add decimal places until it does not, so the figure on the page never reads as met when it is missed.
7. **Show what each claimed exclusion changes.** For every exclusion left out under steps 3 and 4, work out the result as if it were counted. If the status would change, show both results, mark the service level "met only with a claimed exclusion" in the Overall line, and raise a question. The Overall line still counts that service level as met, and lists its id after the counts so that no one reads the count alone. If it would not change, show the other result under Exclusions claimed and raise no question.
8. **Explain each miss from the records.** For each MISSED service level: for on-time, how many more records done by their due time would have met the target, the smallest whole number that does it; for availability, how many minutes more than the allowed downtime were counted (counted minutes − allowed minutes), with both figures shown. Then list every missed record (its `record_id`, due time, done time or "still open", and how late, in minutes when under two hours, otherwise in hours and minutes) or every counted outage (its `outage_id`, start, end and minutes counted), each with its `cause_note` exactly as written. If a note names a person, quote it with the name replaced by that person's role in square brackets, such as "[on-call engineer]", or "[a named person]" when the role is not stated, and tell the person to remove the name from the source. With no cause note, write "cause not recorded" and raise a question. Never supply a cause of your own, and never draw one from the records that the note does not state. For a supplied figure, the miss is explained only by what its source says; if nothing is supplied, write "no explanation supplied" and raise a question.
9. **List the credits that may apply.** For each MISSED service level, by its `credit_form`:
   - `percent of fee`: `credit_value` % × the amount of the `credit_base` fee in the settings, with the working. If the settings give no amount for that fee, write "amount not worked out: [fee] not supplied" and raise a question;
   - `fixed amount`: the `credit_value`, with its currency;
   - `other`: do not work it out. Write "not worked out; for the [role confirming credits] to work out", quote `credit_terms` as copied, give the `contract_ref` and raise a question. Contract wording that steps, rounds or escalates is read by a person, never by the assistant;
   - `none`: write "no credit stated in the schedule".
   For a service level met only with a claimed exclusion, list the credit that would apply if the exclusion is not confirmed, marked "only if the exclusion of [id] is not confirmed", and keep it out of the main total. Total the worked-out credits, and separately the total including those marked "only if". If the settings give a cap as a percentage of a named fee or as an amount, work out the cap and say whether each total is within it; if any credit is not worked out, say the cap check is incomplete. A cap in any other form is quoted, not applied. Mark every credit "may apply; to be confirmed by the service delivery manager with the [role confirming credits]". Never say a credit is owed, never offer one and never net one off an invoice.
10. **Match each miss to corrective actions.** For each MISSED service level, list every action on the action list with its `sl_id`, with owner, due date and status, and OVERDUE when the due date is before today and the status is not Done or Closed. A missed service level with no action still open (every action is Done or Closed, or there is none) is shown "No open action recorded" and gets a question. Report a status only as supplied. Never propose an action unless the service delivery manager asks for options to discuss; then list them under the question, marked "for discussion, not agreed", and never on the action list.
11. **Compare with last period.** For each service level, give last period's result and status from the previous report. When a service level is MISSED this period and was MISSED last period, add "missed two periods running".
12. **Write the questions,** numbered, for the service delivery manager: each record or outage for a service level not on the schedule; each exclusion claimed with a reason not on the list; each exclusion a status depends on; each miss with no cause recorded; each credit not worked out, and an incomplete cap check; each missed service level with no open action; each overdue action; each service level not measured because its row or its figure is missing. Give the facts, then the question. Recommend nothing unless asked.
13. **Return the draft** to the person who ran it, for the service delivery manager's review. A person decides what the client receives and sends it.

## Exceptions and stop conditions

- **No schedule, a header that does not match, two rows with the same id, a time that cannot be read, or a done or end time before its start:** stop, show what was found, and ask.
- **Records exported before the period ended, or no time zone given:** stop and ask; a report built on part of the period would be wrong.
- **Only the contract is supplied, with no schedule:** stop and ask the service delivery manager for the schedule. Do not read service levels, exclusions or credits out of the contract and use them.
- **The records and the schedule disagree about what a service level measures,** such as resolution times exported for a service level the schedule describes as response: stop and ask which is right.
- **Asked what the contract means, whether the business is in breach, whether a credit is owed, or whether to dispute a client's claim:** decline; record it as a question for the commercial owner of the contract. This workflow template gives no legal advice.
- **Asked to leave out a record or an outage, to treat a reason as excluded when it is not on the schedule's list, to round a result up, or to call a missed service level met:** decline, and show the working.
- **Asked to work out a credit whose form is `other`, or to apply a cap written in another form:** decline to work it out; quote the wording and its reference for the person confirming credits.
- **Asked to send the report, offer or apply a credit, or change a record or a status:** decline; a person approves and does each of these.
- **A record or a note names a client's employee, a member of the business's staff, or holds personal details, bank details, a password or a login code:** do not repeat the personal or account details; refer to people by role only (in a cause note, replace the name with the role as step 8 sets out), and tell the person to remove such details from the source. Never rate or blame an individual for a miss.

## Output format

```
CLIENT SERVICE LEVEL REPORT: [client], [contract], [period]

For: [service delivery manager role]. Prepared [weekday date] from the service level schedule ([n] service levels, written from [contract and version or date]); [record files, each with its number of rows], as exported [date time] ([time zone]); supplied figures ([n] / none needed / not supplied); the action list ([n] actions / action list not supplied); last period's results ([month year] / not supplied).
Overall: [n] met, [n] missed, [n] no events, [n] not measured this period.[ Met only with a claimed exclusion: [ids].]

Performance by service level
[sl_id] [service level] ([contract_ref]): [result / no result this period] against a target of [target] ([higher / lower] is better). [MET / MISSED / NO EVENTS / NOT MEASURED: reason]. Last period ([month year]): [result], [status] / not supplied.[ Missed two periods running.]

How each result was worked out
[sl_id]: [met] met of [counted] counted = [result]. From [file]: [n] rows for [sl_id], [n] due in the period[, [n] excluded ([ids])][, [n] due after the period ([ids])].
[sl_id]: service minutes [days] × 1,440 = [n] / [n] as set in the settings. Counted outage minutes [a] + [b] = [n]. ([service minutes] − [counted]) ÷ [service minutes] × 100 = [result]. Downtime the target allows: [n] minutes.[ Excluded: [ids], [n] minutes.]
[sl_id]: [value], as supplied: [source], [as_of]. Not recomputed.
[sl_id]: not measured: [reason].

Misses and what the records show
[sl_id] [service level]: [result] against [target]. Short by: [n more records on time would have met the target ([met + n] of [counted], [result]) / [n] minutes more downtime than the target allows ([n] counted, [n] allowed)].
  [record_id], due [date time], done [date time / still open], [lateness] late: [cause note as written / cause not recorded].
  [outage_id], [start] to [end], [n] minutes counted[ ([n] fell outside the period)]: [cause note as written / cause not recorded].
/ No service level was missed.

Exclusions claimed
[id] ([sl_id]), "[reason]"[, [n] minutes]: on the schedule's list; left out, to be confirmed. Without the exclusion, [sl_id] would be [result], [status].[ The status depends on it. See question [n].]
[id] ([sl_id]), "[reason]": not on the schedule's list; counted[ as missed, due [date time], done [date time / still open], [lateness] late: [cause note as written / cause not recorded]]. See question [n].
/ No exclusions were claimed.

Credits that may apply, to be confirmed by the service delivery manager with the [role confirming credits]
[sl_id], missed: [credit_value]% of the [credit_base] ([contract_ref]): [credit_value]% × [fee amount] = [credit]. May apply.
[sl_id], missed: [fixed amount] ([contract_ref]). May apply.
[sl_id], missed: not worked out; for the [role confirming credits] to work out. The schedule copies the contract's terms ([contract_ref]) as: "[credit_terms]". See question [n].
[sl_id], missed: no credit stated in the schedule.
[sl_id], only if the exclusion of [id] is not confirmed: [working] = [credit].
Total worked out: [amount][; [amount] including credits marked "only if"]. Cap ([reference]): [working] = [cap]; [the total is / both totals are] [within / above] the cap[; the cap check is incomplete because [sl_id] is not worked out / the cap is quoted, not applied: "[wording]"].
/ No service level was missed, so no credit is listed.
No credit has been offered, applied or invoiced.

Corrective actions
[sl_id]: [action_id] [action], owner [role], due [date], [status as supplied][, OVERDUE. See question [n]].
[sl_id]: No open action recorded. See question [n].
/ No service level was missed. / Action list not supplied.

Records left out
[file]: [n] rows due after the period ([ids]); [n] rows for service levels not on the schedule ([ids], see question [n]); [outage_id]: [n] of its [n] minutes fell outside the period.
/ None.

Questions for the [service delivery manager role]
[n]. [The facts.] [The question.]
/ None.

Draft for the [service delivery manager role]'s review. Every result traces to the records named above. Nothing has been sent to the client, no credit has been offered or applied, and no record has been changed.
```

Write dates in words, such as "14 October 2026" and "14 October 2026 02:40". Keep an export's own form only when naming a row in it, as in "the row for 2026-09". Amounts keep the currency given in the settings.

## Reviewer checklist

1. Every service level on the schedule appears once, with its target, type and reference as the schedule gives them, and the schedule matches the current contract. (Commercial owner of the contract)
2. Every result can be recomputed from the records with the working shown, and no missed result is rounded to look met. (Service coordinator)
3. Every record due in the period is counted, excluded or listed as left out, and the counts add up to the rows in each file. (Service coordinator)
4. Every exclusion is one the schedule allows and the records support, and every status that depends on one has been confirmed. (Service delivery manager)
5. Every cause given for a miss is the record's own note, or says none was recorded. (Service delivery manager)
6. Every credit is worked out only from the schedule and the fees supplied, and every credit not worked out quotes the contract's wording and reference. (Finance lead)
7. Every miss has an open corrective action, or a question asking for one. (Service delivery manager)
8. No individual is named, rated or blamed. (Account manager)
9. The report is approved, and what the client receives is decided, before anything is sent. (Account manager)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary month.** Five service levels, all records present, nothing missed. Expected: every result worked out and MET; Misses, Credits and Corrective actions print their "none" lines.
2. **Exactly on target.** 9 met of 10 counted against a target of 90.0%. Expected: 90.0%, MET.
3. **Rounding would hide a miss.** Availability of 99.496% against a target of 99.5%. Expected: shown as 99.496%, not 99.50%, and MISSED.
4. **Renamed column.** A records export headed `resolved_at` in place of `done`. Expected: stops, shows the expected and the found headers, and asks; nothing drafted.
5. **Exclusion on the list that changes the status.** Expected: excluded, both results shown, "met only with a claimed exclusion" in the Overall line, a question, and the credit listed as "only if the exclusion is not confirmed".
6. **Exclusion reason not on the list.** Expected: counted, listed as "not on the schedule's list; counted", and a question.
7. **Outage crossing the start of the period.** 50 minutes, 30 of them before the period. Expected: 20 minutes counted, 30 listed as outside the period.
8. **Record still open and past due.** `done` blank, due in the period. Expected: counted as missed, shown "still open".
9. **Record due after the period.** Expected: left out, listed under Records left out, not counted as missed.
10. **Credit in another form.** A stepped credit for each tenth of a percent below target. Expected: not worked out; the wording and reference quoted; a question.
11. **No cause note on a missed record.** Expected: "cause not recorded" and a question; no cause supplied by the assistant.
12. **Records exported before the period ended.** Expected: stops and asks.
13. **Asked whether the credit must be paid.** Expected: declines, and records the question for the commercial owner of the contract.
14. **Quarterly service level in a month that does not end a quarter.** Expected: NOT MEASURED, with the month of the report it is due in.

## Instructions for the AI assistant

```
You prepare the service level report for one client contract and one
reporting period, for the service delivery manager. You prepare; people
decide. You never decide what the contract means, whether an exclusion
holds or whether a credit is owed. You never offer, apply or invoice a
credit, send the report to the client, change a record or a status, or
propose a corrective action unless asked. You never ask for a password
or a login code and need no access to any system.

The user will supply: the service level schedule (sl_id, service_level,
type, target, better, measurement_period, service_minutes,
excluded_reasons, credit_form, credit_value, credit_base, credit_terms,
contract_ref); the service records (record_id, sl_id, opened, due, done,
excluded_reason, cause_note); the outage log (outage_id, sl_id, start,
end, excluded_reason, cause_note); supplied figures (sl_id, value,
source, as_of); the action list (action_id, sl_id, action, owner, due,
status); last period's results (sl_id, period, result, status); and the
settings: client, contract and schedule version, period, export time,
today, time zone, roles, fee amounts, any credit cap, service minutes
where needed, quarter ends. If there is no schedule, stop and ask; never
read service levels out of the contract yourself. If a header does not
match, stop, show expected and found, and ask; never guess a column. If
the records or outage log a service level needs are missing, if the
period, export time or time zone is missing, if the export time is
before the period ends, if an id repeats, if a time cannot be read, if a
done or end time is before its start, if an outage has no end time, or
if the records and the schedule disagree about what a service level
measures, stop and ask. If
the action list or last period's results are missing, say so and
continue.

1. Measure monthly service levels in every report; quarterly ones only
   in the report whose period ends a quarter, otherwise NOT MEASURED
   with the month of the report they are due in. A row that cannot be
   measured as written: NOT MEASURED, with the reason and a question.
2. On-time: records for the sl_id with due inside the period (a
   quarterly service level: inside the quarter, so the export must cover
   the quarter; if it does not, stop and ask). Due after
   the period: left out, listed. sl_id not on the schedule: left out,
   listed, question. excluded_reason on the service level's list: left
   out, listed for confirmation. Reason not on the list: counted,
   listed, question; if that record is missed, its line under
   Exclusions claimed gives due, done, lateness and its cause_note. Met
   when done is at or before due; missed when done is later or blank.
   Result = met / counted x 100. None counted: NO EVENTS.
3. Availability: service minutes = days x 1,440 for 24x7, else from the
   settings. Count only outage minutes inside the period; show minutes
   outside it. Exclusions as in step 2. Result = (service minutes -
   counted minutes) / service minutes x 100. Allowed downtime = service
   minutes x (100 - target) / 100.
4. Supplied: show value, source and date; say it was not recomputed.
   If the figure is missing: NOT MEASURED, "figure not supplied", and
   ask for it.
5. Rate on the unrounded result: higher is better, MET at or above
   target; lower is better, MET at or below. Round on-time to one
   decimal and availability to two; if rounding would show a miss as
   equal to the target, add decimal places until it does not.
6. For each exclusion left out, work out the result as if counted. If
   the status changes, show both, add the id to "met only with a
   claimed exclusion" (the Overall line still counts it as met) and
   ask. If it does not change, show the other result under Exclusions
   claimed and ask nothing.
7. For each miss: how many more on time would have met the target, or
   how many minutes more than the allowed downtime were counted (show
   both figures); then each missed record or counted outage with its
   cause_note exactly as written, or "cause not recorded" and a
   question. A missed supplied figure is explained only by what its
   source says; if nothing is supplied, "no explanation supplied" and a
   question. Show lateness in minutes under two hours, otherwise in
   hours and minutes. If a note names a person, quote it with the name
   replaced by the role in square brackets, such as "[on-call
   engineer]", and tell the user to remove the name from the source.
   Never give a cause of your own.
8. Credits, for each miss: percent of fee = credit_value % x the fee
   amount in the settings, with the working; fixed amount as given;
   other = "not worked out; for the [role confirming credits] to work
   out", quote credit_terms with contract_ref, and ask; none = "no
   credit stated in the schedule". For a status that depends on an
   exclusion, list the credit "only if the exclusion of [id] is not
   confirmed", outside the main total. Total; apply a cap only if it is
   a percentage of a named fee or an amount, and say the check is
   incomplete if any credit is not worked out. Mark every credit "may
   apply; to be confirmed". End the section with "No credit has been
   offered, applied or invoiced."
9. Corrective actions for each miss: every action for the sl_id with
   owner, due and status as supplied, OVERDUE if due before today and
   not Done or Closed. No action still open (all Done or Closed, or
   none): "No open action recorded" and a question. If asked for options, list them
   under the question marked "for discussion, not agreed".
10. Last period's result and status for each; "missed two periods
    running" where both are MISSED.
11. Questions, numbered, facts first, for the service delivery manager.
    Recommend nothing unless asked.
12. Use the output format exactly, every section in order. Where a
    section is empty, print its "none" line. Records left out lists
    rows due after the period, rows for service levels not on the
    schedule and any outage minutes outside the period. Write dates in
    words. End with the draft line saying nothing has been sent, no
    credit offered or applied and no record changed.

If asked what the contract means, whether the business is in breach or
whether a credit must be paid, decline and record it as a question for
the commercial owner of the contract. If asked to leave out a record,
widen an exclusion, round a result up or call a miss met, decline and
show the working. Refer to people by role only and never blame an
individual for a miss. Do not repeat personal or bank details, a
password or a login code found in an input; tell the user to remove
them. Check every figure against its working before you return the
draft.
```

## What to customize

- The service level schedule for each contract: written once by the service delivery manager from the contract, checked by the commercial owner of the contract, and updated whenever the contract changes.
- Your export column headers, if your ticketing, monitoring or delivery systems name them differently.
- The time zone and the business hours your systems use to set due times; the template reads the due time your system sets and does not recalculate it.
- The fees each credit is taken of, and the credit forms your contracts use. As written, only a plain percentage of a named fee and a fixed amount are worked out.
- The roles: who runs it, who confirms exclusions, who confirms credits, and who approves and sends the report.
- Your action statuses, if you use words other than Open, In progress, Done and Closed.
- The form the client receives: this draft is for the service delivery manager; what reaches the client is the account manager's decision.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 11 November 2026. Written by Fully Powered AI from its own published map of the work. Editorially reviewed. One run on the invented example was made in Claude on 11 November 2026, and its record is published beside the example. After the first run the instruction block, the output format and the example were revised, and the recorded run is the second, on the revised text. After that run, five small clauses were added to the instruction block (quarterly counting, an outage with no end time, a missing supplied figure, an unexplained supplied miss, the wording of the open-action rule); the amended block has not been run. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
