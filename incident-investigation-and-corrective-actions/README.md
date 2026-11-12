# Incident investigation and corrective actions

After an injury, near miss or property damage, the site, operations or safety manager gets the investigation written up from the evidence: a timeline, the immediate and underlying causes, actions with owners and dates, and a register that follows each action until a check shows it worked.

*Workflow template · Operations and process improvement · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/incident-investigation-and-corrective-actions/)*

## The outcome

Every incident gets the same careful record, however busy the week. The facts sit in time order, each one tied to a statement, a photo or a record. The causes go past "someone made a mistake" to what the organisation controls: a layout, a procedure, a check nobody owns. Every action is linked to the cause it deals with and carries an owner, a date and a check that will show whether it worked. Fix the system rather than the person, and the same event becomes much harder to repeat.

The register stays open until each action has passed its check. Finishing the work is not the same as closing the action; an action closes when the check result is in.

A qualified person leads the investigation and decides the causes, the actions and anything that has to be reported. The AI assistant prepares the record. It reports nothing, assigns nothing and blames no one.

## Who starts the work, and when

The site, operations or safety manager, or whoever the company names to lead investigations, starts it once the scene is safe and the first statements, photos and records are in hand, usually within a day or two. They run it again after the team has met to agree actions, and then on a set rhythm, weekly for example, to bring the register up to date until every action is closed.

## What they supply

- **Their incident notes:** what happened, when, where, the outcome, and what was done straight away.
- **The evidence list:** each statement, photo, record or document with a short summary. A spreadsheet export works.
- **The procedures, permits or plans** that applied to the task, as evidence items.
- **Earlier incidents** involving that equipment, task or area, from the incident log.
- **The actions the team proposed,** with owners, dates and checks.
- **The company's written reporting rules:** what must be reported, by whom, to whom and by when.
- **For each update:** the register, with each action's status and any check results.

## What comes out

One investigation record: what happened, the people by label, the timeline, the evidence log, the causes in three layers, earlier incidents, the action register, the stopgap controls, the reporting duties to confirm, and numbered questions for the investigation lead. Where the evidence is thin, the record says so and asks; it never fills the gap with a guess.

The people involved appear as Person A, Person B. If names were supplied, the key comes separately for the lead to keep apart from the record. Medical details beyond what the investigation needs are left out.

Each update shows what is open, overdue, done and waiting for its check, verified, or reopened because its check failed.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where the procedures, layouts and checks that most incidents trace back to are owned.
- [Health, safety and environment](https://fullypowered.ai/functions/health-safety-and-environment/), where the qualified person leads the investigation and owns the reporting duties.
- [Quality management](https://fullypowered.ai/functions/quality-management/), which runs the same loop of cause, action and checked closure for every nonconformity.
- [Construction](https://fullypowered.ai/industries/construction/), where sites change daily and a near miss is the cheapest warning there is.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where machines, guards and shift handovers produce most incidents.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/), where forklifts, racking and people on foot share the same floor.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where incidents are investigated by whoever is free and actions drift once the paperwork is filed.

## What has to change for your company

Name who leads investigations and who your qualified safety person is. Write your reporting rules down with that person, so the record can point to them: duties differ by country, region and sector, and the template never assumes one. Set the order of controls you use, your action statuses, and how far ahead the register warns about checks falling due. Decide where records and label keys are kept and who may see each. Agree what may be shared beyond the investigation team, and how. It runs in ChatGPT, Claude, Copilot or Gemini, from the files and notes you supply; it needs no access to any system.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example on 10 November 2026 in two runs: the first, by an assistant that had not written it, showed where the instructions left room to guess; the instructions and the example were revised after an independent review, and the record of the second run, made on the revised instructions, is published with it. After a second independent review, one update run on the same register was made by the assistant that applied that review's fixes, not by an independent one, and its record is published too, with the points it left to judgement. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past incidents your qualified person knows well, plus hard cases written in advance, each with its expected behaviour: two accounts that disagree, a cause the evidence does not support, an analysis that wants to stop at "he ignored the rules", an action marked done with no check, a renamed column. The qualified person checks every cause against the evidence before anyone relies on the record. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Write an SOP from how the work is done](../sop-from-how-the-work-is-done/)
- [Training needs analysis](https://fullypowered.ai/workflow templates/training-needs-analysis/)
- [SOP exception capture](../sop-exception-capture/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
