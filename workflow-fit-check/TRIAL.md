# Workflow fit check: one trial on its invented example

- **Product:** Claude (run in Claude Code, its command-line coding tool)
- **Model:** Claude Fable 5.2
- **Date:** 2026-11-09
- **Runs:** one on this version of the instructions. Two earlier runs the same day, on earlier wording, are summarised at the end.

The inputs are the invented example published with this template. The company, its people, its cases and its software are invented, and no client data was used. This is a record of one run on that example. It is not a test in any company's environment.

## Inputs used

Exactly what the operations manager supplies in [the example](example.md) under "What Priya supplied", and nothing else:

- the owner's request, an email dated 2 November 2026;
- the operations manager's walkthrough notes, dated 3 November 2026, including how a finished list would be confirmed;
- three past cases with people and companies named by role or label (March, June and September 2026), one of which went wrong;
- the note on what the company runs on: the job software and its unused "Vendor documents" tab, a single-seat AI plan on the owner's login, nobody named as workspace owner or data approver, no written data rule, no bar set for "quick to check", and 4 November 2026 given as today's date.

The template's instructions for an AI assistant and its output format were pasted as written, followed by these inputs, as one message to a new session. That session had no tools and had not seen the template's other sections, the example's page or any earlier run. The run was started by the session that had just revised the instructions, which is a limit on how independent it is: the same model wrote the rules and followed them.

## What came out

The run finished in one reply, did not stop to ask anything, and produced a full page with the verdict "Do something simpler first". The complete output, as it came back (the lines are not wrapped):

