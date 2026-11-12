# SOP exception capture

Workflow template 0.1.0 · Operations and process improvement · Fully Powered AI

## Purpose

Prepare an exception register for one procedure: for each step, the decisions it leaves out, the conditions that stop the work, who is asked, the expert's rule and its evidence. The owner settles the open questions and approves it. Approved, it becomes the team's standard and the basis for job aids and AI instructions.

## When to use it and when not to

Use it before a procedure goes to an AI assistant or a new colleague, after a mistake recurs in one step, before the expert changes role, or when two teams run it differently.

Do not use it for a procedure with no owner or one being redesigned. A reserved professional judgment, such as legal advice, conflict clearance, a clinical decision or a hiring decision, is never written as a rule; record who makes it and when the work goes to them.

## Roles

- **Preparer** (runs it): an operations analyst, team lead or the owner, with an AI assistant.
- **Expert** (source and reviewer): the person who does the work most reliably; checks the register against their words.
- **Colleagues** (consulted): others who do the work; their differences become open questions.
- **Procedure owner** (decides): settles open questions, approves the register, authorizes any change to the procedure.

## Inputs

1. **The written procedure**, from the procedure library or the owner. If none exists, transcribe a 20-minute walkthrough of one real case.
2. **Three to five recent cases, including one that went sideways**: the record, what happened, the outcome, from the system of record or email. With fewer than three, proceed and note the gap. If none went sideways, record the expert's account of the last one that needed help.
3. **Notes or a transcript from thirty minutes with the expert.** Without them, prepare the questions (step 5) and stop.
4. **Colleagues' accounts** (optional). If absent, say so in the header.
5. **Local settings**: owner role, redaction rule, thresholds already set.

## The procedure

1. **Confirm scope.** One procedure, one version, one named owner. For several procedures, prepare one register each, starting with the owner's choice.
2. **Prepare the cases.** Apply the redaction rule. Use plain identifiers (Case 1, Account 5502) and refer to people by role.
3. **Number the steps exactly as written.** Do not improve the wording. For a walkthrough, use the expert's order.
4. **Read each case against the steps.** Note every departure: missing information, a judgment, a wait, an unnamed person asked, records that disagree.
5. **Prepare the conversation.** Five standard questions, plus one per departure the cases do not explain:
   - Walk me through the last one that went sideways. What did you notice first?
   - For each step, what makes you stop, and whom do you ask?
   - What do you check that the procedure never mentions?
   - When two records disagree, which one wins?
   - Who does this differently from you, and which way should be the rule?
6. **Hold the conversation.** A person asks, recording only with the expert's agreement.
7. **Draft one entry per step** in the output format. Stop conditions must be observable, the person asked is a role, the rule is imperative and close to the expert's words. Rules for drafting:
   - A rule enters only with a case or a direct quotation behind it; otherwise it becomes an "Unconfirmed" open question. Never alter quoted words.
   - Record numbers the expert stated. Where they gave none ("a big difference"), write `[threshold: owner to set]` and add an open question.
   - Where the cases show nothing, write "No exception found in the cases supplied."
8. **Compare with colleagues.** Where accounts differ, do not choose. Write an open question with both versions, the role following each and the evidence.
9. **Expert accuracy check.** The expert's corrections replace the original wording.
10. **Send to the owner** as a Draft to settle each open question and approve or amend each entry.
11. **Record approval**: date, owner role, procedure version. Only then does `[procedure editor role]` change the procedure.

## Exceptions and stop conditions

- **No named owner.** Stop and ask the requester to name one.
- **Personal or client data beyond the redaction rule.** Stop; return the case to the owner.
- **A rule that conflicts with written policy, a contract or a regulation.** Do not enter it as a rule. Open question marked "Conflicts with written policy," for the owner and `[compliance role]`.
- **A rule that bypasses an approval limit**, such as approving one's own purchase. Also flag it to the owner directly.
- **The expert asks for something to stay off the record.** Leave it out; the header says "One topic withheld at the expert's request."
- **The owner is the only expert.** `[second reviewer role]` reads the register before approval.

## Output format

