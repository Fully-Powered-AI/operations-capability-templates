# Trial: Incident investigation and corrective actions, run on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Opus 5.5 (model ID claude-opus-5-5)
- **Date:** 2026-11-10
- **Template version:** 0.1.0

This is a record of one run of the workflow template on its own invented example. The business, the people, the incident, the evidence and the dates are invented, and no client data was used. It shows what the template produced on one set of inputs, and then on one update to the register those inputs started. It is not a test in any company's environment.

This is the second run on the same example. The first run, earlier the same day, was made by an assistant that had not written the template. It, and an independent review of the template afterwards, found where the instructions left room to guess and where the published example went beyond its own inputs. The instructions, the output format and the example's output were revised, and the run recorded here was made on the revised instructions. What the first run found, and what was changed, follows the observations. After that come an update run on the same register, made after a second review, and what that review changed.

## How this run was made

The inputs are exactly those in [the worked example](example.md), under "The inputs": the incident notes for Y2-2026-07, evidence E1 to E9, earlier incidents H1 and H2, proposed actions A1 to A5 and reporting rules R1 and R2. Settings were the defaults for the order of controls and the action statuses, with the 14-day warning window and Monday to Friday working days from the notes.

This run is not independent. It was made by the assistant that revised the template after the review, and that assistant had read the first run, the review and the earlier example output before running. It followed the revised instruction block and output format step by step on the inputs alone. The published example's output was then replaced with this run's output, unchanged, so the two were the same text. After a second review, two lines of the example's output were edited, as listed at the end; the record below is this run's output as produced.

## What came out

**INCIDENT INVESTIGATION RECORD: Y2-2026-07, injury and property damage**

**For:** Operations manager (investigation lead). Prepared Wednesday 14 October 2026 from the incident notes, the evidence list (E1 to E9), the earlier incidents (H1, H2), the proposed actions (A1 to A5) and the reporting rules (R1, R2). Not supplied: the order of controls and the action statuses (defaults used).

**What happened**

On Tuesday 13 October 2026 at about 07:40, forklift FLT 3, reversing out of bay 4 in Yard 2, struck the bay's front upright. A bundle of timber battens fell from the top level into aisle 4 and struck Person A, who was walking down the aisle, on the right foot and lower leg. Person A had first aid on site, went to hospital by taxi at 08:10 with bruising and no fracture, and was off work on 13 and 14 October. FLT 3 was taken out of use at 08:00, and bays 4 and 5 were unloaded and closed with barrier tape at 08:30.

**People**

Person A (yard operative; struck by the falling bundle). Person B (forklift driver; driving FLT 3). Others appear by job role.

Names found in the inputs: none; no label key. Personal details left out: none found.

**Timeline**

- 14 August 2026, time not known: the rack inspection records minor damage to the bay 4 front upright, "monitor", and recommends upright protectors on bays 4 to 12. (E7)
- 5 to 7 October 2026, time not known: the FLT 3 pre-use check sheets mark the reversing alarm "faint". No repair request is raised for FLT 3 in October. (E5)
- 8 to 13 October 2026, time not known: the check sheets mark the alarm "OK". (E5)
- The week before 13 October, day not known: returns are stacked on the pedestrian walkway along the north fence. (E3)
- 13 October, about 07:40: Person B reverses FLT 3 out of bay 4 with a pack of sheet material, looks over the shoulder and sees no one; the truck strikes the bay 4 front upright. (E1, E4, Notes)
- 13 October, about 07:40: a bundle of battens falls from the top level into aisle 4 and strikes Person A, who is walking down the aisle to the delivery board at bay 5 and does not hear the truck. This is inside the 06:00 to 09:00 forklift-only hours for the aisles. (E2, E4, E6, Notes)
- 13 October, 08:00: FLT 3 is taken out of use until the reversing alarm is repaired. (Notes)
- 13 October, 08:05: photos show the upright bent inward about 10 cm at about 1 m high, no protector at bay 4, and the bundle across aisle 4. (E4)
- 13 October, 08:10: Person A goes to hospital by taxi after first aid on site. (Notes)
- 13 October, 08:30: bays 4 and 5 are unloaded and closed with barrier tape until the rack inspector has seen them. (Notes)
- 13 October, 14:00: the safety adviser is phoned; answer awaited. (Notes)
- 14 October, morning: the team meets and proposes actions A1 to A5. (Notes)

