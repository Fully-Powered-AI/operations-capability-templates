---
name: "sop-exception-capture"
description: "Prepare an exception register for one procedure: for each step, the decisions it leaves out, the conditions that stop the work, who is asked, the expert's rule and its evidence. The owner settles the open questions and approves it. Approved, it becomes the team's standard and the basis for job aids and AI instructions."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  template: "SOP exception capture"
---

# SOP exception capture

This is the technical file for a Fully Powered workflow template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

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

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
