# Client service level report: an invented example

*Illustrative example with invented data.* The business, the client, the contract, the people, the records, the fees and every date below are invented. The business is an invented 40-person managed IT services provider that runs a service desk and a hosted platform for its clients. Its client appears as Client A, and the contract as Managed service agreement MSA-A. People appear by role only. All times are US Pacific time. The service desk system sets the due time of each priority 2 incident from business hours of 08:00 to 18:00, Monday to Friday.

October 2026 has closed. On the morning of Monday 2 November 2026 the service coordinator exported the month's records and ran the report for the service delivery manager. The inputs come first, in full, so the workflow template can be run on them. The draft report it returned follows.

## The inputs

### 1. Settings (typed by the service coordinator)

```
Client: Client A
Contract: Managed service agreement MSA-A, Schedule 3, version of 1 March 2026
Report period: October 2026 (1 to 31 October 2026)
Records exported: 2 November 2026 09:00
Today: Monday 2 November 2026
Time zone: US Pacific time
Runs it: Service coordinator
Service delivery manager: Service delivery manager
Confirms credits with the service delivery manager: Finance lead
Approves and sends the report: Account manager
Fees for October 2026: monthly service fee 24,000 USD; monthly hosting fee 6,500 USD
Credit cap: total service credits in any month are capped at 10% of the monthly service fee (Schedule 3, paragraph 5.2)
Quarters: calendar
```

### 2. Service level schedule (written by the service delivery manager from Schedule 3 of the contract)

```
sl_id,service_level,type,target,better,measurement_period,service_minutes,excluded_reasons,credit_form,credit_value,credit_base,credit_terms,contract_ref
SL1,Priority 1 incident response within 30 minutes,on-time,95.0,higher,month,,awaiting client,percent of fee,5,monthly service fee,"A service credit of 5% of the Monthly Service Fee applies for any month in which this service level is not met.","Schedule 3, paragraph 2.1"
SL2,Priority 2 incident resolution within 8 business hours,on-time,90.0,higher,month,,awaiting client,percent of fee,3,monthly service fee,"A service credit of 3% of the Monthly Service Fee applies for any month in which this service level is not met.","Schedule 3, paragraph 2.2"
SL3,Hosted platform availability,availability,99.5,higher,month,24x7,planned maintenance,other,,monthly hosting fee,"For each 0.1% (or part of 0.1%) by which availability falls below 99.5% in a month, a service credit of 2% of the Monthly Hosting Fee applies, up to 10% of that fee.","Schedule 3, paragraph 2.3"
SL4,Monthly patching report delivered by the fifth working day,on-time,100.0,higher,month,,,none,,,,"Schedule 3, paragraph 2.4"
SL5,Client satisfaction score of at least 4.2 out of 5,supplied,4.2,higher,month,,,none,,,,"Schedule 3, paragraph 2.5"
SL6,Disaster recovery test completed by the end of each quarter,on-time,100.0,higher,quarter,,,percent of fee,2,monthly service fee,"A service credit of 2% of the Monthly Service Fee applies for any quarter in which this service level is not met.","Schedule 3, paragraph 2.6"
```

### 3. Service records export: service_records.csv

```
record_id,sl_id,opened,due,done,excluded_reason,cause_note
INC-4101,SL1,2026-10-02 08:14,2026-10-02 08:44,2026-10-02 08:31,,
INC-4103,SL2,2026-10-02 09:00,2026-10-02 17:00,2026-10-02 15:42,,
INC-4109,SL2,2026-10-05 08:30,2026-10-05 16:30,2026-10-05 16:05,,
INC-4117,SL1,2026-10-05 22:40,2026-10-05 23:10,2026-10-05 22:58,,
RPT-0926,SL4,2026-10-01 00:00,2026-10-07 17:00,2026-10-06 15:20,,
INC-4121,SL2,2026-10-07 09:20,2026-10-07 17:20,2026-10-07 13:48,,
INC-4128,SL2,2026-10-08 08:10,2026-10-08 16:10,2026-10-09 10:25,awaiting client,Waiting on the client to approve a firewall change from 11:00 on 8 October; approval arrived at 08:55 on 9 October.
INC-4133,SL1,2026-10-09 11:02,2026-10-09 11:32,2026-10-09 11:20,,
INC-4136,SL2,2026-10-12 09:45,2026-10-12 17:45,2026-10-12 17:10,,
INC-4144,SL2,2026-10-13 08:00,2026-10-13 16:00,2026-10-13 14:22,,
INC-4150,SL1,2026-10-14 02:10,2026-10-14 02:40,2026-10-14 03:05,,On-call engineer's phone had no signal; the second page reached the backup engineer at 02:55.
INC-4152,SL2,2026-10-15 09:05,2026-10-15 17:05,2026-10-16 11:40,third-party vendor delay,The replacement licence key from the software vendor arrived the next morning.
INC-4162,SL1,2026-10-17 15:45,2026-10-17 16:15,2026-10-17 15:59,,
INC-4160,SL2,2026-10-19 08:45,2026-10-19 16:45,2026-10-19 12:30,,
INC-4171,SL2,2026-10-21 09:30,2026-10-21 17:30,2026-10-21 16:58,,
INC-4178,SL1,2026-10-22 09:30,2026-10-22 10:00,2026-10-22 09:41,,
INC-4183,SL2,2026-10-23 08:20,2026-10-23 16:20,2026-10-23 15:15,,
INC-4185,SL7,2026-10-24 10:12,2026-10-27 10:12,2026-10-26 16:40,,
INC-4189,SL1,2026-10-26 19:05,2026-10-26 19:35,2026-10-26 19:33,,
INC-4191,SL2,2026-10-28 10:00,2026-10-28 18:00,2026-10-28 17:21,,
INC-4196,SL1,2026-10-30 07:50,2026-10-30 08:20,2026-10-30 08:12,,
INC-4199,SL2,2026-10-30 16:00,2026-11-02 14:00,,,
```

