# Software subscription and vendor spend review: an invented example

*Illustrative example with invented data.* The agency, the suppliers, the people, the dates and the amounts below are all invented. The agency is an invented 38-person design and marketing agency, called Agency W here, and its suppliers are called Vendor A to Vendor Q. Its finance and operations manager is running the quarterly review of what the agency pays for. First come the inputs the finance and operations manager supplied, in full, then the review the workflow template returned.

## The inputs

### 1. Settings (typed by the finance and operations manager)

```
Company: Agency W
Today: Monday 9 November 2026
Period: 1 July 2026 to 31 October 2026
Currency: USD
Runner: Finance and operations manager
Decision-maker: Managing director
Look-ahead window: 90 days
Price-change threshold: 5%
```

### 2. Spend export (company card statement and ledger, software and subscriptions accounts, combined)

```
date,payee,description,amount,paid_by
2026-07-01,Vendor E,"Cloud file storage, monthly",480.00,direct debit
2026-07-02,Vendor G,"Website hosting, monthly, usage billed",118.40,company card
2026-07-03,Vendor A,"Design software, 14 seats, monthly",840.00,company card
2026-07-06,Vendor C,"Video meetings, monthly",300.00,company card
2026-07-11,Vendor F,"Project management, 20 seats, monthly",400.00,company card
2026-07-15,Vendor H,"Stock images, monthly",49.00,company card
2026-07-18,Vendor B,"Design software, 4 seats, monthly",220.00,company card
2026-07-20,Vendor J,"Accounting software, monthly",90.00,direct debit
2026-07-22,Vendor L,"Email marketing, yearly plan",2400.00,company card
2026-07-27,Vendor D,"Video meetings, 5 hosts",75.00,expense claim
2026-08-01,Vendor E,"Cloud file storage, monthly",480.00,direct debit
2026-08-02,Vendor G,"Website hosting, monthly, usage billed",131.20,company card
2026-08-03,Vendor A,"Design software, 14 seats, monthly",840.00,company card
2026-08-06,Vendor C,"Video meetings, monthly",300.00,company card
2026-08-11,Vendor F,"Project management, 20 seats, monthly",400.00,company card
2026-08-14,Vendor K,"Customer relationship software, annual plan, 10 users",6000.00,bill pay
2026-08-15,Vendor H,"Stock images, monthly",49.00,company card
2026-08-18,Vendor B,"Design software, 4 seats, monthly",220.00,company card
2026-08-20,Vendor J,"Accounting software, monthly",90.00,direct debit
2026-08-25,Vendor F,"Project management, 20 seats, monthly",400.00,company card
2026-08-27,Vendor D,"Video meetings, 5 hosts",75.00,expense claim
2026-09-01,Vendor E,"Cloud file storage, monthly",480.00,direct debit
2026-09-02,Vendor G,"Website hosting, monthly, usage billed",126.00,company card
2026-09-03,Vendor A,"Design software, 14 seats, monthly",840.00,company card
2026-09-06,Vendor C,"Video meetings, monthly",345.00,company card
2026-09-09,Vendor P,"Online course, one seat",199.00,company card
2026-09-11,Vendor F,"Project management, 20 seats, monthly",400.00,company card
2026-09-15,Vendor H,"Stock images, monthly",49.00,company card
2026-09-18,Vendor B,"Design software, 4 seats, monthly",220.00,company card
2026-09-20,Vendor J,"Accounting software, monthly",90.00,direct debit
2026-09-28,Vendor D,"Video meetings, 5 hosts",75.00,expense claim
2026-10-01,Vendor E,"Cloud file storage, monthly",480.00,direct debit
2026-10-02,Vendor G,"Website hosting, monthly, usage billed",140.40,company card
2026-10-03,Vendor A,"Design software, 14 seats, monthly",840.00,company card
2026-10-06,Vendor C,"Video meetings, monthly",345.00,company card
2026-10-11,Vendor F,"Project management, 20 seats, monthly",400.00,company card
2026-10-12,Vendor Q,"Survey tool, monthly plan",39.00,company card
2026-10-18,Vendor B,"Design software, 4 seats, monthly",220.00,company card
2026-10-20,Vendor J,"Accounting software, monthly",90.00,direct debit
2026-10-27,Vendor D,"Video meetings, 5 hosts",75.00,expense claim
```

