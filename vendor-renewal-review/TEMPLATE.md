# Vendor renewal review

Workflow template, version 0.1.0.

## Purpose

Prepare one page for one supplier's renewal, for the person who has to decide it: the dates that matter, counted only from the dates the person supplies; how much of what the business pays for is used; what has been invoiced and what the renewal quote would cost; how the supplier has done against the commitments the person lists; how much the business depends on it; the questions worth putting to the supplier; and the decisions, each with its deadline. The assistant reads no agreement and interprets none. It prepares; it never gives notice, accepts a quote, cancels, claims a credit, contacts the supplier or changes a record.

## When to use it and when not to

Use it when a renewal is coming: when the supplier's renewal quote arrives, when the renewal appears on the calendar, or a few weeks before the notice date. It suits software subscriptions and service agreements that charge for a countable measure, such as seats, licences, site visits, hours or deliveries.

Do not use it:

- to find the dates in an agreement or to say what a clause means, whether the business may end early or what a notice has to contain. The person supplies the dates as they read them or as whoever reviews contracts confirms them, and questions of meaning go to that person;
- to choose between quotes from competing suppliers. That is a separate piece of work;
- to write renewal terms, a notice letter or a message to the supplier;
- for a security or data-protection assessment of the supplier. The page records what company data the supplier holds, as the person states it, and nothing more;
- for several suppliers at once. One supplier per run.

## Roles

- **Runs it:** the operations lead, procurement lead or office manager who looks after the supplier.
- **Supplies and confirms the dates:** whoever holds the signed order form or agreement, such as the finance director or the contract owner.
- **Supplies use, invoices and the service log:** the runner, from the supplier's admin screen, the accounting system and the team's own records.
- **Decides:** [your decision-maker], such as the owner, managing director or finance director.
- **Gives notice, accepts or signs, claims a credit, talks to the supplier:** the people the business names. Always people.

## Inputs

1. **Renewal facts,** typed by the runner: the supplier and what it supplies; today's date; the term end date; what happens at the end, as supplied (renews automatically unless notice is given, ends unless renewed, or not stated); the notice, either as a date or as a number of calendar days before the term end; who supplied the dates and from what; the teams that use it; the current annual price; the unit price and quantity for each measure, as a monthly price, and the price of any extra units; the renewal quote, if one has arrived, with the date received, the quoted unit prices and any quoted quantities; the currency; [your decision-maker]; and [your decision lead]. If the supplier or the term end date is missing, stop and ask. If the notice is given in months, in working days or as a condition ("by the end of the quarter before"), ask for it as a calendar date or a number of calendar days. If no notice is given at all, carry on and see step 2.
2. **Use export,** one row per measure per month, with these default headers: `period` (as YYYY-MM), `measure`, `paid_for`, `used`. If it is missing, write "use not supplied" under Use.
3. **Invoices export,** one row per invoice line, with these default headers: `invoice_date`, `invoice_number`, `description`, `type`, `amount`. `type` is `base` (the agreed subscription or service charge), `extra` (anything charged on top) or `credit` (a credit from the supplier, as a negative amount). If it is missing, write "invoices not supplied" under Cost and still show the price and the quote.
4. **Service log and commitments.** The commitments as the runner reads them in the supplier's service description, one line each. Then the log, one row per event that a commitment applies to, with these default headers: `date`, `what_happened`, `commitment`, `met` (yes or no), `credit_due`, `credit_received` (amounts, blank when none). If the log is missing, write "service log not supplied" under Performance.
5. **Team notes** (optional): short remarks from the people who use the service, each with the speaker's role.
6. **Dependence notes,** typed by the runner: what happens to the work if the service stopped, as one of "stops the work", "slows the work" or "little effect", with a line on what that looks like; whether a written fallback exists; what company data the supplier holds; known costs of leaving. Any item missing is written "not supplied"; an item the runner gives as "not known" was supplied, and is reported in their words.

Headers are matched ignoring case. If a required header is not there, stop and ask which column holds that information; never guess, and never use another column in its place. Months are the default period and unit prices are monthly; if the use export or the prices use another period, stop and ask.

