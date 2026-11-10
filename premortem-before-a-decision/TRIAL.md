# Premortem before a decision: tried on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Sonnet 5.5 (model ID claude-sonnet-5-5), run by a model that did not write the template
- **Date:** 2026-11-10

The inputs are the invented example in [example.md](example.md): the invented distributor's brief and written reasons for the first pass, and the agreed groups, ratings and facilitator's notes for the second. No client data was used. The run followed the instruction block in the member template and its output format. The published example's output was read only after this output was complete.

## Inputs used

- The brief (input 1 in the example).
- The written reasons, 18 rows (input 2).
- The agreed groups and ratings, 8 rows (input 3).
- The facilitator's notes on checks, dated Wednesday 4 November 2026 (input 4).
- Settings: defaults.

## What came out

Both passes, in full.

```
FIRST PASS

PREMORTEM GROUPING SHEET: Seven-year lease on a larger warehouse, and the move
Session: Tuesday 3 November 2026. Reasons: 18 from 6 people. Proposed groups: 8.

G1 Orders not shipped after the move weekend. Named by 4 of 6.
  R01 The move weekend ran over and we could not ship on the Monday or Tuesday; two of our biggest customers ordered elsewhere.
  R06 We moved in the same week as a big seasonal order and could not cope.
  R12 Orders backed up for two weeks and we lost a regular account.
  R15 Sales lost during the move week were bigger than we assumed.

G2 Racking, dock and yard not ready. Named by 3 of 6.
  R04 The racking was not installed by the move date because the installer took longer than quoted.
  R08 The loading dock only takes one truck at a time and incoming deliveries queued.
  R17 The yard is too small to turn the big truck.

G3 Costs above plan. Named by 2 of 6.
  R02 The rent on the new building plus the move cost more than planned and cash got tight by April.
  R13 The fit-out cost more than budgeted (power for the forklift chargers, the office).
  R14 We paid rent on both buildings for longer than planned because the old lease could not be ended early.

G4 Longer delivery routes from the new site. Named by 2 of 6.
  R03 Customers near the old site got later deliveries and complained.
  R16 Routes from the new site are longer and drivers ran out of hours.

G5 Stock records wrong after the move. Named by 2 of 6.
  R05 Stock counts were wrong after the move, so we sold things we did not have.
  R09 Pallets were labelled badly during packing so nobody could find anything for a week.

G6 Pickers leave over the longer commute. Named by 2 of 6.
  R07 Two of the four pickers left because the new site is 12 miles further out and there is no bus.
  R18 Pickers quit because of the commute.

G7 Customers not told in time. Named by 1 of 6.
  R10 We did not tell customers early enough and they were surprised by delays.

G8 Phones and internet not working on the first day. Named by 1 of 6.
  R11 Phones and the internet line were not working on the Monday at the new site.

Withheld, for the facilitator to reword: none.
For the room: move, merge, split or rename any group, then rate each one:
likelihood 1-3, harm 1-3, warning early / late / none.
Draft for the facilitator. Nothing has been rated, decided or sent.

SECOND PASS

PREMORTEM RECORD: Seven-year lease on a larger warehouse, and the move

Decision: Whether to sign a seven-year lease on a larger warehouse 12 miles from the current one, and move into it over one weekend.
Decides: Owner. Go decision due: Friday 13 November 2026.
Hard to reverse because: seven-year lease; a deposit of three months' rent; the current building will be let to someone else once we give notice.
Failure imagined at: 31 May 2027. The plan went ahead as agreed and did not work.
Took part: 6 people: Owner, Operations manager, Warehouse lead, Customer service lead, Finance lead, Senior driver. Facilitator: Office manager.
Session: Tuesday 3 November 2026. Reasons written privately before discussion: yes.
Prepared: Wednesday 4 November 2026, from the brief, the written reasons, the agreed groups and ratings and the notes on checks; default settings. Reasons are not attributed to anyone.

Reasons written: 18 from 6 people, in 8 groups. Top risks: 4.

RANKED FAILURE REASONS
1. G1 Orders not shipped after the move weekend. Named by 4 of 6. Likelihood 2, harm 3, score 6, warning late. TOP RISK. Reasons: R01, R06, R12, R15.
2. G2 Racking, dock and yard not ready. Named by 3 of 6. Likelihood 2, harm 3, score 6, warning early. TOP RISK. Reasons: R04, R08, R17.
3. G6 Pickers leave over the longer commute. Named by 2 of 6. Likelihood 3, harm 2, score 6, warning early. TOP RISK. Reasons: R07, R18.
4. G5 Stock records wrong after the move. Named by 2 of 6. Likelihood 2, harm 2, score 4, warning late. Reasons: R05, R09.
5. G3 Costs above plan. Named by 2 of 6. Likelihood 2, harm 2, score 4, warning early. Reasons: R02, R13, R14.
6. G8 Phones and internet not working on the first day. Named by 1 of 6. Likelihood 1, harm 3, score 3, warning none. TOP RISK. Named by one person. Reasons: R11.
7. G4 Longer delivery routes from the new site. Named by 2 of 6. Likelihood 2, harm 1, score 2, warning early. Reasons: R03, R16.
8. G7 Customers not told in time. Named by 1 of 6. Likelihood 1, harm 2, score 2, warning early. Reasons: R10.

TOP RISKS: CHECKS, WARNING SIGNS AND OWNERS
G1 Orders not shipped after the move weekend
  Check before go: get the moving company's written hour-by-hour plan for the move weekend. Owner: Operations manager. Due: Tuesday 10 November 2026. Status: not done.
  Warning sign: share of pallets racked at the new site during the move weekend. Act when: under half by 6 pm on Saturday 13 February; the owner then decides whether Monday's orders ship from the old building. Watched by: Operations manager.

G2 Racking, dock and yard not ready
  Check before go: racking installer to confirm in writing an installation start at least two weeks before the move. Owner: Warehouse lead. Due: Friday 6 November 2026. Status: done.
  Check before go: walk the new yard with the largest truck to confirm it can turn. Owner: Senior driver. Due: Monday 16 November 2026. Status: not done.
  Warning sign: installer has not started work at the new site. Act when: no start by Monday 25 January 2027; the owner then reviews the move date. Watched by: Warehouse lead.

G6 Pickers leave over the longer commute
  Check before go: map travel options to the new site for each shift (bus, car-share, parking) and talk them through with the pickers. Owner: Warehouse lead. Due: Wednesday 11 November 2026. Status: not done.
  Warning sign: pickers giving notice or asking to change shifts once the move is announced. Act when: not agreed. Watched by: Warehouse lead.

G8 Phones and internet not working on the first day
  Check before go: order the new internet line and the move of the phone numbers at least 60 days before the move. Owner: not assigned. Due: not stated. Status: not stated.
  Warning sign: none agreed. Act when: not agreed. Watched by: not assigned.

CHANGES TO THE PLAN AGREED IN THE ROOM
1. Move weekend changed from 6-7 February to 13-14 February 2027, after the spring order for Customer A ships on 10 February.
2. Keep the old building's dock in use until Wednesday 17 February 2027 as a fallback for shipping.

BEFORE THE GO DECISION
Checks before go: 5. Done: G2, racking installer written confirmation of installation start. Not done: G1, moving company's hour-by-hour plan, Operations manager, Tuesday 10 November 2026; G2, walk the yard with the largest truck, Senior driver, Monday 16 November 2026; G6, map travel options for each shift, Warehouse lead, Wednesday 11 November 2026. Due after the go decision: G2, walk the yard with the largest truck (Monday 16 November 2026). No owner or no due date: G8, order the new internet line and phone number move. Status not stated: G8, order the new internet line and phone number move.

OPEN QUESTIONS FOR THE OWNER
1. G2 Racking, dock and yard not ready: the check to walk the new yard with the largest truck is due Monday 16 November 2026, after the go decision on Friday 13 November 2026. Is the go decision to wait for it, or to be taken without it?
2. G6 Pickers leave over the longer commute: the warning sign is pickers giving notice or asking to change shifts, but no level at which someone acts was agreed. What level, and who then decides what?
3. G8 Phones and internet not working on the first day: the room agreed the internet line and phone numbers should be ordered at least 60 days before the move, but nobody took it, and no due date, status, warning sign, level to act or watcher was agreed. The Finance lead thinks the line order takes 30 to 60 days. Who owns this check, by when, and what warning sign, level and watcher?

NEXT PREMORTEM
Date: Friday 15 January 2027. Sooner if: the move date changes or the racking installer's start date moves.

THE REASONS AS WRITTEN
R01 The move weekend ran over and we could not ship on the Monday or Tuesday; two of our biggest customers ordered elsewhere.
R02 The rent on the new building plus the move cost more than planned and cash got tight by April.
R03 Customers near the old site got later deliveries and complained.
R04 The racking was not installed by the move date because the installer took longer than quoted.
R05 Stock counts were wrong after the move, so we sold things we did not have.
R06 We moved in the same week as a big seasonal order and could not cope.
R07 Two of the four pickers left because the new site is 12 miles further out and there is no bus.
R08 The loading dock only takes one truck at a time and incoming deliveries queued.
R09 Pallets were labelled badly during packing so nobody could find anything for a week.
R10 We did not tell customers early enough and they were surprised by delays.
R11 Phones and the internet line were not working on the Monday at the new site.
R12 Orders backed up for two weeks and we lost a regular account.
R13 The fit-out cost more than budgeted (power for the forklift chargers, the office).
R14 We paid rent on both buildings for longer than planned because the old lease could not be ended early.
R15 Sales lost during the move week were bigger than we assumed.
R16 Routes from the new site are longer and drivers ran out of hours.
R17 The yard is too small to turn the big truck.
R18 Pickers quit because of the commute.

Owner's decision: [ ] Proceed  [ ] Proceed with the changes above
[ ] Hold  [ ] Stop   Date: [ ]
Prepared for the Owner's decision. Nothing has been decided, sent, booked, signed or changed.
```