```
WORKFLOW FIT CHECK: Weekly list of missing or expiring subcontractor certificates for next week's job starts
Requested by: Owner   Does the work: Operations manager   Decides: Owner
Prepared: 4 November 2026, from the owner's email (2 November 2026), the operations manager's walkthrough notes (3 November 2026), three past cases with names removed (March, June and September 2026) and the "What we run on" list (4 November 2026).

THE REQUEST
"We got burned twice in the past year with lapsed insurance on subs. I want an AI that tracks all of this for us: every sub, every certificate, every expiry date, and chases them when something is about to run out. Can we get that built this quarter?"
This page checks: the piece the walkthrough describes, with the result in the operations manager's words: "for each job starting next week, a list of what is missing or expiring." The request names different results. Two were set aside: the tracking ("every sub, every certificate, every expiry date") and the chasing ("chases them when something is about to run out"). Both are judged under the reasons to say no (b and e). The owner chooses between them in question 1.

THE SIX CHECKS
1. The people: CLEAR
   The operations manager does the work: "the week before a start date, I search email and the shared drive for that sub's latest certificates, job by job." Acting on the result: "Who decides whether a job starts: the project manager. The owner, if there is a gap."
2. Start and finish: CLEAR
   Start: "the week before a start date". Finish: "for each job starting next week, a list of what is missing or expiring."
   Depends on: one record of each sub's certificates and expiry dates, which does not exist ("There is no single list. Some of the dates are in my head."), so reason b is weighed and creating it is under WHAT TO DO. It also depends on job start dates, which exist: "Job start dates and sub records are in our job software."
3. Inputs: NOT CLEAR
   - Certificates (general liability, workers' compensation): "PDF attachments from insurers and brokers. Some come to me, some to the project manager, some to accounts." They are searched for in "email and the shared drive". The form is known; the home is scattered.
   - Expiry dates: "Some of the dates are in my head."
   - Job start dates and sub records: "in our job software". How they would come out of it (file, export, pasted text) is Not known.
   - Trade licences ("any trade licence the job needs"): where they are kept, how they arrive and which jobs need one are Not known.
4. Exceptions: NOT CLEAR
   Four are named: "a general contractor that requires particular additional-insured wording on the certificate; a broker's letter in place of a certificate; a sub working under another company's policy; a renewal that is 'in process'."
   - Renewal in process: Case 3 shows what was done once: "I called the broker. The project manager let the job start after the owner agreed." Whether that is the rule is Not known.
   - Additional-insured wording: what is done and which role decides are Not known.
   - Broker's letter in place of a certificate: what is done and which role decides are Not known.
   - Sub under another company's policy: what is done and which role decides are Not known.
5. Examples and a way to judge: FAILS
   Three real past cases were supplied (March, June, September 2026). No bar was supplied ("Bar for 'quick to check': not set"), so the default was used: under half the time the work takes. The work takes "About 20 minutes per sub per job when the files are easy to find", and half of that is 10 minutes. The owner is asked for the bar in question 3. For the whole list, the operations manager says: "the only way I could trust it would be to go and find the certificates again myself."
   Step that differs: reading one expiry date from one certificate: CLEAR. "One date is different: I can check it against the PDF in a few seconds." The three supplied cases count for it.
6. Platform and permission: FAILS
   "the owner has a single-seat plan on his own login. Nobody else has an account. No shared workspace." The operations manager, who would run it, has no account. "Workspace owner and data approver: nobody is named for either. Both would fall to the owner." "Data rule: none written. The certificates show each sub's policy numbers. They were sent to us for this purpose." The reason the data was sent is not approval for this use.

REASONS TO SAY NO
a. Your software already does it: APPLIES. "Each sub record has a 'Vendor documents' tab. We have never used it. I do not know whether it holds expiry dates or sends reminders." Nobody has looked, so the first action is that a person opens it and looks.
b. It is a list, a register, a reminder or a fixed rule: APPLIES. The request is a register ("every sub, every certificate, every expiry date") and a reminder ("chases them when something is about to run out"). The result the operations manager wants is "a list of what is missing or expiring", and it rests on a record that does not exist: "There is no single list."
c. Checking would take as long as doing: APPLIES. Check 5 FAILS for the whole: "the only way I could trust it would be to go and find the certificates again myself."
d. Nobody here can judge it: DOES NOT APPLY. The operations manager can judge a result on the company's own cases: "I can check it against the PDF in a few seconds" for one date, and for the whole list by finding the certificates again (that cost is reason c). Who judges the additional-insured wording is Not known.
e. It needs more than a person-run workflow: APPLIES. "chases them when something is about to run out" is a message sent by the AI, and "an AI that tracks all of this for us" is a run nobody starts. That piece is taken out: the chasing stays with a person (in Case 3, "I called the broker") or becomes separate scoped work. What is left is the weekly list and the date-reading step, judged above.
f. The data would pass through a party nobody has approved: DOES NOT APPLY.
   The inputs name no connector or go-between tool. The route by which certificates would reach the AI product is Not known. Approval of the AI product itself is check 6.

VERDICT: DO SOMETHING SIMPLER FIRST
Line 2 of the order decided it: nobody has looked at whether the job software's "Vendor documents" tab already does this (a), and the work is at heart a register and a reminder, with no single list yet (b).

WHAT TO DO, IN ORDER
1. Operations manager: open the "Vendor documents" tab on one sub record and see whether it holds expiry dates and sends reminders; tell the owner what is there.
2. Owner: choose which piece is wanted (question 1) and name one place where every certificate is sent and kept, whether it arrives at the operations manager, the project manager or accounts.
3. Operations manager: start the one list (each sub, each of the three documents, each expiry date, including the dates now "in my head"), in the tab if step 1 shows it serves, otherwise in one list. Count the job starts with subs for a month.
4. Owner: for each of the four awkward ones, write down what is done and which role decides.
5. Owner: only if the date-reading part is still wanted after steps 1 to 3, decide on a plan that lets a team share instructions and an account for the operations manager. Then name the workspace owner and say whether certificates showing "each sub's policy numbers" are approved for this use.

THE PART WORTH A WORKFLOW
One certificate PDF goes in; a proposed expiry date for the one list comes out. The operations manager confirms it against the PDF on screen "in a few seconds".
It would never: decide whether a job starts; chase a sub, broker or insurer; send anything; change a record in the job software; judge additional-insured wording, a broker's letter, another company's policy or a renewal "in process".
Ready now: No, it needs check 6 to be CLEAR (an account for the operations manager on a plan that lets a team share instructions, a named workspace owner, approval of this data for this use). It also needs the one list it would fill, which does not exist, and the look at the "Vendor documents" tab to be done first. Check 5 is CLEAR for it and neither e nor f touches it.

WHAT IT IS WORTH
Supplied: "About 20 minutes per sub per job when the files are easy to find. Longer when they are not." "Job starts with subs per month: six to ten, I think. I have not counted." "Fifteen to twenty subcontractors in rotation." "We got burned twice in the past year". Case 1: "expired 11 days before the start", "Crew stood down for one day." Case 2: "Found in 10 minutes." Case 3: "The certificate arrived nine days later."
Not known: a counted number of job starts with subs per month; how many subs per job; how long the search takes when files are not easy to find; what the stood-down day cost; which two events the owner means; how long the chasing takes; what a different plan would cost.
Measures to watch: job starts where a certificate was missing or expired on the start date; minutes per sub per job to produce the list. No saving is estimated here.

WHAT WOULD CHANGE THE VERDICT
- A person looks at the "Vendor documents" tab and reports what it holds. If it holds expiry dates and sends reminders, the simpler step is the answer. If it does not, reason a stops applying.
- One list exists in one known home and check 6 is CLEAR. The date-reading part could then be checked again as its own piece.
- With one list in place, the operations manager can confirm the weekly list in under the bar without finding the certificates again. Check 5 for the whole would change and reason c would stop applying.

OPEN QUESTIONS
For the owner:
1. Which piece do you want: the weekly list the walkthrough describes ("for each job starting next week, a list of what is missing or expiring"), the tracking of "every sub, every certificate, every expiry date", or the chasing? This page checked the first and set the other two aside.
2. Nobody is named as workspace owner or data approver, and both "would fall to the owner". Do you take both roles, and do you approve certificates showing "each sub's policy numbers" for this use?
3. What is your bar for "quick to check"? The default (under half the time the work takes, here 10 minutes) was used.
4. For additional-insured wording, a broker's letter in place of a certificate and a sub under another company's policy, what is done and which role decides? Is Case 3 the rule for a renewal "in process"?
5. Where should every certificate be sent and kept from now on?
For the operations manager:
6. What does the "Vendor documents" tab hold, and does it send reminders?
7. Counted, how many job starts with subs are there in a month, and how long does the search take when the files are not easy to find?
8. In what form can job start dates come out of the job software, and where are trade licences kept?
Also not known: how far ahead "about to run out" means; who would do the chasing and how; whether the project manager and accounts would pass certificates on; whether anything could be built "this quarter" (no date is promised here).

Status: Prepared for the owner's decision. Nothing built, sent or changed.
Owner's decision: [blank until decided]   Date: [ ]
```

