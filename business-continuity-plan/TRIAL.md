# Business continuity plan: a trial run on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in `public/example.md` (the scope brief, the activities table, the dependencies table, the roles roster, the external contacts and the notes). No client data was used. The run followed the fenced instruction block and the output format in `member/template.md`. The model that ran it did not write the template and did not read the example's output until its own draft was finished. The template's reviewer checklist and the published output were then used for the comparison below.

## What came out

The full draft, as the workflow template returned it:

```
BUSINESS CONTINUITY PLAN: Kitchen-equipment wholesaler, Warehouse and office at Unit 4

Prepared for: Operations manager. Plan owner, who approves: Owner and managing director.
Competent reviewer: External business continuity adviser.
Plan date: 10 November 2026. Next review: 10 November 2027. Next full test: not set.
Sources: scope brief; activities table, 3 rows; dependencies table, 8 rows; roles
roster, 5 rows; external contacts, 5 rows; notes of 9 November 2026
Disruptions the owner named: a fire or flood at Unit 4; the order system going down;
Courier B letting us down in peak season; Owen being off when payroll is due
Times compared in hours, a day counting as 24 hours.
Fallback proof age limit: 12 months (the default).
Activities: 3. Dependencies: 8, 2 with no fallback. Activities flagged: 3.
Roles flagged: 2. Plan-level gaps: 2. Decisions: 7.

RECOVERY ORDER
1. A1 Taking and confirming customer orders: longest tolerable outage 2 days; target 1 day.
2. A2 Picking and dispatching orders: longest tolerable outage 3 days; target 3 days.
3. A3 Paying staff and suppliers: longest tolerable outage 5 days; target 2 days.

ACTIVITIES AND DEPENDENCIES

A1. Taking and confirming customer orders. Output: Orders confirmed to customers.
  Impact over time: After 4 hours customers start phoning to chase; after 1 day trade
  customers order from competitors; after 2 days we lose the weekly orders from our
  two largest accounts
  Longest tolerable outage: 2 days. Target recovery time: 1 day
  (margin 1 day, 24 hours).
  Data loss tolerance: 4 hours.
  Dependencies:
    D1 Systems: Online order system hosted by Supplier A. Fallback: Take orders by
    phone and email on paper order forms and key them in when the system returns.
    Ready in: 2 hours. Last proven: never. Backup interval: 24 hours.
    Flag, fallback not proven, backups too far apart, no contact listed: never
    proven; backup interval 24 hours against a data loss tolerance of 4 hours; the
    order system is hosted by Supplier A, which has no external contact line.
    D2 People: Customer service team (4). Fallback: Sales staff (3) trained to take
    orders. Ready in: 4 hours. Last proven: 12 March 2026.
    D3 Premises: Office at Unit 4. Fallback: Customer service team works from home
    on company laptops. Ready in: 4 hours. Last proven: 20 June 2025.
    Flag, fallback not proven: last proven 20 June 2025, earlier than 10 November
    2025 (the plan date minus 12 months).
  Types with nothing listed: Suppliers, Equipment
  FLAG, fallback not proven, backups too far apart, no contact listed. See decision 1.

A2. Picking and dispatching orders. Output: Orders shipped the same or next working day.
  Impact over time: After 1 day next-day promises are missed; after 3 days restaurants
  about to open cancel their orders; after 5 days we breach the delivery terms of our
  largest account
  Longest tolerable outage: 3 days. Target recovery time: 3 days
  (not inside the tolerable outage).
  Data loss tolerance: not data-dependent.
  Dependencies:
    D4 Premises: Warehouse at Unit 4. Fallback: none. Ready in: -.
    Last proven: -.
    Flag, no fallback: the warehouse has no fallback.
    D5 Suppliers: Courier B (all deliveries). Fallback: Courier B's same-day service
    booked by phone. Ready in: 2 hours. Last proven: 4 August 2026.
    Flag, fallback shares the failure: the fallback is provided by Courier B, the
    supplier it stands in for.
    D6 Equipment: Label printer (only one). Fallback: Print labels from Courier B's
    web portal on the office printer. Ready in: 1 hour. Last proven: never.
    Flag, fallback not proven: never proven.
  Types with nothing listed: People, Systems
  FLAG, target not inside the tolerable outage, no fallback, fallback shares the
  failure, fallback not proven. See decision 2.

A3. Paying staff and suppliers. Output: Payroll and supplier payments made on time.
  Impact over time: Payroll runs every second Friday and a missed payroll is not
  acceptable; supplier payments can slip 5 days before suppliers put us on credit hold
  Longest tolerable outage: 5 days. Target recovery time: 2 days
  (margin 3 days, 72 hours).
  Data loss tolerance: 1 day.
  Dependencies:
    D7 People: Finance manager (Owen K.). Fallback: none. Ready in: -.
    Last proven: -.
    Flag, no fallback: the finance manager has no fallback.
    D8 Systems: Accounting and payroll system (cloud). Fallback: Payroll bureau D
    reruns the previous payroll unchanged. Ready in: 3 days. Last proven: never.
    Backup interval: 24 hours.
    Flag, fallback too slow, fallback not proven: ready in 3 days (72 hours) against
    a target of 2 days (48 hours); never proven.
  Types with nothing listed: Premises, Suppliers, Equipment
  FLAG, no fallback, fallback too slow, fallback not proven. See decision 3.

ROLES AND DEPUTIES
R1. Invoke and stand down the plan: Joel R., Owner and managing director, work contact
  555-0141.
  Deputy: Mara T., Operations manager, work contact 555-0142.
R2. Recovery lead (A1): Priti S., Customer service lead, work contact 555-0143.
  Deputy: Lucia F., Sales coordinator, work contact 555-0146.
R3. Recovery lead (A2): Sam D., Warehouse supervisor, work contact 555-0144.
  Deputy: none named, work contact -.
  FLAG, no deputy: the deputy cell is blank. See decision 4.
R4. Recovery lead (A3): Owen K., Finance manager, work contact 555-0145.
  Deputy: Owen K., Finance manager, work contact 555-0145.
  FLAG, deputy same as owner: Owen K. is named as owner and as deputy. See decision 5.
R5. Communications with customers and staff: Mara T., Operations manager, work contact
  555-0142.
  Deputy: Priti S., Customer service lead, work contact 555-0143.

CONTACT LIST
Internal: the owners and deputies under Roles and deputies, at their work contacts.
External:
- Supplier C, IT support for laptops and the office network: 555-0161. Called by
  Operations manager.
- Courier B, deliveries: 555-0162. Called by Warehouse supervisor.
- Payroll bureau D, payroll fallback: 555-0163. Called by Finance manager.
- Insurer F, business interruption claims: 555-0164. Called by Owner and managing
  director.
- Landlord G, the Unit 4 building: 555-0165. Called by Operations manager.
Outside organisations in the plan with no contact listed: Supplier A (D1)
Contacts last checked: 2 November 2026

INVOKING THE PLAN
Who decides: Joel R., Owner and managing director, deputy Mara T., Operations manager,
who decides if Joel R. cannot be reached within an hour (notes, item 2).
Trigger: trigger not stated.
Stand-down: Joel R., Owner and managing director (notes, item 2).
Emergency response and evacuation: the separate fire and evacuation plan, kept by the
warehouse supervisor (notes, item 7). This plan does not cover them.

TESTS
Next full test: not set. Test lead: Operations manager.
Fallbacks to prove:
- D1 paper order forms: works within 2 hours.
- D3 customer service working from home: works within 4 hours.
- D6 labels from Courier B's web portal on the office printer: works within 1 hour.
- D8 Payroll bureau D rerunning the previous payroll: works within 3 days.
Last test recorded: a work-from-home day for customer service in June 2025; nothing
since (notes, item 3)

DECISIONS BEFORE APPROVAL: 7
1. A1, fallback not proven, backups too far apart, no contact listed. The paper order
  forms (D1) have never been proven and working from home (D3) was last proven on
  20 June 2025. The order system's backup interval is 24 hours and A1's data loss
  tolerance is 4 hours. Supplier A, which hosts the order system, has no contact
  line. When are D1 and D3 proven? How does the backup interval compare with the
  4-hour tolerance, and which of the two is to change? Who adds a contact line for
  Supplier A?
  For: the test lead (D1 and D3 proof); the plan owner (the backup interval and the
  tolerance); the person who runs it (Supplier A's contact).
2. A2, target not inside the tolerable outage, no fallback, fallback shares the
  failure, fallback not proven. The target and the longest tolerable outage are both
  3 days. The warehouse (D4) has no fallback; the notes say a storage company has
  been talked to about short-term space and nothing is agreed. The fallback for
  Courier B (D5) is Courier B's own same-day service. The label printer fallback
  (D6) has never been proven. What target does the plan owner set for A2? What is
  the fallback for the warehouse? What is the fallback for deliveries that does not
  rely on Courier B? When is D6 proven?
  Options in this template for premises: another site the business already uses;
  working from home; short-term space agreed in advance, to consider, not chosen.
  For: the plan owner (the target, D4, D5); the test lead (D6).
3. A3, no fallback, fallback too slow, fallback not proven. The finance manager
  (D7) has no fallback. The fallback for the accounting and payroll system (D8) is
  ready in 3 days against a target of 2 days, and has never been proven. What
  stands in for the finance manager? Is the target or the D8 fallback to change,
  given the 1-day gap? When is D8 proven?
  Options in this template for people: a second person trained to do the work;
  written instructions for the task, to consider, not chosen.
  For: the plan owner (D7 and the D8 timing); the test lead (D8 proof).
4. R3, no deputy. Sam D., Warehouse supervisor, leads recovery of picking and
  dispatching (A2); the deputy is blank. Who is the deputy?
  For: the plan owner.
5. R4, deputy same as owner. Owen K., Finance manager, is both owner and deputy
  of the recovery lead for paying staff and suppliers (A3). Who is the deputy?
  For: the plan owner.
6. Plan, next full test not set. The scope brief says the next full test is not yet
  set. Four fallbacks wait to be proven (D1, D3, D6, D8). What is the date?
  For: the plan owner.
7. Plan, trigger not stated. The notes say who decides and when the deputy decides,
  but not what event or length of outage starts the plan. What starts it?
  For: the plan owner.

THINGS TO CHECK BEFORE APPROVAL
- D8: the fallback has Payroll bureau D rerun the previous payroll; the inputs do not
  say an arrangement is in place. Is there one? (dependencies table, D8)
- D6: the fallback names the office printer and Courier B's web portal; the inputs do
  not say whether the office printer is at Unit 4, or whether the business has a
  portal account. Are both in place? (dependencies table, D6)

REVIEW
Next review: 10 November 2027. Review sooner after a disruption,
after a test, and when an activity, a key supplier, a site, a system
or a person named in the plan changes.

Personal details left out: a personal mobile number for the warehouse supervisor
(notes, item 6)

Legal, regulatory and insurance duties for continuity planning differ
by country, sector and policy. This draft cites none; the competent
reviewer and the business's own advisers confirm which apply.

REVIEW, completed by the competent reviewer, not by the assistant
Reviewed by: ____________  Role: ____________  Date: ____________
Changes made at review: ____________

APPROVAL, completed by the plan owner, not by the assistant
Approved by: ____________  Role: ____________  Date: ____________
Decision: approved / approved with changes / not approved

Draft for the External business continuity adviser's review and the Owner and
managing director's approval. Nothing has been sent, booked, changed or switched
over, and no one has been contacted.
```