Accounts that differ: Person B says the FLT 3 reversing alarm had been quiet "for a couple of weeks" and was written on the check sheet (E1). The check sheets mark it "faint" on 5 to 7 October and "OK" from 8 October (E5). The notes take FLT 3 out of use "until the reversing alarm is repaired" (Notes). Neither account is chosen.

**Evidence log**

- **E1** statement, from Person B, 13 October 2026, 09:15: reversing out of bay 4 with sheet material; looked over the shoulder and saw no one; felt a knock, then heard the bundle fall; says the reversing alarm had been quiet for a couple of weeks and was written on the check sheet.
- **E2** statement, from Person A by phone, 13 October 2026, 11:30: walking down aisle 4 to get the delivery note from the board at bay 5; did not hear the truck; struck on the right foot and shin; hospital said bruising only.
- **E3** statement, from the yard supervisor, 13 October 2026, 10:00: returns stacked on the walkway along the north fence since the week before, so people walk down aisle 4 to reach the delivery board at bay 5; 07:00 to 09:00 is the busiest loading time.
- **E4** photo, from the yard supervisor, 13 October 2026, 08:05: bay 4 front upright bent inward about 10 cm at about 1 m high; no upright protector at bay 4; bundle across aisle 4.
- **E5** record, from the workshop, 14 October 2026, 08:30: FLT 3 check sheets for 1 to 13 October; alarm "faint" on 5 to 7 October and "OK" from 8 October; no repair request raised for FLT 3 in October.
- **E6** document, from the operations manager, 14 October 2026, 08:30: yard traffic plan, version 2, March 2024; pedestrians on the north fence walkway; aisles forklift-only from 06:00 to 09:00; nothing on keeping the walkway clear or on what to do when it is blocked.
- **E7** record, from the rack inspector, 14 August 2026, time not known: bay 4 front upright, minor damage, monitor; protectors recommended on bays 4 to 12 to match bays 1 to 3.
- **E8** document, from the operations manager, 14 October 2026, 08:30: forklift pre-use check procedure; the driver completes the sheet each shift and tells the workshop of any defect; nothing on when a truck must stop being used.
- **E9** record, from the maintenance lead, 14 October 2026, 09:00: the maintenance plan for July to December 2026 has no entry for upright protectors; rack inspection reports are filed by the office and their recommendations are not entered in the plan.

Gaps: whether Person B told the workshop about the alarm, beyond writing it on the check sheet, as the procedure asks (E1, E8); it shows whether the defect reached anyone who could act on it. The day the returns were first stacked on the walkway (E3); it shows how long the walkway was blocked. Where the delivery board at bay 5 is normally reached from, and whether its position takes people on foot into the aisles; the inputs say only that people walked down aisle 4 to reach it while the walkway was blocked (E2, E3, E6). It shows whether a clear walkway is enough to keep people on foot out of the aisles.

**Causes**

*Immediate*

- **IC1** FLT 3 reversed out of bay 4 into the bay's front upright; Person B looked over the shoulder and saw no one. (E1, E4)
- **IC2** Person A was walking down aisle 4 during the forklift-only hours and did not hear the truck. (E2, E6, Notes)
- **IC3** Bay 4 had no upright protector; the upright bent and the top-level bundle fell into the aisle. (E4)

*Underlying*

- **UC1** The pedestrian walkway along the north fence was blocked by returns, so people walked down aisle 4 to reach the delivery board at bay 5. (E2, E3)
- **UC2** FLT 3 stayed in use after its reversing alarm was marked faint on 5 to 7 October, and no repair request was raised. (E5)
- **UC3** The August recommendation to fit protectors to bays 4 to 12 had not been carried out. (E7, E9)

*Root*

- **RC1** The yard traffic plan has no rule for keeping the pedestrian walkway clear or for what people on foot do when it is blocked. (E3, E6)
- **RC2** The pre-use check procedure leaves a defect to the driver to pass on and never says when a truck must stop being used. (E5, E8)
- **RC3** Rack inspection recommendations have no route into the maintenance plan, so the August recommendation got no owner and no date. (E7, E9)

