# Write an SOP from how the work is done: trial on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Fable 5.2
- **Date:** 2026-11-09
- **Runs:** three. One on the template as first written, two on the revised template.

The inputs are the invented example published with this template. The company, its people, its systems, its policy and its figures are invented, and no client data was used. This is a record of runs on that example. It is not a test in any company's environment.

## Inputs used

The three inputs in [the example](example.md) under "The inputs", and nothing else:

- the request and local settings from the operations lead, dated 9 November 2026 (L);
- the walkthrough with the returns coordinator, dated 3 November 2026, lines W1 to W14;
- the note from the customer service lead, dated 5 November 2026, lines N1 to N3.

Each time, the template's instructions for an AI assistant and its output format were given to the assistant as written, followed by these inputs.

## The first run, and what it changed

The first run used the template as first written and a request with no redaction rule. It finished without stopping and produced all ten sections: 18 steps, 3 exceptions, 5 stop conditions and 17 open questions. It found the three disagreements between sources and chose none of them. It also showed where the instructions left the assistant guessing, and the template was revised on each point:

1. **"Done when".** The walkthrough rarely says how the coordinator knows a step is done. Read strictly, seven steps got `[To confirm]`. The template now says a check may restate the visible result the step itself names, and may add nothing else.
2. **Look-ups before a choice.** Steps such as "check the photos" have no result another person can see. They are now part of the decision they serve, on a "How to tell" line.
3. **"Cannot be undone".** The first wording covered anything that "sends"; the run marked four steps and could not tell where to stop. The mark is now for payments and refunds, filings outside the company, deletions, and anything the doer says cannot be reversed. Routine messages are not marked, and "Approved by" appears only when the material names an approver.
4. **Deadlines.** A deadline with nobody to ask did not fit a stop condition. It now goes in the step it governs, and what happens when it is missed is an open question.
5. **Stops with no step.** The format now allows "before step 1" and "at any step".
6. **Teams as roles.** The rule that a team or department is not a role was missing from the instructions. It is there now: the role is written `[To confirm]` and asked about.
7. **No redaction rule.** The instructions now say what to do without one (use roles, go on, ask for the rule), and the example's request now carries a rule: "roles only. No customer or staff names."
8. **A disputed step.** Where two accounts differ over a whole step, the doer's account stays in the draft, marked, until the owner decides.
9. **Who answers.** Seventeen questions is a lot to put to an owner. The doer now answers the questions marked Missing or Unclear wording about their own practice during their read; the rest stay with the owner.

## The runs on the revised template

Both were fresh sessions with no tools, no project files and no sight of the earlier output: only the instructions, the output format and the inputs.

The second run produced 17 steps, 4 exceptions, 4 stop conditions and 19 open questions. It followed every revised rule, but it wrote the customer service lead's late-claim decision and the operations lead's refund approval as steps of their own, alongside the stop conditions that already held them. One sentence was added to the instructions: an approval or answer given at a stop condition is not a step.

The third run used the instructions as they are published. **Its complete reply is the output shown in [the example](example.md).** Two things differ there from what the assistant returned. The typesetting: the reply came partly as plain text, and the example sets it as headings and lists. And one line of section 4, which read "A prepaid return label for items over $75"; that takes "over $75" to mean the item, which step 10 of the same reply leaves to the owner (Q9), so the example says "when step 10 calls for one".

The third run finished without stopping to ask anything: 15 steps, 2 exceptions, 4 stop conditions and 18 open questions.

## What was observed in the third run

Set against the template's reviewer checklist:

- Every required part was produced: the note at the top about disagreeing sources, the ten sections, both Draft status lines in the format's words, and the closing list of what could not be completed.
- Every step has one role and a source. The shipment (step 7) has `[To confirm]` for its role, because the walkthrough says only "the warehouse", with a question (Q5).
- Every "Done when" either restates the step's own result (the order has been raised, the claim number is on the ticket, the row is in the sheet, the ticket is closed) or is `[To confirm]` with a question (steps 3, 7, 9 and 11).
- Every decision has two destinations, and each exists. The three look-ups (photos, delivery date, stock) sit inside their decisions.
- Every `[To confirm]`, in every section, points to a question, including "Not covered" and "How often" (Q18). The summary counts are right.
- The three disagreements (the $150 or $200 refund limit, the 30 or 21 day claim window, who deals with a ticket without photos) were left for the owner. No figure from either pair was written as the rule. The coordinator's handling of a ticket without photos stays as E1, marked.
- "Cannot be undone" is on the refund and the carrier claim only. The carrier's deadline is in step 12, and a missed window is a question (Q13).
- The third-claim stop applies "before step 1" and the glass injury stop "at any step", as the walkthrough has them.
- The vague wording ("I sort of play that by ear", "in a year", "it's over $75") was quoted and not turned into a rule.
- No names, personal detail or sign-in detail appear.
- The closing list says the returns coordinator reads first and names the questions she can answer.

Where the reply falls short or the instructions still leave a choice:

1. **Two "How to tell" lines are the assistant's words, not the doer's.** Step 4 says "the customer's answer to step 3" and step 8 says "compare the refund amount with the limit". Neither adds a fact, but the format asks for the doer's words or `[To confirm]`.
2. **Restated checks are a judgment.** The second run wrote "the refund has been made in the payment system" for the refund; the third wrote `[To confirm]` and asked what shows it has gone through. Both are within the rule. An owner who wants fewer questions will get different counts from run to run.
3. **Eighteen questions for fifteen steps.** The reply sends thirteen of them to the returns coordinator first. Several of those (Q5 on the warehouse role, Q16 on where approvals are recorded, Q18 on scope) are not hers alone to answer, so the split is rough.
4. **Section 4 read "over $75" as the item** while step 10 asked. Corrected in the example, as noted above.
5. **The mark "Reserved decision"** was used for the glass injury case. Whether that case counts as a reserved judgment is the assistant's guess; the instructions list legal, clinical and hiring judgments "or another reserved judgment".
6. **The tagging of the ticket** is done by "customer service", a department. The third run did not ask which role; the second did. It happens before the procedure starts, and the rule does not say whether that counts.

Shortcomings of this trial: three runs, one model, on tidy invented inputs with a clear start and end. The runs differed in step count (17 and 15 on nearly the same instructions), so the shape of a draft is not fixed by the template alone. No run exercised a path that stops the work (no owner, no walkthrough, detail to redact, more than one procedure, more than 20 steps, a shared sign-in), and none of the template's ten proposed acceptance tests was run as such. Whether the draft matches how the work is really done cannot be judged from invented material: the doer's read and the owner's approval are steps for people and were not part of any run.

## Edits after the recorded runs

9 November 2026. The template was edited after the third run, and no run was repeated. Two changes touch the instructions and the output format, each answering a shortfall above:

- **Shortfall 1.** The format's "How to tell" line now also allows a pointer to the earlier step or the supplied limit that answers the decision, as steps 4 and 8 of the recorded output have it.
- **Shortfall 6.** The instructions now say that a team named only in what starts the work, before step 1, does no step and may stay as the doer named it, which is what the third run did.

A sentence was also added under "When to use it and when not to", saying this workflow template comes first where nothing is written yet. The recorded output is unchanged.