## What was observed

**Every heading and label of the output format was produced,** in order, ending with the status line and the owner's decision left blank as written. Nothing followed the last line.

**It did not stop on the mixed request.** The owner asks for tracking and chasing; the walkthrough describes a check before each job start. As the instructions now say, the page checks the walkthrough's piece, quotes both results under "The request", names the two pieces set aside, and makes the choice the owner's question 1.

**Every mark is one of the three,** with nothing added. Check 2 is "CLEAR" with the missing list on its own "Depends on" line. Check 4 is "NOT CLEAR" because what is done is shown for one of the four exceptions only. Check 5 is "FAILS" for the whole and "CLEAR" for reading one date, each on the operations manager's quoted words. Check 6 is "FAILS".

**The verdict follows the order.** Reasons a, b, c and e apply. Reason c on its own would point to "Leave it with your people"; the page takes line 2 of the order, because a and b apply, and says so under the verdict. The first action is to open the "Vendor documents" tab, and reading one certificate is named as the part, not ready. That is what the template's first proposed acceptance test expects.

**Against the reviewer checklist,** as far as a run on invented notes can show:

1. One piece of work, and the page says which: yes.
2. One mark per check, with quoted words, nothing Clear on an assumption: yes for the six checks. Under reason d the run argues that the whole list can be judged "by finding the certificates again", which is its own reasoning and not a quotation.
3. Open questions for every gap that could change a mark or the verdict: yes for the tab, the exceptions, the export, the trade licences, the counts, the approval and the bar. Several items listed as not known under "What it is worth" (among them which two events the owner means, what the stood-down day cost and what a different plan would cost) appear neither as a question nor on the "Also not known" line.
4. All six reasons on the page, each marked: yes.
5. Nothing stated about what a named product can do: yes. The job software is not named in the inputs.
6. The verdict is one of the five and is the first line of the order that fits: yes, line 2.
7. The part takes a file in, proposes, and a person confirms; its "would never" line covers sending, recording and deciding: yes.
8. No figure that was not supplied: yes. "10 minutes" is half of the supplied 20, shown as that, which the instructions allow. Nothing was added to "burned twice".
9. No names: yes. The inputs now name people by role, so this run did not show what happens when a name is supplied.
10. Every action starts with a role; at most five actions and eight questions: yes by count. The limits were met partly by merging: action 3 holds two actions, and questions 2, 4, 7 and 8 each hold two questions.
11. Status line present, owner's decision blank: yes.

