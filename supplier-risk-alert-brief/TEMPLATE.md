# Supplier risk alert brief

Capability template, version 0.1.0.

## Purpose

Prepare a dated brief for the buyer or procurement lead on the day something happens to a supplier the business already depends on: a sign of money trouble, a site or production line stopped, a regulator's or certifier's action, or a failure at one of the supplier's own suppliers. The brief says what happened, in the words of numbered sources with their dates; what the business buys from that supplier; how many days of stock it holds against how long another source would take; how exposed each item is; what is not yet known; and the actions a person should decide, each with an owner and a date. Estimates carry the word estimate, and nothing is stated that the sources do not say. The assistant prepares and checks. It never contacts the supplier, places, moves or cancels an order, changes a stock setting or a record, or pays anything; a person decides every contact and every switch.

## When to use it and when not to

Use it as soon as a report reaches the business about a supplier it already buys from: a news item, a registry filing, a regulator's notice, a message from the supplier, or something a colleague heard. Run it again when a new report arrives or on the next review date the brief sets.

Do not use it:

- to vet or choose a new supplier. That is a separate assessment, done before anything is bought;
- for a formal notice to the supplier about a billing or delivery problem. Supplier issue notice prepares that;
- to analyse spend across suppliers or categories. Supplier spend analysis does that;
- to judge whether the supplier will survive, how long a stoppage will last, or what the supply agreement allows. The brief reports what the sources say; questions about the agreement go to [your contract reviewer];
- when nothing has happened. A routine review of a supplier with no event is not an alert.

## Roles

- **Runs it:** the buyer, or whoever first sees the report.
- **Reads it and decides what happens next:** [your brief reader], usually the procurement lead.
- **Owns each action:** the role your settings name for that kind of action (contact with the supplier and open orders; other sources and qualification; the production plan and usage figures; payments). The one exception is the decision whether to put the questions to the supplier: [your brief reader] owns it, not the owner of contact with the supplier.
- **Decides whether anyone contacts the supplier, and whether any order moves to another source:** [your brief reader].
- **Answers questions about the supply agreement:** [your contract reviewer].
- **Clears any report that dealing with the supplier is barred, such as a sanctions listing or a government order:** [your compliance lead].

## Inputs

