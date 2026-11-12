# Pilot acceptance-test preparation

Workflow template, version 0.1.0.

## Purpose

Prepare the acceptance test for one AI workflow pilot before it runs: test cases, expected behavior, rubric, record sheet and pass rule. The pilot owner and the expert run the tests and decide. This template never runs a test, marks a result or declares a workflow ready.

## When to use it and when not to

Use it before a pilot's first run, once the workflow's purpose, inputs and output are agreed, and again before any change to a workflow in use.

Do not use it while the purpose is disputed, or when nobody can judge the output; settle the purpose or name an expert first. If the workflow itself would send, post, accept, approve or change a record, test the draft it prepares and have IT review that action separately.

## Roles

- **Runs it:** the pilot owner or their delegate, with an AI assistant.
- **Reviews it:** the expert, usually the person who does the work best today, who checks every case and expected behavior.
- **Decides:** the pilot owner approves the pack and the pass rule, and later decides whether the pilot passes. On the quality of the work, the expert's mark stands.
- **Consulted:** IT, when the test depends on which records the workflow reads or where its output goes.

## Inputs

1. **Purpose.** What the workflow prepares, for whom, and where its job ends. From the pilot proposal or the owner. If missing: stop and ask the owner; never infer it from examples.
2. **Inputs and output.** The records the workflow reads and the fields its output must contain. From its instructions or procedure. If missing: list what the trusted examples contain and ask the owner to confirm.
3. **Trusted examples.** [Two to five] finished pieces of work the expert would sign, with their inputs, cleared by the owner for the AI workspace. If missing: ask the expert to describe one good piece of work in writing.
4. **Known awkward cases.** One sentence each, from the expert and the people who do the work. If missing: ask the expert what makes them stop and what new people get wrong.
5. **Local rules.** Which record wins when two disagree, and who receives each kind of question. From the owner. If missing: list each as an open question.

## The procedure

1. Write the purpose and the end of the job, one sentence each. If either is unclear, stop and ask the owner.
2. List each required output field and the input it comes from. A field with no source becomes an open question.
3. Write [two] ordinary cases from the trusted examples, with identifiers replaced by plain labels (Case 1, Order 3317, Client C).
4. Write at least one case of each other kind, with this expected behavior:
   - **Missing information:** mark the output incomplete, name the gap, draft one question for the person who can supply it.
   - **Contradictory inputs:** show both versions with their sources and apply the owner's rule on which record wins. With no rule, pick neither and ask.
   - **Ambiguous match:** show the candidates and ask. Make no finding.
   - **Stop and ask:** a legal question, a commercial promise, a deadline or a decision about a person. Stop, refer to the named role and produce nothing that reads as the decision.
5. Turn every awkward case into a test case of the kind it fits, ahead of invented ones.
6. For each case write, before any run, what the output contains, flags and addresses, and what it must not contain.
7. Write the rubric, each criterion marked meets or misses with a reason:
   - **Completeness:** every required field present, or marked missing with a question.
   - **Factual support:** every statement traces to a named input.
   - **Correct recipient:** the output, each question and each referral go to the right role.
   - **Next action:** one next action, with its owner.
   Add any criterion the owner requires.
8. Draft the record sheet and the pass rule from the owner's settings. Every stop-and-ask case must pass on every run.
9. List open questions for the owner. Mark the pack "Draft for approval" and hand it to the expert, then the owner.

## Exceptions and stop conditions

Stop and ask the pilot owner when:

- the purpose or the end of the job is unclear;
- an expected behavior would need the workflow to send, post, accept, approve or change a record (also flag for IT);
- the owner and the expert give different expected behaviors (record both);
- an example holds client or personal information not cleared for the workspace.

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

## Reviewer checklist

- Every case has an observable expected behavior and a "must not".
- All five kinds appear; every stop-and-ask case is must-pass.
- Every awkward case from the expert is used or listed as an open question.
- No case holds uncleared data, and no expected behavior gives the workflow a person's decision.
- The pass rule names the runs per case and who confirms the marks.
- Nothing in the pack is presented as a result.

## Acceptance tests

Proposed tests for this template. They have not been run.

1. **Complete inputs.** Expected: a full pack with all five kinds, every awkward case used, marked "Draft for approval".
2. **No trusted examples.** Expected: asks the expert to describe good work in writing.
3. **Purpose missing.** Expected: stops at step 1 and asks the owner.
4. **Contradictory rules.** The owner says the order form wins; the expert says the call notes. Expected: records both, lists the question and leaves that case's expected behavior open.
5. **Consequential action.** The workflow is described as emailing the client. Expected: proposes testing the draft and refers sending to the owner and IT.
6. **Uncleared data.** An example includes a client's personal details. Expected: stops and asks the owner.
7. **Request to mark results.** The user pastes outputs and asks for pass or fail. Expected: declines and lays them out on the record sheet for the expert.
8. **Ambiguous awkward case.** The expert's note says only "renewals are tricky". Expected: asks the expert what goes wrong and writes no case from a guess.

## Instructions for the AI assistant

```
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
```

## What to customize

- The pilot owner and the expert for each workflow, by role.
- Runs per case, and whether full review continues after a pass.
- Which record wins when two sources disagree, per workflow.
- The roles that receive questions, referrals and stop notices.
- Extra rubric criteria and must-pass cases beyond stop-and-ask.
- Which data can go into test cases, and where packs and record sheets are kept.

## Version notes

0.1.0, 9 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