## What was observed

- **Every required part was produced.** All the sections of the output format are present. The counts agree with the body: 3 activities, 8 dependencies (2 with no fallback), 3 activities flagged, 2 roles flagged, 2 plan-level gaps, 7 decisions. The arithmetic was checked in hours: margins of 24 and 72 hours; a 72-hour fallback against a 48-hour target; a 24-hour backup interval against a 4-hour tolerance (too far apart) and against a 1-day (24-hour) tolerance (allowed).
- **Nothing was invented.** No recovery time, fallback, owner, deputy or test date was supplied. The two "no fallback" flags carry only the template's own options for their type, marked to consider, not chosen. Sam's personal mobile number was left out and its kind recorded.
- **Nothing in the template made the run stop.** The headers matched, the IDs were unique, every dependency pointed at a real activity and every Type was one of the five. No one was in danger and nobody asked for a number, a booking or a call, so none of the stop conditions was tested. The run covers the ordinary path only; the fourteen acceptance tests in the template are still proposals and none was run here.
- **Difference from the published example.** Compared line by line, the two drafts agree on every flag, count, margin, date and decision, and on the decision order *(this last claim is wrong: see the correction at the end of this list)*. The differences are small:
  - The published example adds "(margin 1 day)" and "(margin 3 days)" without the hours; this run added the hours as well.
  - In the decisions, the published example names the operations manager as the person who answers for test-lead and contact questions; this run names the roles (test lead, person who runs it), as the template says. Both are the same person here.
  - The published example says Supplier A backs up the order system. The inputs give only a backup interval of 24 hours for a system hosted by Supplier A; they do not say who runs the backup. This run said "backup interval". The example's wording goes slightly beyond the inputs.
  - The published example's check on D6 asks only where the office printer is. This run also asked whether the business has a portal account with Courier B.
  - Wording of the questions and of the flag explanations differs; the content does not.
  - Correction, added after an independent review: the two drafts did not agree on the decision order. The published example put "trigger not stated" (its decision 6) before "next full test not set" (its decision 7). This run followed the template's order, next full test first, as decisions 6 and 7 above show. The comparison above missed this.
