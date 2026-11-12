# Software subscription and vendor spend review

Workflow template, version 0.1.0.

## Purpose

Turn a card statement or ledger export into one review of every subscription the business pays for, for the finance or operations lead: a register with the annual cost, owner, payment method and renewal date of each; spend by category; the annual renewals inside the look-ahead window and any month where several fall together; flags for unused seats, duplicate tools, changed charges, owners who have left, expense-claim payments, double charges and charges that stopped; consolidation candidates with the saving range before switching costs; the questions to put to owners; and the decisions for the decision-maker. The assistant reads no agreement. It prepares; it never cancels, downgrades, changes, pays, contacts a supplier or an owner, or edits a record.

## When to use it and when not to

Use it once a quarter, before budget season, when the card bill jumps, or after people who paid for tools have left. It covers every kind of subscription and recurring vendor charge: software, storage, hosting, media libraries, fonts, newsletters, memberships and services billed on a fixed cycle.

Do not use it:

- for a single supplier's renewal in depth, with use, invoices and service record. A vendor renewal review does that, one supplier at a time;
- to choose between quotes from competing suppliers. That is a separate piece of work;
- to find notice periods or renewal terms in an agreement, or to say what a clause means. The person supplies renewal dates as they know them, and questions of meaning go to whoever reviews contracts;
- for a budget, a forecast or a cash plan;
- for a security or data-protection assessment of any supplier.

## Roles

- **Runs it:** the finance lead, operations lead or office manager who sees the card statements and the ledger.
- **Supplies the owner notes:** the runner, from last year's register or from asking each team.
- **Answers the questions:** the owner named for each subscription, or the runner where none is on record.
- **Decides:** [your decision-maker], such as the owner, managing director or finance director.
- **Cancels, downgrades, moves a payment, claims a refund or talks to a supplier:** the people the business names. Always people.

## Inputs

1. **Settings,** typed by the runner: the company; today's date; the period start and end (at least three full calendar months; twelve is better); the currency; the runner's role; [your decision-maker]; [your look-ahead window] (default 90 calendar days); [your price-change threshold] (default 5%). If the period is shorter than three months, stop and ask for a longer export.
2. **Spend export,** one row per charge, from the card statement, the ledger or both, with these default headers: `date` (YYYY-MM-DD), `payee`, `description`, `amount` (a refund or credit is negative), `paid_by`. `paid_by` is one of `company card`, `bill pay`, `direct debit`, `expense claim` or `personal card`. If it is missing, stop: there is nothing to review.
3. **Owner notes** (optional), one row per subscription, with these default headers: `payee`, `what_it_is_for`, `category`, `owner`, `cycle` (`monthly`, `annual` or blank), `renewal_date`, `annual_cost`, `seats_paid`, `seats_used`, `critical` (`yes`, `no` or blank: yes means the work stops without it), `fallback` (`yes`, `no` or blank: whether a written fallback exists), `switching_cost`. Any cell may be blank. If the notes are missing, write "owner notes not supplied" under Not supplied or not checked, and every subscription has no owner on record.
4. **Leavers list** (optional), with these default headers: `owner` (spelled as in the owner notes) and `left_on`. If it is missing, write "leavers list not supplied" and raise no owner-has-left flag.

Headers are matched ignoring case. If a required header is not there, stop and ask which column holds that information; never guess, and never use another column in its place. If a `paid_by`, `cycle`, `critical` or `fallback` value is not one of the allowed values, stop and ask about that row.

The assistant works from files the person supplies. It needs no connection to the card provider, the bank or the accounting system, and it never asks for a password, a login code or a full card number.

## The procedure

1. **Check the inputs.** One currency throughout. Every charge date reads as a date and falls inside the period. Two rows with the same date, payee and amount: stop and ask whether they are one charge counted twice (for example in both the card and the ledger export) or two real charges; never drop either on your own. Payees are grouped by their name exactly as written, ignoring case and surrounding spaces; two different names are never merged, even when they look like the same supplier.
2. **Class each payee** from the months in which it has a positive charge.
   - **Monthly:** charged in three or more calendar months, each month after the first following the one before without a gap.
   - **Irregular:** charged in three or more calendar months with a gap between them.
   - **Annual:** charged in one or two months, where a charge's description contains "annual", "yearly" or "12 months", or the owner notes give `cycle` as annual.
   - **Not classed:** every other payee charged in one or two months.
   - **From the owner notes only:** a payee on the notes with no charge in the period. If its `cycle` is annual, it goes on the register as "annual, no charge in the period". Otherwise it is flagged "on the owner notes, no charge in the period" and stays off the register.
   - If the owner notes give `cycle` as annual for a payee the charges class as monthly, or the other way round, stop and ask.
   Refunds and credits (negative amounts) are listed against their payee, counted in what was paid, and do not make a month count as charged.
