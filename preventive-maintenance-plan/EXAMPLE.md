# Preventive maintenance plan: an invented example

*Illustrative example with invented data.* The business, the equipment, the costs, the dates and the failures below are all invented. The business is an invented 35-person commercial bakery supplying cafés, called the Bakery here, with six main pieces of equipment on one site. Its operations manager runs the plan; an outside maintenance engineer is its competent person for safety-critical equipment. People are referred to by role.

The inputs come first, in full, so the template can be run on them. The plan follows.

## The inputs

### 1. Settings (typed by the operations manager)

```
Site: the Bakery, production floor and plant room
Prepared for: operations manager
Today and plan start: Monday 4 January 2027
Plan period: 52 weeks
History period: 52 weeks, Monday 5 January 2026 to Sunday 3 January 2027
Days the site is closed: none (production runs every day)
Currency: US dollars
Band A: failure cost of $4,000 or more, or safety-critical
Band B: failure cost of $1,000 to $3,999
Condition checks: every month
Competent person for safety-critical equipment: the contracted maintenance engineer
Records stoppages and completed tasks: the maintenance technician
Approves spare-part purchases: the operations manager
```

### 2. Equipment register

```
asset_id,asset,area,installed,run_hours_per_week,safety_critical,cost_per_hour_stopped,est_hours_stopped,est_repair_cost,condition_check
MIX-01,Spiral mixer 120 kg,Mixing,2018,60,no,600,6,900,"motor bearing temperature, limit 70 C"
OVN-01,Four-deck gas oven,Baking,2015,70,yes,600,8,1500,
CHL-01,Walk-in chiller,Stores,2019,168,no,150,10,1200,"refrigerant suction pressure, limit not known"
WRP-01,Flow wrapper,Packing,2021,50,no,200,4,600,
CMP-01,Air compressor 7.5 kW,Plant room,2017,60,yes,300,5,800,
SLC-01,Bread slicer,Packing,2020,40,no,40,3,250,
```

### 3. Maker's tasks

```
asset_id,task,every,unit,last_done,reference
MIX-01,Check drive belt tension and wear,6,months,2026-10-06,Manual p. 22
MIX-01,Grease bowl bearings,500,run hours,2026-11-16,Manual p. 23
OVN-01,Clean and inspect burners and flues,6,months,2026-07-14,Manual s. 7.2
OVN-01,Service and safety check of the gas system,12,months,2026-01-20,Manual s. 7.1
OVN-01,Check door seals and hinges,1,months,2026-12-21,Manual s. 6.4
CHL-01,Clean condenser coil,3,months,2026-05-12,Manual p. 9
CHL-01,Check door gasket and heater,1,months,,Manual p. 10
WRP-01,Clean and inspect sealing jaws,1,weeks,2026-12-31,Manual 5.3
WRP-01,Replace jaw heater elements,2000,run hours,2026-04-14,Manual 5.6
CMP-01,Drain the receiver,1,weeks,2026-12-31,Manual p. 14
CMP-01,Change oil and air filter,2000,run hours,2026-08-03,Manual p. 15
CMP-01,Inspection of the pressure system,12,months,2026-03-09,Manual p. 3
SLC-01,Sharpen or replace blades,6,months,2026-06-01,Manual p. 4
```

### 4. Failure history (Monday 5 January 2026 to Sunday 3 January 2027)

```
asset_id,date_failed,hours_stopped,repair_hours,parts_and_labour,cause
MIX-01,2026-02-17,7,5,1100,drive belt snapped
PAL-01,2026-03-03,1,1,150,battery fault
WRP-01,2026-04-14,3,2,420,heater element failed
MIX-01,2026-06-23,5,4,900,drive belt worn through
SLC-01,2026-07-20,2,1,180,blade guard switch failed
WRP-01,2026-09-08,5,3,640,film sensor fault
MIX-01,2026-10-06,6,4,1000,drive belt snapped
```

### 5. Spare parts list

