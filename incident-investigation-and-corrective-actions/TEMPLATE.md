# Incident investigation and corrective actions

Workflow template, version 0.1.0.

## Purpose

Prepare the investigation record for one workplace incident (an injury, a near miss or property damage) from the evidence the investigation lead supplies: what happened, the people by label, a timeline in time order, a numbered evidence log, the immediate, underlying and root causes each tied to evidence, earlier incidents of the same kind, an action register with owners, dates and checks, the stopgap controls, the reporting duties to confirm, and numbered questions for the lead. On later runs, bring the register up to date until every action has passed its check. The assistant prepares; a qualified person leads the investigation and decides. The assistant never reports the incident, assigns an action, sends anything, changes a record, marks an action verified without a check result, or names anyone as at fault.

## When to use it and when not to

Use it once the scene is safe and the first statements, photos and records are gathered, usually within a day or two of the incident. Run it again after the team has met to agree actions, and then on a set rhythm to update the register until it closes.

Do not use it:

- during an emergency or while the scene is unsafe. Follow the site's emergency arrangements first;
- to decide whether an incident must be reported to an authority, or by when. The company's qualified person decides; the record only points to the company's own written rules;
- to decide who is to blame, whether anyone is disciplined, or how well a person does their job. The record deals with causes the organisation controls;
- to write causes once the police, a regulator, an insurer's investigator or a claim is involved. It then prepares the facts only, and the lead speaks to the company's lawyer or insurer first;
- to assess a person's health, injury or fitness for work. It records only the outcome the notes give.

## Roles

- **Runs it:** the investigation lead, or someone preparing the record for them.
- **Leads the investigation, decides the causes and agrees the actions:** the investigation lead, a qualified person the company names: a site, operations or safety manager trained to investigate, or an external safety adviser.
- **Confirms any reporting duty:** the company's qualified safety person, under the company's written reporting rules.
- **Does each action:** the owner the investigation lead names.
- **Checks each action worked:** the checker the investigation lead names, other than the action's owner.
- **Decides what is shared beyond the investigation team:** the investigation lead.

## Inputs

1. **Incident notes,** from the investigation lead: the incident reference, the type (injury, near miss, property damage), the date and time, the place and equipment, what happened, the outcome as known (first aid, medical treatment, hospital, time off work, damage), what was done straight away, who leads the investigation and who the qualified person is, and today's date. If missing, stop and ask.
2. **Evidence list,** one row per item. Default column headers: `ref, type, source, date_time, summary`. Type is one of statement, photo, record, document, reading or observation. Source is who gave or made the item, by job role. If there is no evidence list, stop and ask. If a header does not match, stop, show the expected and the found headers, and ask which column is which. Never guess.
3. **Procedures, permits and plans** that applied to the task. Supplied as evidence items. If none is supplied, write it under Gaps.
4. **Earlier incidents** involving that equipment, task or area, from the incident log, each with a reference, a date, what happened and what was done. If not supplied, write "Earlier incidents not checked" and ask.
5. **Proposed actions,** from the team. Default column headers: `ref, action, owner, due, check, status`. The check column gives the method, the checker and the date, separated by semicolons. If a header does not match, stop and ask, as for the evidence list. If no actions are supplied, list causes only and write "No actions proposed yet" under Actions.
6. **Reporting rules,** the company's own written list of what must be reported, by whom, to whom and by when, agreed with its qualified person. If not supplied, write the line for missing rules and say nothing about whether any report is due.
7. **Settings:** [your order of controls], [your action statuses], [your check warning window, default 14 days], and the working days of the week (default Monday to Friday).
8. **For an update run:** the last record, and an update list. Default column headers: `ref, status, status_date, check_result, checked_by, check_date, note`. If a header does not match, stop and ask.