Possible causes not evidenced: that the FLT 3 reversing alarm was not sounding at 07:40 on 13 October. Person B says it had been quiet (E1), and FLT 3 was taken out of use until the alarm is repaired (Notes); the check sheets mark it "OK" from 8 October (E5). The workshop's record of the alarm as found when it was repaired would settle it.

**Earlier incidents**

- **H1**, 2 June 2026: FLT 1 hit the front upright at bay 2 in Yard 2; no one hurt; the upright was replaced and protectors fitted to bays 1 to 3. Same task (a forklift working at the racking), same yard and same kind of damage as IC1 and IC3. An action was recorded.
- **H2**, 19 August 2026: near miss in Yard 2, aisle 6, at 07:30; a reversing forklift came close to a pedestrian; reported by the driver; no action recorded. Same yard and pattern as IC1 and IC2: a reversing forklift near a person on foot, inside the forklift-only hours.

This is event 3 of this kind in Yard 2 since 2 June 2026, counting forklift strikes on racking and reversing forklifts coming close to people on foot.

**Actions**

- **A1** Fit upright protectors to bays 4 to 12 in Yard 2. Preventive. Level: engineering. Deals with: IC3, UC3. Owner: maintenance lead. Due: 30 October 2026. Check: no new impact damage on bays 4 to 12 at the next inspection, by the rack inspector, on 12 February 2027. Status: Open.
- **A2** Clear the returns off the pedestrian walkway. Corrective. Level: rules and training. Deals with: UC1. Owner: yard supervisor. Due: 14 October 2026. Check: to be set. Status: Done, awaiting check (reported done 13 October 2026). FLAG: no check.
- **A3** Repair the FLT 3 reversing alarm before the truck goes back into use. Corrective. Level: engineering. Deals with: UC2. Owner: workshop lead. Due: 14 October 2026. Check: repair confirmed, by the workshop lead, on 14 October 2026. Status: In progress. FLAG: check shows completion, not effect; checker is the owner.
- **A4** Retrain forklift drivers to check behind before reversing. Preventive. Level: rules and training. Deals with: IC1. Owner: yard supervisor. Due: 6 November 2026. Check: to be set. Status: Open. FLAG: no check; relies on people remembering.
- **A5** Remind all yard staff at the morning briefing to use the walkway. Preventive. Level: rules and training. Deals with: IC2, UC1. Owner: yard supervisor. Due: 16 October 2026. Check: to be set. Status: Open. FLAG: no check; relies on people remembering.
- **S1** Add to the yard traffic plan a rule that the pedestrian walkway is kept clear, and what people on foot do when it is blocked. Preventive. Level: rules and training. Deals with: RC1, UC1. Owner: to be set. Due: to be set. Check: to be set. Status: Suggested, not agreed.
- **S2** Change the pre-use check procedure to say when a truck with a defect on a safety item stops being used, and how the defect reaches the workshop. Preventive. Level: rules and training. Deals with: RC2, UC2. Owner: to be set. Due: to be set. Check: to be set. Status: Suggested, not agreed.
- **S3** Enter every rack inspection recommendation in the maintenance plan with an owner and a date. Preventive. Level: rules and training. Deals with: RC3, UC3. Owner: to be set. Due: to be set. Check: to be set. Status: Suggested, not agreed.
- **S4** Have the rack inspector see bays 4 and 5, and put the bay 4 upright right, before the bays are reloaded. Corrective. Level: engineering. Deals with: IC3. Owner: to be set. Due: to be set. Check: to be set. Status: Suggested, not agreed.

Cause coverage: IC1: A4. IC2: A5. IC3: A1, S4. UC1: A2, A5, S1. UC2: A3, S2. UC3: A1, S3. RC1: S1. RC2: S2. RC3: S3.

**Stopgap controls**

- People on foot in aisle 4 while forklifts reverse during the forklift-only hours (IC1, IC2): returns cleared off the walkway, reported done on 13 October (A2, awaiting check). Lifted by S1.
- Forklifts reversing near the uprights at bays 6 to 12, for which the August inspection recommended protectors (IC1, IC3; E7): no stopgap control recorded.
- Damaged upright at bay 4 (IC3): bays 4 and 5 unloaded and closed with barrier tape at 08:30 on 13 October, until the rack inspector has seen them (Notes). Lifted by S4.
- FLT 3 reversing alarm reported quiet (the possible cause): FLT 3 taken out of use at 08:00 on 13 October until the alarm is repaired (Notes). Lifted by A3.

