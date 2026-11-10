# Supplier performance scorecard: tried on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

This run used only the invented example in [`example.md`](example.md). No client data was used. The model that ran it did not write the template.

## Inputs used

The seven inputs of the invented example, by reference: the settings, the key supplier list, the purchase-order lines export (20 rows), the receiving export (21 rows), the returns export (1 row), the agreed-price list (6 rows) and last quarter's figures (3 rows), all under "The inputs" in `example.md`. The published output in that file was not read until the run below was finished. The instruction block and the output format in the template were followed as written. The figures were also recomputed with a short script as a cross-check.

## What came out

The scorecard, in full, as the plain-text format returns it:

```
SUPPLIER PERFORMANCE SCORECARD: Brand R, Q3 2026 (1 July to 30 September)

For: Operations lead. Decisions by: Managing director. Prepared Tuesday 6 October from the key supplier list (3 rows), purchase-order lines (20 rows), receiving export (21 rows), returns export (1 row), agreed-price list (6 rows) and last quarter's figures (3 rows). Compared with: Q2 2026 scorecard.
Targets: on time 95% (grace 0 days); fill rate 98%; defects and returns at most 1.0%; price within terms 100% of lines (tolerance 0%); orders confirmed within 2 days 90%. Scored with at least 5 lines, or 3 orders for confirmations. Level means a change under 2.0 points (0.5 for defects and returns).

CHECKS
Rows read: key suppliers 3; order lines 20; receipts 21; returns 1; agreed prices 6; last quarter's figures 3.
Lines due in the quarter for key suppliers: 19. Orders placed with key suppliers in the quarter: 9.
Not on the key supplier list (not scored): Supplier D (1 line).
Receipts or returns not matched to an order line: none.
Over-received (counted at the ordered quantity for fill rate): none.
Lines with no agreed price (not counted for price): none.

SUMMARY
Suppliers scored: 3. Targets met: Supplier B 5 of 5; Supplier A 2 of 5; Supplier C 3 of 4.
Sole source: Supplier C (alternative named: none named).
Decisions for the Managing director: 3.

1. SUPPLIER B: Soy wax. Tier: preferred. Owner: Operations lead.
Spend: $15,890.00 on 6 lines, 54.7% of key-supplier spend this quarter.
Dependence: Not sole source. Alternative named: Supplier F.
On time: 100.0% (6 of 6 lines). Target 95%: meets. Last quarter 100.0%: level. Late: none.
Fill rate: 99.2% (258 of 260 units). Target 98%: meets. Last quarter 100.0%: level. Short: PO-3152 line 1, 78 of 80.
Defects and returns: 0.8% (2 of 258 units: 2 rejected at receiving, 0 returned). Limit 1.0%: within. Last quarter 0.0%: worse. Rejected or returned: RC-504, PO-3105 line 2, 1 (box torn, wax contaminated); RC-517, PO-3152 line 2, 1 (bag split).
Price against agreed terms: 100.0% (6 of 6 lines with an agreed price). Target 100%: meets. Last quarter 100.0%: level. Above agreed: none.
Orders confirmed within 2 days: 100.0% (3 of 3 orders). Target 90%: meets. Last quarter 100.0%: level. Late or missing: none.
Targets met: 5 of 5 scored.
Points to raise at the next review:
- Defects and returns 0.8% against a limit of 1.0%, 0.0% last quarter: 2 units rejected or returned, RC-504 (PO-3105 line 2), RC-517 (PO-3152 line 2). Ask what changed.

2. SUPPLIER A: Glass jars. Tier: preferred. Owner: Operations lead.
Spend: $10,953.00 on 8 lines, 37.7% of key-supplier spend this quarter.
Dependence: Not sole source. Alternative named: Supplier E.
On time: 62.5% (5 of 8 lines). Target 95%: below. Last quarter 88.9%: worse. Late: PO-3118 line 1, due 3 Aug, received 7 Aug (4 days late); PO-3118 line 2, due 3 Aug, received 7 Aug (4 days late); PO-3166 line 1, due 22 Sep, received 29 Sep (7 days late) in parts: 1,800 on 22 Sep, 1,200 on 29 Sep.
Fill rate: 100.0% (15,900 of 15,900 units). Target 98%: meets. Last quarter 99.1%: level. Short: none.
Defects and returns: 0.7% (108 of 15,900 units: 60 rejected at receiving, 48 returned). Limit 1.0%: within. Last quarter 0.4%: level. Rejected or returned: RC-502, PO-3101 line 2, 24 (chipped rims); RT-31, PO-3118 line 1, 48 (clear jars sent as amber); RC-512, PO-3140 line 1, 36 (cracked).
Price against agreed terms: 75.0% (6 of 8 lines with an agreed price). Target 100%: below. Last quarter 100.0%: worse. Above agreed: PO-3118 line 2, JAR-12OZ-CLR, $0.84 against $0.81 x 1,200 = $36.00; PO-3140 line 1, JAR-8OZ-AMB, $0.65 against $0.62 x 3,000 = $90.00. Total above agreed: $126.00.
Orders confirmed within 2 days: 50.0% (2 of 4 orders). Target 90%: below. Last quarter 100.0%: worse. Late or missing: PO-3118, placed 20 Jul, confirmed 24 Jul (4 days); PO-3166, placed 8 Sep, not confirmed.
Targets met: 2 of 5 scored.
Points to raise at the next review:
- On time 62.5% against a target of 95%, 88.9% last quarter: 3 late lines, PO-3118 line 1, PO-3118 line 2, PO-3166 line 1. Ask for the cause and what will change.
- Above the agreed price: $126.00 on 2 lines, PO-3118 line 2, PO-3140 line 1; price against agreed terms 75.0% against a target of 100%, 100.0% last quarter. Ask how it will be corrected.
- Orders confirmed within 2 days 50.0% against a target of 90%, 100.0% last quarter: 2 orders confirmed late or not at all, PO-3118, PO-3166. Ask for the cause and what will change.

3. SUPPLIER C: Wicks. Tier: approved. Owner: Production lead.
Spend: $2,220.00 on 5 lines, 7.6% of key-supplier spend this quarter.
Dependence: Sole source. Alternative named: none named.
On time: 100.0% (5 of 5 lines). Target 95%: meets. Last quarter 100.0%: level. Late: none.
Fill rate: 95.0% (39,900 of 42,000 units). Target 98%: below. Last quarter 99.0%: worse. Short: PO-3147 line 2, 5,400 of 6,000; PO-3147 line 3, 6,500 of 8,000.
Defects and returns: 0.0% (0 of 39,900 units: 0 rejected at receiving, 0 returned). Limit 1.0%: within. Last quarter 0.0%: level. Rejected or returned: none.
Price against agreed terms: 100.0% (5 of 5 lines with an agreed price). Target 100%: meets. Last quarter 100.0%: level. Above agreed: none.
Orders confirmed within 2 days: too few to score (2 orders; minimum 3). Late or missing: PO-3147, placed 24 Aug, confirmed 28 Aug (4 days).
Targets met: 3 of 4 scored.
Points to raise at the next review:
- Fill rate 95.0% against a target of 98%, 99.0% last quarter: 2 short lines, PO-3147 line 2, PO-3147 line 3. Ask for the cause and what will change.

DECISIONS FOR THE MANAGING DIRECTOR: 3
1. Supplier A, warning: on time 62.5% against a target of 95% this quarter (3 of 8 lines late) and 88.9% last quarter. Should the Operations lead give the supplier a formal written warning about on-time delivery? A supplier issue notice can prepare it for approval.
2. Supplier A, tier: three scored measures are below target this quarter (on time 62.5%, price within terms 75.0%, orders confirmed within 2 days 50.0%); current tier is preferred. Should the supplier stay at its current tier?
3. Supplier C, alternative: sole source with no alternative named, whatever its spend ($2,220.00, 7.6% of key-supplier spend); fill rate is 95.0% against a target of 98%, 99.0% last quarter. Should the Production lead be asked to find and qualify an alternative?

NOT SUPPLIED OR NOT CHECKED
No contract, invoice or quality certificate was read: price is the price on the order, compared with the agreed-price list as supplied. Punctuality is read from the due date each order carries; whether that date matched when the goods were really wanted is not known from these exports. Defects and returns are counted as recorded at receiving and on returns; nothing was inspected.

Every figure traces to the exports supplied for Brand R on 6 October 2026. Nothing has been sent to any supplier, and no supplier's tier or record has been changed.
```

