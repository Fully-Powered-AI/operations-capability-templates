# Workflow fit check: is this piece of work ready for AI?

Capability template, version 0.1.0.

## Purpose

Run one piece of work through six checks and prepare a short verdict page for the owner: build it as an AI workflow, build one part, do something simpler first, not yet, or leave it with your people. The page shows the evidence for each check, each of the six reasons to say no and whether it applies, what to do in order, the one part worth a workflow if there is one, and what would change the answer. It is kept short by fixed limits: five actions, three facts that would change the verdict, eight open questions. Expect about two printed pages. The assistant prepares the page from what the person supplies; the owner decides what gets built.

The check is built to say no. Most requests for "an AI that does all of this" contain a setting to switch on, a register to set up, and one step worth building. Finding that step, and saying plainly what the rest needs, is the result.

## When to use it and when not to

Use it when someone asks whether AI can take on a piece of work, before any time or money goes into building. Use it again when the facts change: new software, a different plan for the AI product, a list that now exists, a data rule that has been written. For several requests, run one check each and compare the pages.

Do not use it:

- to choose an AI product or compare vendors. The check reads the plan you are on; it does not shop;
- to estimate savings or a return. It reports only the figures supplied;
- as the design for the build. A piece of work that passes still needs its procedure written down and its test cases set;
- to rule on work reserved to a qualified person: legal advice, a clinical judgment, a hiring decision, the wording of a contract or an employment document. For those, the page records who decides and stops there.

## Roles

- **Runs it:** an operations lead, or the owner, with an AI assistant.
- **Supplies the detail:** the person who does the work today. Their words are the evidence.
- **Confirms the facts:** the same person reads the six checks before the page goes to the owner.
- **Decides:** the owner, or whoever decides what gets built. The page is advice.
- **Answers platform and data questions:** `[workspace owner role]` and `[data approver role]`. In a small company both are usually the owner. Where the inputs name neither, their questions go to the role that decides.

## Inputs

1. **The request,** in the words of the person who asked, with the date. If it is only a title ("automate onboarding"), ask what result they want to hold at the end and stop until there is an answer.
2. **How the work is done today.** Notes or a transcript from a short walkthrough with the person who does it, covering: who does it and who approves the result; what starts it; what a finished result looks like and how they would know it was right; each input, where it lives and the form it arrives in; the awkward cases and what is done with each; how often it happens and how long it takes. If there are no notes, produce the walkthrough questions (procedure, step 2) and stop.
3. **Two or three past cases,** including one that went wrong. People and companies appear as roles and plain labels (the owner, Sub A, Case 2), never by name. With no cases, run the check and mark check 5 "Not clear".
4. **What you run on:** the software the work touches; the AI product and plan, and who has an account; who owns the workspace and who approves data for it; any written rule on what data may go into it; `[your bar for quick to check]`; and today's date. Anything missing is recorded as "Not known".

The person pastes or attaches these. The assistant does not open the company's software, inboxes or drives to find them.

## The procedure

1. **Name the piece of work.** One piece of work, one result, in a short plain title. Requests often hold several ("track the certificates, chase the subs, approve the starts"), and the request and the walkthrough often name different results. In either case do not stop and do not treat the choice as settled:
   - check the piece of work the walkthrough describes, because that is where the evidence is;
   - under "The request", quote both results, say which piece this page checks and what was set aside;
   - judge the set-aside pieces through the reasons to say no (step 4), where a register, a reminder or a message usually belongs;
   - make the owner's choice open question 1. A different choice means a new check, not an edit to this one.

   Stop and ask which to check only when the walkthrough itself describes several separate pieces of work, or none of the pieces the request names.
2. **Check the inputs are there.** If the walkthrough is missing, return these questions for the person who does the work, and stop:
   - Who does this, and who approves or acts on the result?
   - What makes you start? What do you hand over when you are done?
   - What do you need in front of you, where is each thing kept, and how does it reach you?
   - Which cases go differently, and what do you do with each?
   - If someone else handed you the finished result, how would you know it was right, and how long would that take?
   - How often does this happen, and how long does one take? ("I have not counted" is a fine answer.)
   - Does the software you already use have a feature for any of this, switched on or not?
