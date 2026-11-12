# Vendor renewal review: an invented example

*Illustrative example with invented data.* The company, the supplier, the people, the dates and the amounts below are all invented. The company is an invented 85-person regional delivery business. Its operations lead is reviewing the renewal of its dispatch software, from an invented supplier called Supplier D here. First come the inputs the operations lead supplied, in full, then the page the workflow template returned.

## The inputs

### 1. Renewal facts (typed by the operations lead)

```
Supplier: Supplier D
Supplies: dispatch and route-planning software, with a driver app
Today: Monday 9 November 2026
Term: 1 February 2026 to 31 January 2027
At the end: renews automatically for 12 months unless notice is given
Notice: 60 calendar days before the term end
Dates supplied by: Finance director, from the signed order form
Teams that use it: dispatch (day and night shifts), drivers, the
  customer service desk
Current annual price: $43,200
Unit prices: dispatcher seats, 30 at $90 a month; driver app licences,
  60 at $15 a month; extra driver licences $20 a month each
Renewal quote, received 2 November 2026: dispatcher seat $99 a month;
  driver app licence $16.50 a month; extra driver licences $22 a month;
  no quantities given
Currency: USD
Decision-maker: Managing director
Decision lead: 14 days
```

### 2. Use export (from the supplier's admin screen)

```
period,measure,paid_for,used
2026-05,dispatcher seats,30,26
2026-05,driver app licences,60,57
2026-06,dispatcher seats,30,25
2026-06,driver app licences,60,58
2026-07,dispatcher seats,30,24
2026-07,driver app licences,60,58
2026-08,dispatcher seats,30,22
2026-08,driver app licences,60,59
2026-09,dispatcher seats,30,22
2026-09,driver app licences,60,61
2026-10,dispatcher seats,30,21
2026-10,driver app licences,60,62
```

### 3. Invoices export (from the accounting system)

```
invoice_date,invoice_number,description,type,amount
2026-02-28,D-2602,Subscription February,base,3600.00
2026-03-31,D-2603,Subscription March,base,3600.00
2026-04-30,D-2604,Subscription April,base,3600.00
2026-04-30,D-2604,Onboarding training day for night dispatch,extra,900.00
2026-05-31,D-2605,Subscription May,base,3600.00
2026-06-30,D-2606,Subscription June,base,3600.00
2026-07-31,D-2607,Subscription July,base,3600.00
2026-07-31,D-2607,Service credit for 3 June outage,credit,-180.00
2026-08-31,D-2608,Subscription August,base,3600.00
2026-09-30,D-2609,Subscription September,base,3600.00
2026-09-30,D-2609,Additional driver licences (1),extra,20.00
2026-10-31,D-2610,Subscription October,base,3600.00
2026-10-31,D-2610,Additional driver licences (2),extra,40.00
```

### 4. Commitments and service log (kept by the operations lead)

```
Commitments, as I read them in Supplier D's service description:
- Availability: the system is available at least 99.5% of each month.
- Priority-1 response: first response within 1 hour on a priority-1
  ticket.

date,what_happened,commitment,met,credit_due,credit_received
2026-03-12,Dispatch screen froze for 25 minutes,Priority-1 response,yes,,
2026-06-03,Outage of 4 hours 10 minutes; morning dispatch on paper,Availability,no,180,180
2026-06-03,First response to the outage ticket after 2 hours,Priority-1 response,no,,
2026-08-19,Route import failed for 1 hour 40 minutes,Priority-1 response,yes,,
2026-09-08,Outage of 3 hours 30 minutes,Availability,no,180,
2026-10-14,Driver app sync down for 50 minutes,Priority-1 response,no,,
2026-10-27,Driver app crashing on login,Priority-1 response,yes,,
```

### 5. Team notes

```
Dispatch supervisor: "Since July the night shift plans routes on a
spreadsheet; they found the planning board slow at night. The day
shift uses it all day."
Driver team lead: "Drivers rely on the app for every drop. The login
crashes in late October were sorted within a day."
Customer service lead: "We look up delivery status in it several times
an hour."
```

### 6. Dependence notes (typed by the operations lead)

```
If it stopped: stops the work. Dispatch goes to paper and the driver
  app shows nothing.
Written fallback: no. On 3 June the morning was run on paper from
  memory.
Company data it holds: customer delivery addresses, driver names and
  mobile numbers, delivery history.
Costs of leaving: not known.
```

## The output

**VENDOR RENEWAL REVIEW: Supplier D, dispatch and route-planning software, with a driver app**

