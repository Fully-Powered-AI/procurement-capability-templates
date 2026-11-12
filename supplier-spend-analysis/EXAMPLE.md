# Supplier spend analysis: an invented example

*Illustrative example with invented data.* The company, the suppliers, the people, the dates and the amounts below are all invented. The company is an invented 60-person bakery and snack manufacturer, called Maker K here, and its suppliers are called Supplier A to Supplier Y. Two payees whose rows are left out as not supplier spend are called Tax authority and Lender A. Its finance manager is looking at where the business spent with suppliers last quarter, before next year's budget. First come the inputs the finance manager supplied, in full, then the analysis the workflow template returned.

## The inputs

### 1. Settings (typed by the finance manager)

```
Company: Maker K
Today: Tuesday 10 November 2026
Period: 1 July 2026 to 30 September 2026
Currency: USD
Runner: Finance manager
Decision-maker: Managing director
Concentration line: 80%
Consolidation floor: $10,000 in the period
Saving assumption: 3% to 6%
Accounts to leave out: Sales tax payable; Loan repayments
```

### 2. Accounts-payable export (bills and credit notes, 1 July to 30 September 2026)

```
date,supplier,invoice,description,account,amount
2026-07-01,Supplier W,W-0701,"Rent, unit 4, July",Rent,12000.00
2026-07-03,Supplier A,A-5512,"Bread flour and rye, July",Ingredients,31840.00
2026-07-05,Supplier B,B-2201,"Butter and cream, July",Ingredients,26300.00
2026-07-07,Supplier S,S-1201,"Paper, toner, stationery",Office supplies,520.00
2026-07-08,Supplier C,C-901,"Sugar and glucose syrup",Ingredients,13600.00
2026-07-09,Supplier G,G-3310,"Shipping cartons, 12-pack",Packaging,7980.00
2026-07-10,Supplier Q,Q-301,"Sanitiser and hygiene consumables",Cleaning and hygiene,1980.00
2026-07-12,Supplier V,V-07,"Electricity and gas, July",Utilities,8640.00
2026-07-14,Supplier D,D-77,"Walnuts, almonds, raisins",Ingredients,5450.00
2026-07-15,Supplier K,K-118,"Printed labels and wrap film",Packaging,4950.00
2026-07-16,Supplier M,M-4410,"Pallet deliveries, July part 1",Freight,1240.00
2026-07-18,Supplier H Ltd,H-1009,"Display boxes",Packaging,3100.00
2026-07-20,Tax authority,ST-Q2,"Sales tax, second quarter",Sales tax payable,9850.00
2026-07-21,Supplier E,E-410,"Spelt and wholemeal flour",Ingredients,5900.00
2026-07-22,Supplier N,N-77120,"Courier parcels",Freight,380.00
2026-07-24,Supplier P,P-55,"Oven service visit",Repairs and maintenance,2650.00
2026-07-28,Supplier Y,Y-610,"Product testing, batch samples",Laboratory testing,2100.00
2026-07-30,Supplier X,X-2026-07,"Quarterly bookkeeping review",Professional fees,7500.00
2026-07-31,Supplier L,L-7781,"Chilled freight, July",Freight,5860.00
2026-07-31,Lender A,LN-0731,"Equipment loan, July",Loan repayments,4200.00
2026-08-01,Supplier W,W-0801,"Rent, unit 4, August",Rent,12000.00
2026-08-04,Supplier A,A-5578,"Bread flour and rye, August",Ingredients,32610.00
2026-08-05,Supplier B,B-2264,"Butter and cream, August",Ingredients,25880.00
2026-08-06,Supplier S,S-1288,"Paper and stationery",Office supplies,480.00
2026-08-07,Supplier M Express,MX-88,"Same-day pallet delivery",Freight,960.00
2026-08-10,Supplier C,C-944,"Sugar and glucose syrup",Ingredients,14250.00
2026-08-11,Supplier G,G-3372,"Shipping cartons, 12-pack",Packaging,8240.00
2026-08-12,Supplier Q,Q-322,"Sanitiser and hygiene consumables",Cleaning and hygiene,2040.00
2026-08-12,Supplier V,V-08,"Electricity and gas, August",Utilities,9210.00
2026-08-14,Supplier M,M-4466,"Pallet deliveries, August",Freight,1310.00
2026-08-17,Supplier K,K-131,"Printed labels and wrap film",Packaging,5180.00
2026-08-19,Supplier B,B-CN-118,"Credit, returned cream, short date",Ingredients,-420.00
2026-08-19,Supplier N,N-77395,"Courier parcels",Freight,410.00
2026-08-20,SUPPLIER H LTD.,H-1032,"Display boxes",Packaging,2950.00
2026-08-21,Supplier F,F-12,"Hazelnuts and dried apricots",Ingredients,3500.00
2026-08-25,Supplier R,R-44,"Floor cleaner and gloves",Cleaning and hygiene,880.00
2026-08-26,Supplier D,D-82,"Walnuts, almonds, raisins",Ingredients,5550.00
2026-08-28,Supplier P,P-61,"Mixer gearbox repair",Repairs and maintenance,3900.00
2026-08-29,Supplier U,U-3,"Batteries and torches",,186.00
2026-08-31,Supplier L,L-7840,"Chilled freight, August",Freight,6120.00
2026-08-31,Lender A,LN-0831,"Equipment loan, August",Loan repayments,4200.00
2026-09-01,Supplier W,W-0901,"Rent, unit 4, September",Rent,12000.00
2026-09-02,Supplier E,E-433,"Spelt and wholemeal flour",Ingredients,6100.00
2026-09-03,Supplier A,A-5641,"Bread flour and rye, September",Ingredients,30950.00
2026-09-04,Supplier S,S-1340,"Paper, toner, stationery",Office supplies,510.00
2026-09-05,Supplier B,B-2330,"Butter and cream, September",Ingredients,26140.00
2026-09-08,Supplier N,N-77608,"Courier parcels",Freight,420.00
2026-09-09,Supplier C,C-987,"Sugar and glucose syrup",Ingredients,13150.00
2026-09-10,Supplier G,G-3419,"Shipping cartons, 12-pack",Packaging,7780.00
2026-09-11,Supplier Q,Q-345,"Sanitiser and hygiene consumables",Cleaning and hygiene,1980.00
2026-09-12,Supplier V,V-09,"Electricity and gas, September",Utilities,8950.00
2026-09-15,Supplier J,J-501,"Shipping cartons, rush order",Packaging,2400.00
2026-09-16,Supplier K,K-144,"Printed labels and wrap film",Packaging,4870.00
2026-09-17,Supplier M,M-4502,"Pallet deliveries, September",Freight,1150.00
2026-09-18,Supplier T,T-9,"Desk chairs, two",Office supplies,615.00
2026-09-22,Supplier H,H-1057,"Display boxes",Packaging,3050.00
2026-09-24,Supplier M Express,MX-93,"Same-day pallet delivery",Freight,840.00
2026-09-25,Supplier P,P-66,"Thermostat replacement",Repairs and maintenance,1450.00
2026-09-29,Supplier Y,Y-655,"Product testing, batch samples",Laboratory testing,2100.00
2026-09-30,Supplier L,L-7902,"Chilled freight, September",Freight,6020.00
2026-09-30,Lender A,LN-0930,"Equipment loan, September",Loan repayments,4200.00
```

