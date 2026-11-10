# Operations KPI scorecard: tried on its example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

This run used only the invented inputs from the worked example (`public/example.md`): the settings, the seven-measure sheet for the invented wholesale distributor, the four exports, the scorecard history, the action list and the owners' notes. No client data was used. The assistant that ran it did not write the template. It followed the instruction block and the output format in `member/template.md`, and it did not read the example's output until its own scorecard was finished.

## What came out

This is the whole scorecard, in the template's format.

```
OPERATIONS KPI SCORECARD: October 2026

For: Operations manager, for the operations review on Monday 2 November 2026. Prepared Monday 2 November 2026 from the measure sheet (7 measures), wms_monthly.csv, low_stock_2026-10-31.csv, complaints.csv and transport_monthly.csv, the scorecard history (2026-08, 2026-09), the action list (4 actions) and owners' notes for M1, M2, M4, M6 and M7.
Overall: 2 red, 3 amber, 2 green, 0 not rated.

Scorecard
M1 On-time dispatch: 92.9%. RED. Target 97.0%; red at 93.0%; higher is better. Trend: 2026-08 97.4% · 2026-09 95.1% · 2026-10 92.9%, worse on last month, worse two months running. Owner: Warehouse manager.
M2 Pick errors: 4.2 per 1000 lines. RED. Target 2.0; red at 4.0; lower is better. Trend: 2026-08 2.1 · 2026-09 2.6 · 2026-10 4.2, worse on last month, worse two months running. Owner: Warehouse manager.
M3 Picking productivity: 56.0 lines per hour. GREEN. Target 55.0; red at 48.0; higher is better. Trend: 2026-08 57.2 · 2026-09 58.0 · 2026-10 56.0, worse on last month. Owner: Warehouse manager.
M4 Core range out of stock: 7 items. AMBER. Target 5; red at 12; lower is better. Trend: 2026-08 6 · 2026-09 4 · 2026-10 7, worse on last month. Owner: Purchasing lead.
M5 Customer complaints: 2.2 per 1000 orders. AMBER. Target 2.0; red at 4.0; lower is better. Trend: 2026-08 1.7 · 2026-09 1.5 · 2026-10 2.2, worse on last month. Owner: Customer service lead.
M6 Failed first deliveries: 1.8%. GREEN. Target 2.0%; red at 4.0%; lower is better. Trend: 2026-08 2.3% · 2026-09 2.2% · 2026-10 1.8%, better on last month, better two months running. Owner: Transport manager.
M7 Vehicle checks done: 99.1%. AMBER. Target 100.0%; red at 95.0%; higher is better. Trend: 2026-08 98.4% · 2026-09 99.6% · 2026-10 99.1%, worse on last month. Owner: Transport team. FLAG: the owner is a team, not a single person. See question 2.

How each value was worked out
M1: 3828 / 4120 × 100 = 92.9%. From wms_monthly.csv, the row for 2026-10.
M2: 262 / 61850 × 1000 = 4.2. From wms_monthly.csv, the row for 2026-10.
M3: 61850 / 1105 = 56.0. From wms_monthly.csv, the row for 2026-10.
M4: count of rows where core_range = Y and available = 0 = 7. From low_stock_2026-10-31.csv, 10 rows dated 2026-10-31. Rows left out: 3, because C-3320 has 6 available and S-7781 and S-7914 are not core range.
M5: 9 / 4120 × 1000 = 2.2. From complaints.csv, 9 rows logged in October 2026, and wms_monthly.csv, the row for 2026-10. Rows left out: 2, because CP-0412 was logged on 2026-09-30 and CP-0422 on 2026-11-01.
M6: 62 / 3460 × 100 = 1.8%. From transport_monthly.csv, the row for 2026-10.
M7: 541 / 546 × 100 = 99.1%. From transport_monthly.csv, the row for 2026-10.

What moved
M1 On-time dispatch, AMBER to RED (95.1% to 92.9%): "Two experienced pickers left at the end of September and the four agency pickers who replaced them started on 5 October. Most late orders were in the weeks of 5 and 12 October."
M2 Pick errors, AMBER to RED (2.6 to 4.2): "Mis-picks rose with the new agency pickers. Scan-to-confirm is fitted on twelve of the twenty pick faces; the last eight are waiting for brackets."
M4 Core range out of stock, GREEN to AMBER (4 to 7): "Two suppliers short-shipped gloves and catering foil. Both deliveries are due on 6 November."
M5 Customer complaints, GREEN to AMBER (1.5 to 2.2): reason not given by the owner.
M6 Failed first deliveries, AMBER to GREEN (2.2% to 1.8%): "Fewer failed drops on the rural routes this month; nothing changed in how we run them."

Reds and the actions agreed
M1 On-time dispatch, 92.9%: No open action agreed. See question 1.
M2 Pick errors, 4.2 per 1000 lines: A2 Fit scan-to-confirm on the twenty fastest-moving pick faces, owner Warehouse manager, due 2026-10-30, In progress.
M2 Pick errors, 4.2 per 1000 lines: A4 Pair each agency picker with an experienced picker for their first two weeks on the floor, owner Warehouse manager, due 2026-11-13, Open.

Ambers
M4 Core range out of stock, 7 items: 2 items from target, 5 items before red. "Two suppliers short-shipped gloves and catering foil. Both deliveries are due on 6 November."
M5 Customer complaints, 2.2 per 1000 orders: 0.2 from target, 1.8 before red. No note.
M7 Vehicle checks done, 99.1%: 0.9 points from target, 4.1 points before red. "Five checks were missed, all on Saturday shifts, when no supervisor is on site."

Last month's actions
A1 (M1) Add a second packer on the dispatch bench on Mondays and Tuesdays, owner Warehouse manager, due 2026-10-19: Done.
A2 (M2) Fit scan-to-confirm on the twenty fastest-moving pick faces, owner Warehouse manager, due 2026-10-30: In progress, OVERDUE.
A3 (M7) Shift lead signs off the Saturday vehicle checks, owner Transport manager, due 2026-10-31: Open, OVERDUE.

Measure sheet checks
Measures: 7 of at most ten. Leading: M4, M7. M7: the owner is given as "Transport team", a team rather than a single person or role. No differences between the history and the exports for September (M1, M2, M3, M6, M7 recomputed and match).

Questions for the Operations manager
1. M1 On-time dispatch is red at 92.9% and worse two months running. Its only action, A1, is Done, so no open action covers it. What action is agreed for M1, with which owner and date?
2. M7 Vehicle checks done names "Transport team" as its owner. Which one person or job role owns it?
3. A2 (M2), scan-to-confirm on the twenty fastest-moving pick faces, was due 2026-10-30 and is In progress. What is its new due date?
4. A3 (M7), the shift lead's sign-off of the Saturday vehicle checks, was due 2026-10-31 and is Open. What is its new due date?

Draft for the Operations manager's review. Every value traces to the exports named above. Nothing has been sent, posted or changed, and the assistant has set no measure, target, owner or action.
```

