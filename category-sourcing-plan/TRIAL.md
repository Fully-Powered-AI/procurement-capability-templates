# Category sourcing plan: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Opus 5.5 (model ID claude-opus-5-5), the model that revised the template after review; not an independent run
- **Date:** 2026-11-10

The inputs were the invented example's own inputs (the category brief, spend export, supplier facts, market notes and user notes in `public/example.md`), as revised on 10 November 2026 so that each supplier line says which items the supplier is qualified for. No client data was used. The company, suppliers, people and figures are all invented. The company settings were the template's defaults.

This record replaces the record of an earlier run of the first draft (summarised at the end). The run below followed the instruction block and the output format in `member/template.md` on the inputs above. Because the same model revised the template and made this run, it is a weaker check than a run by a model that had not seen the template's reasoning; the published example's plan was then written from this output. Small edits made after the run, and not re-run, are listed under "Edits after this record was written".

## What came out

The full plan, as produced:

```
CATEGORY SOURCING PLAN: shipping packaging

For: operations director. Prepared by: purchasing lead on 10 November 2026. Plan goes to the operations director by: 4 December 2026.
Spend period: 1 November 2025 to 31 October 2026. Currency: US dollars.
Spend export: 15 rows read; 14 in the period; 1 outside it, excluded; 0 outside the scope, excluded. Columns ignored: none. Rows to check: none.
Inputs not supplied: none. Settings: template defaults.

1. THE CATEGORY
In scope: corrugated shipping boxes, divider inserts, printed display trays. Left out: jar labels and glass jars (other categories).
Objectives, in the order given: cost, then reliable delivery. Constraints: the six-cell insert must hold six 250 ml jars; its size does not change.

2. SPEND
Total: $233,950 over 14 rows. Share of company spend: $233,950 ÷ $4,300,000 = 5.4%.
By supplier: Supplier A: $138,800, 59.3%, 7 rows. Supplier B: $63,100, 27.0%, 4 rows. Supplier C: $28,000, 12.0%, 2 rows. Supplier D: $4,050, 1.7%, 1 row.
Check: supplier amounts add to $233,950, the category total.
By item: BX-12 Shipper box 12x10x8: 195,000 units, $127,050, 54.3%, unit price $0.62 to $0.81. BX-18 Shipper box 18x12x10: 55,000 units, $53,700, 23.0%, unit price $0.95 to $1.02. TRAY-P Printed display tray: 20,000 units, $28,000, 12.0%, unit price $1.40. INS-6 Six-cell divider insert: 120,000 units, $25,200, 10.8%, unit price $0.21.
Largest supplier: Supplier A, 59.3%. Top three suppliers: 98.3%. Small suppliers (under 2% each): Supplier D, $4,050.
Shares are rounded to one decimal and may not add to exactly 100.0.

3. SUPPLIERS
Supplier A: supplies BX-12, BX-18, INS-6. Qualified for: BX-12, BX-18, INS-6. Only qualified supplier for: none. Agreement ends 31 March 2027; notice date 31 December 2026. Lead time: 10 days. Payment terms: 30 days. Problems in the period: two late deliveries of BX-12, 8 June and 22 June 2026. NOTICE DATE WITHIN 90 DAYS
Supplier B: supplies BX-12, BX-18. Qualified for: BX-12, BX-18, INS-6 (has not supplied INS-6 this year). Only qualified supplier for: none. No agreement; notice date not stated. Lead time: 7 days. Payment terms: 30 days. Problems in the period: none recorded.
Supplier C: supplies TRAY-P. Qualified for: TRAY-P. Only qualified supplier for: TRAY-P. Agreement ends 30 June 2027; notice date 31 March 2027. Lead time: 35 days. Payment terms: 45 days. Problems in the period: none recorded.
Supplier D: supplies BX-12, emergency buys only. Qualified for: BX-12. Only qualified supplier for: none. No agreement; notice date not stated. Lead time: 2 days. Payment terms: company card. Problems in the period: none recorded.
Dates as supplied by the finance director. No agreement was read. The 90-day notice window runs from 10 November 2026 to 8 February 2027.

4. POSITION ON THE MATRIX
Spend impact: High. The category is 5.4% of company spend, at or above 5%. The brief says that if supply fails, orders cannot be shipped.
R1 Concentration: Supplier A, 59.3% (spend export) against 70%: Low.
R2 Single-source spend: TRAY-P, 12.0% (supplier facts, spend export) against 25%: Low.
R3 Alternatives for the main items (BX-12 and BX-18, 77.3% of spend): 2 qualified (Supplier A, Supplier B), 2 candidates (Supplier E, Supplier F, market notes, not yet checked) against a minimum of 3: Low. Not counted, covering only some main items: Supplier D: BX-12. Qualification assumed from the export for: none.
R4 Switching time for the main items: about 4 weeks to approve a new box maker (market notes) against 8 weeks: Low.
R5 Supply problems: Supplier A, 59.3%, two late deliveries of BX-12 on 8 June and 22 June 2026 (supplier facts): High.
Supply risk: Low (1 of 5 factors High).
Position: Leverage (spend impact High, supply risk Low).
Items that sit apart: TRAY-P: one qualified supplier (Supplier C); about 12 weeks to approve another, above the 8-week limit (market notes). On its own it falls in the high-supply-risk half and is handled as an exception.
For the operations director to confirm.

5. VALUE LEVERS
Price: Supported: BX-12 was bought at five unit prices from $0.62 to $0.81, and BX-18 at three from $0.95 to $1.02. The market notes say Supplier A raised its box prices in June 2026; the export shows Supplier A's BX-12 at $0.64 from 11 June 2026 ($0.62 before) and its BX-18 at $0.97 on 10 September 2026 ($0.95 before). For the main items there are two qualified suppliers (A and B) and two candidates not yet checked (E and F, who have asked to quote). Price gap: BX-12 (lowest $0.62): 30,000 x $0.06 + 40,000 x $0.02 + 5,000 x $0.19 + 30,000 x $0.06 + 10,000 x $0.08 = $6,150. BX-18 (lowest $0.95): 15,000 x $0.07 + 20,000 x $0.02 = $1,450. Total $7,600, 3.2% of category spend.
Demand and specification: Supported: the warehouse lead says the 18x12x10 box often goes out part-empty on small orders and would like a middle size. No figure.
Supplier base: Supported: BX-12 was bought from three suppliers (A, B and D) and BX-18 from two (A and B); Supplier D, a small supplier, is used for emergency buys and its $0.81 is the highest BX-12 price in the period; INS-6 was bought only from Supplier A, though Supplier B is also qualified for it. No figure.
Total cost: Supported: payment terms differ: 30 days (Suppliers A and B), 45 days (Supplier C), company card (Supplier D). No figure.
Working with suppliers: Supported: Supplier A, with 59.3% of spend, delivered BX-12 late twice in June 2026, a problem a supplier could fix with an agreed commitment. No figure.
Baseline: unit prices and quantities by item, 1 November 2025 to 31 October 2026. Later results compare unit prices on the units actually bought, so buying less is never counted as a price saving. The price gap is indicative: not a forecast, a target or a promise.

6. APPROACH OPTIONS
Option 1: ask Suppliers A and B and candidates E and F for quotes on BX-12, BX-18 and INS-6, with a quote for a middle box size as the warehouse lead asks, then combine the volume in fewer suppliers; TRAY-P stays with Supplier C. Levers: Price, Supplier base, Demand and specification. Main risk: a new supplier's boxes may not run on the taping machine (warehouse lead). Affects: purchasing lead, warehouse lead, production manager, finance director; Suppliers A, B, D, E, F.
Option 2: negotiate with Suppliers A and B only, using the $7,600 price gap and their combined volume, including INS-6, for which Supplier B is also qualified. Levers: Price, Supplier base. Main risk: Supplier A, with 59.3% of spend, delivered BX-12 late twice in June 2026 (supplier facts). Affects: purchasing lead, finance director; Suppliers A, B, D.
Option 3: Keep the current arrangement and fix the named issues: Supplier A's two late deliveries of BX-12 in June 2026, fix to be agreed; Supplier A's June 2026 price rise, explained, as the finance director asks; the part-empty 18x12x10 box, a middle size, as the warehouse lead asks. Levers: Working with suppliers, Demand and specification. Main risk: the $7,600 price gap stays (spend export). Affects: purchasing lead, warehouse lead, finance director; Suppliers A, B.
Approach to plan: Option 1, proposed by the purchasing lead. Fits the usual directions for Leverage.

7. SOURCING PLAN
S1 Agree requirements with the people who use the category: purchasing lead. 4 January 2027 to 15 January 2027.
S2 Find and check suppliers not yet qualified (Supplier E, Supplier F): purchasing lead. 18 January 2027 to 5 February 2027.
S3 Request quotes, compare them and negotiate: purchasing lead, with the vendor quote comparison; requests sent by a person. 8 February 2027 to 19 March 2027.
S4 Decision by the operations director; the outside lawyer reads the agreements affected: 22 March 2027 to 2 April 2027.
S5 Move orders, set up suppliers, tell suppliers whose share changes: purchasing lead; every message sent by a person after approval. 5 April 2027 to 14 May 2027.
S6 First check of results against the baseline, reported to the operations director: purchasing lead. 9 August 2027 to 13 August 2027.
Lengths are calendar weeks; holidays and closures are not skipped.
Exception items: TRAY-P: kept with Supplier C, outside the quotes.
Timing: Supplier A's notice date, 31 December 2026, falls before S1 starts. Supplier A's agreement end, 31 March 2027, falls within S4, 22 March 2027 to 2 April 2027. Supplier C's notice date, 31 March 2027, falls within S4, 22 March 2027 to 2 April 2027. Supplier C's agreement end, 30 June 2027, falls between S5 and S6, 14 May 2027 to 9 August 2027.

8. CONCERNS AND RISKS
Warehouse lead: the 18x12x10 box often goes out part-empty on small orders; would like a middle size. Handled in: S1 and S3.
Warehouse lead: worried a new supplier's boxes may not run on the taping machine. Handled in: S2.
Production manager: the insert must hold six 250 ml jars; no change to its size. Handled in: S1.
Marketing manager: the tray artwork is approved; does not want the tray supplier changed this year. Handled in: exception (TRAY-P kept with Supplier C).
Finance director: wants Supplier A's June price rise explained before any new arrangement with Supplier A. Handled in: open.
Supply risk, R5 supply problems (Supplier A, 59.3% of spend, two late deliveries of BX-12 in June 2026): open.

9. FOR THE CONTRACT REVIEWER
Supplier A: agreement ends 31 March 2027; notice date 31 December 2026, as supplied by the finance director. The plan would: end it, change it or let it run on, depending on the quotes and the operations director's decision in S4. Not read or interpreted.
Supplier C: agreement ends 30 June 2027; notice date 31 March 2027, as supplied by the finance director. The plan would: let it run on. Not read or interpreted.
Any new or changed agreement goes to the outside lawyer before it is signed.

10. GAPS AND QUESTIONS
No volumes for 2027 were given; quotes would use the last twelve months' quantities (BX-12 195,000; BX-18 55,000; INS-6 120,000): purchasing lead, with the production manager.
Delivery and minimum-order charges, rejected goods and rush orders were not supplied, so total cost can be compared on payment terms only: purchasing lead, with the finance director.
Whether Suppliers E and F make both box sizes and the insert, as they say, is not checked: purchasing lead.
What Supplier A's June 2026 price rise rested on: finance director.
How often the 18x12x10 box goes out part-empty, and what middle size is wanted: warehouse lead.
Why BX-12 was bought from Supplier D on 9 July 2026: purchasing lead.

11. DECISIONS FOR THE OPERATIONS DIRECTOR
1. Confirm the position: Leverage (spend impact High, supply risk Low, 1 of 5 factors High).
2. Approve Option 1 as the approach to plan, or choose Option 2 or 3.
3. Supplier A's agreement: notice date 31 December 2026, within 90 days and before S1 starts on 4 January 2027; agreement ends 31 March 2027, within S4, 22 March 2027 to 2 April 2027. For the operations director to decide after the outside lawyer has read the agreement.
4. Supplier C's agreement: notice date 31 March 2027, within S4, 22 March 2027 to 2 April 2027; agreement ends 30 June 2027, between S5 and S6. For the operations director to decide after the outside lawyer has read the agreement.
5. The exception item: keep TRAY-P with Supplier C outside the quotes.
6. When Supplier A's June 2026 price rise is to be explained, since the finance director asks for it before any new arrangement with Supplier A.

Status: prepared for the operations director's decision. No supplier has been contacted, no order or record changed, and nothing sent, accepted or signed.
```