**Register position as of Wednesday 14 October 2026**

Open 3 (A1, A4, A5). In progress 1 (A3). Done, awaiting check 1 (A2). Verified effective 0. Not effective, reopened 0. Suggested, not agreed 4 (S1 to S4).

Overdue: none. Checks due by Wednesday 28 October 2026: A3, 14 October 2026.

**Reporting duties to confirm**

- **R1** appears to apply: Person A went to hospital (Notes). The safety adviser to confirm. The rule gives the duty to the operations manager. Deadline in the rule: tell the insurer by Tuesday 20 October 2026, 5 working days counted from the day after Tuesday 13 October (14, 15, 16, 19 and 20 October). Done so far: nothing recorded.
- **R2** appears to apply: Person A was off work on 13 and 14 October (Notes), and the bay 4 upright was bent (E4). The safety adviser to confirm. The rule gives the duty to the operations manager. Deadline in the rule: ask the safety adviser the same day, Tuesday 13 October 2026. Done so far: the safety adviser was phoned at 14:00 on 13 October; answer awaited (Notes).

This record decides no report. The safety adviser confirms every reporting duty.

**Questions for the investigation lead**

1. S1 to S4 are suggested, not agreed. For each: agree, change or drop it, and name an owner, a due date and a check.
2. A2, A4 and A5 have no check. For each: what will show it worked, who checks, and when?
3. A3's check, the workshop lead confirming the repair, shows the repair was finished, not that the alarm can now be heard in the aisles. What check would show that?
4. A3's checker is the workshop lead, who also owns the action. Who else could carry out the check?
5. A4 and A5 rely on people remembering. Is a physical change practical for the causes they deal with (IC1, IC2, UC1)?
6. Did Person B tell the workshop about the alarm, beyond writing it on the check sheet, as the procedure asks (E1, E8)?
7. On what day were the returns first stacked on the walkway (E3)?
8. Where is the delivery board at bay 5 normally reached from, and does its position take people on foot into the aisles? The inputs say only that people walked down aisle 4 to reach it while the walkway was blocked (E2, E3, E6).
9. Person B says the alarm had been quiet for a couple of weeks (E1); the check sheets mark it "OK" from 8 October (E5); FLT 3 was taken out of use until the alarm is repaired (Notes). Was the alarm sounding at 07:40 on 13 October? The workshop's record of the alarm as found when it was repaired would settle it.
10. No stopgap control is recorded for forklifts reversing near the uprights at bays 6 to 12 until A1's protectors are fitted (IC1, IC3; E7). Is one needed until then?
11. H2, the August near miss in aisle 6, has no action recorded. Should it be reviewed alongside this incident?

**Before sharing more widely**

Before this record or a summary is used in a toolbox talk, on a notice board or in a report beyond the investigation team, remove the dates and times, "Yard 2, aisle 4, bays 4 and 5", the truck number and the outcome details (hospital, days off), and refer to "a yard operative" and "a forklift driver". The operations manager decides what is shared.

Draft for the operations manager's review. Nothing has been sent, reported, assigned or changed.

## What was observed

**Every required part was produced.** All sections of the format were filled. No stop condition was met: the headers matched the defaults, no names, medical records, passwords, police, regulator, insurer or claim appeared, the scene was safe and no one was still in hospital, so the URGENT line did not apply. Nothing was refused.

