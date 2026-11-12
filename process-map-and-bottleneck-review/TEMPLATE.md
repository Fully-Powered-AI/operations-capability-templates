# Process map and bottleneck review

Workflow template, version 0.1.0.

## Purpose

Prepare a review of one repeating process from figures the team supplies: a map of every step with its role, the hours an item waits before it and the hours of work it takes, the hand-overs and the send-back loops; where the elapsed time goes; the weekly load on each role; the one step that limits how many items the process finishes; up to three things to try first at that step with the time and people already there; the steps to leave alone; and where the bottleneck goes next. Every figure traces to the inputs or to arithmetic on them that a reader can redo. The assistant prepares; it never changes a process, a system or anyone's work, never sends the review, and never decides what changes. The process owner decides.

## When to use it and when not to

Use it when people disagree about why one process takes so long, when work piles up in one place, before adding people or buying software to speed a process up, and again after a change has been tried, with fresh figures.

Do not use it:

- for several processes at once. One process per run; if the material covers more, the owner picks one;
- to write the procedure itself. That is the companion workflow template, Write an SOP from how the work is done;
- to judge whether a piece of work is ready for AI. That is Workflow fit check, which can follow once this review has named the step worth changing;
- for work done once, such as a project, which has no steady flow of items to measure;
- to judge how well a person works, to set anyone's workload or terms, or to decide whether to add staff. The review is about the process; it names roles, never individuals, and adding capacity is the owner's call;
- to change how a judgment reserved to a licensed or qualified person is made. The map can show who makes it and how long work waits for it; the options never alter the judgment itself.

## Roles

- **Runs it:** the operations lead or the process owner, with an AI assistant.
- **Supplies the figures and notes:** the people who do each step, or whoever keeps the job or ticket records.
- **Decides:** the process owner. Chooses what to try, who carries it and when to measure again.
- **Answers open questions:** the role each question names.

## Inputs

All times are in working hours.

1. **The process request.** The process name; the owner's role; what starts one item and what finishes it; the one number that should rise (for example quotes sent a week) and its current weekly value; items arriving a week; the period the figures cover; hours in a working day (default 8); and, optional, a time target for one item and the step people complain about most. If there is no named owner, stop and ask. If the number that should rise or its current value is missing, ask one question for it before anything else. If items arriving a week is missing, map the process and report the time, but write "load not computed: arrivals not supplied" and leave the constraint "not confirmed".
2. **The step table,** typed or exported, one row per step in order. Default column headings: `step`, `name`, `role`, `wait_before_hours`, `work_hours`, `sent_back_to`, `sent_back_per_10`, `basis`, `notes`. `wait_before_hours` is the typical time an item sits before the step starts; `work_hours` is the typical hands-on time per item; `sent_back_to` is the earlier step an item returns to when this step finds a problem, blank if none; `sent_back_per_10` is how many items in ten are sent back; `basis` is "measured" or "estimated". If the headings do not match these, stop: list the headings expected and the headings found, and ask which column is which. Never guess a mapping. If there is no step table, stop and ask for one; offer the headings above.
3. **Role hours,** one row per role. Default headings: `role`, `hours_per_week`, the hours that role gives to this process each week, all people in the role together. The same rule applies to headings that do not match. A role in the step table with no row here gets "hours not supplied" and no load. Role hours count as estimated unless the person says they were measured.
4. **Notes from the people who do the work** (optional): when approvals happen, why items come back, what else takes their time. If none, write "no notes supplied" in the header.

The assistant works only from what the person supplies. It needs no connection to any system and never asks for a password or a login code.

## The procedure

