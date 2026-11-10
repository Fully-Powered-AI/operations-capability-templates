# Pilot acceptance-test preparation: an invented example

*Illustrative example with invented data.* An invented 60-person software company’s client-onboarding handoff. The owner’s brief, then the pack prepared from it.

**Pilot brief: client-onboarding handoff**

Pilot owner: client success lead · Expert: senior client success manager

1.  Purpose: prepare the handoff record a client success manager reads before kickoff.
2.  Inputs: the signed order form, the account record and the account executive’s call notes.
3.  Output: what was sold, the start date and whether it is confirmed, contacts, sales commitments, open questions, next action.
4.  Awkward cases: an unconfirmed start date, a missing billing contact, a promise the order form does not show.

**Owner:** Client success lead

| Case | Invented record | Expected behavior |
|----|----|----|
| Ordinary | Order 3317. All three sources agree. | Complete record, every item sourced. Next action: the client success manager confirms kickoff. |
| Missing information | Client C. No billing contact anywhere. | Marks the record incomplete and drafts one question for the account executive. |
| Contradictory inputs | Order 3320. The form gives one start date; the notes say the client asked for an earlier one. | Shows both dates with their sources, marks the start unconfirmed and asks the account executive. |
| Ambiguous match | Client D. Two contacts titled project lead. | Shows both and asks which leads onboarding. |
| Stop and ask | Order 3325. The notes promise a discount the form does not show. | Stops and refers it to the sales lead. States no discount as agreed. |

**Rubric, record sheet and pass rule**

- **Completeness:** Every required field present, or marked missing with a question.
- **Factual support:** Every statement traces to one of the three inputs.
- **Correct recipient:** Record to the client success manager, questions to the account executive, promises outside the order form to the sales lead.
- **Next action:** One next action, with its owner.
- **Record sheet:** Case, instruction version, AI workspace, output as produced, a mark per criterion, the reviewer’s reason.
- **Pass rule:** Two runs per case. Every run meets its expected behavior, and the expert agrees with every mark. A miss on the stop-and-ask case fails the pilot. Any other miss is fixed and the set rerun.

Expected behavior only. The owner and the expert record the actual outputs when they run the test.
