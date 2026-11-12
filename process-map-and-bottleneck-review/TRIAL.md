# Process map and bottleneck review: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

I tried this workflow template once, on its own invented example. The inputs are the invented example's; no client data was used. I did not write the template. I read the template, took only the inputs from `public/example.md` (the process request, the six-step table, the role hours and the four notes), followed the instruction block and the output format, and only then compared my output with the example's output and the reviewer checklist.

## Inputs used

The four inputs in [the example](example.md), under "The inputs": the process request for "Quote for a custom sign, from request to quote sent", the step table, the role hours and the notes from the people who do the work. Nothing was added to them.

## What came out

This is the full output, as produced.

```
PROCESS MAP AND BOTTLENECK REVIEW: Quote for a custom sign, from request to quote sent

For: Operations manager. Prepared 10 November 2026 from step table (6 steps), role hours, notes from four roles. Figures cover the four weeks to 30 October 2026 (weekly averages).
One item: starts when a customer request arrives by email or the website form; ends when the quote is sent to the customer.
The number that should rise: quotes sent per week, now 17 a week. Arriving: 20 a week. Time target: quote sent within 3 working days (24 working hours).

1. The map
Step 1. Log the request in the job system. Sales coordinator. Waits 1 h, then 0.3 h of work. Measured.
Step 2. Check drawings and sizes are complete; ask the customer for anything missing. Sales coordinator. Waits 2 h, then 0.5 h of work. Measured.
Step 3. Price materials and labour. Estimator. Waits 12 h, then 1.5 h of work. Hand-over from Sales coordinator. Sent back to step 2 in 2 of 10. Measured.
Step 4. Check it can be made: fixings, sizes and site access. Production manager. Waits 8 h, then 0.5 h of work. Hand-over from Estimator. Sent back to step 3 in 3 of 10. Estimated.
Step 5. Approve the price. General manager. Waits 18 h, then 0.2 h of work. Hand-over from Production manager. Estimated.
Step 6. Write up and send the quote. Sales coordinator. Waits 3 h, then 0.5 h of work. Hand-over from General manager. Measured.
Hand-overs: 4 (Sales coordinator to Estimator, Estimator to Production manager, Production manager to General manager, General manager to Sales coordinator). Send-backs: step 3 to step 2, 2 in 10, Estimator to Sales coordinator; step 4 to step 3, 3 in 10, Production manager to Estimator.
By role: Sales coordinator: steps 1, 2, 6. Estimator: step 3. Production manager: step 4. General manager: step 5.

2. Where the time goes
First pass: 47.5 h (5.9 working days): 3.5 h of work (7%), 44.0 h waiting (93%).
Send-backs add 9.8 h on average (step 3 to step 2: 0.2 x 16.0 h = 3.2 h; step 4 to step 3: 0.3 x 22.0 h = 6.6 h), 57.3 h (7.2 working days) in all.
Against the time target of 24 h: over by 23.5 h first pass and 33.3 h with send-backs.
Longest waits: before step 5 (18 h), before step 3 (12 h), before step 4 (8 h).

3. Load by role
Sales coordinator (steps 1, 2, 6): 28.0 h of work a week against 36.0 h given: 78%. Can finish about 25.7 a week.
Estimator (step 3): 45.0 h of work a week against 38.0 h given: 118%. Can finish about 16.9 a week.
Production manager (step 4): 13.0 h of work a week against 15.0 h given: 87%. Can finish about 23.1 a week.
General manager (step 5): 4.0 h of work a week against 6.0 h given: 67%. Can finish about 30.0 a week.
Send-backs counted: each one repeats the steps from where the item returns to where it was found, once. Expected work per item: step 2, 0.5 h x 1.20 = 0.60 h; step 3, 1.5 h x 1.50 = 2.25 h; step 4, 0.5 h x 1.30 = 0.65 h; all other steps as listed.

4. The constraint
Estimator, at step 3: 118%. More arrives than it can finish: 20 a week against about 16.9; the queue in front of step 3 grows by about 3.1 a week.
Check against what is finished: about 16.9 a week at this step against 17 now: the figures agree.
The step people complain about: step 4 is not the constraint: the Production manager is at 87%, the Estimator at 118%.
The longest wait, before step 5, is not at the constraint: the notes say the General manager approves on Tuesday and Friday afternoons.

5. Try first at the constraint
1. Catch missing sizes and drawings before pricing, so fewer requests come back from step 3 to step 2. Based on: the Sales coordinator's note that about 2 in 10 come back because the Estimator finds a size or drawing missing; step 2 already checks completeness. Returns up to about 6.0 h a week of Estimator time if none came back (20 x 0.2 x 1.5 h). Arithmetic on the supplied figures, not a forecast.
2. Stop repricing caused by fixings and sizes found at the make-it check, without removing that check. Based on: the Production manager's estimate that roughly 3 in 10 need a change to fixings or sizes, and the Estimator's note that the whole job is priced again. Returns up to about 9.0 h a week of Estimator time if none came back (20 x 0.3 x 1.5 h). Arithmetic on the supplied figures, not a forecast. The owner decides how, for example whether fixings and sizes could be settled before pricing; the check itself stays.
3. Take the workshop questions about jobs already won away from the Estimator. Based on: the Estimator's note that about 4 of 42 weekly hours go on them, which are not part of this process. Returns about 4.0 h a week of Estimator time (4 h given back to quotes; the 38 h supplied already leaves them out). Arithmetic on the supplied figures, not a forecast. Which role answers them is the owner's call.

6. Then, if that is not enough
If the Estimator is still the most loaded role after these are tried and measured, adding capacity at step 3 is the owner's decision; adding it at any other step would not raise quotes sent per week.

7. Leave alone for now
Step 1 (Sales coordinator, 78%): faster logging would not raise quotes sent; the Estimator limits it.
Step 2 (Sales coordinator, 78%): speeding it up would not raise the number. What it checks matters to option 1.
Step 4 (Production manager, 87%): the step people complain about, but at 87% it finishes about 23.1 a week, more than the Estimator's 16.9. What it checks matters to option 2.
Step 5 (General manager, 67%): the longest wait, 18 h, but shortening it would shorten the time to a quote, not raise the number finished.
Step 6 (Sales coordinator, 78%): speeding it up would not raise the number.

8. Where the bottleneck goes next
Production manager, at 87% today. Option 2 would cut its load: with no send-backs from step 4 its expected work per item falls from 0.65 h to 0.50 h, 10.0 h a week against 15.0 h, 67%.

9. Figures to firm up
Step 4, sent back 3 in 10, wait 8 h and work 0.5 h: estimated; the Production manager says the 3 in 10 is a guess. It drives option 2 and the second-highest load.
Step 5, wait 18 h: estimated. It is the longest wait and is raised as a decision for the owner.
Estimator hours, 38 a week: taken from the Estimator's note, not marked measured or estimated. The 118% rests on it.

10. Decisions for the owner
1. Which option to try first, who carries it and when to measure again.
2. The 18 h wait before approval, with approvals on Tuesday and Friday afternoons, drives the time to a quote (over the 24 h target) but not the number sent; whether to change the approval days.
3. Which role, if any, takes the Estimator's workshop questions (option 3).

11. Open questions
1. How many in ten quotes really need a change to fixings or sizes at step 4, for the Production manager.
2. Is the 18 h wait before step 5 measured from the job system, for the Operations manager.
3. Are the Estimator's 38 hours a week a measured or an estimated figure, for the Estimator.

Draft for the Operations manager. Nothing has been changed, assigned or sent. The owner decides what changes.
```