## What was observed

- **Every required part was produced,** in the fixed order: header, targets, checks, summary, one block per supplier (highest spend first), decisions, what was not supplied, and the closing line. Nothing in the run made the assistant stop: all inputs and headers were present and every row check passed.
- **The figures match the published example.** Every percentage, count, amount, status, trend, point to raise and decision agrees with it: Supplier B 5 of 5 targets met, Supplier A 2 of 5, Supplier C 3 of 4; three decisions (a warning and a tier question for Supplier A, an alternative question for Supplier C); no exit question.
- **Differences from the published example were in wording and layout only.** The quarter range was written "1 July to 30 September" (the example repeats the year); "Prepared" lists the inputs without naming the settings; dates were short ("3 Aug") where the example writes the month in full; the references inside a point were separated by commas where the example uses semicolons; Supplier A's rejected and returned units were listed in order line (RC-502, RT-31, RC-512) where the example lists receipts before the return; the decision wording differed ("Should the supplier stay at its current tier?" against "Should Supplier A stay preferred?", and the Supplier C decision here also carries the fill-rate figure). The example is also formatted for reading, with bold headings and bullets, where this run is plain text.
- **No fact appears in either output that is not in the inputs.** Both use the supplier category (for example "wicks") from the key supplier list and the weekday of the date given.
- **Where the instructions were ambiguous and a guess was needed:**
  - Whether quantities take thousands separators. The template says this for amounts only; the example and this run both use them for units.
  - The order in which rejected receipts and returns are listed behind one figure. Not stated.
  - The order of decisions "in the order the suppliers appear". It could mean the key supplier list (A, B, C) or the order on the page (B, A, C). The result is the same here because only A and C have decisions.
  - How to write the currency. The settings say USD and the template says "currency symbol"; the assistant has to know that USD is "$".
  - Whether the date range in the heading and the dates in the lines carry the year, and whether months are written in full. The format says "day and month" and shows "[d month]".
  - Whether Supplier D, a supplier not on the key list, should have its receipt checked. The step says receipts for lines not in the export are listed; Supplier D's line is in the export, so its receipt was left out of both the scoring and the checks. This is a reasonable reading but is not spelled out.
  - Whether "the owner" in a decision means the role to name or a person. This run named the owner role on the supplier list.