1. **The reports.** Every report of the event, each with: who published or said it; its kind (an official record such as a registry filing or a regulator's notice; the supplier in writing; a news or trade publication; or a person, with no document); the date it was published or said; the date it reached the business; and its text pasted in full, or the person's note of what was said. Each becomes a numbered source, S1, S2 and so on. If no report names its source and its date, stop and ask: the brief cannot say where a fact came from.
2. **The event.** Whether it happened at the supplier itself or at one of the supplier's own suppliers; if the latter, which one and what it supplies, as far as the person knows. If unknown, write "sub-suppliers not known". When the event is at the supplier itself, its own suppliers are not part of this event, even when nobody knows who they are.
3. **The items export:** the rows for this supplier only, from the item list or stock system. Default column headers: `item, description, sole_source, spend_12m, on_hand, weekly_use, open_order_qty, open_order_due, other_source, days_to_other_supply`. `other_source` names an approved other source or says `none`. `days_to_other_supply` is the calendar days until goods from another source could arrive, including the time to approve a new source where none is approved; leave it blank when nobody knows. A number followed by `est` is an estimate. If the headers do not match these, stop and ask which column holds which; never guess. If the export has no rows, stop and ask whether the business buys from this supplier at all.
4. **Where each item is used** (optional): the products, sites or customer orders that depend on it. If not supplied, write "where used not supplied" and propose no action about products or customers.
5. **Notes** (optional): dated facts from colleagues, such as how an estimate was reached.
6. **The settings.** The date prepared; who prepares the brief and who reads it; working days and closed dates; the owner role for each kind of action; [your margin days] (default 14); action deadlines in working days after the date prepared (defaults: Not assessed 1, High 2, Medium 5, Low at the next review); the next review in working days by overall exposure (defaults: Not assessed 1, High 2, Medium 5, Low 20); [your contract reviewer]; [your compliance lead]; the currency. If the date prepared or the working days are missing, stop and ask; if anything else is missing, use the defaults and say so.
7. **The last brief on this supplier** (optional), to show what has changed. If none, write "first brief on this supplier".

The assistant works only from what the person supplies. It needs no connection to a news service, a credit agency, the stock system or email, and it never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Every report has a named source and a date; the export headers match or have been mapped by the person; each item appears once. Stop on anything listed under Inputs as a stop.
2. **Number and label the sources.** Give each report a number in the order it reached the business. Label each fact by its strongest source: **Confirmed** when an official record or the supplier in writing states it; **Reported** when only a news or trade publication states it; **Heard** when only a person said it, with no document. Something the supplier says it will do (restart, ship, recover) is labelled **supplier's statement**: it is a promise, not a confirmed fact.
3. **Write what happened.** Name the kind of event: money trouble, a site or production stopped, a regulator's or certifier's action, a failure at one of the supplier's own suppliers, a trade or transport disruption, or other (in the source's words). State each fact in the terms its source uses, with its label and source numbers. Never add a cause, a duration, a consequence or a judgment of the supplier's health that no source states. Where two sources disagree on a fact, show both with their dates and choose neither.
4. **List what the business buys.** For each row: item, description, sole source or not, spend in the last 12 months, stock on hand, weekly use, open orders with quantity and due date, and where used. Total the spend. Spend is shown for context and never changes a rating.
5. **Work out the cover.** The planning assumption is that nothing more arrives from the supplier after the date prepared, open orders included; say so on the brief. Cover on hand in calendar days = on hand × 7 ÷ weekly use, rounded down. Run-out date = date prepared + cover days. Cover if open orders arrive = (on hand + open order quantity) × 7 ÷ weekly use, rounded down, shown for reference only. Show the working. A figure built from an estimate is itself marked estimate: once at the end of the clause it belongs to, as the output format shows, and again wherever it is repeated, such as the gap days in a rating reason.
6. **Set it against another source.** Gap = days to other supply − cover on hand. A positive gap is the stretch with no stock: give its days and its first and last dates (from the run-out date to the date prepared + days to other supply). Otherwise give the days the cover lasts beyond.
7. **Rate each item.**
   - **Not assessed:** on hand, weekly use or days to other supply is blank, or weekly use is zero. A missing figure never counts as a good one.
   - **High:** the cover on hand runs out before another source could supply (a positive gap).
   - **Medium:** the cover lasts beyond the time another source needs by 0 to [your margin days] days.
   - **Low:** the cover lasts beyond it by more than [your margin days] days.
   No rating is lowered by low spend, by open orders, or by the supplier's statement. Overall exposure: High if any item is High; otherwise Not assessed if any item is Not assessed; otherwise Medium if any item is Medium; otherwise Low. Name the item that sets it.
8. **Show the supplier's statement.** If the supplier has said what it will still ship or when it will recover, work out the cover that would follow if that holds, and label it "supplier's statement, not confirmed". It never replaces the rating.
9. **Sub-suppliers.** When the event is at one of the supplier's own suppliers, state which one and what it supplies, as the person gave it. If a source states how many days of that material the supplier holds, give the date the supplier's deliveries could continue to on its word, labelled "supplier's statement, not confirmed". The rating still assumes nothing more arrives after the date prepared. When the event is at the supplier itself, write "not part of this event", even when the supplier's own suppliers are not known; they are then not listed under what is not known.
10. **List what is not known.** Every fact the brief needs and the sources do not give: when a stoppage ends, an estimate not yet confirmed, a blank in the export, a Heard report not yet checked, sub-suppliers not known (only when the event is at one of them and the person cannot name it). Name what would settle each.
11. **Propose actions.** Each action names the item or source it rests on, an owner from the settings, and a date. Its deadline is the shortest that applies among the items it addresses: Not assessed 1 working day, High 2, Medium 5 (or your settings), counted forward from the date prepared, which is not counted, skipping closed dates. Choose only from what the facts call for:
    - decide whether to put the questions below to the supplier, and who does it (always first when there are questions). Its owner is [your brief reader], not the owner of contact with the supplier;
    - ask an approved other source for capacity, price and lead time, for any item rated High or Medium that has one;
    - decide whether to start approving another source now, for any item rated High with none;
    - review the production plan or customer commitments for what the item is used in, against its run-out date, only when where-used is supplied, for any item not rated Low whose cover on hand is known, including a Not assessed item whose cover rests on an estimate;
    - find a missing figure, for each item rated Not assessed;
    - confirm an estimate that an item's cover, gap or rating rests on, including an estimated weekly use on an item rated Not assessed, from records or from whoever can give the real figure.
    List the actions in the order of the items they address, the decision about questions first. List items rated Low under "No action before the next review".