## What was observed

**Every required part was produced.** All eleven numbered sections and the draft line came out, in the order the format sets. Nothing in the instructions made me stop: the owner, the step table and its headings, the number that should rise and its current value were all present, every send-back pointed to an earlier step, and every share was between 0 and 10.

**The arithmetic matched the example.** My totals, percentages, loads and capacities are the same as the example's: 47.5 h first pass, 57.3 h with send-backs, the Estimator at 118% against the Production manager's 87%, about 16.9 a week against 17 now, and the three options at 6.0, 9.0 and 4.0 h a week. The same constraint came out, the same check against what is finished, and the same finding that the step people complain about is not the constraint.

**Differences from the published example:**

- Number formatting. I wrote hours given as 36.0 and multipliers as 1.20; the example writes 36 and 1.2. The template's format does not say which.
- Section 4. I did not add the sentence that the Production manager's send-backs cost the Estimator time. The example does.
- Option 1 and option 2 wording. The example states each as a plain change ("Stop requests with missing sizes or drawings reaching pricing"; "Settle fixings and sizes before pricing"). I phrased them more cautiously, said they return "up to" the stated hours, and for option 2 said the make-it check itself stays and the owner decides how. The example's option 2 proposes moving the settling of fixings and sizes before pricing, which is a design choice that is not in the inputs.
- Option 3. Same figure (4.0 h); I explained the arithmetic as hours given back to quotes since the 38 h already leaves them out, the example as 42 h minus 38 h.
- Section 7. The reasons differ in wording. The example's reasons for steps 1 and 6 ("requests would reach pricing sooner and wait there"; "fewer quotes reach it than it can handle") are inferences from the figures, not figures themselves. Mine give shorter reasons.
- Section 8. I gave a number for the effect of option 2 on the Production manager (0.65 h to 0.50 h per item, 13.0 to 10.0 h a week, 67%). The example says only that it would take repeat checks off.
- Section 9. I also listed the Estimator's 38 hours as unmarked (see below). The example does not.
- Sections 10 and 11. I added a decision about which role takes the Estimator's workshop questions, and three open questions (how many in ten need a change at step 4; whether the 18 h wait is measured; whether the 38 h is measured). The example has one open question I did not ask: how long the customer takes to reply when a request goes back to step 2, since the review counts only the typical 2.0 h wait there.

