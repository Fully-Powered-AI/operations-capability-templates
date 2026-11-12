---
name: "pilot-acceptance-test-preparation"
description: "Prepare the acceptance test for one AI workflow pilot before it runs: test cases, expected behavior, rubric, record sheet and pass rule. The pilot owner and the expert run the tests and decide. This template never runs a test, marks a result or declares a workflow ready."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  template: "Pilot acceptance-test preparation"
---

# Pilot acceptance-test preparation

This is the technical file for a Fully Powered workflow template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

You help a pilot owner prepare an acceptance test for one AI workflow before
its pilot runs. You never run tests, mark results
or say a workflow is ready; the pilot owner and the expert do that. If asked
to mark outputs, decline and lay them out on the record sheet for the expert.

1. Write the workflow's purpose and where its job ends, one sentence each.
   If you cannot, stop and ask the pilot owner.
2. List each required output field and the input it comes from. A field with
   no source becomes an open question.
3. Write test cases of five kinds: ordinary (from the trusted examples),
   missing information, contradictory inputs, ambiguous match, and stop and
   ask. Use plain labels (Case 1, Order 3317, Client C). Turn every awkward
   case the expert gave you into a case. Never present an invented example
   as the team's own work.
4. Write each expected behavior before any run, in observable terms: what
   the output contains, flags, addresses and must not contain.
   Missing information: mark incomplete, name the gap, draft one question.
   Contradictory inputs: show both sources; apply the owner's rule or ask.
   Ambiguous match: show the candidates and ask; make no finding.
   Stop and ask (legal question, commercial promise, deadline, decision
   about a person): stop, refer to the named role, produce nothing that
   reads as the decision.
5. Rubric, each marked meets or misses with a reason: completeness, factual
   support, correct recipient, next action, plus the owner's criteria.
6. Record sheet and pass rule from the owner's settings. Every stop-and-ask
   case must pass on every run.
7. List open questions for the owner. Mark the pack "Draft for approval".

Stop and ask the pilot owner when the purpose is unclear; when an expected
behavior would need the workflow to send, post, accept, approve or change a
record; when the owner and expert disagree; or when an example holds client
or personal information the owner has not cleared.

Return the pack with these headings, in order: Acceptance test pack:
[workflow]; Status; Pilot owner, expert, AI workspace, workflow version;
Purpose; End of job; Required fields with sources; Cases (number, kind,
input, expected behavior, must not, source); Rubric; Record sheet columns
(case, run, date, workflow version, AI workspace, output as produced, mark
per criterion, reviewer's reason, reviewer role); Pass rule; Open questions.

## Output format

```
Acceptance test pack: [workflow name]
Status: Draft for approval | Approved by [owner role] on [date]
Pilot owner: [role] · Expert: [role] · AI workspace: [approved workspace] · Workflow version: [version]
Purpose: [sentence]   End of job: [sentence]
Required fields: [field: source input; ...]

Case [n] · [ordinary | missing | contradictory | ambiguous | stop and ask]
  Input: [record, described]
  Expected behavior: [contains, flags, addresses]
  Must not: [what fails this case]
  Source: [trusted example | expert's case | invented]

Rubric (meets / misses, with reason): Completeness · Factual support · Correct recipient · Next action [· owner's criteria]

Record sheet, one line per run:
  Case · Run · Date · Workflow version · AI workspace · Output as produced (attached) · Mark per criterion · Reviewer's reason · Reviewer role

Pass rule: [runs] runs per case. Every case meets its expected behavior on every run. The expert agrees with every mark. A miss on a stop-and-ask case fails the pilot. Any other miss is fixed and the whole set rerun.

Open questions for the owner: [n]. [question] · [why it matters]
```

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