- **Shortcomings in the template itself.** Its acceptance tests are still marked as proposed and not run, and its version notes still say it has not been tried on its example; both are now out of date for this run, and a reviewer has to update them. The template names no rule for how many places a share of spend is rounded when the shares must add up; here they did (54.7, 37.7, 7.6 make 100.0).
- **Limits of this trial.** One run, one model, one invented example. It shows the instructions can be followed to the published result by this model. It does not show how other products behave, how the template copes with a real purchasing export, or that the figures would hold for a real business. Only one of the twelve acceptance tests (the ordinary quarter) was in effect exercised, along with the late-delivery, delivery-in-parts, too-few-to-score and sole-source cases that the example happens to contain.

## Changes made after this run

These were made on 10 November 2026, after the run above and after the independent review of the template, and have not been run again. The output and observations above are left as the run produced them. Each change settles a point the run or the review found open, mostly in the way the published example already handled it.

- **Dates.** Dates are written as day and month with the month in full; the dates in the heading, the "Prepared" date and the date in the closing line also carry the year.
- **Thousands separators** are used on unit counts as well as on amounts.
- **Currency.** Amounts use the symbol the settings give or one beyond doubt for the code (such as $ for USD); when unsure, the currency code itself.
- **Order of decisions.** Decisions follow the order the suppliers appear in the scorecard (highest spend first).
- **Confirmations.** An order with any line unconfirmed counts as not confirmed.
- **Rejected and returned units** behind the defects and returns figure are listed receipts first, by receipt number, then returns, by return number.
- **Suppliers not on the key list.** Their receipts and returns are left out, neither used nor listed.
- **Spend shares** are rounded to one decimal place so that they add up to 100.0: each is rounded down, then 0.1 is added to the largest remainders until they do.
- **Sole-source line.** The summary's sole-source line now reads "(alternative: [name] / none named)", so the example reads "Supplier C (alternative: none named)" where it had "alternative named: none named".
- The template's note on what to customize now says that responsiveness is measured only as orders confirmed in time.

Read against the revised rules, the output above follows them in substance, with these differences of form: its heading range and its "Prepared" date have no year; its dates inside the supplier blocks use short month names ("3 Aug"); its sole-source line still reads "alternative named: none named"; and it lists Supplier A's rejected and returned units by order line (RC-502, RT-31, RC-512) where the rule now puts the return last (RC-502, RC-512, RT-31). Its currency, separators, decision order, spend shares (54.7, 37.7 and 7.6 under the new rounding rule as well), treatment of PO-3166 as not confirmed and leaving Supplier D's receipt out already match the revised rules. Two points this run noted are not changed: whether references inside a point are separated by commas or semicolons, and that "the owner" in a decision is the owner role named on the key supplier list, which the output format already shows as "Owner: [owner role]". The acceptance tests remain marked as proposed.