1. **Check the run.** One process, one named owner, one step table. If the table describes how the process should run rather than how it runs today, say so and ask for today's figures.
2. **Check the table.** Steps numbered 1 to n without gaps or repeats. Every row has a role and a work time; a blank becomes "not stated" and an open question. A `sent_back_to` must name an earlier step; a `sent_back_per_10` must be 0 to 10. If either is wrong, stop and ask. A blank `basis` counts as estimated.
3. **Draw the map.** For each step: its name, role, wait, work, whether it is a hand-over (its role differs from the step before), any send-back, and whether the figures are measured or estimated. Then count hand-overs, list the send-back loops with the roles at each end, and list which steps each role does.
4. **Count send-backs.** A send-back from step B to step A means the item goes through steps A to B once more. Its share is `sent_back_per_10` divided by 10. For each step, expected work per item is its work hours times one plus the shares of every send-back whose span includes it. Where send-backs overlap, their shares are added, and a returned item is assumed to go round once only; a second return is not counted. This rule is used for every load figure; when any send-back exists, state it under the load table with the expected work per item for each step a send-back touches.
5. **Where the time goes.** First pass: the sum of every wait and every work time, in hours and in working days, with work and waiting each as a whole percentage. Send-backs: for each loop, its share times the waits and work of every step in its span; add these for the average extra time, and give the all-in average. Against the time target, give how far over or under. List the three longest waits with their steps.
6. **Load by role.** Number formats, used throughout the review: every hour figure to one decimal, waits and hours given included (1.0 h, 36.0 h), except expected work per item, which takes two decimals (0.60 h); working days to one decimal; send-back multipliers to two decimals (1.20); loads and the shares of work and waiting to whole percentages; capacity to one decimal. For each role: arrivals a week times the expected work per item across all its steps gives the hours of work arriving a week. Divide by the role's hours a week for the load, as a whole percentage. Divide its hours a week by its expected work per item for how many items it can finish a week.
7. **Name the constraint.** The role with the highest load, at the steps it does.
   - At 100 percent or more: more arrives than it can finish; state arrivals, its capacity and how much the queue grows a week.
   - Within [your tie margin, default 5] percentage points of the next role: write "too close to call from these figures", name both, and make it a decision for the owner.
   - Highest load under [your nearly-full line, default 80] percent: write that no role on this map is nearly full at these arrivals, so the limit is how much arrives or something outside the map, and ask the owner.
   - A role with hours not supplied that could change the answer: write "not confirmed" and ask for its hours.
8. **Check it.** The process can finish no more than arrives and no more than the constraint can finish, so take the smaller of arrivals a week and the constraint's capacity, and compare it with the current value of the number that should rise. If they differ by more than [your agreement margin, default 20] percent of the current value, write "the figures disagree", keep the finding as not confirmed, and list the figures most likely wrong under Figures to firm up. If the longest wait sits before a step that is not the constraint, say so, with the reason the notes give (an approval day, work saved up, waiting on someone outside) or an open question. If the person named the step people complain about, say whether it is the constraint and why, using its load.
9. **Try first at the constraint.** Up to three options, using the time and people already there, each tied to a fact in the inputs, in this order of preference: stop work reaching the constraint that it will have to redo (send-backs into or through it); take away work the constraint does that is not this process, or that the notes say another role could do, leaving which role to the owner; remove a wait in front of it caused by a rule or by saving work up, where the notes show that wait leaves the constraint with nothing to work on. For each, give the hours a week of the constraint's time it would return, computed from the inputs (for a wait, the hours without work that the notes give) as the most it could return if the cause went away, labelled as arithmetic, not a forecast. Describe the outcome to reach (fewer items sent back, for example), not a new way of working the inputs do not show; how to reach it is the owner's choice. Never propose cutting a check that guards quality or safety. If no option is supported by the inputs, write "none found in the supplied figures".
10. **Then, if that is not enough.** One line: adding capacity at the constraint is the owner's decision, after the options above have been tried and measured; adding it anywhere else would not raise the number.
11. **Leave alone for now.** Every other step, with its role, its load and one line on why speeding it up would not raise the number. A step that matters to an option (because of what it checks, not how fast it is) says so.
12. **Where the bottleneck goes next.** The role with the second-highest load today and its load. If an option would also cut that role's load, say so.
13. **Figures to firm up.** Every estimated figure on the constraint's steps, on any step in a send-back loop through it, and behind any wait raised as a decision for the owner; the constraint's role hours, unless the person said they were measured; then any disagreement from step 8. If every figure is measured and nothing disagrees, write "none".
14. **Decisions and questions.** Decisions for the owner: which option to try first, who carries it and when to measure again; any tie or disagreement; any long wait that affects the time target but not the number. Open questions: every gap, each for a named role. Return the draft to the person who ran it.

## Exceptions and stop conditions

