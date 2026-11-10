# Project status report: an invented example

*Illustrative example with invented data.* The firm, its people, its clients, the project and every date and figure below are invented. The firm is an invented 90-person engineering consultancy replacing its project-accounting system, with go-live set for January. The project lead is the operations manager and the sponsor is the managing director; people are named by role only, and clients by letter. First come the five inputs the operations manager supplied, in full, then the draft the capability returned.

## The inputs

### 1. Settings

```
Project: New project-accounting system
Sponsor: Managing director
Project lead: Operations manager
Period: Monday 9 to Friday 13 November 2026 (weekly)
Report date: Friday 13 November 2026
Next report: Friday 20 November 2026
End date: go-live, Monday 4 January 2027
Colour rules: default
Long-open limit: default
```

### 2. The milestone plan (exported from the firm's project tracker)

```
ID,Workstream,Milestone,Owner,Due,Evidence required,Depends on,Agreed new due,Completed
A1,Data migration,Map old fields to the new system,Data lead,2026-10-23,Field map signed off by the finance lead,,,2026-10-22
A2,Data migration,Trial load of open projects,Data lead,2026-11-10,All open projects loaded in the test system and the error list reviewed by the finance lead,A1,,
A3,Data migration,Final load rehearsal,Data lead,2026-12-04,Rehearsal load complete and totals agreed to the old system,A2,,
B1,Billing set-up,Invoice layouts designed,Billing lead,2026-10-30,Draft layouts shared with the finance lead,,,2026-10-29
B2,Billing set-up,Invoice templates approved,Billing lead,2026-11-10,Written approval from the finance lead,B1,,
B3,Billing set-up,Rates loaded for all clients,Billing lead,2026-11-27,Every active client has rates in the test system,B2,,
C1,Training,Training plan agreed,Training lead,2026-11-04,Plan approved by the operations manager,,,2026-11-04
C2,Training,Trainers booked for all six sessions,Training lead,2026-11-20,Six sessions each with a date and a confirmed trainer,C1,,
C3,Training,All staff trained,Training lead,2026-12-18,Attendance record shows every user attended a session,C2,,
D1,Reporting,Report list agreed with partners,Reporting lead,2026-10-30,List approved in the partners' meeting notes,,,2026-10-28
D2,Reporting,Project profitability report built and checked,Reporting lead,2026-11-18,Report run on trial data and agreed to September's figures,A2,,
D3,Reporting,Partners sign off the report pack,Reporting lead,2026-11-25,Sign-off recorded in the partners' meeting notes,D2,,
```

### 3. The workstream updates (as each lead sent them)

```
DATA MIGRATION, from the Data lead
Colour I'd give: GREEN. The load basically worked.
Done: A2, I'd call it done. The trial load ran on Monday 9 November:
  412 of 418 open projects loaded (trial load log, 9 November).
Problem: the other six projects fail because their clients have
  duplicate client codes. The finance lead has to choose which code to
  keep for each. Raised Tuesday 10 November. No workaround: they cannot
  load until the codes are settled.
Forecast: with four more days of the data contractor, the six are fixed
  and reloaded by 17 November and the finance lead reviews the error
  list on 18 November, so A2 is done on 18 November and A3 holds at
  4 December. If I fix them myself, A2 is done on 25 November and A3
  moves to 11 December.
Decision for the sponsor: approve four more days of the data contractor
  at $950 a day ($3,800), or I fix the six in-house. Needed by Wednesday
  18 November. I recommend approving the days.

BILLING SET-UP, from the Billing lead
Colour I'd give: AMBER.
Done: B2. The finance lead approved the invoice templates by email on
  Monday 9 November (approval email, 9 November).
Still waiting: rate cards for three framework clients (Client F,
  Client K, Client M). Asked the commercial director on 2 November.
  Workaround: load our standard rates for them now and correct them
  before go-live.
Forecast: B3 holds at 27 November if by 20 November we have either the
  rate cards or the go-ahead to use standard rates.
Decision for the sponsor: load standard rates now for the three and
  correct them before go-live, or hold B3 until the rate cards arrive.
  Needed by Friday 20 November. I recommend loading standard rates now.

TRAINING, from the Training lead
Colour I'd give: GREEN.
Progress: sessions 1 to 4 booked with trainers for 24, 25 and
  30 November and 1 December (booking confirmations attached).
  Sessions 5 and 6 have dates offered; the trainer confirms by
  18 November. Session 6 is the partners' session.
Forecast: C2 on 20 November as planned.
Blockers: none.

REPORTING, from the Reporting lead
Colour I'd give: AMBER.
Progress: none this week; still waiting on the trial data.
Forecast: I need about two weeks after A2 is done to build and check
  the profitability report. If A2 is done on 18 November, D2 lands on
  2 December and D3, the partners' sign-off, on 9 December.
Blocker: the report tool has three user licences and the partners want
  five. Nobody has been asked to buy the extra two. Raised Friday
  6 November. Workaround: partners read a shared PDF of the report
  until then.
```