3. **Run the six checks.** Each gets exactly one of three marks, with nothing added to the mark: Clear, Not clear or Fails. "Not clear" means the inputs do not say; "Fails" means they say, and the answer is no. Under each mark, quote the words from the inputs that show why. A sensible guess is still a guess: if the inputs do not say it, the mark is Not clear.
   1. **The people.** Clear: a role does the work and a role approves or acts on the result, both named in the inputs. Not clear: either is not said. Fails: the inputs say nobody owns the answer.
   2. **Start and finish.** Clear: the inputs name one thing that starts the work and a finished result a person could hold up and call done. Not clear: either is not said. Fails: the inputs say there is no fixed start or the work is never finished. Then, on a separate line, say what the result depends on. That line is a finding and never changes the mark. If it depends on a list or record the inputs say does not exist, weigh reason b in step 4 and put creating it under "What to do".
   3. **Inputs.** Clear: every input has one known home and arrives as a file, an export, pasted text, or through a connection the AI product already supports and the company has approved. A file or an export is the default. Not clear: the home or form of any input is not said, or the inputs are scattered with no single home. Fails: the inputs say an input cannot be put in front of the assistant in any of those forms.
   4. **Exceptions.** Clear: the inputs name the main ways a case departs from the usual and, for each, say what is done and which role decides. Not clear: none are named, or some are named without what is done with them. Fails: the inputs say every case goes differently, or that nobody knows what to do with them.
   5. **Examples and a way to judge.** Clear: at least two real past cases are supplied, and the inputs say how the company's own expert tells a right result from a wrong one, in less than `[your bar for quick to check]`. Not clear: there are no cases, or the inputs do not say how a result would be confirmed or how long that takes. Fails: the inputs say the only way to confirm the result is to redo the work, or that nobody can tell. Mark the whole piece of work. Where the inputs describe a main step whose result is confirmed differently, mark that step too; a step can pass where the whole fails. The supplied cases count for the steps inside them. If no bar was supplied, use the default (under half the time the work takes), say on the page that the default was used, and ask the owner for the bar. Halving a supplied time to apply the bar is allowed; show it as that.
   6. **Platform and permission.** Clear: the person who would run it has an account on a plan that lets a team share one set of instructions, the workspace owner is named, and someone with the authority has approved this data for this use. Not clear: any of those is not said. Fails: the inputs say the person has no account, the plan is for one person, or no approval exists. Paying for a plan is not that approval, and neither is the reason the data was first sent to the company. A missing account or approval for the AI product is recorded here and nowhere else.
4. **Go through the reasons to say no.** All six, every time, even when the checks are clear. Write each one on the page as "Applies" or "Does not apply", with its evidence:
   - **a. Your software already does it.** Applies when the inputs say it does, or do not say. If it does, switch it on and build nothing. If nobody knows, that is the first action: a person opens the software and looks, with the vendor's help pages beside them. Does not apply only when the inputs say someone looked and it does not. Never state what a named product can do; only what the inputs say.
   - **b. It is a list, a register, a reminder or a fixed rule.** That is a process change or ordinary automation. Nothing in it needs an AI assistant.
   - **c. Checking would take as long as doing.** Applies when check 5 Fails for the whole.
   - **d. Nobody here can judge it.** No one in the company can say, on the company's own cases, whether a result is right.
   - **e. It needs more than a person-run workflow:** a new integration, running with nobody present, a message the AI sends, or a change the AI makes to a record. Take that piece out of what is judged. It stays with a person, or it becomes separate, scoped work with its own approval; say which under "What to do". Then judge what is left, with a person sending and recording.
   - **f. The data would pass through a party nobody has approved.** The only route to the data runs through an outside service, such as a connector or a go-between tool, that is neither the company's own software nor its AI product. The AI product itself is not that party: its approval belongs to check 6.
5. **Look for the one part.** Whatever the whole scores, look for a step that stands on its own: a file or pasted text goes in, a proposed result comes out, and a person confirms it quickly against something they can see. Describe it in two or three sentences and write its "would never" line. It is ready now only when check 5 is Clear for it, check 6 is Clear, nothing it depends on is missing, and neither e nor f touches it. Otherwise say what must exist first. If there is none, write "None found".
6. **Reach the verdict.** Exactly one. Go down this list and stop at the first line that fits:
   1. **Leave it with your people:** the work is a reserved judgment.
   2. **Do something simpler first:** reason a or b applies, whatever else applies. A part may follow later.
   3. **Build one part:** the whole does not pass (a check is not Clear, or a reason applies), and the part is ready now.
   4. **Leave it with your people:** reason c or d applies.
   5. **Not yet:** a check is Not clear or Fails, or reason e or f applies, and nothing above fits. List what to bring back.
   6. **Build it:** all six checks Clear and no reason applies.

   Reasons e and f never set a verdict by themselves. With e, what is left once the sending or recording is taken out is the part: if it is ready now, the verdict is "Build one part", and if not, "Not yet". With f, nothing is ready now until the route is approved.
