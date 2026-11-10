# Workplace risk assessment

For one task or workplace, the site or operations manager gets each hazard, who could be harmed, the controls already in place, a likelihood-and-severity rating before and after, and further controls with an owner and a date, ready for a competent person to review and sign.

*Capability template · Operations and process improvement · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/workplace-risk-assessment/)*

## The outcome

The assessment is written about the work your people actually do, step by step, from what they told you on the walk-round. Each hazard says how someone would get hurt and who that could be, what already protects them, how likely and how bad the harm is today, and what changes once the further controls are in.

The further controls start with the strongest. Removing the hazard or engineering it out comes before a new rule, and a rule comes before protective equipment, so ear plugs and a reminder are never offered as the whole answer without a reason written down. Every control carries an owner and a date. A High hazard whose fix is weeks away gets something to hold the line in the meantime, and a missing owner arrives as a question rather than a guess.

A competent person reviews the draft, settles the open decisions and signs it. The AI assistant signs nothing, assigns nothing, orders nothing and stops no work.

## Who starts the work, and when

The site manager, office manager or operations manager responsible for the task starts it: before a new task begins, when the equipment, materials, people or place change, after a near miss shows the old assessment missed something, and on the review date. They walk the task with the people who do it first, then run the capability on their notes the same day.

The competent person, from inside the business or an outside adviser, reviews and signs before the assessment is shared.

## What they supply

- **A short scope brief.** The task or place, who does the work and how often, who else is around, the assessment date, the competent person and how often to review.
- **The steps of the work,** in the order they are done.
- **Walk-round notes.** What was seen, what goes wrong, what is already in place, any ratings the manager would give, and the fixes already agreed with owners and dates.
- **The incident and near-miss log** for the task, if there is one, with stated column headers.
- **Your rating scale,** if you have one. Otherwise a plain five-by-five scale comes with it.

## What comes out

One draft assessment in a fixed order. A header with the task, the steps, who is involved, the scale and the deadline for High hazards. Then each hazard: the step, how harm happens, who could be harmed, the existing controls, the rating before, the further controls with owner and date, and the rating after, each rating with its reason.

Then the action plan, the decisions the manager and the competent person must make before sign-off, the facts worth checking, the review date, the personal details that were left out, a line on legal duties, and a blank sign-off block for the competent person.

A good draft can be checked against the walk-round notes line by line, and the people who do the task recognize every hazard in it.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where the person who runs the work owns how safely it runs.
- [Health, safety and environment](https://fullypowered.ai/functions/health-safety-and-environment/), which sets the scale, names the competent people and keeps the signed assessments.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where machines, materials and shift patterns change often enough to need the assessment rerun.
- [Construction](https://fullypowered.ai/industries/construction/), where every site and every phase brings its own hazards.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/), where vehicles, forklifts and people share the same yard.
- [Hospitality](https://fullypowered.ai/industries/hospitality/), where kitchens, cellars and busy floors are workplaces too.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where assessments written years ago no longer match the work.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when a new site, a new shift or new equipment arrives before anyone has written it down.

## What has to change for your company

Set your own rating scale or keep the one supplied, and decide how many days a High hazard's fix may take. Name your competent person for each kind of work, and who names owners and dates. Decide how often each assessment is reviewed, where signed assessments are kept and how the people who do the work see theirs. Legal duties for risk assessment differ by country and by sector, so your competent person confirms which apply; the template cites none. Work that needs measuring, such as noise or dust, goes to a specialist. It runs in ChatGPT, Claude, Copilot or Gemini from the notes and records you supply, with no connection to any system. When the steps themselves need writing down first, [SOP from how the work is done](https://fullypowered.ai/capabilities/sop-from-how-the-work-is-done/) does that, and [training needs analysis](https://fullypowered.ai/capabilities/training-needs-analysis/) picks up the training an action calls for.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026 in two runs: the template was revised after an independent review of the first, and the record of the second is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three tasks your competent person already knows well, plus hard cases written in advance, each with its expected behavior: a request for "the whole warehouse", a log with a renamed column, a fix dated after the deadline, a noise hazard controlled by ear plugs alone, a name and an injury in the notes. The competent person checks every rating and every hazard against the walk-round before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete capability template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the capability drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related capabilities

- [Write an SOP from how the work is done](../sop-from-how-the-work-is-done/)
- [Training needs analysis](https://fullypowered.ai/capabilities/training-needs-analysis/)
- [SOP exception capture](../sop-exception-capture/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
