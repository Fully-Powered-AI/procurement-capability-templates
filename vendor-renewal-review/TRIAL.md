# Vendor renewal review: a trial on its invented example

- **Product:** Claude, run in Claude Code

Model: Claude Sonnet 5.5 (model ID claude-sonnet-5-5). Date: 2026-11-09.

The inputs are the invented example in `public/example.md` (Supplier D, an invented dispatch software supplier). No client data was used. The person trying the template did not write it, and read only the example's inputs before producing the page below; the example's own output was read afterwards, for comparison.

## Inputs used

The six inputs in `public/example.md` under "The inputs": the renewal facts, the use export (12 rows), the invoices export (13 rows), the two commitments and the service log (7 rows), the three team notes and the dependence notes. Nothing was added or changed.

## What came out

**VENDOR RENEWAL REVIEW: Supplier D, dispatch and route-planning software, with a driver app**

For: Operations lead. Decision by: Managing director. Prepared Monday 9 November 2026 from the renewal facts, the use export (12 rows), the invoices export (13 rows), 2 commitments and the service log (7 rows), 3 team notes and the dependence notes.

**DATES**

- Term ends: Sunday 31 January 2027, 83 days from today. At the end: renews automatically for 12 months unless notice is given, as supplied by the finance director, from the signed order form.
- Notice date: Wednesday 2 December 2026, 23 days from today (computed: term end minus 60 days, from the period supplied).
- Decide by: Wednesday 18 November 2026, 9 days from today (14 days before the notice date).
- Status: ON TRACK.

**USE (May 2026 to October 2026)**

- Dispatcher seats: 21 of 30 used in October 2026 (70%). Average 23.3 of 30 (78%). May 26, October 21. Unused in October: 9, $810 a month, $9,720 a year at the current unit price.
- Driver app licences: 62 of 60 used in October 2026 (103%). Average 59.2 of 60 (99%). May 57, October 62. Used more than paid for: September 2026 (61 of 60); October 2026 (62 of 60).
- Teams that use it: dispatch (day and night shifts), drivers, the customer service desk.

**COST**

- Annual price: $43,200 (dispatcher seats 30 x $90 a month + driver app licences 60 x $15 a month, x 12).
- Invoiced February to October 2026, 9 invoices: base $32,400, extras $960, credits -$180, net $33,180. Base check: $43,200 / 12 x 9 months = $32,400; matches base invoiced.
- Extras: 30 April 2026, onboarding training day for night dispatch, $900; 30 September 2026, additional driver licences (1), $20; 31 October 2026, additional driver licences (2), $40.
- Renewal quote, received 2 November 2026: dispatcher seat $99 a month (+10.0%); driver app licence $16.50 a month (+10.0%); extra driver licences $22 a month (+10.0%). As quoted (current quantities, as the quote gives none): $47,520 a year, +$4,320 (+10.0%) on the current price. At October's use (21 dispatcher seats, 62 driver app licences, all at the quoted standard unit prices): $37,224 a year.

**PERFORMANCE (12 March 2026 to 27 October 2026)**

- Availability: 2 logged, 0 met, 2 missed (3 June, 8 September 2026). Missed in August to October 2026: 1; earlier: 1.
- Priority-1 response: 5 logged, 3 met, 2 missed (3 June, 14 October 2026). Missed in August to October 2026: 1; earlier: 1.
- Credits recorded as due and not received: 8 September 2026, $180 outstanding. Credits received: $180 in the log, $180 in the invoices; match.
- From the teams: Dispatch supervisor: "Since July the night shift plans routes on a spreadsheet; they found the planning board slow at night." Driver team lead: "Drivers rely on the app for every drop." Customer service lead: "We look up delivery status in it several times an hour."

**DEPENDENCE**

If it stopped: stops the work: dispatch goes to paper and the driver app shows nothing. Written fallback: no; on 3 June the morning was run on paper from memory. Company data it holds: customer delivery addresses, driver names and mobile numbers, delivery history. Costs of leaving: not known (as supplied).

**QUESTIONS FOR THE SUPPLIER: 5, for the operations lead to decide whether to ask**

1. Dispatcher seats: 21 of 30 were used in October 2026, 9 unused. Can the renewal be set at a different number of seats, and at what unit price?
2. Driver app licences: 61 and 62 were used against 60 paid for in September and October 2026. Can the renewal cover actual use at the standard unit price?
3. The quote raises all three unit prices by 10.0%. What is the change based on?
4. A $180 credit is recorded as due for the 8 September 2026 outage and not received. When will it be applied?
5. Availability was missed on 3 June and 8 September 2026, and a priority-1 response on 3 June and 14 October 2026. What has Supplier D changed since?

