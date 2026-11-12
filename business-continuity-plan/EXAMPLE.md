# Business continuity plan: an invented example

*Illustrative example with invented data.* The business, the people, the suppliers, the phone numbers, the dates and the times below are all invented, and the phone numbers use the 555-01xx range kept for fiction. The business is an invented 32-person kitchen-equipment wholesaler with one warehouse and office, at Unit 4. Its operations manager prepared the plan. First come the inputs she supplied, in full, then the draft the workflow template returned for the competent reviewer and the owner.

## The inputs

### 1. Scope brief

```
Business: Kitchen-equipment wholesaler, 32 people
Sites covered: Warehouse and office at Unit 4 (our only site)
Run by: Operations manager
Plan owner, who approves: Owner and managing director
Competent reviewer: External business continuity adviser
Plan date: Tuesday 10 November 2026
Review interval: 12 months
Next full test: not yet set
Test lead: Operations manager
```

### 2. Activities table

```
ID,Activity,Output,Impact over time,Longest tolerable outage,Target recovery time,Data loss tolerance
A1,Taking and confirming customer orders,Orders confirmed to customers,"After 4 hours customers start phoning to chase; after 1 day trade customers order from competitors; after 2 days we lose the weekly orders from our two largest accounts",2 days,1 day,4 hours
A2,Picking and dispatching orders,Orders shipped the same or next working day,"After 1 day next-day promises are missed; after 3 days restaurants about to open cancel their orders; after 5 days we breach the delivery terms of our largest account",3 days,3 days,not data-dependent
A3,Paying staff and suppliers,Payroll and supplier payments made on time,"Payroll runs every second Friday and a missed payroll is not acceptable; supplier payments can slip 5 days before suppliers put us on credit hold",5 days,2 days,1 day
```

### 3. Dependencies table

```
ID,Activity,Type,Dependency,Fallback,Ready in,Last proven,Backup interval
D1,A1,Systems,Online order system hosted by Supplier A,Take orders by phone and email on paper order forms and key them in when the system returns,2 hours,never,24 hours
D2,A1,People,Customer service team (4),Sales staff (3) trained to take orders,4 hours,2026-03-12,-
D3,A1,Premises,Office at Unit 4,Customer service team works from home on company laptops,4 hours,2025-06-20,-
D4,A2,Premises,Warehouse at Unit 4,none,-,-,-
D5,A2,Suppliers,Courier B (all deliveries),Courier B's same-day service booked by phone,2 hours,2026-08-04,-
D6,A2,Equipment,Label printer (only one),Print labels from Courier B's web portal on the office printer,1 hour,never,-
D7,A3,People,Finance manager (Owen K.),none,-,-,-
D8,A3,Systems,Accounting and payroll system (cloud),Payroll bureau D reruns the previous payroll unchanged,3 days,never,24 hours
```

### 4. Roles roster

```
Plan role,Owner,Deputy,Owner work contact,Deputy work contact
Invoke and stand down the plan,"Joel R., Owner and managing director","Mara T., Operations manager",555-0141,555-0142
Recovery lead (A1),"Priti S., Customer service lead","Lucia F., Sales coordinator",555-0143,555-0146
Recovery lead (A2),"Sam D., Warehouse supervisor",,555-0144,
Recovery lead (A3),"Owen K., Finance manager","Owen K., Finance manager",555-0145,555-0145
Communications with customers and staff,"Mara T., Operations manager","Priti S., Customer service lead",555-0142,555-0143
```

### 5. External contacts

```
Contact,What for,Phone,Who calls them
Supplier C,IT support for laptops and the office network,555-0161,Operations manager
Courier B,Deliveries,555-0162,Warehouse supervisor
Payroll bureau D,Payroll fallback,555-0163,Finance manager
Insurer F,Business interruption claims,555-0164,Owner and managing director
Landlord G,The Unit 4 building,555-0165,Operations manager
```

### 6. Notes (typed by the operations manager)

