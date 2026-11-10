# Business insurance renewal review: tried on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs were the invented example in [example.md](example.md): Business C, Broker B and Insurers K, M and N. No client data was used. This model did not write the template. It followed the instruction block and the output format in the template and used only the inputs section of the example. It read the example's own output only after it had produced its pack.

## Inputs used

All eight inputs under "The inputs" in [example.md](example.md): the renewal facts, the four expiring schedules, the three sets of renewal terms, the business changes table and the one other change, the two new contracts, the loss run of four claims, the business's own record of five rows and the managing director's one question.

## What came out

The pack came out in the template's fixed order with every part present. It is shown here in full, in the template's plain output format.

```
BUSINESS INSURANCE RENEWAL PACK: Business C, renewing Friday 1 January 2027

For: Operations lead. Decided by: Managing director, with Broker B. Prepared Tuesday 10 November 2026 from 4 expiring schedules, 3 sets of renewal terms, 5 business-change rows and 1 other change, 2 contract rows, a loss run of 4 claims, 5 rows of the business's own record and 1 question from the managing director.

DATES
Renewal date: Friday 1 January 2027, 52 days from today.
Questions to the broker by: Friday 11 December 2026, 31 days from today (21 days before the renewal date).
Status: ON TRACK.
Policies ending on another date: Commercial auto, Insurer K, ends Monday 15 March 2027, 125 days from today.

THE POLICIES: 4 expiring, 3 with renewal terms supplied
1. COMMERCIAL GENERAL LIABILITY. Insurer: Insurer K → Insurer K (SAME). Policy GL-4471. Period: 1 January 2026 to 1 January 2027 → 1 January 2027 to 1 January 2028 (starts the day the expiring period ends).
- Each occurrence limit: $1,000,000 → $1,000,000. SAME
- General aggregate limit: $2,000,000 → $2,000,000. SAME
- Products-completed operations aggregate limit: $2,000,000 → $2,000,000. SAME
- Deductible, each claim: $2,500 → $5,000. CHANGED, +$2,500 (+100.0%)
- Endorsement, Blanket additional insured where required by written contract: listed → listed. SAME
- Exclusion, Fungi or bacteria exclusion: none → listed. NEW
- Annual premium: $9,400 → $11,280. CHANGED, +$1,880 (+20.0%)
Changes marked: 3.
2. COMMERCIAL PROPERTY. Insurer: Insurer M → Insurer M (SAME). Policy PR-2290. Period: 1 January 2026 to 1 January 2027 → 1 January 2027 to 1 January 2028 (starts the day the expiring period ends).
- Premises: Location 1, the main yard and workshop → Location 1, the main yard and workshop. SAME
- Contents limit: $350,000 → $350,000. SAME
- Tools and equipment limit: $120,000 → $120,000. SAME
- Business income limit: $250,000 → $250,000. SAME
- Deductible, each loss: $1,000 → $1,000. SAME
- Annual premium: $3,150 → $3,465. CHANGED, +$315 (+10.0%)
Changes marked: 1.
3. WORKERS COMPENSATION AND EMPLOYERS LIABILITY. Insurer: Insurer N → Insurer N (SAME). Policy WC-8812. Period: 1 January 2026 to 1 January 2027 → 1 January 2027 to 1 January 2028 (starts the day the expiring period ends).
- Workers compensation: statutory → statutory. SAME
- Employers liability, each accident: $500,000 → $1,000,000. CHANGED, +$500,000 (+100.0%)
- Employers liability, disease each employee: $500,000 → $500,000. SAME
- Premium (printed as "Annual premium, estimated"): $38,000 → $41,800. CHANGED, +$3,800 (+10.0%)
Changes marked: 2.
4. COMMERCIAL AUTO. Insurer: Insurer K. Policy CA-3305. Period: 15 March 2026 to 15 March 2027. Renewal terms not supplied.
- Vehicles scheduled: 9 vans.
- Combined single limit, each accident: $1,000,000.
- Physical damage deductible, each vehicle: $1,000.
- Annual premium: $14,600.
Expiring premiums: $65,150, 4 policies. For the 3 policies with renewal terms: expiring $50,550, renewal $56,545, +$5,995 (+11.9%).

WHAT CHANGED IN THE BUSINESS
Employees: 38 → 46 (from payroll system headcount), +8 (+21.1%). Given to the insurer: 46, in renewal application (equals the figure now).
Annual revenue: $4,600,000 → $5,400,000 (from accounts for the last 12 months), +$800,000 (+17.4%). Given to the insurer: $5,000,000, in renewal application (differs by $400,000).
Annual payroll: $1,900,000 → $2,300,000 (from payroll for the last 12 months), +$400,000 (+21.1%). Given to the insurer: $2,050,000, in renewal application (differs by $250,000).
Sites: 1 → 2 (from lease register), +1 (+100.0%). Given to the insurer: 1, in renewal application (differs by 1).
Vehicles: 9 → 12 (from fleet list), +3 (+33.3%). Given to the insurer: not supplied.
Other changes: Since June 2026 the business cleans gutters and repairs roofs on two-storey buildings, working at height from ladders and towers.

NEW CONTRACTS THAT ASK FOR COVER
Customer P facilities maintenance agreement, signed 14 April 2026, as read by Operations director: asks for Each occurrence limit of $2,000,000 on Commercial general liability; the renewal schedule prints $1,000,000, so the figure asked for is higher than the figure printed. Other requirement: Customer P named as additional insured. Whether the request is met is for Broker B to confirm.
Customer Q reactive repairs agreement, signed 1 July 2026, as read by Operations director: asks for Combined single limit, each accident of $1,000,000 on Commercial auto; the expiring schedule prints $1,000,000 (no renewal terms were supplied), so the figure asked for is equal to the figure printed. Other requirement: none. Whether the request is met is for Broker B to confirm.

CLAIMS HISTORY: loss run dated 31 October 2026, policy years 2024 to 2026
Commercial general liability: 2 claims, 1 open. Paid $7,400, reserved $15,000, incurred $22,400.
Commercial auto: 1 claim, 0 open. Paid $3,850, reserved $0, incurred $3,850.
Workers compensation: 1 claim, 0 open. Paid $4,300, reserved $0, incurred $4,300.
All lines: 4 claims, 1 open. Paid $15,550, reserved $15,000, incurred $30,550.
Largest incurred: K-GL-1307, Commercial general liability, 21 August 2026, $16,200, open.
Open claims: K-GL-1307, Commercial general liability, 21 August 2026, a visitor tripped over a cable at a customer site, reserved $15,000.
In the business's own record, not in the loss run: 2 October 2026, Commercial property, break-in at the yard; two power tools taken.

QUESTIONS FOR THE BROKER: 15, for the Operations lead to decide whether to send
1. Premiums rise on all three policies with renewal terms: general liability $9,400 to $11,280 (+$1,880, +20.0%), property $3,150 to $3,465 (+$315, +10.0%), workers compensation and employers liability, estimated, $38,000 to $41,800 (+$3,800, +10.0%); together $50,550 to $56,545 (+$5,995, +11.9%). What accounts for each premium change?
2. The general liability deductible for each claim moves from $2,500 to $5,000 (+$2,500, +100.0%). What is the reason for the change?
3. A "Fungi or bacteria exclusion" is listed on the general liability renewal terms and not on the expiring schedule. What is it, and what is the reason it has been added?
4. Employers liability, each accident, moves from $500,000 to $1,000,000 (+$500,000, +100.0%) on the workers compensation renewal terms. What is the reason for the change?
5. The commercial auto policy CA-3305 ends Monday 15 March 2027, 125 days from today, not on the renewal date, and no renewal terms were supplied. When will its renewal terms be issued, and how will its renewal be handled beside the other policies?
6. Annual revenue is $5,400,000 now (from the accounts for the last 12 months) against $5,000,000 given in the renewal application, a difference of $400,000. How should the current figure reach the insurer, and by when?
7. Annual payroll is $2,300,000 now (from payroll for the last 12 months) against $2,050,000 given in the renewal application, a difference of $250,000. How should the current figure reach the insurer, and by when?
8. Sites are 2 now (from the lease register) against 1 given in the renewal application; the property schedule, expiring and renewal, prints Location 1 only. How should the second site be put to the insurer, and by when?
9. Vehicles are 12 now (from the fleet list), up 3 (+33.3%) from 9, and no figure given to the insurer was supplied; the expiring commercial auto schedule prints 9 vans. How should the current number reach the insurer, and by when?
10. Since June 2026 the business cleans gutters and repairs roofs on two-storey buildings, working at height from ladders and towers. How should this change be put to the insurers, and by when?
11. Customer P facilities maintenance agreement (signed 14 April 2026, read by the Operations director) asks for an each occurrence limit of $2,000,000 on Commercial general liability; the renewal schedule prints $1,000,000. It also asks for Customer P to be named as additional insured. Is the request met?
12. Customer Q reactive repairs agreement (signed 1 July 2026, read by the Operations director) asks for a combined single limit, each accident, of $1,000,000 on Commercial auto; the expiring schedule prints $1,000,000. It asks for nothing else. Is the request met?
13. Claim K-GL-1307 (Commercial general liability, 21 August 2026) is open, with $1,200 paid and $15,000 reserved. What is its current status, and what is expected next?
14. The business's own record lists a break-in at the yard on 2 October 2026 (Commercial property, two power tools taken, no claim number), and the loss run dated 31 October 2026 does not list it. Do the broker or insurer have any record of it?
15. Can the premiums be paid in instalments, and would that cost more?

DECISIONS FOR THE MANAGING DIRECTOR: 3
1. Whether the questions go to Broker B by Friday 11 December 2026, and who sends them.
2. Who gives Broker B the current figures for annual revenue, annual payroll, sites and vehicles, and by when.
3. The renewal: renew on the terms offered, ask the broker for changes or ask the broker to look for other terms, for Commercial general liability, Commercial property and Workers compensation and employers liability, decided with Broker B before Friday 1 January 2027.

NOT SUPPLIED OR NOT CHECKED
The policy wordings were not read or interpreted; nothing in this pack says whether any loss is or is not covered; figures are as printed on the schedules supplied by the Operations lead. Renewal terms for Commercial auto (CA-3305) were not supplied. The Workers compensation and employers liability schedule, expiring and renewal, shows no deductible. No figure given to the insurer was supplied for vehicles.

Every figure traces to the documents and files supplied for Business C on 10 November 2026. Nothing has been sent, accepted, bound, paid, reported or changed.
```

