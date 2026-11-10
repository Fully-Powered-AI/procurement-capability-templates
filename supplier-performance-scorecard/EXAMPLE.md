# Supplier performance scorecard: an invented example

*Illustrative example with invented data.* The company, the suppliers, the people, the orders, the dates and the amounts below are all invented. The company is an invented 40-person maker of scented candles that sells online and through gift shops, called Brand R here. Its suppliers are called Supplier A to Supplier F. Its operations lead is scoring the key suppliers for the third quarter of 2026 before the quarterly supplier reviews. First come the inputs the operations lead supplied, in full, then the scorecard the capability returned.

## The inputs

### 1. Settings (typed by the operations lead)

```
Company: Brand R
Today (exports run): Tuesday 6 October 2026
Quarter scored: Q3 2026, 1 July 2026 to 30 September 2026
Currency: USD
Runner: Operations lead
Decision-maker: Managing director
Targets: on time 95%; fill rate 98%; defects and returns at most 1.0%;
  price within terms 100%; orders confirmed within the window 90%
Grace days: 0
Price tolerance: 0%
Confirmation window: 2 days
Minimum to score: 5 lines; 3 orders for confirmations
Trend step: 2.0 points; 0.5 for defects and returns
Tier review count: 3
Exit count: 3
```

### 2. Key supplier list

```
supplier,category,tier,sole_source,alternative,owner
Supplier A,Glass jars,preferred,no,Supplier E,Operations lead
Supplier B,Soy wax,preferred,no,Supplier F,Operations lead
Supplier C,Wicks,approved,yes,,Production lead
```

### 3. Purchase-order lines export (lines due and orders placed in Q3 2026)

```
po,line,supplier,item,order_date,due_date,qty_ordered,unit_price,confirmed_date
PO-3101,1,Supplier A,JAR-8OZ-AMB,2026-07-01,2026-07-15,2400,0.62,2026-07-02
PO-3101,2,Supplier A,JAR-12OZ-CLR,2026-07-01,2026-07-15,1200,0.81,2026-07-02
PO-3105,1,Supplier B,WAX-SOY-20KG,2026-07-03,2026-07-17,60,58.00,2026-07-03
PO-3105,2,Supplier B,WAX-COCO-20KG,2026-07-03,2026-07-17,20,71.50,2026-07-03
PO-3110,1,Supplier C,WICK-CD10-150,2026-07-06,2026-07-27,10000,0.05,2026-07-07
PO-3110,2,Supplier C,WICK-CD12-180,2026-07-06,2026-07-27,6000,0.06,2026-07-07
PO-3118,1,Supplier A,JAR-8OZ-AMB,2026-07-20,2026-08-03,2400,0.62,2026-07-24
PO-3118,2,Supplier A,JAR-12OZ-CLR,2026-07-20,2026-08-03,1200,0.84,2026-07-24
PO-3129,1,Supplier B,WAX-SOY-20KG,2026-08-03,2026-08-17,60,58.00,2026-08-04
PO-3129,2,Supplier B,WAX-COCO-20KG,2026-08-03,2026-08-17,20,71.50,2026-08-04
PO-3133,1,Supplier D,CARTON-12,2026-07-29,2026-08-12,500,1.10,2026-07-29
PO-3140,1,Supplier A,JAR-8OZ-AMB,2026-08-17,2026-08-31,3000,0.65,2026-08-18
PO-3140,2,Supplier A,JAR-12OZ-CLR,2026-08-17,2026-08-31,1200,0.81,2026-08-18
PO-3147,1,Supplier C,WICK-CD10-150,2026-08-24,2026-09-14,12000,0.05,2026-08-28
PO-3147,2,Supplier C,WICK-CD12-180,2026-08-24,2026-09-14,6000,0.06,2026-08-28
PO-3147,3,Supplier C,WICK-CD10-150,2026-08-24,2026-09-28,8000,0.05,2026-08-28
PO-3152,1,Supplier B,WAX-SOY-20KG,2026-09-01,2026-09-15,80,58.00,2026-09-02
PO-3152,2,Supplier B,WAX-COCO-20KG,2026-09-01,2026-09-15,20,71.50,2026-09-02
PO-3166,1,Supplier A,JAR-8OZ-AMB,2026-09-08,2026-09-22,3000,0.62,
PO-3166,2,Supplier A,JAR-12OZ-CLR,2026-09-08,2026-09-22,1500,0.81,
```

### 4. Receiving export

