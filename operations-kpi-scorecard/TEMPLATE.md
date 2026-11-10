# Operations KPI scorecard

Capability template, version 0.1.0.

## Purpose

Prepare the monthly red-amber-green scorecard for the measures the operations manager has chosen to run the operation by, ten at most. Each value is worked out from the exports the person supplies, using the formula on the measure sheet, and shown with its working. Each measure gets its status against its target and red level, its trend over three months, the reason it moved in its owner's own words, and, for every red, the action a person agreed. The assistant prepares; it never chooses a measure, sets or changes a target or red level, names an owner, decides an action or proposes one unless the operations manager asks for options to discuss, rates an individual's performance, sends the scorecard or changes any record.

## When to use it and when not to

Use it once a month, after the month's exports are out and before the operations review, and again after the review once the actions for the reds are agreed and written into the action list. The second run is the scorecard that is kept.

Do not use it:

- to choose the measures or set the targets. The operations manager writes the measure sheet first; this capability reads it and checks it;
- for financial results such as revenue, margin, receivables or spend against budget. Those belong to finance's own monthly work;
- to define a service promise to customers, such as response or resolution times. That is a separate piece of work;
- to judge or compare individual employees. The scorecard covers the operation, never a person's performance;
- when the measure sheet has more than ten measures, until the operations manager has chosen the ten.

## Roles

- **Runs it:** the operations manager, or an analyst or coordinator preparing it for them.
- **Chooses the measures, writes the definitions and formulas, sets each target and red level, names each owner:** the operations manager, with the owner or general manager where the business wants it.
- **Explains a move in their measure:** the measure's owner, in a short note.
- **Agrees the action for every red, with its owner and date:** the operations manager and the measure's owner, at the monthly review.
- **Reads the approved scorecard:** the owner, general manager or leadership team the business names.

## Inputs

1. **The measure sheet,** one row per measure, set by the operations manager. Default column headers: `code, measure, definition, formula, source_file, period_column, unit, better, target, red, owner, type`. `formula` names the columns it uses exactly as they are headed in the export. `source_file` names the export or exports the formula reads, separated by semicolons, and `period_column` names, in the same order, the column in each that places a row in a month. `better` is `higher` or `lower`. `type` is `leading` (signals trouble before it shows in results) or `lagging` (reports results already in). If there is no measure sheet, stop and ask. If it has more than ten measures, stop and ask which ten the scorecard covers. If a header does not match, stop, show the expected and the found headers, and ask which column is which. Never guess.
2. **The exports** the measure sheet names: summary exports with one row per month, line-level exports with one row per event or item, or both. Their column headers are the ones the formulas name. If a named export is missing, stop and ask for it. If a column a formula names is not in its export, stop, show the column expected and the headers found, and ask. Never guess which column was meant.
3. **The scorecard history:** earlier months' values and statuses. Default column headers: `code, month, value, status`, with the month written as YYYY-MM. If a header does not match, stop and ask, as for the measure sheet. If there is no history, continue and write "no history supplied" in every trend.
4. **The action list:** actions agreed at this and earlier reviews. Default column headers: `ref, code, action, owner, due, status, agreed_on`. Status is the business's own, such as Open, In progress or Done. Actions closed and reported in an earlier scorecard are left off the list by the person who keeps it. If a header does not match, stop and ask. If there is no action list, continue, write "action list not supplied" in the header, and treat every red as having no open action.
5. **The owners' notes:** a line or two from each owner on why their measure moved, by measure code. If none are supplied, write "no owner notes supplied" in the header.
6. **The settings:** the month being scored, today's date, the date of the review, and who the operations manager is. If the month is missing, stop and ask.

The assistant works only from what the person supplies. It needs no access to any system and never asks for a password or a login code.

## The procedure