3. **Annual cost.** For each monthly payee, look at the months with exactly one charge and count the steps where the amount differs from the month before. No step or one step: the annual cost is the latest month's charge times twelve ("latest charge x 12"); if the latest month has more than one charge, stop and ask which one is the regular charge. Two or more steps: mark it "varies", and the annual cost is the average of those single-charge months times twelve ("average x 12"). For an annual payee, the annual cost is its latest charge ("as charged"). For an annual payee from the notes only, it is `annual_cost` ("as supplied") or "not known". For an irregular payee, the annual cost is "not known"; show what was paid in the period.
4. **Charges stopped.** A monthly payee whose latest charge falls before the period's last month is listed under "Charges stopped" at the end of the register, with its last charge and the months without one. Its annual cost is not counted in any total.
5. **Renewal dates,** for annual payees only: `renewal_date` from the notes ("as supplied"); otherwise the latest charge date plus twelve months ("estimated from the charge"); otherwise none. Monthly payees get no renewal date.
6. **The register.** One line per subscription, highest annual cost first, ties in payee order, those with an unknown annual cost after the rest, and the charges-stopped lines at the very end. Each line: payee; what it is for (from the notes, or from the charge description marked "from the description"); category (from the notes, or one you suggest from the description, marked "suggested"; a suggested category reuses a category name already in the owner notes wherever one fits, so tools that do the same job land in the same category); owner (from the notes, or "none on record"); how it is paid (every `paid_by` value seen, latest first, or "no charge in the period" for a line from the notes only); the cycle and charge details; the annual cost and its basis; the renewal date with its basis, for annual lines; seats used of seats paid, when both are supplied.
7. **Summary.** The count of register lines by class, with the charges-stopped count. The total annual cost of the active lines with a known cost, and that total divided by twelve. What was paid in the period across every row of the export, split by `paid_by`, and how much of it went to payees not classed. Then the count of renewals in the window, of flag lines and of consolidation candidates.
8. **Spend by category.** For each category among the active lines with a known cost: the total annual cost, its share of the total as a whole percent (each share is rounded on its own, so the shares may add to 99 or 101), and the number of subscriptions. Mark a category "includes suggested" when any line in it has a suggested category. Highest first.
9. **Renewals.** Every annual renewal date from today to today plus [your look-ahead window], soonest first, with its weekday, the days from today, the payee, the annual cost, the basis of the date and the owner. Then renewal clusters: each calendar month in the twelve months from today's month in which three or more annual renewal dates fall.
10. **Flags.** One line per finding, grouped by kind, printing only kinds that have a finding:
    - **No owner on record:** an active register line with no owner.
    - **Owner has left:** the owner appears on the leavers list; give the leaving date and the number and total of charges dated after it.
    - **Paid on an expense claim or personal card:** any charge paid that way; give the count and the total in the period.
    - **Charge changed by [your price-change threshold] or more:** a monthly payee with exactly one step whose change is at least the threshold; give both amounts, the month of the change with its year, and the change as a percent to one decimal place. The export does not show whether the change came from price, seats or use, and the review never says which.
    - **Unused seats:** `seats_used` below `seats_paid`; give the unused count and the annual cost times unused divided by paid, to the cent, labelled "at the average cost per paid seat".
    - **More than one charge in a month:** a monthly payee with two or more charges in one month; give each date and amount.
    - **Charges stopped:** as in step 4.
    - **On the owner notes, no charge in the period:** as in step 2, non-annual payees only.
    - **Supplied renewal date already passed:** a `renewal_date` before today.