**Judgement calls the run made.**
- The revised test for stopgap controls (a hazard remains while an immediate or possible cause has no action that is verified effective) brought in a hazard neither earlier output listed: forklifts reversing near the uprights at bays 6 to 12 until A1's protectors are fitted, with no stopgap control recorded, and a question (Q10). It reads E7 ("protectors on bays 4 to 12 to match bays 1 to 3") as saying those bays have none; E7 implies this but does not state it.
- The stopgap for people on foot is the cleared walkway, which comes from A2 (reported done, not yet checked) rather than from the notes. The revised step allows a control from an action reported done.
- UC2 (FLT 3 stayed in use after its alarm was marked faint, with no repair request) was kept as an underlying cause, and RC2 with it. Whether the alarm was sounding at 07:40 is the possible cause, because the accounts differ; UC2 itself states only facts the check sheets give. A reader could argue that UC2 and RC2 bear on this event only through the possible cause.
- A3 deals with UC2. The format's "Deals with" lists causes, so the link from A3 to the possible cause shows only in the stopgap line.
- A1 was linked to UC3, because it carries out the August recommendation, but not to RC3, because it does not change how recommendations reach the maintenance plan.
- Suggested actions are numbered in the order the procedure adds them: S1 to S3 from cause coverage, S4 from the stopgap list. The corrective for the bay 4 upright is therefore S4.
- "Event of this kind" was counted as forklift strikes on racking plus reversing forklifts coming close to people on foot, and the record says so.
- The inputs already used job roles; the run still labelled the two people directly involved and wrote "none; no label key".
- A1's check ("no new impact damage at the next inspection") was not flagged, although no damage may happen anyway. The template still gives no test for what shows effect.

**Facts in the output that are not in the inputs.** "A toolbox talk" and "a notice board" in the sharing note are examples of wider sharing, not facts. That bays 6 to 12 have no protectors is inferred from E7, as above. The 20 October deadline is worked out from R1, and "inside the forklift-only hours" from E6 and the time in the notes. S4 says "put the bay 4 upright right" and does not say whether it must be replaced.

**Against the reviewer checklist.** Items 1 to 7 and 10 were met by the output as read. Item 8 is partly open: three hazards have a stopgap control and the action that lifts it, and one has none, which Q10 asks about; whether the closed bays are in fact closed cannot be told from the inputs. Item 9: the rules are quoted from the company's list, the date count is shown and correct on the stated convention, and nothing says a report is or is not due. Item 11 needs each owner to read their actions and cannot be tested here.

**Acceptance test 1, as now written,** was met: every cause has an action or a suggested action; each root cause has a preventive suggested action that changes what it names (S1 the traffic plan, S2 the check procedure, S3 the route into the maintenance plan); there is one question for the suggested actions, one for each of the four kinds of flag, and one each for the three gaps, the conflict that is also the possible cause, the missing stopgap control and H2, eleven in all; no names appear; and R1 and R2 are marked for the safety adviser to confirm, each naming the operations manager as the role the rule gives the duty to.

## What the first run found, and what was changed

The first run was made on 10 November 2026 in Claude, by an assistant (Claude Sonnet 5.5) that had not written the template and saw only the template and the example's inputs before comparing its output with the published one. Its record is replaced by this one; what it found is summarised here.

It produced four suggested actions and twelve questions, against the published example's three and eleven. Its root causes were the inspection recommendations, the traffic plan and the check procedure; the published example instead had a root cause saying the yard layout puts the delivery board inside the forklift-only area, which the inputs do not say. It put the alarm's state at 07:40 under possible causes, because the evidence conflicts, where the example had stated it as an immediate cause. It treated the cleared walkway as the stopgap for people on foot, where the example said no stopgap was recorded. It named the safety adviser as the role that confirms each reporting duty; the example named the operations manager on each rule and the safety adviser in the closing line, which disagreed with itself and with the template. It noted that the example's possible cause about the speed of FLT 3, and its question about a witness or camera footage, had no basis in the inputs, and that "replace the bay 4 front upright" went beyond them. It found these points the template left open: whether the incident day counts in working days; whether earlier incidents belong in the timeline; what "event of this kind" means; which hazards "remain" for the stopgap list; the level for repairs and clear-ups; how direct an action's link to a root cause must be; whether a conflict that is also a possible cause gets one question or two; trailing asterisks in the format that read like output; and small differences between the instruction block and the procedure. It said acceptance test 1's exact counts were stricter than the template.