1. **Check the measure sheet.** Count the measures; more than ten, stop and ask. Two rows with the same code, stop and ask. For each measure check: a definition and a formula; a target and a red level; `better` given; the red level on the far side of the target (below it when higher is better, above it when lower is better); one owner who is a single person or a single job role, not a team, a department or "everyone". Write each problem as a flag on the measure. A measure with no formula, no target, no red level, no `better`, or a red level on the wrong side of the target is rated NOT RATED. A measure whose only problem is its owner is rated as usual and flagged. Note which measures are leading; if none is, say so under the measure sheet checks and ask whether that is intended.
2. **Check the exports.** For every formula, confirm that each column it names is in the export it names; if not, stop as set out under Inputs. For a summary export, find the row for the month in its period column. No row: the measure has no data. Two rows for the month: stop and ask which is right.
3. **Work out each value.** Apply the formula exactly as written. For a line-level export, count or add only the rows whose period column falls inside the month and that meet the formula's conditions, and record how many rows were left out and why: outside the month, or not meeting the formula's conditions. If a line-level export has no rows for the month, do not treat that as zero: rate the measure NOT RATED, write "no rows for [month] in [file]", and ask whether the true value is zero. Round a percentage or a rate to one decimal place and a count to a whole number. Write the working for every measure: the figures, the calculation and the result.
4. **Rate each measure** on the value as shown, after rounding. When higher is better: GREEN at or above the target, RED at or below the red level, AMBER between them. When lower is better: GREEN at or below the target, RED at or above the red level, AMBER between them. Use the target and red level on this month's sheet only.
5. **Show the trend.** From the history, give the values for the two months before this one, then this month's. Say whether this month is better, worse or unchanged on last month, judged by `better`. If it is worse than last month and last month was worse than the month before, add "worse two months running"; the same for better. A month not in the history is written "[month] not in history". If a summary export also holds last month's row and the value it gives differs from the history, keep the history and note the difference under the measure sheet checks.
6. **Say what moved.** List every measure whose status differs from last month's status as recorded in the history, and every red, even if it was red last month. For each, give the change in status and value and the owner's note as written. With no note, write "reason not given by the owner". With no history there is no last status to compare, so list the reds only. Never supply a reason of your own, and never draw a cause from the data that the owner has not stated.
7. **Match the reds to actions.** For each red, list every action in the action list with that measure's code and a status other than Done or Closed, with its owner, due date and status. A red with no such action is shown "No open action agreed" and gets a question. An action marked Done does not cover this month's red.
8. **Show the ambers.** For each amber, give how far it is from its target and how far from its red level, in the measure's unit, and the owner's note if there is one.
9. **Report last month's actions.** List every action in the action list agreed before the date of this month's review, last month's and any older ones still on the list; an action agreed on the review day is not listed here. Give its status as supplied, and OVERDUE if its due date is before today and its status is not Done or Closed. Report a status only as supplied; never mark an action done.
10. **Write the questions.** One numbered question for the operations manager for each: red with no open action; flagged measure; measure with no data; overdue action; red with no owner note. Give the facts, then the question. Recommend nothing unless the operations manager asks.
11. **Return the draft** to the person who ran it, for the operations manager's review. A person decides who receives the approved scorecard and sends it.

## Exceptions and stop conditions

- **No measure sheet, more than ten measures, or two measures with the same code:** stop and ask. Never supply a standard set of measures.
- **A header in the measure sheet, the history or the action list does not match, or a column a formula names is missing from its export:** stop, show expected and found, and ask.
- **Two rows for the month in a summary export:** stop and ask which is right.
- **A summary export also holds last month's row, and the value worked out from it differs from the value in the history:** use the history as recorded for the trend and the status change, and note the difference under the measure sheet checks for the operations manager.
- **Asked to choose or drop a measure, set or change a target or red level, or name an owner:** decline; the operations manager decides.
- **Asked to propose or decide an action for a red:** decline and record the red as a question. If the operations manager asks for options to discuss, list them under the question, marked "for discussion, not agreed", and never in the action list.
- **Asked to change a value, round differently or rate a measure other than by the rule, so that it looks better:** decline and show the working.
- **Asked to rate, rank or compare named employees, or an export lists people by name:** decline the rating; refer to people by job role only, and leave names out of the scorecard.
- **An export contains customers' personal details, bank details, a password or a login code:** do not repeat them; tell the person to remove them from the source.

## Output format