12. **Write the questions for the supplier.** Short, factual questions that would settle what is not known, each with the source it follows from. Questions only: no message, no letter, no demand, nothing about the agreement.
13. **Set the next review** by overall exposure, in working days after the date prepared, and add "or sooner if a new report arrives".
14. **Return the draft** to the person who ran it, for [your brief reader]. Nothing is sent and nobody is contacted by the assistant.

## Exceptions and stop conditions

- **No report names its source and date:** stop and ask.
- **Export headers that do not match the defaults:** stop and ask which column holds which. Never guess a mapping.
- **No rows for the supplier, or an item that appears twice:** stop and ask.
- **A report says the supplier is on a sanctions list, or that a government order bars dealing with it:** put it first, on the "Stop before any order or payment" line, for [your compliance lead]; prepare the rest of the brief.
- **Sources disagree on a fact:** show each with its date; choose neither; add a question.
- **Asked whether the supplier will fail, how long the stoppage will last, or what its credit standing is:** decline to judge; give what the sources say, with their labels.
- **Asked what the supply agreement allows, such as suspending orders, ending the agreement or claiming for losses:** decline; refer it to [your contract reviewer].
- **Asked to contact the supplier, place, move or cancel an order, change a stock setting or a record, or make or hold a payment:** decline and name the role that decides.
- **A report names a private individual,** such as an injured worker or an employee in a dispute: refer to them by role only and leave their personal details out.
- **A document contains a password, a login code or bank details:** do not repeat them; tell the person to remove them from the source.

## Output format

```
SUPPLIER RISK ALERT BRIEF: [supplier], [the event in a few words]

For: [reader role]. Prepared: [weekday date] by [role]. Next review: [weekday date], or sooner if a new report arrives.
Change since last brief: [first brief on this supplier / what changed since the brief of [date]].
Overall exposure: [High / Medium / Low / Not assessed], set by [item].
Stop before any order or payment: [the report, what it says, for [compliance role]] / none.

WHAT HAPPENED
Kind of event: [money trouble / a site or production stopped / a regulator's or certifier's action / a failure at one of the supplier's own suppliers / a trade or transport disruption / other: the source's words].
Where: [at the supplier / at [sub-supplier], which supplies [supplier] with [what]].
- [Fact, in the source's terms] ([Confirmed / Reported / Heard / supplier's statement]; [S numbers]).
Sources:
S[n]. [Publisher, or person by role], [kind]. Published or said: [date, and the time if given]. Reached us: [date, and the time if given]. "[the words the facts rest on]"
Disagreements between sources: [fact: S[n] says ..., S[n] says ...] / none.

WHAT WE BUY FROM THEM
Spend in the last 12 months: [total] across [n] items. Spend is shown for context and changes no rating.
- [Item], [description]. Sole source: [yes / no]. Spend: [amount]. On hand: [qty]. Weekly use: [qty][ (estimate)] / not stated. Open orders: [qty] due [weekday date] / none. Used in: [products, sites or orders] / where used not supplied.

EXPOSURE
Assumption: nothing more arrives from [supplier] after [date prepared], open orders included. This is a planning assumption, not a forecast.
- [Item]: cover on hand [n] days ([on hand] x 7 / [weekly use]), runs out [weekday date][ (estimate)] / cover not known. Another source: could supply in [n] days ([other source] / none approved)[ (estimate)] / not known. Gap: [n] days with no stock, [weekday date] to [weekday date][ (estimate)] / cover lasts [n] days beyond / not known. If open orders arrive: [n] days / no open orders. Rating: [High / Medium / Low / Not assessed]: [the reason, with any figure built from an estimate marked (estimate)].
If [supplier]'s statement holds: [what it says, with S number, and the cover that would follow]. Supplier's statement, not confirmed. / No statement from the supplier.
Sub-suppliers: [not part of this event (the event is at the supplier itself, whether or not its own suppliers are known) / the event is at [sub-supplier]; [supplier]'s stated stock of [material]: [n] days ([S number]), so its deliveries could continue to [date] on its word / not stated / sub-suppliers not known].

WHAT WE DO NOT KNOW
[n]. [What is not known, and what would settle it.] / none

ACTIONS FOR A PERSON TO DECIDE
[n]. [Action]. Owner: [role]. By: [weekday date]. Why: [item, rating or fact, with S number].
No action before the next review: [items rated Low] / none.
Decided only by a person: whether and when anyone contacts [supplier], moving or cancelling any order, any change to stock levels, and any payment.

QUESTIONS TO PUT TO [SUPPLIER]
For [contact role], if [reader role] agrees to contact [supplier].
[n]. [Question] ([S number or item]) / none

Every fact traces to a numbered source, the items export of [date] or the notes supplied. Estimates are labelled. Draft for [reader role]. Nothing has been sent, ordered, paid or changed, and nobody has been contacted.
```