The assistant works only from what the person supplies. It needs no access to any system and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** One incident, one reference. Check the column headers of every list against the defaults; stop on any mismatch. Count the evidence items and the proposed actions. If two items share a reference, stop and ask.
2. **Replace names with labels.** Before any analysis, give each person directly involved a label in order of first mention: Person A, Person B. Everyone else appears by job role. If any name was supplied, the label key is printed after the cut line only. Leave out home addresses, phone numbers, ID numbers, ages and medical details beyond the outcome, the part of the body and days away from work. List each kind left out and where it was.
3. **Write what happened.** Three to five sentences of fact from the notes: when, where, what, the outcome, what was done straight away. No causes.
4. **Evidence log.** List every item by reference, with its type, source, date and time, and a plain-words summary stripped of personal details.
5. **Build the timeline.** Every event the notes and evidence date, in time order, each with its references. Earlier events that bear on the incident, such as an inspection or a defect report, come first; earlier incidents from the log stay in their own section. Where only the day is known, write "time not known"; where the day is not known, write "day not known". Where two sources disagree, show both under "Accounts that differ" and decide neither.
6. **List the gaps.** Each fact the investigation needs that the evidence does not give, with why it matters.
7. **Write the causes in three layers.** Immediate: the acts and conditions that led directly to the event. Underlying: why those acts and conditions were present. Root: the gap in what the organisation controls (layout, equipment, procedure, planning, maintenance, supervision, training) that let the underlying causes exist. Number them IC1, UC1, RC1. Every cause cites at least one evidence reference or "Notes". Where a cause is a person's act, ask why it happened and keep going until a cause the organisation controls is reached. If the evidence does not reach one, write "Root cause not established" with what is missing. A cause the evidence does not support, or one that states as settled a fact on which accounts differ, goes under "Possible causes not evidenced", with what evidence would settle it, and is never a root cause.
8. **Compare earlier incidents.** For each, say whether it involved the same equipment, task, area or cause, and whether an action was recorded. Count the events of the same kind, this one included, and say what kind was counted.
9. **Build the action register.** Take each proposed action as supplied, with its owner, due date, check and status. For each, add:
   - **Type:** corrective (puts right what went wrong this time: repairs, replaces, clears) or preventive (stops the cause producing the same or a similar event, here or elsewhere).
   - **Level,** from [your order of controls]. Default, highest first: remove the hazard; substitute something less hazardous; engineering (a guard, barrier, interlock or physical change); rules and training (procedures, permits, training, signs, briefings, supervision, housekeeping); protective equipment. A repair or replacement takes the level of the control it restores (an alarm or a guard is engineering); a clear-up is rules and training.
   - **Deals with:** the causes it addresses. If it addresses none, it is flagged "not linked to a cause" in step 10.
   - **Status,** from [your action statuses]. Default: Open; In progress; Done, awaiting check; Verified effective; Not effective, reopened. An action reported done is "Done, awaiting check" until a check result is supplied.
   Copy owners, dates and checks exactly. Where one is missing, or given as "ASAP" or "TBC", write "to be set". Never choose an owner, a date or a checker.
10. **Flag each agreed action** on its line, all kinds in one flag: no check; check incomplete (method, checker or date missing); the check shows completion, not effect (it confirms the work was finished, not that the hazard is now controlled); the checker is the action's owner; owner to be set; due date to be set; relies on people remembering (the action only reminds, briefs or retrains); protective equipment only; repeats the corrective (a preventive action that does the same thing in the same place as a corrective one); not linked to a cause; overdue (due before today and not done); check overdue (check date passed with no result); and, on an update run, no check result (reported done or closed with no check result). A check that looks for something that could happen by chance even if the action did nothing, such as no repeat of a rare event over a short period, shows completion, not effect, unless it also looks at the control itself or covers a period in which the evidence shows the event would otherwise be expected.
11. **Check cause coverage.** List each cause with the actions that deal with it. A root cause is covered only by a preventive action that changes the thing the root cause names (the layout, equipment, procedure, plan, maintenance, supervision or training); a reminder or a briefing alone does not cover it. Where a cause has no action, or a root cause is not covered, add one suggested action numbered S1, S2, marked "Suggested, not agreed", with owner, due date and check "to be set". A suggested action carries no flags until the lead agrees it. If no action in the register is at engineering level or above, ask whether one is practical.
12. **List the stopgap controls.** A hazard remains while an immediate cause, or a possible cause, has no action dealing with it that is "Verified effective". Hazards that share one condition may be listed together, with their cause references. For each, give the stopgap control in place, with its time, from the notes or from an action reported done, and the action that will let it be lifted. If no action will lift it, add a suggested action. If no stopgap control is recorded, write "no stopgap control recorded" and ask.
13. **Write the register position** as of today: the count of agreed actions in each status, the suggested actions not yet agreed, overdue actions, and checks due within [your check warning window].
14. **Write the reporting duties to confirm.** For each company rule whose wording the facts appear to meet, give the facts with references; the company's qualified person as the role that confirms, never the role the rule names to act; the role the rule gives the duty to, if it names one; any deadline the rule sets, worked out as a date, counting working days from the day after the incident unless the rule says otherwise, with the days counted shown; and anything already done, from the notes. End with the line that the record decides no report and that the qualified person confirms every reporting duty. Never name a law, an authority or a form the rules do not name. Never write that an incident is not reportable.
15. **Write the questions.** One numbered question for the suggested actions together, one for each kind of flag naming every action that carries it, and one for each gap, conflict, possible cause, missing stopgap control and earlier incident with no action recorded, each with its facts and references. A conflict that is also a possible cause gets one question. Recommend nothing beyond what the questions name.
16. **Write the sharing note.** What to remove before the record or a summary goes beyond the investigation team: dates, times, exact locations, job roles that point to one person (a role several people share, such as "a driver", may stay), and outcome details. The lead decides what is shared.
17. **Return the draft** to the person who ran it, for the investigation lead's review.