### 3. Owner notes (last year's register, updated by the finance and operations manager)

```
payee,what_it_is_for,category,owner,cycle,renewal_date,annual_cost,seats_paid,seats_used,critical,fallback,switching_cost
Vendor A,Design software for the studio,design software,Creative director,monthly,,,14,11,yes,no,
Vendor B,Design software for the packaging team,design software,Senior designer,monthly,,,4,4,no,,1500
Vendor C,Video meetings with clients,video meetings,Operations lead,monthly,,,,,,,
Vendor E,Shared client files,file storage,Account director,monthly,,,,,yes,yes,
Vendor F,Project management for all staff,project management,Operations lead,monthly,,,20,20,yes,yes,
Vendor G,Hosting for the agency website,website hosting,Web developer,monthly,,,,,,,
Vendor H,Stock images,stock images,Creative director,monthly,,,,,,,
Vendor J,Accounting software,accounting,Finance and operations manager,monthly,,,,,yes,yes,
Vendor K,Client and pipeline records,CRM,Client services lead,annual,,,10,6,yes,no,
Vendor L,Newsletters to clients,email marketing,Marketing lead,annual,,,,,,,
Vendor M,Website accessibility checker,website tools,Web developer,annual,2026-12-01,1200,,,,,
Vendor N,Font licences for the studio,fonts,Creative director,annual,2027-01-15,900,,,,,
```

### 4. Leavers list

```
owner,left_on
Account director,2026-08-31
```

## The output

The output is shown here formatted for reading, with bold headings and lists. The assistant returns the same sections, in the same order, as the plain-text format in the template.

**SOFTWARE SUBSCRIPTION AND VENDOR SPEND REVIEW: Agency W, 1 July 2026 to 31 October 2026**

For: Finance and operations manager. Decisions by: Managing director. Prepared Monday 9 November 2026 from the settings, the spend export (40 rows), the owner notes (12 rows) and the leavers list (1 row).

**SUMMARY**

Register: 13 subscriptions: 9 monthly (1 with charges stopped), 2 annual charged in the period, 2 annual from the owner notes.

Annual cost of the 12 active subscriptions with a known cost: \$41,448.00 (\$3,454.00 a month).

Paid in the period: \$19,411.00 (company card \$10,831.00; bill pay \$6,000.00; direct debit \$2,280.00; expense claim \$300.00), of which \$238.00 to payees not classed.

Renewals in the next 90 days: 2. Flags: 8. Consolidation candidates: 2.

**REGISTER (by annual cost, highest first)**

1. **Vendor A:** Design software for the studio. Category: design software. Owner: Creative director. Paid by: company card. Monthly, \$840.00 a month, last charged 3 October 2026. Annual cost: \$10,080.00 (latest charge x 12). Seats: 11 of 14 used.
2. **Vendor K:** Client and pipeline records. Category: CRM. Owner: Client services lead. Paid by: bill pay. Annual, charged 14 August 2026. Annual cost: \$6,000.00 (as charged). Renews: Saturday 14 August 2027, estimated from the charge. Seats: 6 of 10 used.
3. **Vendor E:** Shared client files. Category: file storage. Owner: Account director. Paid by: direct debit. Monthly, \$480.00 a month, last charged 1 October 2026. Annual cost: \$5,760.00 (latest charge x 12).
4. **Vendor F:** Project management for all staff. Category: project management. Owner: Operations lead. Paid by: company card. Monthly, \$400.00 a month, last charged 11 October 2026. Annual cost: \$4,800.00 (latest charge x 12). Seats: 20 of 20 used.
5. **Vendor C:** Video meetings with clients. Category: video meetings. Owner: Operations lead. Paid by: company card. Monthly, \$345.00 a month, last charged 6 October 2026. Annual cost: \$4,140.00 (latest charge x 12).
6. **Vendor B:** Design software for the packaging team. Category: design software. Owner: Senior designer. Paid by: company card. Monthly, \$220.00 a month, last charged 18 October 2026. Annual cost: \$2,640.00 (latest charge x 12). Seats: 4 of 4 used.
7. **Vendor L:** Newsletters to clients. Category: email marketing. Owner: Marketing lead. Paid by: company card. Annual, charged 22 July 2026. Annual cost: \$2,400.00 (as charged). Renews: Thursday 22 July 2027, estimated from the charge.
8. **Vendor G:** Hosting for the agency website. Category: website hosting. Owner: Web developer. Paid by: company card. Monthly, varies, average \$129.00 a month over 4 months, last charged 2 October 2026. Annual cost: \$1,548.00 (average x 12).
9. **Vendor M:** Website accessibility checker. Category: website tools. Owner: Web developer. Paid by: no charge in the period. Annual, no charge in the period. Annual cost: \$1,200.00 (as supplied). Renews: Tuesday 1 December 2026, as supplied.
10. **Vendor J:** Accounting software. Category: accounting. Owner: Finance and operations manager. Paid by: direct debit. Monthly, \$90.00 a month, last charged 20 October 2026. Annual cost: \$1,080.00 (latest charge x 12).
11. **Vendor D:** Video meetings, 5 hosts (from the description). Category: video meetings (suggested). Owner: none on record. Paid by: expense claim. Monthly, \$75.00 a month, last charged 27 October 2026. Annual cost: \$900.00 (latest charge x 12).
12. **Vendor N:** Font licences for the studio. Category: fonts. Owner: Creative director. Paid by: no charge in the period. Annual, no charge in the period. Annual cost: \$900.00 (as supplied). Renews: Friday 15 January 2027, as supplied.