```
receipt,po,line,received_date,qty_received,qty_rejected,reject_reason
RC-501,PO-3101,1,2026-07-14,2400,0,
RC-502,PO-3101,2,2026-07-14,1200,24,chipped rims
RC-503,PO-3105,1,2026-07-16,60,0,
RC-504,PO-3105,2,2026-07-16,20,1,"box torn, wax contaminated"
RC-505,PO-3110,1,2026-07-24,10000,0,
RC-506,PO-3110,2,2026-07-24,6000,0,
RC-507,PO-3118,1,2026-08-07,2400,0,
RC-508,PO-3118,2,2026-08-07,1200,0,
RC-509,PO-3133,1,2026-08-12,500,0,
RC-510,PO-3129,1,2026-08-17,60,0,
RC-511,PO-3129,2,2026-08-17,20,0,
RC-512,PO-3140,1,2026-08-31,3000,36,cracked
RC-513,PO-3140,2,2026-08-31,1200,0,
RC-514,PO-3147,1,2026-09-14,12000,0,
RC-515,PO-3147,2,2026-09-14,5400,0,
RC-516,PO-3152,1,2026-09-14,78,0,
RC-517,PO-3152,2,2026-09-14,20,1,bag split
RC-518,PO-3166,1,2026-09-22,1800,0,
RC-519,PO-3166,2,2026-09-22,1500,0,
RC-520,PO-3147,3,2026-09-25,6500,0,
RC-521,PO-3166,1,2026-09-29,1200,0,
```

### 5. Returns export

```
return,po,line,return_date,qty_returned,reason
RT-31,PO-3118,1,2026-08-20,48,clear jars sent as amber
```

### 6. Agreed-price list

```
supplier,item,agreed_price,valid_from,valid_to
Supplier A,JAR-8OZ-AMB,0.62,2026-01-01,2026-12-31
Supplier A,JAR-12OZ-CLR,0.81,2026-01-01,2026-12-31
Supplier B,WAX-SOY-20KG,58.00,2026-01-01,2026-12-31
Supplier B,WAX-COCO-20KG,71.50,2026-01-01,2026-12-31
Supplier C,WICK-CD10-150,0.05,2026-01-01,2026-12-31
Supplier C,WICK-CD12-180,0.06,2026-01-01,2026-12-31
```

### 7. Last quarter's scorecard figures

```
supplier,quarter,on_time,fill_rate,defects_returns,price_within_terms,confirmed_in_window
Supplier A,Q2 2026,88.9,99.1,0.4,100.0,100.0
Supplier B,Q2 2026,100.0,100.0,0.0,100.0,100.0
Supplier C,Q2 2026,100.0,99.0,0.0,100.0,not scored
```

## The output

The output is shown here formatted for reading, with bold headings and lists. The assistant returns the same lines, in the same order, as the plain-text format in the template.

**SUPPLIER PERFORMANCE SCORECARD: Brand R, Q3 2026 (1 July 2026 to 30 September 2026)**

For: Operations lead. Decisions by: Managing director. Prepared Tuesday 6 October 2026 from the settings, the key supplier list (3 rows), the purchase-order lines export (20 rows), the receiving export (21 rows), the returns export (1 row), the agreed-price list (6 rows) and last quarter's figures (3 rows). Compared with: Q2 2026 scorecard.

Targets: on time 95% (grace 0 days); fill rate 98%; defects and returns at most 1.0%; price within terms 100% of lines (tolerance 0%); orders confirmed within 2 days 90%. Scored with at least 5 lines, or 3 orders for confirmations. Level means a change under 2.0 points (0.5 for defects and returns).

**CHECKS**

- Rows read: key suppliers 3; order lines 20; receipts 21; returns 1; agreed prices 6; last quarter's figures 3.
- Lines due in the quarter for key suppliers: 19. Orders placed with key suppliers in the quarter: 9.
- Not on the key supplier list (not scored): Supplier D (1 line).
- Receipts or returns not matched to an order line: none.
- Over-received (counted at the ordered quantity for fill rate): none.
- Lines with no agreed price (not counted for price): none.

**SUMMARY**

- Suppliers scored: 3. Targets met: Supplier B 5 of 5; Supplier A 2 of 5; Supplier C 3 of 4.
- Sole source: Supplier C (alternative: none named).
- Decisions for the Managing director: 3.

**1. SUPPLIER B: Soy wax. Tier: preferred. Owner: Operations lead.**

- Spend: \$15,890.00 on 6 lines, 54.7% of key-supplier spend this quarter.
- Dependence: Not sole source. Alternative named: Supplier F.
- On time: 100.0% (6 of 6 lines). Target 95%: meets. Last quarter 100.0%: level. Late: none.
- Fill rate: 99.2% (258 of 260 units). Target 98%: meets. Last quarter 100.0%: level. Short: PO-3152 line 1, 78 of 80.
- Defects and returns: 0.8% (2 of 258 units: 2 rejected at receiving, 0 returned). Limit 1.0%: within. Last quarter 0.0%: worse. Rejected or returned: RC-504, PO-3105 line 2, 1 (box torn, wax contaminated); RC-517, PO-3152 line 2, 1 (bag split).
- Price against agreed terms: 100.0% (6 of 6 lines with an agreed price). Target 100%: meets. Last quarter 100.0%: level. Above agreed: none.
- Orders confirmed within 2 days: 100.0% (3 of 3 orders). Target 90%: meets. Last quarter 100.0%: level. Late or missing: none.
- Targets met: 5 of 5 scored.

Points to raise at the next review:

- Defects and returns 0.8% against a limit of 1.0%, 0.0% last quarter: 2 units rejected or returned, RC-504; RC-517. Ask what changed.

