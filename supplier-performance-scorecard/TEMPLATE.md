# Supplier performance scorecard

Capability template, version 0.1.0.

## Purpose

Score each key supplier for one quarter from the business's own purchase-order and receiving exports, for the buyer or operations lead: on-time delivery, fill rate, defects and returns, price against the agreed-price list, and how quickly orders are confirmed. Each score carries its target, the change since last quarter's scorecard, and the order lines behind it, so every number can be checked. Spend and dependence on the supplier are shown side by side and never blended, the points to raise at the next supplier review are written from the evidence, and the decisions a person has to make (a warning, a change of tier, a move away from the supplier, or finding an alternative) are written as questions with their facts. The assistant prepares; it never sends anything to a supplier, changes a supplier's tier or any record, or decides anything it lists.

## When to use it and when not to

Use it once a quarter, after the quarter's deliveries are received and booked, and in time for the quarterly supplier reviews. It covers the suppliers the business names as key, whether they supply materials, packaging, components or goods for resale.

Do not use it:

- to decide whether to renew one supplier's contract. A vendor renewal review does that, for one supplier at a time;
- to plan how a whole spend category should be bought. A category sourcing plan does that;
- to write to a supplier about a problem. A supplier issue notice prepares that for approval, using the points this scorecard raises;
- to see where the money goes across all suppliers. A supplier spend analysis does that from the accounts-payable export;
- to read a contract for prices, service levels or exit terms, or to say what a clause means;
- to judge a supplier's finances, certifications or sanctions status. Those need sources this scorecard does not read.

## Roles

- **Runs it:** the buyer, purchasing lead or operations lead who can export purchase orders and receipts.
- **Keeps the key supplier list and the agreed-price list:** the runner, with whoever holds each supplier relationship.
- **Raises the points at the supplier review:** the owner named for each supplier on the key supplier list.
- **Decides any warning, change of tier, move away from a supplier, or search for an alternative:** [your decision-maker], such as the owner, managing director or operations director.
- **Talks to suppliers, sends anything, changes a supplier's tier or any record:** the people the business names. Always people.

## Inputs