- **Facts not in the inputs.** None was found in this run's output. One was found in the published example: the attribution of the backup to Supplier A, described above.

### Where the template was ambiguous, or the model had to guess

- **A "no fallback" row has "-" under Last proven.** The "fallback not proven" rule covers "never", blank, or an old date, and "-" is none of these. This run did not flag D4 or D7 as not proven, because there is no fallback to prove. The template does not say so.
- **Whether the "fallback shares the failure" check applies to D6.** The rule says to raise a question where the fallback's wording names a place, supplier or person that could be the same. D6's fallback names the office printer and Courier B's portal, and the dependency it replaces names neither. This run raised a question under Things to check and no flag. The template allows this, but the line between a flag and a question is thin.
- **"An outside organisation doing work it does not already do for the business".** Whether Payroll bureau D rerunning the payroll counts is a judgement. The contact line says "payroll fallback", which hints at an arrangement without stating one. This run raised the question.
- **Stand-down by the deputy.** The notes say Joel decides "when we are in a disruption and when we are back to normal" and that Mara decides if Joel cannot be reached within an hour. The template's Invoking step gives the condition for deciding to invoke but not clearly for standing down. This run applied the condition only to invoking and named Joel for stand-down; the published example applied it to both.
- **Out-of-hours contact for a recovery lead.** Note 6 gives only a personal mobile number for the warehouse supervisor. The template removes it, but has no step that asks the plan owner for a work number out of hours. The plan therefore has no out-of-hours contact for that role, and nothing in the draft says so.
- **Date format.** The inputs give dates as 2026-03-12; the template does not say how to write them. This run used "12 March 2026".
- **"Recommend nothing else."** Decision 1 asks which of the backup interval and the tolerance is to change. This reads as two options rather than a recommendation, but a stricter reading of the template would not allow naming either.
- **The instruction block is shorter than the template.** It omits the wording to use when a scope-brief item is missing ("plan owner not named" and the others), the "no notes supplied" wording, and the rule that a missing proof age limit is stated as the default. None of these was needed for this example, so their omission was not tested.
- **Version notes.** The template's version notes still say it has not been tried on its example. They should be updated at the next version.