### 4. Outage log export: outages.csv

```
outage_id,sl_id,start,end,excluded_reason,cause_note
O-0,SL3,2026-09-30 23:30,2026-10-01 00:20,,Utility power work at the data centre; the notice reached us after the work began.
O-1,SL3,2026-10-04 01:00,2026-10-04 03:00,planned maintenance,Quarterly platform update in the notified window.
O-2,SL3,2026-10-21 13:12,2026-10-21 17:40,,Storage controller failed; service restored on the paired unit.
O-3,SL3,2026-10-27 09:05,2026-10-27 09:20,,
```

### 5. Supplied figures

```
sl_id,value,source,as_of
SL5,4.4,"Client satisfaction survey export, October 2026, 23 responses",2026-10-31
```

### 6. Action list

```
action_id,sl_id,action,owner,due,status
A1,SL1,Add a backup engineer to the priority 1 paging rota,Service desk lead,2026-10-09,Done
A2,SL3,Replace the failed storage controller and check the controller in the paired unit,Infrastructure lead,2026-10-30,In progress
```

### 7. Last period's results (from the September 2026 report)

```
sl_id,period,result,status
SL1,2026-09,93.3,MISSED
SL2,2026-09,92.3,MET
SL3,2026-09,99.97,MET
SL4,2026-09,100.0,MET
SL5,2026-09,4.3,MET
SL6,2026-09,100.0,MET
```

## The output

**CLIENT SERVICE LEVEL REPORT: Client A, Managed service agreement MSA-A, October 2026**

**For:** Service delivery manager. Prepared Monday 2 November 2026 from the service level schedule (6 service levels, written from Managed service agreement MSA-A, Schedule 3, version of 1 March 2026); service_records.csv (22 rows) and outages.csv (4 rows), as exported 2 November 2026 09:00 (US Pacific time); supplied figures (1); the action list (2 actions); last period's results (September 2026).

**Overall:** 3 met, 2 missed, 0 no events, 1 not measured this period. Met only with a claimed exclusion: SL2.

**Performance by service level**

- **SL1 Priority 1 incident response within 30 minutes** (Schedule 3, paragraph 2.1): 87.5% against a target of 95.0% (higher is better). **MISSED.** Last period (September 2026): 93.3%, MISSED. Missed two periods running.
- **SL2 Priority 2 incident resolution within 8 business hours** (Schedule 3, paragraph 2.2): 90.0% against a target of 90.0% (higher is better). **MET.** Last period (September 2026): 92.3%, MET.
- **SL3 Hosted platform availability** (Schedule 3, paragraph 2.3): 99.32% against a target of 99.5% (higher is better). **MISSED.** Last period (September 2026): 99.97%, MET.
- **SL4 Monthly patching report delivered by the fifth working day** (Schedule 3, paragraph 2.4): 100.0% against a target of 100.0% (higher is better). **MET.** Last period (September 2026): 100.0%, MET.
- **SL5 Client satisfaction score of at least 4.2 out of 5** (Schedule 3, paragraph 2.5): 4.4 against a target of 4.2 (higher is better). **MET.** Last period (September 2026): 4.3, MET.
- **SL6 Disaster recovery test completed by the end of each quarter** (Schedule 3, paragraph 2.6): no result this period against a target of 100.0% (higher is better). **NOT MEASURED:** measured each quarter; due in the report for December 2026. Last period (September 2026): 100.0%, MET.

**How each result was worked out**

- **SL1:** 7 met of 8 counted = 87.5%. From service_records.csv: 8 rows for SL1, 8 due in the period.
- **SL2:** 9 met of 10 counted = 90.0%. From service_records.csv: 12 rows for SL2, 11 due in the period, 1 excluded (INC-4128), 1 due after the period (INC-4199).
- **SL3:** service minutes 31 × 1,440 = 44,640. Counted outage minutes 20 + 268 + 15 = 303. (44,640 − 303) ÷ 44,640 × 100 = 99.32%. Downtime the target allows: 223.2 minutes. Excluded: O-1, 120 minutes.
- **SL4:** 1 met of 1 counted = 100.0%. From service_records.csv: 1 row for SL4, 1 due in the period.
- **SL5:** 4.4, as supplied: Client satisfaction survey export, October 2026, 23 responses, 31 October 2026. Not recomputed.
- **SL6:** not measured: measured each quarter; due in the report for December 2026.