### 3. Category map (kept by the finance manager with the budget holders)

```
supplier,category,owner
Supplier A,Flour and grains,Production manager
Supplier E,Flour and grains,Production manager
Supplier B,Dairy,Production manager
Supplier C,Sugar and syrups,Production manager
Supplier D,Nuts and dried fruit,Production manager
Supplier F,Nuts and dried fruit,Production manager
Supplier G,Cartons and boxes,Production manager
Supplier H,Cartons and boxes,Production manager
Supplier J,Cartons and boxes,Production manager
Supplier K,Labels and film,Production manager
Supplier L,Freight,Operations manager
Supplier M,Freight,Operations manager
Supplier N,Freight,Operations manager
Supplier P,Equipment maintenance,Operations manager
Supplier Q,Cleaning and hygiene,Operations manager
Supplier R,Cleaning and hygiene,Operations manager
Supplier S,Office supplies,Office manager
Supplier V,Energy,Finance manager
Supplier W,Rent,Finance manager
Supplier X,Accounting,Finance manager
Supplier Y,Laboratory testing,Quality lead
```

## The output

The output is shown here formatted for reading, with bold headings and lists. The assistant returns the same sections, in the same order, as the plain-text format in the template.

**SUPPLIER SPEND ANALYSIS: Maker K, 1 July 2026 to 30 September 2026**

For: Finance manager. Decisions by: Managing director. Prepared Tuesday 10 November 2026 from the settings, the accounts-payable export (61 rows) and the category map (21 rows). All figures are for the period, in USD; nothing is annualised.

**CLEANING**