- **No named owner, no step table, or headings that do not match:** stop and ask, as set out under Inputs.
- **No number that should rise:** ask one question for it. Do not choose one.
- **A send-back that points forward, to a missing step, or a share outside 0 to 10:** stop and ask.
- **More than one process in the material:** list them and ask which to review.
- **Figures that disagree with what is finished:** report both, keep the constraint "not confirmed", and say which figures to check. Never adjust a figure to make it fit.
- **Notes that name a person or comment on how well someone works:** refer to the role only and leave the comment out.
- **Asked to pick the change, reassign work, change a system or send the review:** decline; name the owner as the one who decides and the role that would act.
- **Asked whether to add staff, or how many:** decline; give the constraint's load and capacity as facts for the owner.
- **The inputs contain bank details, a password or a login code:** do not repeat them; tell the person to remove them from the source.

## Output format

```
PROCESS MAP AND BOTTLENECK REVIEW: [process name]

For: [owner role]. Prepared [date] from [step table, n steps], [role hours], [notes / no notes supplied]. Figures cover [period].
One item: starts when [trigger]; ends when [end].
The number that should rise: [measure], now [n] a week. Arriving: [n] a week / arrivals not supplied. Time target: [target / none set].

1. The map
Step [n]. [Name]. [Role / not stated]. Waits [h] h, then [h] h of work. [Hand-over from [role].] [Sent back to step [n] in [n] of 10.] [Measured / Estimated].
Hand-overs: [n] ([role] to [role], ...). Send-backs: [step n to step n, [n] in 10, [role] to [role]; ... / none].
By role: [Role]: steps [n, n]. ...

2. Where the time goes
First pass: [h] h ([d] working days): [h] h of work ([%]), [h] h waiting ([%]).
Send-backs add [h] h on average ([loop]: [share] x [h] h = [h] h; ...), [h] h ([d] working days) in all. / No send-backs.
Against the time target of [h] h: [over by [h] h first pass and [h] h with send-backs / within it / no target set].
Longest waits: before step [n] ([h] h), before step [n] ([h] h), before step [n] ([h] h).

3. Load by role
[Role] (steps [n]): [h] h of work a week against [h] h given: [%]. Can finish about [n] a week. / Hours not supplied.
/ Load not computed: arrivals not supplied.
[Send-backs counted: each one repeats the steps from where the item returns to where it was found, once. Expected work per item: step [n], [h] h x [multiplier] = [h] h; ...; all other steps as listed.]

4. The constraint
[Role], at step(s) [n]: [%]. [More arrives than it can finish: [n] a week against about [n]; the queue in front of step [n] grows by about [n] a week.]
/ Too close to call from these figures: [role] [%] and [role] [%]. / No role on this map is nearly full: [...]. / Not confirmed: [why].
Check against what is finished: about [n] a week expected ([the constraint's capacity / arrivals], the smaller of the two) against [n] now: [the figures agree / the figures disagree].
The step people complain about: step [n] is / is not the constraint: [reason, with its load]. / Not named.
[The longest wait, before step [n], is not at the constraint: [reason from the notes / reason not known, see question n].]

5. Try first at the constraint
[n]. [Option]. Based on: [fact from the inputs]. Returns up to about [h] h a week of [role] time if the cause went away ([arithmetic]). Arithmetic on the supplied figures, not a forecast.
/ None found in the supplied figures.

6. Then, if that is not enough
If [role] is still the most loaded role after these are tried and measured, adding capacity at step [n] is the owner's decision; adding it at any other step would not raise [measure].

7. Leave alone for now
Step [n] ([role], [%]): [why speeding it up would not raise the number]. / None: every step is at the constraint.

8. Where the bottleneck goes next
[Role], at [%] today. [Effect of an option on it, if any.]

9. Figures to firm up
[Step n, figure / Role, hours given]: [estimated / disagrees with what is finished]. [Why it matters.] / None.

10. Decisions for the owner
[n]. [Question, with its facts.]

11. Open questions
[n]. [Question], for [role]. / None.

Draft for the [owner role]. Nothing has been changed, assigned or sent. The owner decides what changes.
```

## Reviewer checklist

1. Every step, role and time on the map matches the step table; nothing is added. (Operations lead)
2. Every total, percentage, load and capacity can be recomputed from the inputs, and the send-back rule is applied the same way throughout. (Operations lead)
3. The constraint is the role with the highest load, or the review says why it is not confirmed or too close to call. (Process owner)
4. The check against what is finished is present and honest. (Process owner)
5. Every option sits at the constraint, rests on a fact in the inputs, uses the time and people already there and removes no quality or safety check. (Process owner)
6. No option or line judges an individual or proposes changing anyone's terms. (Operations lead)
7. Every estimate that affects the finding is listed under Figures to firm up. (The role that keeps the figures)
8. The draft line is present and nothing is described as changed. (Process owner)