```
OPERATIONS KPI SCORECARD: [month year]

For: [operations manager role], for the operations review on [weekday date]. Prepared [date] from the measure sheet ([n] measures), [exports, by file name], the scorecard history ([months] / no history supplied), the action list ([n] actions / action list not supplied) and [owners' notes for codes / no owner notes supplied].
Overall: [n] red, [n] amber, [n] green, [n] not rated.

Scorecard
[Code] [Measure]: [value and unit]. [RED / AMBER / GREEN / NOT RATED]. Target [target]; red at [red]; [higher / lower] is better. Trend: [month] [value] · [month] [value] · [month] [value], [better / worse / unchanged] on last month[, worse two months running / better two months running] / no history supplied. Owner: [owner]. [FLAG: the problem. See question [n].]

How each value was worked out
[Code]: [figures and calculation] = [result]. From [file], [the row for month / n rows in the month]. [Rows left out: [n], because [reason].] / [No rows for [month] in [file].]

What moved
[Code] [Measure], [last status] to [this status] ([last value] to [this value]): [owner's note / reason not given by the owner].
/ No measure changed status and none is red.

Reds and the actions agreed
[Code] [Measure], [value]: [Ref] [action], owner [role], due [date], [status].
[Code] [Measure], [value]: No open action agreed. See question [n].
/ No measure is red.

Ambers
[Code] [Measure], [value]: [gap] from target, [margin] before red. [Owner's note / No note.]
/ No measure is amber.

Last month's actions
[Ref] ([code]) [action], owner [role], due [date]: [status as supplied][, OVERDUE].
/ No actions carried from last month.

Measure sheet checks
Measures: [n] of at most ten. Leading: [codes / none, see question [n]]. [Code]: [flag]. [Differences between the history and the exports, or targets changed.]
/ Measures: [n] of at most ten. Leading: [codes]. No problems found.

Questions for the [operations manager role]
[n]. [The facts.] [The question.]
/ None.

Draft for the [operations manager role]'s review. Every value traces to the exports named above. Nothing has been sent, posted or changed, and the assistant has set no measure, target, owner or action.
```

Write months and dates in words, such as "October 2026", "30 October 2026" and "Monday 2 November 2026". Keep an export's own form only when naming a row in it, as in "the row for 2026-10".

## Reviewer checklist

1. Every measure on the sheet appears once, with its target, red level and owner unchanged, and there are ten or fewer. (Operations manager)
2. Every value can be recomputed from the export with the working shown, and the rounding is right. (Analyst or coordinator)
3. Every status follows the rule for its direction, judged on the value as shown. (Operations manager)
4. No measure with missing data has been rated as if its value were zero. (Analyst or coordinator)
5. Every reason under "What moved" is the owner's own, or says that none was given. (Each owner)
6. Every red has an open agreed action, or a question asking for one; no action appears that nobody agreed. (Operations manager)
7. Every overdue action is marked, and no status has been changed by the assistant. (Operations manager)
8. No named employee is rated or compared, and no customer's personal details appear. (Operations manager)
9. The scorecard is approved before it is shared. (Operations manager)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary month.** Seven measures, all exports present, history for two months, every red with an open action. Expected: every value worked out and rated; trends shown; no questions except those the rules require.
2. **Value exactly on the red level.** Higher is better, red at 93.0%, value 93.0%. Expected: RED.
3. **Value between rounding steps.** 92.96% against a red level of 93.0%. Expected: shown as 93.0% and rated RED, judged on the value as shown.
4. **Renamed column.** An export headed `on_time` where the formula names `orders_on_time`. Expected: stops, shows the column expected and the headers found, and asks; nothing drafted.
5. **No rows for the month.** A complaints log with rows only from the month before. Expected: NOT RATED, "no rows for [month] in [file]", and a question asking whether the true value is zero.
6. **Eleven measures.** Expected: stops and asks which ten.
7. **Team as owner.** Owner given as "Transport team". Expected: rated as usual, flagged, and a question asking which one person owns it.
8. **Red level on the wrong side.** Higher is better, target 95%, red at 97%. Expected: NOT RATED, flagged, and a question.
9. **Red covered only by a done action.** Last month's action for the measure is Done and nothing new is open. Expected: "No open action agreed" and a question.
10. **Overdue action.** Due before today, status In progress. Expected: OVERDUE under last month's actions and a question.
11. **No owner note on a red.** Expected: "reason not given by the owner" and a question; no reason supplied by the assistant.
12. **Asked to suggest the actions.** Expected: declines to put any in the action list; options listed only under the question, marked "for discussion, not agreed", if the operations manager asks for them.
13. **An error log naming pickers.** Expected: the value counted; no names in the scorecard; no individual rated.

## Instructions for the AI assistant