11. **Consolidation candidates.** Every category, among active register lines, that holds two or more subscriptions. For each: the members with their annual cost and owner; the combined annual cost; the range a business would save by keeping one, from the combined cost less the dearest member to the combined cost less the cheapest, marked "before switching costs, depending on which is kept"; each member's switching cost as supplied, or "not known". When any member has `critical` yes and `fallback` not yes, add: "Critical with no written fallback: [payee]. Write a fallback before any consolidation." When the category is suggested for any member, say so and ask for it to be confirmed. Never say which member to keep; a member with an unknown annual cost is listed but left out of the arithmetic.
12. **Not classed.** Each not-classed payee with its descriptions, dates and amounts, for the runner to mark.
13. **Questions.** Write a question only where a fact calls for it, each addressed to the owner on record or, where there is none, to the runner, and each with its fact: one per unused-seats flag (can the seats be reduced: at the next charge for a monthly line, at the renewal for an annual line); one per changed charge (was it a price rise, or more seats or use); one per month with more than one charge (was the extra charge expected); one per stopped subscription (was it cancelled, or is it paid some other way now); one per subscription with no owner (who uses it, and is it still needed); one per consolidation candidate, to the owners of its members (do the tools do the same work, and what would moving to one involve); one per payee on the notes with no charge (is it paid some other way); one per supplied renewal date already passed (what the correct date is); and one covering the not-classed payees (are any of them subscriptions). The runner decides whether to ask them; the assistant contacts no one.
14. **Decisions for [your decision-maker].** In this order: one per renewal in the window (renew, change or end, with the date, the days left and the cost, the note that notice terms were not supplied and should be confirmed with whoever holds the agreement, and that a vendor renewal review can prepare it in depth); one per owner who has left (who takes the subscription over, or whether it ends); one per subscription paid on an expense claim or personal card (whether it moves to a company payment method, once its question is answered); one per consolidation candidate (whether to ask the owners to look into moving to one tool, and, where a critical member has no written fallback, whether to have one written first and by whom). Write each as a question with its facts. Recommend nothing unless [your decision-maker] asks; if asked, add one suggestion for that decision, labelled as made at their request, with the facts for it and the facts against it.
15. **Not supplied or not checked.** Always first: no agreement, order form or terms were read; renewal dates are as supplied or estimated from the charge history; notice terms are not known. Then: seats, owners and whether a subscription is critical are as supplied in the owner notes; annual subscriptions charged before the period start appear only if they are on the owner notes; payees with different names were not merged. Then each input that was missing.
16. **Return the review** to the runner, in the output format and its fixed order, adding no section or commentary beyond it. Where a section has nothing in it, print the word the format gives for that case. Nothing goes to an owner, a supplier or the decision-maker from the assistant.

## Exceptions and stop conditions

- **Spend export missing, or a period shorter than three months:** stop and ask.
- **A required header does not match, or a value is not one of the allowed values:** stop and ask; never guess.
- **A row dated outside the period, or more than one currency:** stop and ask.
- **Two rows with the same date, payee and amount:** stop and ask whether they are one charge counted twice.
- **The owner notes and the charges disagree on whether a payee is monthly or annual:** stop and ask.
- **The latest month of a monthly payee has more than one charge:** stop and ask which is the regular charge.
- **Asked to cancel, downgrade, change a payment method, claim a refund, email an owner or a supplier, or update the ledger or the register:** decline and name the role that does it.
- **The person pastes an agreement and asks for the renewal or notice date:** decline to read it for dates or meaning; ask for the dates as they know them or as whoever reviews contracts confirms them.
- **Asked which tool to keep or what to cut:** recommend nothing unless the decision-maker asks; then follow step 14.
- **The inputs contain a full card number, a password, a login code or bank details:** do not repeat them; tell the person to remove them from the source. The last four digits of a card may be shown as supplied.
- **The export names individual employees on expense claims:** report the payee and the totals; do not repeat the employees' names.

## Output format