```
Exception register · [Procedure name] · Procedure version [n]
Owner: [role]  Expert: [role]  Prepared by: [role]  Date: [D Month YYYY]
Sources: [procedure | walkthrough]; Cases [identifiers]; conversation [date]
Coverage notes: [gaps, withheld topic, or None]
Status: Draft for the owner's approval. The procedure has not been changed.

Step [n]: [wording exactly as written]
  Missing decisions: [...]
  Stop conditions: [...]
  Who is asked: [role], when [condition]
  Expert's rule: [instruction]
  Evidence: [Case identifier]. [Role]: "[exact words]"

Open questions for the owner
  Q[n]. [Question]
    Version A: [practice], followed by [role]. Evidence: [...]
    Version B: [practice], followed by [role]. Evidence: [...]
    Marked: [Disagreement | Unconfirmed | Conflicts with written policy | Threshold to set]
    Owner's decision: [blank until settled]

Approval: [owner role]  Date: [ ]  Procedure version: [ ]
```

## Reviewer checklist

- Every step appears, in order, in its original wording.
- Every rule cites a case or an exact quotation.
- Stop conditions are observable; every person asked is a real role.
- No disagreement has been resolved by the preparer or the assistant.
- Thresholds are the expert's figures or marked for the owner.
- No client or staff names remain.
- The status says Draft and the procedure is unchanged.

## Acceptance tests

Proposed tests. They have not been run.

1. **Complete inputs**: procedure, four cases, transcript. Expected: an entry per step, each rule cited.
2. **Walkthrough only.** Expected: steps in the expert's order; Sources says "walkthrough".
3. **Two cases only.** Expected: register prepared; the gap noted.
4. **Contradictory colleagues**: the expert holds an incomplete application; a colleague opens it on restricted terms. Expected: an open question with both versions; no rule chosen.
5. **Unsupported rule** in the preparer's notes. Expected: appears only as an "Unconfirmed" open question.
6. **Ambiguous threshold**: "if it's well over, it goes back." Expected: `[threshold: owner to set]` and a matching open question.
7. **Unredacted case** with a client's name and home address. Expected: the assistant stops and asks for redaction.
8. **Policy conflict**: the expert approves their own small purchases, which policy forbids. Expected: no rule, a "Conflicts with written policy" question and a direct flag to the owner.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You help a procedure owner prepare an exception register for one written
procedure. You prepare; people decide. Never change the procedure, contact
anyone or settle a disagreement.

You will receive the procedure (or a walkthrough), three to five cases, a
conversation record with the expert, optional colleagues' notes and local
settings.

Before drafting:
1. Confirm one procedure and one named owner. If not, stop and ask.
2. If a case contains names or personal details the redaction rule
   excludes, stop and ask for a redacted version. Refer to people by role.
3. With no conversation record, produce only interview questions: the last
   case that went sideways, where they stop and whom they ask, what they
   check that the procedure omits, which record wins, who does it
   differently. Add one per unexplained departure in the cases.

Drafting:
4. Copy and number each step exactly as written.
5. For each step write: Missing decisions; Stop conditions (observable);
   Who is asked (a role); Expert's rule (imperative, close to their words);
   Evidence (case identifier and exact quotation).
6. Enter a rule only if a case or a quotation supports it. Otherwise add an
   open question marked "Unconfirmed". Never alter quoted words.
7. Record numbers the expert stated. If none, write [threshold: owner to
   set] and add an open question.
8. Where the cases show nothing, write "No exception found in the cases
   supplied."
9. Where accounts differ, write an open question with both versions, the
   role following each and the evidence. Do not choose.
10. If a rule conflicts with written policy, a contract or a regulation, or
    bypasses an approval limit, enter it only as an open question marked
    "Conflicts with written policy" and say so at the top of your reply.
11. If a step needs legal advice, conflict clearance, a clinical decision or
    a hiring decision, record who decides and when. Write no rule for it.

Use the register format provided, with the Draft status line. Then list
what you could not complete and what you need. If asked to edit the
procedure, say that changes follow the owner's written approval.
```

## What to customize

- Each procedure's owner, and who settles questions in their absence.
- `[procedure editor role]`, `[compliance role]`, `[second reviewer role]`.
- The redaction rule, and who applies it.
- Thresholds already set (tolerances, approval limits, cutoffs).
- Which judgments are reserved to qualified people.
- Recording consent; where transcripts and registers are kept; who approves later changes.
- The approved AI platform: ChatGPT, Claude, Copilot or Gemini.

## Version notes

0.1.0 · 9 November 2026 · Written by Fully Powered AI. Editorially reviewed. Not yet tested in a client environment, and not yet tested in ChatGPT, Claude, Copilot or Gemini as a packaged version.
