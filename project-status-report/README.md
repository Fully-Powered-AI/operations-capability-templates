# Project status report

The lead of an internal project gets a status report the sponsor can read in two minutes: each workstream red, amber or green with the reason, what moved, who must clear each blocker, the decisions needed and the dates at risk. No milestone is called done without evidence, and the lead confirms every status.

*Capability template · Operations and process improvement · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/project-status-report/)*

## The outcome

The sponsor opens one page and knows in the first sentence whether the project needs them. The decisions that only they can make come next, each with its deadline and what slips if it waits. Then the dates in danger, then each workstream: its colour, why, what actually finished and what is next. Blockers close the page, each with the person who has to clear it and how long it has been open.

The colours mean something because rules set them, not moods. A milestone past its date without proof that it finished is red, however close it feels. A workstream lead who calls their own work green when the rules say otherwise is shown to the project lead, not quietly believed or quietly overruled. A workstream that stays amber for the same reason two reports running is raised as a question: is it really red now?

The project lead reads the draft, confirms or changes every colour, and decides what goes to the sponsor. The AI assistant sends nothing and marks nothing done.

## Who starts the work, and when

The project lead, or a project coordinator on the lead's behalf, runs it at the end of each reporting period, weekly or monthly, once the workstream leads have sent their updates. It suits any internal project with several workstreams and a sponsor above it: a new system, an office move, a new service, a merger of two teams. The lead confirms the statuses the same day and sends the report on the agreed day.

## What they supply

- **The milestone plan,** exported as a spreadsheet: each milestone with its workstream, owner, due date, what it waits on, and the evidence that will show it is finished.
- **Each workstream lead's update** for the period: what finished and the proof, progress, forecasts for open milestones, blockers with who must clear them, decisions needed, and the colour they would give.
- **The last report,** so colours, blockers and decisions carry over and nothing quietly drops out.
- **The project lead's notes:** decisions the sponsor has made since, and anything else the lead knows.
- **The settings:** project name, sponsor, period, report date, next report date, the end date and any changes to the colour rules.

## What comes out

One page for the sponsor, in a fixed order: the overall colour with a one-sentence headline, decisions needed, dates at risk, workstreams, blockers. Empty sections say so in a word, such as "None this period", so the reader knows nothing was left out.

Beneath it, a short part for the project lead only, removed before sending: milestones claimed as done that the evidence does not support, every colour listed for confirmation with any reason for doubt, and gaps such as a blocker nobody owns. The lead signs off there before the report goes.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/), which runs the plan and answers to the sponsor for it.
- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), which often leads the internal change: the new system, the new site, the new process.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where a firm's internal projects compete with client work for the same people.
- [Engineering firms](https://fullypowered.ai/industries/engineering-firms/), where an internal system change has to land between project deadlines.
- [Construction](https://fullypowered.ai/industries/construction/), for the office-side projects: a new estimating system, a new yard, a new safety programme.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where projects run alongside a full working week and the sponsor has minutes, not hours.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the company starts running several internal projects at once.

## What has to change for your company

Decide who sponsors each project and on which day the report reaches them. Agree the colour rules once and keep them: the defaults are strict on purpose, and you may loosen one, but write it down. Settle how long a stuck blocker can wait before the sponsor hears of it. Make the milestone plan the single source of dates, and give every milestone the evidence that will show it is finished. Agree whether a monthly report replaces the weekly one for the sponsor or sits beside it. It runs in ChatGPT, Claude, Copilot or Gemini from files and notes you supply; it needs no connection to your project software.

## What has been checked

Fully Powered AI wrote this capability template, drawing on two published open-source methods credited in its sources. It was editorially reviewed on 10 November 2026. It was tried on its invented example on 10 November 2026 in Claude, in three runs: the instructions were tightened after the first and again after an independent review of the second, and the record of the third is published with it. That run reached the expected colours, counts, order and open questions for the project lead, and left a few points for judgement: whether a forecast that holds only on a condition is enough, and a one-page limit the example only just meets. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past periods of a project your lead remembers, with hard cases written in advance: a milestone claimed done without proof, a blocker with no owner, a decision past its date, a workstream lead who rates their own work greener than the rules allow. The project lead checks every colour and date against the plan before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) sets up those cases, and [Decision log](https://fullypowered.ai/capabilities/decision-log/) keeps the sponsor's answers once they are given.

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

- [Decision log](https://fullypowered.ai/capabilities/decision-log/)
- [Meeting agenda, notes and follow-ups](https://fullypowered.ai/capabilities/meeting-agenda-notes-and-follow-ups/)
- [Client-status update preparation](https://fullypowered.ai/capabilities/client-status-update-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