- Rows read: 61. Left out: 4 rows, \$22,450.00 (Loan repayments: 3 rows, \$12,600.00; Sales tax payable: 1 row, \$9,850.00).
- Credit notes: 1, -\$420.00, netted against their suppliers (Supplier B -\$420.00).
- Names merged: Supplier H Ltd: "Supplier H Ltd", "SUPPLIER H LTD.", "Supplier H" (3 rows).
- Possible same supplier, not merged: Supplier M and Supplier M Express.
- Not coded: 1 row, \$186.00 (Supplier U \$186.00).
- Not on the category map: Supplier M Express (placed by its account, Freight); Supplier T (placed by its account, Office supplies); Supplier U (not coded).
- Net or zero after credits: none.
- Spend analysed: \$407,701.00, 24 suppliers, 56 bills and 1 credit note.

**SUMMARY**

- 24 suppliers (8 in the concentration group) across 14 categories, plus \$186.00 not coded.
- Concentration: 8 of 24 suppliers (33.3%) take 81.9% of spend (\$334,100.00).
- Tail: 16 suppliers (66.7%) take 18.1% (\$73,601.00) in 32 bills.
- Same need, more than one supplier: 6 categories. Consolidation opportunities: 4.

**SPEND BY CATEGORY (highest first; shares rounded to one decimal place)**

- Flour and grains: \$107,400.00, 26.3%, 2 suppliers, 5 bills. Owner: Production manager.
- Dairy: \$77,900.00, 19.1%, 1 supplier, 3 bills. Owner: Production manager.
- Sugar and syrups: \$41,000.00, 10.1%, 1 supplier, 3 bills. Owner: Production manager.
- Rent: \$36,000.00, 8.8%, 1 supplier, 3 bills. Owner: Finance manager.
- Cartons and boxes: \$35,500.00, 8.7%, 3 suppliers, 7 bills. Owner: Production manager.
- Energy: \$26,800.00, 6.6%, 1 supplier, 3 bills. Owner: Finance manager.
- Freight (includes from the account): \$24,710.00, 6.1%, 4 suppliers, 11 bills. Owner: Operations manager.
- Labels and film: \$15,000.00, 3.7%, 1 supplier, 3 bills. Owner: Production manager.
- Nuts and dried fruit: \$14,500.00, 3.6%, 2 suppliers, 3 bills. Owner: Production manager.
- Equipment maintenance: \$8,000.00, 2.0%, 1 supplier, 3 bills. Owner: Operations manager.
- Accounting: \$7,500.00, 1.8%, 1 supplier, 1 bill. Owner: Finance manager.
- Cleaning and hygiene: \$6,880.00, 1.7%, 2 suppliers, 4 bills. Owner: Operations manager.
- Laboratory testing: \$4,200.00, 1.0%, 1 supplier, 2 bills. Owner: Quality lead.
- Office supplies (includes from the account): \$2,125.00, 0.5%, 2 suppliers, 4 bills. Owner: Office manager.
- Not coded: \$186.00, 0.0%, 1 supplier, 1 bill.

**SPEND BY SUPPLIER (highest first)**