Charges stopped: **Vendor H:** Stock images. Last charged 15 September 2026, \$49.00; no charge in October 2026. Annual cost not counted.

**SPEND BY CATEGORY (active, known cost; shares rounded to whole percent)**

- Design software: \$12,720.00, 31%, 2 subscriptions.
- CRM: \$6,000.00, 14%, 1 subscription.
- File storage: \$5,760.00, 14%, 1 subscription.
- Video meetings (includes suggested): \$5,040.00, 12%, 2 subscriptions.
- Project management: \$4,800.00, 12%, 1 subscription.
- Email marketing: \$2,400.00, 6%, 1 subscription.
- Website hosting: \$1,548.00, 4%, 1 subscription.
- Website tools: \$1,200.00, 3%, 1 subscription.
- Accounting: \$1,080.00, 3%, 1 subscription.
- Fonts: \$900.00, 2%, 1 subscription.

**RENEWALS IN THE NEXT 90 DAYS (annual subscriptions, to Sunday 7 February 2027)**

- Tuesday 1 December 2026, 22 days from today: Vendor M, \$1,200.00 a year, renewal date as supplied. Owner: Web developer.
- Friday 15 January 2027, 67 days from today: Vendor N, \$900.00 a year, renewal date as supplied. Owner: Creative director.

**RENEWAL CLUSTERS (months with three or more annual renewals, November 2026 to October 2027)**

None.

**FLAGS: 8**

- **No owner on record:** Vendor D.
- **Owner has left:** Vendor E: Account director, left 31 August 2026; charged since: 2 charges, \$960.00.
- **Paid on an expense claim or personal card:** Vendor D: 4 charges, \$300.00 in the period.
- **Charge changed by 5% or more:** Vendor C: \$300.00 to \$345.00 from September 2026 (+15.0%).
- **Unused seats:** Vendor A: 3 of 14 unused; about \$2,160.00 a year at the average cost per paid seat.
- **Unused seats:** Vendor K: 4 of 10 unused; about \$2,400.00 a year at the average cost per paid seat.
- **More than one charge in a month:** Vendor F: August 2026: \$400.00 on 11 August 2026 and \$400.00 on 25 August 2026.
- **Charges stopped:** Vendor H: last charged 15 September 2026.

**CONSOLIDATION CANDIDATES: 2**

1. **Design software:** Vendor A (\$10,080.00 a year, owner Creative director); Vendor B (\$2,640.00 a year, owner Senior designer). Combined: \$12,720.00 a year. Keeping one would save between \$2,640.00 and \$10,080.00 a year, before switching costs, depending on which is kept. Switching cost, as supplied: Vendor A not known; Vendor B \$1,500.00. Critical with no written fallback: Vendor A. Write a fallback before any consolidation.
2. **Video meetings (suggested for Vendor D; to confirm):** Vendor C (\$4,140.00 a year, owner Operations lead); Vendor D (\$900.00 a year, owner none on record). Combined: \$5,040.00 a year. Keeping one would save between \$900.00 and \$4,140.00 a year, before switching costs, depending on which is kept. Switching cost, as supplied: Vendor C not known; Vendor D not known.

