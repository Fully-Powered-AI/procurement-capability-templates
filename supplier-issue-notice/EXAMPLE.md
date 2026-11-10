# Supplier issue notice: an invented example

*Illustrative example with invented data.* The companies, the documents, the contact details and every figure below are invented. Company M is an invented 60-person maker of steel storage cabinets. Supplier A, also invented, sells it hinges, screws, drawer slides and shelf clips. One invoice from Supplier A does not agree with the order or with what arrived, and Company M's buyer prepares an invoice dispute for the purchasing manager to approve. People are referred to by role.

The inputs come first, in full, so the template can be run on them. The draft follows.

## The inputs

### 1. The brief

```
Kind of notice: invoice dispute
Supplier: Supplier A
Contact: accounts receivable lead, Supplier A
Our company: Company M
Sent by: buyer, Company M, purchasing@companym.example, 555-0142
Approver: purchasing manager
Prepared: Tuesday 10 November 2026, by the buyer
Planned send date: Wednesday 11 November 2026
Our reference: PO 4471
```

### 2. The settings

```
Working days: Monday to Friday
Closed dates: Friday 13 November 2026 (plant maintenance day);
  Thursday 26 and Friday 27 November 2026
Reply period: 5 working days for an invoice dispute; 10 for a
  corrective-action request
Price tolerance: a price difference is not raised when it is under 2%
  of the order price and under $25 on the line
Undisputed amounts: paid when due on our normal terms
Approval: invoice disputes with a disputed amount up to $1,000,
  purchasing manager; above $1,000 and every corrective-action
  request, operations director
Bank-detail changes: confirmed by the finance lead by phone, on the
  number already on file
Currency: US dollars
```

### 3. The invoice (typed copy)

```
INVOICE A-30417     Date: 2 November 2026
From: Supplier A    To: Company M
Your order: PO 4471    Terms: 30 days from invoice date

Line  Item                                 Qty     Unit price  Total
1     H-110 concealed hinge, 110 degree    2,000   $1.42       $2,840.00
2     S-410 M4 x 10 mm screw, box of 500   40      $18.50      $740.00
3     D-450 drawer slide pair, 450 mm      300     $6.80       $2,040.00
4     C-20 shelf clip                      5,000   $0.09       $450.00
5     Freight                              1       $185.00     $185.00
                                           Invoice total       $6,255.00
No sales tax charged.

Note: Please make all future payments to our new bank account.
Details enclosed.
```

### 4. The purchase order (typed copy)

```
PURCHASE ORDER 4471     Date: 19 October 2026
From: Company M    To: Supplier A

Line  Item                                 Qty     Unit price  Total
1     H-110 concealed hinge, 110 degree    2,000   $1.35       $2,700.00
2     S-410 M4 x 10 mm screw, box of 500   40      $18.50      $740.00
3     D-450 drawer slide pair, 450 mm      300     $6.80       $2,040.00
4     C-20 shelf clip                      5,000   $0.089      $445.00
                                           Order total         $5,925.00

Terms: prices include delivery to our site. Payment 30 days from
invoice date.
```

### 5. The goods-received record (export)

```
receipt,date,po,po_line,item,qty_received
GR-5512,2026-10-28,4471,1,H-110,2000
GR-5512,2026-10-28,4471,2,S-410,20
GR-5512,2026-10-28,4471,3,D-450,300
GR-5512,2026-10-28,4471,4,C-20,5000
GR-5530,2026-10-30,4471,2,S-410,12
```

### 6. Earlier invoices against PO 4471

```
None.
```

### 7. Notes (typed by the buyer)

```
- 9 November: the warehouse lead confirms 32 boxes of S-410 received
  in total. The delivery note with GR-5530 says the other 8 boxes are
  to follow.
- No price change for H-110 has been agreed. The order price stands.
```

## The draft

**SUPPLIER ISSUE NOTICE: Invoice dispute, Supplier A, invoice A-30417**

**FOR THE APPROVER (not part of the notice)**

- **Approver:** purchasing manager, under the rule for invoice disputes with a disputed amount up to \$1,000 (disputed: \$473.00). Prepared by: buyer on Tuesday 10 November 2026. Planned send date: Wednesday 11 November 2026.
- **Inputs:** invoice A-30417, purchase order 4471, goods-received export (5 rows), the brief and the settings. Earlier invoices: none supplied; treated as the first invoice against the order. Notes: supplied.
- **Reply by:** Thursday 19 November 2026, 5 working days after the planned send date; closed dates skipped: Friday 13 November 2026.
- **Checks:**
  - Invoice arithmetic: passed. Every line's quantity × unit price equals its total, and the five lines add to \$6,255.00.
  - Every line matched to the order: lines 1 to 4 matched; line 5, freight, has no order line (issue 3).
  - Received quantities: from GR-5512 (28 October 2026) and GR-5530 (30 October 2026). S-410: 20 + 12 = 32 boxes, as the warehouse lead confirmed on 9 November.
  - Tie-out: passed. \$6,255.00 = \$473.00 + \$5,782.00, and \$5,782.00 equals the accepted lines (\$2,700.00 + \$592.00 + \$2,040.00 + \$450.00).
  - Reply date against the invoice's due date: the reply is due on 19 November 2026, before the invoice falls due on 2 December 2026 (30 days from 2 November).