1. Supplier A: \$95,400.00, 23.4% (cumulative 23.4%). Flour and grains. 3 bills. Concentration group.
2. Supplier B: \$77,900.00, 19.1% (cumulative 42.5%). Dairy. 3 bills, 1 credit note. Concentration group.
3. Supplier C: \$41,000.00, 10.1% (cumulative 52.6%). Sugar and syrups. 3 bills. Concentration group.
4. Supplier W: \$36,000.00, 8.8% (cumulative 61.4%). Rent. 3 bills. Concentration group.
5. Supplier V: \$26,800.00, 6.6% (cumulative 68.0%). Energy. 3 bills. Concentration group.
6. Supplier G: \$24,000.00, 5.9% (cumulative 73.9%). Cartons and boxes. 3 bills. Concentration group.
7. Supplier L: \$18,000.00, 4.4% (cumulative 78.3%). Freight. 3 bills. Concentration group.
8. Supplier K: \$15,000.00, 3.7% (cumulative 81.9%). Labels and film. 3 bills. Concentration group.
9. Supplier E: \$12,000.00, 2.9% (cumulative 84.9%). Flour and grains. 2 bills. Tail.
10. Supplier D: \$11,000.00, 2.7% (cumulative 87.6%). Nuts and dried fruit. 2 bills. Tail.
11. Supplier H Ltd: \$9,100.00, 2.2% (cumulative 89.8%). Cartons and boxes. 3 bills. Tail.
12. Supplier P: \$8,000.00, 2.0% (cumulative 91.8%). Equipment maintenance. 3 bills. Tail.
13. Supplier X: \$7,500.00, 1.8% (cumulative 93.6%). Accounting. 1 bill. Tail.
14. Supplier Q: \$6,000.00, 1.5% (cumulative 95.1%). Cleaning and hygiene. 3 bills. Tail.
15. Supplier Y: \$4,200.00, 1.0% (cumulative 96.1%). Laboratory testing. 2 bills. Tail.
16. Supplier M: \$3,700.00, 0.9% (cumulative 97.0%). Freight. 3 bills. Tail.
17. Supplier F: \$3,500.00, 0.9% (cumulative 97.9%). Nuts and dried fruit. 1 bill. Tail.
18. Supplier J: \$2,400.00, 0.6% (cumulative 98.5%). Cartons and boxes. 1 bill. Tail.
19. Supplier M Express: \$1,800.00, 0.4% (cumulative 98.9%). Freight (from the account). 2 bills. Tail.
20. Supplier S: \$1,510.00, 0.4% (cumulative 99.3%). Office supplies. 3 bills. Tail.
21. Supplier N: \$1,210.00, 0.3% (cumulative 99.6%). Freight. 3 bills. Tail.
22. Supplier R: \$880.00, 0.2% (cumulative 99.8%). Cleaning and hygiene. 1 bill. Tail.
23. Supplier T: \$615.00, 0.2% (cumulative 100.0%). Office supplies (from the account). 1 bill. Tail.
24. Supplier U: \$186.00, 0.0% (cumulative 100.0%). Not coded. 1 bill. Tail.

**CONCENTRATION (line: 80%)**

8 of 24 suppliers (33.3%) take \$334,100.00, 81.9% of spend: Supplier A; Supplier B; Supplier C; Supplier W; Supplier V; Supplier G; Supplier L; Supplier K. The group ends at the first supplier whose cumulative share reaches 80%.

Largest supplier: Supplier A, 23.4% of spend.

**TAIL**

16 suppliers (66.7% of suppliers) take \$73,601.00, 18.1% of spend, in 32 bills; average bill \$2,300.03. Billed once in the period: 6 (Supplier X; Supplier F; Supplier J; Supplier R; Supplier T; Supplier U)

Tail spend by category: Nuts and dried fruit \$14,500.00 (2 suppliers); Flour and grains \$12,000.00 (1 supplier); Cartons and boxes \$11,500.00 (2 suppliers); Equipment maintenance \$8,000.00 (1 supplier); Accounting \$7,500.00 (1 supplier); Cleaning and hygiene \$6,880.00 (2 suppliers); Freight \$6,710.00 (3 suppliers); Laboratory testing \$4,200.00 (1 supplier); Office supplies \$2,125.00 (2 suppliers); Not coded \$186.00 (1 supplier)

**SAME NEED, MORE THAN ONE SUPPLIER**

- Flour and grains: \$107,400.00, 2 suppliers: Supplier A \$95,400.00 (88.8%); Supplier E \$12,000.00 (11.2%).
- Cartons and boxes: \$35,500.00, 3 suppliers: Supplier G \$24,000.00 (67.6%); Supplier H Ltd \$9,100.00 (25.6%); Supplier J \$2,400.00 (6.8%).
- Freight: \$24,710.00, 4 suppliers: Supplier L \$18,000.00 (72.8%); Supplier M \$3,700.00 (15.0%); Supplier M Express \$1,800.00 (7.3%); Supplier N \$1,210.00 (4.9%).
- Nuts and dried fruit: \$14,500.00, 2 suppliers: Supplier D \$11,000.00 (75.9%); Supplier F \$3,500.00 (24.1%).
- Cleaning and hygiene: \$6,880.00, 2 suppliers: Supplier Q \$6,000.00 (87.2%); Supplier R \$880.00 (12.8%). Below the consolidation floor of \$10,000.00.
- Office supplies: \$2,125.00, 2 suppliers: Supplier S \$1,510.00 (71.1%); Supplier T \$615.00 (28.9%). Below the consolidation floor of \$10,000.00.

**CONSOLIDATION OPPORTUNITIES: 4 (categories at or above \$10,000.00 with more than one supplier)**