## What was observed

- **Every required part was produced.** Grouping sheet, ranked reasons, top risks with checks, plan changes, the before-go count, open questions, next premortem, the reasons as written, a blank decision line and the closing sentence. Nothing in the instructions made it stop: there were no names in the reasons, no missing or out-of-scale ratings, every R number sat in exactly one group, and the headers matched.
- **Counts, scores and ranking were rechecked by hand** and match the rule: three groups at score 6 ordered late, then three people, then two; G8 marked a top risk by the harm 3 and no warning rule although its score is 3, and flagged as named by one person; G5 ahead of G3 on the warning tie-break.
- **Difference from the published example, in the output.** The two outputs agree on every group, reason, count, score, rank, check, owner, date, status, warning sign, plan change, count of checks and next date. They differ only in wording: the decision title ("Seven-year lease on a larger warehouse, and the move" against "New warehouse lease and move"); the Prepared line; "racking installer written confirmation of installation start" against "racking installer's written start date" and similar short labels in the before-go list; the open questions, which are worded differently (the example adds that the senior driver is on routes until 16 November, a fact from the notes that I left out, and asks how many notices or shift requests should be raised, where I asked for the level and who then decides what); "Sooner if" joins the two events with "or" in mine and a semicolon in the example; and the example puts no blank line between top risks. The example also ends with a sentence after the record, which is not part of the output format.
- **Facts not in the inputs.** None in my output. Everything traces to the brief, reasons or notes. The example's output also adds none; its extra fact (the senior driver on routes until 16 November) is in the notes.
- **The first pass was not blind.** I read all four inputs before producing anything, so the second-pass ratings file showed me which reasons the room put in which group, and the second-pass text said the room kept the eight groups as proposed. My first-pass grouping matched the example's exactly, but I cannot say how much of that is the template and how much is having seen the answer in the inputs. A fair test of the first pass would give the model only the brief and the reasons.

