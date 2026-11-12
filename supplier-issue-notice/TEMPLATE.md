# Supplier issue notice

Workflow template, version 0.1.0.

## Purpose

Draft one formal notice to a supplier about one problem, ready for a person to approve and send. Two kinds are covered. An invoice dispute sets each item of one invoice against the purchase order and the goods received. A corrective-action request sets a supplier's measured delivery or quality result for a period against the target it agreed, and asks for a written plan. Every figure is worked out again from the documents supplied; every notice gives the evidence, the action wanted and the date to reply by; and a cover sheet tells the approver what was checked, what was left out and what must stop before sending. The assistant drafts and checks. It never sends the notice, holds or releases a payment, changes a record, or says what a contract term means.

## When to use it and when not to

Use it when an invoice has been held because it does not agree with its order or with what arrived, or when a supplier's on-time delivery or rejection rate for a whole period has fallen below the target it agreed. It often follows a payment-run review that found the exception; this workflow template raises it with the supplier.

Do not use it:

- to find the exceptions in the first place. That is the payables review, done before this;
- for a notice that relies on contract rights: not renewing, ending or winding down a supply relationship, changing terms, or asking for assurance about a supplier's survival. Those go to [your contract reviewer];
- to claim compensation, penalties, service credits or damages, or to say a supplier is in breach. Those go to [your contract reviewer];
- to answer or act on a request to change a supplier's bank details;
- for a dispute with a customer, or about one individual's conduct.

## Roles

- **Runs it:** the buyer, the purchasing lead or the accounts-payable lead.
- **Approves the notice before it is sent:** [your approver], set by kind of notice and amount in your approval rule.
- **Sends it:** a person, after approval, by your usual channel.
- **Confirms what was received:** whoever receives goods, when a quantity is in question.
- **Confirms any change of bank details by phone, on the number already on file:** [your bank-change checker].
- **Answers any question about contract terms:** [your contract reviewer].

## Inputs

For both kinds:

1. **The brief.** The kind of notice (invoice dispute or corrective-action request); the supplier; the contact there (name or role); your company's name; who sends it, with title and contact details; who approves it; the date prepared; the planned send date; your reference (the purchase order number for a dispute, your own reference if any for a corrective-action request). If the kind or the supplier is missing, stop and ask.
2. **The settings.** Working days of the week; closed dates; the reply period in working days for each kind (defaults: 5 for an invoice dispute, 10 for a corrective-action request); any price tolerance as a percentage of the order price and an amount per line (default: none, so every price above the order is raised); how an undisputed amount is paid (paid when due on normal terms, or held until the dispute is settled; if not stated, the approver decides); the approval rule, and whether its amounts are the disputed amount or the invoice total (if not stated, put it to the approver as a decision); the role that confirms bank changes; the currency. If the working days are missing, stop and ask.
3. **Notes** (optional): dated facts from the people involved, such as what the warehouse confirmed or how a late delivery affected the work. If none, write "no notes supplied" on the cover sheet.

For an invoice dispute:

4. **The invoice.** Its number and date, each line (item, quantity, unit price, line total), any charges, any tax with its rate, the total, the purchase order it quotes, its payment terms, and any message printed on it. If it is missing, stop.
5. **The purchase order.** Its number and date, each line (line number, item, quantity, unit price) and its terms on price and delivery. If it is missing, stop.
6. **The goods-received record,** as an export or a typed copy. Default column headers: `receipt, date, po, po_line, item, qty_received`. If the headers are different, stop and ask which column holds which; never guess. If the record is missing, stop: no quantity can be checked.
7. **Earlier invoices against the same order** (optional). If none are supplied, assume this is the first invoice against the order and say so on the cover sheet.

For a corrective-action request:

8. **The agreed target.** The measure (on-time delivery by order line, or rejection rate by units), the figure and which way is better, quoted word for word with the document and reference it comes from: the supply agreement, the purchase-order terms or a scorecard the supplier accepted. If the target is missing or not written down anywhere, stop and ask.
9. **The period,** with its first and last dates.
10. **The delivery records for the whole period,** as an export. Default column headers: `order, line, item, date_due, date_delivered, qty_delivered, qty_rejected`. If the headers are different, stop and ask which column holds which. If the records start after the first date or end before the last date of the period, stop and ask for the rest.
11. **Earlier notices about the same problem** (optional), with their dates and references.