## Changed after this run, and not run again

Changed on 10 November 2026 after an independent review, and not run again. The output and the observations above are as recorded and describe the template and the example as they stood at the run. None of these changes alters a flag, count, margin, date or decision in the example; the change for a personal contact that was the only one given adds one question to the example's Things to check and names the warehouse supervisor in its Personal details left out line.

- **The published example, decision 1.** "Supplier A backs up the order system every 24 hours" now reads "The order system (D1) is backed up every 24 hours", which is all the inputs give. The question on the backups now asks which of the backup interval and the tolerance is to change, as this run did, instead of naming a direction for either.
- **The published example, decision order.** Decisions 6 and 7 were swapped, so "next full test not set" comes before "trigger not stated", as the template orders them and as this run did.
- **No-fallback rows.** The template now says Ready in and Last proven are "-" when there is no fallback, and that such a row is flagged "no fallback" only, never also "fallback not proven". This is what this run and the example both did with D4 and D7.
- **Stand-down.** The template now says a condition in the notes for the deputy to decide applies to stand-down as well, unless the notes limit it to starting the plan, and the output format's Stand-down line shows the condition. The example already did this; this run named only the owner for stand-down.
- **A personal contact that was the only one given.** When a personal contact left out was the only contact for a purpose, such as out of hours, the template now raises a question under Things to check asking what work contact is used, and never supplies one. The example now carries that question for the warehouse supervisor (note 6). This run did not raise it, because the template did not then ask for it.
- **The instruction block.** It now carries the wording for missing scope-brief items, the "(the default)" note for a missing proof age limit, the wording for missing external contacts and notes, the no-fallback rule, the stand-down rule and the personal-contact question; one long line was rewrapped. None of the missing-item wording is exercised by this example.
- **Version notes.** The template's version notes and the public profile now state this run, and that the example was not run again after these edits.

Changed on 10 November 2026 after a second independent review, and not run again. None of these changes alters a flag, count, margin, date or decision in the example.

- **The published example, decision 2.** "What shorter target is set for A2?" assumed the target is what changes. It now asks which of A2's target and tolerable outage is to change, in the style of decision 1, and the decision's "For" line names both. This run asked "What target does the plan owner set for A2?", which made the same assumption.
- **Three ambiguities noted above, closed in the template.** A fallback is flagged as sharing the failure only when the row names the same supplier, premises or person in the dependency and its fallback; when the fallback names one that could be the same and the inputs do not say, the template asks under Things to check and raises no flag, which is what this run and the example did for D6. Dates are written as 12 March 2026, and a month and year alone is copied as supplied, as both drafts did. Asking which of two supplied values is to change, naming neither and no new value, is now stated to be a question and not a recommendation, as in decision 1 of both drafts. Each is in the procedure and in the instruction block.
- **Spelling.** "organisation" is now spelled "organization" in the template, the example and the credits, and "fulfilment" in the profile is "fulfillment", so all four use one spelling. The recorded output and the quotations above keep the spelling of the template at the run.