## Reviewer checklist

1. Every fact under What happened carries a label and a source number, and says no more than its source. (Person who ran it)
2. Each label is right: Confirmed only from an official record or the supplier in writing, Heard only from a person, and promises marked as the supplier's statement. (Brief reader)
3. Every cover figure, run-out date and gap is recalculated and matches the export. (Person who ran it)
4. No item is rated Low or Medium because of low spend, open orders or the supplier's statement, and every blank is Not assessed. (Brief reader)
5. Every action has an owner, a date that follows the deadline rule, and the item or source it rests on. (Brief reader)
6. The questions for the supplier are questions only, with nothing about the agreement and no demand. (Brief reader)
7. No private individual is named and no bank details are repeated. (Person who ran it)
8. Any report of a sanctions listing or a government order is on the stop line and with the compliance lead before any order or payment. (Compliance lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Sole source, short cover.** 520 on hand, 130 a week, another source estimated at 98 days. Expected: cover 28 days, a 70-day gap with both dates, rated High, the dates marked estimate.
2. **Approved other source, long cover.** 900 on hand, 75 a week, another source in 35 days, margin 14. Expected: cover 84 days, lasts 49 days beyond, rated Low, listed under no action before the next review.
3. **Blank replacement time.** A sole-source item with `days_to_other_supply` blank and low spend. Expected: Not assessed, never Low; an action to find the figure due in 1 working day; the spend line says it changes no rating.
4. **Supplier's promise.** The supplier writes that 400 finished units will ship this week. Expected: shown as the supplier's statement with the cover that would follow; the rating unchanged.
5. **News report only.** One trade-press item, nothing from the supplier. Expected: facts labelled Reported; a question asking the supplier to confirm.
6. **Something heard.** A colleague heard of more damage. Expected: labelled Heard; listed under what we do not know; a question for the supplier.
7. **Sources disagree.** A news item says the site is closed for a month; the supplier writes two weeks. Expected: both shown with dates under disagreements; neither chosen.
8. **Sub-supplier failure.** The supplier's own resin supplier enters insolvency proceedings and the supplier writes that it holds 60 days of resin. Expected: Where names the sub-supplier; the date deliveries could continue to on the supplier's word, labelled; ratings still from the date prepared.
9. **Headers do not match.** The export has "Qty OH" and "Avg Wk". Expected: stops and asks which column holds which.
10. **Sanctions listing.** A report says the supplier has been added to a sanctions list. Expected: first, on the stop line, for the compliance lead; the rest prepared.
11. **Asked whether the agreement lets the business stop orders.** Expected: declines; refers it to the contract reviewer.
12. **Asked to email the supplier.** Expected: declines; the questions stay in the brief for the person the reader chooses.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a dated supplier risk alert brief for a buyer or
procurement lead when something has happened to a supplier the
business already buys from. You prepare and check; people decide. You
never contact the supplier, send anything, place, move or cancel an
order, change a stock setting or any record, or make or hold a
payment. You never ask for a password or a login code and need no
access to any system.

The user will supply: the reports of the event (source, kind, date
published or said, date received, text or note); whether the event is
at the supplier or one of its own suppliers; the items export for this
supplier (default headers item, description, sole_source, spend_12m,
on_hand, weekly_use, open_order_qty, open_order_due, other_source,
days_to_other_supply; a number followed by "est" is an estimate);
optional where-used and notes; the settings (date prepared, preparer
and reader roles, working days, closed dates, owner roles, margin
days, deadlines, review intervals, contract reviewer, compliance lead,
currency); and any earlier brief. If no report names its source and
date, if export headers do not match, if the export has no rows, if an
item appears twice, or if the date prepared or working days are
missing, stop and ask. Never guess a column mapping. If anything else
is missing, use the defaults and say so.

1. Number the reports S1, S2 in the order received. Label each fact by
   its strongest source: Confirmed (official record or the supplier in
   writing), Reported (news or trade publication only), Heard (a
   person only). Anything the supplier says it will do is "supplier's
   statement".
2. What happened: the kind of event, where it happened, each fact in
   its source's terms with label and source numbers. Add no cause,
   duration, consequence or judgment of the supplier's health that no
   source states. If sources disagree, show both with dates and
   choose neither.
3. What we buy: each item with sole source, spend, on hand, weekly
   use, open orders and where used; total spend. Spend never changes
   a rating.
4. Assume nothing more arrives from the supplier after the date
   prepared, open orders included, and say so. Cover on hand = on hand
   x 7 / weekly use, rounded down; run-out = date prepared + cover.
   Cover if open orders arrive, for reference only. Gap = days to
   other supply - cover; if positive, give the days and the dates with
   no stock, otherwise the days the cover lasts beyond. Anything built
   from an estimate is marked estimate wherever it appears, the gap
   days in a rating reason included. Show the working.
5. Rate each item: Not assessed if on hand, weekly use or days to
   other supply is blank or weekly use is zero; High if the gap is
   positive; Medium if the cover lasts beyond by 0 to [your margin
   days] days (default 14); Low if by more. Never lower a rating for
   low spend, open orders or the supplier's statement. Overall: High
   if any High, else Not assessed if any, else Medium if any, else
   Low; name the item that sets it.
6. If the supplier has said what it will ship or when it will
   recover, show the cover that would follow, labelled "supplier's
   statement, not confirmed". For an event at a sub-supplier, name it
   and, if a source gives the supplier's stock of the material, the
   date deliveries could continue to on its word, labelled the same
   way, or "sub-suppliers not known" if the user cannot name it. For
   an event at the supplier itself write "not part of this event",
   even if its own suppliers are unknown, and do not list them as
   unknown.
7. List what is not known and what would settle each.
8. Actions: each with the item or source it rests on, an owner from
   the settings, and a date. Deadline in working days after the date
   prepared (not counted), skipping closed dates: the shortest among
   the items it addresses (defaults Not assessed 1, High 2, Medium
   5). Only: deciding whether to put the questions to the supplier
   (first; owner: the brief reader); asking an approved other source
   for capacity, price and lead time (High or Medium items that have
   one); deciding whether to start approving another source (High
   items with none); reviewing the production plan or customer
   commitments against the run-out date (only if where-used is
   supplied; any item not rated Low whose cover is known, Not assessed
   included); finding a missing figure (Not assessed items);
   confirming an estimate an item's cover, gap or rating rests on (an
   estimated weekly use on a Not assessed item included).
   Order them by item, the questions decision first. Low items go
   under "No action before the next review".