The assistant works from files and notes the person supplies. It needs no connection to the supplier's system or the accounting system, and it never asks for a password or a login code.

## The procedure

1. **Check the inputs.** One supplier and one currency across every input. Every `type` is base, extra or credit; every `met` is yes or no; every date reads as a date. If anything fails, stop and ask about the row that fails.
2. **Count the dates.** If a notice date is given, use it. If a number of days is given, the notice date is the term end minus that many calendar days; show the arithmetic and mark it "computed from the period supplied". If the facts say the service ends unless renewed, write "not needed by the facts supplied" for the notice date and count from the term end instead. The decide-by date is the notice date (or the term end) minus [your decision lead] (default: 14 calendar days). Count calendar days from today to each date and write every date with its weekday. Status: NOTICE DATE PASSED, with the number of days, when today is after the notice date; DECIDE NOW when today is on or after the decide-by date; ON TRACK otherwise; NOTICE DATE NOT SUPPLIED when there is no notice and the facts do not say the service ends unless renewed. If the notice date falls after the term end, stop and ask.
3. **Use.** For each measure: in the latest month, used of paid for and the share used as a whole percent; the average used across all months to one decimal place, with its share; the first month's figure and the latest. Where the latest month has unused units, give their number and their cost at the current unit price, a month and a year (twelve months). Where use is above paid for in any month, name each month with its year and both figures, and mark "used more than paid for". Never say whether a charge applies. Then list the teams that use it.
4. **Cost.** Show the annual price with its make-up (quantity times monthly unit price, times twelve, for each measure). If the make-up does not equal the annual price, show the difference. From the invoices: the months covered, counted as the distinct calendar months in which a base line was invoiced (not the months since the term start), the number of distinct invoices, and the totals of base, extras and credits, and the net. Base check: the annual price divided by twelve, times the months covered, against the base invoiced; write "matches" or the difference. List every extra with its date, description and amount. From the quote: each quoted unit price with its change from the current one as a percent to one decimal place; the annual cost as quoted (the quoted quantities, or the current ones when the quote gives none), with the change from the current annual price in money and percent; and the annual cost with each quantity set to the latest month's use, every unit at the quoted standard unit price, even where the quote gives a separate price for extra units; say so on the page. If no quote is supplied, write "renewal quote not supplied".
5. **Performance.** For each commitment on the list: how many log rows, how many met, how many missed with their dates, and how many of the misses fall in the three calendar months before today's month against how many fall earlier. Whether a row was met comes from the log; never judge it from the description. A row naming a commitment that is not on the list: stop and ask which commitment it belongs to. Credits: every row whose `credit_received` is blank or smaller than its `credit_due`, with the date and the amount still outstanding. Compare the credits received in the log with the credits in the invoices and write "match" or the difference. Then quote each team note briefly, with the speaker's role.
6. **Dependence.** Report the dependence notes as supplied.
7. **Questions for the supplier.** Write a question only where a fact calls for it, each with the fact behind it: one for each measure with unused units in the latest month (can the renewal be set at a different quantity, and at what price); one for each measure used above paid for (can the renewal cover actual use at the standard unit price); one when the quote changes a price (what the change is based on); one for each credit recorded as due and not received (when it will be applied); and one covering every commitment missed in the log, with the dates (what the supplier has changed since). Plain questions only: no claims about what the agreement says and no threats. The runner decides whether to ask them and who asks; the assistant contacts no one.
8. **Decisions for [your decision-maker].** Always first: renew as quoted, renew with changes or give notice, by the decide-by date, with the notice date, and whether to put the questions to the supplier first. When the status is NOTICE DATE PASSED, write instead that by the dates supplied the notice date passed that many days ago, and that what options remain is a question for whoever reviews contracts. When the status is NOTICE DATE NOT SUPPLIED, the first decision is who confirms the notice date, and by when. Then one decision for each credit recorded as due and not received (whether to claim it, and who does). Then, when the dependence is "stops the work" and there is no written fallback, one decision on whether to have a fallback written before the renewal, and by whom. Write each as a question with its facts. Recommend nothing unless [your decision-maker] asks; if asked, add one suggestion, labelled as made at their request, with the facts for it and the facts against it.
9. **Not supplied or not checked.** Always first: the agreement was not read, and the dates are as supplied by the role named. Then each input that was missing, and the line that whether each log row met its commitment is as recorded in the log.
10. **Return the page** to the runner, in the output format and its fixed order, adding no section or commentary beyond it. "One page" in this template means that single document, not a printed sheet. Nothing goes to the supplier or to the decision-maker from the assistant.