Changed afterwards, before the run recorded above:
- The reporting line names the company's qualified person as the role that confirms, never the role the rule names to act, and states separately the role the rule gives the duty to. The example now says "The safety adviser to confirm" on R1 and R2 and names the operations manager as the role the rule gives the duty to.
- The example's layout root cause was replaced by the traffic plan's gap alone; the delivery board's position became a gap and a question for the lead. The cause coverage, the suggested actions, the stopgap list, the register counts and the questions were worked out again.
- The alarm's state at 07:40 moved to possible causes, and the template now says that a cause stating as settled a fact on which accounts differ is a possible cause. The speed and camera line was removed.
- A root cause now counts as covered only by a preventive action that changes the thing it names; a reminder or briefing alone does not cover it.
- The stopgap step now says which hazards remain, and allows a control from an action reported done.
- Working days are counted from the day after the incident unless the rule says otherwise, with the days shown.
- Earlier incidents stay in their own section, not in the timeline; the kind of event counted is stated; a repair takes the level of the control it restores and a clear-up is rules and training; a conflict that is also a possible cause gets one question.
- The instruction block now follows the procedure's order, includes the "time not known" and "day not known" rule, the earlier-events-first rule and the "not linked to a cause" flag in the same place as the procedure, ends the reporting section with the procedure's closing line, and says not to print the format's asterisks.
- Acceptance test 1 states properties instead of exact counts. The example's medical-details line now says none were left out, with the outcome kept in What happened; H2 is described as the same yard and pattern, not the same area; S4 (formerly S1) says "put the bay 4 upright right" instead of "replace".
- The version notes and the public page now say the template was tried on its example.

## An update run on the same register

### How this run was made

The update run was made on 10 November 2026, after a second independent review asked for one, by the assistant that applied that review's points (Claude Opus 5.5, model ID claude-opus-5-5, in the same product). It wrote the update list, which is invented, then followed the instruction block and output format as revised after that review: the last record was the example's record as published, with the two edits listed at the end, and the update list is the one in [the worked example](example.md), under "An update run". It is not independent: the same assistant wrote the inputs, knew what each row was meant to exercise, and ran the template on them. The example's update output is this run's output, unchanged.

### What came out

**INCIDENT INVESTIGATION RECORD: Y2-2026-07, injury and property damage / REGISTER UPDATE**

**For:** Operations manager (investigation lead). Prepared Monday 2 November 2026 from the last record (14 October 2026) and the update list (A1 to A5). Not supplied: the order of controls and the action statuses (defaults used).

**Actions**

- **A1** Fit upright protectors to bays 4 to 12 in Yard 2. Preventive. Level: engineering. Deals with: IC3, UC3. Owner: maintenance lead. Due: 30 October 2026. Check: no new impact damage on bays 4 to 12 at the next inspection, by the rack inspector, on 12 February 2027. Status: In progress (reported in progress 28 October 2026). FLAG: overdue.
- **A2** Clear the returns off the pedestrian walkway. Corrective. Level: rules and training. Deals with: UC1. Owner: yard supervisor. Due: 14 October 2026. Check: to be set. Status: Verified effective (reported done 13 October 2026; check result 27 October 2026, by the operations manager: walkway clear at 07:30 on 19, 22 and 27 October, and no one on foot in aisle 4 during the forklift-only hours).
- **A3** Repair the FLT 3 reversing alarm before the truck goes back into use. Corrective. Level: engineering. Deals with: UC2. Owner: workshop lead. Due: 14 October 2026. Check: repair confirmed, by the workshop lead, on 14 October 2026. Status: Verified effective (reported done 14 October 2026; check result 15 October 2026, by the yard supervisor: alarm heard clearly from the far end of aisles 4 and 6 with two other trucks running).
- **A4** Retrain forklift drivers to check behind before reversing. Preventive. Level: rules and training. Deals with: IC1. Owner: yard supervisor. Due: 6 November 2026. Check: to be set. Status: Done, awaiting check (reported closed 30 October 2026). FLAG: no check; no check result; relies on people remembering.
- **A5** Remind all yard staff at the morning briefing to use the walkway. Preventive. Level: rules and training. Deals with: IC2, UC1. Owner: yard supervisor. Due: 16 October 2026. Check: to be set. Status: Not effective, reopened (reported done 16 October 2026; check result 28 October 2026, by the operations manager: two people on foot seen in aisle 5 at 07:45 on 28 October, crossing to the delivery board). FLAG: relies on people remembering; overdue.
- **S1** Add to the yard traffic plan a rule that the pedestrian walkway is kept clear, and what people on foot do when it is blocked. Preventive. Level: rules and training. Deals with: RC1, UC1. Owner: to be set. Due: to be set. Check: to be set. Status: Suggested, not agreed.
- **S2** Change the pre-use check procedure to say when a truck with a defect on a safety item stops being used, and how the defect reaches the workshop. Preventive. Level: rules and training. Deals with: RC2, UC2. Owner: to be set. Due: to be set. Check: to be set. Status: Suggested, not agreed.
- **S3** Enter every rack inspection recommendation in the maintenance plan with an owner and a date. Preventive. Level: rules and training. Deals with: RC3, UC3. Owner: to be set. Due: to be set. Check: to be set. Status: Suggested, not agreed.
- **S4** Have the rack inspector see bays 4 and 5, and put the bay 4 upright right, before the bays are reloaded. Corrective. Level: engineering. Deals with: IC3. Owner: to be set. Due: to be set. Check: to be set. Status: Suggested, not agreed.

