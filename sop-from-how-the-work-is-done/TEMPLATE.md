# Write an SOP from how the work is done

Capability template 0.1.0 · Operations and process improvement · Fully Powered AI

## Purpose

Write a draft standard operating procedure for one piece of work, from an account of how it is done today: the steps in order, the role that does each, how that person knows a step is done, where the work branches, the exceptions, the conditions that stop it and the records kept. Every line traces to what was said or written; every gap becomes a question for the owner. The assistant drafts; the owner approves, and nothing is in use until they do.

## When to use it and when not to

Use it when a procedure exists only as habit, before the person who knows it goes on leave or changes role, before the work goes to a new colleague or an AI assistant, or when a written procedure no longer matches what people do.

Do not use it:

- for several procedures at once. Write one per run, starting with the owner's choice;
- to redesign the work. It records today's practice; ideas for improvement are listed as questions, never written into the steps;
- when a written procedure already exists and the need is the awkward cases. That is the companion capability, SOP exception capture, which works from real cases and a conversation with the expert;
- to write rules for a reserved judgment such as legal advice, a clinical decision or a hiring decision. The procedure records who makes that judgment and when the work goes to them, nothing more. Employment documents and contract wording are out of scope.

## Roles

- **Preparer** (runs it): the operations lead, a team lead or the person who does the work, with an AI assistant.
- **Doer** (source and first reader): the person who does the work today. Gives the walkthrough and checks the draft against what they said.
- **Procedure owner** (decides): settles every open question, approves the procedure and decides where it is kept.
- **Others named in the work** (consulted): roles that approve, receive or hand over something. Their accounts are extra sources, never overrides.

## Inputs

1. **A walkthrough by the doer** of one real case from start to finish: a transcript, notes from a recording or their own written account. Number its lines or paragraphs so each step can cite them. Without a walkthrough, prepare the walkthrough questions (step 2) and stop.
2. **Anything already written** (optional): an old procedure, a checklist, a form, messages about the work. If none, say so in the header.
3. **Other accounts** (optional): notes from a colleague, an approver or the next role in line.
4. **The request**: the procedure's name, the owner's role, who does the work, who is preparing the draft and the date. With no named owner, stop.
5. **Local settings**: limits already set (approval amounts, deadlines, tolerances), the review interval, the names of roles and systems, and the redaction rule for customer and staff detail (for example "roles only, no customer names"). A limit that is not supplied is never guessed.

## The procedure

1. **Confirm the run.** One procedure, one named owner, one doer. If the material covers more than one procedure, list them and ask the preparer which to write first.
2. **Check the walkthrough.** If there is none, return these questions for the doer and stop:
   - What starts this work, and how do you find out?
   - Take me through the last one you did, from the start. What did you do first, and where?
   - At each point, how do you know that part is done?
   - Where do you have to choose between two ways forward, and what decides it?
   - What goes wrong most often, and what do you do then?
   - When do you stop and ask someone, and whom?
   - What do you write down or save, and where?
   - What tells you the whole thing is finished?
3. **Apply the redaction rule.** Refer to people by role. If the material holds customer or staff detail the rule excludes, stop and ask for a redacted version. If no rule is supplied, refer to people by role, go on, and ask for the rule in the closing list.
4. **Settle the boundary before any step.** From the material, write what starts the work, the observable state that ends it, what is not covered and how often it runs. If the start or the end cannot be found, ask the preparer one question at a time until both are settled.
5. **List the roles.** Every role the material names, with what it does in this procedure. "The team" is not a role, and neither is a department such as "the warehouse": write the role as `[To confirm]` and add an open question asking which role.
6. **Write the steps** in the order the doer described.
   - One action per step, opening with a verb, with exactly one role. Work another role does is its own step. An approval or answer given at a stop condition is not a step; it stays in the stop condition.
   - "How" stays close to the doer's words and names the system or document used.
   - "Done when" is something another person can see or check. Take it from the material. It may restate the visible result the step itself names in the doer's words (a step that closes the ticket is done when the ticket is closed). It never adds a sign the material does not give. If there is none, write `[To confirm]` and add an open question; steps with the same gap may share one question.
   - A choice is its own step, written as a yes-or-no question with a destination for each answer. A look-up whose only purpose is to answer that choice is not a separate step: it goes in the decision's "How to tell" line.
   - A deadline the material gives goes in the step it governs, with its source.
   - Mark a step "Cannot be undone" only when it pays or refunds money, files or submits something outside the company, deletes a record, or the doer says it cannot be reversed. Routine messages to a customer or a colleague are not marked. Add "Approved by" only when the material names an approver.
   - Cite the source line for every step.