## Where the template was ambiguous or needed a guess

1. **Grouping reasons.** The instructions say to group reasons with "the same cause" but give no rule for a reason that fits two groups (for example, the seasonal-order reason, or late deliveries to customers near the old site, which could sit with customers not told in time). A different model could group differently and the template would still be followed.
2. **The G8 line in the notes.** The notes say everyone agreed to order the internet line 60 days before the move and nobody took it. The template does not say whether an agreement with no owner, due date or status counts as a "check". I counted it as one, so it is in the count of five. The due date is relative ("60 days before the move"); I did not turn it into a date because the template forbids supplying one, so it reads "not stated".
3. **An unfilled placeholder.** Input 5 (Settings) still says "failure imagined [your failure horizon]" in the text a user sees, and the instruction block says "[your top-risk score] (default 6)". The first reads as an unfinished sentence.
4. **Open questions that ask only for what is missing.** The rule is to ask only for what is missing. The question about a check due after the go decision is really a choice for the owner (decide before it, or without it). It stays within "recommend nothing" but is not strictly a missing fact.
5. **List punctuation.** The format shows "[R numbers]" and "[events]" without saying how to separate them; I used commas for reasons and "or" for events.
6. **Wording of the Prepared line and the before-go entries** is open ("[the inputs used]"), so outputs will not match word for word.
7. **Dates.** The template does not say how to treat a date in the notes that falls before the session or after today; here all dates were consistent, so the question did not arise.

