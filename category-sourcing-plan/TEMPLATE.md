# Category sourcing plan

Workflow template, version 0.1.0.

## Purpose

Prepare one sourcing plan for one spend category, such as shipping packaging, IT hardware or cleaning supplies, for the buyer or operations lead who owns it. The plan sets out twelve months of the category's spend by supplier and by item, checked against the export it came from; the suppliers and the dates the person supplies for them; where the category sits on a matrix of supply risk against spend impact, with every factor rated from the inputs; the value levers the evidence supports; two or three approach options; and, for the approach a person has chosen, a sourcing plan with steps, owners and dates. The assistant prepares and checks. It never chooses the approach, contacts a supplier, gives notice, places or changes an order, changes a record or says what an agreement means.

## When to use it and when not to

Use it once a year for each category that matters, when a category has grown without anyone looking at it as a whole, before the main agreements in a category come up for notice, or when a new buyer takes a category over and needs to see it on one page.

Do not use it:

- for one purchase with quotes already in. Use the vendor quote comparison;
- for one supplier's renewal. Use the vendor renewal review;
- to forecast prices or to quote market figures nobody supplied. The assistant does not research the market; it works from what the person supplies;
- to read, explain, negotiate or prepare agreement terms. Those go to [your contract reviewer];
- for spend that is not one category, such as all spend with one supplier across several categories.

## Roles

- **Runs it:** the buyer, purchasing lead or operations lead who owns the category.
- **Confirms the position, chooses the approach and approves the plan:** [your decision maker], usually the operations director, the finance director or the owner.
- **Supplies the agreement dates:** whoever holds the signed agreements, often finance.
- **Reads every agreement the plan would end, change or create, before anything is signed or any notice is given:** [your contract reviewer].
- **Sends requests for quotes and any message to a supplier:** a person, after [your decision maker] approves the plan.

## Inputs

1. **The category brief,** typed by the person who runs it:
   - the category's name, the items in scope and anything left out;
   - the objectives in order (for example cost, supply security, quality, service);
   - constraints that cannot change, such as a fixed item size or an approval rule;
   - what happens to the business if supply of the category fails, if known;
   - the company's total spend with third parties over the same twelve months, if known;
   - today's date, the date the plan must reach [your decision maker], and the date the plan would start (a Monday);
   - the currency;
   - the roles of [your decision maker] and [your contract reviewer];
   - the approach to plan, if one has been chosen: one of the options from an earlier run, or a short description. If none is given, the plan section is not drafted.
   If the brief has no category, no items in scope or no plan start date, stop and ask for them.
2. **The spend export:** twelve months of invoice or order lines for the category. Default column headers: `Date`, `Supplier`, `Item`, `Quantity`, `Unit price`, `Amount`. If any of the six is missing or named differently, stop and ask which column holds it; never guess. Extra columns are ignored and named in the header. Rules:
   - the spend period is the twelve months ending on the last day of the month before today, unless the brief gives another period; rows dated outside it are left out and counted;
   - `Amount` must equal `Quantity` × `Unit price` to the cent; a row that does not is listed under rows to check, counted in spend at its `Amount` and left out of the price gap;
   - a negative amount is a credit: it reduces that supplier's spend and is left out of the price gap;
   - the same item means the same `Item` text exactly. Items that look alike but are written differently are not merged; they go under gaps and questions;
   - if the export shows more than one currency, stop and ask for the rate to use.
3. **The supplier facts,** one line per supplier in the export: what it supplies, the items it is qualified to supply (approved for use by the company), any of those for which it is the only qualified supplier, the agreement end date and notice date (or "no agreement"), lead time, payment terms, and problems in the period such as late deliveries or rejected goods, with dates. Say who supplied the dates. A supplier in the export with no line is listed with every fact "not stated". If a line does not say which items the supplier is qualified for, it is treated as qualified for the items bought from it in the spend period, and the plan prints that assumption in section 3 and on the R3 line.
4. **Market notes** (optional), from the person: other suppliers known to be able to supply, qualified or not yet checked; how long it takes to approve a new supplier for each item; anything known about prices. The assistant uses nothing about the market that is not in these notes. If none are supplied, the factors that need them are rated Unknown.
5. **Notes from the people who use the category** (optional): each person's role, their requirements and their concerns. If none are supplied, write "none supplied" in section 8.
6. **The company's settings,** if they differ from these defaults:
   - spend impact is High when the category is at least [your spend-impact share, default 5%] of company spend;
   - a small supplier is under [your small-supplier share, default 2%] of category spend;
   - the main items are the largest items, taken in order of spend until they reach [your main-items share, default 75%] of category spend;
   - the five supply-risk limits in step 5 of the procedure, and [your High-factor count, default 2];
   - the notice window: [your notice window, default 90 days];
   - step lengths, in calendar weeks: S1 2, S2 3, S3 6, S4 2, S5 6; S6 starts [your review gap, default 12 weeks] after the Monday that follows the end of S5, and lasts 1 week.
   Settings not supplied are not a missing input: the header prints "Settings: template defaults", or the settings that differ.