For: Operations lead. Decision by: Managing director. Prepared Monday 9 November 2026 from the renewal facts, the use export (12 rows), the invoices export (13 rows), 2 commitments and the service log (7 rows), 3 team notes and the dependence notes.

**DATES**

- **Term ends:** Sunday 31 January 2027, 83 days from today. At the end: renews automatically for 12 months unless notice is given, as supplied by the finance director, from the signed order form.
- **Notice date:** Wednesday 2 December 2026, 23 days from today (computed: term end minus 60 days, from the period supplied).
- **Decide by:** Wednesday 18 November 2026, 9 days from today (14 days before the notice date).
- **Status:** ON TRACK.

**USE (May 2026 to October 2026)**

- **Dispatcher seats:** 21 of 30 used in October 2026 (70%). Average 23.3 of 30 (78%). May 26, October 21. Unused in October: 9, \$810 a month, \$9,720 a year at the current unit price.
- **Driver app licences:** 62 of 60 used in October 2026 (103%). Average 59.2 of 60 (99%). May 57, October 62. Used more than paid for: September 2026 (61 of 60); October 2026 (62 of 60).
- **Teams that use it:** dispatch (day and night shifts), drivers, the customer service desk.

**COST**

- **Annual price:** \$43,200 (dispatcher seats 30 x \$90 a month + driver app licences 60 x \$15 a month, x 12).
- **Invoiced February to October 2026, 9 invoices:** base \$32,400, extras \$960, credits −\$180, net \$33,180. Base check: \$43,200 / 12 x 9 months = \$32,400; matches base invoiced.
- **Extras:** 30 April 2026, onboarding training day for night dispatch, \$900; 30 September 2026, additional driver licences (1), \$20; 31 October 2026, additional driver licences (2), \$40.
- **Renewal quote, received 2 November 2026:** dispatcher seat \$99 a month (+10.0%); driver app licence \$16.50 a month (+10.0%); extra driver licences \$22 a month (+10.0%). As quoted: \$47,520 a year, +\$4,320 (+10.0%) on the current price. At October's use (21 dispatcher seats, 62 driver app licences, every unit at the quoted standard unit price): \$37,224 a year.

**PERFORMANCE (12 March 2026 to 27 October 2026)**

- **Availability, at least 99.5% of each month:** 2 logged, 0 met, 2 missed (3 June, 8 September). Missed in August to October: 1; earlier: 1.
- **Priority-1 response, first response within 1 hour:** 5 logged, 3 met, 2 missed (3 June, 14 October). Missed in August to October: 1; earlier: 1.
- **Credits recorded as due and not received:** 8 September 2026, \$180. Credits received: \$180 in the log, \$180 in the invoices; match.
- **From the teams:** Dispatch supervisor: "Since July the night shift plans routes on a spreadsheet; they found the planning board slow at night." Driver team lead: "Drivers rely on the app for every drop." Customer service lead: "We look up delivery status in it several times an hour."

**DEPENDENCE**

If it stopped: stops the work: dispatch goes to paper and the driver app shows nothing. Written fallback: no; on 3 June the morning was run on paper from memory. Company data it holds: customer delivery addresses, driver names and mobile numbers, delivery history. Costs of leaving: not known.

**QUESTIONS FOR THE SUPPLIER: 5, for the operations lead to decide whether to ask**

1. 21 of 30 dispatcher seats were used in October, down from 26 in May. Can the renewal be set at a different number of seats, and at what unit price?
2. 61 and 62 driver app licences were used against 60 paid for in September and October. Can the renewal cover the drivers actually using the app at the standard licence price?
3. The quote raises all three unit prices by 10.0%. What is the increase based on?
4. A \$180 credit is recorded as due for the 8 September outage and has not appeared on an invoice. When will it be applied?
5. Availability was missed on 3 June and 8 September, and a priority-1 response was missed on 3 June and 14 October. What has Supplier D changed since?

**DECISIONS FOR THE MANAGING DIRECTOR: 3**

1. Renew as quoted, renew with changes, or give notice: decide by Wednesday 18 November 2026; the notice date is Wednesday 2 December 2026. Should questions 1 to 5 go to Supplier D before deciding, and who asks them?
2. A \$180 credit is recorded as due for the 8 September outage and has not been received. Should it be claimed, and who claims it?
3. If Supplier D stopped, dispatch would go to paper, and there is no written fallback. Should one be written before the renewal, and by whom?

**NOT SUPPLIED OR NOT CHECKED**

The agreement was not read; the dates are as supplied by the finance director. Whether each logged event met its commitment is as recorded in the log.

Every figure traces to the inputs supplied for Supplier D on 9 November 2026. Nothing has been sent, accepted, cancelled, claimed or changed.