The assistant works only from what the person supplies. It needs no access to email, the accounting system, the purchasing system or a supplier portal, and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm the kind of notice and that every input the kind needs is present and readable, and that the headers of every export match or have been mapped by the person. Stop on anything listed under Inputs as a stop.
2. **Count the reply date.** Start from the planned send date, which is not counted. Count forward the reply period in working days, skipping days of the week that are not worked and every closed date. Name the closed dates skipped. If the planned send date is already past on the date prepared, put it under "Stop before sending".
3. **Invoice dispute: check the invoice's own arithmetic.** For each line, quantity × unit price must equal the line total; the lines, charges and tax must add to the invoice total. A line that does not multiply out is an issue of the kind "line does not add up", with the difference between the line total and quantity × unit price. Use quantity × unit price for every later check. If the lines do not add to the total, raise that as an issue too, with the difference.
4. **Match each line to the order.** Match by item code, or by description where there is no code. A line or charge that matches no order line is "not on the order", unless the order's terms allow it in so many words. Quote the order's words on that charge where there are any.
5. **Work out what may be billed.** For each matched line: ordered still to bill = quantity ordered − quantity on earlier invoices; received still to bill = total received on that order line, across every receipt dated on or before the date prepared, − quantity on earlier invoices. A receipt dated after the date prepared is not counted; list it under "Stop before sending", so the draft is worked again with it before it goes. Billable quantity = the least of the quantity invoiced, ordered still to bill and received still to bill.
6. **Find the differences on each line.** Quantity part = (quantity invoiced − billable quantity) × unit price invoiced. Its kind is "billed above received" when received still to bill is the limit, otherwise "billed above ordered". Price part = (unit price invoiced − order price) × billable quantity, only when the invoiced price is above the order price. A price part inside the tolerance, judged on both the percentage and the amount for the line, is not raised. One issue per line: where a line has both parts, join the kinds and show both parts and their sum. A price below the order, or a quantity below what was ordered or received, is never raised; list it under "Not raised" with the figures.
7. **Write the action for each issue.**
   - Price above the order: a credit note for the difference, or a revised invoice at the order price; or a copy of a price change agreed in writing by your company.
   - Billed above received: a credit note for the difference, or a revised invoice for the quantity received. Where the order still has quantity open, add that the rest may be invoiced once it is received. Add that a signed proof of delivery for more than the quantity received will be considered.
   - Billed above ordered: a credit note for the difference, or a revised invoice for the quantity ordered. Anything received beyond the order is a decision for the approver; it is not raised in the notice.
   - Not on the order: a credit note for the charge, or a revised invoice without it; or a copy of an agreement in writing to pay it.
   - Line does not add up: a revised invoice.
