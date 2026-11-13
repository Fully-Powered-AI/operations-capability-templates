# Client service level report

At the end of each reporting period, the service delivery manager gets the report a client contract calls for: every service level measured from your own records, each miss explained by those records, the credits the contract states listed for a person to confirm, and the open questions. Nothing is sent.

*Workflow template · Operations and process improvement · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/client-service-level-report/)*

## The outcome

The report the contract promises arrives on time and stands up to the client's own checking. Every service level in the contract appears once, measured from the business's own tickets, outage log and delivery records, with the arithmetic shown, so anyone on either side can follow a figure back to the rows behind it. A result is never rounded into a pass.

A miss comes with its explanation already attached: the records that missed, how late each one was and the cause your own team noted at the time. Where no cause was noted, the report says so and asks. Exclusions your team claimed, such as time spent waiting on the client, are shown openly with what each one changes, so the service delivery manager confirms them before the client sees the figures.

Credits are listed exactly as the contract states them, worked out only where the contract gives a plain percentage of a named fee or a fixed amount, and quoted word for word where it does not. Every credit waits for the service delivery manager and finance to confirm. Each miss sits beside the corrective actions your team agreed, and a miss with nothing open against it becomes a question. Your people decide what the contract means, which exclusions stand, which credits apply and what the client receives.

## Who starts the work, and when

The service delivery manager, or the account manager or a service coordinator working for them, runs it at the end of each reporting period the contract sets, usually monthly, once the period's records are closed and exported. A first run shows the misses and the questions. A second run, after the service delivery manager has answered them, gives the report that is approved, kept and passed to the account manager to send.

## What they supply

- **The service level schedule:** every service level in the contract, set out once by the service delivery manager and checked against the contract: what it measures, its target, the exclusions the contract allows, the credit it carries and where it sits in the contract.
- **The period's service records:** tickets, incidents, deliveries or reports exported from your own systems, each with its due time, when it was done and any cause or exclusion your team noted.
- **The outage log,** for any availability service level.
- **Figures measured elsewhere,** such as a satisfaction score, with their source.
- **The corrective action list** for the contract, and last period's results.
- **The settings:** the period, when the records were exported, the time zone, the fees a credit is taken of, and any cap on credits.

## What comes out

One draft report in a fixed order: the count of service levels met, missed and not measured; each service level with its result, its target, its status and last period's result; the working behind every figure; each miss with the records that caused it and their cause notes; every exclusion claimed and what it changes; the credits that may apply, totalled and checked against any cap; the corrective actions for each miss, with overdue ones marked; the records left out and why; and numbered questions for the service delivery manager.

When an export's columns do not match, or the records were exported before the period ended, the work stops and asks. It never reads service levels out of the contract on its own, never says whether a credit is owed and sends nothing to the client.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), which runs the service the contract measures and reports on it every period.
- [Customer success and account management](https://fullypowered.ai/functions/customer-success-and-account-management/), where the account manager decides what the client receives and keeps the relationship sound through a bad month.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where managed services and outsourced work are sold on response times, turnaround and availability written into the contract.
- [Software and technology](https://fullypowered.ai/industries/software-technology/), where hosted platforms and support desks report uptime and resolution times to every client that has a service level agreement.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/), where warehousing and transport contracts promise on-time dispatch and delivery and carry credits when they slip.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where several client contracts each set their own service levels and reporting dates.
- [Growth and scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the number of contracts outgrows the spreadsheet one person rebuilds every month.

## What has to change for your company

Set out a service level schedule for each contract once, and have whoever owns the contract commercially check it against the contract; update it whenever the contract changes. Map your export columns to the ones the template expects. Name who confirms exclusions, who confirms credits with the service delivery manager, and who approves and sends the report. Give the fees each credit is taken of. Decide whether the client receives the full report or a version of it. It runs in ChatGPT, Claude, Copilot or Gemini, from the files you supply; it needs no access to any system.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 11 November 2026. It was tried on its invented example on 11 November 2026 in one run, in Claude; the record of the run is published with it. After an earlier run, the instructions, the output format and the example were revised, and the published record is of the run on the revised text. That run was made by the model that made the revisions, so it is not independent. A few small clauses were added to the instructions after that run, and the amended text has not been run. It has not yet been tested in a client environment.

Testing in your environment means running it on two or three past periods your service delivery manager already reported, with hard cases written in advance: a result just under its target that rounds to it, an exclusion the contract does not allow, an outage that starts the month before, a record still open past its due time, a credit written as a sliding scale. The service delivery manager checks every figure against its working before anyone relies on the report. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 11 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 11 November 2026. The record is in [TRIAL.md](TRIAL.md).
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
- [Support service level definition](https://fullypowered.ai/workflows/support-service-level-definition/)
- [Client-status update preparation](https://fullypowered.ai/workflows/client-status-update-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