Cause coverage: IC1: A4. IC2: A5. IC3: A1, S4. UC1: A2, A5, S1. UC2: A3, S2. UC3: A1, S3. RC1: S1. RC2: S2. RC3: S3.

**Stopgap controls**

- People on foot in aisle 4 while forklifts reverse during the forklift-only hours (IC1, IC2): returns cleared off the walkway on 13 October, and the walkway checked clear on 19, 22 and 27 October (A2, verified effective). Lifted by A4 and A5.
- Forklifts reversing near the uprights at bays 6 to 12, for which the August inspection recommended protectors (IC1, IC3; E7): no stopgap control recorded.
- Damaged upright at bay 4 (IC3): bays 4 and 5 unloaded and closed with barrier tape at 08:30 on 13 October, until the rack inspector has seen them (Notes). Lifted by S4.

**Register position as of Monday 2 November 2026**

Open 0. In progress 1 (A1). Done, awaiting check 1 (A4). Verified effective 2 (A2, A3). Not effective, reopened 1 (A5). Suggested, not agreed 4 (S1 to S4).

Overdue: A1, due 30 October 2026; A5, due 16 October 2026. Checks due by Monday 16 November 2026: none.

**Reporting duties to confirm**

- **R1** appears to apply: Person A went to hospital (Notes). The safety adviser to confirm. The rule gives the duty to the operations manager. Deadline in the rule: tell the insurer by Tuesday 20 October 2026, 5 working days counted from the day after Tuesday 13 October (14, 15, 16, 19 and 20 October). Done so far: nothing recorded.
- **R2** appears to apply: Person A was off work on 13 and 14 October (Notes), and the bay 4 upright was bent (E4). The safety adviser to confirm. The rule gives the duty to the operations manager. Deadline in the rule: ask the safety adviser the same day, Tuesday 13 October 2026. Done so far: the safety adviser was phoned at 14:00 on 13 October; answer awaited (Notes).

This record decides no report. The safety adviser confirms every reporting duty.

**Questions for the investigation lead**

1. S1 to S4 are still suggested, not agreed. For each: agree, change or drop it, and name an owner, a due date and a check.
2. A5's check found two people on foot in aisle 5 at 07:45 on 28 October, crossing to the delivery board, and A5 is reopened. What new or changed action follows, with an owner, a due date and a check?
3. A4 has no check. What will show it worked, who checks, and when?
4. A4 was reported closed on 30 October with no check result, so it stays done, awaiting check. When will it be checked, and by whom?
5. A4 and A5 rely on people remembering. Is a physical change practical for the causes they deal with (IC1, IC2, UC1)?
6. A1 and A5 are overdue. A1 was due 30 October; the update says protectors were ordered on 28 October, with delivery expected on 6 November. A5 was due 16 October and is reopened. What are the new due dates?
7. Did Person B tell the workshop about the alarm, beyond writing it on the check sheet, as the procedure asks (E1, E8)?
8. On what day were the returns first stacked on the walkway (E3)?
9. Where is the delivery board at bay 5 normally reached from, and does its position take people on foot into the aisles? The inputs say only that people walked down aisle 4 to reach it while the walkway was blocked (E2, E3, E6).
10. Person B says the alarm had been quiet for a couple of weeks (E1); the check sheets mark it "OK" from 8 October (E5); FLT 3 was taken out of use until the alarm is repaired (Notes). Was the alarm sounding at 07:40 on 13 October? The workshop's record of the alarm as found when it was repaired would settle it.
11. No stopgap control is recorded for forklifts reversing near the uprights at bays 6 to 12 until A1's protectors are fitted (IC1, IC3; E7). Is one needed until then?
12. H2, the August near miss in aisle 6, has no action recorded. Should it be reviewed alongside this incident?