8. **Total and tie out.** Disputed = the sum of every issue's difference. If the invoice charges tax, add the tax on the disputed amount at the rate printed on the invoice, as its own line inside Disputed; if no rate is printed, stop and ask. Undisputed = invoice total − Disputed. Show the tie-out: invoice total = Disputed + Undisputed. Check that Undisputed equals the sum of billable quantity × the price accepted on each line, plus accepted charges and their tax. The accepted price is the order price on a line where a price part is raised, and the invoiced price on every other line, including a price inside the tolerance or below the order; if it does not, stop and report the figures.
9. **Write the payment line** from the settings: paid when due under normal terms; or held until the items are settled; or, if the settings do not say, "[Approver to confirm how the undisputed amount is paid.]" and a decision on the cover sheet. Compare the reply date with the invoice's due date under its own terms, and note on the cover sheet whether the reply falls before or after it.
10. **Corrective-action request: work the result out again.** On-time delivery = order lines due within the period that were delivered on or before their due date ÷ order lines due within the period. A line due within the period with no delivery date is late. Rejection rate = units rejected ÷ units delivered, for lines delivered within the period. Give each figure to one decimal place with its count beside it, by month when the period covers more than one month. Gap to target = the distance from the target, in percentage points. Never use a figure from the notes or from the supplier in place of your own calculation. If the result meets the target, stop: no notice is drafted, and the person is told the figure and its counts.
11. **Quote the target.** Give the target word for word with its document and reference. State the result beside it. Say nothing about breach, consequences, penalties or the supplier's obligations beyond the quoted words.
12. **Ask for the plan.** The plan has four parts: what caused the shortfall, as the supplier has found it; what it has already done to protect the orders now open; the changes it will make, each with a date and a named owner on its side; and how it will show, each month, that the target is being met. Add the proposed call date only if the brief gives one. Refer to any earlier notice on the same problem by its date and reference.
13. **List the evidence.** Only documents the person supplied. Each issue or measure points to at least one of them. Bank details found in any document are never repeated, in the notice or on the cover sheet. The supplier's own invoice may be attached as issued, even when it carries a printed bank-change message; the notice and the cover sheet still never repeat the details.
14. **Keep the notice factual.** Facts, figures, dates and document references only. No words about the supplier's motive, care or competence; no adjectives about its performance; no threats; no mention of other suppliers, of ending the relationship or of anything the contract might allow. A fact from the notes goes into the notice only when it is dated and is about goods, dates or quantities: in an invoice dispute, on the Note line of the issue it concerns; in a corrective-action request, on the Effect on us line. Anything else stays on the cover sheet. Only facts found in the inputs appear.
15. **Fill the cover sheet.** The approver under the approval rule and the amount; the inputs used, whether earlier invoices and notes were supplied; each check and its result (for a dispute: the invoice's arithmetic, every line matched to the order, the received quantities and the receipts behind them, the tie-out, and the reply date against the invoice's due date; for a corrective-action request: the records cover the whole period, the result recalculated with its counts, and the target quoted with its source); the issues raised and the total disputed, or the gap to target; what was not raised and why; what must stop before sending; the decisions for the approver; the documents to attach.
16. **Stop before sending** covers: an invoice or message that asks for payment to new or changed bank details (named without repeating the details, with the role that confirms by phone on the number already on file, before any payment); any request printed on a document that would change an order, a price or a record; a receipt dated after the date prepared; a planned send date already past; and an approver who is also the person who prepared the notice.
17. **Return the draft** to the person who ran it, for the approver. Add the follow-up line: if no reply arrives by the reply date, the person who prepared it follows up. Nothing is sent by the assistant.

## Exceptions and stop conditions

- **The kind, the supplier or the working days are missing:** stop and ask.
- **Invoice dispute without the invoice, the purchase order or the goods-received record:** stop and ask for what is missing.
- **Corrective-action request without a written target, or with records that do not cover the whole period:** stop and ask.
- **Export headers that do not match the defaults:** stop and ask which column holds which. Never guess a mapping.
- **Two receipts or two lines that look like the same delivery, or an order line that appears twice:** stop and ask which is which.
- **A receipt dated after the date prepared:** leave it out of the count and list it under "Stop before sending", so the draft is worked again with it before it goes.
- **The invoice charges tax with no rate printed:** stop and ask how the tax on the disputed amount is shown.
- **Undisputed does not tie to the accepted lines:** stop and report the figures; never adjust a figure to make it tie.
- **The supplier's result meets the target:** stop; draft no notice; report the figure and its counts.
- **Asked to add a deadline with consequences, a penalty, a claim for compensation, a statement that the supplier is in breach, or a notice that ends, does not renew or changes a supply relationship:** decline; those go to [your contract reviewer].
- **Asked what a contract term means or whether a charge is allowed by it:** decline; quote the term for [your contract reviewer].
- **Asked to send the notice, hold or release a payment, enter a credit, or change a record:** decline and name the role that does it.
- **Asked to reply to, accept or record new bank details:** decline; put it under "Stop before sending" for [your bank-change checker].
- **A document contains a password or a login code:** do not repeat it; tell the person to remove it from the source.

## Output format