**Nothing made the run stop.** The walkthrough notes were present, the cases had no names, and no password, promise, sending or change of verdict was asked for. Those refusals were not exercised in this run.

**Where the instructions still left a choice to the assistant:**

1. **What counts as an input.** The run listed the expiry dates "in my head" as an input of their own under check 3. The published example treats the dates as something read from the certificates. The mark is the same either way.
2. **How to read "tracks all of this for us" under reason e.** The run read it as a run nobody starts. The example reads it as a record kept by the AI. Both are in reason e; the instructions do not say which a loose phrase means.
3. **Who answers the exception questions.** The run sent them to the owner; the example sends them to the operations manager, who does the work.
4. **How much to list as not known under "What it is worth".** The run added figures nobody had raised, such as the cost of a different plan.
5. **Merging to stay inside a limit.** The instructions cap the number of actions and questions and do not say that each holds one thing.

**Differences from the published example:**

- The marks on all six checks, the step inside check 5, all six reasons and the verdict are the same.
- The title is different.
- What to do: the run asks the owner to write down what is done with each awkward case, and folds the month of counting into the action about the list. The example gives the counting its own line and leaves the awkward cases to an open question.
- The part: the run proposes the expiry date only. The example proposes the insured company, the kind of cover and the expiry date.
- Open questions: the run asks where certificates should be sent and kept. The example asks what the second "burned" event was; the run lists that as not known and asks no question.
- The example's lines are wrapped; the run's are not.

**Shortcomings of this trial.** One run, on one example, in one product, started by the session that wrote the instructions. The example leads to a single verdict; "Build it", "Build one part", "Not yet" and "Leave it with your people" were not reached, so most of the order of verdicts was not exercised. The run did not exercise a title-only request, a missing walkthrough, sensitive detail in a case, a reserved judgment, pressure to change a verdict, a pasted password, or a request to send or switch something on. The page runs to about two printed pages. Nobody who does this kind of work read the result.

## Earlier runs the same day

**The first run** was on the first draft of the instructions and the first version of the example's inputs. It reached the same verdict and showed where the draft left the assistant a choice: a strict reading told it to stop and ask which piece of work to check, while the example carried on; check 2 produced a mark that is not one of the three ("CLEAR, with a finding"); check 4 had no rule for its mark; the verdict rules left out "Leave it with your people" from their order and gave reasons e and f no verdict; the rule for a request and a walkthrough that disagree was missing from the instructions; and nothing said whether the AI product itself is the unapproved outside party. The instructions were rewritten to settle each of these, and the published example was rewritten to follow them. One line was added to the example's walkthrough notes (how the operations manager would confirm a finished list, and one date), a line naming nobody as workspace owner or data approver, and today's date; people in the notes are now named by role.

**The second run** was on the rewritten instructions and the inputs as published. It reached the same marks and verdict as the run recorded above. It left the owner's decision as empty space where the format has "[blank until decided]", and added a note after the page about which date to use. Two sentences of the instructions were tightened for those two points (copy the last two lines as written and add nothing after them; "Prepared" carries the date the user gives as today's), and the run recorded above was made on that final wording.