```
part,asset_id,on_hand,lead_time_days,unit_cost,used_last_12_months
Drive belt set,MIX-01,1,10,180,3
Bowl bearing grease cartridge,MIX-01,4,5,12,7
Burner igniter,OVN-01,0,21,95,0
Oven door seal kit,OVN-01,0,14,240,1
Condenser fan motor,CHL-01,0,,420,0
Jaw heater element,WRP-01,2,28,150,1
Film sensor,WRP-01,0,14,310,1
Cutting knife,WRP-01,1,21,22,26
"Compressor oil, 5 litres",CMP-01,1,3,45,2
Air filter element,CMP-01,0,7,38,2
Slicer blade set,SLC-01,1,10,160,2
```

## The output

**PREVENTIVE MAINTENANCE PLAN: the Bakery, production floor and plant room**

- **Prepared for:** operations manager. Prepared: Monday 4 January 2027. Plan period: Monday 4 January 2027 to Sunday 2 January 2028 (52 weeks).
- **History:** Monday 5 January 2026 to Sunday 3 January 2027, 7 rows.
- **Sources:** equipment register (6 assets); maker's tasks (13 tasks); failure history; spare parts list (11 parts); settings. Defaults used: none.
- **Bands:** A, failure cost \$4,000 or more, or safety-critical; B, \$1,000 to \$3,999; C, below \$1,000. (The organization's bands.)
- **Competent person for safety-critical equipment:** the contracted maintenance engineer.
- **Assets:** 6. Band A 3, B 2, C 1, not banded 0. Safety-critical: 2.
- **Approaches:** run to failure 1, scheduled 4, condition-based 1.
- **Tasks on the calendar:** 13 (12 from the maker's tasks, 1 condition check). Left off: 1.
- **Flagged:** 2 assets, 1 history item. Decisions: 3.

**1. Equipment ranked by failure cost**

1. **OVN-01** Four-deck gas oven (Baking). Failure cost \$6,300 = 8 h stopped x \$600 an hour + \$1,500 parts and labour (manager's estimate, no failures in the history). Band A. Safety-critical: yes.
2. **MIX-01** Spiral mixer 120 kg (Mixing). Failure cost \$4,600 = 6.0 h stopped x \$600 an hour + \$1,000 parts and labour (from history, 3 failures). Band A. Safety-critical: no. **FLAG, interval proposed from history.** See decision 1.
3. **CHL-01** Walk-in chiller (Stores). Failure cost \$2,700 = 10 h stopped x \$150 an hour + \$1,200 parts and labour (manager's estimate, no failures in the history). Band B. Safety-critical: no. **FLAG, condition check has no limit, overdue, no record, part lead time not stated.** See decision 2.
4. **CMP-01** Air compressor 7.5 kW (Plant room). Failure cost \$2,300 = 5 h stopped x \$300 an hour + \$800 parts and labour (manager's estimate, no failures in the history). Band A (safety-critical). Safety-critical: yes.
5. **WRP-01** Flow wrapper (Packing). Failure cost \$1,330 = 4.0 h stopped x \$200 an hour + \$530 parts and labour (from history, 2 failures). Band B. Safety-critical: no.
6. **SLC-01** Bread slicer (Packing). Failure cost \$260 = 2.0 h stopped x \$40 an hour + \$180 parts and labour (from history, 1 failure). Band C. Safety-critical: no.

**2. Maintenance approach**

- **OVN-01** Four-deck gas oven: Scheduled. Safety-critical, so its maker's tasks go on the calendar for the competent person to confirm.
- **MIX-01** Spiral mixer 120 kg: Condition-based. Band A with a check that states a limit (motor bearing temperature, 70 C): the maker's tasks stay on the calendar, the check is taken every month, and a reading of 70 C or more goes to the operations manager the same day.
- **CHL-01** Walk-in chiller: Scheduled. Band B; its check gives no limit, so it does not count.
- **CMP-01** Air compressor 7.5 kW: Scheduled. Safety-critical, so its maker's tasks go on the calendar for the competent person to confirm.
- **WRP-01** Flow wrapper: Scheduled. Band B with no condition check.
- **SLC-01** Bread slicer: Run to failure. Band C and not safety-critical; it is repaired when it fails.

**3. Task calendar**

*Every week*

- **WRP-01** Clean and inspect sealing jaws. Last done: Thursday 31 December 2026; next due Thursday 7 January 2027. Ref: Manual 5.3.
- **CMP-01** Drain the receiver. Last done: Thursday 31 December 2026; next due Thursday 7 January 2027. Ref: Manual p. 14. Safety-critical: interval for the competent person to confirm.

*Every month*

- **MIX-01** Take the motor bearing temperature. First due Monday 4 January 2027. Last done: new condition check. Ref: condition check, limit 70 C.
- **CHL-01** Check door gasket and heater. First due Monday 4 January 2027. Last done: no record. Ref: Manual p. 10.
- **OVN-01** Check door seals and hinges. First due Thursday 21 January 2027. Last done: Monday 21 December 2026. Ref: Manual s. 6.4. Safety-critical: interval for the competent person to confirm.

*January 2027*

- Monday 4 January 2027 **CHL-01** Clean condenser coil. Every 3 months. Ref: Manual p. 9. Overdue, was due Wednesday 12 August 2026.
- Wednesday 6 January 2027 **MIX-01** Check drive belt tension and wear. Every quarter, proposed from history; maker's interval 6 months. Ref: Manual p. 22.
- Monday 11 January 2027 **MIX-01** Grease bowl bearings. Every 8 weeks, converted from 500 run hours at 60 a week. Ref: Manual p. 23.
- Thursday 14 January 2027 **OVN-01** Clean and inspect burners and flues. Every 6 months. Ref: Manual s. 7.2. Safety-critical: interval for the competent person to confirm.
- Tuesday 19 January 2027 **WRP-01** Replace jaw heater elements. Every 40 weeks, converted from 2,000 run hours at 50 a week. Ref: Manual 5.6.
- Wednesday 20 January 2027 **OVN-01** Service and safety check of the gas system. Every 12 months. Ref: Manual s. 7.1. Safety-critical: interval for the competent person to confirm.

*February 2027*

- None beyond the weekly and monthly tasks.

*March 2027*

- Monday 8 March 2027 **MIX-01** Grease bowl bearings. Every 8 weeks, converted from 500 run hours at 60 a week. Ref: Manual p. 23.
- Tuesday 9 March 2027 **CMP-01** Inspection of the pressure system. Every 12 months. Ref: Manual p. 3. Safety-critical: interval for the competent person to confirm.
- Monday 22 March 2027 **CMP-01** Change oil and air filter. Every 33 weeks, converted from 2,000 run hours at 60 a week. Ref: Manual p. 15. Safety-critical: interval for the competent person to confirm.

*April 2027*

- Sunday 4 April 2027 **CHL-01** Clean condenser coil. Every 3 months. Ref: Manual p. 9.
- Tuesday 6 April 2027 **MIX-01** Check drive belt tension and wear. Every quarter, proposed from history; maker's interval 6 months. Ref: Manual p. 22.

*May 2027*

- Monday 3 May 2027 **MIX-01** Grease bowl bearings. Every 8 weeks, converted from 500 run hours at 60 a week. Ref: Manual p. 23.

*June 2027*

- Monday 28 June 2027 **MIX-01** Grease bowl bearings. Every 8 weeks, converted from 500 run hours at 60 a week. Ref: Manual p. 23.

*July 2027*

- Sunday 4 July 2027 **CHL-01** Clean condenser coil. Every 3 months. Ref: Manual p. 9.
- Tuesday 6 July 2027 **MIX-01** Check drive belt tension and wear. Every quarter, proposed from history; maker's interval 6 months. Ref: Manual p. 22.
- Wednesday 14 July 2027 **OVN-01** Clean and inspect burners and flues. Every 6 months. Ref: Manual s. 7.2. Safety-critical: interval for the competent person to confirm.

*August 2027*

- Monday 23 August 2027 **MIX-01** Grease bowl bearings. Every 8 weeks, converted from 500 run hours at 60 a week. Ref: Manual p. 23.

*September 2027*

- None beyond the weekly and monthly tasks.

*October 2027*

- Monday 4 October 2027 **CHL-01** Clean condenser coil. Every 3 months. Ref: Manual p. 9.
- Wednesday 6 October 2027 **MIX-01** Check drive belt tension and wear. Every quarter, proposed from history; maker's interval 6 months. Ref: Manual p. 22.
- Monday 18 October 2027 **MIX-01** Grease bowl bearings. Every 8 weeks, converted from 500 run hours at 60 a week. Ref: Manual p. 23.
- Tuesday 26 October 2027 **WRP-01** Replace jaw heater elements. Every 40 weeks, converted from 2,000 run hours at 50 a week. Ref: Manual 5.6.

*November 2027*

- Monday 8 November 2027 **CMP-01** Change oil and air filter. Every 33 weeks, converted from 2,000 run hours at 60 a week. Ref: Manual p. 15. Safety-critical: interval for the competent person to confirm.

*December 2027*

- Monday 13 December 2027 **MIX-01** Grease bowl bearings. Every 8 weeks, converted from 500 run hours at 60 a week. Ref: Manual p. 23.

*January 2028*

- None beyond the weekly and monthly tasks.

*Left off the calendar (run to failure):* **SLC-01** Sharpen or replace blades, every 6 months.

*Assets with no maker's tasks:* None.

**4. Spare parts to hold**

- Drive belt set for MIX-01 (band A). Used 3 in the last 12 months; lead time 10 days; use during the lead time 0.08. Hold at least 1. On hand 1: enough.
- Bowl bearing grease cartridge for MIX-01 (band A). Used 7 in the last 12 months; lead time 5 days; use during the lead time 0.10. Hold at least 1. On hand 4: enough.
- Burner igniter for OVN-01 (band A). Used 0 in the last 12 months; lead time 21 days; use during the lead time 0.00. Hold at least 1 (band A minimum). On hand 0: short 1, \$95.
- Oven door seal kit for OVN-01 (band A). Used 1 in the last 12 months; lead time 14 days; use during the lead time 0.04. Hold at least 1. On hand 0: short 1, \$240.
- Condenser fan motor for CHL-01 (band B). Used 0 in the last 12 months. Lead time not stated: minimum not worked out.
- Jaw heater element for WRP-01 (band B). Used 1 in the last 12 months; lead time 28 days; use during the lead time 0.08. Hold at least 1. On hand 2: enough.
- Film sensor for WRP-01 (band B). Used 1 in the last 12 months; lead time 14 days; use during the lead time 0.04. Hold at least 1. On hand 0: short 1, \$310.
- Cutting knife for WRP-01 (band B). Used 26 in the last 12 months; lead time 21 days; use during the lead time 1.50. Hold at least 2. On hand 1: short 1, \$22.
- Compressor oil, 5 litres, for CMP-01 (band A). Used 2 in the last 12 months; lead time 3 days; use during the lead time 0.02. Hold at least 1. On hand 1: enough.
- Air filter element for CMP-01 (band A). Used 2 in the last 12 months; lead time 7 days; use during the lead time 0.04. Hold at least 1. On hand 0: short 1, \$38.
- Slicer blade set for SLC-01 (band C). Used 2 in the last 12 months; lead time 10 days; use during the lead time 0.05. Hold at least 1. On hand 1: enough.

To buy, for the operations manager's approval: burner igniter, 1, \$95; oven door seal kit, 1, \$240; film sensor, 1, \$310; cutting knife, 1, \$22; air filter element, 1, \$38. Total \$705. Nothing has been ordered.

Parts for assets not on the register: None.

**5. Downtime and repair-time measures**

Baseline from the history, Monday 5 January 2026 to Sunday 3 January 2027:

- **OVN-01:** no failures in 3,640 run hours.
- **MIX-01:** 3 failures; 18 h stopped (average 6.0 h); repair 13 h (average 4.3 h); 3,120 run hours, 1,040 run hours between failures; parts and labour \$3,000.
- **CHL-01:** no failures in 8,736 run hours.
- **CMP-01:** no failures in 3,120 run hours.
- **WRP-01:** 2 failures; 8 h stopped (average 4.0 h); repair 5 h (average 2.5 h); 2,600 run hours, 1,300 run hours between failures; parts and labour \$1,060.
- **SLC-01:** 1 failure; 2 h stopped (average 2.0 h); repair 1 h (average 1.0 h); 2,080 run hours, 2,080 run hours between failures; parts and labour \$180.
- **All registered assets:** 6 failures; 28 h stopped (average 4.7 h); repair 19 h (average 3.2 h); parts and labour \$4,240.

History items, not counted above: PAL-01, Tuesday 3 March 2026, battery fault.

To track from Monday 4 January 2027, recorded by the maintenance technician, reviewed monthly by the operations manager:

1. Unplanned stoppages each month. Baseline: 6 in the history period.
2. Hours stopped by failures each month. Baseline: 28 h in the history period.
3. Average hours stopped per failure. Baseline: 4.7 h.
4. Average repair time per failure. Baseline: 3.2 h.
5. Run hours between failures, each band A and band B asset. Baseline: OVN-01 no failure in 3,640; MIX-01 1,040; CHL-01 no failure in 8,736; CMP-01 no failure in 3,120; WRP-01 1,300.
6. Calendar tasks done by their due date, as a share of the tasks due that month. Baseline: none in the inputs.

Targets: set by the operations manager; none proposed in this draft.

**6. For the competent person: safety-critical equipment**

- **OVN-01** Four-deck gas oven. Tasks at the maker's intervals: clean and inspect burners and flues, every 6 months, next due Thursday 14 January 2027; service and safety check of the gas system, every 12 months, next due Wednesday 20 January 2027; check door seals and hinges, every month, next due Thursday 21 January 2027. Failures in the history: none. Spare parts short: burner igniter, oven door seal kit. No flag. To confirm: each interval, and the plan for this asset, before anyone relies on it.
- **CMP-01** Air compressor 7.5 kW. Tasks at the maker's intervals: drain the receiver, every week, next due Thursday 7 January 2027; inspection of the pressure system, every 12 months, next due Tuesday 9 March 2027; change oil and air filter, every 2,000 run hours, which is every 33 weeks at 60 run hours a week, next due Monday 22 March 2027. Failures in the history: none. Spare parts short: air filter element. No flag. To confirm: each interval, and the plan for this asset, before anyone relies on it.

**7. Decisions: 3**

1. **MIX-01, interval proposed from history.** The history has three drive-belt failures, on 17 February, 23 June and 6 October 2026: 126 and 105 days apart, an average of 115.5 days. The maker sets the belt check at every 6 months (182 days), so the plan carries it every quarter (91 days) from Wednesday 6 January 2027. Keep the quarterly check, or return to the maker's 6 months? For: operations manager.
2. **CHL-01, condition check has no limit, overdue, no record, part lead time not stated.** The register gives the chiller's check as "refrigerant suction pressure, limit not known", so the chiller is scheduled, not condition-based. Cleaning the condenser coil was last done on 12 May 2026 at every 3 months, was due on Wednesday 12 August 2026, and is now on the plan start. The door gasket and heater check has no last done date and is also on the plan start. The condenser fan motor has no lead time on the parts list. What limit should the suction pressure check use? Can the coil be cleaned on Monday 4 January 2027, or on which date? When was the gasket and heater check last done? What is the fan motor's lead time? For: operations manager.
3. **PAL-01, history item.** The history has a stoppage on Tuesday 3 March 2026 for PAL-01 (battery fault, 1 h stopped, 1 h repair, \$150 parts and labour), and PAL-01 is not on the register. Should PAL-01 be added to the register with its maker's tasks, or left out of the plan? For: operations manager.

**8. Things to check**

- SLC-01: the failure on Monday 20 July 2026 was a blade guard switch, a guard, but the register marks the slicer not safety-critical, so the plan runs it to failure. Should the slicer, or its guard switch, be marked safety-critical? (Failure history and equipment register.)
- WRP-01: the film sensor fault on Tuesday 8 September 2026 links to no maker's task, and the wrapper is band B. Does the maker's guidance give a check for the film sensor that should go on the calendar? (Failure history and maker's tasks.)
- MIX-01: "Check drive belt tension and wear" was last done on Tuesday 6 October 2026, the day the drive belt snapped. Was the check done that day, or is that date the repair? The quarterly check is dated from it. (Maker's tasks and failure history.)
- WRP-01: "Replace jaw heater elements" was last done on Tuesday 14 April 2026, the day a heater element failed. Was the task done that day, or is that date the repair? The 40-week replacement is dated from it. (Maker's tasks and failure history.)

Draft for the operations manager. Intervals for safety-critical equipment are confirmed and signed by the competent person; this plan is not an engineering sign-off. Inspection duties set by law differ by country and by type of equipment; the competent person confirms which apply. Nothing has been ordered, booked, sent or changed in any system.