```
SOFTWARE SUBSCRIPTION AND VENDOR SPEND REVIEW: [company], [period start] to [period end]

For: [runner role]. Decisions by: [decision-maker role]. Prepared [weekday date] from [the inputs used, with row counts].

SUMMARY
Register: [n] subscriptions: [n] monthly ([n] with charges stopped), [n] annual charged in the period, [n] annual from the owner notes[, [n] irregular].
Annual cost of the [n] active subscriptions with a known cost: [amount] ([amount] a month).
Paid in the period: [amount] ([paid_by] [amount], largest first; ...), of which [amount] to payees not classed.
Renewals in the next [n] days: [n]. Flags: [n]. Consolidation candidates: [n].

REGISTER (by annual cost, highest first)
[n]. [Payee]: [what it is for][ (from the description)]. Category: [category][ (suggested)]. Owner: [owner / none on record]. Paid by: [paid_by, latest first / no charge in the period]. [Monthly, [amount] a month, last charged [date] / Monthly, varies, average [amount] a month over [n] months, last charged [date] / Annual, charged [date] / Annual, no charge in the period / Irregular, charged in [months], [amount] paid in the period]. Annual cost: [amount] ([latest charge x 12 / average x 12 / as charged / as supplied]) / not known. [Renews: [weekday date], [as supplied / estimated from the charge].] [Seats: [used] of [paid] used.]
Charges stopped: [payee]: [what it is for]. Last charged [date], [amount]; no charge in [months]. Annual cost not counted.
/ No subscriptions found.

SPEND BY CATEGORY (active, known cost; shares rounded to whole percent)
[Category][ (includes suggested)]: [amount], [n]%, [n] subscription(s).
/ None.

RENEWALS IN THE NEXT [n] DAYS (annual subscriptions, to [weekday date])
[Weekday date], [n] days from today: [payee], [amount] a year, renewal date [as supplied / estimated from the charge]. Owner: [owner / none on record].
/ None.

RENEWAL CLUSTERS (months with three or more annual renewals, [month year] to [month year])
[Month year]: [payee, date]; ...
/ None.

FLAGS: [n]
No owner on record: [payee]; ...
Owner has left: [payee]: [owner], left [date]; charged since: [n] charges, [amount].
Paid on an expense claim or personal card: [payee]: [n] charges, [amount] in the period.
Charge changed by [threshold]% or more: [payee]: [amount] to [amount] from [month year] ([+/-n.n]%).
Unused seats: [payee]: [unused] of [paid] unused; about [amount] a year at the average cost per paid seat.
More than one charge in a month: [payee]: [month year]: [amount] on [date] and [amount] on [date].
Charges stopped: [payee]: last charged [date].
On the owner notes, no charge in the period: [payee].
Supplied renewal date already passed: [payee]: [date].
/ None.

CONSOLIDATION CANDIDATES: [n]
[n]. [Category][ (suggested for [payee]; to confirm)]: [payee] ([amount] a year, owner [owner / none on record]); ... Combined: [amount] a year. Keeping one would save between [amount] and [amount] a year, before switching costs, depending on which is kept. Switching cost, as supplied: [payee] [amount / not known]; ... [Critical with no written fallback: [payee]. Write a fallback before any consolidation.]
/ None.

NOT CLASSED (one or two months, no annual marker)
[Payee]: "[description]", [date], [amount]; ...
/ None.

QUESTIONS: [n], for the [runner role] to decide whether to ask
[n]. To the [owner or runner role]: [the fact]. [The question.]
/ None.

DECISIONS FOR THE [DECISION-MAKER ROLE]: [n]
[n]. [The facts.] [The question.]
[Suggestion, made at the [decision-maker role]'s request: [one option], because [facts]. Against it: [facts].]
/ None.

NOT SUPPLIED OR NOT CHECKED
No agreement, order form or terms were read; renewal dates are as supplied or estimated from the charge history, and notice terms are not known. Seats, owners and whether a subscription is critical are as supplied in the owner notes. Annual subscriptions charged before [period start] appear only if they are on the owner notes. Payees with different names were not merged. [Each input that was missing.]

Every figure traces to the inputs supplied for [company] on [date]. Nothing has been cancelled, changed, paid or sent.
```

## Reviewer checklist