- **Raised:** 3 issues. Disputed: \$473.00.
- **Not raised:** line 4, C-20 shelf clip, billed at \$0.09 against the order price of \$0.089: \$5.00 over on 5,000, 1.1% of the order price. Inside the tolerance (under 2% and under \$25 on the line).
- **Stop before sending:** the invoice asks for future payments to a new bank account. The details are not repeated here and the notice does not mention them. Before any payment to Supplier A, the finance lead confirms the change by phone on the number already on file.
- **Decisions for the approver:** 2
  1. Approve the notice as drafted for sending on Wednesday 11 November 2026, change it, or hold it.
  2. Pass the bank-account request on invoice A-30417 to the finance lead for the phone check before the invoice falls due on 2 December 2026.
- **Attachments to include:** PO 4471 (19 October 2026); goods-received records GR-5512 (28 October 2026) and GR-5530 (30 October 2026); invoice A-30417 (2 November 2026).

**THE NOTICE**

- **To:** accounts receivable lead, Supplier A
- **From:** buyer, Company M
- **Date:** Wednesday 11 November 2026
- **Subject:** Invoice A-30417 of 2 November 2026: 3 lines in question
- **Reference:** PO 4471

Invoice A-30417 of 2 November 2026, for \$6,255.00, does not agree with our purchase order 4471 or our records of goods received on 3 lines. Each is set out below. The amount in question, \$473.00, is on hold until each one is settled.

**ISSUE 1: Price above the order**

- **Invoice line:** line 1, H-110 concealed hinge, 110 degree
- **Billed:** 2,000 at \$1.42 = \$2,840.00
- **Ordered and received:** PO 4471 line 1, 2,000 ordered at \$1.35; 2,000 received (GR-5512, 28 October 2026)
- **Amount in question:** \$140.00 (\$0.07 × 2,000)
- **To settle it:** a credit note for \$140.00, or a revised invoice at \$1.35 each; or a copy of a price change agreed in writing by Company M.

**ISSUE 2: Billed above received**

- **Invoice line:** line 2, S-410 M4 x 10 mm screw, box of 500
- **Billed:** 40 at \$18.50 = \$740.00
- **Ordered and received:** PO 4471 line 2, 40 ordered at \$18.50; 32 received (20 on GR-5512, 28 October 2026; 12 on GR-5530, 30 October 2026)
- **Amount in question:** \$148.00 (8 × \$18.50)
- **To settle it:** a credit note for \$148.00, or a revised invoice for the 32 boxes received. The other 8 boxes on the order may be invoiced once they are received. A signed proof of delivery for more than 32 boxes will be considered.

**ISSUE 3: Not on the order**

- **Invoice line:** line 5, Freight
- **Billed:** 1 at \$185.00 = \$185.00
- **Ordered and received:** No order line on PO 4471; its terms say "prices include delivery to our site"
- **Amount in question:** \$185.00 (the whole charge)
- **To settle it:** a credit note for \$185.00, or a revised invoice without the charge; or a copy of an agreement in writing to pay it.

**Summary:** Invoice total \$6,255.00. Disputed \$473.00. Undisputed \$5,782.00. (\$6,255.00 = \$473.00 + \$5,782.00.)

**WHAT WE ASK YOU TO DO**

Please reply by Thursday 19 November 2026 with a credit note or a revised invoice for each line, or with the documents named under it.

The rest of the invoice, \$5,782.00, is not in question and will be paid when it falls due under our usual terms.

**EVIDENCE ATTACHED**

1. Purchase order 4471, 19 October 2026
2. Goods-received records GR-5512, 28 October 2026, and GR-5530, 30 October 2026
3. Invoice A-30417, 2 November 2026

If any of this differs from your records, tell us which item and send what you hold.

Buyer, Company M, purchasing@companym.example, 555-0142

**FOLLOW-UP (not part of the notice)**

- If no reply by Thursday 19 November 2026: the buyer follows up.
- Status: draft for the approver. Nothing has been sent, paid, held or changed.