```
You prepare the monthly operations KPI scorecard for an operations
manager, from their measure sheet and the exports they supply. You
prepare; people decide. You never choose a measure, set or change a
target or red level, name an owner, propose or decide an action, mark
an action done, rate or compare an individual employee, send the
scorecard or change any record. You never ask for a password or a login
code and need no access to any system.

The user will supply: the measure sheet (code, measure, definition,
formula, source_file, period_column, unit, better, target, red, owner,
type); the exports it names; the scorecard history (code, month, value,
status); the action list (ref, code, action, owner, due, status,
agreed_on); the owners' notes; and the month, today's date, the review
date and the operations manager's role. If the measure sheet or the
month is missing, stop and ask. If the sheet has more than ten measures
or two with the same code, stop and ask. If a header in the sheet, the
history or the action list does not match, or a column a formula names
is not in its export, stop, show the expected and the found headers,
and ask. Never guess a column. If a named export is missing, stop and
ask for it. If the history, action list or notes are missing, say so in
the header and continue.

1. Check each measure: definition and formula present; target and red
   level present; better is higher or lower; the red level lies beyond
   the target in the bad direction; one owner who is a single person or
   role, not a team. Flag every problem on the measure. No formula,
   target, red level or better, or a red level on the wrong side:
   NOT RATED. Owner problem only: rate as usual and flag. Say which
   measures are leading; if none, say so and ask.
2. Work out each value with the formula exactly as written. Summary
   export: use the row for the month; two rows, stop and ask. Line-level
   export: use only rows whose period column falls in the month and
   that meet the formula's conditions, and say how many rows were left
   out and why: outside the month, or not meeting the formula's
   conditions. No row or no rows for the month: NOT RATED, "no rows
   for [month] in [file]", and ask whether the true value is zero.
   Never count missing data as zero. Round percentages and rates to
   one decimal, counts to whole numbers. Show the working for every
   value.
3. Rate on the value as shown. Higher is better: GREEN at or above
   target, RED at or below the red level, AMBER between. Lower is
   better: GREEN at or below target, RED at or above the red level,
   AMBER between.
4. Trend: the two earlier months from the history and this month; better,
   worse or unchanged on last month by the measure's direction; add
   "worse two months running" or "better two months running" where it
   applies. A missing month is "[month] not in history". If a summary
   export also holds last month's row and it gives a different value
   from the history, keep the history and note the difference under
   the measure sheet checks.
5. What moved: every measure whose status differs from last month's
   recorded status, and every red. Give the change and the owner's note
   as written; with no note, "reason not given by the owner". With no
   history, list the reds only. Never give a reason or cause of your
   own.
6. Reds: list each action for that code whose status is not Done or
   Closed, with owner, due date and status. None: "No open action
   agreed" and a question. A Done action does not cover this month.
7. Ambers: the gap to target and the margin before red, in the unit,
   with the owner's note if any.
8. Last month's actions: each action agreed before this month's review
   date, older ones still on the list included (an action agreed on the
   review day is not listed here), with its status as supplied, marked
   OVERDUE when due before today and not Done or Closed.
9. Questions, numbered, for the operations manager: each red with no
   open action, each flagged measure, each measure with no data, each
   overdue action, each red with no owner note. Facts, then the
   question. Recommend nothing unless asked; if asked for options for a
   red, list them under its question marked "for discussion, not
   agreed", never in the action list.
10. Use the output format exactly. Write months and dates in words,
    such as October 2026 and 30 October 2026, except when naming a row
    in an export (the row for 2026-10). Where a section has nothing in
    it, print its "none" line. End with the draft line saying nothing
    has been sent, posted or changed and no measure, target, owner or
    action was set by you.

If asked to change a value, rounding or status to make a measure look
better, decline and show the working. If an export names employees,
refer to them by job role only and rate no one. If an input contains
customers' personal details, bank details or a password, do not repeat
them; tell the user to remove them. Check every value against its
working before you return the scorecard.
```

## What to customize

- Your measures, ten at most: the definitions, formulas, targets, red levels and owners, set by the operations manager.
- The exports each formula reads, and their column headers as your systems produce them.
- Your action statuses, if you use words other than Open, In progress, Done and Closed.
- Rounding, if a measure needs more than one decimal place.
- Who adds owners' notes, and by which working day after the month ends.
- Whether a status change with no owner note should also raise a question; as written, only a red without a note does.
- Who receives the approved scorecard, in what form, and where the history is kept for next month.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried on its invented example in Claude on 10 November 2026. Small edits made to the procedure, the output format and the pasted instructions after the recorded run have not been run again; the trial record lists them. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
