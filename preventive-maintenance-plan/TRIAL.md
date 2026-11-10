# Preventive maintenance plan: tried on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Opus 5.5 (model ID claude-opus-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in [example.md](example.md): the settings, the equipment register, the maker's tasks, the failure history and the spare parts list of an invented 35-person bakery. No client data was used. The run was a fresh session with no tools: its instructions were the template's instruction block followed by the output format, and its one message was the example's inputs. It did not see the example's output. The template's latest edits were made by a separate session of the same model, which had read the example.

This record replaces the record of an earlier run the same day, by Claude Sonnet 5.5, on the template as it stood before the second round of review edits. Those edits tightened how a failure is linked to a task (the cause must name the task's part as the thing that failed; a shared word alone does not count, and the tasks of a run-to-failure asset are not examined), said what happens when linked failures are closer together than any interval step, said how to date a monthly task whose day does not exist in the target month, and added a question for a task whose last done date is the date of a failure of its own part. The example's header also gained "Defaults used: none." This run is on the edited template.

## What came out

The model followed the instruction block and the output format on those inputs and produced all eight sections. Its output, in substance:

**Header.** Plan period 4 January 2027 to 2 January 2028 (52 weeks). History 7 rows. Sources: 6 assets, 13 tasks, 11 parts. Defaults used: none. No name left out. Assets 6: band A 3, B 2, C 1, not banded 0; safety-critical 2. Approaches: run to failure 1, scheduled 4, condition-based 1. Tasks on the calendar 13 (12 from the maker's tasks, 1 condition check); left off 1. Flagged 2 assets and 1 history item; 3 decisions.

**1. Ranked by failure cost.**
1. OVN-01 gas oven, $6,300 = 8 h x $600 + $1,500 (manager's estimate). Band A. Safety-critical.
2. MIX-01 spiral mixer, $4,600 = 6 h x $600 + $1,000 (from history, 3 failures). Band A. Flag: interval proposed from history.
3. CHL-01 walk-in chiller, $2,700 = 10 h x $150 + $1,200 (estimate). Band B. Flags: condition check has no limit, overdue, no record, part lead time not stated.
4. CMP-01 air compressor, $2,300 = 5 h x $300 + $800 (estimate). Band A (safety-critical).
5. WRP-01 flow wrapper, $1,330 = 4 h x $200 + $530 (from history, 2 failures). Band B.
6. SLC-01 bread slicer, $260 = 2 h x $40 + $180 (from history, 1 failure). Band C.

**2. Approach.** OVN-01 and CMP-01 scheduled (safety-critical, no condition check). MIX-01 condition-based (band A, not safety-critical, check limit 70 C). CHL-01 scheduled (its check has no numeric limit). WRP-01 scheduled (band B, no check). SLC-01 run to failure.

**3. Calendar.** A line saying there are no closed days, so no date was moved. Weekly: WRP-01 jaws and CMP-01 receiver, next due 7 January 2027. Monthly: MIX-01 bearing temperature check (4 January, new), OVN-01 door seals (21 January), CHL-01 door gasket and heater (4 January, no record). Dated tasks: MIX-01 drive belt check every quarter, proposed from history against the maker's 6 months: 6 Jan, 6 Apr, 6 Jul, 6 Oct. MIX-01 bearing grease, 500 / 60 = 8.33 rounded down to every 8 weeks: 11 Jan, 8 Mar, 3 May, 28 Jun, 23 Aug, 18 Oct, 13 Dec. CHL-01 condenser coil on 4 January (overdue, was due 12 August 2026), then 4 Apr, 4 Jul, 4 Oct. OVN-01 burners and flues 14 Jan and 14 Jul; gas system service 20 Jan. WRP-01 heater elements, 2,000 / 50 = every 40 weeks: 19 Jan, 26 Oct. CMP-01 pressure system inspection 9 Mar; oil and filter, 2,000 / 60 = 33.33 rounded down to every 33 weeks: 22 Mar, 8 Nov. February, September and January 2028 (to 2 January) say "None beyond the weekly and monthly tasks." Left off: SLC-01 blade sharpening, every 6 months. Assets with no maker's tasks: none. Every safety-critical task carries the competent-person line.

**4. Spare parts.** Short: burner igniter 1 ($95, band A minimum), oven door seal kit 1 ($240), film sensor 1 ($310), cutting knife 1 ($22; use during the lead time 1.50, hold 2, have 1), air filter element 1 ($38). Total $705, for the operations manager's approval; nothing ordered. Condenser fan motor: lead time not stated, minimum not worked out. The other five parts: enough. No part is for an asset off the register.

**5. Measures (5 January 2026 to 3 January 2027).** MIX-01: 3 failures, 18 h stopped (average 6.0), repair 13 h (4.3), 3,120 run hours, 1,040 between failures, $3,000. WRP-01: 2 failures, 8 h (4.0), repair 5 h (2.5), 2,600 run hours, 1,300 between, $1,060. SLC-01: 1 failure, 2 h, repair 1 h, 2,080 run hours, $180. OVN-01, CHL-01 and CMP-01: no failures in 3,640, 8,736 and 3,120 run hours. All registered assets: 6 failures, 28 h (4.7), repair 19 h (3.2), $4,240. History item not counted: PAL-01, 3 March 2026, battery fault. Six measures to track with baselines (6 and 28 h in the history period, 4.7 h, 3.2 h, run hours between failures for each band A and B asset, and none for tasks done on time). No targets.

**6. Competent person.** OVN-01 and CMP-01: tasks at the maker's intervals with next due dates, no failures, parts short (igniter and door seal kit; air filter element), no flag, a line saying the history shows no failures and the cost rests on the manager's estimate, and the confirmation line.

**7. Decisions (3).** MIX-01: three drive belt failures linked to the belt check, 126 and 105 days apart, average 115.5 days, against the maker's 182; quarterly in the draft; accept it or keep the maker's interval? For the operations manager. CHL-01: the suction pressure limit, the overdue coil cleaning, the missing last-done date of the gasket check and the fan motor's lead time, one question each. PAL-01: add to the register, or is the row an error?

**8. Things to check (6).**
1. SLC-01's failure was a blade guard switch, yet the slicer is not marked safety-critical.
2. WRP-01's film sensor fault links to no maker's task and the wrapper is band B.
3. MIX-01's belt check was last done on 6 October 2026, the day the drive belt snapped: done that day, or the date of the repair?
4. WRP-01's heater element replacement was last done on 14 April 2026, the day a heater element failed: done that day, or the date of the repair? The 40-week interval is counted from it.
5. CHL-01's check says "limit not known": does the manual or the refrigeration contractor give one?
6. The last done dates of 21 and 31 December 2026 are recent: are they dates of work done, and not planned dates?

The closing paragraph (draft for the operations manager, not an engineering sign-off, inspection duties confirmed by the competent person, nothing ordered or changed) was included as written.

## What was observed

- **Every required part was produced,** in the order of the format. Nothing in the inputs triggered a stop: the headers matched, no asset ID was repeated, the history had its period, and the equipment was not unsafe.
- **Same figures as the published example.** Every cost, band, approach, interval, due date, part minimum, shortage, total, measure, flag and decision matched the example's output, including the 115.5-day average, the 33-week and 40-week conversions and the $705 total. The differences in layout: the model wrote dates as year-month-day where the example writes weekday names, wrote "6 h" where the example writes "6.0 h" in the ranked list, put the oven's door seal check before the chiller's gasket check in the monthly group, set out the competent person's section as a nested list, and added a line saying no date was moved off a closed day.
- **The new question about a last done date found two cases, not one.** The review had pointed only to the wrapper's heater elements (last done on the day a heater element failed). The run also found the mixer's belt check, last done on 6 October 2026, the day the drive belt snapped. Both follow the rule as written. The published example now carries both questions; the mixer's was added to it after this run showed the rule applies there.
- **The tightened link rule behaved as intended on these inputs.** The three belt failures linked to the belt check and the heater element failure to the heater element task; the film sensor fault linked to nothing and was raised as a question. The slicer is run to failure, so its tasks are not examined, and nothing in the output links its guard switch failure to the blade task.
- **Where the template left room.** The model raised two questions under "a fact stated loosely" that the example does not carry: the chiller's missing limit, which repeats a question already in decision 2, and whether the recent last done dates are planned rather than done, which nothing in the inputs suggests. The rule names no test for what counts as loose. In decision 2 the model added that a numeric limit would make the chiller condition-based, which is the template's own rule restated, not a new recommendation, but sits close to the line. The template does not fix a date style, so year-month-day and weekday names are both within it.
- **Not tried.** The example has no linked failures closer than a week apart, no monthly task on a day missing from a later month, and no closed days, so the new rules for those cases were not exercised.
- **Acceptance tests.** The invented example happens to exercise the situations in the template's proposed tests 4 (repeated failure), 6 (run-hour interval), 7 (overdue and unrecorded tasks), 8 (check with no limit), 9 (band A part never used), 10 (history row for an unknown asset) and 12 (guard switch on an asset not marked safety-critical), and each behaved as that test expects. It does not exercise tests 2, 3, 5, 11, 13 or 14, so the stop conditions, the declines, the no-history path and a safety-critical asset with a numeric check were not tried. The template still says none of its tests has been run as a set.
- **One run, one model.** This is a single run on an invented example in one product. It shows the template produces a complete, consistent plan on a clean set of inputs. It does not show how it behaves on messy real files, or in other products.
