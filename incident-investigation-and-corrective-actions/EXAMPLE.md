# Incident investigation and corrective actions: an invented example

*Illustrative example with invented data.* The business, the people, the incident, the evidence and every date below are invented. The business is an invented builders' merchant with two timber yards. Its operations manager leads the investigation; its external safety adviser is the qualified person. The inputs refer to people by job role, as the business asks of everyone who writes up an incident.

The inputs come first, in full, so the template can be run on them. The record the workflow template returned follows. After it comes an update run on the same register, nineteen days later, with its inputs and what it returned.

## The inputs

### 1. Incident notes (typed by the operations manager)

```
Incident reference: Y2-2026-07
Type: injury and property damage
Date and time: Tuesday 13 October 2026, about 07:40
Where: Yard 2, timber racking, aisle 4 at bays 4 and 5
Investigation lead: operations manager. Qualified person: the company's
  external safety adviser.
What happened: forklift FLT 3, reversing out of bay 4, hit the bay's
  front upright. A bundle of timber battens fell from the top level into
  aisle 4 and struck the yard operative, who was walking down the aisle,
  on the right foot and lower leg.
Outcome: first aid on site, then to hospital by taxi at 08:10. Bruising,
  no fracture. Off work 13 and 14 October; expected back on light duties
  15 October.
Done straight away: FLT 3 taken out of use at 08:00 until the reversing
  alarm is repaired. Bays 4 and 5 unloaded and closed with barrier tape
  at 08:30 until the rack inspector has seen them. Safety adviser phoned
  at 14:00 on 13 October; answer awaited.
Today: Wednesday 14 October 2026. The team met this morning.
Check warning window: 14 days. Working days: Monday to Friday.
```

### 2. Evidence list (export)

```
ref,type,source,date_time,summary
E1,statement,forklift driver,2026-10-13 09:15,"Reversing out of bay 4 with a pack of sheet material. Looked over my shoulder and did not see anyone. Felt a knock at the back, then heard the bundle come down. The reversing alarm on FLT 3 has been quiet for a couple of weeks; I put it on the check sheet."
E2,statement,yard operative,2026-10-13 11:30,"By phone. Was walking down aisle 4 to get the delivery note from the board at bay 5. Did not hear the truck. The bundle hit my right foot and shin. Hospital said bruising only."
E3,statement,yard supervisor,2026-10-13 10:00,"Returns have been stacked on the pedestrian walkway along the north fence since last week, so people walk down aisle 4 to reach the delivery board at bay 5. 07:00 to 09:00 is the busiest loading time."
E4,photo,yard supervisor,2026-10-13 08:05,"Bay 4 front upright bent inward about 10 cm at about 1 m high. No upright protector at bay 4. Bundle of battens lying across aisle 4."
E5,record,workshop,2026-10-14 08:30,"FLT 3 pre-use check sheets, 1 to 13 October: reversing alarm marked 'faint' on 5, 6 and 7 October, 'OK' from 8 October. No repair request raised for FLT 3 in October."
E6,document,operations manager,2026-10-14 08:30,"Yard traffic plan, version 2, March 2024: pedestrians use the marked walkway along the north fence; aisles are for forklifts only from 06:00 to 09:00. Says nothing about keeping the walkway clear or what to do if it is blocked."
E7,record,rack inspector,2026-08-14,"Rack inspection report: bay 4 front upright, minor damage, monitor. Recommend upright protectors on bays 4 to 12 to match bays 1 to 3."
E8,document,operations manager,2026-10-14 08:30,"Forklift pre-use check procedure: the driver completes the sheet at the start of each shift and tells the workshop about any defect. Nothing says when a truck must stop being used."
E9,record,maintenance lead,2026-10-14 09:00,"Maintenance plan, July to December 2026: no entry for upright protectors. Rack inspection reports are filed by the office; nobody enters their recommendations in the plan."
```

### 3. Earlier incidents (from the incident log)

```
H1, 2026-06-02: FLT 1 hit the front upright at bay 2, Yard 2. No one hurt.
  Upright replaced; protectors fitted to bays 1 to 3.
H2, 2026-08-19: Near miss, Yard 2, aisle 6, 07:30. A reversing forklift
  came close to a pedestrian. Reported by the driver. No action recorded.
```

### 4. Actions proposed at the team meeting, 14 October (export)

```
ref,action,owner,due,check,status
A1,Fit upright protectors to bays 4 to 12 in Yard 2,Maintenance lead,2026-10-30,"No new impact damage on bays 4 to 12 at the next inspection; rack inspector; 2027-02-12",Open
A2,Clear the returns off the pedestrian walkway,Yard supervisor,2026-10-14,,Done 2026-10-13
A3,Repair the FLT 3 reversing alarm before the truck goes back into use,Workshop lead,2026-10-14,"Repair confirmed; workshop lead; 2026-10-14",In progress
A4,Retrain forklift drivers to check behind before reversing,Yard supervisor,2026-11-06,,Open
A5,Remind all yard staff at the morning briefing to use the walkway,Yard supervisor,2026-10-16,,Open
```

### 5. Reporting rules (the business's written list, agreed with its safety adviser)

```
R1 Injury that needs hospital treatment: the operations manager tells the
   insurer within 5 working days.
R2 Injury that keeps someone off normal work, or damage to racking or any
   other structure: the operations manager asks the safety adviser, the
   same day, whether a report to the authorities is due and by when.
```

## The output

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
- **RC3** Rack inspection recommendations have no route into the maintenance plan, so the August recommendation was never entered in the plan. (E7, E9)

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

- People on foot in aisle 4 while forklifts reverse during the forklift-only hours (IC1, IC2): returns cleared off the walkway, reported done on 13 October (A2, awaiting check). Lifted by A4 and A5.
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

## An update run

### The inputs

The last record is the one above. The operations manager supplies the update list, with today's date.

```
Today: Monday 2 November 2026.

ref,status,status_date,check_result,checked_by,check_date,note
A1,In progress,2026-10-28,,,,"Protectors ordered 28 October; delivery expected 6 November"
A2,Done,2026-10-13,"Walkway walked at 07:30 on 19, 22 and 27 October: clear each time, and no one on foot in aisle 4 during the forklift-only hours",Operations manager,2026-10-27,
A3,Done,2026-10-14,"Alarm heard clearly from the far end of aisles 4 and 6 with two other trucks running",Yard supervisor,2026-10-15,"FLT 3 back in use 15 October"
A4,Closed,2026-10-30,,,,"All six drivers retrained 30 October"
A5,Done,2026-10-16,"Two people on foot seen in aisle 5 at 07:45 on 28 October, crossing to the delivery board",Operations manager,2026-10-28,
```

### The output

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
