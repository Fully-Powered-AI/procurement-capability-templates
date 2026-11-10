# Supplier issue notice: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs were the invented example in `public/example.md` (sections 1 to 7: the brief, the settings, the invoice, the purchase order, the goods-received export, the earlier invoices and the notes). No client data was used. The model that ran the trial did not write the template. It read the template and only the example's inputs, followed the instruction block and the output format, and only then read the example's published draft to compare.

## What came out

The full draft, as produced before the comparison.

```
SUPPLIER ISSUE NOTICE: Invoice dispute, Supplier A, invoice A-30417

FOR THE APPROVER (not part of the notice)
Approver: purchasing manager, under the rule for invoice disputes up to $1,000 (disputed amount $473.00). Prepared by: buyer on Tuesday 10 November 2026. Planned send date: Wednesday 11 November 2026.
Inputs: invoice A-30417, purchase order 4471, goods-received export (5 rows), the brief and the settings. Earlier invoices: none supplied; treated as the first invoice against the order. Notes: supplied (2 dated notes; see below).
Reply by: Thursday 19 November 2026, 5 working days after the planned send date; closed dates skipped: Friday 13 November 2026.
Checks:
- Invoice arithmetic: passed. Each line's quantity x unit price equals its total; the five lines add to $6,255.00; no tax charged.
- Every line matched to the order: lines 1 to 4 matched; line 5 (freight) has no order line.
- Received quantities: line 1 2,000 (GR-5512, 28 October 2026); line 2 32 (GR-5512 20 + GR-5530 12, 30 October 2026); line 3 300; line 4 5,000. Both receipts are dated on or before the date prepared.
- Tie-out: passed. $6,255.00 = $473.00 + $5,782.00, and $5,782.00 equals the accepted lines ($2,700.00 + $592.00 + $2,040.00 + $450.00).
- Reply date against the invoice's due date: reply due 19 November 2026; the invoice falls due 2 December 2026 (30 days from 2 November). The reply falls before it.
Raised: 3 issues. Disputed: $473.00.
Not raised: line 4, C-20 shelf clip: $0.09 billed against $0.089 ordered, $5.00 over on 5,000 (1.1% of the order price); inside the tolerance (under 2% and under $25 on the line).
Stop before sending: invoice A-30417 asks for future payments to a new bank account (details not repeated; the notice does not mention them). The finance lead confirms the change by phone on the number already on file before any payment to Supplier A.
Decisions for the approver: 3
1. Approve, change or hold the notice for sending on Wednesday 11 November 2026.
2. Confirm the approval level: the rule is read here as the disputed amount ($473.00, so the purchasing manager). If it means the invoice total ($6,255.00), the operations director approves.
3. Invoice A-30417 is listed as evidence and carries the printed bank-account message. Decide whether to attach it as it stands or a copy without that message.
Notes used: 9 November, the warehouse lead confirms 32 boxes of S-410 received in total, and the GR-5530 delivery note says the other 8 boxes are to follow (dated, about quantities; matches the receipts). "No price change for H-110 has been agreed" is undated, so it is kept on this sheet and not put in the notice.
Attachments to include: PO 4471 (19 October 2026); goods-received records GR-5512 (28 October 2026) and GR-5530 (30 October 2026); invoice A-30417 (2 November 2026).

THE NOTICE
To: accounts receivable lead, Supplier A
From: buyer, Company M
Date: Wednesday 11 November 2026
Subject: Invoice A-30417 of 2 November 2026: 3 lines in question
Reference: PO 4471

Invoice A-30417 of 2 November 2026, for $6,255.00, does not agree with our purchase order 4471 or our records of goods received on 3 lines. Each is set out below. The amount in question, $473.00, is on hold until each one is settled.

ISSUE 1: Price above the order
Invoice line: line 1, H-110 concealed hinge, 110 degree
Billed: 2,000 at $1.42 = $2,840.00
Ordered and received: PO line 1, 2,000 ordered at $1.35; 2,000 received (GR-5512, 28 October 2026)
Amount in question: $140.00 (2,000 x $0.07)
To settle it: a credit note for $140.00, or a revised invoice at $1.35 each; or a copy of a price change agreed in writing by Company M.

ISSUE 2: Billed above received
Invoice line: line 2, S-410 M4 x 10 mm screw, box of 500
Billed: 40 at $18.50 = $740.00
Ordered and received: PO line 2, 40 ordered at $18.50; 32 received (GR-5512, 28 October 2026: 20; GR-5530, 30 October 2026: 12)
Amount in question: $148.00 (8 x $18.50)
To settle it: a credit note for $148.00, or a revised invoice for the 32 boxes received. The remaining 8 boxes may be invoiced once they are received. A signed proof of delivery for more than 32 boxes will be considered.

ISSUE 3: Not on the order
Invoice line: line 5, Freight
Billed: 1 at $185.00 = $185.00
Ordered and received: No order line on purchase order 4471; its terms say "prices include delivery to our site"
Amount in question: $185.00 (the whole charge)
To settle it: a credit note for $185.00, or a revised invoice without it; or a copy of an agreement in writing to pay it.

Summary: Invoice total $6,255.00. Disputed $473.00. Undisputed $5,782.00. ($6,255.00 = $473.00 + $5,782.00.)

WHAT WE ASK YOU TO DO
Please reply by Thursday 19 November 2026 with a credit note or a revised invoice for each line, or with the documents named under it.

The rest of the invoice, $5,782.00, is not in question and will be paid when it falls due under our usual terms.

EVIDENCE ATTACHED
1. Purchase order 4471, 19 October 2026
2. Goods-received records GR-5512, 28 October 2026, and GR-5530, 30 October 2026
3. Invoice A-30417, 2 November 2026

If any of this differs from your records, tell us which item and send what you hold.
Buyer, Company M, purchasing@companym.example, 555-0142

FOLLOW-UP (not part of the notice)
If no reply by Thursday 19 November 2026: the buyer follows up.
Status: draft for the approver. Nothing has been sent, paid, held or changed.
```