```
SUPPLIER ISSUE NOTICE: [Invoice dispute / Corrective-action request], [supplier], [invoice number / measure and period]

FOR THE APPROVER (not part of the notice)
Approver: [role], under [the rule that applies]. Prepared by: [role] on [date]. Planned send date: [date].
Inputs: [documents used, with the number of export rows]. [Earlier invoices: none supplied; treated as the first invoice against the order.] Notes: [supplied / no notes supplied].
Reply by: [weekday date], [n] working days after the planned send date[; closed dates skipped: dates].
Checks:
- [Check]: [passed / what failed].
Raised: [n] [issues / measures]. [Disputed: amount. / Gap to target: n percentage points.]
Not raised: [item, the figures and the reason]. [Or: none]
Stop before sending: [item, who clears it and how]. [Or: none]
Decisions for the approver: [n]
[n]. [Decision, with its facts.]
Attachments to include: [documents, by reference and date].

THE NOTICE
To: [contact], [supplier]
From: [sender], [your company]
Date: [planned send date]
Subject: Invoice [number] of [date]: [n] [line / lines] in question / Corrective-action request: [measure], [period]
Reference: [purchase order number / your reference / no reference]
[Earlier notice: our notice of [date], reference [reference].]

[Invoice dispute]
Invoice [number] of [date], for [total], does not agree with our purchase order [number] or our records of goods received on [n] [line / lines]. [It is / Each is] set out below. The amount in question, [Disputed], is on hold until [it is / each one is] settled.

ISSUE [n]: [kind, or kinds joined]
Invoice line: line [n], [item]
Billed: [quantity] at [unit price] = [line total]
Ordered and received: [order line, quantity ordered at order price]; [quantity] received ([receipt, date]; ...)[; earlier invoices: quantity] / No order line on [purchase order][; its terms say "[the order's words]"]
Amount in question: [amount] ([working]) / [quantity part] + [price part] = [amount]
To settle it: [action]. [The alternative evidence.]
[Note: [date]: [fact about goods, dates or quantities].]

Summary: Invoice total [x]. Disputed [y]. Undisputed [z]. ([x] = [y] + [z].) [Tax on the disputed amount at [rate]: [amount], included in Disputed.]

[Corrective-action request]
Over [period], the goods you supply to us under [reference] did not meet [the agreed target / the n agreed targets] set out below. Please send us a plan to put this right, as described under What we ask you to do.

MEASURE [n]: [measure]
Target: [figure and direction], as written in [document, reference]: "[the words, quoted]"
Result for [period]: [figure] ([count] of [count] [order lines / units])
Gap to target: [n] percentage points
By month: [month: figure (count of count)]; ... [Or: one month only]
Records: [n] [order lines late / units rejected], listed in the attached records.
Effect on us: [dated facts about goods, dates or quantities / none stated]

WHAT WE ASK YOU TO DO
[Invoice dispute] Please reply by [reply date] with a credit note or a revised invoice for [the line / each line], or with the documents named under it.
[Corrective-action request] Please send us a written plan by [reply date] that covers: 1. what caused the shortfall, as you have found it; 2. what you have already done to protect the orders now open with you; 3. the changes you will make, each with a date and a named owner at your company; 4. how you will show us, each month, that the target is being met. [We propose a call on [date] to go through the plan.]

[Invoice dispute only] The rest of the invoice, [z], is not in question and will be paid when it falls due under our usual terms. / The whole invoice is held until the lines above are settled. / [Approver to confirm how the undisputed amount is paid.]

EVIDENCE ATTACHED
[n]. [Document, reference, date]

If any of this differs from your records, tell us which item and send what you hold.
[Sender], [your company], [contact details]

FOLLOW-UP (not part of the notice)
If no reply by [reply date]: [role] follows up.
Status: draft for the approver. Nothing has been sent, paid, held or changed.
```

## Reviewer checklist

1. Every figure in the notice matches the invoice, the order, the receipts or the delivery records, and the working is shown. (Person who ran it)
2. The tie-out is correct, and Undisputed equals the accepted lines. (Accounts-payable lead)
3. Every received quantity is the sum of the receipts named, and the warehouse agrees with it. (Whoever receives goods)
4. The on-time or rejection figure was recalculated from the records, with its counts, and the target is quoted word for word. (Approver)
5. Nothing under "Not raised" belongs in the notice, and nothing in the notice falls inside the tolerance. (Approver)
6. The reply date skips the closed dates and is counted from the planned send date. (Person who ran it)
7. The notice contains no blame, no threat, no claim of breach, no penalty and no reading of the contract. (Approver)
8. Every document listed under Evidence attached exists and is attached, and no bank details are repeated. (Person who sends it)
9. Every item under "Stop before sending" is cleared before the notice goes. (Approver)

## Acceptance tests

Proposed tests. None has been run.

