# Workflow fit check: an invented example

*Illustrative example with invented data.* Tarnbrook Mechanical is an invented commercial heating and cooling contractor. Its people, its cases and its software are invented too. The owner (Marcus) asks for an AI to track subcontractor paperwork; the operations manager (Priya) runs the fit check on 4 November 2026. What she supplied comes first, in full, with people named by role as the template asks. Then the page that came back. It is a worked refusal: the answer is not to build what was asked for.

Two things to notice. The owner asks for a tracker that chases; the walkthrough describes a check before each job start. The page does not stop on that and does not choose: it checks the piece the walkthrough describes, says so, and makes the choice the owner’s first question. And two reasons pull in different directions: checking the whole would take as long as doing it, and the work is a register the job software may already hold. The order of the verdicts settles it, and the page says which line decided.

## What Priya supplied

**1. The request** (email from the owner, 2 November 2026)

> We got burned twice in the past year with lapsed insurance on subs. I want an AI that tracks all of this for us: every sub, every certificate, every expiry date, and chases them when something is about to run out. Can we get that built this quarter?

**2. How the work is done today** (the operations manager’s walkthrough notes, 3 November 2026)

- About forty field staff. Fifteen to twenty subcontractors in rotation.
- Before a sub’s crew starts on a job I need three things to be current: their general liability certificate, their workers’ compensation certificate, and any trade licence the job needs.
- How I do it: the week before a start date, I search email and the shared drive for that sub’s latest certificates, job by job. About 20 minutes per sub per job when the files are easy to find. Longer when they are not.
- Job starts with subs per month: six to ten, I think. I have not counted.
- Certificates arrive as PDF attachments from insurers and brokers. Some come to me, some to the project manager, some to accounts.
- There is no single list. Some of the dates are in my head.
- Job start dates and sub records are in our job software. Each sub record has a “Vendor documents” tab. We have never used it. I do not know whether it holds expiry dates or sends reminders.
- Who decides whether a job starts: the project manager. The owner, if there is a gap.
- The awkward ones: a general contractor that requires particular additional-insured wording on the certificate; a broker’s letter in place of a certificate; a sub working under another company’s policy; a renewal that is “in process”.
- Result I want at the end: for each job starting next week, a list of what is missing or expiring.
- If someone else handed me that list, the only way I could trust it would be to go and find the certificates again myself. One date is different: I can check it against the PDF in a few seconds.

**3. Three past cases** (names removed)

- **Case 1, March 2026.** Sub A, rooftop unit replacement. The liability certificate had expired 11 days before the start. The general contractor’s site supervisor found it on day two. Crew stood down for one day.
- **Case 2, June 2026.** Sub B, ductwork. Both certificates current. Found in 10 minutes. No issue.
- **Case 3, September 2026.** Sub C, controls. Broker’s letter said renewal was in process; no certificate. I called the broker. The project manager let the job start after the owner agreed. The certificate arrived nine days later.

**4. What we run on**

- Job software: used for scheduling and sub records. “Vendor documents” tab unused (see above).
- AI product: the owner has a single-seat plan on his own login. Nobody else has an account. No shared workspace.
- Workspace owner and data approver: nobody is named for either. Both would fall to the owner.
- Data rule: none written. The certificates show each sub’s policy numbers. They were sent to us for this purpose.
- Bar for “quick to check”: not set.
- Today’s date: 4 November 2026.

## What came back