```
Notes, Monday 9 November 2026.

1. What worries us most: a fire or flood at Unit 4, the order system
   going down, Courier B letting us down in peak season, and Owen being
   off when payroll is due.
2. Joel decides when we are in a disruption and when we are back to
   normal. If Joel can't be reached within an hour, Mara decides.
3. Last test: a work-from-home day for customer service in June 2025.
   Nothing since.
4. Contacts last checked: 2 November 2026.
5. If we lose Unit 4 the warehouse has nowhere to go. Joel has talked to
   a storage company about short-term space but nothing is agreed.
6. For Sam out of hours, use his personal mobile: 555-0198.
7. Our fire and evacuation plan is separate and kept by the warehouse
   supervisor.
```

No proof age limit was given, so the default of 12 months applies.

## The output

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
  (margin 1 day).
  Data loss tolerance: 4 hours.
  Dependencies:
    D1 Systems: Online order system hosted by Supplier A. Fallback: Take orders by
    phone and email on paper order forms and key them in when the system returns.
    Ready in: 2 hours. Last proven: never. Backup interval: 24 hours.
    Flag, fallback not proven, backups too far apart, no contact listed: never
    proven; backed up every 24 hours against a data loss tolerance of 4 hours; no
    external contact line for Supplier A.
    D2 People: Customer service team (4). Fallback: Sales staff (3) trained to take
    orders. Ready in: 4 hours. Last proven: 12 March 2026.
    D3 Premises: Office at Unit 4. Fallback: Customer service team works from home
    on company laptops. Ready in: 4 hours. Last proven: 20 June 2025.
    Flag, fallback not proven: last proven 20 June 2025, more than 12 months before
    the plan date.
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
  (margin 3 days).
  Data loss tolerance: 1 day.
  Dependencies:
    D7 People: Finance manager (Owen K.). Fallback: none. Ready in: -.
    Last proven: -.
    Flag, no fallback: the finance manager has no fallback.
    D8 Systems: Accounting and payroll system (cloud). Fallback: Payroll bureau D
    reruns the previous payroll unchanged. Ready in: 3 days. Last proven: never.
    Backup interval: 24 hours.
    Flag, fallback too slow, fallback not proven: ready in 3 days against a target of
    2 days; never proven.
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
  FLAG, no deputy: no one is named to lead the recovery of picking and dispatching if
  Sam D. is unavailable. See decision 4.
R4. Recovery lead (A3): Owen K., Finance manager, work contact 555-0145.
  Deputy: Owen K., Finance manager, work contact 555-0145.
  FLAG, deputy same as owner: Owen K. is named as both owner and deputy. See
  decision 5.
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
Outside organizations in the plan with no contact listed: Supplier A (D1)
Contacts last checked: 2 November 2026

INVOKING THE PLAN
Who decides: Joel R., Owner and managing director, deputy Mara T., Operations manager,
who decides if Joel R. cannot be reached within an hour (note 2).
Trigger: trigger not stated.
Stand-down: Joel R., or Mara T. if Joel R. cannot be reached within an hour (note 2).
Emergency response and evacuation: in the separate fire and evacuation plan kept by
the warehouse supervisor (note 7). This plan does not cover them.

TESTS
Next full test: not set. Test lead: Operations manager.
Fallbacks to prove:
- D1 paper order forms: works within 2 hours.
- D3 customer service working from home: works within 4 hours.
- D6 labels from Courier B's web portal on the office printer: works within 1 hour.
- D8 Payroll bureau D rerunning the previous payroll: works within 3 days.
Last test recorded: a work-from-home day for customer service in June 2025; nothing
since (note 3)

