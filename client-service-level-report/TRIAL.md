# Client service level report: one trial run on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-11

The inputs are the invented example in [`example.md`](example.md) (section "The inputs": the settings, the service level schedule, the service records, the outage log, the supplied figure, the action list and last period's results). No client data was used. This is the second run on the invented example. The first, made earlier the same day by a model that did not write the template, was given the instruction block and output format and the inputs; it found the gaps listed under "What was observed", and the block, the output format and the example were revised to close them. Its record was replaced by this one. This second run was made once, by the model that made those revisions, which had the whole template open and had read the first run's output and the example's published output before it ran. It is therefore not an independent run, and it is one run, not a test for a client. The example's published output was compared with it afterwards.

## What came out

```
CLIENT SERVICE LEVEL REPORT: Client A, Managed service agreement MSA-A, October 2026

For: Service delivery manager. Prepared Monday 2 November 2026 from the service level schedule (6 service levels, written from Managed service agreement MSA-A, Schedule 3, version of 1 March 2026); service_records.csv (22 rows) and outages.csv (4 rows), as exported 2 November 2026 09:00 (US Pacific time); supplied figures (1); the action list (2 actions); last period's results (September 2026).
Overall: 3 met, 2 missed, 0 no events, 1 not measured this period. Met only with a claimed exclusion: SL2.

Performance by service level
SL1 Priority 1 incident response within 30 minutes (Schedule 3, paragraph 2.1): 87.5% against a target of 95.0% (higher is better). MISSED. Last period (September 2026): 93.3%, MISSED. Missed two periods running.
SL2 Priority 2 incident resolution within 8 business hours (Schedule 3, paragraph 2.2): 90.0% against a target of 90.0% (higher is better). MET. Last period (September 2026): 92.3%, MET.
SL3 Hosted platform availability (Schedule 3, paragraph 2.3): 99.32% against a target of 99.5% (higher is better). MISSED. Last period (September 2026): 99.97%, MET.
SL4 Monthly patching report delivered by the fifth working day (Schedule 3, paragraph 2.4): 100.0% against a target of 100.0% (higher is better). MET. Last period (September 2026): 100.0%, MET.
SL5 Client satisfaction score of at least 4.2 out of 5 (Schedule 3, paragraph 2.5): 4.4 against a target of 4.2 (higher is better). MET. Last period (September 2026): 4.3, MET.
SL6 Disaster recovery test completed by the end of each quarter (Schedule 3, paragraph 2.6): no result this period against a target of 100.0% (higher is better). NOT MEASURED: measured each quarter; due in the report for December 2026. Last period (September 2026): 100.0%, MET.

How each result was worked out
SL1: 7 met of 8 counted = 87.5%. From service_records.csv: 8 rows for SL1, 8 due in the period.
SL2: 9 met of 10 counted = 90.0%. From service_records.csv: 12 rows for SL2, 11 due in the period, 1 excluded (INC-4128), 1 due after the period (INC-4199).
SL3: service minutes 31 x 1,440 = 44,640. Counted outage minutes 20 + 268 + 15 = 303. (44,640 - 303) / 44,640 x 100 = 99.32%. Downtime the target allows: 223.2 minutes. Excluded: O-1, 120 minutes.
SL4: 1 met of 1 counted = 100.0%. From service_records.csv: 1 row for SL4, 1 due in the period.
SL5: 4.4, as supplied: Client satisfaction survey export, October 2026, 23 responses, 31 October 2026. Not recomputed.
SL6: not measured: measured each quarter; due in the report for December 2026.

Misses and what the records show
SL1 Priority 1 incident response within 30 minutes: 87.5% against 95.0%. Short by: 1 more record on time would have met the target (8 of 8, 100.0%).
  INC-4150, due 14 October 2026 02:40, done 14 October 2026 03:05, 25 minutes late: On-call engineer's phone had no signal; the second page reached the backup engineer at 02:55.
SL3 Hosted platform availability: 99.32% against 99.5%. Short by: 79.8 minutes more downtime than the target allows (303 counted, 223.2 allowed).
  O-0, 30 September 2026 23:30 to 1 October 2026 00:20, 20 minutes counted (30 fell outside the period): Utility power work at the data centre; the notice reached us after the work began.
  O-2, 21 October 2026 13:12 to 17:40, 268 minutes counted: Storage controller failed; service restored on the paired unit.
  O-3, 27 October 2026 09:05 to 09:20, 15 minutes counted: cause not recorded. See question 4.

Exclusions claimed
INC-4128 (SL2), "awaiting client": on the schedule's list; left out, to be confirmed. Without the exclusion, SL2 would be 81.8%, MISSED. The status depends on it. See question 3.
INC-4152 (SL2), "third-party vendor delay": not on the schedule's list; counted as missed, due 15 October 2026 17:05, done 16 October 2026 11:40, 18 hours 35 minutes late: The replacement licence key from the software vendor arrived the next morning. See question 2.
O-1 (SL3), "planned maintenance", 120 minutes: on the schedule's list; left out, to be confirmed. Without the exclusion, SL3 would be 99.05%, MISSED.

Credits that may apply, to be confirmed by the service delivery manager with the Finance lead
SL1, missed: 5% of the monthly service fee (Schedule 3, paragraph 2.1): 5% x 24,000 USD = 1,200 USD. May apply.
SL3, missed: not worked out; for the Finance lead to work out. The schedule copies the contract's terms (Schedule 3, paragraph 2.3) as: "For each 0.1% (or part of 0.1%) by which availability falls below 99.5% in a month, a service credit of 2% of the Monthly Hosting Fee applies, up to 10% of that fee." See question 5.
SL2, only if the exclusion of INC-4128 is not confirmed: 3% x 24,000 USD = 720 USD.
Total worked out: 1,200 USD; 1,920 USD including credits marked "only if". Cap (Schedule 3, paragraph 5.2): 10% x 24,000 USD = 2,400 USD; both totals are within the cap; the cap check is incomplete because SL3 is not worked out.
No credit has been offered, applied or invoiced.

Corrective actions
SL1: A1 Add a backup engineer to the priority 1 paging rota, owner Service desk lead, due 9 October 2026, Done.
SL1: No open action recorded. See question 6.
SL3: A2 Replace the failed storage controller and check the controller in the paired unit, owner Infrastructure lead, due 30 October 2026, In progress, OVERDUE. See question 7.

Records left out
service_records.csv: 1 row due after the period (INC-4199); 1 row for a service level not on the schedule (INC-4185, see question 1).
outages.csv: O-0: 30 of its 50 minutes fell outside the period.

Questions for the Service delivery manager
1. INC-4185 is recorded against SL7, which the schedule does not list, and was left out of every count. Is a service level SL7 missing from the schedule, or is the record's service level wrong?
2. INC-4152 (SL2) was done on 16 October 2026 11:40, after its due time of 15 October 2026 17:05, and claims "third-party vendor delay", which is not on the schedule's list of exclusions for SL2, so it was counted as missed. SL2 is 90.0% and met with it counted, and met whether or not INC-4152 is excluded while INC-4128 stays excluded. Does the contract allow that reason, or should the record's reason change?
3. INC-4128 (SL2) is left out as "awaiting client", a reason on the schedule's list. With it left out SL2 is 90.0% and MET; counted, SL2 is 81.8% and MISSED, and a credit of 720 USD may apply. Do the records support the exclusion?
4. O-3 (SL3), 15 minutes on 27 October 2026, has no cause note. What was the cause?
5. The SL3 credit is in a form this report does not work out, so the contract's wording is quoted above, and the cap check is incomplete without it. What credit, if any, does the Finance lead confirm for SL3?
6. SL1 is missed two periods running. Its action A1 is Done, and no open action is recorded. Is another action agreed for SL1?
7. A2 (SL3) was due on 30 October 2026, is In progress, and today is 2 November 2026. What is its new due date?

Draft for the Service delivery manager's review. Every result traces to the records named above. Nothing has been sent to the client, no credit has been offered or applied, and no record has been changed.
```

## What was observed

- **Every required part was produced,** in the order the format gives. Every section had content, so no "none" line was needed. Nothing in the inputs triggered a stop: the headers matched, no id repeated, every time read in one time zone, and the export was made after the period ended.
- **Against the published output,** the results and the working are the same: 87.5%, 90.0%, 99.32%, 100.0%, 4.4 and not measured; the same two misses; the same exclusions and the same three outcomes for them; the same credits (1,200 USD, 720 USD only if the exclusion fails, SL3 not worked out), totals and cap check; the same seven questions in the same order. The differences are wording only: the published output writes the finance lead in lower case; this run adds "See question 4" to the O-3 line; this run's question 2 gives the two times where the published one gives the lateness; this run's question 6 only asks whether another action is agreed, where the published one also asks who owns it and by when.
- **The five judgments the first run had to make are now settled by the text,** and this run followed the text: the "other" credit line carries both the "for the Finance lead to work out" wording and the quoted terms; the availability shortfall is the difference (79.8 minutes, with 303 counted and 223.2 allowed); the cause note of INC-4152, a missed record under a service level that is met, appears on its Exclusions claimed line; the Overall line counts SL2 as met and lists it after the counts; and the lateness of INC-4152 is given as 18 hours 35 minutes. The rule for a cause note that names a person did not come up, because no cause note in the inputs names anyone.
- **No fact outside the inputs** was found. The only figures not typed in the inputs are ones worked out from them (for example 18 hours 35 minutes, 81.8%, 99.05%, 223.2 and 79.8 minutes).
- **The arithmetic was checked** with a small one-off calculation after the report was written. It confirmed 18 hours 35 minutes, 99.32%, 223.2 minutes, 79.8 minutes, 99.05%, 81.8%, 87.5% and the 1,200, 720 and 2,400 USD figures.
- **"Prepared [weekday date]"** was taken from the settings' "Today", not from the real date.
- **What the first run found and what was done.** The first run found the block thinner than the procedure. The block now covers an exclusion that does not change a status, the stop when the records and the schedule disagree about what a service level measures, lateness units, what goes under Records left out and the quoting of a note that names a person. This run was made with the whole template open, so it does not show that a product given only the instruction block and output format would behave the same; that has not been tried since the revision.
- **Step numbers differ** between the procedure (13 steps) and the block (12 steps). That does not affect the result.
- **The block was amended after this run,** by five small clauses (a quarterly service level counts records due in the quarter; an outage with no end time stops the run; a missing supplied figure is NOT MEASURED; a missed supplied figure with nothing supplied is "no explanation supplied"; "no open action" is worded as no action still open). None of them applies to the example's inputs, so the run was not repeated and its record is unchanged; the amended block has not been run.
- **Limits of this trial:** one run, one product, one model, not independent of the revisions, on an invented example whose inputs were written to produce these cases. It did not test the stop conditions, the refusals (for example "is this credit owed?"), the rule for a cause note that names a person or the other acceptance tests listed in the template.