## What was observed

- **Every required part was produced.** All sections of the output format were filled, with the "none" lines unneeded. Nothing in the template told the assistant to stop: the sheet had seven measures, no duplicate codes, matching headers and every named column present, one row per month in each summary export.
- **Same result as the published example.** After the run, the output was compared with the example's output. Every value, status, trend, working, action match, overdue flag and question agrees. The differences are only in layout and wording: I wrote months as 2026-08 rather than "August", dates as 2026-10-30 rather than "30 October 2026", figures without thousands separators, the section lines as plain text rather than bold bullets, and I added to the measure sheet checks a line saying the September values recomputed from the exports match the history. The published example does not say that. The questions differ slightly in wording; the content is the same.
- **No facts beyond the inputs** in my output. In the published example's output, every figure and phrase also traces to the inputs.
- **Where the instructions needed a judgment.**
  - The "Last month's actions" section takes actions "agreed before the date of this month's review". The review and the run were on the same day, so A4 (agreed that day) was left out of that section. It still appears under the red it covers. The section's title says "last month" while its rule is a date, and the rule does not say what happens to an action agreed on the review day.
  - "Rows left out" for the low-stock export: the three rows are in the month but fail the formula's conditions, rather than falling outside the month. The template speaks of rows outside the month only. I reported them as left out with the reason, as the example does.
  - The format does not say in which order to list trend months; I used oldest to newest.
  - The format does not say how to write a date or a month (words or numbers); I used the numbers in the inputs.
  - The format has no way to draw attention to a green measure that keeps sliding. M3 is green but has fallen since September; the trend line shows it and no question is raised, because the rules ask for questions only in the listed cases.
  - An amber with no owner note (M5) raises no question, as written. A reader may want one; the template lists that as a thing to customize for status changes.
  - I recomputed September's values from the summary exports and noted that they match the history. The template asks for this only when a summary export holds last month's row and a difference appears, so the added line is my own. For M5 it could not be done, because the complaints log holds only one September row.
- **Shortcomings and cautions.** This was one run by one assistant on one invented example; it shows the instructions can be followed to a result a reader can check, not that other products or other data will behave the same. The template's own acceptance tests (renamed column, no rows for the month, eleven measures, wrong-side red level and others) were not run.

## Changed after this run, and not run again

Changed on 10 November 2026 after an independent review of the published template, and not run again. The output and the observations above are as recorded and describe the template and the example as they stood at the run. No change alters a value, a status, a trend, an action match or a question in either output.

- **Rows left out** now covers rows inside the month that do not meet the formula's conditions, as well as rows outside it, in the procedure and in the pasted instructions. This run and the example both reported the three low-stock rows that way.
- **Months and dates** are now written in words, such as "October 2026" and "30 October 2026", except when naming a row in an export, as in "the row for 2026-10". The example already wrote them so; this run wrote them as numbers. The example's working for M4 now says "10 rows dated 31 October 2026".
- **Last month's actions** now says, in the procedure and the pasted instructions, that it takes in older actions still on the list as well as last month's, and that an action agreed on the review day is not listed there. This run left A4 out of that section on the same reading.
- **What moved** now says that with no history there is no last status to compare, so only the reds are listed.
- **The purpose** now says the assistant proposes no action unless the operations manager asks for options to discuss, as the stop conditions and the pasted instructions already said.
- The check this run added, recomputing September's values against the history, was not added to the template.