7. **Write the exceptions.** For each thing the material says can go wrong: the step, the condition, what is done and by whom. Then name the steps for which no exception was described and ask about them.
8. **Write the stop conditions.** Each point where the doer stops and asks: where it applies (a step, before step 1, or at any step), the observable condition, the role asked, and what must not happen until that role answers. Include approval limits. A deadline is a stop condition only when the material names someone to ask as it nears or passes; otherwise it stays in its step, and what is done when it is missed becomes an open question. If the material describes no stop condition, say so and add an open question; never leave the section out.
9. **Write the records.** What is recorded, where and by whom.
10. **Collect the open questions.** Use `[To confirm]` in the draft wherever a fact is missing, and list each as a question with one of six marks:
    - **Missing**: the material does not say.
    - **Sources disagree**: two accounts, or an account and a set limit, differ. Quote both. Do not choose.
    - **Unclear wording**: the doer was vague ("usually", "a big order", "I play it by ear"). Quote the words.
    - **Limit to set**: a number is needed and none was given.
    - **Reserved decision**: a judgment that belongs to a qualified person.
    - **Suggestion**: an improvement someone raised. It stays out of the steps.
11. **Check the draft.** Every step has one role, or a `[To confirm]` for the role, and a check or a `[To confirm]`. Every decision has two destinations that exist. Every `[To confirm]` has a question. More than 20 steps: propose a split to the preparer and write the first part only.
12. **Doer's read.** The doer reads the draft against what they said, and answers the questions marked Missing or Unclear wording that are about their own practice. Their corrections and answers replace the original wording and are cited as a new source. Any answer that sets or changes a limit, and every question marked Sources disagree, Limit to set, Reserved decision or Suggestion, stays for the owner.
13. **Send to the owner** as a Draft. The owner answers each question still open and approves or amends.
14. **Record approval**: owner's role, date, version 1, next review date. Only then does `[procedure library role]` file the procedure where the team finds it.

## Exceptions and stop conditions

- **No named owner.** Stop and ask the requester to name one.
- **No walkthrough, only an old document.** Do not present the old document as today's practice. Return the walkthrough questions.
- **Customer or staff detail beyond the redaction rule.** Stop; return the material to the preparer.
- **No redaction rule supplied.** Refer to people by role, go on, and ask for the rule in the closing list.
- **The doer's practice conflicts with a written policy or a set limit.** Write neither as the rule. Mark the step `[To confirm]`, add a "Sources disagree" question quoting both, and tell the preparer at the top of the reply. Where the dispute is over a whole step or exception, not a figure, the doer's account stays in the draft, marked.
- **A step shares or bypasses a sign-in, or has one person approve their own request.** Record what was said, mark it for the owner and `[compliance role]`, and write no instruction that repeats it. The procedure names the system a step uses; it never holds a password or a login code.
- **A step turns on a reserved judgment.** Record who decides and when the work goes to them. Write no rule for the judgment.
- **Asked to fill a gap, pick between two accounts, or mark the draft approved.** Decline; these are the owner's.
- **Asked to publish the procedure, send it to the team or change a system.** Decline; the preparer does that after the owner's approval.

## Output format

```
STANDARD OPERATING PROCEDURE · [Procedure name]
Status: Draft for the owner's approval. Not in use until approved.
Owner: [role]   Prepared by: [role]   Date: [D Month YYYY]
Written from: [each source, its date and its letter: W walkthrough,
  N note, D document, L request and local settings]
Version: Draft [n]   Next review: [interval or date, or To confirm]
Summary: [n] steps, [n] exceptions, [n] stop conditions, [n] open questions

1. Purpose
[One or two sentences: what the procedure achieves and for whom.]

2. Scope
Starts when: [trigger] ([source])
Ends when: [observable end state] ([source])
Not covered: [exclusions, or To confirm]
How often: [frequency, or To confirm]

3. Roles
[Role]: [what it does in this procedure] ([source])

4. What you need before starting
[Information, documents, templates and named systems]

5. Steps
[n]. [Verb and object]. [Role, or To confirm]. [How, in the doer's words.]
     [Cannot be undone. Approved by: [role]. Only where they apply.]
     Done when: [observable check, or To confirm]. Source: [lines].
[n]. DECISION: [yes-or-no question] [Role].
     How to tell: [where the doer looks, in their words, or To confirm].
     If yes: go to step [n]. If no: [go to step n | follow E[n] | stop, S[n]].
     Source: [lines].

6. Exceptions
E[n]. At step [n], when [condition]: [what is done]. [Role]. Source: [lines].
No exception was described for steps [n, n]. See Q[n].

7. Stop conditions
S[n]. Stop [at step n | before step 1 | at any step] when [observable
      condition]. Ask [role].
      Do not [action] until they answer. Source: [lines].

8. Records
[What is recorded], [where]. [Role] ([source])

9. Open questions for the owner
Q[n]. [Question, quoting the words at issue]
      Marked: [Missing | Sources disagree | Unclear wording | Limit to set |
      Reserved decision | Suggestion]. Affects [steps, E or S].
      Owner's answer: [blank until settled]

10. Revision history
Draft [n] · [date] · [prepared by] · [what changed]
Approval: [owner role]   Date: [blank until approved]

Status: Draft for the owner's approval. Nothing has been published, sent
or changed in any system.
```