DECISIONS BEFORE APPROVAL: 7
1. A1, fallback not proven, backups too far apart, no contact listed. The paper
  order forms (D1) have never been proven, and working from home (D3) was last
  proven on 20 June 2025, more than 12 months before the plan date. The order
  system (D1) is backed up every 24 hours; A1 can lose no more than 4 hours of
  data. No external contact is listed for Supplier A, which hosts the order system.
  Are D1 and D3 proven at the next full test, or before it? The backup interval
  and A1's data loss tolerance do not fit: which of the two is to change? Who adds
  Supplier A's contact to the list?
  For: the operations manager, as test lead (D1 and D3) and as the person who runs
  the plan (Supplier A's contact); the owner and managing director (the backups).
2. A2, target not inside the tolerable outage, no fallback, fallback shares the
  failure, fallback not proven. The target recovery time and the longest tolerable
  outage are both 3 days. The warehouse (D4) has no fallback; note 5 says a storage
  company has been approached about short-term space but nothing is agreed. The
  fallback for Courier B (D5) is Courier B's own same-day service. The label
  printer's fallback (D6) has never been proven. Which of A2's target and
  tolerable outage is to change? What is the fallback for the warehouse? What
  fallback for deliveries does not depend on Courier B? Is D6 proven at the next
  full test?
  Options in this template for premises: another site the business already uses;
  working from home; short-term space agreed in advance, to consider, not chosen.
  For: the owner and managing director (A2's target and tolerable outage, D4 and
  D5); the operations manager, as test lead (D6).
3. A3, no fallback, fallback too slow, fallback not proven. The finance manager,
  Owen K. (D7), has no fallback. Payroll bureau D's rerun (D8) takes 3 days to be
  ready against a target of 2 days, and has never been proven. Who or what stands
  in for the finance manager? How is A3 running again within 2 days when the D8
  fallback takes 3, or is the target changed? Is D8 proven at the next full test?
  Options in this template for people: a second person trained to do the work;
  written instructions for the task, to consider, not chosen.
  For: the owner and managing director (D7 and the D8 timing); the operations
  manager, as test lead (D8 proof).
4. R3, no deputy. Sam D., Warehouse supervisor, leads the recovery of picking and
  dispatching (A2), and no deputy is named. Who is the deputy?
  For: the owner and managing director.
5. R4, deputy same as owner. Owen K., Finance manager, is named as both owner and
  deputy of the recovery of payments (A3), and the finance manager is also a
  dependency of A3 with no fallback (D7). Who is the deputy?
  For: the owner and managing director.
6. Plan, next full test not set. The scope brief says the next full test is not yet
  set; note 3 says the last test was a work-from-home day in June 2025, with nothing
  since. Four fallbacks are waiting to be proven (D1, D3, D6, D8). On what date is
  the next full test?
  For: the owner and managing director.
7. Plan, trigger not stated. Note 2 says Joel R. decides when the business is in a
  disruption and when it is back to normal, and Mara T. decides if Joel R. cannot be
  reached within an hour; it does not say what event or length of outage starts the
  plan. What starts the plan?
  For: the owner and managing director.

THINGS TO CHECK BEFORE APPROVAL
- D8: the fallback has Payroll bureau D rerun the previous payroll, and the inputs do
  not say an arrangement with the bureau is in place. Is one in place? (dependencies
  table, D8)
- D6: the fallback prints labels on the office printer, and the inputs do not say
  where that printer is. Is it at Unit 4, and so lost with the site? (dependencies
  table, D6)
- R3: note 6 gives only a personal mobile number for reaching the warehouse
  supervisor out of hours, and it is left out of this plan. What work contact is
  used for the warehouse supervisor out of hours? (notes, note 6)

REVIEW
Next review: 10 November 2027. Review sooner after a disruption,
after a test, and when an activity, a key supplier, a site, a system
or a person named in the plan changes.

Personal details left out: a personal mobile number for the warehouse supervisor (note 6)

Legal, regulatory and insurance duties for continuity planning differ
by country, sector and policy. This draft cites none; the competent
reviewer and the business's own advisers confirm which apply.

REVIEW, completed by the competent reviewer, not by the assistant
Reviewed by: ____________  Role: ____________  Date: ____________
Changes made at review: ____________

APPROVAL, completed by the plan owner, not by the assistant
Approved by: ____________  Role: ____________  Date: ____________
Decision: approved / approved with changes / not approved

Draft for the external business continuity adviser's review and the owner and
managing director's approval. Nothing has been sent, booked, changed or switched
over, and no one has been contacted.
```