## What was observed

- **Every required part was produced.** All eight sections of the format appeared in order. Nothing in the inputs made the template stop. Nothing was refused, because nothing in the inputs asked for advice, sending or a coverage opinion.
- **The arithmetic agreed with the published example.** Dates and weekdays (renewal Friday 1 January 2027 in 52 days, questions by Friday 11 December 2026 in 31 days, status ON TRACK, auto ending Monday 15 March 2027 in 125 days), the marks, every difference and percent, the premium totals ($65,150 expiring; $50,550 to $56,545, +$5,995, +11.9%) and the claims totals ($30,550 incurred, largest K-GL-1307 at $16,200) matched.
- **The person's name and the injury detail in the workers compensation claim did not appear.** The claim is only counted in the totals.
- **No fact outside the inputs appeared in this run's pack.** Every figure and name traces to the inputs. One thing goes slightly past what the template instructs: question 8 notes that the property schedule prints Location 1 only, and question 9 notes that the auto schedule prints 9 vans. Both are printed facts, but the template does not say to set business figures beside schedule items.

### Differences from the published example

- **Line titles.** This run kept the titles as the schedules print them, in capitals ("COMMERCIAL GENERAL LIABILITY"). The example writes them in sentence case. The template says to keep names as printed.
- **Premium label.** This run wrote "Annual premium" where the schedule prints that, and the printed label for the estimated premium. The example writes "Premium" throughout.
- **Prepared line.** The example names the date of the broker's renewal summary; this run gave counts only.
- **Question wording.** The example's questions are more probing. Question 2 asks what the premium would be with the deductible kept at $2,500. Question 3 asks "What does it change for Business C?" Question 4 asks how much of the premium change comes from the limit. Question 11 asks what meeting the request "would take and cost". Question 13 asks whether the insurer has taken the open claim into account in the renewal terms. Questions 6, 7 and 10 in the example ask whether the insurers "should have" a figure. This run asked how and by when the figure reaches the insurer. Question 1 here also gives each money change.
- **Decisions.** The example's decisions carry more facts (the figures that differ, and the premium totals). This run wrote each decision as a short question, as the format shows.
- **Markdown.** The example uses bold and bullets; this run used the plain text of the format block.

