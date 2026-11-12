# Process map and bottleneck review: an invented example

*Illustrative example with invented data.* The company is an invented 25-person maker of custom signs for shops and offices. Its people, process, figures and notes are all invented, and everyone is named by role. First come the inputs the operations manager supplied, in full. Then comes the review the workflow template should return from them, worked to the template's rules.

## The inputs

### 1. The process request

```
Process: Quote for a custom sign, from request to quote sent
Owner: Operations manager
Starts when: a customer request arrives by email or the website form
Ends when: the quote is sent to the customer
The number that should rise: quotes sent per week. Now 17 a week.
Arriving: 20 requests a week
Figures cover: the four weeks to 30 October 2026 (weekly averages)
Hours in a working day: 8
Time target: quote sent within 3 working days (24 working hours)
The step people complain about: the production check (step 4)
Prepared: 10 November 2026, by the operations manager
```

### 2. The step table (exported from the job system, then completed by hand)

```
step,name,role,wait_before_hours,work_hours,sent_back_to,sent_back_per_10,basis,notes
1,Log the request in the job system,Sales coordinator,1,0.3,,,measured,
2,Check drawings and sizes are complete; ask the customer for anything missing,Sales coordinator,2,0.5,,,measured,
3,Price materials and labour,Estimator,12,1.5,2,2,measured,Missing sizes found during pricing go back to the coordinator
4,"Check it can be made: fixings, sizes and site access",Production manager,8,0.5,3,3,estimated,Changes to fixings or sizes go back for repricing
5,Approve the price,General manager,18,0.2,,,estimated,
6,Write up and send the quote,Sales coordinator,3,0.5,,,measured,
```

### 3. Role hours

```
role,hours_per_week
Sales coordinator,36
Estimator,38
Production manager,15
General manager,6
```

### 4. Notes from the people who do the work

```
Sales coordinator, 3 November: About 2 in 10 requests come back from
pricing because the estimator finds a size or a drawing missing. I chase
the customer, then the request goes back into the pricing queue.

Estimator, 3 November: I work 42 hours a week. About 4 of them go on
questions from the workshop about jobs we have already won, so about 38
are left for quotes. When the production manager changes the fixings or
sizes, I price the whole job again.

Production manager, 4 November: I do quote checks when I am off the
floor, about 15 hours a week. Roughly 3 in 10 need a change to fixings
or sizes. That is a guess; I do not track it.

General manager, 4 November: I approve quotes on Tuesday and Friday
afternoons.
```

## The output