1. Flour and grains: \$107,400.00 with 2 suppliers. Largest by spend (not a recommendation): Supplier A, \$95,400.00 (88.8%). With the other 1: \$12,000.00 in 2 bills. At your assumption of 3% to 6% of the category's spend: \$3,222.00 to \$6,444.00 in the period; an assumption, not a quote.
2. Cartons and boxes: \$35,500.00 with 3 suppliers. Largest by spend (not a recommendation): Supplier G, \$24,000.00 (67.6%). With the other 2: \$11,500.00 in 4 bills. At your assumption of 3% to 6% of the category's spend: \$1,065.00 to \$2,130.00 in the period; an assumption, not a quote.
3. Freight: \$24,710.00 with 4 suppliers. Largest by spend (not a recommendation): Supplier L, \$18,000.00 (72.8%). With the other 3: \$6,710.00 in 8 bills. At your assumption of 3% to 6% of the category's spend: \$741.30 to \$1,482.60 in the period; an assumption, not a quote.
4. Nuts and dried fruit: \$14,500.00 with 2 suppliers. Largest by spend (not a recommendation): Supplier D, \$11,000.00 (75.9%). With the other 1: \$3,500.00 in 1 bill. At your assumption of 3% to 6% of the category's spend: \$435.00 to \$870.00 in the period; an assumption, not a quote.

**QUESTIONS: 6, for the Finance manager to decide whether to ask**

1. To the Finance manager: Supplier M (3 bills, \$3,700.00) and Supplier M Express (2 bills, \$1,800.00) are both coded to Freight and were not merged. Are they the same supplier?
2. To the Finance manager: Supplier M Express (placed by its account, Freight), Supplier T (placed by its account, Office supplies) and Supplier U (not coded; one bill, "Batteries and torches", \$186.00) are not on the category map. Which category does each belong in?
3. To the Production manager: Flour and grains went to Supplier A (\$95,400.00) and Supplier E (\$12,000.00). Do they supply the same thing, and is there a reason each is used, such as a specification, a site or a backup?
4. To the Production manager: Cartons and boxes went to Supplier G (\$24,000.00), Supplier H Ltd (\$9,100.00) and Supplier J (\$2,400.00). Do they supply the same thing, and is there a reason each is used, such as a specification, a site or a backup?
5. To the Operations manager: Freight went to Supplier L (\$18,000.00), Supplier M (\$3,700.00), Supplier M Express (\$1,800.00) and Supplier N (\$1,210.00). Do they supply the same thing, and is there a reason each is used, such as a specification, a site or a backup?
6. To the Production manager: Nuts and dried fruit went to Supplier D (\$11,000.00) and Supplier F (\$3,500.00). Do they supply the same thing, and is there a reason each is used, such as a specification, a site or a backup?

**DECISIONS FOR THE MANAGING DIRECTOR: 5**

1. Flour and grains: \$107,400.00 with 2 suppliers; \$12,000.00 went to suppliers other than the largest. At your assumption of 3% to 6%, \$3,222.00 to \$6,444.00 in the period. Should the Production manager look into moving flour and grains to fewer suppliers, once question 3 is answered? A vendor quote comparison can prepare the choice.
2. Cartons and boxes: \$35,500.00 with 3 suppliers; \$11,500.00 went to suppliers other than the largest. At your assumption of 3% to 6%, \$1,065.00 to \$2,130.00 in the period. Should the Production manager look into moving cartons and boxes to fewer suppliers, once question 4 is answered? A vendor quote comparison can prepare the choice.
3. Freight: \$24,710.00 with 4 suppliers; \$6,710.00 went to suppliers other than the largest. At your assumption of 3% to 6%, \$741.30 to \$1,482.60 in the period. Should the Operations manager look into moving freight to fewer suppliers, once question 5 is answered? A vendor quote comparison can prepare the choice.
4. Nuts and dried fruit: \$14,500.00 with 2 suppliers; \$3,500.00 went to suppliers other than the largest. At your assumption of 3% to 6%, \$435.00 to \$870.00 in the period. Should the Production manager look into moving nuts and dried fruit to fewer suppliers, once question 6 is answered? A vendor quote comparison can prepare the choice.
5. The tail: 16 of 24 suppliers took \$73,601.00 (18.1% of spend) in 32 bills, and 6 of them were billed once in the period. Should anyone look at whether this spend can go through suppliers already used, and who?

**NOT SUPPLIED OR NOT CHECKED**

No contract, price list, quote or delivery record was read, so whether two suppliers sell the same item, at what price or on what terms is not known from this export. Categories are as set on the category map or the account each bill was coded to. Spend is what was billed in the period, not what was committed or paid. Names that differ other than by case, punctuation, spacing or a legal ending were not merged.

Every figure traces to the inputs supplied for Maker K on 10 November 2026. Nothing has been sent, paid, changed or agreed with any supplier.