1. Every row of the export is counted once, and what was paid in the period adds up by payment method. (Runner)
2. Every payee is classed by the rule in step 2, and no two payee names were merged. (Runner)
3. Every annual cost recomputes from the charges with its stated basis, and the summary total equals the sum of the active register lines with a known cost. (Finance lead)
4. Every renewal date shows its basis, every weekday and day count is right, and nothing says what an agreement allows. (Runner)
5. Every flag and every consolidation saving range recomputes from the export and the owner notes. (Finance lead)
6. Every question names who it is for and rests on a fact on the page. (Runner)
7. No decision recommends a tool to keep or cut unless the decision-maker asked. (Decision-maker)
8. The review keeps the fixed section order, prints the empty-section word where a section is empty, and adds nothing beyond the output format. (Runner)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary quarter.** Four months of charges for nine monthly payees, two annual and two one-off. Expected: nine monthly, two annual charged in the period, two not classed; totals recompute.
2. **Header does not match.** The export's columns are `posted`, `merchant`, `memo`, `value`, `card`. Expected: stops and asks which column holds which; drafts nothing.
3. **Same charge twice.** The same date, payee and amount appear once with `company card` and once with `bill pay`. Expected: stops and asks whether it is one charge in both exports.
4. **Price step.** $300 a month for two months, then $345. Expected: annual cost $4,140 (latest charge x 12); flag "Charge changed by 5% or more", +15.0% from the month of the change; one question to the owner; nothing said about why.
5. **Usage-billed charge.** $118.40, $131.20, $126.00, $140.40. Expected: "varies", average $129.00 a month, annual cost $1,548.00 (average x 12); no changed-charge flag.
6. **Double charge.** Two $400 charges in August from a monthly payee, one charge in each other month. Expected: annual cost $4,800; flag with both dates; one question; nothing claimed.
7. **Owner has left.** Owner on the leavers list, left 31 August, two $480 charges since. Expected: flag "charged since: 2 charges, $960.00"; one decision on who takes it over.
8. **Annual renewal before the period.** On the owner notes as annual, renewal 1 December, annual cost $1,200, no charge in the period. Expected: on the register as "annual, no charge in the period", renewal as supplied, listed under renewals in the window, one decision.
9. **Two tools in one category, one critical without a fallback.** Expected: one consolidation candidate with the saving range and the line "Write a fallback before any consolidation"; no member named as the one to keep.
10. **Asked to cancel.** "Cancel the stock image subscription for me." Expected: declines; names the role that cancels; nothing drafted to the supplier.
11. **Asked what to cut.** The decision-maker asks which tools to drop. Expected: one suggestion per decision asked about, labelled as made at their request, with facts for and against.
12. **Card number in the export.** A description holds a full card number. Expected: not repeated; the person is told to remove it from the source.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a review of every subscription and recurring vendor charge
a business pays for, from a spend export, for its finance or
operations lead. You prepare; people decide. You never cancel,
downgrade, change a payment method, pay, claim a refund, contact an
owner or a supplier, send anything or change any record. You never
read an agreement for dates or say what a clause means. You never ask
for a password, a login code or a full card number, and you need no
access to any system.

The user will supply: settings (company, today's date, period start
and end of at least three full months, currency, runner role,
decision-maker, look-ahead window default 90 days, price-change
threshold default 5%); a spend export (date, payee, description,
amount, paid_by, where paid_by is company card, bill pay, direct
debit, expense claim or personal card); owner notes (payee,
what_it_is_for, category, owner, cycle, renewal_date, annual_cost,
seats_paid, seats_used, critical, fallback, switching_cost); a
leavers list (owner, left_on).

Stop and ask when: the export is missing or the period is under three
months; a header does not match (match ignoring case; ask which
column holds it; never guess); a paid_by, cycle, critical or
fallback value is not an allowed one; a row
falls outside the period; there is more than one currency; two rows
share date, payee and amount; the notes and the charges disagree on
monthly or annual; the latest month of a monthly payee has more than
one charge. If the notes or leavers list are missing, say so in NOT
SUPPLIED OR NOT CHECKED and continue.

1. Group rows by payee name as written, ignoring case; never merge
   two names. Class each payee by the months with a positive charge:
   monthly (3+ months, no gap); irregular (3+ months with a gap);
   annual (1 or 2 months and a description with "annual", "yearly"
   or "12 months", or notes cycle annual); not classed (other 1 or 2
   month payees). A notes payee with no charge: on the register if
   annual, else flagged "on the owner notes, no charge in the
   period". Negative amounts are refunds: count them in what was
   paid; they do not make a month charged.
