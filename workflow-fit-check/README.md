# Workflow fit check: is this piece of work ready for AI?

Before you build anything, run one piece of work through six checks and get a straight answer on one short page: build it, build one part, do something simpler first, not yet, or leave it with your people. The owner decides what gets built first, with the reasons in front of them.

*Workflow template · Operations and process improvement · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/workflow-fit-check/)*

## The outcome

You stop guessing which piece of work to hand to AI first. Each candidate gets the same six checks and one short page that says what to do, why, and what would change the answer. The work that is ready goes to the front of the line. The work that only needs a setting switched on or a simple register gets that, often within the week, at no cost to build.

Building the right thing first is the fastest way to 10X what your team can do. A fit check that says “do not build this” is doing its job: it saves the weeks you would have spent on a workflow nobody could check, and it usually finds the one step inside the request that is worth building.

The answer is advice. The owner decides.

## Who starts the work, and when

An owner or operations lead starts it, when someone says “can we get AI to do this?” and before any time or money goes into building. Run it again when the facts change: new software, a new plan for your AI product, or a register that now exists.

The person who does the work today supplies the detail. The owner reads the page and decides what happens next.

## What they supply

- **The request,** in the words of whoever asked.
- **How the work is done today.** Notes from a short walkthrough with the person who does it: who does it and who approves, what starts it, what a finished result looks like, where each input lives, the awkward cases and what is done with each, how they would know a result was right, how often and how long.
- **Two or three past cases,** including one that went wrong, with people and companies named by role or label (the owner, Sub A).
- **What you run on.** The software the work touches, your AI product and plan, who owns the workspace, and any rule about what data may go into the AI product and who approves it.

Anything you do not know, you say so. The check marks each gap “Not known” and turns the ones that matter into questions for a named role.

## What comes out

One short page per piece of work, two to three printed pages, held to five actions and eight open questions:

1.  **The six checks,** each marked clear, not clear or fails, with the words from your notes that show why: the people; start and finish; inputs; exceptions; examples and a way to judge; platform and permission.
2.  **The six reasons to say no,** each shown as applying or not: your software already does it; it is a list, a register, a reminder or a fixed rule; checking would take as long as doing; nobody here can judge it; it needs more than a person-run workflow; the data would pass through a party nobody has approved.
3.  **The verdict,** one of five: build it, build one part, do something simpler first, not yet, or leave it with your people. A fixed order decides when more than one fits, and the page says which line decided.
4.  **What to do,** in order, each line with the role that does it, starting with anything you can do without building.
5.  **The part worth a workflow,** if there is one, with what it would never do.
6.  **What it is worth,** using only the figures you supplied, and **what would change the verdict.**
7.  **Open questions,** each for a named role, and a blank line for the owner’s decision.

A good page lets a reader who was not in the room see why the answer is the answer.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

The six checks are the same in any industry. These are the places the requests pile up fastest:

- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where the list of “could AI do this?” requests lands.
- [Leadership](https://fullypowered.ai/functions/leadership/), for owners choosing where the first build goes.
- [Construction](https://fullypowered.ai/industries/construction/), where paperwork, schedules and subcontractors generate requests faster than anyone can sort them.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where much of the work is judgment and the fit check separates the part that repeats.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where existing systems often already hold the feature being asked for.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/), where documents arrive in every form and the question is which ones a person can check quickly.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the work is outgrowing the people and you need to pick what to build first.

## What has to change for your company

Name who decides what gets built. Say which AI product and plan you are on, and who may add a shared set of instructions or a connection. Write down your rule for data: what may be pasted into an AI product, and who approves it. Set your own bar for “quick to check”: the template suggests a person should confirm a result in well under half the time it takes to do the work. Decide where the finished pages are kept, so the next request is judged against the last ones.

## What has been checked

Fully Powered AI wrote this workflow template from its own method for qualifying a piece of work before building. It was editorially reviewed on 9 November 2026. It was tried on its invented example, in Claude on 9 November 2026: one recorded run, after two earlier runs the same day on earlier wording. The record is published with it and lists the small edits made to the instructions since. Runs on one invented example are not a test. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three requests whose answer you already know, including one you built and regret, and seeing whether the page reaches the same answer for the same reasons. When a piece of work passes, [SOP exception capture](https://fullypowered.ai/workflows/sop-exception-capture/) records how your best person handles its awkward cases, and [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets up the cases that prove the build.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 9 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 9 November 2026. The record is in [TRIAL.md](TRIAL.md).
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

- [SOP exception capture](../sop-exception-capture/)
- [Pilot acceptance-test preparation](../pilot-acceptance-test-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