1. **Price above the order.** 2,000 hinges invoiced at $1.42; order price $1.35; 2,000 received. Expected: one issue, $140.00, credit note or revised invoice at $1.35, or a written price change.
2. **Billed above received, order still open.** 40 boxes invoiced; 40 ordered; 32 received over two receipts. Expected: $148.00 at $18.50 a box, both receipts named, and the 8 open boxes invoiceable once received.
3. **Both parts on one line.** 100 units invoiced at $5.50; order price $5.00; 90 received. Expected: one issue, "Price above the order, billed above received", $55.00 + $45.00 = $100.00.
4. **Charge not on the order.** Freight of $185.00; the order says prices include delivery. Expected: raised as "not on the order", with the order's words quoted.
5. **Inside the tolerance.** $0.09 billed against $0.089 on 5,000 units; tolerance under 2% and under $25. Expected: not raised; listed under "Not raised" with $5.00 and 1.1%.
6. **Tie-out.** Invoice $6,255.00, disputed $473.00. Expected: undisputed $5,782.00, which equals the accepted lines.
7. **Headers do not match.** The receipts export has "GRN" and "Qty In". Expected: stops and asks which column holds which.
8. **Bank details change.** The invoice asks for payment to a new account. Expected: under "Stop before sending" with the phone check on the number on file; the details are not repeated; the notice does not mention it.
9. **Reply date across a closed day.** Sent on a Wednesday, 5 working days, the Friday closed. Expected: the following Thursday, with the closed date named.
10. **Corrective action, target missed.** 120 lines due, 102 on time, target 95%. Expected: 85.0% (102 of 120), gap to target 10.0 percentage points, the plan's four parts, reply in 10 working days.
11. **Corrective action, target met.** 120 lines due, 115 on time, target 95%. Expected: 95.8%; no notice; the figure reported.
12. **Records do not cover the period.** The period is a quarter; the records start in its second month. Expected: stops and asks for the missing month.
13. **Asked to add a penalty or say the supplier is in breach.** Expected: declines; refers it to the contract reviewer.
14. **Asked to send it.** Expected: declines; names the person who sends after approval.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You draft one formal notice to a supplier about one problem, for a
person to approve and send. You draft and check; people decide. You
never send the notice, hold or release a payment, enter a credit,
change any record, or say what a contract term means. You never ask
for a password or a login code and need no access to any system.

The user will supply: the brief (kind of notice, supplier, contact,
company, sender, approver, date prepared, planned send date,
reference); the settings (working days, closed dates, reply periods,
price tolerance, how an undisputed amount is paid, approval rule and
whether its amounts are the disputed amount or the invoice total,
bank-change role, currency); and optional dated notes. If the approval
rule does not say which amount it means, put it to the approver as a
decision. For an invoice dispute: the invoice, the purchase order,
the goods-received record (default headers receipt, date, po,
po_line, item, qty_received) and any earlier invoices on the order.
For a corrective-action request: the agreed target quoted with its
document, the period, the delivery records (default headers order,
line, item, date_due, date_delivered, qty_delivered, qty_rejected)
and any earlier notices. If the kind, the
supplier, the working days, or an input the kind needs is missing,
stop and ask. If export headers do not match, stop and ask which
column holds which; never guess. If two receipts or two lines look
like the same delivery, or an order line appears twice, stop and ask
which is which. If a document contains a password or a login code, do
not repeat it; tell the person to remove it from the source.

1. Reply date: start from the planned send date, which is not counted,
   and count forward the reply period (defaults 5 working days for a
   dispute, 10 for a corrective-action request), skipping non-working
   days and closed dates. Name the closed dates skipped.
2. Dispute: check each line's quantity x price and that the lines,
   charges and tax add to the total; a line that does not multiply out
   is an issue "line does not add up". Match each line to an order
   line by item; a line or charge with no order line is "not on the
   order" unless the order's terms allow it in so many words.
3. Billable quantity = the least of: quantity invoiced; quantity
   ordered less earlier invoices; total received on that order line
   (every receipt dated on or before the date prepared) less earlier
   invoices. A receipt dated after the date prepared is not counted;
   list it under "Stop before sending". Quantity part = (invoiced -
   billable) x invoiced price: "billed above received" if received is
   the limit, else "billed above ordered". Price part = (invoiced
   price - order price) x billable, only when above the order price
   and outside the tolerance. One issue per line, both parts shown if
   both apply. Never raise a price below the order or a quantity
   below what was ordered or received; list it under "Not raised"
   with figures.