## Not shown by this trial

- Whether the stop conditions work: none was triggered, since the example inputs are clean. The eleven proposed acceptance tests were not run.
- Behaviour in ChatGPT, Copilot or Gemini, and in a real client setting.
- Whether a person can run the session part (the hour in the room) from the template. Only the assistant's two passes were tried.

## Changed after this run, and the second pass not run again

Changed on 10 November 2026 after an independent review of the published template. The output and the observations above are as recorded and describe the template and the example as they stood at the run. No change alters a group, a count, a score, a rank, a check, an owner, a date or a status in either output. The second pass has not been run again since these changes.

- **Settings wording** (item 3 above). Input 5 now reads "the failure is imagined three to twelve months after the go date ([your failure horizon])".
- **An agreed action with no owner, and a relative date** (item 2 above). The procedure and the pasted instructions now say that an action the room agreed counts as a check even with no owner, due date or status, and that a due date not given as a calendar date is printed "not stated". Both this run and the example already did this for the G8 line.
- **A check due after the go decision** (item 4 above). The open-question rule now allows the question to ask whether the owner decides before such a check is done or without it, as both outputs did.
- **Separators** (item 5 above). The format now says R numbers are separated by commas, as both outputs did, and "Sooner if" events by semicolons, as the example did; this run used "or".
- **The Prepared line** (item 6 above). The format now gives the inputs in fixed words: "from the brief, the written reasons, the agreed groups and ratings, and the notes on checks". The example's Prepared line now uses them; neither output above matched them exactly.
- **Top risks known in the room.** The session now has the facilitator multiply likelihood by harm and read out the top risks after rating, so the room knows which groups need checks. If the notes cover a group that is not a top risk, the record now names it on a "Notes also given for" line instead of leaving it out silently. The example's notes cover only top risks, so neither output would show that line.
- **Typing order.** The facilitator is now told to type the reasons in a mixed order, because the R numbers follow the typing order; a list typed person by person, as in the example, lets anyone who knows that order tell who wrote what, and in a small room a group named by one person can still point to its author. The example now says its reasons are typed sheet by sheet only so it is easy to follow. Its inputs are unchanged.
- **The example's G8 question** now also asks whether the action has been done, at what level someone should act and who watches, so it covers every gap the rule names. This run's question already asked for the level and the watcher.