## Exceptions and stop conditions

- **No supplier or no term end date:** stop and ask.
- **Notice given in months, working days or as a condition:** ask for a calendar date or a number of calendar days. Do not convert it.
- **Notice date after the term end:** stop and ask.
- **A required header does not match, or a `type` or `met` value is not one of the allowed values:** stop and ask; never guess.
- **More than one currency or more than one supplier in the inputs:** stop and ask which to use.
- **The person pastes the agreement and asks for the dates or for what a clause means:** decline. Ask for the dates as they read them or as whoever reviews contracts confirms them, and send questions of meaning to that person.
- **Asked to give notice, write the notice, accept the quote, cancel, claim a credit, email the supplier or change a record:** decline and name the role that does it.
- **Asked to score the supplier or to say whether to renew:** recommend nothing unless the decision-maker asks; then follow step 8.
- **An export carries the names or email addresses of individual users:** count them; do not repeat them on the page.
- **The inputs contain a password, a login code or bank details:** do not repeat them; tell the person to remove them from the source.

## Output format

```
VENDOR RENEWAL REVIEW: [supplier], [what it supplies]

For: [runner role]. Decision by: [decision-maker role]. Prepared [weekday date] from [the inputs used, with row counts].

DATES
Term ends: [weekday date], [n] days from today. At the end: [renews automatically unless notice is given / ends unless renewed / not stated], as supplied by [role], from [source].
Notice date: [weekday date], [n] days from today [(computed: term end minus [n] days, from the period supplied)] / not needed by the facts supplied / not supplied.
Decide by: [weekday date], [n] days from today ([n] days before the [notice date / term end]).
Status: [ON TRACK / DECIDE NOW / NOTICE DATE PASSED, [n] days ago / NOTICE DATE NOT SUPPLIED].

USE ([first month] to [latest month])
[Measure]: [used] of [paid for] used in [latest month] ([n]%). Average [n.n] of [paid for] ([n]%). [First month] [n], [latest month] [n]. [Unused in [latest month]: [n], [amount] a month, [amount] a year at the current unit price.] [Used more than paid for: [month year] ([used] of [paid for]); ...]
Teams that use it: [as supplied / not supplied].
/ Use not supplied.

COST
Annual price: [amount] ([measure] [quantity] x [unit price] a month + ..., x 12)[; the make-up differs by [amount]].
Invoiced [first month] to [last month], [n] invoices: base [amount], extras [amount], credits [amount], net [amount]. Base check: [annual price] / 12 x [n] months = [amount]; [matches base invoiced / differs by [amount]].
Extras: [date, description, amount]; ... / none.
Renewal quote, received [date]: [measure] [unit price] a month ([+/-n.n]%); ... As quoted: [amount] a year, [+/-amount] ([+/-n.n]%) on the current price. At [latest month]'s use ([quantities], every unit at the quoted standard unit price): [amount] a year. / Renewal quote not supplied.
[Invoices not supplied.]

PERFORMANCE ([first log date] to [last log date])
[Commitment, as supplied]: [n] logged, [n] met, [n] missed ([dates]). Missed in [the three months]: [n]; earlier: [n].
Credits recorded as due and not received: [date, amount]; ... / none. Credits received: [amount] in the log, [amount] in the invoices; [match / differ by [amount]].
From the teams: [role]: "[short quote]" ... / No team notes supplied.
/ Service log not supplied.

DEPENDENCE
If it stopped: [stops the work / slows the work / little effect / not supplied]: [what that looks like]. Written fallback: [yes / no / not supplied][; the note supplied with it]. Company data it holds: [as supplied / not supplied]. Costs of leaving: [as supplied / not supplied].

QUESTIONS FOR THE SUPPLIER: [n], for the [runner role] to decide whether to ask
[n]. [The fact.] [The question.]
/ None.

DECISIONS FOR THE [DECISION-MAKER ROLE]: [n]
1. [The renewal decision, its decide-by date and the notice date / the notice date passed / who confirms the notice date.]
[n]. [The facts.] [The question.]
[Suggestion, made at the [decision-maker role]'s request: [one option], because [facts]. Against it: [facts].]

NOT SUPPLIED OR NOT CHECKED
The agreement was not read; the dates are as supplied by [role]. [Each input that was missing.] Whether each logged event met its commitment is as recorded in the log.

Every figure traces to the inputs supplied for [supplier] on [date]. Nothing has been sent, accepted, cancelled, claimed or changed.
```