Draft for the operations manager's review. Nothing has been sent, reported, assigned or changed.

### What was observed

**Statuses.** A2 and A3 became "Verified effective": each check result shows the intended effect and gives who checked, someone other than the owner, and when. A4, reported closed with no check result, stayed "Done, awaiting check" with the flag "no check result", as acceptance test 8 expects. A5's check result showed people still on foot in the aisles, so A5 became "Not effective, reopened" with a question on what follows, the behaviour acceptance test 9 expects, here with a different kind of failed check. A1, still in progress after its due date, was flagged overdue. The register counts match the action lines.

**Judgement calls the run made, where the template does not say.**
- The output format has no place for a check result or for who checked. The run put them in the status brackets. The Check field kept the last record's text exactly, so A2 and A5 read "Check: to be set" beside a check result, and A3 keeps its planned check (repair confirmed by the workshop lead) beside a result from the yard supervisor.
- "No check" was not applied to A2 or A5, because a check was in fact made, and A3's earlier flags (completion, not effect; checker is the owner) were dropped, because its result shows effect and comes from someone other than the owner. Verified actions were given no flags.
- A5 was flagged overdue: reopened is not done, and its due date has passed. The template has no rule for a new due date on a reopened action, so question 6 asks.
- The stopgap line for the alarm was dropped: A3 is verified effective, and the update notes FLT 3 back in use on 15 October. Read strictly, the stopgap step ties a hazard to an action dealing with its cause, and A3's "Deals with" lists UC2, not the possible cause.
- Each section marked for update runs was printed whole, including cause coverage, which sits under Actions without its own mark.
- Questions 7 to 12 were carried forward unchanged from the last record, because the update answers none of them. The template does not say whether an update run repeats open questions.
- The update list's notes have no place in the format. A1's order and delivery date appear in question 6; A3's return to use was read but not printed.
- R1's deadline, 20 October, has passed with nothing recorded as done. The reporting section was reprinted unchanged and still says nothing about whether a report is due; the template does not say whether an update run should point out a passed deadline.
- No suggested action was agreed in the update, so none was added. The template does not say how the lead supplies an agreed suggested action with its owner, date and check: the update list has no columns for them.

**Facts in the output that are not in the inputs.** None found beyond the last record. The overdue dates are worked out from the due dates and today's date, and "Checks due by Monday 16 November 2026" from the 14-day window.


## Changed after the second review

A second independent review passed the template with minor points. These were changed afterwards:
- The record now credits the incident investigation package's intake reference as a fifth source path, for the procedures and permits in force and for earlier incidents on the same equipment or task.
- In the example's output, RC3 now ends "so the August recommendation was never entered in the plan", which E9 supports, in place of "so the August recommendation got no owner and no date", which the run above produced.
- In the example's output, the stopgap for people on foot in aisle 4 is now "Lifted by A4 and A5", the actions that deal with IC1 and IC2, in place of "Lifted by S1", which the run above produced. S1 deals with RC1 and UC1, and the stopgap step ties a remaining hazard to an action dealing with the immediate cause.
- The procedure's sharing step now says that a role several people share may stay. The example's note, unchanged, keeps "a yard operative" and "a forklift driver"; the business has several drivers (A4).
- The flag "no check result", used on update runs, is now in the procedure's flag list and the instruction block's.
- The procedure now says that a check which could pass by chance, such as no repeat of a rare event over a short period, shows completion, not effect, unless it also looks at the control itself or covers a period in which the evidence shows the event would otherwise be expected. The instruction block was not changed for this, so the first record stands as produced. Read against the new sentence, A1's check stays unflagged: it covers about three and a half months on bays where the evidence records upright damage twice between August and October (E7, E4).
- The example gained the update run above, and the acceptance tests, version notes and public page now say that one update run has been made.
