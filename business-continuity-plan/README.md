# Business continuity plan

For an owner or operations manager: the activities the business cannot stop for long, how long each can be down and how much data it can lose, what each depends on, the fallback for each, and named owners, deputies, contacts and a test date, ready for a competent reviewer and the owner's approval.

*Workflow template · Operations and process improvement · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/business-continuity-plan/)*

## The outcome

When the building floods, the order system goes dark or the one person who runs payroll is away, your team opens a plan instead of improvising. It names the work that cannot wait, in the order to bring it back, with how long each piece can be down before the damage is real and how much recent data it can afford to lose.

Under every activity sits what it depends on, the people, the premises, the systems, the suppliers and the equipment, with the fallback for each, how fast that fallback is working and when it was last shown to work. Weak spots surface before a disruption does: a target that is no shorter than the outage the business can bear, a fallback that is slower than the target, backups further apart than the data you can lose, a courier whose only fallback is the same courier, a deputy who is the same person as the lead.

Each weak spot arrives as a plain question for the person who decides. A competent reviewer reads the draft, the owner settles the questions and approves it, and everyone named in it gets a copy. The AI assistant sets no recovery times, chooses no fallbacks, names nobody and contacts nobody.

## Who starts the work, and when

The owner, operations manager or office manager starts it: when the business has no written plan, when the old one no longer matches how the work is done, after a disruption or a near miss, before the busy season, when a key supplier, system, site or person changes, and on the review date. They gather the facts from the people who lead each activity and from the IT provider, then run the workflow template the same day.

The competent reviewer, from inside the business or an outside adviser, reads the draft before the owner approves it.

## What they supply

- **A short scope brief.** The business, the sites covered, who prepares it, who approves it, the reviewer, the plan date, how often to review and the next test date.
- **The activities table.** Each activity the business cannot stop for long, what it produces, what goes wrong as the hours and days pass, the longest outage the business can bear, the target recovery time and how much data it can lose.
- **The dependencies table.** What each activity needs, the fallback, how fast the fallback works, when it was last proven and, for systems, how often the data is backed up.
- **The roles roster.** Who starts and stands down the plan, who leads each recovery, each with a deputy and a work contact.
- **External contacts,** such as the IT provider, the courier, the insurer and the landlord.
- **Notes.** The disruptions that worry you most, what starts the plan, the last test, when contacts were last checked and where the evacuation plan is kept.

## What comes out

One draft plan in a fixed order. A header with the scope, the dates and the counts. The recovery order. Each activity with its times, the margin between target and tolerable outage, and its dependencies, every weak spot flagged where it stands. Then the roles and deputies, the contact list, who starts the plan and on what trigger, the fallbacks the next test must prove, the decisions for the owner, the facts worth checking, the review date, the personal details left out, and blank blocks for the reviewer and the owner.

A good draft can be checked against your tables line by line, and every person named in it recognizes what is expected of them.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where the person who runs the work knows what it depends on.
- [Compliance, risk and privacy](https://fullypowered.ai/functions/compliance-risk-and-privacy/), which keeps the approved plan and asks when it was last tested.
- [IT and systems](https://fullypowered.ai/functions/it-and-systems/), which supplies the backup intervals and proves that a restore works.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where one machine, one site or one supplier can stop every order.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/), where a warehouse and a courier carry every promise to a customer.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where client work, billing and payroll all run on a few systems and a few people.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where an order system, a fulfillment partner and a payment provider each sit on the critical path.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the plan lives in the founder's head and should live on a page.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when new sites, suppliers and systems arrive faster than anyone writes down what happens if one fails.

## What has to change for your company

List the activities that count for your business and who leads each. Decide whether times are counted in calendar hours or working days, how old a proof may be before a fallback counts as unproven, and whether a target must sit a set margin inside the tolerable outage. Name your competent reviewer and who approves. Decide where the approved plan lives, how the people in it get their copy, and where the personal contact sheet is kept apart from it. Legal, regulatory and insurance duties for continuity planning differ by country, sector and policy, so your reviewer and advisers confirm which apply; the template cites none. The evacuation plan stays a separate document. It runs in ChatGPT, Claude, Copilot or Gemini from the tables and notes you supply, with no connection to any system. When a disruption has already happened, [incident investigation and corrective actions](https://fullypowered.ai/workflows/incident-investigation-and-corrective-actions/) works out what went wrong; for hazards to people at work, use [workplace risk assessment](https://fullypowered.ai/workflows/workplace-risk-assessment/).

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026 in one run, by a model that had not written it; the record of that run is published with it. After two independent reviews, the example's output was corrected and a few clarifications were made to the template; the record lists them, and the example has not been run again since. That run did not reach the stop conditions. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on your own tables with hard cases written in advance, each with its expected behavior: a target equal to the tolerable outage, a fallback slower than the target, backups further apart than the data you can lose, a supplier whose only fallback is itself, a renamed column, a personal mobile number in the notes. The reviewer checks every time comparison against the tables before anyone relies on the plan. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Workplace risk assessment](../workplace-risk-assessment/)
- [Incident investigation and corrective actions](../incident-investigation-and-corrective-actions/)
- [Premortem before a decision](../premortem-before-a-decision/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