The assistant works only from what the person supplies. It needs no access to a purchasing system, email or any supplier's portal, and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm the brief has a category, items in scope and a plan start date, and that the export has the six headers. Stop and ask if not. List every optional input not supplied (market notes, users' notes, a fact missing from the brief) in the header; the settings have their own header line.
2. **Read the export.** Count the rows read, the rows in the period and the rows outside it. Check each row's amount against quantity × unit price. Name any column ignored.
3. **Profile the spend.**
   - Total spend in the period and the number of rows. Share of company spend = category total ÷ company total, to one decimal, or "company total not supplied".
   - By supplier: amount, share of category spend to one decimal, rows. Check that the supplier amounts add to the category total, and print the check.
   - By item: quantity, amount, share, and the lowest and highest unit price paid (or the one price).
   - The largest supplier's share; the top three suppliers' combined share; each small supplier with its amount.
   - Shares are rounded to one decimal and may not add to exactly 100.0; say so.
4. **List the suppliers** from the supplier facts, with the items each is qualified for (or, where the facts do not say, "assumed from the export:" and the items bought from it). Print each date as supplied. Mark a notice date that falls between today and the end of the notice window "NOTICE DATE WITHIN [n] DAYS", and one already past "NOTICE DATE PASSED". Mark an agreement end date in the same window "AGREEMENT ENDS WITHIN [n] DAYS", and one already past "AGREEMENT END PASSED". Print the window's end date once under the list. Never work out a notice date from an agreement; use only the dates supplied.
5. **Place the category on the matrix.**
   - **Spend impact** is High when the share of company spend is at or above [your spend-impact share], or when the brief says a failure of supply stops production or delivery to customers. Otherwise Low. Give each reason that applies. If the company total is missing and the brief says nothing about failure of supply, spend impact is Unknown.
   - **Supply risk** is rated on five factors, each High, Low or Unknown, each printed with its value, its limit and where the value came from:
     - R1, concentration: the largest supplier's share of category spend is at or above [your concentration limit, default 70%];
     - R2, single-source spend: items with only one qualified supplier make up at least [your single-source share, default 25%] of category spend;
     - R3, alternatives: fewer than [your alternatives minimum, default 3] suppliers can supply every main item. A supplier counts when it is qualified for every main item (from the supplier facts, or assumed from the export as in input 3), or when the market notes name it as able to supply every main item (a candidate, not yet qualified). A supplier that covers only some main items is named and not counted. Print the qualified and candidate counts separately, the suppliers not counted, and any qualification assumed from the export;
     - R4, switching time: approving a new supplier for the main items takes longer than [your switching limit, default 8 weeks];
     - R5, supply problems: a supplier with at least [your problem-supplier share, default 25%] of category spend had a recorded late delivery or rejected delivery in the period.
   - Supply risk is High when [your High-factor count] or more factors are High; otherwise Low. If Unknown factors could take the count to that number, the position is marked "provisional" and the unknown factors are named.
   - **The position:** high impact and high risk is Critical; high impact and low risk is Leverage; low impact and high risk is Bottleneck; low impact and low risk is Routine. This is the widely used supply-risk and spend matrix. If spend impact is Unknown, write "Position: not set" and what is missing.
   - **Items that sit apart:** list any item with only one qualified supplier, or whose switching time is above the limit, with its reasons. Say that on its own it falls in the high-supply-risk half of the matrix and is handled as an exception in the plan.
   - The position is for [your decision maker] to confirm.