### 4. The last report (sent on Friday 6 November, shortened here to what carries over)

```
OVERALL: AMBER.
Data migration: GREEN. Why: no milestone late; the trial load is set
  for 9 November, due 10 November.
Billing set-up: AMBER. Why: a blocker is open with a workaround (rate
  cards for three framework clients).
Training: GREEN. Why: no milestone late, no blocker.
Reporting: AMBER. Why: D2 is forecast late while it waits on the trial
  data; a blocker is open with a workaround (report-tool licences).
Blockers:
  1. Rate cards for Client F, Client K and Client M (Billing set-up).
     Resolver: Commercial director. Raised 2 November.
  2. Two more report-tool licences (Reporting). Resolver: not named.
     Raised 6 November.
Decisions needed:
  1. Do partners attend the staff training sessions or a separate one?
     Workstream: Training. Needed by 13 November.
```

### 5. The project lead's notes

```
- The sponsor decided on Tuesday 10 November: partners get their own
  training session.
- All four workstream leads say go-live on 4 January still holds.
```

## The output

```
PROJECT STATUS REPORT: New project-accounting system, 9 to 13 November 2026
DRAFT for the Operations manager's confirmation. Not for sending until every colour is confirmed.

For: Managing director. Report date: Friday 13 November 2026. Next report: Friday 20 November 2026. End date: Monday 4 January 2027.
Prepared from: the milestone plan (12 milestones, 4 workstreams); updates from 4 of 4 workstreams; the last report of 6 November 2026; the project lead's notes; default rules.

OVERALL: RED (was AMBER). Red because the trial load of open projects (A2) is past due and not yet complete, and if it finishes on 18 November the reporting milestones are forecast for December; go-live on 4 January 2027 still holds, and you have two decisions to make, by 18 and 20 November.

DECISIONS NEEDED FROM THE SPONSOR: 2
1. Will you approve four more days of the data contractor at $950 a day ($3,800) to fix and reload the six projects that failed? Needed by Wednesday 18 November. What moves: with the contractor days, A2 is done on 18 November and A3 holds at 4 December; in-house, A2 is done on 25 November and A3 moves to 11 December. Options given: approve the four days; or the Data lead fixes the six in-house. Recommendation: Data lead: approve the days.
2. Should standard rates be loaded now for Client F, Client K and Client M and corrected before go-live, or should B3 wait for their rate cards? Needed by Friday 20 November. What moves: B3 holds at 27 November if, by 20 November, this is decided or the rate cards arrive. Options given: load standard rates now and correct them before go-live; hold B3 until the rate cards arrive. Recommendation: Billing lead: load standard rates now.
Settled since last report: partners get their own training session, decided by the Managing director on 10 November.

DATES AT RISK: 5, earliest date first
A2 Trial load of open projects (Data migration). Due 10 November. Past due. Forecast 18 November, if the contractor days are approved; 25 November, if fixed in-house. Waiting on it: A3, D2.
D2 Project profitability report built and checked (Reporting). Due 18 November. Forecast 2 December, if A2 is done on 18 November. Waiting on it: D3.
D3 Partners sign off the report pack (Reporting). Due 25 November. Forecast 9 December, if A2 is done on 18 November. Waiting on it: nothing.
B3 Rates loaded for all clients (Billing set-up). Due 27 November. Forecast 27 November, if decision 2 is made or the rate cards arrive by 20 November. Waiting on it: nothing.
A3 Final load rehearsal (Data migration). Due 4 December. Forecast 4 December, if the contractor days are approved; 11 December, if fixed in-house. Waiting on it: nothing.
End date Monday 4 January 2027: holds, per the project lead's notes.

WORKSTREAMS
Data migration: RED (was GREEN). Lead: Data lead.
  Why: A2 is past due and not done; a blocker has no workaround.
  Moved: trial load run on 9 November, 412 of 418 open projects loaded (trial load log, 9 November).
  Next: A2 Trial load of open projects, due 10 November, past due, forecast 18 November, if the contractor days are approved; 25 November, if fixed in-house.
Billing set-up: AMBER (was AMBER). Lead: Billing lead.
  Why: a blocker is open with a workaround; decision 2 is needed by the next report date.
  Moved: B2 Invoice templates approved, done 9 November (finance lead's approval email, 9 November).
  Next: B3 Rates loaded for all clients, due 27 November, forecast 27 November, if decision 2 is made or the rate cards arrive by 20 November.
Training: GREEN (was GREEN). Lead: Training lead.
  Why: none of the red or amber rules applies.
  Moved: four of six sessions booked with trainers, 24 November to 1 December (booking confirmations); the trainer confirms sessions 5 and 6 by 18 November.
  Next: C2 Trainers booked for all six sessions, due 20 November, forecast 20 November.
Reporting: AMBER (was AMBER). Lead: Reporting lead.
  Why: D2 is forecast later than its date; a blocker is open with a workaround.
  Moved: Nothing moved this period.
  Next: D2 Project profitability report built and checked, due 18 November, forecast 2 December, if A2 is done on 18 November.

BLOCKERS: 3
1. Two more report-tool licences for the partners (Reporting). Resolver: not named. Open 7 days. Workaround: partners read a shared PDF of the report.
2. Rate cards for Client F, Client K and Client M not supplied (Billing set-up). Resolver: Commercial director. Open 11 days. Workaround: load standard rates now and correct them before go-live. Long-open, over 7 days: raise with the sponsor.
3. Six open projects fail to load because of duplicate client codes (Data migration). Resolver: Finance lead, to choose which code to keep. Open 3 days. Workaround: none.

FOR THE OPERATIONS MANAGER ONLY. Remove before sending.
Not reported as done: 1
  A2 Trial load of open projects: claimed done by the Data lead. Evidence required: all open projects loaded in the test system and the error list reviewed by the finance lead. Evidence supplied: trial load log of 9 November, 412 of 418 open projects loaded; no review of the error list yet. Left open.
Colours to confirm: 5
  1. Data migration: RED. The Data lead proposed GREEN; the rules give RED (A2 past due and not done; a blocker with no workaround). Confirm or change: [ ]
  2. Billing set-up: AMBER. Amber again, same reason as the last report (the rate-card blocker, open with a workaround); new this period: decision 2 is needed by the next report date. Is it now red? Confirm or change: [ ]
  3. Training: GREEN. No doubt raised. Confirm or change: [ ]
  4. Reporting: AMBER. Amber again, same reasons as the last report (D2 forecast late while it waits on the trial data; the licence blocker, open with a workaround). Is it now red? Confirm or change: [ ]
  5. Overall: RED, the worst workstream colour. No doubt raised. Confirm or change: [ ]
Gaps to fill: 3
  1. Who will clear the report-tool licence blocker? No resolver has been named since it was raised on 6 November.
  2. By when will the Finance lead choose which client code to keep for the six projects that failed to load? The blocker has no workaround, and the six cannot load until the codes are settled.
  3. If the Data lead fixes the six in-house and A2 is done on 25 November, when are D2 and D3 forecast, and does go-live on 4 January 2027 still hold? The Reporting lead's forecast covers only A2 done on 18 November.
Confirmed by: [ ]  Date: [ ]
Prepared for the Operations manager's confirmation. Nothing has been sent, marked done or changed in any plan or record.
```

Every colour follows the default rules, every date comes from the plan or an update, and the day counts run from the date each blocker was raised to Friday 13 November: 11 days from 2 November, 7 from 6 November, 3 from 10 November. The licence blocker, at 7 days, is not over the default limit of 7, so only the rate-card blocker is marked long-open. The dates at risk run in date order, and the two forecasts that depend on decision 1 give both dates, each with its condition. Reporting stays amber for the same two reasons as last week, so the operations manager is asked whether it is now red. The gaps ask who owns the licence blocker, by when the duplicate codes will be settled, and what happens to the reporting milestones and go-live if the six projects are fixed in-house. The sponsor's part, from the title line to the last blocker, comes to just under the 800-word limit for one page. The operations manager answers the questions in the last part, confirms each colour, removes the last part and sends the page.