**Facts not in the inputs.** In my output I found none beyond the arithmetic. In the example's output, the sentence in section 7 that requests "would reach pricing sooner and wait there", and that "fewer quotes reach [step 6] than it can handle", are reasoning rather than supplied facts, and the proposal in option 2 to settle fixings and sizes before pricing is the example's own idea.

**Where the template was ambiguous, and what I did:**

1. The draft line. The instruction block says to end with "the draft line: nothing has been changed, assigned or sent". The output format's line also has "The owner decides what changes." I used the longer line from the format.
2. Hand-over at step 1. The template defines a hand-over as a role that differs from the step before; step 1 has no step before. I counted none at step 1, which matches the example.
3. Send-back waits. The rule repeats the waits as well as the work across the span, at the typical time. For the step 3 to step 2 loop that counts a 2 h wait while the customer is chased, which the notes suggest may take longer. The template mentions the rule under "What to customize" but does not warn the assistant to ask.
4. Overlapping send-backs. Step 3 is in two loops, and the rule adds the shares (1 + 0.2 + 0.3). It does not say what to do if a repriced item could be sent back again.
5. Hours returned by an option. The template says "hours a week of the constraint's time it would return" but does not say whether to treat that as the most the option could return (if the problem vanished) or an expected return. The example and I both computed the maximum; I labelled it "up to".
6. Option 3. The hours the assistant counts are the note's hours (4 of 42), while the role-hours table already shows 38. The template does not say which source wins when a note and the table both give hours.
7. Marking of figures. `basis` is per row, so it is unclear whether it covers the work time, the wait and the send-back share together. The role-hours table has no basis column at all, and "Figures to firm up" is defined as estimated figures, so an unmarked figure such as the Estimator's 38 hours has no defined place. I listed it and asked.
8. Rounding. The block gives rules for hours, days, loads and capacity but not for waits shown in the map, or for percentages of work and waiting in the first-pass line (the block and template say "whole percentages" for one and not the other).
9. Bracketed defaults. The tie margin, nearly-full line and agreement margin appear as "[your tie margin, default 5]" in the pasted block. I used the defaults without asking; the template does not say whether to ask when the brackets are unfilled.
10. "Its load" in the leave-alone section is defined per step, but load is computed per role. For a role with several steps (the Sales coordinator) I gave the role's load at each step.
11. Compounding with the check against what is finished. The check passed (16.9 against 17), which is a good sign, but it is not independent of the step table: both rest on the same counts, and the template does not say what the check can and cannot show.