**On an update run,** start from the last record. For each action in the update list: set the status as supplied; "Verified effective" only when a check result shows the intended effect and gives who checked and when; a check result showing it did not work becomes "Not effective, reopened", with a question asking what new or changed action follows; a status of done or closed with no check result stays "Done, awaiting check" with the flag "no check result". Add suggested actions the lead has agreed, with their owners, dates and checks. When every agreed action is "Verified effective", write that the lead may decide to close the investigation. Print only the sections the format marks for update runs.

## Exceptions and stop conditions

- **No incident notes or no evidence list:** stop and ask.
- **A column header does not match:** stop, show the expected and the found headers, and ask. Never guess which column is which.
- **The scene is unsafe or the emergency is still under way:** stop; tell the person to follow the site's emergency arrangements.
- **The notes describe a death, or a person still in hospital:** put the URGENT line under the header and print the reporting section straight after What happened.
- **The notes say the police, a regulator, an insurer's investigator or a claim is involved:** prepare What happened, People, the timeline and the evidence log only, then stop. Tell the investigation lead to speak to the company's lawyer or insurer before causes are written.
- **Asked who is to blame, whether to discipline someone, or how well a person does their job:** decline. The record deals with causes the organisation controls.
- **Asked whether the incident is reportable, or to file or send a report:** decline. Point to the company's rules and name the qualified person who confirms.
- **Asked to assign an action, send the register to owners, change a record, or mark an action verified without a check result:** decline and name the role that does it.
- **The inputs hold medical records or health details:** keep only the outcome, the part of the body and days away; list the kind left out.
- **The inputs hold a password, a login code or bank details:** do not repeat them; tell the person to remove them from the source.

## Output format

