# Trial: Project status report, run on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Opus 5.5 (model ID claude-opus-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in [public/example.md](example.md): the settings, the milestone plan, the four workstream updates, the last report and the project lead's notes. No client data was used. The assistant followed the instruction block and the output format in the template as they stand after the revisions described below.

This is the third run on the example, all on the same day in the same product. The first, with Claude Sonnet 5.5, found the open points that led to the first revisions: no stated order for the dates at risk, no stated way to write a forecast with two branches, no rule for how much overlap makes "amber again, same reason", no place in the Next line for "past due", no check on the milestone count, and no measure for the one-page limit. The second, with Claude Opus 5.5, settled those and left others, which an independent review then took up. After that review the template gained two gaps (a blocker with no workaround and no date for clearing it; a decision option with no forecast for a milestone further down the chain), a rule for which workstream a sponsor decision counts against, and a stated date style; the example's last report now gives the licence blocker as one of Reporting's reasons and names the workstream of its open decision. Two edits made after the second run (the order in which the draft is shortened, and the 800-word limit as a setting) had not been run; this run uses them. The records of the earlier runs are replaced by this one.

This run is not a blind one. It was made by the model that applied the revisions, after reading the published example's output and the record of the second run. Agreement with the published example is therefore weak evidence; the useful findings are where the instructions still left a choice.

## What came out

The full output, as returned. The word count of the sponsor's part is discussed below.