## Reviewer checklist

1. Every date has the right weekday, and every day count is correct from today's date. (Runner)
2. The notice date matches what the person who supplied the dates holds, and the page says it was not read from the agreement. (Finance director or contract owner)
3. Every use figure, percent and unused cost recomputes from the use export and the unit prices. (Runner)
4. The invoice totals, the base check and the quote arithmetic recompute from the invoices export and the quote. (Finance)
5. Every miss and every outstanding credit appears in the service log as stated. (Runner)
6. Every question for the supplier rests on a fact on the page and makes no claim about the agreement. (Runner)
7. The first decision carries the decide-by date and the notice date, and nothing is recommended unless the decision-maker asked. (Decision-maker)
8. The page keeps the fixed section order and adds nothing beyond the output format. (Runner)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary renewal.** Term end 31 January 2027, notice 60 days, today 9 November 2026, decision lead 14 days. Expected: notice date Wednesday 2 December 2026 (23 days), marked computed; decide by Wednesday 18 November (9 days); status ON TRACK.
2. **Notice date passed.** The same dates, today 4 December 2026. Expected: NOTICE DATE PASSED, 2 days ago; the first decision says what options remain is a question for whoever reviews contracts; no option is offered.
3. **Notice in months.** "Three months before the end." Expected: asks for a calendar date or a number of days; does not convert.
4. **Agreement pasted.** The person pastes the renewal clause and asks when notice is due. Expected: declines to read it for dates; asks for the dates as they read them or as whoever reviews contracts confirms.
5. **Header does not match.** The use export's columns are `month`, `item`, `licensed`, `active`. Expected: stops and asks which column holds which; drafts nothing.
6. **Unused seats.** 30 paid for, 21 used in the latest month, $90 a month each. Expected: unused 9, $810 a month, $9,720 a year; one question about the renewal quantity.
7. **Use above paid for.** 62 used against 60 paid for. Expected: "used more than paid for" with the month and both figures; nothing said about whether a charge applies.
8. **Credit not received.** A log row with $180 due and nothing received. Expected: listed under Performance, one question for the supplier and one decision on whether to claim it; nothing claimed.
9. **No fallback for a critical service.** Dependence "stops the work", no written fallback. Expected: a decision on whether to have one written before the renewal.
10. **Asked to send the notice.** "Email them our notice today." Expected: declines; names the role that gives notice; nothing drafted to the supplier.
11. **Asked whether to renew.** The decision-maker asks for a recommendation. Expected: one suggestion, labelled as made at their request, with the facts for and against.
12. **No quote yet.** Expected: "renewal quote not supplied" under Cost; no price change question.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a one-page renewal review of one supplier for the person
who looks after it. You prepare; people decide. You never give notice,
accept a quote, cancel, claim a credit, contact the supplier, send
anything or change any record. You never read an agreement for dates
or say what a clause means. You never ask for a password or a login
code and need no access to any system.

The user will supply: the renewal facts (supplier, what it supplies,
today's date, term end, what happens at the end, the notice as a date
or as calendar days before the term end, who supplied the dates, the
teams that use it, annual price, monthly unit prices and quantities,
the renewal quote, currency, the decision-maker, the decision lead);
a use export (period, measure, paid_for, used); an invoices export
(invoice_date, invoice_number, description, type, amount); the
commitments and a service log (date, what_happened, commitment, met,
credit_due, credit_received); team notes; dependence notes.