**DECISIONS FOR THE MANAGING DIRECTOR: 3**

1. Renew as quoted, renew with changes or give notice: decide by Wednesday 18 November 2026; the notice date is Wednesday 2 December 2026. Should the five questions go to Supplier D first, and who asks them?
2. A $180 credit is recorded as due for the 8 September 2026 outage and has not been received. Should it be claimed, and who claims it?
3. If Supplier D stopped, the work would stop and there is no written fallback. Should one be written before the renewal, and by whom?

**NOT SUPPLIED OR NOT CHECKED**

The agreement was not read; the dates are as supplied by the finance director. No input was missing. Whether each logged event met its commitment is as recorded in the log.

Every figure traces to the inputs supplied for Supplier D on 9 November 2026. Nothing has been sent, accepted, cancelled, claimed or changed.

## What was observed

- Every part of the output format was produced, in the fixed order. No input was missing, so no "not supplied" lines were needed. Nothing in the inputs triggered a stop: the notice was given in calendar days, every header matched, every `type` and `met` value was allowed, and there was one supplier and one currency.
- I recomputed every date, count, percent and total from the inputs before writing them. They agree with the published example's.
- Differences from the published example are in wording only; all figures, dates, counts, questions and decisions are the same. The example's output shortens two team notes slightly differently, leaves out "No input was missing", and words the dependence line a little differently. My question 2 does not say the extras were billed at $20 each; the example's does.
- Facts not in the inputs: none in my output. In the example, "the extras were billed at $20 each" is worked out from the invoice lines ($20 for one licence, $40 for two) rather than stated, and it links the extras to the months of heavier use, which sits close to the template's rule never to say whether a charge applies. "Has not appeared on an invoice" in its question 4 is true of the export supplied, which ends in October.
- Where the instructions left me to guess:
  - The quote's annual cost "at the latest month's use": October's driver use was 62 against 60 paid for, and the quote has a separate price for extra licences. The template does not say whether the two extra licences are priced at the standard $16.50 or the extra $22. I used the standard price for all 62 ($37,224); the other reading gives $37,356. Question 2 in the template points to the standard price, so I followed that. The page should say which it used, and I added a note.
  - "Not supplied" against "not known": the dependence notes say costs of leaving are "not known". The template says to write "not supplied" for a missing item. I kept the person's words and added "(as supplied)".
  - Whether to count one question for the quote or one for each changed price. I wrote one, as the template says "one when the quote changes a price".
  - "On one page" is not defined; the page is about 60 lines and long for a single printed sheet.
  - Whether to list every measure's months on a "used more than paid for" line with the year; I added the year.
  - Whether the base check's months covered counts invoice months (February to October, 9) or months since the term start; both give 9 here, so the example does not show the difference.
- The template's own notes say the acceptance tests are proposals that have not been run; this trial did not run them. It covers the ordinary path only: no stop condition, no passed notice date, no missing input.
- It was not tested as a packaged version in any product, and not in a client environment.

## Changed after this run, and not run again

Changed on 9 November 2026 after an independent review of the published template, and not run again. The output and the observations above are as recorded and describe the template and the example as they stood at the run:

- **The annual cost at the latest month's use.** The procedure, the pasted instructions and the output format now say every unit is priced at the quoted standard unit price, even where the quote gives a separate price for extra units, and that the page says so. This is the reading this run used ($37,224). The example's cost line now says so too.
- **"Not known" against "not supplied".** The template now says an item the runner gives as "not known" was supplied and is reported in their words; only a missing item is "not supplied". The example already kept "not known".
- **"One page".** The template now says "one page" means the single document in the output format and its fixed order, with nothing added, not a printed sheet; reviewer item 8 checks the order and that nothing is added.
- **Months on the "used more than paid for" line.** The procedure, the pasted instructions and the output format now say each month carries its year, as this run wrote it. The example now does too.
- **Months in the base check.** The procedure and the pasted instructions now count the distinct calendar months in which a base line was invoiced, not the months since the term start. Both give 9 on this example.
- **The example's question 2** no longer says the extras were billed at $20 each, as this run's question 2 did not.
- **Pasting.** The template now says to paste the output format beneath the instruction block.