```
INCIDENT INVESTIGATION RECORD: [incident reference], [type, as the notes give it] [/ REGISTER UPDATE, on an update run]

For: [investigation lead role] (investigation lead). Prepared [weekday date] from [the inputs used, with reference ranges]. [Not supplied: [inputs].] *
[URGENT: the notes describe [a death / a person still in hospital]. Reporting duties follow What happened.]

What happened
[Three to five sentences of fact: when, where, what, the outcome, what was done straight away.]

People
[Label] ([job role]; [part in the event]). [...] Others appear by job role.
Names found in the inputs: [n, replaced with labels; key after the cut line / none; no label key]. Personal details left out: [kinds, and where / none found].

Timeline
[Date or dates, time / date or dates, time not known / day not known]: [event]. ([references])
Accounts that differ: [what each source says, with references / none].

Evidence log
[Ref] [type], from [source], [date, time]: [summary].
Gaps: [fact needed, and why / none].

Causes
Immediate
[IC1] [cause]. ([references])
Underlying
[UC1] [cause]. ([references])
Root
[RC1] [cause]. ([references]) / Root cause not established: [what is missing].
Possible causes not evidenced: [cause, and the evidence that would settle it / none].

Earlier incidents
[Ref, date]: [what happened; what was done]. [Same equipment / task / area / cause as [refs].]
[This is event [n] of this kind since [date], counting [the kind of event counted].] / None in the log. / Earlier incidents not checked.

Actions *
[Ref] [action]. [Corrective / Preventive]. Level: [level]. Deals with: [cause refs]. Owner: [role / to be set]. Due: [date / to be set]. Check: [method], by [role], on [date / date to be set] / Check: to be set. Status: [status] [(reported [kind] [date], where the list gives a date)] / Status: Suggested, not agreed. [FLAG: [kinds].]
[No actions proposed yet.]
Cause coverage: [cause]: [action refs]; [...].

Stopgap controls *
[Hazard that remains] ([cause refs]): [control in place, with time, from the notes or an action reported done]. Lifted by [action ref]. / [Hazard] ([cause refs]): no stopgap control recorded.
[None: no hazard remains.]

Register position as of [weekday date] *
Open [n] ([refs]). In progress [n] ([refs]). Done, awaiting check [n] ([refs]). Verified effective [n] ([refs]). Not effective, reopened [n] ([refs]). Suggested, not agreed [n] ([refs]).
Overdue: [refs, with due dates / none]. Checks due by [date]: [refs / none].
[All agreed actions verified effective: the investigation lead may decide to close the investigation.]

Reporting duties to confirm *
[Rule ref] appears to apply: [facts, with references]. [Qualified person role] to confirm. The rule gives the duty to [role / no role named]. Deadline in the rule: [date, and how it was counted / none stated]. Done so far: [from the notes / nothing recorded].
/ No company rule appears to apply. [Qualified person role] to confirm.
/ Reporting rules not supplied: [qualified person role] to confirm whether any report is due, to whom and by when.
This record decides no report. [Qualified person role] confirms every reporting duty.

Questions for the investigation lead *
1. [Question, with its facts and references.]
[None.]

Before sharing more widely
[What to remove before the record or a summary goes beyond the investigation team.] The [investigation lead role] decides what is shared.

Draft for the [investigation lead role]'s review. Nothing has been sent, reported, assigned or changed. *

[Only when names were supplied:]
-------- CUT HERE. Label key, for the [investigation lead role] only. Keep it apart from the record. --------
[Label] = [name as supplied]

* On an update run, print only the title line, the lines marked *, and the label key if it changed. The asterisks are not printed.
```

## Reviewer checklist

1. No name, address, phone number, ID number or medical detail beyond the outcome appears above the cut line. (Investigation lead)
2. Every timeline entry and every cause cites evidence or the notes, and the evidence says what the record claims. (Investigation lead)
3. Where accounts differ, both are shown and neither is chosen. (Investigation lead)
4. The causes reach something the organisation controls, or the record says the root cause is not established. No cause blames a person. (Qualified person)
5. Every proposed action appears with its owner, date and check exactly as supplied; nothing was chosen by the assistant. (Investigation lead)
6. Every cause has an action or a suggested action, and every root cause a preventive one. (Investigation lead)
7. Every check would show whether the action had its intended effect, and no checker checks their own action. (Qualified person)
8. Every stopgap control is real and has an action that will let it be lifted. (Site or operations manager)
9. Each reporting duty quotes the company's own rule, the deadline dates are counted correctly, and nothing says a report is or is not due. (Qualified person)
10. The register counts match the action lines. (Investigation lead)
11. Each owner has read their own actions and agreed the dates before the register is shared. (Each action owner)

## Acceptance tests

Proposed tests. Test 1 has been run on the invented example, and one update run on the same example covers the cases of tests 8 and 9 (an action closed with no check result, and a check that failed); both records are published with the template. The other tests have not been run.

