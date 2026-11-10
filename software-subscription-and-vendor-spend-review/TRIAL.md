# Software subscription and vendor spend review: tried on its example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID `claude-sonnet-5-5`)
- **Date:** 2026-11-09

The inputs were the invented example in `public/example.md` (Agency W, with suppliers called Vendor A to Vendor Q): its settings, spend export (40 rows), owner notes (12 rows) and leavers list (1 row). No client data was used. The model did not write the template. It read the template and the example's inputs, followed the instruction block and the output format, produced the review, and only then read the example's published output and the reviewer checklist to compare. The figures were recomputed with a short script after the review was drafted. Nothing was executed from the template itself.

## What came out

The review came out whole, in the fixed order, with no stop and no question put back to the person. Its substantial parts:

- **Summary:** 13 subscriptions (9 monthly, 1 of them with charges stopped; 2 annual charged in the period; 2 annual from the owner notes). Annual cost of the 12 active subscriptions with a known cost: \$41,448.00 (\$3,454.00 a month). Paid in the period: \$19,411.00 (company card \$10,831.00; bill pay \$6,000.00; direct debit \$2,280.00; expense claim \$300.00), of which \$238.00 to payees not classed. Renewals in the next 90 days: 2. Flags: 8. Consolidation candidates: 2.
- **Register, highest first:** Vendor A \$10,080.00; K \$6,000.00; E \$5,760.00; F \$4,800.00; C \$4,140.00; B \$2,640.00; L \$2,400.00; G \$1,548.00 (varies, average x 12); M \$1,200.00; J \$1,080.00; D \$900.00; N \$900.00. Vendor H listed last under charges stopped, its annual cost not counted.
- **Spend by category:** design software \$12,720.00 (31%); CRM \$6,000.00 (14%); file storage \$5,760.00 (14%); video meetings \$5,040.00 (12%, includes suggested); project management \$4,800.00 (12%); email marketing \$2,400.00 (6%); website hosting \$1,548.00 (4%); website tools \$1,200.00 (3%); accounting \$1,080.00 (3%); fonts \$900.00 (2%).
- **Renewals in the next 90 days (to Sunday 7 February 2027):** Vendor M on Tuesday 1 December 2026 (22 days) and Vendor N on Friday 15 January 2027 (67 days), both dates as supplied. No renewal clusters.
- **Flags (8):** no owner on record (Vendor D); owner has left (Vendor E, Account director, left 31 August 2026, 2 charges and \$960.00 since); expense claim (Vendor D, 4 charges, \$300.00); charge changed (Vendor C, \$300.00 to \$345.00 from September 2026, +15.0%); unused seats (Vendor A, 3 of 14, about \$2,160.00 a year; Vendor K, 4 of 10, about \$2,400.00 a year); more than one charge in a month (Vendor F, August 2026, 11 and 25 August); charges stopped (Vendor H, last charged 15 September 2026).
- **Consolidation candidates (2):** design software (Vendors A and B, combined \$12,720.00, saving between \$2,640.00 and \$10,080.00 before switching costs, with the line that Vendor A is critical with no written fallback); video meetings (Vendors C and D, combined \$5,040.00, saving between \$900.00 and \$4,140.00, category suggested for Vendor D, to confirm). No tool was named as the one to keep.
- **Not classed:** Vendor P (\$199.00, 9 September 2026) and Vendor Q (\$39.00, 12 October 2026).
- **Questions (9)** and **decisions for the Managing director (6):** two renewals, the departed owner's subscription, the expense-claim subscription, and the two consolidation candidates. No recommendation was made.
- **Not supplied or not checked:** the fixed opening sentence, the notes about seats, owners and annual charges before the period, and that different payee names were not merged. No input was missing.
- The closing line read: "Every figure traces to the inputs supplied for Agency W on 9 November 2026. Nothing has been cancelled, changed, paid or sent."

## What was observed

Every required section was produced, in order, and every figure matched the example's output: the register order, all annual costs and bases, the totals, the category shares, the renewal dates, weekdays and day counts, the flags, the saving ranges and the counts of questions (9) and decisions (6). The checklist items on counting rows, classing payees, recomputing annual costs, renewal bases, flags, savings, questions and decisions were all met. The review was not told to stop for anything and nothing in the inputs triggered a stop condition.

Where the output differed from the published example, the differences were in wording only:

- The example's summary uses bullets; the output format shows plain lines. The model followed the format.
- Question 1 (Vendor A seats) asked whether seats could be reduced "at the next charge or at renewal", following step 13; the example asks only about the next monthly charge. Question 2 (Vendor K) used the same wording for the same reason; the example asks about setting the renewal at fewer users.
- Question 3 (Vendor C) asked whether the rise was a price rise, or more seats or use; the example says "more hosts or use". The inputs give no hosts for Vendor C (only Vendor D's description mentions hosts), so that word in the example is not in the inputs.
- Decision 6 and Question 8 name the runner as standing in for Vendor D's missing owner; the model did this by reading step 13 ("or, where there is none, to the runner"), and the example does the same.
- Small phrasing choices differ (for example the stopped-charges line and the "from the description" mark on Vendor D).

Anything in either output not in the inputs: the one found was "hosts" for Vendor C in the example's question 3. The suggested category "video meetings" for Vendor D is marked as suggested in both outputs.

Where the template was ambiguous and the model had to choose:

1. **Date and money format.** The output format shows `[date]` and `[amount]` with no pattern for ordinary dates or the currency symbol. The model wrote "3 October 2026" and "\$840.00", as the example does.
2. **Suggested category names.** Step 6 says to suggest a category "from the description" but not to reuse a category name already in the owner notes. The model reused "video meetings" for Vendor D. A different name would have hidden the consolidation candidate.
3. **Whole-percent shares add to 101%.** Rounding each share gives a total of 101. The template does not say what to do, and the model left each share as rounded.
4. **Notes-only annual payees and the "on the owner notes, no charge" flag.** Step 10 lists that flag "as in step 2", and step 2 flags only non-annual notes payees. The model read it that way, so Vendors M and N were on the register but not flagged. A reader could expect them flagged.
5. **Questions for a consolidation candidate with no owner.** Step 13 says to ask "the owners of its members" and to use the runner where there is none. The model named both owners for each candidate, with the runner standing in for Vendor D.
6. **Unused-seat questions on a monthly line and an annual line.** Step 13 gives "at the next charge or at renewal" for both. It is not said which applies to which.
7. **Ordering of questions, flags and candidates.** The format gives the order of kinds but not the order within a kind; the model used register order.
8. **Counting.** The summary's register count (13) includes the charges-stopped line while the annual-cost count (12) excludes it. The format makes this clear but a reader may need a second look.
9. **Empty `critical` and `fallback`.** The notes allow blank values; the template says a critical member with `fallback` not yes triggers the line, and the model treated a blank fallback on a critical line as "not yes". No such case arose in the example.

Shortcomings: the instruction block repeats most of the template but leaves out a few small rules (the stop for an invalid `paid_by`, `cycle`, `critical` or `fallback` value is covered only as "a value is not an allowed one", and the rule that the last four digits of a card may be shown is missing). Both were added after the run; see "Changed after this run, and not run again" below. The acceptance tests in the template were not run in this trial; only the one example was.

This is one run, by one model, on an invented example. It shows the instructions can be followed to the stated output on these inputs. It does not show how the template behaves on a real export, in other products or on other models.

## Changed after this run, and not run again

Changed on 9 November 2026 after an independent review of the published template, and not run again. The output and the observations above are as recorded and describe the template and the example as they stood at the run:

- **Suggested category names** (ambiguity 2). The procedure and the pasted instructions now say a suggested category reuses a category name already in the owner notes wherever one fits. This is the reading this run used for Vendor D ("video meetings").
- **Rounded shares** (ambiguity 3). The procedure and the pasted instructions now say each share is rounded on its own, so the shares may not add to 100. The example's shares, which add to 101, are unchanged.
- **Unused-seat questions** (ambiguity 6). The procedure and the pasted instructions now say a monthly line's seats are reduced at the next charge and an annual line's at the renewal. This run asked "at the next charge or at renewal" for both; the example already asked about the next monthly charge for Vendor A and the renewal for Vendor K.
- **The pasted instructions** now also carry three rules that were only in the procedure: register ties go in payee order, the expense-claim decision waits on its question, and the last four digits of a card may be shown as supplied. They also name the four fields (`paid_by`, `cycle`, `critical`, `fallback`) whose values must be allowed ones.
- **The example's question 3** now says "more seats or use", not "more hosts or use", as this run's question 3 did. Its question 2 now speaks of seats rather than users, matching the register line.
- **The example's summary** is now plain lines, as the output format shows and as this run wrote it.
- **Notes-only annual payees** (ambiguity 4). Step 10 and the pasted instructions now say the "on the owner notes, no charge in the period" flag is for non-annual payees only. This is the reading this run used: Vendors M and N were on the register and not flagged.
- **Smaller wording fixes.** Step 1 now says every charge date falls inside the period, so owner-notes renewal dates and leaving dates are not caught by it. The NOT CLASSED heading no longer says "not on the notes", since a payee on the notes as monthly with only one or two months of charges is not classed too. The pasted instructions now also say that a consolidation member with an unknown annual cost is listed but left out of the arithmetic, and that a suggested category is to be confirmed. None of these touched the example's inputs or figures.
- **The example's output** now opens with a line saying it is formatted for reading, with bold headings and lists, where the plain-text format has plain lines; its NOT CLASSED heading follows the template's; and its decision 6 says "(no owner on record for Vendor D)", as its question 8 does, in place of a gloss about who answers for Vendor D.