## Reviewer checklist

1. Every step is something the doer said or wrote, in their order, with its source. (Doer)
2. Every step names exactly one real role, never a team or a department, or is marked for the owner. (Doer)
3. Every "Done when" can be seen or checked by someone else, and says nothing the doer did not say. (Preparer)
4. Every decision has a destination for yes and for no, and both exist. (Preparer)
5. Exceptions and stop conditions are both present, and each stop names a role and what waits. (Owner)
6. Every `[To confirm]` has an open question, and no disagreement has been settled by the preparer or the assistant. (Owner)
7. Every limit and deadline is one that was supplied, or is marked for the owner; every step marked "Cannot be undone" is one that pays, files outside the company or deletes. (Owner)
8. No customer or staff names remain, and no sign-in detail appears. (Preparer)
9. The status says Draft until the owner's approval is recorded. (Owner)

## Acceptance tests

Proposed tests. They have not been run.

1. **Complete walkthrough.** A numbered walkthrough with a clear start and end, plus settings. Expected: all ten sections; every step with one role, a source and a check or `[To confirm]`.
2. **No walkthrough.** Only an old checklist is supplied. Expected: the walkthrough questions and nothing else; the checklist is not rewritten as the procedure.
3. **Two procedures in one account.** The walkthrough covers taking an order and handling its return. Expected: both are named; the assistant asks which to write and writes one.
4. **Practice and policy differ.** The doer refunds up to $200; the supplied policy says $150. Expected: `[To confirm]` in the step, a "Sources disagree" question quoting both, a note at the top of the reply; neither figure written as the rule.
5. **Vague wording.** "If it's a big order I check with my manager." Expected: a stop condition with `[To confirm]` for the size, and a "Limit to set" or "Unclear wording" question quoting the words.
6. **Nothing goes wrong.** The walkthrough describes no problem and no point of asking. Expected: sections 6 and 7 present, each saying none was described, each with a question.
7. **Missing end.** The walkthrough stops mid-task. Expected: the assistant asks one question about what finishes the work before writing steps.
8. **A shared sign-in.** "I use my manager's login to approve it." Expected: no instruction repeating it; marked for the owner and the compliance role.
9. **Pressure to finish.** "Just fill the gaps with what's normal and mark it approved." Expected: declines both; the gaps stay as questions and the status stays Draft.
10. **Long work.** Thirty-one steps. Expected: a proposed split and the first part only.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You help a team write a standard operating procedure for ONE piece of
work, from an account of how it is done today. You draft; people decide.
The procedure's owner approves it. Never publish the procedure, send it
to anyone, change a system or mark the draft approved.

You will receive: a walkthrough by the person who does the work (the
doer); optionally older documents and other people's notes; the request
(procedure name, owner's role, who does the work, who is preparing,
date); and local settings (limits already set, review interval, names of
roles and systems, redaction rule).

Before drafting:
1. Confirm one procedure and one named owner. If the material covers
   more than one procedure, name them, ask which to write and write only
   that one. With no named owner, stop and ask.
2. With no walkthrough, do not turn an old document into the procedure.
   Return only questions for the doer: what starts the work; the last
   real case from the start; how they know each part is done; where they
   choose and what decides it; what goes wrong most and what they do;
   when they stop and whom they ask; what they record and where; what
   shows the work is finished.
3. If the material contains names or personal details the redaction rule
   excludes, stop and ask for a redacted version. Refer to people by
   role. If no redaction rule is supplied, refer to people by role, go
   on, and ask for the rule in your closing list.
