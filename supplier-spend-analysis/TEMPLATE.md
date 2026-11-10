# Supplier spend analysis

Capability template, version 0.1.0.

## Purpose

Turn one accounts-payable export into an analysis of where the business spends with its suppliers, for the finance or operations lead: the rows cleaned (accounts left out, supplier spellings merged and listed, credit notes netted), spend grouped by category and by supplier, the few suppliers that take most of the spend, the tail of everyone else, the categories bought from more than one supplier, and the consolidation opportunities among them, each with its figures. The assistant reads no contract or price list. It prepares; it never chooses a supplier, contacts one, pays, changes a category or a record in the accounting system, or agrees anything.

## When to use it and when not to

Use it once or twice a year, before budget season, before a sourcing round, after an acquisition brings in a second set of suppliers, or when the owner asks where the money goes. It reads every supplier the business is billed by: ingredients and materials, packaging, freight, maintenance, rent, energy, services.

Do not use it:

- for subscriptions and recurring software charges, with seats, owners and renewal dates. A software subscription and vendor spend review does that;
- to check individual bills before a payment run. A supplier bill review does that, bill by bill;
- to compare quotes from competing suppliers for one purchase. A vendor quote comparison does that;
- to compare unit prices for the same item across suppliers. An accounts-payable export carries amounts, not quantities or item codes;
- to read a contract for prices, terms or notice periods, or to say what a clause means;
- for a budget, a forecast or a cash plan.

## Roles

- **Runs it:** the finance lead, finance manager or operations lead who can export accounts payable.
- **Keeps the category map:** the runner, with the budget holders.
- **Answers the questions:** the category owner named on the map, or the runner where none is named.
- **Decides what to act on:** [your decision-maker], such as the owner, managing director or finance director.
- **Talks to suppliers, runs a sourcing round, moves spend, recodes bills:** the people the business names. Always people.

## Inputs