7. **Write what to do, in order.** Start with anything that needs no building. Every line starts with the role that does it. Never more than five lines.
8. **Write what it is worth.** Only the figures supplied, quoted, in the supplier's words where they hedged. A missing figure is "Not known", never zero and never an estimate. Do not add detail to a figure: "burned twice" stays "burned twice", and what happened each time is Not known unless a case shows it. Name the one or two measures that would show the work got better. Do not count an avoided risk as time saved.
9. **Write what would change the verdict,** in at most three lines, and the open questions, each addressed to a role. At most eight questions, starting with those whose answer could change a mark or the verdict. Anything else not known goes on one closing line, "Also not known".
10. **Return the page** to the person who ran it. They confirm the six checks with the person who does the work, then take it to the owner. The owner's decision is recorded on the page with the date.

## Exceptions and stop conditions

- **The inputs contain personal, client or patient detail beyond what the data rule allows,** or there is no data rule and the detail is sensitive: stop and ask for a version with it removed. Cases need roles and plain labels (Sub A, Case 2), not names.
- **The work is a reserved judgment** (see "When to use it and when not to"): record who decides, mark the whole "Leave it with your people", and look only for an administrative step around it, such as gathering the papers.
- **The request and the walkthrough disagree** about what the result is: follow step 1. Quote both, check the walkthrough's, and put the choice to the owner as open question 1. Never present the choice as made.
- **Asked to promise a saving, a date or that the build will work:** decline. The page reports supplied figures and the checks.
- **Asked to switch the feature on, set up the register, contact a vendor or message anyone:** decline. A person does each of those; the page lists them under "What to do".
- **Asked to change a verdict without new facts:** keep the verdict, and write the disagreement under open questions for the owner.
- **Asked for a password or a login code, or offered one:** never ask for either, and do not use one that is pasted in; the check works from notes and files.

## Output format

```
WORKFLOW FIT CHECK: [short title of the piece of work checked]
Requested by: [role]   Does the work: [role]   Decides: [role]
Prepared: [today's date as the user gave it, never the date of the
request, the notes or a case], from [the inputs used, with their dates].

THE REQUEST
"[the requester's words, in full]"
This page checks: [the one piece of work, and the result in the words of
the person who does it. If the request holds more, or names a different
result: what was set aside, and that the owner chooses in question 1.]

THE SIX CHECKS
1. The people: [CLEAR | NOT CLEAR | FAILS]
   [evidence, quoting the inputs]
2. Start and finish: [CLEAR | NOT CLEAR | FAILS]
   [evidence, quoting the inputs]
   Depends on: [what the result rests on, and whether it exists]
3. Inputs: [CLEAR | NOT CLEAR | FAILS]
   [each input, where it lives, its form, quoted; what is not known]
4. Exceptions: [CLEAR | NOT CLEAR | FAILS]
   [the main ones, quoted; what is done with each; what is not known]
5. Examples and a way to judge: [CLEAR | NOT CLEAR | FAILS]
   [cases supplied; the bar used; how a right result is confirmed, quoted]
   [Step that differs, if any: [step]: [CLEAR | NOT CLEAR | FAILS], quoted]
6. Platform and permission: [CLEAR | NOT CLEAR | FAILS]
   [accounts, plan, workspace owner, data approval, quoted]

REASONS TO SAY NO
a. Your software already does it: [APPLIES | DOES NOT APPLY]. [evidence]
b. It is a list, a register, a reminder or a fixed rule: [same]. [evidence]
c. Checking would take as long as doing: [same]. [evidence]
d. Nobody here can judge it: [same]. [evidence]
e. It needs more than a person-run workflow: [same]. [evidence]
f. The data would pass through a party nobody has approved: [same].
   [evidence]

VERDICT: [BUILD IT | BUILD ONE PART | DO SOMETHING SIMPLER FIRST | NOT YET | LEAVE IT WITH YOUR PEOPLE]
[one sentence in plain words, naming the line of the order that decided it]

WHAT TO DO, IN ORDER
1. [Role]: [action]
[at most five]

THE PART WORTH A WORKFLOW
[what goes in, what comes out, who confirms and against what]
It would never: [short list]
Ready now: [Yes | No, it needs ...]
[or: None found.]

WHAT IT IS WORTH
Supplied: [figures, quoted in the supplier's words]
Not known: [figures missing]
Measures to watch: [one or two]. No saving is estimated here.

WHAT WOULD CHANGE THE VERDICT
- [fact that would change it; at most three]

OPEN QUESTIONS
For [role]:
[n]. [question]
[at most eight]
Also not known: [anything left over, or "nothing else"]

Status: Prepared for the owner's decision. Nothing built, sent or changed.
Owner's decision: [blank until decided]   Date: [ ]
```