## What was observed

All eleven sections and the status line were produced, in the order and wording the format gives. No stop condition applied: the brief had a category, items in scope and a start date; the six export headers were present; there was one currency; the supplier amounts added to the category total; every supplier line said which items it was qualified for, so no qualification was assumed.

Every figure and date was recomputed with a short script and by hand: 14 rows in the period totalling $233,950 (one row, 5 November 2026, outside it); supplier amounts $138,800, $63,100, $28,000 and $4,050 with their shares; item amounts and shares; top three 98.3%; main items BX-12 and BX-18 at 77.3%; share of company spend 5.4%; the price gap $6,150 + $1,450 = $7,600, 3.2%; the notice window to 8 February 2027; the six step dates, each step starting on a Monday and ending on a Friday, and S6 starting 12 weeks after Monday 17 May 2027.

The position comes from stated facts, not an assumption: Suppliers A and B are qualified for both main items, Suppliers E and F are named in the market notes as able to make both box sizes, and Supplier D, qualified for BX-12 only, is named and not counted. That gives 2 qualified and 2 candidates against a minimum of 3, so R3 is Low; with R5 the only High factor, supply risk is Low and the position is Leverage.

### Wording gaps found during the run

Two gaps in the template's wording turned up while producing the output. Both were fixed in the template before this record was written, and the output above was then checked again, line by line, against the final instruction block and output format; it needed no change. No other edit has been made since.

