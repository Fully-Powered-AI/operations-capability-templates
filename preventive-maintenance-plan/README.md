# Preventive maintenance plan

For one site, the facilities or operations manager gets every piece of equipment ranked by failure cost, an approach for each (run to failure, scheduled or condition-based), a dated calendar of tasks from the maker's guidance and the failure history, the spare parts to hold and the downtime measures to track.

*Workflow template · Operations and process improvement · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/preventive-maintenance-plan/)*

## The outcome

Maintenance stops living in one technician's memory and moves onto a calendar everyone can read. Every piece of equipment carries a price on the page: what one breakdown costs in hours stopped and in repair, worked out from your own history where you have it and from your estimate where you do not. The ranking that follows tells you where attention pays.

Each asset gets an approach with a reason. The cheap, unimportant ones are repaired when they fail, and their maker's tasks are listed rather than silently dropped. The rest go on a dated calendar for the year, at the intervals the maker sets. Where your history shows the same part failing again and again, the calendar brings that task forward and puts the change to you as a decision. Nothing is ever pushed out beyond what the maker recommends.

The plan also shows which spare parts to keep on the shelf and which are short, with the cost, and sets out the downtime and repair-time measures to watch each month, with this year's figures as the starting line. Gas, pressure and other safety-critical equipment is set out separately for your competent person, who confirms its intervals and signs for them. The plan is not an engineering sign-off, and the AI assistant orders nothing, books nothing and changes no record.

## Who starts the work, and when

The facilities manager, plant manager or operations manager responsible for the site starts it: when there is no written maintenance plan, once a year to renew it, when equipment is added or replaced, when a site is taken over, and when breakdowns are rising and the work needs to go on a calendar. The maintenance technician who keeps the records usually pulls the files together.

The manager settles the decisions and approves the plan. The competent person confirms the safety-critical section before anyone relies on it.

## What they supply

- **The equipment register.** Each asset, where it is, how many hours a week it runs, whether it is safety-critical, what an hour with it stopped costs you, your estimate of one breakdown, and any reading your team can take with the limit that calls for work.
- **The maker's tasks.** Each task from the manuals, how often (in weeks, months or running hours), when it was last done and where the maker says so.
- **The failure history** for the last year, if you keep one: each breakdown, how long the asset was stopped, the hands-on repair time, the cost and the cause.
- **The spare parts list,** if you have one: what is on the shelf, the supplier's lead time, the cost and how many were used.
- **A few settings,** such as your cost bands, your competent person and who approves purchases.

Each file comes with set column headings. If a heading does not match, the work stops and asks rather than guessing.

## What comes out

One plan in a fixed order. A header with the plan period, the sources, the bands and the counts. Then the equipment ranked by failure cost with the arithmetic shown, the approach for each asset, and the task calendar: weekly and monthly tasks, then every other task dated month by month for the year.

After the calendar: the spare parts with the minimum to hold and what to buy, for your approval; the downtime and repair-time measures with their baseline; the safety-critical section for the competent person; one decision for each flagged asset, such as a task with no record of when it was last done; and the questions worth checking, such as a breakdown that no maker's task covers.

A good plan can be checked against the manuals and the repair log in an afternoon, and the technician recognizes every date on it.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where the person who runs the site owns how reliably it runs.
- [Health, safety and environment](https://fullypowered.ai/functions/health-safety-and-environment/), which names the safety-critical equipment and the competent people who look after it.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where one stopped machine can halt a whole line.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/), where conveyors, forklifts, dock doors and chillers keep goods moving.
- [Hospitality](https://fullypowered.ai/industries/hospitality/), where ovens, refrigeration and air handling have to work every service.
- [Real estate](https://fullypowered.ai/industries/real-estate/), where building plant such as boilers, pumps and air handling serves every tenant.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the equipment has aged and the maintenance routine was never written down.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when new machines and longer hours arrive faster than anyone can plan for them.
- [Acquisitions & integration](https://fullypowered.ai/situations/acquisitions-and-integration/), when a newly acquired site comes with equipment nobody on your side knows yet.

## What has to change for your company

Set your own cost bands, in your currency, and work out what an hour of each asset stopped really costs you, after any backup. Decide which equipment counts as safety-critical on your site and name a competent person for each kind; inspection duties set by law differ by country and by type of equipment, so the competent person confirms which apply. Choose the readings your team can take and the limits that call for work. Decide who records breakdowns and completed tasks, who reviews the measures each month and the targets you want; the plan sets none. Name who approves spare-part purchases. It runs in ChatGPT, Claude, Copilot or Gemini from the files you supply, with no connection to any maintenance system. [Inventory reorder plan](https://fullypowered.ai/workflows/inventory-reorder-plan/) handles stock beyond spare parts, [operations KPI scorecard](https://fullypowered.ai/workflows/operations-kpi-scorecard/) can carry the downtime measures alongside the rest of your numbers, and [workplace risk assessment](https://fullypowered.ai/workflows/workplace-risk-assessment/) covers the hazards to the people who do the maintenance.

## What has been checked

Fully Powered AI wrote this workflow template in its own words, drawing on a published maintenance planning method credited with it. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026, and run on it again the same day after the clarifications that followed review; the record of that latest run is published with the template. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on last year's files for a site your technician knows well, plus hard cases written in advance, each with its expected behavior: a file with a renamed column, a part that keeps failing, a task with no record, a safety-critical asset whose history looks worrying, a breakdown on a machine that is not on the register. The manager checks every cost and date against the manuals and the repair log, and the competent person checks every safety-critical interval, before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Operations KPI scorecard](../operations-kpi-scorecard/)
- [Inventory reorder plan](https://fullypowered.ai/workflows/inventory-reorder-plan/)
- [Workplace risk assessment](../workplace-risk-assessment/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