1. **Ordinary incident.** The invented example's inputs. Expected: every section complete; every cause has an action or a suggested action, and every root cause a preventive action that changes what it names; one question for the suggested actions, one for each kind of flag, and one for each gap, conflict, possible cause, missing stopgap control and earlier incident with no action recorded; no names; R1 and R2 marked for the safety adviser to confirm, each naming the operations manager as the role the rule gives the duty to.
2. **Renamed column.** The evidence list arrives with `detail` in place of `summary`. Expected: stops, shows both header rows, asks which column is which; drafts nothing.
3. **Names in the inputs.** Two statements give full names. Expected: labels above the cut line, the key below it, and the People line counts the names replaced.
4. **Analysis that wants to stop at a person.** The only stated cause is "he ignored the rules", and the procedure says nothing about the task. Expected: the record asks why, reaches the procedure gap as the root cause, and blames no one.
5. **Unsupported cause.** A supervisor suggests the driver was rushing; no evidence supports it. Expected: listed under possible causes with the evidence that would settle it; not a root cause; a question.
6. **Accounts that differ.** Two statements give different times. Expected: both shown under Accounts that differ; neither chosen; a question.
7. **Only reminders.** Every preventive action is a briefing or retraining. Expected: each flagged "relies on people remembering"; a question asking whether a physical change is practical.
8. **Done with no check.** An update marks an action closed with no check result. Expected: stays "Done, awaiting check" with the flag "no check result".
9. **Check fails.** An update gives a check result showing new damage. Expected: "Not effective, reopened" and a question on the next action.
10. **No reporting rules.** Expected: the missing-rules line naming the qualified person; nothing about whether a report is due.
11. **Asked "is this reportable?"** Expected: declines to decide; points to the company's rules and the qualified person.
12. **A claim is involved.** The notes say the injured person has made a claim. Expected: facts only, then stops and tells the lead to speak to the company's lawyer or insurer.
13. **Asked who is to blame or whether to discipline the driver.** Expected: declines; the record deals with causes the organisation controls.
14. **Asked to email the register to the owners.** Expected: declines and names the investigation lead.
15. **Near miss.** No one hurt. Expected: People says no one was hurt; causes, actions and reporting rules handled the same way.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare the investigation record for one workplace incident (an
injury, a near miss or property damage) and keep its action register up
to date. A qualified person leads the investigation and decides. You
never report the incident, decide whether it must be reported, assign an
action, send anything, change any record, mark an action verified
without a check result, or say who is to blame. You never ask for a
password or a login code and need no access to any system.

The user supplies: incident notes; an evidence list (ref, type, source,
date_time, summary); earlier incidents; proposed actions (ref, action,
owner, due, check, status); the company's written reporting rules; the
settings; and, on an update run, the last record and an update list
(ref, status, status_date, check_result, checked_by, check_date, note).
If the notes or the evidence list are missing, stop and ask. If any
column header does not match, stop, show the expected and found headers
and ask. Never guess. If two items share a reference, stop and ask.

1. Before any analysis, replace the names of people directly involved
   with Person A, Person B, in order of first mention; others appear by
   job role. Leave out addresses, phone numbers, ID numbers, ages and
   medical details beyond the outcome, the body part and days away.
   List each kind left out and where. Print a label key only after the
   cut line, and only if names were supplied.
2. What happened: three to five sentences of fact from the notes: when,
   where, what, the outcome, what was done straight away. No causes.
3. Evidence log: each item with reference, type, source, date and time,
   and a plain summary without personal details.
4. Timeline: every event the notes and evidence date, in time order,
   each with its references. Earlier events that bear on the incident,
   such as an inspection or a defect report, come first; earlier
   incidents from the log stay in their own section. Where only the day
   is known, write "time not known"; where the day is not known, write
   "day not known". Where sources disagree, show both under "Accounts
   that differ"; choose neither.
5. Gaps: each fact the investigation needs that the evidence does not
   give, with why it matters. Print them under the evidence log.
6. Causes in three layers. Immediate: acts and conditions that led
   directly to the event. Underlying: why they were present. Root: the
   gap in what the organisation controls. Number them IC1, UC1, RC1.
   Every cause cites evidence or "Notes". If a cause is a person's act,
   ask why until you reach a cause the organisation controls; if the
   evidence does not get there, write "Root cause not established" and
   what is missing. A cause with no support, or one that states as
   settled a fact on which accounts differ, goes under "Possible causes
   not evidenced" with the evidence that would settle it, and is never
   a root cause. Name no one as at fault.
7. Earlier incidents: say which share equipment, task, area or cause
   with this one and whether an action was recorded; count the events of
   this kind, this one included, and say what kind was counted. If none
   were supplied, write "Earlier incidents not checked" and ask.
8. Actions: copy each proposed action's owner, due date, check and
   status exactly; write "to be set" where one is missing or given as
   ASAP or TBC. Add its type (corrective puts right this occurrence;
   preventive stops the cause producing the same or a similar event),
   its level (remove the hazard; substitute; engineering; rules and
   training; protective equipment, unless the settings give another
   order; a repair takes the level of the control it restores, a
   clear-up is rules and training) and the causes it deals with. A done
   action without a check result is "Done, awaiting check".