1. The procedure asks for each supply-risk factor's source, but the format's R1, R2, R3 and R5 lines had no place for it. The run printed the source in brackets, and the format now has that slot.
2. The rule for the last option's named issues said "each change a user asks for that the current suppliers could make", which needs a judgment about what the suppliers can do. It now reads "each change or explanation a user asks for, other than a change of supplier". The run's Option 3 (Supplier A's late deliveries, the price rise explained, a middle box size) fits both wordings.

### Judgment calls another run could make differently

None of these changes a figure, a rating, a date or the position.

- Option 1 includes a quote for a middle box size because the warehouse lead asks for one, and so lists the Demand and specification lever. A run that kept Option 1 to the boxes and insert as they are would list two levers, not three.
- The "Affects" lists and the "Handled in" lines are matched by reading the inputs (for example, Supplier D under Option 1 because its BX-12 buys would be among the volume combined; the middle-size concern under S1 and S3).
- The gaps and questions list is open-ended. This run listed six; another might add the excluded 5 November row or leave out the question about Supplier D's emergency buy.
- Decision 6, on when Supplier A's price rise is explained, comes under "any other choice the plan cannot make" and is a judgment.
- Decision 4 lists Supplier C's agreement although the plan lets it run on, because the decisions rule takes every supplier whose dates fall before S6 ends. That is what the rule says, and it keeps the outside lawyer's reading ahead of any decision on it.

### Facts in the output that are not in the inputs

None found. The price lever names E and F as candidates who have asked to quote and are not yet checked, as the market notes say. No remedy is proposed that the inputs do not mention, and no course of action is suggested on either agreement.

## Edits after this record was written

An independent review of this version, the same day, passed it with minor points. The following small edits were then made, by Opus 5.5 (claude-opus-5-5), the same model that revised the template and made the run above. "No other edit has been made since", above, was true when the record was written; these edits came after it.

1. The instruction block's five supply-risk limits, written as fixed figures, now use the same "[your ..., default ...]" form as the other settings. The defaults are unchanged (70%, 25%, 3, 8 weeks, 25%).
2. The instruction block's sentence on gaps and questions now also asks for items that look alike but are written differently, and, when no volumes for the coming year are given, a line saying quotes would use the last twelve months' quantities. Both were already in the procedure.
3. The instruction block's lines were re-wrapped where they were ragged.
4. The brief now names the decision maker and contract reviewer roles, in the template's inputs, in the instruction block and in the example's brief ("Decision maker: operations director." and "Contract reviewer: outside lawyer."). At the time of the run these roles were stated only in the example's introduction, and the output above used them from there.
5. The source credits now say that the usual order of sourcing steps comes from the source.

The template was not run again after these edits. The output above was checked line by line against the edited instruction block, the output format (which did not change) and the edited example inputs: with the default limits, the ratings and the position are the same; the example has no items written two ways, and its gaps and questions already carry the line on last year's quantities; the roles in the output match the new brief lines, so "Inputs not supplied: none" still holds. It needed no change. The output above and the observations are as first recorded.

## The earlier run, of the first draft

The first draft was run once the same day, also in Claude, by Sonnet 5.5 (claude-sonnet-5-5), a model that had not written it. Its figures, ratings, position and step dates matched the first draft's example. It recorded twelve ambiguities; the main one was that the supplier facts never asked which items a supplier is qualified for, so its R3 count rested on assuming Suppliers A and B were qualified. The independent review pointed out that without that assumption R3 would have been High and the position Critical, not Leverage. The run also found that a date between S5 and S6 had no wording, that the decisions rule and the reviewer checklist disagreed, and that the format did not say whether to print cents. An independent review afterwards also found that the pasted block named the four positions without saying how spend impact and supply risk map to them, and referred to the positions' usual directions without listing them. The template, the example's inputs and its plan were revised to deal with each point, and the run recorded above is on the revised version.