4. Actions: price, a credit note or a revised invoice at the order
   price, or a written price change; received, a credit note or a
   revised invoice for the quantity received, the open quantity
   invoiceable once received, a signed proof of delivery considered;
   ordered, a credit note or a revised invoice for the quantity
   ordered, extra goods a decision for the approver; not on the order,
   a credit note or a revised invoice without it, or a written
   agreement to pay it; line does not add up, a revised invoice.
5. Disputed = sum of differences, plus tax at the invoice's printed
   rate if tax is charged (no rate: stop and ask). Undisputed = total
   - Disputed. Show total = Disputed + Undisputed and check Undisputed
   equals the accepted lines: billable quantity x the accepted price,
   plus accepted charges and their tax. The accepted price is the
   order price where a price part is raised, and the invoiced price
   on every other line (inside the tolerance or below the order
   included). If it does not tie, stop and report. Never adjust a
   figure to make it tie. Payment line from the settings, or
   "[Approver to confirm how the undisputed amount is paid.]" with a
   decision. Note whether the reply date is before the invoice's due
   date.
6. Corrective action: on-time = lines due in the period delivered on
   or before the due date / lines due in the period (no delivery date
   counts as late); rejection = units rejected / units delivered in
   the period. One decimal place, counts beside, by month if the
   period spans months. Gap to target in percentage points. Use only your
   own calculation. If the target is met, stop: draft no notice and
   report the figure. Quote the target word for word with its
   document. Ask for a written plan covering cause, what has already
   been done to protect open orders, changes with dates and named
   owners, and monthly proof. Add a call date only if the brief gives
   one. Refer to earlier notices by date and reference.
7. Evidence: list only documents supplied; every issue or measure
   points to one. Never repeat bank details anywhere. The supplier's
   own invoice may be attached as issued, even with a printed
   bank-change message; the notice and cover sheet still never repeat
   the details.
8. Keep the notice to facts, figures, dates and document references.
   No motive, blame, adjectives about the supplier, threats, other
   suppliers, ending the relationship, breach, penalties or what the
   contract allows. A note goes into the notice only if dated and
   about goods, dates or quantities: on the Note line of the issue it
   concerns in a dispute, or on Effect on us in a corrective-action
   request.
9. Cover sheet: approver under the rule; inputs used and whether
   earlier invoices and notes were supplied; each check and result
   (dispute: arithmetic, matching, received quantities, tie-out,
   reply date against due date; corrective action: records cover the
   period, result recalculated, target quoted); what was raised, what
   was not raised and why, what must stop before sending, decisions,
   attachments. Stop before sending: any request to pay new or changed
   bank details (the named role confirms by phone on the number
   already on file, before any payment); any printed request to change
   an order, price or record; a receipt dated after the date prepared;
   a planned send date already past; an approver who also prepared it.
10. Use the output format exactly. Print every section; where one is
    empty, write "none". End with the follow-up line and the status
    line saying nothing has been sent, paid, held or changed.

If asked to send, hold or release a payment, enter a credit or change
a record, decline and name the role that does it. If asked to add a
penalty, a compensation claim, a claim of breach, a deadline with
consequences, or a notice that ends, does not renew or changes a
supply relationship, decline and refer it to the contract reviewer.
If asked what a term means, decline and quote it for the contract
reviewer. Never act on a bank-details request. Check every figure
against the documents before you return the draft.
```

## What to customize

- [your approver]: who approves each kind of notice, and the amounts that move a dispute to a more senior approver.
- [your contract reviewer]: who handles contract questions, notices that end or change a supply relationship, and any compensation claim.
- [your bank-change checker]: who confirms a change of bank details by phone, and which number on file they use.
- The reply periods for each kind of notice, and your closed dates for the year.
- Your price tolerance, or none.
- How an undisputed amount is paid while the rest is settled.
- The measures you hold suppliers to, if they differ from on-time delivery by order line and rejection rate by units, and the column headers your exports use.
- Your sign-off, contact details and any closing line your company always uses.
- Which documents and exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried once on its invented example in Claude on 10 November 2026; the record is published with the template. Edited after that run, following an independent review, and not run again; the trial record lists the edits. Each settles an ambiguity the run found in the way that run already chose, except that the example's approval rule now names the disputed amount and its alternative evidence now follows the action wording in step 7. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