```
WORKFLOW FIT CHECK: Subcontractor paperwork check before a job starts
Requested by: Owner   Does the work: Operations manager   Decides: Owner
Prepared: 4 November 2026, from the owner's email (2 November 2026), the
walkthrough notes (3 November 2026), Cases 1 to 3 and the "What we run on"
note.

THE REQUEST
"We got burned twice in the past year with lapsed insurance on subs. I want
an AI that tracks all of this for us: every sub, every certificate, every
expiry date, and chases them when something is about to run out. Can we get
that built this quarter?"
This page checks: the check the operations manager does before each start,
with the result in the operations manager's words: "for each job starting
next week, a list of what is missing or expiring". The request names a
different result. Two pieces were set aside and are judged under reasons b
and e: the tracking ("every sub, every certificate, every expiry date") and
the chasing ("chases them when something is about to run out"). The owner
chooses in question 1.

THE SIX CHECKS
1. The people: CLEAR
   The operations manager does the work: "the week before a start date, I
   search email and the shared drive for that sub's latest certificates".
   A role acts on the result: "Who decides whether a job starts: the
   project manager. The owner, if there is a gap."
2. Start and finish: CLEAR
   Start: "the week before a start date". Finish: "for each job starting
   next week, a list of what is missing or expiring".
   Depends on: a record of each sub's certificates and expiry dates, which
   does not exist: "There is no single list. Some of the dates are in my
   head." Reason b is weighed below, and creating the list is action 3.
3. Inputs: NOT CLEAR
   - Certificates: "PDF attachments from insurers and brokers. Some come
     to me, some to the project manager, some to accounts." Searched for
     in "email and the shared drive". The form is known; there is no
     single home.
   - Job start dates and sub records: "in our job software". Whether they
     can come out as a file is Not known.
   - Trade licences ("any trade licence the job needs"): where they are
     kept and how they arrive is Not known.
4. Exceptions: NOT CLEAR
   Four are named: "a general contractor that requires particular
   additional-insured wording on the certificate; a broker's letter in
   place of a certificate; a sub working under another company's policy; a
   renewal that is 'in process'". What is done is shown for one, once
   (Case 3): "I called the broker. The project manager let the job start
   after the owner agreed." For the other three, what is done and which
   role decides is Not known.
5. Examples and a way to judge: FAILS
   Three past cases supplied, one that went wrong (Case 1). The bar is "not
   set", so the default was used: under half the time the work takes. The
   work takes "About 20 minutes per sub per job when the files are easy to
   find"; half of that is 10 minutes. For the whole list: "the only way I
   could trust it would be to go and find the certificates again myself."
   Step that differs: reading one date from one certificate: CLEAR. "One
   date is different: I can check it against the PDF in a few seconds."
6. Platform and permission: FAILS
   "the owner has a single-seat plan on his own login. Nobody else has an
   account. No shared workspace." The operations manager, who would run
   it, has no account. "Workspace owner and data approver: nobody is named
   for either." "Data rule: none written." The certificates "were sent to
   us for this purpose"; that is not an approval to put them into the AI
   product.

REASONS TO SAY NO
a. Your software already does it: APPLIES. Nobody has looked. "Each sub
   record has a 'Vendor documents' tab. We have never used it. I do not
   know whether it holds expiry dates or sends reminders."
b. It is a list, a register, a reminder or a fixed rule: APPLIES. "every
   sub, every certificate, every expiry date" is a register. "chases them
   when something is about to run out" is a reminder. The weekly list
   rests on a record that does not exist: "There is no single list."
c. Checking would take as long as doing: APPLIES. Check 5 fails for the
   whole: "the only way I could trust it would be to go and find the
   certificates again myself."
d. Nobody here can judge it: DOES NOT APPLY. The operations manager judges
   a date "against the PDF in a few seconds"; the project manager and the
   owner decide the gaps (Case 3).
e. It needs more than a person-run workflow: APPLIES. "chases them" is a
   message sent by the AI, and "tracks all of this for us" is a record kept
   by the AI. Both are taken out: a person sends and a person records.
f. The data would pass through a party nobody has approved: DOES NOT
   APPLY. The inputs name no outside service. The missing approval for the
   AI product itself is under check 6.

VERDICT: DO SOMETHING SIMPLER FIRST
Line 2 of the order decides it: nobody has looked at what the job software
already does (a), and what was asked for is a register and a reminder (b).
Do not build "an AI that tracks all of this".

WHAT TO DO, IN ORDER
1. Operations manager: open the "Vendor documents" tab on one sub record,
   with the software's help pages beside you, and note whether it holds
   expiry dates and sends reminders. If it does, the owner has it switched
   on and nothing is built.
2. Owner: say which result you want (question 1), and name one place every
   certificate is sent.
3. Operations manager: put every sub's certificates and licences, with
   their expiry dates, in one list: the tab if it does the job, otherwise a
   simple register with a reminder on each date.
4. Operations manager: for one month, count the job starts with subs and
   the minutes each check takes.
5. Owner: if the part below is still wanted once the list exists, give the
   operations manager an account on a plan that lets a team share
   instructions, and write down whether certificates may go into the AI
   product.

THE PART WORTH A WORKFLOW
Reading one incoming certificate. The operations manager gives the
assistant one certificate PDF; it proposes the insured company, the kind of
cover and the expiry date; the operations manager confirms each against the
PDF "in a few seconds" and enters it in the list.
It would never: record a date nobody has confirmed; say whether a job can
start; judge a broker's letter, another company's policy or a renewal "in
process"; contact a sub, a broker or an insurer.
Ready now: No, it needs check 6 to be Clear (an account for the operations
manager, a plan a team can share, an approval for this data), the list to
exist (a reading with nowhere to put its answer saves nothing) and a few
real certificates to try it on. Give it its own fit check then.

WHAT IT IS WORTH
Supplied: "burned twice in the past year"; "About 20 minutes per sub per
job when the files are easy to find. Longer when they are not."; job starts
with subs per month "six to ten, I think. I have not counted."; "Fifteen to
twenty subcontractors in rotation"; Case 1: "Crew stood down for one day."
Not known: what happened the second time the company was "burned" (Case 1
shows one lapse; nothing supplied shows the other); a counted number of
starts per month; how long a check takes when the files are hard to find;
what the stand-down day cost.
Measures to watch: job starts where a missing or expired document is found
after the crew has started; minutes per sub per job for the check. A lapse
avoided is not a time saving. No saving is estimated here.

WHAT WOULD CHANGE THE VERDICT
- The "Vendor documents" tab holds expiry dates and sends reminders: the
  verdict stands, the tab is the simpler thing, and nothing is built.
- The tab does not do it, the list exists and check 6 is Clear: the
  certificate-reading part can be checked again as "Build one part".
- With the list in place, the operations manager can confirm the weekly
  list without finding the certificates again: reason c stops applying.

OPEN QUESTIONS
For the owner:
1. Which result do you want checked: "for each job starting next week, a
   list of what is missing or expiring" (the operations manager's words,
   checked here), or a standing tracker that "chases them" (yours)?
2. Do you approve certificates showing "each sub's policy numbers" going
   into the AI product? If not you, who approves?
3. Will the operations manager get an account, on which plan, and who will
   own the workspace?
4. What is your bar for "quick to check"? The default was used: under half
   the time the work takes.
5. What was the second time you were "burned"?
For the operations manager:
6. Does the "Vendor documents" tab hold expiry dates, and does it send
   reminders?
7. What do you do with additional-insured wording, a broker's letter, and
   a sub working under another company's policy, and who decides each?
8. Where are trade licences kept, and can the job software give you next
   week's starts with subs as a file?
Also not known: a counted number of starts per month; how long a check
takes when the files are hard to find; what the stand-down day cost.

Status: Prepared for the owner's decision. Nothing built, sent or changed.
Owner's decision: [blank until decided]   Date: [ ]
```

Marcus read the page with Priya and decided to start with step 1. That decision is his, and he writes it on the last line with the date; the page only prepared it.