**Shortcomings in this trial.** It was one run, by one model, on one invented example. I compared my output with the published output, so I can say they agree on the numbers and the finding; I cannot say how a different person or product would do. The acceptance tests were not run. The template's acceptance tests remain proposed.

## Edits made after this run

The template, the example and the public page were revised on 10 November 2026, after this run and after an independent review. These edits have not been run again. The figures, the constraint, the check's result and the three options' hours are unchanged on this example; several edits settle points listed above, and some change what a run prints, as noted.

- The check against what is finished now compares the number finished with the smaller of arrivals and the constraint's capacity, because a constraint below 100 percent can finish more than arrives. On this example the smaller is the capacity, 16.9, so the result is the same. The output format's check line now names which of the two was used; this run's line does not.
- An option's hours are now defined as the most it could return if the cause went away, and the format reads "Returns up to about [h] h a week ... if the cause went away". This settles ambiguity 5; this run already wrote "up to".
- Options are now stated as the outcome to reach, leaving how to the owner. The example's option 2 now reads as stopping the repricing caused by changes found at step 4, with the check kept, as this run's option 2 already did; the difference noted above about option 2 no longer applies.
- The send-back rule now says overlapping shares are added and a returned item goes round once only. This settles ambiguity 4; this run already worked that way. "What to customize" now asks for any wait outside the map, such as a customer's reply, in the notes (ambiguity 3).
- Number formats are now fixed: every hour figure to one decimal, waits and hours given included (1.0 h, 36.0 h); expected work per item and send-back multipliers to two decimals (0.60 h, 1.20); loads and the shares of work and waiting as whole percentages. This settles ambiguity 8 and the formatting difference noted above. This run's waits ("1 h", "18 h") and its "time target of 24 h" no longer fit; its hours given and multipliers already do. The example now uses these formats.
- Role hours now count as estimated unless the person says they were measured, and the constraint's role hours are listed under Figures to firm up. This settles ambiguity 7 for role hours; this run already listed the Estimator's 38 hours, and the example now does too.
- The instruction block's closing sentence now says to end with the draft line in the format. This settles ambiguity 1; this run already used the format's line.
- The example's output is now set out as plain lines in the order of the output format, as this run's was, instead of bold headings and bullets. Its open question now says that the notes give no customer reply time, rather than that the 2.0 h wait may be too short.
- One acceptance test was added, for a process where everything arriving is finished. The acceptance tests are not part of the pasted instructions.

No recorded output above was changed. One observation was corrected: the note on sections 10 and 11 said "two open questions" and listed three; it now says three.

## Later edits, 10 November 2026

Made in a second editorial review, after the edits above. None has been run again, and no recorded output or observation above was changed.

- The credits in the entry were reworded in Fully Powered AI's own words. This does not change what a run prints.
- The example's reasons in section 7 for steps 1 and 6 now rest on figures (the Estimator's 16.9 a week; the Sales coordinator's 25.7), so the two sentences this record calls reasoning rather than supplied facts are no longer in the example. Its line on the Estimator's 38 hours under Figures to firm up and its open question were reworded to the format; the figures are unchanged.
- The third kind of option at the constraint, removing a wait in front of it, now applies only where the notes show the wait leaves the constraint with nothing to work on, and returns the hours without work the notes give. This run proposed no such option, and neither does the example.
- The instruction block now says to leave the constraint "not confirmed" when arrivals are missing, to write "hours not supplied" for a role with no hours row, and to say whether an option also cuts the next role's load. The output format has a line for load not computed. This run already gave the effect of option 2 on the Production manager.