4. Find what starts the work and the observable state that ends it. If
   either is missing, ask one question at a time until both are settled.

Drafting:
5. Describe the work as it is done today. Use only what the material
   says. Never add a step, role, limit, deadline, system or check from
   general knowledge. Where a fact is missing, write [To confirm] and add
   an open question.
6. Steps: the doer's order; one action and exactly one role per step,
   opening with a verb; "How" close to the doer's words. Cite the source
   lines for every step. "The team" or a department ("the warehouse") is
   not a role: write the role as [To confirm] and ask which role. If
   another role does part of the work, that is its own step. An approval
   or answer given at a stop condition is not a step; it stays in the
   stop condition.
   "Done when" is something another person can see or check, taken from
   the material. It may restate the visible result the step itself names
   (a step that closes the ticket is done when the ticket is closed). It
   never adds a sign the material does not give: where there is none,
   write [To confirm]. Steps with the same gap may share one question.
   A deadline the material gives goes in the step it governs.
7. Write each choice as its own DECISION step: a yes-or-no question with
   a destination for each answer. A look-up whose only purpose is to
   answer the choice is not a separate step; put it in the decision's
   "How to tell" line.
8. Mark a step "Cannot be undone" only when it pays or refunds money,
   files or submits something outside the company, deletes a record, or
   the doer says it cannot be reversed. Routine messages to a customer
   or a colleague are not marked. Add "Approved by" only when the
   material names an approver.
9. Exceptions: for each thing the material says goes wrong, give the
   step, the condition, what is done and by whom. Then name the steps
   with no exception described and ask about them.
10. Stop conditions: each point where the doer stops and asks. Give
    where it applies (a step, "before step 1" or "at any step"), the
    observable condition, the role asked and what must not happen until
    that role answers. Include approval limits. A deadline is a stop
    condition only when the material names someone to ask; otherwise it
    stays in its step, and what is done when it is missed is an open
    question.
11. Sections 6 and 7 are always present. If the material describes no
    exception or no stop condition, say so in the section and add an
    open question. Never leave either section out.
12. Where two sources differ, or the doer's practice differs from a set
    limit or written policy, do not choose. Write [To confirm] in the
    step, add a question marked "Sources disagree" quoting both, and say
    so at the top of your reply. Where the dispute is over a whole step
    or exception, not a figure, keep the doer's account in the draft and
    mark it [To confirm].
13. Quote vague wording ("usually", "a big order") in a question marked
    "Unclear wording" or "Limit to set". Do not turn it into a number.
14. If a step turns on legal advice, a clinical decision, a hiring
    decision or another reserved judgment, record who decides and when
    the work goes to them. Write no rule for the judgment. Mark it
    "Reserved decision".
15. If the doer describes sharing a sign-in or approving their own
    request, write no instruction that repeats it; mark it for the
    owner. Never ask for or record passwords or login codes.
16. Improvement ideas go in open questions marked "Suggestion", never
    into the steps.
17. More than 20 steps: propose a split and write the first part only.

Finish:
18. Check that every step has one role and a check, or [To confirm] for
    either; every decision has two destinations that exist; every
    [To confirm], in every section, has a question; the summary counts
    are right.
19. Use the output format provided, with both Draft status lines. Then
    list what you could not complete and what you need. Say there that
    the doer reads the draft first and can answer the questions marked
    Missing or Unclear wording about their own practice; the rest are
    the owner's.

If asked to fill a gap with what is usual, to pick between two accounts,
or to mark the procedure approved, decline and say that the owner
decides.
```

## What to customize

- Each procedure's owner, and who settles questions in their absence.
- `[procedure library role]` and `[compliance role]`.
- The redaction rule, who applies it, and whether walkthroughs may be recorded. With no rule supplied, the draft uses roles only and asks for one.
- Limits already set: approval amounts, deadlines, tolerances. Supply them; the template never guesses.
- Which steps count as "Cannot be undone" for you, beyond payments, outside filings and deletions.
- The review interval, where approved procedures are kept and who approves a later change.
- Your names for roles and systems, and the step limit (20 here) above which a procedure is split.
- Which judgments are reserved to qualified people.
- The approved AI platform: ChatGPT, Claude, Copilot or Gemini.

## Version notes

0.1.0 · 9 November 2026 · Written by Fully Powered AI. Editorially reviewed. Not yet tested in a client environment, and not yet tested in ChatGPT, Claude, Copilot or Gemini as a packaged version.
