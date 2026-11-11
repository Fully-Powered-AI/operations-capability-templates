# Process map and bottleneck review

Map one process step by step: who does each step, how long work waits and how long it takes, where it is handed over and where it gets sent back. Then find the one step that caps how much gets finished, and what to try there first. The owner decides what changes.

*Capability template · Operations and process improvement · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/process-map-and-bottleneck-review/)*

## The outcome

Everyone has a theory about why the work is slow. This review replaces the theories with one page of figures. Every step of one process is laid out in order, with the role that does it, the hours an item sits waiting before it and the hours of real work it takes. Hand-overs between roles are counted, and every loop where work is sent back to an earlier step is on the map, not hidden.

From those figures the review names the one step that limits how much the process can finish each week: the role with more work arriving than its hours can absorb. It shows the arithmetic, checks it against what the team actually finishes, and says plainly whether the step everyone complains about is that limit or not.

Then it lists what to try first at that step, using the time and people you already have, before anyone talks about hiring or new software. It names the steps to leave alone for now, because making them faster would leave the bottleneck exactly where it is, and it names where the bottleneck is likely to move next. Fix the right step and the whole process moves. That is how a team does far more with the people it already has.

The review proposes. The process owner decides what changes, and nothing is changed until they do.

## Who starts the work, and when

An operations lead or the owner of the process starts it, when people disagree about why a process takes so long, when work is piling up in one place, before adding people or buying software to speed something up, or before deciding which piece of work to improve first.

One run covers one process that repeats, such as turning a request into a quote, onboarding a new customer or approving a supplier bill. Run it again after a change has been tried, with fresh figures, because the bottleneck moves.

## What they supply

- **The process,** in a few lines: its name, its owner, what starts one item and what finishes it, the one number that should rise (quotes sent a week, orders shipped a week) with its current value, how many items arrive a week, and any time target.
- **A step table:** each step in order, the role that does it, the typical hours an item waits before the step and the hours of work it takes, any step it sends work back to and how often, and whether each time was measured or estimated. A spreadsheet export is fine; the template names the column headings it expects.
- **The hours each role gives the process** in a week, everyone in that role together.
- **Short notes from the people who do the work:** when approvals happen, why items come back, what else pulls on their time.

Rough estimates will do to start. The review marks every estimate and says which ones matter most to firm up.

## What comes out

One review, in a fixed order:

1. **The map:** every step with its role, wait, work, hand-overs and send-backs, and which steps each role does.
2. **Where the time goes:** the hours one item spends in the process, how much of that is work and how much is waiting, what send-backs add, and the longest waits.
3. **Load by role:** the hours of work arriving at each role every week against the hours it gives, as a percentage, and how many items it can finish.
4. **The constraint,** with its evidence, the check against what is finished, and a straight answer on the step people complain about.
5. **What to try first** at the constraint, up to three options, each tied to a fact on the map.
6. **What comes after,** if those are not enough, and **the steps to leave alone for now.**
7. **Where the bottleneck goes next, figures to firm up, decisions for the owner and open questions.**

A good review lets someone who was not in the room see why that step is the bottleneck, from figures they can recompute.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where slow processes are noticed, mapped and fixed.
- [Quality management](https://fullypowered.ai/functions/quality-management/), because work sent back to an earlier step is usually the most expensive time on the map.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where proposals, onboarding and approvals queue behind one senior person.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), for quoting, order entry and engineering checks around the line.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/), where bookings and documents pass through several hands before anything moves.
- [Construction](https://fullypowered.ai/industries/construction/), where estimates, submittals and change requests wait on a few busy people.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when demand outruns the team and you need to know where the next hour of capacity counts.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where processes grew by habit and nobody has timed them in years.

## What has to change for your company

Choose the process and name its owner. Agree the one number the process exists to raise; most teams pick items finished a week. Decide how figures are gathered, whether from a ticket system, a job system or a week of people jotting times down, and use your own column headings if they differ. Set the load at which a role counts as nearly full; the template starts at 80 percent. Decide whether the review may propose moving work between roles or only changes within the constraint's own step. Agree where reviews are kept, so the next run starts from the last one. It runs in ChatGPT, Claude, Copilot or Gemini from the tables and notes you supply, with no connection to your systems.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example, in Claude on 10 November 2026, and the record of that run is published with it. The figures and the finding matched the example, and the record lists the places where the instructions left the assistant a choice. Small clarifications made afterward, to settle those places, have not been run again; the record lists them. One run on an invented example is not a test. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a process whose bottleneck you already know, and on one you changed in the past where you know what happened next, then checking every figure by hand. Hard cases belong in the test set: a step everyone blames that is not the limit, a long wait caused by an approval day rather than by lack of time, and estimates that disagree with what is actually finished. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) builds that test set. When the review points at a step worth handing to AI, [Workflow fit check](https://fullypowered.ai/capabilities/workflow-fit-check/) says whether it is ready, and [Write an SOP from how the work is done](https://fullypowered.ai/capabilities/sop-from-how-the-work-is-done/) writes down the changed step once the owner approves it.

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

- [Workflow fit check: is this piece of work ready for AI?](../workflow-fit-check/)
- [Write an SOP from how the work is done](../sop-from-how-the-work-is-done/)
- [SOP exception capture](../sop-exception-capture/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