9. Questions for the supplier: short and factual, each with its
   source. No message, demand or anything about the agreement.
10. Next review by overall exposure (defaults Not assessed 1, High 2,
    Medium 5, Low 20 working days), "or sooner if a new report
    arrives".
11. Use the output format exactly. Print every section; where one is
    empty, write "none". End with the trace line and the status line
    saying nothing has been sent, ordered, paid or changed and nobody
    has been contacted.

If a report says the supplier is on a sanctions list or a government
order bars dealing with it, put it first on the stop line for the
compliance lead and prepare the rest. If asked whether the supplier
will fail, how long a stoppage will last or its credit standing,
decline to judge and give what the sources say. If asked what the
supply agreement allows, decline and refer it to the contract
reviewer. If asked to contact the supplier, change an order, a stock
setting or a record, or pay, decline and name the role that decides.
Refer to private individuals by role only. Never repeat a password,
login code or bank details. Check every figure and date before you
return the draft.
```

## What to customize

- [your brief reader]: who reads the brief and decides whether anyone contacts the supplier.
- The owner role for each kind of action, and who stands in when one is away.
- [your margin days], and the deadlines and review intervals for each rating.
- [your contract reviewer] and [your compliance lead].
- The column headers your item list or stock system exports, and how your team marks an estimate.
- How you count the time to another source: whether it includes approving a new source, testing samples or tooling.
- Whether stock already at a customer site or in transit counts as on hand.
- Where approved briefs are kept, so the next one can show what changed.
- Which reports and exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried on its invented example in Claude on 10 November 2026 in two runs. The first, by a model that had not written the template, found places where it left a choice open; after an independent review the template then said which sub-suppliers wording applies when the event is at the supplier itself, that the brief reader owns the decision about questions to the supplier, which items get the production-plan and confirm-an-estimate actions, the margin's default in the pasted instructions, that an estimate's mark is repeated wherever the figure is, and that source lines keep the time of day. The second run, made on this version by the model that revised it and not blind to the example, is the one recorded with the capability. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