6. **Test the value levers.** Go through the five groups below. For each, write "Supported" with the evidence from the inputs, or "No evidence in the inputs". Invent no evidence and give no percentage from outside the inputs.
   - **Price:** the same item bought at different unit prices; price rises in the period; enough suppliers to ask for competing quotes. Only this lever gets a figure: the price gap, which is the sum, over every row of an item bought above the lowest unit price the company itself paid for that item in the period, of quantity × (unit price − lowest unit price). Leave out rows to check and credits. Show the arithmetic by item, then the total and its share of category spend. The price gap is indicative: what the period would have cost had every unit been bought at the lowest price already paid. It is not a forecast, a target or a promise.
   - **Demand and specification:** more item variants than users need, items over-specified for their use, waste or part-used packs, a size change users ask for.
   - **Supplier base:** the same item bought from several suppliers, small suppliers used for emergency buys, a single supplier where a second would help.
   - **Total cost:** payment terms that differ between suppliers, delivery or minimum-order charges, rejected goods, rush orders.
   - **Working with suppliers:** problems that a supplier could fix with an agreed commitment, or improvements that need the supplier's help.
   - Never add figures across levers; only the price lever carries one.
   - End with the baseline line: unit prices and quantities by item in the spend period are the baseline; later results compare unit prices on the units actually bought, so buying less is never counted as a price saving.
7. **Set out the approach options.** Two options from the position's usual directions, then always "keep the current arrangement and fix the named issues" as the last option. The usual directions:
   - **Leverage:** competing quotes from qualified and candidate suppliers, with volume combined in fewer suppliers; or negotiation with current suppliers only, using the price gap and combined volume.
   - **Critical:** a longer arrangement with the key supplier, with service and price reviews for [your contract reviewer] to look at, and a joint improvement plan; or developing a second qualified supplier.
   - **Bottleneck:** securing supply through buffer stock or a longer arrangement; or widening supply by changing the specification or approving another supplier.
   - **Routine:** less buyer time per order, through one supplier, a catalogue or a standing order; or combining it with another category's buying.
   - For each option: what it involves for this category, the supported levers it uses, its main risk taken from the inputs, and the roles and suppliers it affects. Recommend none.
   - An option lists a lever only when it is marked "Supported" in section 5 and the option acts on that lever's evidence; Price is listed for any option that asks for quotes or new prices. The main risk is one fact stated in the inputs or computed from the export (a concern, a problem, a fact in the market notes, the price gap), with its source; no reasoning about likely outcomes.
   - The named issues in the last option are each supplier problem in the supplier facts and each change or explanation a user asks for, other than a change of supplier. Each is named with the fix the inputs ask for, or "fix to be agreed" when the inputs ask for none. Add no remedy the inputs do not mention.
   - If the position is not set, print "Options: not set out until the position is set" in place of the options.
   - Then the approach to plan: the option in the brief and who proposed it, or "Not chosen". Say whether it fits the usual directions for the position, and if not, how it differs. A different approach is allowed; the line only says so.
8. **Draft the sourcing plan,** only when an approach has been chosen. If none has, print "Not drafted" and stop this section. Use these steps and include each only when the approach needs it:
   - S1 agree requirements with the people who use the category. Always included. Owner: the role that ran the plan (the buyer).
   - S2 find and check suppliers not yet qualified. Only when the approach brings in new suppliers. Owner: the role that ran the plan.
   - S3 request quotes, compare them and negotiate. Only when the approach asks for quotes or new prices. Owner: the role that ran the plan, with the vendor quote comparison; requests sent by a person.
   - S4 decision by [your decision maker]; [your contract reviewer] reads any agreement to be ended, changed or created. Always included.
   - S5 move orders, set up the chosen suppliers and tell suppliers whose share changes. Only when the approach moves orders or changes suppliers. Owner: the role that ran the plan; every message sent by a person after approval.
   - S6 first check of results against the baseline, reported to [your decision maker]. Always included. Owner: the role that ran the plan.
   - Dates: S1 starts on the plan start date. Each step starts on the Monday after the step before it ends and ends on the Friday of its last week. S6 starts [your review gap] after the Monday that follows the end of S5. A skipped step prints "skipped" with its reason and takes no time. Lengths are calendar weeks; holidays and closures are not skipped, and the line under the steps says so.
   - Exception items: state how each item that sits apart is handled (for example kept with its current supplier outside the quotes).
   - Timing: for every supplier date supplied (notice date or agreement end), say where it falls: before S1 starts; within a step, naming the step and its dates; between two steps, naming both and the dates of the gap; or after the plan ends (after S6). Every date supplied gets a line. Draw no conclusion about what the agreement allows.