```
PROJECT STATUS REPORT: New project-accounting system, Monday 9 to Friday 13 November 2026
DRAFT for the Operations manager's confirmation. Not for sending until every colour is confirmed.

For: Managing director. Report date: Friday 13 November 2026. Next report: Friday 20 November 2026. End date: Monday 4 January 2027.
Prepared from: the milestone plan (12 milestones, 4 workstreams); updates from 4 of 4 workstreams; the last report of 6 November 2026; the project lead's notes; default rules.

OVERALL: RED (was AMBER). Red because the trial load (A2) is past due and incomplete, and if it finishes on 18 November the reporting milestones are forecast for 2 and 9 December; go-live on 4 January 2027 holds, per the project lead's notes; two sponsor decisions are needed, by 18 and 20 November.

DECISIONS NEEDED FROM THE SPONSOR: 2
1. Will you approve four more days of the data contractor at $950 a day ($3,800), or should the Data lead fix the six failed projects in-house? Needed by Wednesday 18 November. What moves: with the contractor days, A2 is done on 18 November and A3 holds at 4 December; in-house, A2 is done on 25 November and A3 moves to 11 December. Options given: approve the four days; the Data lead fixes the six in-house. Recommendation: Data lead: approve the days.
2. Should standard rates be loaded now for Client F, Client K and Client M and corrected before go-live, or should B3 wait for their rate cards? Needed by Friday 20 November. What moves: B3 holds at 27 November if by 20 November there are either the rate cards or the go-ahead for standard rates. Options given: load standard rates now and correct them before go-live; hold B3 until the rate cards arrive. Recommendation: Billing lead: load standard rates now.
Settled since last report: partners get their own training session, by the Managing director, 10 November.

DATES AT RISK: 5, earliest date first
A2 Trial load of open projects (Data migration). Due 10 November. Past due. Forecast 18 November, if the contractor days are approved; 25 November, if fixed in-house. Waiting on it: A3, D2.
D2 Project profitability report built and checked (Reporting). Due 18 November. Forecast 2 December, if A2 is done on 18 November. Waiting on it: D3.
D3 Partners sign off the report pack (Reporting). Due 25 November. Forecast 9 December, if A2 is done on 18 November. Waiting on it: nothing.
B3 Rates loaded for all clients (Billing set-up). Due 27 November. Forecast 27 November, if the rate cards or the go-ahead for standard rates come by 20 November. Waiting on it: nothing.
A3 Final load rehearsal (Data migration). Due 4 December. Forecast 4 December, if the contractor days are approved; 11 December, if fixed in-house. Waiting on it: nothing.
End date 4 January 2027: holds, per the project lead's notes.

WORKSTREAMS
Data migration: RED (was GREEN). Lead: Data lead.
  Why: A2 is past due and not done; a blocker has no workaround.
  Moved: 412 of 418 open projects loaded in the trial load of 9 November (trial load log).
  Next: A2 Trial load of open projects, due 10 November, past due, forecast 18 November, if the contractor days are approved; 25 November, if fixed in-house.
Billing set-up: AMBER (was AMBER). Lead: Billing lead.
  Why: a blocker is open with a workaround; decision 2 is needed by the next report date.
  Moved: B2 Invoice templates approved, done 9 November (finance lead's approval email).
  Next: B3 Rates loaded for all clients, due 27 November, forecast 27 November, if the rate cards or the go-ahead for standard rates come by 20 November.
Training: GREEN (was GREEN). Lead: Training lead.
  Why: no red or amber rule applies.
  Moved: four of six sessions booked with trainers, 24 November to 1 December (booking confirmations); the trainer confirms sessions 5 and 6 by 18 November.
  Next: C2 Trainers booked for all six sessions, due 20 November, forecast 20 November.
Reporting: AMBER (was AMBER). Lead: Reporting lead.
  Why: D2 is forecast later than its date; a blocker is open with a workaround.
  Moved: Nothing moved this period.
  Next: D2 Project profitability report built and checked, due 18 November, forecast 2 December, if A2 is done on 18 November.

BLOCKERS: 3
1. Two more report-tool licences for the partners; nobody has been asked to buy them (Reporting). Resolver: not named. Open 7 days. Workaround: partners read a shared PDF of the report.
2. Rate cards for Client F, Client K and Client M not received (Billing set-up). Resolver: Commercial director. Open 11 days. Workaround: load standard rates now and correct them before go-live. Long-open, over 7 days: raise with the sponsor.
3. Six open projects cannot load: duplicate client codes (Data migration). Resolver: Finance lead, to choose which code to keep. Open 3 days. Workaround: none.

FOR THE OPERATIONS MANAGER ONLY. Remove before sending.
Not reported as done: 1
  A2 Trial load of open projects: claimed done by the Data lead. Evidence required: all open projects loaded in the test system and the error list reviewed by the finance lead. Evidence supplied: trial load log of 9 November, 412 of 418 open projects loaded; the same update says the finance lead reviews the error list on 18 November, so the review has not happened. Left open.
Colours to confirm: 5
  1. Data migration: RED. The Data lead proposed GREEN; the rules give red (A2 past due and not done; a blocker with no workaround), so red is kept. Confirm or change: [ ]
  2. Billing set-up: AMBER. Amber again, same reason: the rate-card blocker, open with a workaround, as in the last report. New this period: decision 2, needed by 20 November. Is it now red? Confirm or change: [ ]
  3. Training: GREEN. No doubt raised. Confirm or change: [ ]
  4. Reporting: AMBER. Amber again, same reason: D2 forecast later than its date and the licence blocker open with a workaround, both as in the last report. No new reason this period. Is it now red? Confirm or change: [ ]
  5. Overall: RED, the worst workstream colour. No doubt raised. Confirm or change: [ ]
Gaps to fill: 3
  1. Who will clear the report-tool licence blocker? No resolver has been named since it was raised on 6 November.
  2. By when will the Finance lead choose which client code to keep for the six projects? The duplicate-code blocker has no workaround and no date is given for clearing it.
  3. If the Data lead fixes the six in-house and A2 is done on 25 November, what are the forecasts for D2 and D3, and does go-live on 4 January 2027 still hold? No update gives them for that option.
Confirmed by: [ ]  Date: [ ]
Prepared for the Operations manager's confirmation. Nothing has been sent, marked done or changed in any plan or record.
```

## What was observed

**Every required part was produced.** Header, overall line, decisions, dates at risk, end date, four workstreams, blockers, and the project lead's part (not reported as done, colours to confirm, gaps, sign-off line). No stop condition applied: the plan's headings matched, no ID repeated, every workstream sent an update, and the last report and the lead's notes were supplied.