### Where the instructions were ambiguous, or the template could be better

- **Question wording that may drift toward meaning.** The template says "plain questions only: no view on what the answer should be, no statement about what a policy covers". It does not say whether a question may ask the broker what a clause means. The example's question 3 ("What does it change for Business C?") and question 11 ("what would it take and cost") sit close to that line. This run asked what the exclusion is and why it was added. A reviewer should decide whether asking is allowed.
- **Questions that invite a view.** "Should the insurers have the current figure?" asks the broker for a recommendation. The template says a question asking for advice joins the broker's list, so it is permitted, but the rule on "no view on the answer" is easy to read both ways.
- **Premium label.** The format says to show a printed premium name "where the schedule names it otherwise". It does not say whether "Annual premium" counts as the plain premium or as a different name. This run and the example chose differently.
- **Weekdays.** Step 2 says "write every date with its weekday", but the format shows weekdays only on the dates in DATES, the decisions and the title. Dates in contracts and claims were written without them, in this run and in the example. The rule should name which dates need one.
- **Cross-checking business figures against schedules.** Nothing says whether to set sites against scheduled premises or vehicles against scheduled vans. The example does it, and so did this run.
- **Decisions "with its facts".** Step 9 says to write each decision as a question with its facts, but the format line for each decision has few. This run followed the format; the example followed step 9.
- **Claims line names.** The loss run says "Workers compensation", but the policy is titled "Workers compensation and employers liability". The template does not say whether to match claim lines to policy lines. This run grouped claims by the loss run's wording and did not link them to policies.
- **"Each schedule that shows no ... deductible".** It is unclear whether this covers the renewal terms as well as the expiring schedules. This run named both for the workers compensation policy.
- **Missing figure given to the insurer for vehicles.** Step 10 lists missing inputs and schedules but not a blank `given_to_insurer`. This run added a line for it; the example did not.
- **Case-insensitive match of line names.** Step 5 matches a contract's `line` to a schedule, but not explicitly ignoring case or the capitalised schedule titles. This run matched them ignoring case.
- **Version notes are out of date.** The template's last section still says "Not yet tried on its invented example in a named AI product". This trial changes that, and the line should be updated by whoever owns the template.
- **Acceptance tests.** This run covers the ordinary case only (test 1's dates, and in passing tests 7, 8 and 13, whose situations are in the inputs). The refusal and stop tests (6, 9 to 12) were not run.

### Not shown

This was one run, by one model, on an invented example. It shows the template can be followed to a complete pack on these inputs. It does not show how it behaves on a client's real documents or in other AI products, and it is not a test for any client.

## Edits made after this run

The template, the example and the profile were revised on 10 November 2026, after this run and after an independent review. These edits have not been run again. Most settle points listed above; two of them change what a run on these inputs prints, as noted.

- **Weekdays.** The procedure and the pasted instructions now say which dates carry a weekday: those in the title, the prepared line's date, DATES and the decisions; other dates need none. The reviewer checklist was worded to match. This run's dates already fit.
- **Premium label.** "Premium" and "Annual premium" both print as "Premium"; the printed name is added in brackets only when it says more, such as "Annual premium, estimated". This changes the run's output: its "Annual premium" lines for general liability, property and auto would read "Premium" on the revised template. Its estimated-premium line already fits.
- **Decisions.** The output format's decision lines are now questions carrying their facts (the number of questions, the business figures now and as given to the insurer, and the renewal against the expiring premiums), as step 9 and the example already had them. This changes the run's output: its three decisions are short statements without those facts.
- **Business figures beside the schedules.** A question about a business figure now gives what a schedule prints for the same thing, such as the premises or vehicles scheduled. This run's questions 8 and 9 already did this.
- **Missing items.** NOT SUPPLIED OR NOT CHECKED now names a schedule that shows no deductible (or another item) whether it is the expiring schedule, the renewal terms or both, and lists each business figure with no figure given to the insurer. This run already did both. The example now adds the vehicles line, so the difference noted above no longer applies.
- **Matching.** Claims are grouped by line as the loss run names it, not matched to a policy's title, and a contract's `line` and `item` are matched ignoring case. This run already did both.
- **Question wording in the example.** The example's questions 5 to 8 were reworded so they no longer suggest an answer: question 5 asks how the auto renewal will be handled beside the others, and questions 6 to 8 ask what, if anything, the insurers need and by when. The example's decision 2 and its last section were brought into line with the revised format. This run's questions 5 to 9 were already neutral in this way.
- **Pasted instructions.** Two over-long lines were rewrapped. The block now carries the procedure's instruction to shorten a claim description that carries a name or health detail to the event, and its step for NOT SUPPLIED OR NOT CHECKED now names the output format's statement that figures are as printed on the schedules supplied, which this run already printed. The words of the block are otherwise as this run used them, apart from the points above. This run's output was not affected.
- **Status lines.** The template's version notes, its acceptance-tests note and the profile now say that this run took place and that the refusal and stop cases were not reached.

No recorded output or observation above was changed.