```
PROCESS MAP AND BOTTLENECK REVIEW: Quote for a custom sign, from request to quote sent

For: Operations manager. Prepared 10 November 2026 from the step table (6 steps), the role hours, notes from four roles. Figures cover the four weeks to 30 October 2026.
One item: starts when a customer request arrives by email or the website form; ends when the quote is sent to the customer.
The number that should rise: quotes sent per week, now 17 a week. Arriving: 20 a week. Time target: quote sent within 3 working days (24 working hours).

1. The map
Step 1. Log the request in the job system. Sales coordinator. Waits 1.0 h, then 0.3 h of work. Measured.
Step 2. Check drawings and sizes are complete; ask the customer for anything missing. Sales coordinator. Waits 2.0 h, then 0.5 h of work. Measured.
Step 3. Price materials and labour. Estimator. Waits 12.0 h, then 1.5 h of work. Hand-over from Sales coordinator. Sent back to step 2 in 2 of 10. Measured.
Step 4. Check it can be made: fixings, sizes and site access. Production manager. Waits 8.0 h, then 0.5 h of work. Hand-over from Estimator. Sent back to step 3 in 3 of 10. Estimated.
Step 5. Approve the price. General manager. Waits 18.0 h, then 0.2 h of work. Hand-over from Production manager. Estimated.
Step 6. Write up and send the quote. Sales coordinator. Waits 3.0 h, then 0.5 h of work. Hand-over from General manager. Measured.
Hand-overs: 4 (Sales coordinator to Estimator, Estimator to Production manager, Production manager to General manager, General manager to Sales coordinator). Send-backs: step 3 to step 2, 2 in 10, Estimator to Sales coordinator; step 4 to step 3, 3 in 10, Production manager to Estimator.
By role: Sales coordinator: steps 1, 2, 6. Estimator: step 3. Production manager: step 4. General manager: step 5.

2. Where the time goes
First pass: 47.5 h (5.9 working days): 3.5 h of work (7%), 44.0 h waiting (93%).
Send-backs add 9.8 h on average (step 3 to step 2: 0.2 x 16.0 h = 3.2 h; step 4 to step 3: 0.3 x 22.0 h = 6.6 h), 57.3 h (7.2 working days) in all.
Against the time target of 24.0 h: over by 23.5 h first pass and 33.3 h with send-backs.
Longest waits: before step 5 (18.0 h), before step 3 (12.0 h), before step 4 (8.0 h).

3. Load by role
Sales coordinator (steps 1, 2, 6): 28.0 h of work a week against 36.0 h given: 78%. Can finish about 25.7 a week.
Estimator (step 3): 45.0 h of work a week against 38.0 h given: 118%. Can finish about 16.9 a week.
Production manager (step 4): 13.0 h of work a week against 15.0 h given: 87%. Can finish about 23.1 a week.
General manager (step 5): 4.0 h of work a week against 6.0 h given: 67%. Can finish about 30.0 a week.
Send-backs counted: each one repeats the steps from where the item returns to where it was found, once. Expected work per item: step 2, 0.5 h x 1.20 = 0.60 h; step 3, 1.5 h x 1.50 = 2.25 h; step 4, 0.5 h x 1.30 = 0.65 h; all other steps as listed.

4. The constraint
Estimator, at step 3: 118%. More arrives than it can finish: 20 a week against about 16.9; the queue in front of step 3 grows by about 3.1 a week.
Check against what is finished: about 16.9 a week expected (the constraint's capacity, the smaller of the two) against 17 now: the figures agree.
The step people complain about: step 4 is not the constraint: the Production manager is at 87%, below the Estimator's 118%, so a faster check on its own would not raise quotes sent. Its send-backs do cost the Estimator time; see option 2.
The longest wait, before step 5, is not at the constraint: the General manager approves quotes on Tuesday and Friday afternoons, and is at 67%.

5. Try first at the constraint
1. Stop requests with missing sizes or drawings reaching pricing. Based on: step 3 sends 2 in 10 back to step 2, because the Estimator finds a size or a drawing missing. Returns up to about 6.0 h a week of Estimator time if the cause went away (20 x 0.2 x 1.5 h). Arithmetic on the supplied figures, not a forecast.
2. Stop the repricing caused by changes to fixings or sizes found at the make-it check (step 4). How is the owner's choice; the check itself stays. Based on: step 4 sends 3 in 10 back to step 3, and the Estimator prices the whole job again each time. Returns up to about 9.0 h a week of Estimator time if the cause went away (20 x 0.3 x 1.5 h). Arithmetic on the supplied figures, not a forecast.
3. Take the workshop's questions about jobs already won off the Estimator, to a role the owner chooses. Based on: the Estimator's note that about 4 of 42 hours go on those questions. Returns up to about 4.0 h a week of Estimator time if the cause went away (42.0 h - 38.0 h). Arithmetic on the supplied figures, not a forecast.

6. Then, if that is not enough
If the Estimator is still the most loaded role after these are tried and measured, adding capacity at step 3 is the owner's decision; adding it at any other step would not raise quotes sent per week.

7. Leave alone for now
Step 1 (Sales coordinator, 78%): faster logging would not raise quotes sent while the Estimator can finish only about 16.9 a week.
Step 2 (Sales coordinator, 78%): checking faster would not raise quotes sent. What it checks matters to option 1.
Step 4 (Production manager, 87%): a faster check would not raise quotes sent. What it finds matters to option 2.
Step 5 (General manager, 67%): the longest wait, but not a limit on quotes sent per week. It bears on the time target; see decision 2.
Step 6 (Sales coordinator, 78%): writing up faster would not raise quotes sent: at most about 16.9 a week reach it, and the Sales coordinator can finish about 25.7.

8. Where the bottleneck goes next
Production manager, at 87% today. Option 2 would also take the repeat checks off this role.

9. Figures to firm up
Step 4, wait 8.0 h, work 0.5 h and 3 in 10 sent back: estimated. The Production manager says the share is a guess; it sets the size of option 2 and the Production manager's load.
Step 5, wait 18.0 h: estimated. It is the longest wait and the basis of decision 2.
Estimator, 38.0 h given: estimated (role hours count as estimated unless said to be measured; the Estimator's note gives about 38). The 118% rests on it.

10. Decisions for the owner
1. Which of the three options to try first, who carries it, and when to run this review again with new figures.
2. Whether approval stays at two afternoons a week. The wait before step 5 is 18.0 h of the 44.0 h spent waiting on a first pass, and the time target is 24.0 h. It does not limit quotes sent per week.

11. Open questions
1. How long a customer usually takes to reply when a request goes back to step 2 for missing sizes, for the Sales coordinator. The notes give no reply time, so the review counts only the step's typical 2.0 h wait on the return trip.

Draft for the Operations manager. Nothing has been changed, assigned or sent. The owner decides what changes.
```