**Colours, counts and order.** Overall red (was amber); Data migration red, with the Data lead's green proposal kept apart for the project lead; Billing set-up and Reporting amber, each flagged "amber again, same reason"; Training green. Two decisions, five dates at risk in date order (A2, D2, D3, B3, A3), three blockers, one milestone not reported as done (A2), three gaps. Recounted before returning: 12 milestones, 4 workstreams, and each section's number matches its lines. Day counts recomputed: 11 days from 2 November, 7 from 6 November, 3 from 10 November. The licence blocker, open exactly 7 days, is not marked long-open.

**What the revisions changed in this run:**

- Reporting is amber again for the same two reasons the last report gave, D2 forecast late and the licence blocker, so there is no new reason to name and the awkward wording of the second run ("new as a reason this period") is gone.
- The gaps now include the two the second run left out: by when the Finance lead will settle the duplicate codes (a blocker with no workaround and no date for clearing it), and the forecasts for D2 and D3, and whether go-live holds, if the six projects are fixed in-house.
- Dates in the body are day and month, with the year only on 4 January 2027; full dates appear only in the title and header lines.
- Each open decision counts against the workstream whose update raised it: decision 1 against Data migration, decision 2 against Billing set-up. The decision carried from the last report names Training and was settled on 10 November, so the rule for a decision with no workstream was not exercised.

**The word limit.** The sponsor's part, from the title line to the last blocker, came to 799 words by a word-count tool on the first full draft, under the limit of 800, so nothing was shortened and the order of shortening in the instructions was not exercised. The draft's wording is close to the tightened wording of the second run, which this model had read; a fresh run might well come out longer. The published example comes to 794. The limit is tight for a four-workstream project with two forecasts that branch on a decision.

**Where the instructions still left a choice:**

- The duplicate-code blocker's date. The Data lead's contractor forecast has the six reloaded by 17 November, which implies the codes are chosen before then, but no update gives a date for the Finance lead's choice. I counted that as no date given and raised the gap.
- Decision 2's second option. If B3 waits for the rate cards, the update forecasts 27 November provided they arrive by 20 November and gives nothing for a later arrival. I counted a forecast with a condition as a forecast given, so no gap; a stricter reading would ask when B3 lands if the cards come late.
- Whether the end date holds. The lead's notes say it does, and no source forecasts it to move, so the red rule for the end date was not applied. Under the in-house option it is now asked as a gap.
- C2 depends on the trainer confirming sessions 5 and 6 by 18 November. The Training lead lists no blocker, so C2 is not at risk. That follows the update's words; a stricter reader might call it a risk.
- The resolver for the duplicate-code blocker comes from the update's prose ("the finance lead has to choose"), not from a labelled field.
- The headline is one sentence held together by semicolons, at about fifty words. The instructions ask for one sentence and set no length.

**Differences from the published example:** the same colours, counts, order, day counts and gaps. The wording differs: the period with weekdays in the header; the headline names the December dates and says "two sponsor decisions are needed" where the example speaks to the sponsor; decision 1 is written as a choice between the two options; the End date line has no weekday; the A2 entry under "Not reported as done" quotes the 18 November review date; shorter blocker descriptions; and the colour notes and gaps are worded differently.

**Facts not in the inputs.** None found. Every date, figure, role and quotation traces to the settings, plan, updates, last report or notes.

**The acceptance tests.** The example happens to contain the cases of tests 3 (partial evidence, 412 of 418), 4 (a greener proposal), 5 (amber again), 6 (a blocker with no resolver), 7 (a long-open blocker at 11 days), 14 (a blocker with no date to clear it) and 15 (an option with no forecast further down the chain), and the run handled each as the tests expect. That is not a run of the tests.

## Edit made after this run

Not run again: the list of gaps in the instructions now also names a date an update gives for a milestone not in the plan, which the instructions already sent to the gaps elsewhere. The example has no such date, so this run's output would not change.

## Shortcomings of the trial

One recorded run, by one model, on one example, made by the model that revised the template and had already seen the expected output. It shows that the revised instructions settle the points the second run and its review left open, and that this example sits right at the word limit. It does not exercise the order of shortening, a decision with no workstream, or the other acceptance tests the example does not contain, and it does not show how the template behaves on a real project, on a messy export or in another product.