Item 1 (grouping a reason that fits two groups) and item 7 (dates before the session or after today) are unchanged.

## A blind re-run of the first pass

- **Product:** Claude, run in Claude Code, with no tools
- **Model:** Sonnet 5.5 (model ID claude-sonnet-5-5). It did not write the template. The run was started by the model that made the changes above.
- **Date:** 2026-11-10, after the changes above, none of which touches the first pass's instructions or output format.

To answer the first-pass shortcoming recorded above, the first pass was run again with only the instruction block, the output format, the invented brief and the 18 written reasons. The run saw no ratings, no notes and no part of the example's output. This is the whole output:

```
FIRST PASS

PREMORTEM GROUPING SHEET: Seven-year lease on a larger warehouse and weekend move
Session: Tuesday 3 November 2026. Reasons: 18 from 6 people. Proposed groups: 9.

G1 The move week disrupted shipping and sales. Named by 4 of 6.
  R01 The move weekend ran over and we could not ship on the Monday or Tuesday; two of our biggest customers ordered elsewhere.
  R06 We moved in the same week as a big seasonal order and could not cope.
  R12 Orders backed up for two weeks and we lost a regular account.
  R15 Sales lost during the move week were bigger than we assumed.

G2 Costs ran over what was planned. Named by 2 of 6.
  R02 The rent on the new building plus the move cost more than planned and cash got tight by April.
  R13 The fit-out cost more than budgeted (power for the forklift chargers, the office).
  R14 We paid rent on both buildings for longer than planned because the old lease could not be ended early.

G3 Longer routes from the new site slowed deliveries. Named by 2 of 6.
  R03 Customers near the old site got later deliveries and complained.
  R16 Routes from the new site are longer and drivers ran out of hours.

G4 Stock was not tracked or labelled properly in the move. Named by 2 of 6.
  R05 Stock counts were wrong after the move, so we sold things we did not have.
  R09 Pallets were labelled badly during packing so nobody could find anything for a week.

G5 Pickers left because of the commute to the new site. Named by 2 of 6.
  R07 Two of the four pickers left because the new site is 12 miles further out and there is no bus.
  R18 Pickers quit because of the commute.

G6 The new site's dock and yard are too small for the traffic. Named by 2 of 6.
  R08 The loading dock only takes one truck at a time and incoming deliveries queued.
  R17 The yard is too small to turn the big truck.

G7 Racking was installed late. Named by 1 of 6.
  R04 The racking was not installed by the move date because the installer took longer than quoted.

G8 Customers were told too late. Named by 1 of 6.
  R10 We did not tell customers early enough and they were surprised by delays.

G9 Phones and internet were not working at the new site. Named by 1 of 6.
  R11 Phones and the internet line were not working on the Monday at the new site.

Withheld, for the facilitator to reword: none.
For the room: move, merge, split or rename any group, then rate each one: likelihood 1-3, harm 1-3, warning early / late / none.
Draft for the facilitator. Nothing has been rated, decided or sent.
```

What was observed:

- **Nine groups, not eight.** Run blind, the model kept late racking (R04) apart from the dock and yard being too small (R08, R17); the example and the run above put all three in one group. Both readings fit "the same cause". The other seven groups hold the same reasons as the example's. So the earlier run's exact match with the example owed something to having seen the ratings file, and the grouping sheet is a proposal that can differ from run to run. The room's step of moving, merging and splitting groups is what settles it.
- **Counts and order follow the rule.** Every reason appears once; each "named by" count matches the participants in the group; groups are ordered by how many people named them, then by first R number. No reason was reworded and nothing was rated.
- **Wording differs.** The group titles and the decision title are worded differently from the example's, and the "For the room" lines were joined into one line where the format shows two.
- **Still not shown.** No stop condition was exercised, and the second pass was not re-run.