1. **Settings,** typed by the runner: the company; today's date; the period start and end (at least three full calendar months; twelve is better, because seasonal suppliers then appear); the currency; the runner's role; [your decision-maker]; [your concentration line] (default 80%); [your consolidation floor], the category spend in the period below which a category with several suppliers is listed but not called an opportunity, typed either as an amount or as a percent of the spend analysed (default 1% of the spend analysed; a percent is turned into an amount once the spend analysed is known, and the amount is what the analysis prints); [your saving assumption], a low and a high percent (optional; with no assumption, no saving is estimated); [your accounts to leave out], the ledger accounts that are not supplier spend, such as sales tax, payroll taxes, loan repayments or transfers between the business's own accounts (optional); [your list length], how many suppliers are listed by name (default 50). If the period is shorter than three full months, stop and ask for a longer export.
2. **Accounts-payable export,** one row per bill or credit note for the period, with these default headers: `date` (YYYY-MM-DD, the bill date), `supplier`, `invoice` (the supplier's bill number), `description`, `account` (the ledger account the bill was coded to), `amount` (a credit note is negative). Use bills or payments, never both, so nothing is counted twice. If the export is missing, stop: there is nothing to analyse.
3. **Category map** (optional), one row per supplier, with these default headers: `supplier`, `category`, `owner`. The category is the need the supplier meets, named as finely as the business wants to compare suppliers: "cartons and boxes" rather than "packaging". The owner is the budget holder for that category. Any `owner` cell may be blank. If the map is missing, every category is the account the bill was coded to, and the analysis says so.

Headers are matched ignoring case. If a header is not found, stop and ask which column holds that information; never guess, and never use another column in its place. If the person confirms the export has no `invoice` or no `description` column, continue without it and say so under Not supplied or not checked. The other four headers are required.

The assistant works from files the person supplies. It needs no connection to the accounting system or the bank, and it never asks for a password, a login code or bank details.

## The procedure

1. **Check the rows.** One currency throughout, judged from the amounts and descriptions because the export has no currency column: no amount or description carries a currency symbol or code (such as € or EUR) other than the currency in the settings. Every date reads as a date and falls inside the period. Every amount is a number. Every row has a supplier. If any check fails, stop and ask about the rows concerned.
2. **Leave out what is not supplier spend.** Set aside every row coded to an account on [your accounts to leave out]. Count and total them by account, largest first. Nothing else is left out. If no accounts were listed, say "no accounts listed to leave out".
3. **Clean the supplier names.** Compare names ignoring case, punctuation, spaces at either end or doubled, and one legal ending at the end of the name: Inc, Incorporated, LLC, Ltd, Limited, Co, Corp, Corporation or PLC. Names that are equal after that are one supplier, shown under the spelling of its earliest row. List every merge with each spelling and the number of rows, so a person can undo it. Merge nothing else. Where one cleaned name, word for word, is the opening of a longer cleaned name (Supplier M and Supplier M Express), list the pair as a possible same supplier and keep them apart.
4. **Check for the same bill twice.** Two rows with the same supplier, after cleaning, and the same invoice number: stop and ask whether the bill was exported twice or genuinely billed twice. With no invoice number, use the same supplier, date and amount. Never drop a row on your own.
5. **Net the credit notes.** Each negative amount is netted against its supplier and its category. List each credit note with its supplier and amount. A supplier whose net spend is zero or less goes under "Net or zero after credits" and is left out of the ranking, the counts and the shares.
6. **Assign categories.** Match each supplier to the category map, comparing names the same way as step 3. A supplier on the map takes its category for every row. A supplier not on the map takes, row by row, the account the bill was coded to, marked "from the account"; a row with no account is "Not coded". Suppliers not on the map are listed, wherever they appear, in the order of the supplier list. Categories with the same name, ignoring case, are one category. A category's owner is the owner on the map for its suppliers; where its mapped suppliers carry different owners, list each distinct owner, joined by "and"; with no owner on the map, "not on record". "Not coded" has its own line under spend by category, is not counted as a category, and never appears among the same-need categories or the opportunities.
7. **Spend analysed.** The net total of the rows kept, the number of suppliers, bills and credit notes. A bill is a row with a positive amount; a credit note is never counted as a bill, here or anywhere else in the analysis.
8. **Spend by category,** highest first: the net spend, its share of the spend analysed to one decimal place, the number of suppliers and of bills (credit notes not counted), and the owner. Mark a category "includes from the account" when any supplier in it was placed by its account. Each share is rounded on its own, so the shares may not add to exactly 100.0.
9. **Spend by supplier,** highest first, ties in name order: rank, net spend, share, cumulative share, category (with the split and each category's spend, where a supplier placed by its account falls in more than one; such a supplier counts once in each of those categories' supplier counts and once in the number of suppliers), bills and credit notes, and its group. When there are more than [your list length] suppliers (default 50), list that many and give the rest as one line with their count and total.
10. **Concentration.** Walk down the supplier list adding spend. The concentration group is every supplier down to and including the first one at which the unrounded cumulative share reaches [your concentration line]. Give the count, the share of suppliers, the spend and its share, the names, and the largest single supplier's share.
11. **Tail.** Every supplier after the concentration group. Give the count, the share of suppliers, the spend and its share, the number of bills, the average bill (tail spend divided by tail bills), the suppliers billed only once in the period, and the tail spend by category, largest first, with the number of tail suppliers in each; tail spend that is not coded is the last entry on that line, as "Not coded", as it is under spend by category.
12. **Same need, more than one supplier.** Every category with two or more suppliers, highest spend first: the category spend, the number of suppliers, and each supplier's spend and share of the category. Mark any category under [your consolidation floor] "below the consolidation floor".
13. **Consolidation opportunities.** Every same-need category at or above [your consolidation floor], ordered by the spend with suppliers other than the largest, highest first. For each: the category spend and the number of suppliers; the largest supplier by spend, its spend and share, marked "not a recommendation"; the spend with the others and their number of bills. With a saving assumption, apply the low and high percent to the category's spend and give both figures to the cent, labelled "an assumption, not a quote". Without one, write "No saving assumption supplied; no saving estimated." Never estimate a saving from any other figure, and never say which supplier to keep.
14. **Questions.** Write a question only where a fact calls for it, each with its fact: one per possible same supplier (are they the same supplier?), to the runner; one covering every supplier not on the category map (which category does each belong in?), to the runner; one per consolidation opportunity (do these suppliers supply the same thing, and is there a reason each is used, such as a specification, a site or a backup?), to the category owner or, with none on record, the runner. The runner decides whether to ask them; the assistant contacts no one.
15. **Decisions for [your decision-maker].** One per consolidation opportunity, in the same order (should the category owner look into moving the category to fewer suppliers, once that category's question is answered; a vendor quote comparison can prepare the choice), then one for the tail when there is one (should anyone look at whether the tail's spend can go through suppliers already used, and who). Write each as its facts, then the question. An opportunity's facts are the category spend, the number of suppliers, the spend with suppliers other than the largest and, with a saving assumption, the saving range; with none, leave the saving out of the decision. The tail's facts are its number of suppliers, its spend and share, its bills, and how many were billed once. Recommend nothing unless [your decision-maker] asks; if asked, add one suggestion for that decision, labelled as made at their request, with the facts for it and the facts against it.
16. **Not supplied or not checked.** Always first: no contract, price list, quote or delivery record was read, so whether two suppliers sell the same item, at what price or on what terms is not known from this export. Then: categories are as set on the category map or the account each bill was coded to; spend is what was billed in the period, not what was committed or paid; names that differ other than by case, punctuation, spacing or a legal ending were not merged. Then each input that was missing.
17. **Return the analysis** to the runner, in the output format and its fixed order, adding no section or commentary beyond it. Where a section has nothing in it, print the word the format gives for that case. Write every amount with the currency symbol, thousands separators and two decimals, and a negative amount with a minus sign before the symbol (-$420.00). Use the singular for one (1 bill, 1 supplier, 1 row). Nothing goes to a supplier, a budget holder or the decision-maker from the assistant.

## Exceptions and stop conditions

- **Export missing, or a period shorter than three full months:** stop and ask.
- **A header not found:** stop and ask which column holds it; never guess.
- **A row dated outside the period, an amount that is not a number, a row with no supplier, or more than one currency:** stop and ask about those rows.
- **The same supplier and invoice number twice** (or, with no invoice number, the same supplier, date and amount): stop and ask; never drop either row.
- **Asked which supplier to keep, drop or move spend to:** recommend nothing unless the decision-maker asks; then follow step 15.
- **Asked for a saving without a saving assumption:** decline to invent one; ask the person for the low and high percent they want applied, and label it as their assumption.
- **Asked to contact a supplier, start a sourcing round, recode bills, change the category map in the accounting system, or pay anything:** decline and name the role that does it.
- **The person pastes a contract or price list and asks for prices, terms or notice dates:** decline to read it for terms or meaning; the analysis works from the export only.
- **The export contains bank details, a full card number, a password or a login code:** do not repeat them; tell the person to remove them from the source.
- **A supplier is a person employed by the business,** such as an expense reimbursement paid through accounts payable: show the row as "employee reimbursement" with its amount and account, without the name.

## Output format

```
SUPPLIER SPEND ANALYSIS: [company], [period start] to [period end]

For: [runner role]. Decisions by: [decision-maker role]. Prepared [weekday date] from [the inputs used, with row counts]. All figures are for the period, in [currency]; nothing is annualised.

CLEANING
Rows read: [n]. Left out: [n] rows, [amount] ([account]: [n] rows, [amount]; ... largest first). / Left out: none; no accounts listed to leave out.
Credit notes: [n], [amount], netted against their suppliers ([supplier] [amount]; ...). / Credit notes: none.
Names merged: [shown name]: "[spelling]", "[spelling]" ([n] rows); ... / Names merged: none.
Possible same supplier, not merged: [name] and [name]; ... / Possible same supplier, not merged: none.
Not coded: [n] rows, [amount] ([supplier] [amount]; ...). / Not coded: none.
Not on the category map: [supplier] (placed by its account, [account]); [supplier] (not coded); ... / Not on the category map: none. / Category map not supplied: every category is the account.
Net or zero after credits: [supplier] [amount]; ... / Net or zero after credits: none.
Spend analysed: [amount], [n] suppliers, [n] bills and [n] credit notes.

SUMMARY
[n] suppliers ([n] in the concentration group) across [n] categories[, plus [amount] not coded].
Concentration: [n] of [n] suppliers ([n.n]%) take [n.n]% of spend ([amount]).
Tail: [n] suppliers ([n.n]%) take [n.n]% ([amount]) in [n] bills.
Same need, more than one supplier: [n] categories. Consolidation opportunities: [n].

SPEND BY CATEGORY (highest first; shares rounded to one decimal place)
[Category][ (includes from the account)]: [amount], [n.n]%, [n] supplier(s), [n] bill(s). Owner: [owner / owner and owner / not on record].
Not coded: [amount], [n.n]%, [n] supplier(s), [n] bill(s).
/ None.

SPEND BY SUPPLIER (highest first)
[rank]. [Supplier]: [amount], [n.n]% (cumulative [n.n]%). [Category][ (from the account)] / Not coded. [n] bill(s)[, [n] credit note(s)]. [Concentration group / Tail].
[[n] more suppliers in the tail, [amount].]
/ None.

CONCENTRATION (line: [n]%)
[n] of [n] suppliers ([n.n]%) take [amount], [n.n]% of spend: [supplier]; ... The group ends at the first supplier whose cumulative share reaches [n]%.
Largest supplier: [supplier], [n.n]% of spend.

TAIL
[n] suppliers ([n.n]% of suppliers) take [amount], [n.n]% of spend, in [n] bills; average bill [amount]. Billed once in the period: [n] ([supplier]; ...) / Billed once in the period: none.
Tail spend by category: [category] [amount] ([n] supplier(s)); ...
/ None.

SAME NEED, MORE THAN ONE SUPPLIER
[Category]: [amount], [n] suppliers: [supplier] [amount] ([n.n]%); ... [Below the consolidation floor of [amount].]
/ None.

CONSOLIDATION OPPORTUNITIES: [n] (categories at or above [floor] with more than one supplier)
[n]. [Category]: [amount] with [n] suppliers. Largest by spend (not a recommendation): [supplier], [amount] ([n.n]%). With the other [n]: [amount] in [n] bill(s). At your assumption of [low]% to [high]% of the category's spend: [amount] to [amount] in the period; an assumption, not a quote. / No saving assumption supplied; no saving estimated.
/ None.

QUESTIONS: [n], for the [runner role] to decide whether to ask
[n]. To the [owner or runner role]: [the fact]. [The question.]
/ None.

DECISIONS FOR THE [DECISION-MAKER ROLE]: [n]
[n]. [The facts.] [The question.]
[Suggestion, made at the [decision-maker role]'s request: [one option], because [facts]. Against it: [facts].]
/ None.

NOT SUPPLIED OR NOT CHECKED
No contract, price list, quote or delivery record was read, so whether two suppliers sell the same item, at what price or on what terms is not known from this export. Categories are as set on the category map or the account each bill was coded to. Spend is what was billed in the period, not what was committed or paid. Names that differ other than by case, punctuation, spacing or a legal ending were not merged. [Each input that was missing.]

Every figure traces to the inputs supplied for [company] on [date]. Nothing has been sent, paid, changed or agreed with any supplier.
```

## Reviewer checklist

1. Rows read equals rows left out plus bills plus credit notes, and the left-out total adds up by account. (Runner)
2. Every merge of supplier names is listed, and none goes beyond case, punctuation, spacing or one legal ending. (Runner)
3. The spend analysed equals the sum of the supplier lines, and equals the sum of the category lines including "Not coded". (Finance lead)
4. The concentration group stops at the first supplier whose cumulative share reaches the line, and the tail is every supplier after it. (Finance lead)
5. Every same-need category and every opportunity recomputes from the supplier lines, and the floor is applied as set. (Finance lead)
6. Any saving figure uses the person's own assumption on the category's spend and is labelled as an assumption; with no assumption, there is no saving figure. (Finance lead)
7. No line names a supplier to keep, drop or move to, unless the decision-maker asked. (Decision-maker)
8. The analysis keeps the fixed section order, prints the empty-section word where a section is empty, and adds nothing beyond the output format. (Runner)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary quarter.** A three-month export with 24 suppliers, a category map for most of them, two accounts to leave out. Expected: every section filled; totals recompute; rows read equals left out plus bills plus credit notes.
2. **Header does not match.** The export's columns are `posted`, `vendor`, `ref`, `memo`, `gl`, `value`. Expected: stops and asks which column holds which; analyses nothing.
3. **Same bill twice.** Two rows for one supplier with the same invoice number. Expected: stops and asks whether it was exported twice; drops neither.
4. **Spellings.** "Supplier H Ltd", "SUPPLIER H LTD." and "Supplier H". Expected: one supplier, shown as "Supplier H Ltd", the merge listed with three spellings and three rows.
5. **Look-alike names.** "Supplier M" and "Supplier M Express". Expected: kept apart, listed as a possible same supplier, one question to the runner.
6. **Credit note.** A supplier with three bills and one credit note of -$420.00. Expected: netted; listed under credit notes; the supplier line shows the credit note.
7. **Concentration line.** Cumulative shares of 78.3% and then 81.9% with an 80% line. Expected: the group ends at the supplier that takes it to 81.9%.
8. **Below the floor.** A category with two suppliers and $6,880 of spend, floor $10,000. Expected: listed under same need, marked below the floor, not an opportunity, no decision.
9. **No saving assumption.** Expected: every opportunity says "No saving assumption supplied; no saving estimated."; no saving figure anywhere.
10. **Asked which supplier to keep.** Expected: recommends nothing unless the decision-maker asks; then one labelled suggestion per decision asked about, with facts for and against.
11. **Asked to email the suppliers.** Expected: declines, names the role that does it, drafts nothing to a supplier.
12. **No category map.** Expected: every category is the account, marked from the account; the cleaning section says the map was not supplied.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a supplier spend analysis from an accounts-payable export,
for a finance or operations lead. You prepare; people decide. You never
choose a supplier, contact a supplier or a budget holder, pay, recode a
bill, change a category or any record in the accounting system, agree
anything or send anything. You never read a contract or price list for
prices or terms. You never ask for a password, a login code or bank
details, and you need no access to any system.

The user will supply: settings (company, today's date, period start and
end of at least three full months, currency, runner role,
decision-maker, concentration line default 80%, consolidation floor
typed as an amount or as a percent of spend analysed, default 1% of
spend analysed, an optional saving assumption as a low and high
percent, optional accounts to leave out, list length default 50); an
accounts-payable export (date, supplier, invoice, description, account,
amount; credit notes negative), of bills or of payments, never both, so
nothing is counted twice; an optional category map (supplier, category,
owner).

Stop and ask when: the export is missing or the period is under three
full months; a header is not found (match ignoring case; ask which
column holds it; never guess). If the person confirms there is no
invoice or description column, continue and say so. If the map is
missing, use the account as the category and say so.

1. Check the rows: one currency (no amount or description carries a
   currency symbol or code other than the settings' currency); every
   date a date inside the period; every amount a number; every row has
   a supplier. If not, stop and ask about those rows.
2. Set aside rows coded to the accounts to leave out; count and total
   them by account, largest first. Nothing else is left out.
3. Clean names: ignore case, punctuation, extra spaces and one final
   legal ending (Inc, Incorporated, LLC, Ltd, Limited, Co, Corp,
   Corporation, PLC). Equal names are one supplier, shown under the
   earliest row's spelling; list every merge with its spellings and row
   count. Merge nothing else. When one cleaned name is the whole-word
   start of another, list the pair as a possible same supplier and keep
   them apart.
4. Two rows with the same cleaned supplier and invoice number (with no
   invoice number: supplier, date and amount): stop and ask whether it
   was exported twice or billed twice. Never drop a row.
5. Net credit notes against their supplier and category and list them.
   A supplier with net spend of zero or less goes under "Net or zero
   after credits" and out of the ranking, counts and shares.
6. Category: from the map for a supplier on it; otherwise the row's
   account, marked "from the account"; no account is "Not coded". List
   suppliers not on the map in supplier-list order. Same names ignoring
   case are one category. Owner from the map; where its mapped
   suppliers have different owners, each distinct owner joined by
   "and"; else "not on record". "Not coded" has its own line, is not
   counted as a category, and is never a same-need line or an
   opportunity.
7. Spend analysed: net total, suppliers, bills and credit notes. A bill
   is a row with a positive amount; a credit note is never counted as a
   bill anywhere.
8. Spend by category, highest first: spend, share to one decimal place
   (each rounded on its own), suppliers, bills, owner; mark "includes
   from the account" where any supplier was placed by its account.
9. Spend by supplier, highest first, ties by name: rank, spend, share,
   cumulative share, category (where a supplier placed by its account
   falls in more than one, the split with each category's spend; it
   counts once in each of those categories' supplier counts and once
   in the number of suppliers), bills, credit notes, group. Over the
   list length, list that many and total the rest in one line.
10. Concentration group: down to and including the first supplier at
   which the unrounded cumulative share reaches the line. Give count,
   share of suppliers, spend, share and names, and the largest
   supplier's share.
11. Tail: every supplier after the group. Count, share of suppliers,
   spend, share, bills, average bill (tail spend / tail bills),
   suppliers billed once, and tail spend by category, largest first,
   with tail suppliers in each; not-coded tail spend is the last entry,
   as "Not coded".
12. Same need: every category with 2+ suppliers, highest spend first,
   each supplier's spend and share of the category; mark those under
   the floor "below the consolidation floor".
13. Consolidation opportunities: same-need categories at or above the
   floor, ordered by spend with suppliers other than the largest,
   highest first. Give the largest "by spend (not a recommendation)",
   the others' spend and bills, and, only with a saving assumption, low
   and high percent of the category's spend to the cent, "an
   assumption, not a quote". Without one: "No saving assumption
   supplied; no saving estimated." Never estimate a saving from any
   other figure, and never say which supplier to keep.
14. Questions, each with its fact: each possible same supplier, and one
   covering every supplier not on the map, to the runner; each
   opportunity, to its category owner or else the runner (same thing
   supplied? a reason for each, such as a specification, a site or a
   backup?). Ask a question only where a fact calls for it.
15. Decisions for the decision-maker, each as its facts then the
   question: each opportunity, in the same order (category spend,
   suppliers, spend with the others, and the saving range only with an
   assumption; should the owner look into fewer suppliers once its
   question is answered; a vendor quote comparison can prepare it);
   then the tail, if any (its suppliers, spend and share, bills, how
   many billed once; should anyone look at whether it can go through
   suppliers already used, and who). Recommend nothing unless the
   decision-maker asks; then one suggestion per decision asked about,
   labelled as made at their request, with facts for and against.
16. NOT SUPPLIED OR NOT CHECKED opens with: "No contract, price list,
   quote or delivery record was read, so whether two suppliers sell the
   same item, at what price or on what terms is not known from this
   export." Then: "Categories are as set on the category map or the
   account each bill was coded to. Spend is what was billed in the
   period, not what was committed or paid. Names that differ other than
   by case, punctuation, spacing or a legal ending were not merged."
   Then each input that was missing.
17. Use the output format exactly, in its fixed order, adding nothing,
   printing the empty-section word where a section is empty. Amounts
   carry the currency symbol, thousands separators and two decimals; a
   negative has a minus sign before the symbol (-$420.00). Singular for
   one. End with: "Every figure traces to the inputs supplied for
   [company] on [date]. Nothing has been sent, paid, changed or agreed
   with any supplier."

If asked to contact a supplier, start a sourcing round, recode bills,
change the map in the accounting system or pay, decline and name the
role that does it. If asked for a saving without an assumption, ask for
the person's low and high percent instead of inventing one. If given a
contract or price list and asked for prices, terms or notice dates,
decline; the analysis works from the export only. Do not repeat bank
details, card numbers, passwords or login codes; tell the user to
remove them. Show a person employed by the business as "employee
reimbursement", with its amount and account, without the name.
Recompute every figure before you return the analysis.
```

## What to customize

- [your decision-maker], and who keeps the category map between analyses.
- [your accounts to leave out]: the ledger accounts that are not supplier spend in your books.
- [your concentration line]: the cumulative share that defines the concentration group. The default is 80%.
- [your consolidation floor]: the category spend in the period worth calling an opportunity. The default is 1% of the spend analysed.
- [your saving assumption]: the low and high percent your business is willing to assume for a consolidated category, or none.
- [your list length]: how many suppliers are listed by name before the rest are totalled. The default is 50.
- The column headers your accounting system's export actually uses, and whether you export bills or payments.
- Your category names: fine enough that two suppliers in one category really meet the same need.
- The legal endings common where your suppliers trade, if they differ from the list in step 3.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried once on its invented example in Claude on 10 November 2026, by a model given only this template and the example's inputs; the record is published with the template and lists the small edits made afterward that have not been run again. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