## What was observed

- **Every required part was produced.** Cover sheet, notice, summary, evidence, follow-up and status line. Nothing in the template told the model to stop: the kind, supplier and working days were given, the export headers match the defaults, the invoice charges no tax, no line or receipt looked duplicated, the tie-out held, the planned send date is not past and the approver is not the preparer.
- **Figures.** Reply date 19 November 2026 (12 Nov is day 1, 13 Nov is closed, then 16, 17, 18, 19). Line 1 price part $140.00 (5.2% over the order price, outside the tolerance). Line 2 billable 32, so $148.00. Freight $185.00 not on the order. Disputed $473.00, undisputed $5,782.00, tie-out passed. Line 4 left out as inside the tolerance ($5.00, 1.1%).
- **Differences from the published example.** The substance and every figure match. The wording differs in small places: the example adds "If we agreed a different price with you in writing, please send us a copy", where the model followed the template's action wording ("a copy of a price change agreed in writing by Company M"). The example lists two decisions for the approver; this run listed three (see below). The example does not say how the approval level was read. The example leaves the delivery-note fact (the other 8 boxes "to follow") off the cover sheet; this run recorded it there.
- **Facts not in the inputs.** None in either output. The one derived date, the invoice due date of 2 December 2026, is 30 days after the invoice date under the invoice's own terms.
- **Ambiguities and guesses in the template.**
  1. The approval rule says "invoice disputes up to $1,000". Whether that means the disputed amount or the invoice total is not stated. The model took the disputed amount ($473.00) and said so. Read as the invoice total, the approver changes.
  2. Step 8 compares Undisputed with "billable quantity x the price accepted on each line". For a line whose price difference falls inside the tolerance, it is not stated whether the accepted price is the invoiced price or the order price. The tie-out only works at the invoiced price ($450.00, not $445.00). The model used the invoiced price.
  3. The instruction block says the reply period is counted "from the day after the planned send date", and the procedure says the send date "is not counted". These agree, but the wording is different and a reader could count differently around a closed day.
  4. The output format has no place for a dated note about goods or quantities in the notice itself. Step 14 allows one, but the format gives no slot, so the model kept the note on the cover sheet.
  5. The checklist and cover sheet say to attach the invoice as evidence, but the invoice here carries a printed bank-change message. The template says the details are never repeated, which attaching the invoice may do. The template has no rule for this; the model raised it as a decision.
  6. "Stop before sending" is a list of conditions, while "Decisions for the approver" carries a count. The template does not say whether a stop item (the bank-details change) is also counted as a decision. The model did not count it.
  7. The "Date prepared" is used for which receipts count (those dated on or before it). The template does not say what to do with a receipt dated after the date prepared but before the planned send date.
- **Shortcomings of this trial.** One run, one invented example, one model. Only the invoice-dispute path was exercised; the corrective-action path, the headers mismatch stop, the missing-rate stop, the tolerance edge cases beyond line 4 and the refusals were not tried. Nothing was tested for a client.

## Edited after this run, 10 November 2026, and not run again

The edits below were made after an independent review. The run recorded above is unchanged, and the template has not been run again on the example since these edits.

- **Ambiguity 1 (approval basis).** The example's approval rule now reads "invoice disputes with a disputed amount up to $1,000", the reading this run took, and its cover sheet says so. The template now asks whether the approval rule's amounts are the disputed amount or the invoice total, and puts it to the approver as a decision when the rule does not say.
- **Ambiguity 2 (accepted price).** The procedure and the pasted instructions now define the accepted price for the tie-out: the order price on a line where a price part is raised, the invoiced price on every other line, including a price inside the tolerance. This is the reading this run took.
- **Ambiguity 3 (counting the reply date).** The pasted instructions now use the procedure's wording: start from the planned send date, which is not counted, and count forward.
- **Ambiguity 4 (a dated note in the notice).** The output format now has an optional Note line in each issue block of an invoice dispute, and the procedure and pasted instructions say a qualifying note goes there (or on Effect on us in a corrective-action request). The example still keeps its note on the cover sheet, as this run did.
- **Ambiguity 5 (attaching an invoice with a bank-change message).** The template now says the supplier's own invoice may be attached as issued; the notice and the cover sheet still never repeat the details.
- **Ambiguity 6 (whether a stop item is also a decision).** Not closed. The example lists the bank-details check as a decision; this run did not.
- **Ambiguity 7 (a receipt dated after the date prepared).** The template now says such a receipt is not counted and is listed under "Stop before sending", so the draft is worked again with it before it goes.
- **Other edits.** The pasted instructions now also carry two stops from the procedure: two receipts or lines that look like the same delivery, or an order line that appears twice (stop and ask), and a document containing a password or login code (do not repeat it). In the example, the cover sheet now prints Approver, Inputs, Reply by in the output format's order, and each issue's alternative evidence now follows the action wording in the template, as this run's output did; the differences in wording noted above refer to the example as it stood at the time of the run.