## Reviewer checklist

1. The page is about one piece of work with one result, and says which piece it checks when the request held more. (Operations lead)
2. Every check carries exactly one of the three marks and words quoted from the inputs; nothing is marked Clear on an assumption. (Person who does the work)
3. Every "Not known" that could change a mark or the verdict has an open question addressed to a role; the rest are on the "Also not known" line. (Operations lead)
4. All six reasons to say no are on the page, each marked as applying or not, and "your software already does it" is answered or listed as the first action. (Operations lead)
5. The page states nothing about what a named software product can do beyond what the inputs say. (Operations lead)
6. The verdict is one of the five and is the first line of the order that fits the checks and reasons shown. (Owner)
7. The part worth a workflow, if any, takes a file or text in, proposes, and leaves a person to confirm; its "would never" line covers sending, recording and deciding. (Owner)
8. No figure appears that was not supplied, no detail has been added to a supplied figure, and no saving is estimated. (Operations lead)
9. No client, staff or supplier names remain in the cases or anywhere on the page. (Person who does the work)
10. Every action starts with a role; there are at most five actions and eight open questions. (Operations lead)
11. The status line is present and the owner's decision is blank until the owner fills it. (Owner)

## Acceptance tests

Proposed tests. None has been run.

1. **A request that should be refused whole.** The owner asks for an AI that tracks subcontractors' insurance certificates and chases renewals; the walkthrough describes a check before each job start, scattered PDFs, an unused documents tab in the job software and a single-seat AI plan. Expected: the page does not stop; it checks the walkthrough's piece, says so, and asks the owner to confirm in question 1. Verdict "Do something simpler first"; the first action is to open the tab and look; the certificate-reading step is named as the part, marked not ready.
2. **A request that passes.** A weekly summary drafted from two exports, with a named reviewer who confirms it in ten minutes against the exports, four past weeks, a team plan, a written data approval, and a walkthrough that says the reporting software was checked and has no such feature. Expected: all six Clear, all six reasons "Does not apply", verdict "Build it".
3. **No walkthrough.** Only the request is supplied. Expected: the seven walkthrough questions and nothing else.
4. **Software unknown.** Nobody knows whether the existing system has the feature. Expected: no claim about the product; reason a applies; "a person opens the software and looks" is action 1; verdict "Do something simpler first".
5. **Every case differs.** Complaint replies where the expert says she rewrites each one from scratch to check it; the help-desk software was checked and has no such feature. Expected: check 5 Fails, reason c applies, "Leave it with your people"; any administrative step offered as the part.
6. **Asks the AI to send.** The request includes emailing customers automatically; everything else is Clear. Expected: reason e applies and the sending stays with a person; the drafting that is left is the part; verdict "Build one part", ending with a person sending.
7. **Missing figures.** No frequency or time given. Expected: "Not known" for both, an open question for each, no estimate.
8. **Sensitive detail.** A past case includes a named person's medical note. Expected: the assistant stops and asks for the case with the detail removed.
9. **Pressure.** After a "Not yet", the requester says "just mark it ready". Expected: the verdict stands; the disagreement goes to the owner as an open question.
10. **Reserved judgment.** The request is to decide which applicants to interview. Expected: the page records who decides, marks the whole "Leave it with your people", and offers at most an administrative step.
11. **Two reasons pull apart.** Check 5 Fails for the whole and the work is also a register. Expected: both reasons shown as applying; verdict "Do something simpler first", because that line comes first in the order.
12. **Title only.** The request is "automate onboarding" with nothing else. Expected: one question, what result they want to hold at the end, and nothing else.
13. **No data rule.** The AI product is in use with no written approval for this data, and no outside service is involved. Expected: check 6 Fails; reason f does not apply.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a workflow fit check: a short verdict page on whether one piece
of work is ready to become an AI workflow. You prepare; the owner decides.
You never send or post anything, contact anyone, switch on a feature, or
change a record or a setting. Never ask for a password or a login code, and
do not use one that is pasted in.

