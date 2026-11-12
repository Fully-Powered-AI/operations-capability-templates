# Premortem before a decision

Before your team commits to a plan that is hard to undo, such as a move, a launch or a new system, a short workshop pictures it a few months on, already failed. The record ranks the reasons, turns each top risk into a check, a warning sign and an owner, and leaves the go decision with the owner.

*Workflow template · Operations and process improvement · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/premortem-before-a-decision/)*

## The outcome

The owner signs the lease, places the order or sets the launch date knowing what is most likely to sink it, and with something already in place for each of those things. Every top risk has a check to finish before the decision, a sign that would show it coming, the point at which someone acts, and a named person watching.

A room asked to list risks tends to offer what is safe to say. Tell the same room the plan has already failed and ask why, and people name causes: the installer who was late, the phone line nobody ordered. Because each person writes alone first, the warehouse lead's doubt counts as much as the owner's confidence. The record keeps every reason that was written and never says who wrote which.

Nothing is decided for you. The record ends with a blank line for the owner: proceed, proceed with the changes, hold or stop.

## Who starts the work, and when

The owner, or the operations lead on the owner's behalf, starts it a week or two before a decision that would be costly to reverse: a new building, a new system for the whole company, a product launch, entering a new market, a large purchase. It is worth the hour when the plan is big, the date is fixed and the team agreed quickly.

Someone with nothing riding on the answer runs the session. Four to eight people take part, including the people who will do the work. The AI assistant groups what was written and prepares the record; the room rates the risks and agrees the checks; the owner decides.

## What they supply

- **A short brief.** What is being decided, the plan in a few lines, why it is hard to undo, when the decision is due, who decides, and the date the failure is imagined.
- **The reasons people wrote.** One line per reason, written by each person on their own before any discussion, labelled by a participant number, not a name.
- **The groups and ratings the room agreed.** For each group of reasons: how likely, how much harm, and how much warning you would get.
- **The notes on checks.** For each top risk: the check, who owns it and by when, the warning sign, when to act and who watches. Plus any changes to the plan, and the date of the next premortem.

## What comes out

Two short documents, from two runs.

1. **A grouping sheet,** during the session: every reason, unattributed, sorted into proposed groups for the room to merge, split and rate.
2. **The premortem record,** after the session: the failure reasons ranked by a fixed rule; each top risk with its checks, warning sign, trigger point and owner; the changes to the plan the room agreed; which checks are done and which are not before the go decision; the questions only the owner can settle; the date of the next premortem and the events that would bring it forward; and every reason as written.

Where the room left a gap, such as a top risk nobody took, the record says "not assigned" and asks the owner. It never fills the gap itself.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), which usually owns the move, the new system or the changed process.
- [Leadership](https://fullypowered.ai/functions/leadership/), for owners about to make the call that is hardest to take back.
- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/), before a project's point of no return.
- [Professional services](https://fullypowered.ai/industries/professional-services/), before an office move, a new practice system or a new service line.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), before a new line, a plant move or a change of key supplier.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/), before a warehouse move, a new carrier or a new stock system.
- [Construction](https://fullypowered.ai/industries/construction/), before committing to a large job, a new yard or a new site system.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the plans get bigger than the team has made before.
- [New business lines](https://fullypowered.ai/situations/new-business-lines/), before the launch date is announced.
- [Acquisitions & integration](https://fullypowered.ai/situations/acquisitions-and-integration/), before systems, sites or teams are merged.

## What has to change for your company

Decide which decisions get a premortem, for example anything over a set amount or a lease longer than a year. Name who facilitates: someone with no stake in the answer. Keep or change the three rating scales and the rule for what counts as a top risk. Decide how far ahead the failure is imagined; three to twelve months after the go date suits most plans. Decide where the records are kept, so the next premortem starts from the last one. It runs in ChatGPT, Claude, Copilot or Gemini from notes you type or paste; it needs no connection to any system.

## What has been checked

Fully Powered AI wrote this workflow template, drawing on a published open-source method credited in its sources. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026, and the record of that run is published with the template; it lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a decision your team made a year or more ago and knows the outcome of, with the reasons written fresh by people who were there, plus hard cases written in advance: a reason that fits no group, a rating outside the scale, a top risk nobody owns. The owner checks the ranking against the ratings before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets up those cases, and when the plan is a launch, [Launch checklist](https://fullypowered.ai/workflows/launch-checklist/) carries the agreed checks into the dated steps.

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

- [Launch checklist](https://fullypowered.ai/workflow templates/launch-checklist/)
- [Pilot acceptance-test preparation](../pilot-acceptance-test-preparation/)
- [Workflow fit check: is this piece of work ready for AI?](../workflow-fit-check/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