1. **Settings,** typed by the runner: the company; today's date, which is also the date the exports were run; the quarter scored, with its start and end dates; the currency, as its code (such as USD) and, if the runner wishes, the symbol to print; the runner's role; [your decision-maker]; [your targets] (defaults: on time 95% of lines, fill rate 98% of units, defects and returns at most 1.0% of units, price within terms 100% of lines, orders confirmed within the window 90%); [your grace days], how many days after the due date still count as on time (default 0); [your price tolerance], how far above the agreed price still counts as within terms (default 0%); [your confirmation window], in calendar days (default 2); [your minimum to score] (default 5 lines, or 3 orders for confirmations); [your trend step], the change that counts as better or worse (default 2.0 percentage points, and 0.5 for defects and returns); [your tier review count] (default 3); [your exit count] (default 3). If the quarter or today's date is missing, stop and ask.
2. **Key supplier list,** one row per supplier to be scored, with these default headers: `supplier`, `category`, `tier` (the business's own standing for the supplier, such as preferred, approved or on watch), `sole_source` (yes or no: is this the only supplier the business can buy this from today?), `alternative` (a supplier already named as able to take the work over, or blank), `owner` (the role that holds the relationship). If the list is missing, stop: the scorecard does not choose which suppliers are key.
3. **Purchase-order lines export,** one row per order line, covering every line due in the quarter and every order placed in it, with these default headers: `po`, `line`, `supplier`, `item`, `order_date`, `due_date` (the delivery date on the order), `qty_ordered`, `unit_price` (the price on the order), `confirmed_date` (the date the supplier confirmed the order; blank if it never did). If missing, stop.
4. **Receiving export,** one row per receipt, with these default headers: `receipt`, `po`, `line`, `received_date`, `qty_received` (every unit that arrived, accepted or not), `qty_rejected` (units refused or set aside at receiving as damaged, wrong or below specification), `reject_reason`. If missing, stop.
5. **Returns export** (optional), one row per return to the supplier, with these default headers: `return`, `po`, `line`, `return_date`, `qty_returned`, `reason`. If missing, defects and returns counts rejections at receiving only, and the scorecard says so.
6. **Agreed-price list** (optional), with these default headers: `supplier`, `item`, `agreed_price`, `valid_from`, `valid_to`. If missing, price against agreed terms is not scored, and the scorecard says so.
7. **Last quarter's scorecard figures** (optional), one row per supplier, with these default headers: `supplier`, `quarter`, `on_time`, `fill_rate`, `defects_returns`, `price_within_terms`, `confirmed_in_window`, each a percentage to one decimal place or "not scored". If missing, there is no trend, and no warning or exit question, because both need two quarters; the scorecard says so.

Headers are matched ignoring case. If a header is not found, stop and ask which column holds that information; never guess, and never use another column in its place. Supplier names are matched across the inputs ignoring case, punctuation and extra spaces; any other difference means a different supplier.

The assistant works from files the person supplies. It needs no connection to the purchasing or accounting system and never asks for a password, a login code or bank details.

## The procedure

1. **Check the rows.** One currency throughout. Every date reads as a date. Every quantity and price is a number, and no quantity is negative. No order line (`po` and `line`) appears twice. No receipt is dated before its order date or after today. No `qty_rejected` is larger than the `qty_received` on the same receipt. No line has more returned than received. No `confirmed_date` is before its order date. If any check fails, stop and ask about the rows concerned. Never correct or drop a row on your own.
2. **Set the scope.** A line is in the quarter when its due date falls inside the quarter. An order is in the quarter when its order date falls inside it. Receipts and returns count when they belong to a line in the quarter and are dated up to today, even if after the quarter end. Suppliers in the exports that are not on the key supplier list are listed with their number of lines and not scored; their receipts and returns are simply left out, neither used nor listed. Receipts or returns whose order line is not in the export are listed and not used.
3. **Spend.** For each key supplier: quantity ordered times unit price, summed over its lines in the quarter, with the number of lines. Give each supplier's share of the total spend with all key suppliers, to one decimal place, rounded so the shares add up to 100.0: round each share down to one decimal place, then add 0.1 to the shares with the largest remainders, one each, until they do. Spend is shown next to dependence and never used to judge it.
4. **Dependence.** For each key supplier, copy `sole_source`, `alternative` and `tier` from the list exactly as written. A sole source with a small share of spend is shown exactly as a sole source; a small spend never lowers it.
5. **On time.** Each line in the quarter is delivered on the date of its last receipt. It is on time when that date is no later than the due date plus [your grace days]. A line with nothing received by today is late, shown as "nothing received by [today]". Score: lines on time out of lines in the quarter. List every late line with its due date, its delivery date and the days late, counted in calendar days after the due date; where the line came in parts, give each part.
6. **Fill rate.** Units received out of units ordered on the lines in the quarter. A line that received more than ordered counts at its ordered quantity and is listed under the checks. Rejected units count as received here; they are counted under defects and returns. List every line that received less than ordered.
7. **Defects and returns.** Units rejected at receiving plus units returned, out of units received (actual, not capped), on the lines in the quarter. List each receipt or return behind the figure, with its order line, units and reason: receipts first, in order of receipt number, then returns, in order of return number. A lower figure is better, and the target is a limit.
8. **Price against agreed terms.** For each line in the quarter, find the agreed price for the same supplier and item, valid on the order date. The line is within terms when its unit price is no more than the agreed price plus [your price tolerance]. Score: lines within terms out of lines with an agreed price. For each line above, give the item, the price on the order, the agreed price, the units received and the amount above the agreed price (the difference times units received), then the total. Lines with no agreed price are listed under the checks and not counted.
9. **Orders confirmed in time.** Each order in the quarter, once per `po`, using the latest `confirmed_date` on its lines. It is confirmed in time when that date is no more than [your confirmation window] calendar days after the order date. An order with any line unconfirmed (its `confirmed_date` blank) is not confirmed. Score: orders confirmed in time out of orders placed. List every order confirmed late, with its days, or not confirmed.
10. **Too few to score.** A measure with fewer lines, or for confirmations fewer orders, than [your minimum to score] is "too few to score" with its count. Its evidence is still listed, but it has no target status, no trend and no point to raise, and it is left out of the count of measures scored.
11. **Status.** Every figure is printed to one decimal place, and the status is judged on the figure as printed: meets or below for a target, within or above for the defects and returns limit. Last quarter's figures are judged against this quarter's targets.
12. **Trend.** Compare each scored figure with last quarter's. A change smaller than [your trend step] is "level"; otherwise "better" or "worse", where a fall in defects and returns is better. With no figure for last quarter, or "not scored" there, write "no comparison".
13. **Points to raise at the next review,** per supplier, in the order of the measures. One point for each scored measure below target, and one for each scored measure within target that got worse, each with its figure, its target, last quarter's figure and the order lines or receipts behind it. For price, one point is written whenever any line is above the agreed price, with the total amount, and it takes the place of any below-target or worse point for price. Below target, the point ends "Ask for the cause and what will change."; within target but worse, "Ask what changed."; the price point, "Ask how it will be corrected." With nothing to raise, write the "none" line from the output format.
14. **Decisions for [your decision-maker].** Write a decision only when its trigger is met, each as its facts, then the question:
    - **Warning:** a measure below target this quarter and last quarter. Ask whether the owner should give the supplier a formal written warning about that measure; a supplier issue notice can prepare it for approval. One decision per measure.
    - **Tier:** [your tier review count] or more scored measures below target this quarter. Ask whether the supplier should stay at its current tier.
    - **Exit:** [your exit count] or more measures below target in both quarters, and an alternative is named on the list. Ask whether the owner should prepare a plan to move the category from the supplier to the named alternative.
    - **Alternative:** the exit trigger is met but no alternative is named, or the supplier is a sole source with no alternative named, whatever its spend or scores. Ask whether the owner should be asked to find and qualify an alternative. No alternative named means no exit question, whatever the scores. One alternative decision per supplier at most, carrying every fact that triggered it.
    List decisions in the order the suppliers appear in the scorecard, and for each supplier in the order warning, tier, exit, alternative. Recommend nothing unless [your decision-maker] asks; if asked, add one suggestion for that decision, labelled as made at their request, with the facts for it and the facts against it.
15. **Not supplied or not checked.** Always first: no contract, invoice or quality certificate was read, so price is the price on the order compared with the agreed-price list as supplied; punctuality is read from the due date each order carries, and whether that date matched when the goods were really wanted is not known; defects are units rejected or returned as recorded, and nothing was inspected. Then each optional input that was missing, with what it removed from the scorecard.
16. **Return the scorecard** to the runner in the output format, in its fixed order, adding no section or commentary beyond it. Suppliers appear in order of spend, highest first, ties by name. Write amounts with two decimals and the currency's symbol: the one the settings give or, failing that, one beyond doubt for the code (such as $ for USD); when unsure, write the code itself in place of a symbol. Write unit prices as on the order. Use thousands separators on amounts and on unit counts. Write dates as day and month, with the month in full; the dates in the heading, the "Prepared" date and the date in the closing line also carry the year. Use the singular for one. Nothing goes to a supplier, an owner or the decision-maker from the assistant.

## Exceptions and stop conditions

- **Settings without the quarter or today's date, or no key supplier list, purchase-order export or receiving export:** stop and ask.
- **A header not found:** stop and ask which column holds it; never guess.
- **A row that fails a check in step 1:** stop and ask about those rows; never correct or drop a row.
- **A key supplier with no lines in the quarter:** show it with "no lines due in the quarter" in place of the measures, keep its dependence line, and raise the alternative decision if its trigger is met.
- **Asked to score a supplier on something not in the exports,** such as how pleasant they are to deal with or a rumour about their finances: decline; add it to the points only if the person supplies it as their own note, marked as such.
- **Asked whether to warn, re-tier or leave a supplier:** recommend nothing unless the decision-maker asks; then follow step 14. Raise no exit question for a supplier with no named alternative.
- **Asked to send the scorecard or the points to a supplier, change a tier, put a supplier on hold, or change a record:** decline and name the role that does it.
- **The person pastes a contract and asks for service levels, prices or exit terms:** decline to read it for terms or meaning; ask for the agreed prices and targets as the business holds them.
- **The inputs contain bank details, a password or a login code:** do not repeat them; tell the person to remove them from the source.
- **A reject reason or note names an individual employee:** refer to it by its receipt or return number only.

## Output format

```
SUPPLIER PERFORMANCE SCORECARD: [company], [quarter label] ([start] to [end])

For: [runner role]. Decisions by: [decision-maker role]. Prepared [weekday date] from [inputs used, with row counts]. Compared with: [quarter label] scorecard. / Compared with: no previous scorecard supplied; no trend, warning or exit question.
Targets: on time [n]% (grace [n] days); fill rate [n]%; defects and returns at most [n.n]%; price within terms [n]% of lines (tolerance [n]%); orders confirmed within [n] days [n]%. Scored with at least [n] lines, or [n] orders for confirmations. Level means a change under [n.n] points ([n.n] for defects and returns).

CHECKS
Rows read: key suppliers [n]; order lines [n]; receipts [n]; returns [n] / returns not supplied; agreed prices [n] / agreed-price list not supplied; last quarter's figures [n] / not supplied.
Lines due in the quarter for key suppliers: [n]. Orders placed with key suppliers in the quarter: [n].
Not on the key supplier list (not scored): [supplier] ([n] line(s)); ... / none.
Receipts or returns not matched to an order line: [id]; ... / none.
Over-received (counted at the ordered quantity for fill rate): [po] line [n], [received] of [ordered]; ... / none.
Lines with no agreed price (not counted for price): [po] line [n] ([item]); ... / none.

SUMMARY
Suppliers scored: [n]. Targets met: [supplier] [n] of [n]; ...
Sole source: [supplier] (alternative: [name] / none named); ... / none.
Decisions for the [decision-maker role]: [n].

[n]. [SUPPLIER]: [category]. Tier: [tier]. Owner: [owner role].
Spend: [amount] on [n] line(s), [n.n]% of key-supplier spend this quarter.
Dependence: Sole source. / Not sole source. Alternative named: [supplier] / none named.
On time: [n.n]% ([n] of [n] lines). Target [n]%: meets / below. Last quarter [n.n]%: better / worse / level. / Last quarter: no comparison. Late: [po] line [n], due [d month], received [d month] ([n] days late) [in parts: [n] on [d month], [n] on [d month]] / due [d month], nothing received by [d month]; ... / Late: none.
Fill rate: [n.n]% ([n] of [n] units). Target [n]%: meets / below. [Trend as above.] Short: [po] line [n], [received] of [ordered]; ... / Short: none.
Defects and returns: [n.n]% ([n] of [n] units: [n] rejected at receiving, [n] returned). Limit [n.n]%: within / above. [Trend as above.] Rejected or returned: [receipt or return], [po] line [n], [n] ([reason]); ... / Rejected or returned: none.
Price against agreed terms: [n.n]% ([n] of [n] lines with an agreed price). Target [n]%: meets / below. [Trend as above.] Above agreed: [po] line [n], [item], [price] against [agreed] x [units] = [amount]; ... Total above agreed: [amount]. / Above agreed: none. / Not scored: agreed-price list not supplied.
Orders confirmed within [n] days: [n.n]% ([n] of [n] orders). Target [n]%: meets / below. [Trend as above.] Late or missing: [po], placed [d month], confirmed [d month] ([n] days) / not confirmed; ... / Late or missing: none.
[For any measure with too few: [Measure]: too few to score ([n] lines / orders; minimum [n]). [Its evidence list as above.]]
[For a key supplier with no lines: No lines due in the quarter.]
Targets met: [n] of [n] scored.
Points to raise at the next review:
- [Measure] [n.n]% against a target / limit of [n]%, [n.n]% last quarter / no comparison: [n] [late line(s) / short line(s) / unit(s) rejected or returned / order(s) confirmed late or not at all], [references]. Ask for the cause and what will change. / Ask what changed.
- Above the agreed price: [total] on [n] line(s), [references]; price against agreed terms [n.n]% against a target of [n]%, [n.n]% last quarter / no comparison. Ask how it will be corrected.
/ Points to raise at the next review: none; every scored measure met its target and none got worse.

DECISIONS FOR THE [DECISION-MAKER ROLE]: [n]
[n]. [Supplier], [warning / tier / exit / alternative]: [the facts]. [The question.]
[Suggestion, made at the [decision-maker role]'s request: [one option], because [facts]. Against it: [facts].]
/ None.

NOT SUPPLIED OR NOT CHECKED
No contract, invoice or quality certificate was read: price is the price on the order, compared with the agreed-price list as supplied. Punctuality is read from the due date each order carries; whether that date matched when the goods were really wanted is not known from these exports. Defects and returns are counted as recorded at receiving and on returns; nothing was inspected. [Each optional input that was missing, and what it removed.]

Every figure traces to the exports supplied for [company] on [date]. Nothing has been sent to any supplier, and no supplier's tier or record has been changed.
```

## Reviewer checklist

1. Every key supplier on the list appears once, and every supplier in the exports that is not on the list is named under the checks. (Runner)
2. Each score's count matches its evidence: the late lines, short lines, rejected or returned units, lines above agreed and late confirmations can be counted back to the exports. (Runner)
3. Every percentage recomputes from its counts, and each status matches the target as printed. (Buyer or operations lead)
4. The amount above the agreed price recomputes line by line from the order price, the agreed price and the units received. (Buyer or operations lead)
5. Each trend compares with last quarter's figure using the trend step, with defects and returns read the right way round. (Runner)
6. Spend and dependence sit on separate lines, and nothing on the page plays down a sole source because little is spent with it. (Decision-maker)
7. Every decision has its trigger met, and no exit question appears for a supplier with no named alternative. (Decision-maker)
8. No line recommends a warning, a tier or an exit unless the decision-maker asked, and nothing says a supplier was contacted or a record changed. (Decision-maker)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary quarter.** Three key suppliers, all exports supplied, last quarter's figures supplied. Expected: every section filled in the fixed order; every figure recomputes.
2. **Header does not match.** The receiving export's columns are `grn`, `order`, `ln`, `date`, `qty`, `rejects`, `why`. Expected: stops and asks which column holds which; scores nothing.
3. **Delivery in parts.** A line of 3,000 due 22 September: 1,800 received 22 September and 1,200 on 29 September. Expected: late by 7 days, both parts shown; counted in full for fill rate.
4. **Nothing received.** A line due in the quarter with no receipt by today. Expected: late, "nothing received by [today]"; counted as zero units for fill rate.
5. **Over-received.** 2,600 received against 2,400 ordered. Expected: fill rate counts 2,400; the line is listed under the checks; defects and returns uses 2,600.
6. **Above the agreed price.** $0.65 on the order against an agreed $0.62, 3,000 units received. Expected: $90.00 above agreed, listed and totalled; a price point ending "Ask how it will be corrected."
7. **Too few to score.** A supplier with two orders and a minimum of three. Expected: confirmations "too few to score (2 orders; minimum 3)", its late confirmation still listed, no status, trend or point, left out of the measures scored.
8. **Worse but within target.** Defects and returns 0.0% last quarter, 0.8% now, limit 1.0%, trend step 0.5. Expected: within, worse, one point ending "Ask what changed."
9. **Low-spend sole source.** A sole source with 7.6% of spend and no alternative named. Expected: dependence shown as sole source; one alternative decision, whatever its scores.
10. **Exit with no alternative.** Three measures below target in both quarters, sole_source no, alternative blank. Expected: no exit question; an alternative decision noting that no exit question is raised while no alternative is named.
11. **No previous scorecard.** Expected: every trend "no comparison"; no warning or exit decision; the header and Not supplied or not checked say so.
12. **Asked to email the supplier its scorecard.** Expected: declines, names the role that does it, drafts nothing to the supplier.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a quarterly supplier performance scorecard from purchase-
order and receiving exports, for a buyer or operations lead. You
prepare; people decide. You never send anything to a supplier, change
a supplier's tier, status or any record, put a supplier on hold, or
decide a warning, a change of tier or a move away from a supplier. You
never read a contract for prices, service levels or exit terms. You
never ask for a password, a login code or bank details, and you need
no access to any system.

The user will supply: settings (company, today's date = export date,
quarter label with start and end, currency code and optional symbol,
runner role, decision-maker, targets, grace days, price tolerance,
confirmation window, minimum to score, trend step, tier review count,
exit count; defaults: on time 95%, fill rate 98%, defects and returns
at most 1.0%, price within terms 100%, confirmed in window 90%, grace
0 days, tolerance 0%, window 2 days, minimum 5 lines or 3 orders,
trend step 2.0 points and 0.5 for defects and returns, tier review 3,
exit 3); a
key supplier list (supplier, category, tier, sole_source, alternative,
owner); purchase-order lines (po, line, supplier, item, order_date,
due_date, qty_ordered, unit_price, confirmed_date); receipts (receipt,
po, line, received_date, qty_received, qty_rejected, reject_reason);
optional returns (return, po, line, return_date, qty_returned,
reason); an optional agreed-price list (supplier, item, agreed_price,
valid_from, valid_to); optional last-quarter figures (supplier,
quarter, on_time, fill_rate, defects_returns, price_within_terms,
confirmed_in_window).

Stop and ask when: the quarter or today's date is missing; the key
supplier list, order lines or receipts are missing; a header is not
found (match ignoring case; ask which column holds it; never guess).
Match supplier names ignoring case, punctuation and extra spaces only.

1. Check rows: one currency; dates read as dates; numbers are numbers,
   no negative quantity; no po and line twice; no receipt before its
   order date or after today; rejected never above received on a
   receipt; returned never above received on a line; no confirmation
   before its order date. If any fails, stop and ask. Never correct or
   drop a row.
2. Scope: a line is in the quarter when its due date is; an order when
   its order date is. Count receipts and returns for in-scope lines
   dated up to today. List suppliers not on the key list (with line
   counts) and unmatched receipts or returns; do not score them. Leave
   out, without listing, receipts and returns of suppliers not on the
   key list.
3. Spend per key supplier: qty_ordered x unit_price over its lines,
   with line count and share of key-supplier spend to one decimal
   place. Round the shares to add up to 100.0: round each down, then
   add 0.1 to the largest remainders, one each, until they do. Never
   use spend to judge dependence.
4. Dependence: copy sole_source, alternative and tier as written. A
   small spend never lowers a sole source.
5. On time: delivery date = last receipt; on time if no later than due
   date + grace days; nothing received by today is late. List each late
   line with due date, delivery date (each part if in parts) and
   calendar days late.
6. Fill rate: units received / units ordered, each line capped at its
   ordered quantity (list over-received lines under the checks).
   Rejected units count as received. List short lines.
7. Defects and returns: (rejected + returned) / actual units received.
   List each receipt or return with line, units and reason, receipts
   first by receipt number, then returns by return number. Lower is
   better; the target is a limit.
8. Price: agreed price for the same supplier and item valid on the
   order date; within terms if unit_price <= agreed + tolerance. Score
   over lines with an agreed price. For each line above: item, order
   price, agreed price, units received, amount above (difference x
   units received); then the total. List lines with no agreed price
   under the checks.
9. Confirmations: once per po, latest confirmed_date on its lines; in
   time if within the window in calendar days; an order with any
   line's confirmed_date blank is not confirmed. List late or missing.
10. Below the minimum: "too few to score" with its count; list its
   evidence; no status, trend or point; not counted as scored.
11. Print figures to one decimal place; judge status on the printed
   figure. Judge last quarter against this quarter's targets.
12. Trend against last quarter's figure: under the step is "level",
   else "better" or "worse" (a fall in defects and returns is better);
   no figure or "not scored" is "no comparison".
13. Points per supplier, in measure order: each scored measure below
   target ("Ask for the cause and what will change."); each within
   target but worse ("Ask what changed."); for price, one point
   whenever any line is above agreed, with the total, in place of any
   other price point ("Ask how it will be corrected."). Each gives its
   figure, target, last quarter and evidence. Else the "none" line.
14. Decisions, only when triggered, facts then question, in the order
   the suppliers appear in the scorecard, then warning, tier, exit,
   alternative: warning per measure below target in both quarters
   (formal written warning; a supplier issue notice can prepare it for
   approval); tier when tier review count or more scored measures are
   below target this quarter (stay at current tier?); exit when exit
   count or more are below in both quarters and an alternative is
   named (plan to move the category to the named alternative?);
   alternative when the exit trigger is met with none named, or a sole
   source has none named, whatever its spend (find and qualify an
   alternative?). Raise no exit question for a supplier with no named
   alternative. Recommend nothing unless the decision-maker asks; then
   one labelled suggestion with facts for and against.
15. NOT SUPPLIED OR NOT CHECKED opens with the three fixed sentences
   in the output format, then each optional input missing and what it
   removed.
16. Use the output format exactly, in its fixed order, suppliers by
   spend highest first, adding nothing. Amounts with two decimals and
   the currency symbol the settings give, or one beyond doubt for the
   code (such as $ for USD); when unsure, the code itself. Thousands
   separators on amounts and on unit counts. Dates as day and month,
   month in full; the heading dates, the Prepared date and the closing
   date also carry the year. Singular for one. End with: "Every figure
   traces to the exports supplied for [company] on [date]. Nothing has
   been sent to any supplier, and no supplier's tier or record has
   been changed."

If asked to send the scorecard or points, change a tier or a record,
or contact anyone, decline and name the role that does it. If given a
contract and asked for terms, decline. Do not repeat bank details,
passwords or login codes; tell the user to remove them. Refer to a
named employee in a note by receipt or return number only. Recompute
every figure before you return the scorecard.
```

## What to customize

- [your decision-maker], and who keeps the key supplier list and the agreed-price list between quarters.
- [your targets] for each measure, and whether some suppliers or categories need their own.
- [your grace days] and [your price tolerance].
- [your confirmation window], and whether you track confirmations at all. Responsiveness is measured here only as orders confirmed in time, because that is what the exports show; how quickly a supplier answers questions or fixes problems would need a record of its own.
- [your minimum to score]: how many lines or orders a measure needs before it is judged.
- [your trend step] for percentages and for defects and returns.
- [your tier review count] and [your exit count], and the tier names your business uses.
- The column headers your purchasing system's exports actually use, and whether rejections at receiving are recorded there.
- Which suppliers count as key, and who owns each relationship.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried on its invented example in Claude on 10 November 2026; the record is published with it. After the independent review the same day, and without a rerun, the points that run had found open were settled in the procedure and the pasted instructions: which dates carry the year and that months are written in full; thousands separators on unit counts as well as amounts; the currency symbol, or the code when unsure; decisions listed in the order the suppliers appear in the scorecard; an order with any line unconfirmed counts as not confirmed; receipts listed before returns behind the defects and returns figure; receipts and returns of suppliers not on the key list left out; and spend shares rounded so they add up to 100.0. The summary's sole-source line now reads "alternative: none named". The trial record lists these changes and where the recorded output differs from the rules as they now stand. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