Stop and ask when: the supplier or term end is missing; the notice is
in months, working days or a condition (ask for a calendar date or a
number of days; never convert it); the notice date falls after the
term end; a header does not match (match ignoring case; ask which
column holds it; never guess); a type is not base, extra or credit, or
met is not yes or no; a log row names a commitment not on the list;
there is more than one currency or supplier; periods are not months.
If another input is missing, say so in the section it feeds and in
NOT SUPPLIED OR NOT CHECKED, and continue.

1. Dates: notice date as given, or term end minus the days given
   (show it, marked "computed from the period supplied"). If the
   service ends unless renewed, the notice is "not needed by the facts
   supplied" and you count from the term end. Decide-by is that date
   minus the decision lead (default 14 days). Count calendar days from
   today; write every date with its weekday. Status: NOTICE DATE
   PASSED (n days ago), DECIDE NOW (on or after decide-by), ON TRACK,
   or NOTICE DATE NOT SUPPLIED.
2. Use, per measure: latest month used of paid for and whole percent;
   average used to one decimal and its percent; first and latest
   month. Unused units in the latest month and their cost a month and
   a year at the current unit price. Months with use above paid for,
   each with its year, marked "used more than paid for". Never say
   whether a charge applies.
3. Cost: annual price and its make-up (quantity x monthly price x 12;
   show any difference). Invoices: months covered, distinct invoices,
   base, extras, credits, net; base check (annual price / 12 x the
   distinct months with a base line invoiced, not months since the
   term start, against base invoiced); every extra listed. Quote: each
   unit price change in percent to one decimal; annual cost as quoted
   and its change in money and percent; annual cost at the latest
   month's use, every unit at the quoted standard unit price (say so
   on the page). Or "renewal quote not supplied".
4. Performance, per commitment: logged, met, missed with dates; misses
   in the three calendar months before today's month against earlier.
   Take met from the log only. Credits due and not received, with
   amounts; credits received in the log against the invoices. Quote
   team notes briefly with the role.
5. Dependence as supplied; a stated "not known" stays in the user's
   words, and only a missing item is "not supplied".
6. Questions for the supplier, each with its fact, only for: unused
   units; use above paid for; a price change in the quote; each credit
   due and not received; one covering every missed commitment with
   dates. No claims about the agreement, no threats. Write "None." if
   there are none.
7. Decisions for the decision-maker: first the renewal choice (renew
   as quoted, renew with changes, give notice) by the decide-by date,
   with the notice date and whether to ask the questions first; or, if
   the notice date passed, say that what options remain is a question
   for whoever reviews contracts; or, if no notice was supplied, who
   confirms it and by when. Then one per credit not received (whether
   to claim, and who). Then, if dependence is "stops the work" with no
   written fallback, whether to have one written first. Recommend
   nothing unless the decision-maker asks; then give one suggestion
   labelled as made at their request, with facts for and against.
8. NOT SUPPLIED OR NOT CHECKED always opens with "The agreement was
   not read; the dates are as supplied by [role]."
9. Use the output format exactly, as one document in its fixed
   order, and end with: "Every figure traces to the inputs supplied
   for [supplier] on [date]. Nothing has been sent, accepted,
   cancelled, claimed or changed."

If asked to give or write notice, accept the quote, cancel, claim a
credit or email the supplier, decline and name the role that does it.
If an export names individual users, count them and do not repeat the
names. If the inputs contain a password, a login code or bank details,
do not repeat them and tell the user to remove them. Recompute every
figure before you return the page.
```

## What to customize

- [your decision-maker], and who confirms the dates for each supplier.
- [your decision lead]: how many days before the notice date the decision should be made. The default is 14 calendar days.
- Your measures and their names, as they appear in each supplier's admin screen or report.
- The column headers your exports actually use, so the template reads them as they come.
- Which suppliers get a review, and how far ahead of the notice date the runner starts.
- Whether a fallback decision should also be raised when the dependence is "slows the work".
- Where the approved page is kept, and who puts the questions to the supplier.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 9 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried once on its invented example in Claude on 9 November 2026; the trial record is published with it. Small edits made to the procedure, the pasted instructions, the output format and the example after an independent review have not been run again; the trial record lists them. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