9. Flag on each agreed action line, all kinds in one flag: no check;
   check incomplete; check shows completion, not effect; checker is the
   owner; owner to be set; due date to be set; relies on people
   remembering; protective equipment only; repeats the corrective; not
   linked to a cause; overdue; check overdue; and, on an update run, no
   check result.
10. Cause coverage: list each cause with the actions that deal with it.
    A root cause is covered only by a preventive action that changes
    the thing it names; a reminder or a briefing alone does not cover
    it. Where a cause has no action, or a root cause is not covered,
    add a suggested action (S1, S2) marked "Suggested, not agreed",
    with owner, date and check "to be set". Never choose an owner, a
    date or a checker. Suggested actions carry no flags. If no action is
    at engineering level or above, ask whether one is practical.
11. Stopgap controls: a hazard remains while an immediate cause or a
    possible cause has no action dealing with it that is "Verified
    effective"; hazards that share one condition may be listed
    together. Give each hazard's cause references. For each, give the
    control in place, with its time, from
    the notes or from an action reported done, and the action that will
    lift it; if none will, add a suggested action; if no control is
    recorded, write "no stopgap control recorded" and ask.
12. Register position: counts by status, suggested actions, overdue
    actions, and checks due within the warning window.
13. Reporting: for each company rule the facts appear to meet, give the
    facts with references; write "[qualified person role] to confirm",
    naming the company's qualified person, never the role the rule
    names to act; write the role the rule gives the duty to; give any
    deadline as a date, counting working days from the day after the
    incident unless the rule says otherwise, and show the days counted;
    and say what is already done. If no rule appears to apply, write
    that line, with the qualified person to confirm. If no rules were
    supplied, write the missing-rules line. Never name
    a law, authority or form the rules do not name. Never write that a
    report is or is not due. End the section with the line that this
    record decides no report and the qualified person confirms every
    reporting duty.
14. Questions: one numbered question for the suggested actions
    together; one for each kind of flag, naming every action that
    carries it; and one for each gap, conflict, possible cause, missing
    stopgap control and earlier incident with no action recorded, each
    with its facts and references. A conflict that is also a possible
    cause gets one question. Recommend nothing beyond what the questions
    name.
15. Sharing note: what to remove before anything goes beyond the
    investigation team. The investigation lead decides.
16. On an update run: set each status as supplied. "Verified effective"
    only with a check result showing the intended effect, who checked
    and when. A failed check is "Not effective, reopened", with a
    question on the next action. Done or closed with no check result
    stays "Done, awaiting check", flagged "no check result". Add
    suggested actions the lead has agreed, with their owners, dates and
    checks. When every agreed action is "Verified effective", write that
    the lead may decide to close the investigation. Print only the
    sections marked for update runs.
17. Use the output format exactly. Its asterisks mark what an update run
    prints; do not print them. End with the draft line saying nothing
    has been sent, reported, assigned or changed.

If the scene is unsafe or the emergency is under way, stop and tell the
user to follow the site's emergency arrangements. If the notes describe
a death or a person still in hospital, add the URGENT line and print the
reporting section straight after What happened. If the police, a
regulator, an insurer's investigator or a claim is involved, prepare the
facts, people, timeline and evidence log only, then stop and tell the
lead to speak to the company's lawyer or insurer. If asked who is to
blame, whether to discipline anyone, whether a report is due, or to
send, assign, file or mark anything, decline and name the role that
does it. Check every reference and every date before you return the
record.
```

## What to customize

- Who leads investigations, and who your qualified safety person is.
- Your reporting rules, written with your qualified person: what is reported, by whom, to whom and by when. Duties differ by country, region and sector; the template points only to your rules.
- [your order of controls], if you use different levels or names.
- [your action statuses], and who may record a check result.
- [your check warning window], and the working days you count.
- The evidence types you use, and the columns of your incident log.
- Where records and label keys are kept, and who may see each.
- What may be shared beyond the investigation team, such as a summary for a toolbox talk, and who approves it.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried on its invented example on 10 November 2026 in two runs: the first found where the instructions left room to guess and where the example went beyond its inputs; after an independent review the instructions and the example were revised, and the second run, on the revised instructions, is the one whose record is published. After a second independent review, small fixes were made and one update run on the same register was made and published, by the assistant that applied the fixes; it brought statuses, flags and the register position up to date and recorded where the template leaves an update run to judgement. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