## Acceptance tests

Proposed tests. None has been run.

1. **Clear constraint.** Six steps, one role at 118 percent and the next at 87. Expected: that role named, the queue growth stated, the check against what is finished shown, the second role under "Where the bottleneck goes next".
2. **Headings do not match.** The table uses "Owner" and "Queue time". Expected: stops, lists expected and found headings, asks which is which; no map drawn.
3. **The blamed step is not the limit.** The person names a step at 87 percent while another is at 118. Expected: says plainly it is not the constraint, with both loads.
4. **Long wait, low load.** The longest wait sits before an approval at 67 percent, and the notes say approvals happen twice a week. Expected: the wait is reported as not at the constraint, with the approval days as the reason, and turnaround is raised as an owner's decision, not as the constraint.
5. **Too close to call.** Two roles at 96 and 93 percent. Expected: "too close to call", both named, a decision for the owner; no single constraint.
6. **Nobody is nearly full.** Highest load 55 percent. Expected: says no role on the map is nearly full and asks the owner where the limit is.
7. **Figures disagree.** The constraint can finish 10 a week by the arithmetic, but 17 a week are finished. Expected: "the figures disagree", the finding not confirmed, the figures to check listed.
8. **Send-back pointing forward.** Step 2 sent back to step 5. Expected: stops and asks.
9. **No number to raise.** Expected: one question asking for the number and its current value, before any map.
10. **Asked to decide.** "Just tell me who to move onto quoting." Expected: declines, gives the load and capacity facts, leaves the choice to the owner.
11. **A note about a person.** "She is slow at checking." Expected: the comment is left out; the step is referred to by role.
12. **Everything arriving is finished.** 12 arrive a week, 12 are finished, and the most loaded role is at 82 percent, able to finish about 14.6 a week. Expected: the check compares 12 (arrivals, the smaller) with 12 finished and says "the figures agree"; it does not compare 14.6 with 12.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a process map and bottleneck review of ONE repeating process
for its owner. You prepare; the owner decides. You never change a
process, a system or anyone's work, never assign work, never send the
review, and never decide what changes. You never ask for a password or
a login code and need no connection to any system. All times are
working hours.

The user will supply: the process request (name, owner's role, what
starts and ends one item, the number that should rise and its current
weekly value, items arriving a week, period, hours in a working day,
optional time target and the step people complain about); a step table
with headings step, name, role, wait_before_hours, work_hours,
sent_back_to, sent_back_per_10, basis, notes; a role hours table with
headings role, hours_per_week; optional notes from the people who do
the work.

Before anything else:
1. With no named owner or no step table, stop and ask. With no number
   that should rise or no current value, ask one question for it.
2. If headings differ from those above, stop: list expected and found
   headings and ask which is which. Never guess.
3. One process only; if there are more, ask which. If the table shows
   how the process should run, not how it runs, ask for today's.
4. Steps run 1 to n with no gaps. sent_back_to must be an earlier step
   and sent_back_per_10 must be 0 to 10, or stop and ask. A missing
   role or work time is "not stated" and an open question. A blank
   basis counts as estimated.

Then:
5. Map every step: name, role, wait, work, hand-over (role differs from
   the step before), send-back, measured or estimated. Count hand-overs,
   list send-back loops with the roles at each end, list steps by role.
6. Send-backs: one from step B to step A repeats steps A to B once, with
   share = sent_back_per_10 / 10. A step's expected work per item is its
   work hours x (1 + the shares of every loop whose span includes it).
   Overlapping shares are added; a returned item goes round once only.
   Under the load table, state this rule and each such step's figure.
7. Time: first pass = all waits + all work, in hours and working days,
   with work and waiting as whole percentages. Each loop adds its share
   x the waits and work across its span; give the average added and the
   all-in figure. Compare with the time target. List the three longest
   waits.
8. Load: for each role, arrivals a week x its expected work per item
   across its steps, against its hours a week, as a whole percentage;
   capacity = its hours / its expected work per item. Without arrivals,
   write "load not computed: arrivals not supplied" and leave the
   constraint "not confirmed". A role with no hours row gets "hours not
   supplied" and no load.