**2. SUPPLIER A: Glass jars. Tier: preferred. Owner: Operations lead.**

- Spend: \$10,953.00 on 8 lines, 37.7% of key-supplier spend this quarter.
- Dependence: Not sole source. Alternative named: Supplier E.
- On time: 62.5% (5 of 8 lines). Target 95%: below. Last quarter 88.9%: worse. Late: PO-3118 line 1, due 3 August, received 7 August (4 days late); PO-3118 line 2, due 3 August, received 7 August (4 days late); PO-3166 line 1, due 22 September, received 29 September (7 days late) in parts: 1,800 on 22 September, 1,200 on 29 September.
- Fill rate: 100.0% (15,900 of 15,900 units). Target 98%: meets. Last quarter 99.1%: level. Short: none.
- Defects and returns: 0.7% (108 of 15,900 units: 60 rejected at receiving, 48 returned). Limit 1.0%: within. Last quarter 0.4%: level. Rejected or returned: RC-502, PO-3101 line 2, 24 (chipped rims); RC-512, PO-3140 line 1, 36 (cracked); RT-31, PO-3118 line 1, 48 (clear jars sent as amber).
- Price against agreed terms: 75.0% (6 of 8 lines with an agreed price). Target 100%: below. Last quarter 100.0%: worse. Above agreed: PO-3118 line 2, JAR-12OZ-CLR, \$0.84 against \$0.81 x 1,200 = \$36.00; PO-3140 line 1, JAR-8OZ-AMB, \$0.65 against \$0.62 x 3,000 = \$90.00. Total above agreed: \$126.00.
- Orders confirmed within 2 days: 50.0% (2 of 4 orders). Target 90%: below. Last quarter 100.0%: worse. Late or missing: PO-3118, placed 20 July, confirmed 24 July (4 days); PO-3166, placed 8 September, not confirmed.
- Targets met: 2 of 5 scored.

Points to raise at the next review:

- On time 62.5% against a target of 95%, 88.9% last quarter: 3 late lines, PO-3118 line 1; PO-3118 line 2; PO-3166 line 1. Ask for the cause and what will change.
- Above the agreed price: \$126.00 on 2 lines, PO-3118 line 2; PO-3140 line 1; price against agreed terms 75.0% against a target of 100%, 100.0% last quarter. Ask how it will be corrected.
- Orders confirmed within 2 days 50.0% against a target of 90%, 100.0% last quarter: 2 orders confirmed late or not at all, PO-3118; PO-3166. Ask for the cause and what will change.

**3. SUPPLIER C: Wicks. Tier: approved. Owner: Production lead.**

- Spend: \$2,220.00 on 5 lines, 7.6% of key-supplier spend this quarter.
- Dependence: Sole source. Alternative named: none named.
- On time: 100.0% (5 of 5 lines). Target 95%: meets. Last quarter 100.0%: level. Late: none.
- Fill rate: 95.0% (39,900 of 42,000 units). Target 98%: below. Last quarter 99.0%: worse. Short: PO-3147 line 2, 5,400 of 6,000; PO-3147 line 3, 6,500 of 8,000.
- Defects and returns: 0.0% (0 of 39,900 units: 0 rejected at receiving, 0 returned). Limit 1.0%: within. Last quarter 0.0%: level. Rejected or returned: none.
- Price against agreed terms: 100.0% (5 of 5 lines with an agreed price). Target 100%: meets. Last quarter 100.0%: level. Above agreed: none.
- Orders confirmed within 2 days: too few to score (2 orders; minimum 3). Late or missing: PO-3147, placed 24 August, confirmed 28 August (4 days).
- Targets met: 3 of 4 scored.

Points to raise at the next review:

- Fill rate 95.0% against a target of 98%, 99.0% last quarter: 2 short lines, PO-3147 line 2; PO-3147 line 3. Ask for the cause and what will change.

**DECISIONS FOR THE MANAGING DIRECTOR: 3**

1. Supplier A, warning: on time 62.5% this quarter and 88.9% last quarter, against a target of 95%. Should the Operations lead give Supplier A a formal written warning about on-time delivery? A supplier issue notice can prepare it for approval.
2. Supplier A, tier: 3 of 5 scored measures below target this quarter (on time 62.5%; price against agreed terms 75.0%; orders confirmed within 2 days 50.0%). Should Supplier A stay preferred?
3. Supplier C, alternative: sole source for wicks, no alternative named; spend \$2,220.00, 7.6% of key-supplier spend; targets met 3 of 4 scored. Should the Production lead be asked to find and qualify an alternative supplier for wicks?

**NOT SUPPLIED OR NOT CHECKED**

No contract, invoice or quality certificate was read: price is the price on the order, compared with the agreed-price list as supplied. Punctuality is read from the due date each order carries; whether that date matched when the goods were really wanted is not known from these exports. Defects and returns are counted as recorded at receiving and on returns; nothing was inspected.

Every figure traces to the exports supplied for Brand R on 6 October 2026. Nothing has been sent to any supplier, and no supplier's tier or record has been changed.