2. Annual cost. Monthly: compare months with exactly one charge; 0 or
   1 change, latest charge x 12; 2+ changes, "varies", average of
   those months x 12. Annual: latest charge (as charged), or notes
   annual_cost (as supplied), or not known. Irregular: not known.
   A monthly payee not charged in the period's last month goes under
   "Charges stopped" at the end of the register and is not counted.
3. Renewal dates, annual only: notes renewal_date (as supplied), else
   latest charge plus 12 months (estimated from the charge).
4. Register, highest annual cost first, ties in payee order, unknown
   costs after, stopped last. Category from the notes, or suggested
   from the description and marked "suggested"; a suggested category
   reuses a category name already in the notes wherever one fits.
   Owner from the notes or "none on record".
5. Summary; spend by category with whole-percent shares, each rounded
   on its own (they may not add to 100); renewals
   from today to today plus the window, with weekday and days from
   today; months in the next 12 with 3+ annual renewals.
6. Flags, printing only kinds with a finding: no owner on record;
   owner has left (date, charges and total since); paid on an expense
   claim or personal card; charge changed by the threshold or more
   (one change only: both amounts, month, percent to one decimal;
   never say why); unused seats (annual cost x unused / paid, "at the
   average cost per paid seat"); more than one charge in a month;
   charges stopped; on the notes with no charge (non-annual only);
   supplied renewal date already passed.
7. Consolidation candidates: each category with 2+ active lines;
   members, combined cost, saving range from combined minus the
   dearest to combined minus the cheapest, "before switching costs,
   depending on which is kept"; switching costs as supplied or "not
   known"; if a member is critical without a written fallback, say a
   fallback should be written before any consolidation; where a
   member's category is suggested, say so and ask for it to be
   confirmed. A member with an unknown annual cost is listed but left
   out of the arithmetic. Never say which to keep.
8. Not classed payees with descriptions, dates and amounts.
9. Questions, each with its fact, to the owner or else the runner:
   unused seats (reduce at the next charge for a monthly line, at the
   renewal for an annual line); changed charge (price, or more seats
   or use); extra charge in a month; stopped
   charges; no owner; each consolidation candidate; notes payee with
   no charge; renewal date passed; one for the not classed payees.
10. Decisions for the decision-maker, as questions with facts: each
   renewal in the window (renew, change or end; notice terms not
   supplied, to confirm with whoever holds the agreement; a vendor
   renewal review can prepare it); each owner who has left; each
   expense-claim or personal-card subscription (move it to a company
   payment method, once its question is answered); each consolidation
   candidate, with the fallback question where it applies.
   Recommend nothing unless the decision-maker asks; then give one
   suggestion per decision asked about, labelled as made at their
   request, with facts for and against.
11. NOT SUPPLIED OR NOT CHECKED opens with: "No agreement, order form
   or terms were read; renewal dates are as supplied or estimated
   from the charge history, and notice terms are not known."
12. Use the output format exactly, in its fixed order. Print the
   empty-section word where a section is empty. End with: "Every
   figure traces to the inputs supplied for [company] on [date].
   Nothing has been cancelled, changed, paid or sent."

If asked to cancel, downgrade, move a payment, claim a refund or
contact anyone, decline and name the role that does it. Do not repeat
a full card number, password, login code or bank details; tell the
user to remove them. The last four digits of a card may be shown as
supplied. Do not repeat employees' names from expense
claims. Recompute every figure before you return the review.
```

## What to customize

- [your decision-maker], and who keeps the register between reviews.
- [your look-ahead window]: how far ahead annual renewals are listed. The default is 90 calendar days.
- [your price-change threshold]: the size of change worth a flag. The default is 5%.
- The period you review, and which ledger accounts or card categories you export so the file holds subscriptions rather than every purchase.
- The column headers your card and ledger exports actually use, and the `paid_by` names your business uses.
- Your category names, so tools that do the same job share one category in the owner notes.
- Whether an owner-has-left or expense-claim flag should also go straight to a named person after the review is approved.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 9 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried once on its invented example in Claude on 9 November 2026; the trial record is published with it. Small edits made to the procedure, the pasted instructions and the example after an independent review have not been run again; the trial record lists them. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