9. Constraint = the role with the highest load. At 100% or more, give
   arrivals, capacity and weekly queue growth. Within [your tie margin,
   default 5] points of the next: "too close to call", name both, make
   it an owner's decision. Highest under [your nearly-full line, default
   80]%: say no role is nearly full and ask the owner. Missing hours that
   could change it: "not confirmed".
10. Take the smaller of arrivals a week and the constraint's capacity
   and compare it with the current number. A gap over [your agreement
   margin, default 20]% of the current number: "the figures disagree",
   finding not confirmed. Say whether the longest wait is at the
   constraint, giving the notes' reason or an open question. Say
   whether the step people complain about is the constraint, with its
   load.
11. Up to three options at the constraint, using the time and people
   already there, each tied to a fact in the inputs: first, stop work
   reaching it that it will redo; then take away work it does that is
   outside this process or that the notes say another role could do,
   leaving which role to the owner; then remove a wait before it caused
   by a rule or by saving work up, where the notes show it leaves the
   constraint with nothing to work on. Give the hours a week each
   returns: the most it could return if the cause went away (for a
   wait, the hours without work the notes give), as arithmetic, not a
   forecast. State each as the outcome to reach, not a new way of
   working the inputs do not show; how is the owner's choice. Never
   propose removing a quality or safety check. If none is supported,
   say so.
12. One line: adding capacity at the constraint is the owner's decision
   after the options are tried and measured; elsewhere it would not
   raise the number. Then every other step with its role, load and why
   speeding it up would not help. Then the role with the second-highest
   load as where the bottleneck goes next, and whether an option would
   also cut its load.
13. List figures to firm up (estimates on the constraint, in a loop
   through it or behind a wait raised as a decision; the constraint's
   role hours unless said to be measured; any disagreement); decisions
   for the owner (which option first, who carries it and when to
   measure again; any tie or disagreement; any long wait that affects
   the time target but not the number); and open questions, each for a
   named role. Write "none" where a list is empty.

Show every hour figure to one decimal, waits and hours given included
(1.0 h, 36.0 h), except expected work per item, to two (0.60 h).
Working days to one decimal, send-back multipliers to two (1.20),
loads and the shares of work and waiting to whole percentages, and
capacity to one decimal. Role hours count as estimated unless the user
says they were measured. Name roles, never people; leave out any
comment on how well someone works. Never adjust a figure to make it
fit. If asked to choose the change, reassign work, change a system,
send the review or say whether to add staff, decline and leave it to
the owner. If the inputs hold bank details or a password, do not
repeat them and ask the user to remove them. Use the output format
exactly and end with the draft line in the format: nothing has been
changed, assigned or sent, and the owner decides what changes.
```

## What to customize

- The process and its owner, and the one number it exists to raise.
- Your column headings, if your job or ticket system exports different ones; tell the assistant the mapping once.
- [your nearly-full line], default 80 percent; [your tie margin], default 5 percentage points; [your agreement margin], default 20 percent.
- Hours in a working day, and whether waits are counted in working hours or calendar hours.
- The send-back rule. As written, a returned item repeats every step in the loop once, waits the typical time again at each and is not sent back a second time. If a return waits on someone outside the map, such as a customer's reply, give that wait in the notes.
- Whether options may propose moving work between roles, or only changes inside the constraint's own step.
- Who keeps the figures, and where each review is stored so the next run starts from the last.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried once on its invented example, in Claude on 10 November 2026; the record is published with it. The figures and the finding matched the example, and the record lists the places where the instructions left the assistant a choice. After that run and an independent review, the instructions were clarified in small ways: the check against what is finished uses the smaller of arrivals and the constraint's capacity; an option's hours are the most it could return; overlapping send-backs are added and a returned item goes round once; number formats are fixed; the constraint's role hours are listed under Figures to firm up unless measured; and the closing line follows the format. Later the same day, in a second editorial review: a wait removed in front of the constraint counts only where the notes show it leaves the constraint with nothing to work on, and returns the hours without work the notes give; the instruction block now says what to do when arrivals or a role's hours are missing, and asks whether an option also cuts the next role's load; and the output format has a line for load not computed. These edits have not been run again. One run on an invented example is not a test. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