**Misses and what the records show**

- **SL1 Priority 1 incident response within 30 minutes:** 87.5% against 95.0%. Short by: 1 more record on time would have met the target (8 of 8, 100.0%).
  - INC-4150, due 14 October 2026 02:40, done 14 October 2026 03:05, 25 minutes late: "On-call engineer's phone had no signal; the second page reached the backup engineer at 02:55."
- **SL3 Hosted platform availability:** 99.32% against 99.5%. Short by: 79.8 minutes more downtime than the target allows (303 counted, 223.2 allowed).
  - O-0, 30 September 2026 23:30 to 1 October 2026 00:20, 20 minutes counted (30 fell outside the period): "Utility power work at the data centre; the notice reached us after the work began."
  - O-2, 21 October 2026 13:12 to 17:40, 268 minutes counted: "Storage controller failed; service restored on the paired unit."
  - O-3, 27 October 2026 09:05 to 09:20, 15 minutes counted: cause not recorded.

**Exclusions claimed**

- INC-4128 (SL2), "awaiting client": on the schedule's list; left out, to be confirmed. Without the exclusion, SL2 would be 81.8%, MISSED. The status depends on it. See question 3.
- INC-4152 (SL2), "third-party vendor delay": not on the schedule's list; counted as missed, due 15 October 2026 17:05, done 16 October 2026 11:40, 18 hours 35 minutes late: "The replacement licence key from the software vendor arrived the next morning." See question 2.
- O-1 (SL3), "planned maintenance", 120 minutes: on the schedule's list; left out, to be confirmed. Without the exclusion, SL3 would be 99.05%, MISSED.

**Credits that may apply, to be confirmed by the service delivery manager with the finance lead**

- SL1, missed: 5% of the monthly service fee (Schedule 3, paragraph 2.1): 5% × 24,000 USD = 1,200 USD. May apply.
- SL3, missed: not worked out; for the finance lead to work out. The schedule copies the contract's terms (Schedule 3, paragraph 2.3) as: "For each 0.1% (or part of 0.1%) by which availability falls below 99.5% in a month, a service credit of 2% of the Monthly Hosting Fee applies, up to 10% of that fee." See question 5.
- SL2, only if the exclusion of INC-4128 is not confirmed: 3% × 24,000 USD = 720 USD.

Total worked out: 1,200 USD; 1,920 USD including credits marked "only if". Cap (Schedule 3, paragraph 5.2): 10% × 24,000 USD = 2,400 USD; both totals are within the cap; the cap check is incomplete because SL3 is not worked out.

No credit has been offered, applied or invoiced.

**Corrective actions**

- SL1: A1 Add a backup engineer to the priority 1 paging rota, owner Service desk lead, due 9 October 2026, Done.
- SL1: No open action recorded. See question 6.
- SL3: A2 Replace the failed storage controller and check the controller in the paired unit, owner Infrastructure lead, due 30 October 2026, In progress, OVERDUE. See question 7.

**Records left out**

- service_records.csv: 1 row due after the period (INC-4199); 1 row for a service level not on the schedule (INC-4185, see question 1).
- outages.csv: O-0: 30 of its 50 minutes fell outside the period.

**Questions for the service delivery manager**

1. INC-4185 is recorded against SL7, which the schedule does not list, and was left out of every count. Does the contract have a service level SL7 that is missing from the schedule, or is the record's service level wrong?
2. INC-4152 (SL2) was resolved 18 hours 35 minutes after its due time and claims "third-party vendor delay", which is not on the schedule's list of exclusions for SL2, so it was counted as missed. SL2 is met whether or not INC-4152 is excluded, as long as INC-4128 stays excluded. Should the record keep that reason, or does the contract allow an exclusion the schedule leaves out?
3. INC-4128 (SL2) is left out as "awaiting client", a reason on the schedule's list. With it left out SL2 is 90.0% and met; counted, SL2 is 81.8% and missed, and a credit of 720 USD may apply. Do the records support the exclusion?
4. O-3 (SL3), 15 minutes on 27 October 2026, has no cause recorded. What caused it?
5. The SL3 credit is in a form this report does not work out, so its terms are quoted above, and the cap check is incomplete without it. What credit, if any, does the finance lead confirm for SL3, and does the cap in paragraph 5.2 cover it?
6. SL1 is missed two periods running. Its only action, A1, is done, and no open action is recorded. What action is agreed for SL1, who owns it, and by when?
7. A2 (SL3), replacing the failed storage controller, was due on 30 October 2026 and is in progress. What is its new due date?

Draft for the service delivery manager's review. Every result traces to the records named above. Nothing has been sent to the client, no credit has been offered or applied, and no record has been changed.