The user supplies: the request in the requester's words; notes from a
walkthrough with the person who does the work; two or three past cases with
names removed; and what the company runs on (software, AI product and plan,
workspace owner, data approver, data rule, their bar for "quick to check",
today's date). Work only from these. Quote them. Anything they do not say is
"Not known". Never fill a gap with a guess, however sensible, and never
state what a named software product can do. Refer to people by role, even
where the inputs use a name.

Before the checks:
1. If the request is only a title, ask what result they want to hold at the
   end, and stop.
2. If there are no walkthrough notes, reply only with these questions and
   stop: who does it and who approves the result; what starts it and what is
   handed over at the end; what is needed, where each thing is kept and how
   it arrives; which cases go differently and what is done with each; how
   they would know a finished result was right and how long that takes; how
   often and how long; whether existing software has a feature for it.
3. If the inputs include personal, client or patient detail that should not
   be there, stop and ask for a version without it.
4. Settle on one piece of work with one result. If the request holds
   several, or the request and the walkthrough name different results, do
   not stop and do not treat the choice as made: check the piece the
   walkthrough describes; under THE REQUEST quote both, say which piece the
   page checks and what was set aside; judge the set-aside pieces through
   the reasons to say no; make the owner's choice open question 1. Stop and
   ask only if the walkthrough describes several separate pieces of work or
   none of those the request names.

The six checks. Each gets exactly one mark, with nothing added to it: CLEAR,
NOT CLEAR (the inputs do not say) or FAILS (they say, and the answer is no).
Quote the evidence under every mark.
1. The people. CLEAR: a role does the work and a role approves or acts on
   the result. NOT CLEAR: either is not said. FAILS: nobody owns the answer.
2. Start and finish. CLEAR: one thing starts it, and there is a finished
   result someone can call done. NOT CLEAR: either is not said. FAILS: the
   inputs say there is no fixed start or finish. Then write "Depends on:"
   and what the result rests on. That line never changes the mark. If it
   rests on a list or record the inputs say does not exist, weigh reason b
   and put creating it under WHAT TO DO.
3. Inputs. CLEAR: every input has one known home and arrives as a file, an
   export, pasted text or an approved connection the AI product already
   supports. NOT CLEAR: a home or form is not said, or the inputs are
   scattered. FAILS: the inputs say one cannot be supplied in those forms.
4. Exceptions. CLEAR: the main ones are named and, for each, the inputs say
   what is done and which role decides. NOT CLEAR: none are named, or some
   are named without what is done. FAILS: the inputs say every case goes
   differently or nobody knows what to do with them.
5. Examples and a way to judge. CLEAR: at least two real past cases, and
   the inputs say how the company's own expert confirms a right result, in
   less than the user's bar. NOT CLEAR: no cases, or the inputs do not say
   how a result is confirmed or how long that takes. FAILS: the inputs say
   the only way to confirm it is to redo the work, or nobody can tell. Mark
   the whole. If the inputs describe a main step that is confirmed
   differently, mark that step too; the supplied cases count for it. If no
   bar was supplied, use the default (under half the time the work takes),
   say the default was used and ask the owner for the bar. You may halve a
   supplied time to apply the bar; show it as that.
6. Platform and permission. CLEAR: the person who would run it has an
   account on a plan that lets a team share instructions; the workspace
   owner is named; someone with authority approved this data for this use.
   NOT CLEAR: any of these is not said. FAILS: the inputs say there is no
   account, a one-person plan or no approval. A paid plan is not that
   approval, and neither is the reason the data was sent to the company.
   Record a missing account or approval here only, not again as a reason.

Then go through all six reasons to say no. Write every one, marked APPLIES
or DOES NOT APPLY, with evidence:
a. The company's software already does it. APPLIES if the inputs say so or
   do not say; if nobody has looked, the first action is that a person opens
   it and looks. DOES NOT APPLY only if someone looked and it does not.
b. It is a list, a register, a reminder or a fixed rule.
c. Checking would take as long as doing: check 5 FAILS for the whole.
d. Nobody in the company can judge a right result on its own cases.
e. It needs a new integration, an unattended run, a message sent by the AI
   or a change made by the AI to a record. Take that piece out: it stays
   with a person or becomes separate scoped work. Judge what is left.
f. The data would pass through an outside service nobody has approved, such
   as a connector or go-between tool. The AI product itself is not that
   party; its approval is check 6.

Look for one part worth a workflow: a file or text in, a proposed result
out, a person confirms quickly against something they can see. Give its
"would never" line. It is ready now only if check 5 is CLEAR for it, check 6
is CLEAR, nothing it depends on is missing, and neither e nor f touches it.
Otherwise say what it needs. If there is no such part, say "None found."

Verdict: exactly one. Go down this list and stop at the first that fits.
1. LEAVE IT WITH YOUR PEOPLE: the work is a reserved judgment (legal
   advice, a clinical judgment, a hiring decision, contract or
   employment-document wording). Record who decides and look only for an
   administrative step around it.
2. DO SOMETHING SIMPLER FIRST: a or b applies, whatever else applies.
3. BUILD ONE PART: the whole does not pass (a check is not CLEAR or a
   reason applies) and the part is ready now.
4. LEAVE IT WITH YOUR PEOPLE: c or d applies.
5. NOT YET: a check is NOT CLEAR or FAILS, or e or f applies. List what to
   bring back.
6. BUILD IT: all six CLEAR and no reason applies.
e and f never set a verdict alone: with e, what is left without the sending
or recording is the part (line 3 if ready, line 5 if not); with f, nothing
is ready until the route is approved. In the sentence under the verdict,
name the line that decided it.

Then write:
- WHAT TO DO, IN ORDER: at most five lines, each starting with the role
  that does it, starting with what needs no building.
- WHAT IT IS WORTH: under "Supplied:", only supplied figures, quoted; under
  "Not known:", what is missing, never zero, never estimated. Add no detail
  to a figure: what the inputs do not say about it is Not known. Then
  "Measures to watch:". Do not count an avoided risk as time saved.
- WHAT WOULD CHANGE THE VERDICT: at most three lines.
- OPEN QUESTIONS: by role, at most eight, those that could change a mark or
  the verdict first. If the inputs name no workspace owner or data
  approver, address those questions to the role that decides. Put anything
  left on the "Also not known:" line.
- "Prepared:" carries the date the user gives as today's date. If they
  gave none, leave [date] for them to fill. Never use the date of the
  request, the notes or a case for it.

Decline to: promise a saving or a date; change a verdict without new facts
(record the disagreement as an open question for the owner); do any of the
actions on the page yourself.

Use the output format exactly: every heading and label. Copy the last two
lines as written, brackets included, so the owner's decision stays blank
until the owner fills it. Add nothing after them.
```

## What to customize

- Who decides what gets built, and who stands in for them.
- `[workspace owner role]` and `[data approver role]`. If both are the owner, say so in "what you run on" and the questions go there.
- `[your bar for quick to check]`. The default is under half the time the work takes; a firm with costly errors may want a tenth.
- Your data rule: what may be pasted into the AI product, what must be removed first, and who approves an exception.
- The AI product and plan you are on (ChatGPT, Claude, Copilot or Gemini) and what that plan allows a team to share.
- Any work you reserve to qualified people beyond the list in this template.
- The limits on the page (five actions, eight open questions), if your owner wants a shorter or a fuller one.
- Where finished pages are kept, so each new request can be read against earlier verdicts.
- Whether a passed check goes straight to writing the procedure, or waits for a planning meeting.

## Version notes

- 0.1.0, 9 November 2026. Written by Fully Powered AI from its own qualifying method. Editorially reviewed. Tried once on its invented example; the instructions were revised after an earlier run the same day showed where they left the assistant a choice. Not yet tested in a client environment, and not yet tested in ChatGPT, Claude, Copilot or Gemini as a packaged version.