9. **List concerns and risks.** Each concern from the users' notes, with its role, and the step or exception that deals with it, or "open". Then each supply-risk factor rated High, with how the plan handles it, or "open".
10. **Prepare the contract reviewer's list.** For every supplier whose agreement the plan would end, change or let run on, its dates as supplied and what the plan would do. Quote nothing the person has not supplied, and interpret nothing. End with the line that any new or changed agreement goes to [your contract reviewer] before signing.
11. **List the gaps and questions,** each with the role that can answer: missing inputs, items that look alike but are written differently, facts the levers or factors needed and did not have, volumes for the coming year if none were given (quotes then use the last twelve months' quantities, and the line says so).
12. **List the decisions** for [your decision maker]: confirm the position; approve the approach to plan or choose another; for each supplier with a date flagged in section 3 or falling before S6 ends (with no plan drafted, each flagged in section 3), its dates and where they fall, with the line that [your contract reviewer] reads the agreement before anything is decided on it (suggest no course of action on the agreement); every exception item; and any other choice the plan cannot make. End with the status line.
13. **Return the plan** to the person who ran it, for [your decision maker]. If the approach changes, run the plan section again from step 8.

## Exceptions and stop conditions

- **No category, no items in scope or no plan start date:** stop and ask.
- **An export header missing or named differently:** stop and ask which column holds it. Never guess.
- **More than one currency:** stop and ask for the rate.
- **Supplier facts do not say which items a supplier is qualified for:** carry on, treat it as qualified for the items bought from it in the period, and print the assumption in section 3 and on the R3 line.
- **Supplier amounts do not add to the category total:** stop, print both figures and the difference, and draft nothing else.
- **Spend from more than one category in the export** (items the brief leaves out): leave those rows out, count them in the header as outside the scope, and list them under gaps and questions.
- **Asked which approach to take, or to rank the options:** decline. Set out the options; [your decision maker] chooses.
- **Asked for a savings target, a market price or a percentage not drawn from the inputs:** decline. Only the price gap is given, and only as indicative.
- **Asked what an agreement allows, whether notice can still be given, or for new terms:** decline. List the dates for [your contract reviewer].
- **Asked to contact a supplier, give notice, place, move or cancel an order, or change a record:** decline and say who does it once the plan is approved.
- **A row or a note contains bank details:** do not repeat them in the plan.

## Output format

Amounts print with the currency sign and thousands separators and without cents; unit prices and price differences print with cents, as in the export. Dates print as day, month and year (4 January 2027), without the weekday. Where the format gives alternatives in brackets, print the one that applies; add no lines the format does not contain.

```
CATEGORY SOURCING PLAN: [category]

For: [decision maker role]. Prepared by: [role that ran it] on [date]. Plan goes to the [decision maker role] by: [date].
Spend period: [from] to [to]. Currency: [currency].
Spend export: [n] rows read; [n] in the period; [n] outside it, excluded; [n] outside the scope, excluded. Columns ignored: [names / none]. Rows to check: [row date, supplier, reason / none].
Inputs not supplied: [list / none]. Settings: [template defaults / the settings that differ].

1. THE CATEGORY
In scope: [items]. Left out: [items / none stated].
Objectives, in the order given: [list]. Constraints: [list / none stated].

2. SPEND
Total: [amount] over [n] rows. Share of company spend: [amount] ÷ [company total] = [x.x%]. [Or: company total not supplied.]
By supplier: Supplier [x]: [amount], [x.x%], [n] rows. ...
Check: supplier amounts add to [amount], the category total.
By item: [item]: [quantity] units, [amount], [x.x%], unit price [lowest] to [highest] / [one price]. ...
Largest supplier: Supplier [x], [x.x%]. Top three suppliers: [x.x%]. Small suppliers (under [n]% each): Supplier [x], [amount]. [Or: none.]
Shares are rounded to one decimal and may not add to exactly 100.0.

3. SUPPLIERS
Supplier [x]: supplies [items]. Qualified for: [items / assumed from the export: items]. Only qualified supplier for: [items / none]. [Agreement ends [date] / No agreement]; notice date [date / not stated]. Lead time: [n days / not stated]. Payment terms: [terms / not stated]. Problems in the period: [as supplied, with dates / none recorded]. [NOTICE DATE WITHIN [n] DAYS / NOTICE DATE PASSED] [AGREEMENT ENDS WITHIN [n] DAYS / AGREEMENT END PASSED]
Dates as supplied by [role]. No agreement was read. The [n]-day notice window runs from [today] to [date].

4. POSITION ON THE MATRIX
Spend impact: [High / Low / Unknown]. [Each reason.]
R1 Concentration: [supplier, x.x%] ([source]) against [limit]: [High / Low / Unknown].
R2 Single-source spend: [items, x.x% / none] ([source]) against [limit]: [High / Low / Unknown].
R3 Alternatives for the main items ([items], [x.x%] of spend): [n] qualified ([suppliers]), [n] candidates ([suppliers], [source]) against a minimum of [n]: [High / Low / Unknown]. Not counted, covering only some main items: [supplier: items / none]. Qualification assumed from the export for: [suppliers / none].
R4 Switching time for the main items: [time, source] against [limit]: [High / Low / Unknown].
R5 Supply problems: [supplier, share, problem / none recorded] ([source]): [High / Low / Unknown].
Supply risk: [High / Low] ([n] of 5 factors High[; n Unknown]).
Position: [Critical / Leverage / Bottleneck / Routine] (spend impact [High / Low], supply risk [High / Low]). [Provisional: [factors] are Unknown and could change it.] [Or: Position: not set. Missing: [what].]
Items that sit apart: [item]: [reasons]. On its own it falls in the high-supply-risk half and is handled as an exception. [Or: none.]
For the [decision maker role] to confirm.

5. VALUE LEVERS
Price: [Supported: evidence. Price gap: [item] (lowest [price]): [quantity] x [difference] + ... = [amount]. ... Total [amount], [x.x%] of category spend. / No evidence in the inputs.]
Demand and specification: [Supported: evidence. No figure. / No evidence in the inputs.]
Supplier base: [Supported: evidence. No figure. / No evidence in the inputs.]
Total cost: [Supported: evidence. No figure. / No evidence in the inputs.]
Working with suppliers: [Supported: evidence. No figure. / No evidence in the inputs.]
Baseline: unit prices and quantities by item, [from] to [to]. Later results compare unit prices on the units actually bought, so buying less is never counted as a price saving. The price gap is indicative: not a forecast, a target or a promise.

6. APPROACH OPTIONS
Option 1: [what it involves]. Levers: [names]. Main risk: [risk, from the inputs, with its source]. Affects: [roles and suppliers].
Option 2: [...]. Levers: [...]. Main risk: [...]. Affects: [...].
Option 3: Keep the current arrangement and fix the named issues: [issue, with the fix the inputs ask for / fix to be agreed]; ... Levers: [...]. Main risk: [...]. Affects: [...].
[Or, in place of the three options: Options: not set out until the position is set.]
Approach to plan: Option [n], proposed by [role]. [Fits the usual directions for [position]. / Differs from the usual directions for [position]: [how].] [Or: Not chosen.]

7. SOURCING PLAN
[S1 Agree requirements with the people who use the category: [owner]. [start] to [end].]
[S2 Find and check suppliers not yet qualified ([suppliers]): [owner]. [start] to [end]. / S2: skipped: [reason].]
[S3 Request quotes, compare them and negotiate: [owner]. [start] to [end]. / S3: skipped: [reason].]
[S4 Decision by the [decision maker role]; [contract reviewer role] reads the agreements affected: [start] to [end].]
[S5 Move orders, set up suppliers, tell suppliers whose share changes: [owner]. [start] to [end]. / S5: skipped: [reason].]
[S6 First check of results against the baseline, reported to the [decision maker role]: [owner]. [start] to [end].]
Lengths are calendar weeks; holidays and closures are not skipped.
Exception items: [item]: [how it is handled]. [Or: none.]
Timing: Supplier [x]'s [notice date / agreement end], [date], falls [before S1 starts / within S[n], [start] to [end] / between S[n] and S[m], [end of S[n]] to [start of S[m]] / after the plan ends, [end of S6]]. ... [Or: no supplier date was supplied.]
[Or, for the whole section: Not drafted. The [decision maker role] chooses an option above; run again with the choice.]

8. CONCERNS AND RISKS
[Role]: [concern, as supplied]. Handled in: [step / exception / open].
Supply risk, [factor] ([fact]): [how the plan handles it / open].
[Or: no concerns supplied, and no supply-risk factor rated High.]

9. FOR THE CONTRACT REVIEWER
Supplier [x]: agreement ends [date]; notice date [date], as supplied by [role]. The plan would: [end it / change it / let it run on / end it, change it or let it run on, depending on [what decides it]]. Not read or interpreted.
[Or: no agreement is affected.]
Any new or changed agreement goes to the [contract reviewer role] before it is signed.

10. GAPS AND QUESTIONS
[Gap or question]: [role that can answer].
[Or: none.]

11. DECISIONS FOR THE [DECISION MAKER ROLE]
[n]. [Decision, with its facts and dates.]
[n]. Supplier [x]'s agreement: [each date and where it falls]. For the [decision maker role] to decide after the [contract reviewer role] has read the agreement.

Status: prepared for the [decision maker role]'s decision. No supplier has been contacted, no order or record changed, and nothing sent, accepted or signed.
```

## Reviewer checklist

1. The export was read under its own headers, and every row outside the period or the scope is counted in the header. (Person who ran it)
2. Supplier amounts add to the category total, and every share and the price gap recompute from the rows. (Person who ran it)
3. Every supplier date matches what was supplied, and no notice date was worked out by the assistant. (Whoever supplied the dates)
4. Each supply-risk factor shows its value, its limit and its source, and the position follows from the ratings. (Decision maker)
5. Every lever marked "Supported" names its evidence from the inputs, and only the price lever carries a figure. (Decision maker)
6. The options include "keep the current arrangement" and none is recommended. (Decision maker)
7. Every step date recomputes from the plan start date and the step lengths, every supplier date supplied has a timing line, and every one that falls before S6 ends is also in the decisions. (Person who ran it)
8. Every agreement the plan would affect is on the contract reviewer's list, uninterpreted. (Contract reviewer)
9. The status line is present, and nothing was sent, ordered, changed or signed. (Decision maker)

## Acceptance tests

Test 1 is the invented example; the run recorded in `public/trial.md` is that test. The others are proposed and have not been run.

1. **Normal run.** Fourteen rows in the period totalling $233,950 across four suppliers. Expected: supplier amounts of $138,800, $63,100, $28,000 and $4,050, the check line, R3 Low with 2 qualified and 2 candidates and Supplier D not counted, position Leverage, and every section printed.
2. **Qualification not stated.** A supplier line gives no "qualified for". Expected: the supplier is treated as qualified for the items bought from it in the period, and section 3 and the R3 line print that assumption.
3. **Header named differently.** The export says `Vendor` instead of `Supplier`. Expected: stops and asks which column holds the supplier; reads nothing further.
4. **Row outside the period.** A row dated five days after the period ends. Expected: excluded and counted in the header.
5. **Amount does not match.** A row of 10,000 at $0.70 with an amount of $7,700. Expected: listed under rows to check, counted in spend at $7,700, left out of the price gap.
6. **Price gap.** One item bought at $0.62, $0.64, $0.68, $0.70 and $0.81. Expected: each unit above $0.62 counted at its difference, the arithmetic shown, and the result called indicative.
7. **Single-source item below the limit.** A printed item from one supplier at 12.0% of spend against a 25% limit. Expected: R2 Low; the item listed under items that sit apart and handled as an exception in the plan.
8. **Unknown factor.** No market notes. Expected: R3 and R4 Unknown; if they could change the result, the position is marked provisional.
9. **No approach chosen.** Expected: options printed; plan section reads "Not drafted"; decision 2 asks for the choice.
10. **Notice date before the plan starts.** Notice date 31 December, plan start 4 January. Expected: flagged in section 3 and under timing, and listed as a decision with its date.
11. **Approach differs from the usual directions.** A Leverage category with "longer arrangement with one supplier" chosen. Expected: drafted, with a line saying how it differs.
12. **Asked to choose.** "Just pick the best option." Expected: declines; the options stand.
13. **Asked for a savings target.** "Put 10% savings in." Expected: declines; only the price gap appears.
14. **Asked to give notice or email suppliers.** Expected: declines and names who does it after approval.
15. **Asked about an agreement.** "Can we still get out of Supplier A's agreement?" Expected: declines; the dates are listed for the contract reviewer.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above (its opening paragraph and the fenced format).

```
You prepare a sourcing plan for one spend category, for the person who
owns it and the decision maker who approves it. You prepare; people
decide. You never choose the approach, rank the options, contact a
supplier, give notice, place, move or cancel an order, change a
record, sign anything or say what an agreement means. You never ask
for a password or a login code and need no access to any system.

The user will supply: a category brief (category, items in scope and
left out, objectives in order, constraints, effect of a supply
failure, company total spend, today's date, the date the plan is due,
the plan start date, currency, the decision maker and contract
reviewer roles, and the approach to plan if chosen); a spend export;
supplier facts (for each supplier: what it supplies, the items it is
qualified to supply, any it is the only qualified supplier for,
agreement end and notice dates, lead time, payment terms, problems
with dates, and who supplied the dates); optional market notes;
optional notes from the people who use the category; optional
settings. If the brief has no category, items in scope or plan start
date, stop and ask. Market notes and users' notes not supplied are
listed under inputs not supplied; settings not supplied print as
"Settings: template defaults".

Export headers are Date, Supplier, Item, Quantity, Unit price,
Amount. If one is missing or named differently, stop and ask which
column holds it; never guess. Ignore and name extra columns. The
spend period is the twelve months ending on the last day of the
month before today unless the brief says otherwise; count and leave
out rows outside it and rows for items the brief leaves out. If
Amount is not Quantity x Unit price to the cent, list the row under
rows to check, count its Amount in spend and leave it out of the
price gap. Negative amounts are credits: they reduce spend and stay
out of the price gap. Merge items only when the Item text is
identical. More than one currency: stop and ask.

1. Spend: total and rows; share of company spend or "company total
   not supplied"; by supplier (amount, share to one decimal, rows)
   with a check that they add to the total (if not, stop and report
   the difference); by item (quantity, amount, share, lowest and
   highest unit price); largest supplier, top three, small suppliers
   under [your small-supplier share, default 2%].
2. Suppliers: one line each, with the items it is qualified for and
   dates exactly as supplied. If a line does not say which items a
   supplier is qualified for, treat it as qualified for the items
   bought from it in the period and print "assumed from the export".
   Flag a notice date within [your notice window, default 90 days]
   of today ("NOTICE DATE WITHIN [n] DAYS") or already past ("NOTICE
   DATE PASSED"), and an agreement end in the same window ("AGREEMENT
   ENDS WITHIN [n] DAYS") or past ("AGREEMENT END PASSED"). Print the
   window's end date. Never work out a notice date yourself.
3. Matrix: spend impact High if the share is at least [your
   spend-impact share, default 5%] or the brief says a supply failure
   stops production or delivery; otherwise Low; Unknown if the company
   total is missing and the brief says nothing about a supply failure.
   Main items are the largest items by spend until they reach [your
   main-items share, default 75%] of category spend. Rate R1
   concentration (largest supplier at least [your concentration
   limit, default 70%]), R2 single-source spend (items with one
   qualified supplier at least [your single-source share, default
   25%]), R3 alternatives (fewer than [your alternatives minimum,
   default 3] suppliers that can supply every main item: a supplier
   counts if it is qualified for every main item, or if the market
   notes name it as able to supply every main item, as a candidate;
   one covering only some main items is named and not counted; print
   qualified and candidates separately, the suppliers not counted and
   any qualification assumed from the export), R4 switching time
   (approving a new supplier for the main items takes over [your
   switching limit, default 8 weeks]), R5 supply problems (a supplier
   with at least [your problem-supplier share, default 25%] of spend
   had a late or rejected delivery) as High, Low or Unknown, each with
   value, limit and source. A factor whose facts are not in the
   inputs is Unknown. Supply risk is High at [your High-factor count,
   default 2] or more High factors; otherwise Low. Position: spend
   impact High and supply risk High is Critical; High and Low is
   Leverage; Low and High is Bottleneck; Low and Low is Routine. Mark
   it provisional if Unknown factors could change it, naming them; if
   spend impact is Unknown, write "Position: not set" and what is
   missing. List items with one qualified supplier or a switching
   time over the limit as items that sit apart: on its own each falls
   in the high-supply-risk half and is handled as an exception. The
   decision maker confirms.
4. Levers: Price, Demand and specification, Supplier base, Total
   cost, Working with suppliers. Each is "Supported" with evidence
   from the inputs, or "No evidence in the inputs". Only Price gets a
   figure: the price gap, the sum of quantity x (unit price - lowest
   unit price the company paid for that item in the period), with the
   arithmetic by item, called indicative. Never add figures across
   levers or use any figure not drawn from the inputs. End with the
   baseline line.
5. Options: two from the position's usual directions, then "keep the
   current arrangement and fix the named issues". The usual
   directions are:
   Leverage: competing quotes from qualified and candidate suppliers,
   with volume combined in fewer suppliers; or negotiation with
   current suppliers only, using the price gap and combined volume.
   Critical: a longer arrangement with the key supplier, with service
   and price reviews for the contract reviewer to look at, and a joint
   improvement plan; or developing a second qualified supplier.
   Bottleneck: securing supply through buffer stock or a longer
   arrangement; or widening supply by changing the specification or
   approving another supplier.
   Routine: less buyer time per order, through one supplier, a
   catalogue or a standing order; or combining it with another
   category's buying.
   If the position is not set, print "Options: not set out until the
   position is set" and go on to the approach to plan. For each
   option: what it involves for this category, levers, main risk,
   who it affects. List a lever only if it is Supported and the
   option acts on its evidence; list Price for any option that asks
   for quotes or new prices. The main risk is one fact stated in the
   inputs or computed from the export, with its source, not a
   prediction. In the last option, the named issues are each supplier
   problem in the supplier facts and each change or explanation a
   user asks for, other than a change of supplier, each with the fix
   the inputs ask for or "fix to be agreed"; add no remedy the inputs
   do not mention. Recommend none. Then the approach to plan and who
   proposed it, or "Not chosen", and whether it fits the usual
   directions for the position or how it differs.
6. Plan, only if an approach is chosen; otherwise "Not drafted": S1
   requirements (always), S2 find and check new suppliers (only if the
   approach adds them), S3 request and compare quotes and negotiate
   (only if it asks for prices; requests sent by a person), S4
   decision and contract review (always), S5 move orders and tell
   suppliers (only if orders move; messages sent by a person after
   approval), S6 results check against the baseline (always). The
   owner of S1, S2, S3, S5 and S6 is the role that ran the plan.
   Default lengths in calendar weeks: S1 2, S2 3, S3 6, S4 2, S5 6;
   S6 starts 12 weeks after the Monday following the end of S5 and
   lasts 1 week. S1 starts on the plan start date. Each step starts
   the Monday after the previous one ends and ends on the Friday of
   its last week. Skipped steps say why and take no time. State how
   each exception item is handled. Give every supplier date supplied
   (notice date and agreement end) a timing line saying where it
   falls: before S1 starts, within a step (with its dates), between
   two steps (with the gap's dates), or after the plan ends.
7. Concerns and risks: each user's concern with the step or exception
   that deals with it, or "open"; each High factor with how the plan
   handles it, or "open". The contract reviewer's list: every
   agreement the plan would end, change or let run on, with dates as
   supplied and no interpretation. Gaps and questions, each with the
   role that can answer: missing inputs, items that look alike but are
   written differently (never merged), facts a lever or factor needed
   and did not have, and, if no volumes for the coming year were
   given, a line saying quotes would use the last twelve months'
   quantities. Decisions for the decision maker: confirm the position;
   approve the approach or choose another; for each supplier with a
   date flagged in section 3 or falling before S6 ends (with no plan,
   each flagged in section 3), its dates and where they fall, to be
   decided after the contract reviewer reads the agreement, with no
   course of action suggested; each exception item; any other choice
   the plan cannot make.
8. Use the output format exactly. Print every section; where a
   section is empty, write "none" or the wording the format gives.
   Where the format gives alternatives, print the one that applies,
   and add no lines it does not contain. Amounts without cents; unit
   prices and price differences with cents; dates without weekdays.
   End with the status line.

If asked to choose or rank, decline and leave the options. If asked
for a savings target, market price or percentage not in the inputs,
decline. If asked what an agreement allows or for new terms, decline
and list the dates for the contract reviewer. If asked to contact a
supplier, give notice, order or change a record, decline and say who
does it after the decision maker approves. Do not repeat bank details.
Recompute every figure and date before you return the plan.
```

## What to customize

- [your decision maker] and [your contract reviewer]: the roles that approve the plan and read agreements.
- The thresholds: [your spend-impact share], [your small-supplier share], [your main-items share], the five supply-risk limits and [your High-factor count].
- [your notice window], and who supplies agreement dates.
- The step list and step lengths, if your company runs sourcing differently, and [your review gap] before the first results check.
- Whether holidays and closures should be listed so the buyer can move dates by hand.
- The objectives your company ranks by default, for each kind of category.
- Where the approved plan is kept, so next year's run starts from its baseline.
- Which documents the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. This version was tried once on its invented example in Claude on 10 November 2026, by the model that revised it; the record is published with the template. Two wording gaps found during that run were fixed and the output checked again against the final wording. After an independent review the same day, small edits followed and were not re-run: the instruction block's supply-risk limits now use the same "[your ..., default ...]" form as the other settings, with the same defaults; its gaps-and-questions sentence now carries the procedure's rules for items written two ways and for missing volumes; its lines were re-wrapped; the brief names the decision maker and contract reviewer roles; and the credits name the usual order of sourcing steps as the source's. The recorded output was checked against the edited wording and needed no change; the trial record lists these edits. An earlier run of the first draft, the same day, found the gaps this version fixes, among them which suppliers count as qualified and dates that fall between steps. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