**NOT CLASSED (one or two months, no annual marker)**

- Vendor P: "Online course, one seat", 9 September 2026, \$199.00.
- Vendor Q: "Survey tool, monthly plan", 12 October 2026, \$39.00.

**QUESTIONS: 9, for the Finance and operations manager to decide whether to ask**

1. To the Creative director: 11 of 14 Vendor A seats are used; the 3 unused cost about \$2,160.00 a year. Can the seat count be reduced at the next monthly charge?
2. To the Client services lead: 6 of 10 Vendor K seats are used; the 4 unused cost about \$2,400.00 a year. Can the renewal, estimated for 14 August 2027, be set at fewer seats?
3. To the Operations lead: Vendor C's monthly charge went from \$300.00 to \$345.00 in September 2026 (+15.0%). Was that a price rise, or more seats or use?
4. To the Operations lead: Vendor F charged \$400.00 twice in August 2026, on 11 and 25 August. Was the second charge expected?
5. To the Creative director: Vendor H was last charged on 15 September 2026 and not in October 2026. Was it cancelled, or is it paid some other way now?
6. To the Finance and operations manager: Vendor D, video meetings for 5 hosts, has no owner on record and was paid on 4 expense claims, \$300.00 in the period. Who uses it, and is it still needed?
7. To the Creative director and the Senior designer: Vendor A and Vendor B are both design software, \$12,720.00 a year together. Do they do the same work, and what would moving to one involve?
8. To the Operations lead and the Finance and operations manager (no owner on record for Vendor D): Vendor C and Vendor D both provide video meetings, \$5,040.00 a year together; Vendor D's category is suggested from its description. Do they do the same work, and what would moving to one involve?
9. To the Finance and operations manager: Vendor P (\$199.00 on 9 September 2026) and Vendor Q (\$39.00 on 12 October 2026, described as a monthly plan) were each charged once. Are any of them subscriptions?

**DECISIONS FOR THE MANAGING DIRECTOR: 6**

1. Vendor M, the website accessibility checker, renews on Tuesday 1 December 2026, 22 days from today, at \$1,200.00 a year; the date is as supplied in the owner notes. Notice terms were not supplied; confirm them with whoever holds the agreement. Renew, change or end? A vendor renewal review can prepare it in depth.
2. Vendor N, the font licences for the studio, renews on Friday 15 January 2027, 67 days from today, at \$900.00 a year; the date is as supplied in the owner notes. Notice terms were not supplied; confirm them with whoever holds the agreement. Renew, change or end? A vendor renewal review can prepare it in depth.
3. Vendor E, the shared client files, is owned by the Account director, who left on 31 August 2026; 2 charges, \$960.00, have been paid since. Who takes it over, or should it end?
4. Vendor D is paid on expense claims: 4 charges, \$300.00 in the period. Once question 6 is answered, should it move to a company payment method?
5. Vendor A and Vendor B are both design software, \$12,720.00 a year together; keeping one would save between \$2,640.00 and \$10,080.00 a year before switching costs. Should the Creative director and the Senior designer look into moving to one tool? Vendor A is marked critical with no written fallback: should a fallback be written first, and by whom?
6. Vendor C and Vendor D both provide video meetings, \$5,040.00 a year together; keeping one would save between \$900.00 and \$4,140.00 a year before switching costs. Should the Operations lead and the Finance and operations manager (no owner on record for Vendor D) look into moving to one tool?

**NOT SUPPLIED OR NOT CHECKED**

No agreement, order form or terms were read; renewal dates are as supplied or estimated from the charge history, and notice terms are not known. Seats, owners and whether a subscription is critical are as supplied in the owner notes. Annual subscriptions charged before 1 July 2026 appear only if they are on the owner notes. Payees with different names were not merged.

Every figure traces to the inputs supplied for Agency W on 9 November 2026. Nothing has been cancelled, changed, paid or sent.
