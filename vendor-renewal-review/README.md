# Vendor renewal review

Before a supplier's notice date, the operations lead takes one page to the decision: the dates counted from the ones you supply, how much of what you pay for is used, what it has cost and what renewal would cost, how the supplier has performed, and the questions to ask. Nothing is sent or cancelled.

*Workflow template · Procurement and suppliers · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/vendor-renewal-review/)*

## The outcome

A renewal becomes a choice someone makes on purpose, in time, instead of something that happens because nobody looked. The decision-maker sees the notice date and the date to decide by at the top of the page, with the days left to each.

Below the dates sit the facts that shape the choice: seats or licences paid for and not used, and what they cost; charges on top of the subscription; the renewal quote against today's price; the commitments the supplier missed and any credit still owed; and how badly the business would be hit if the supplier stopped. Each fact that deserves an answer from the supplier is already written as a question.

The page prepares the decision and stops there. A person decides, a person talks to the supplier, and a person gives notice if notice is given.

## Who starts the work, and when

The operations lead, procurement lead or office manager who looks after the supplier starts it when the renewal quote arrives, when the renewal shows up on the calendar, or a few weeks before the notice date. Whoever holds the signed order form confirms the dates. The owner, managing director or finance director makes the decision.

## What they supply

- **The renewal facts:** the term end, what happens at the end, the notice period or date as they read it, the current price and the renewal quote.
- **A use export** from the supplier's admin screen: for each month, how many of each item were paid for and how many were used.
- **An invoices export** from the accounting system, with each line marked as the agreed charge, an extra or a credit.
- **The supplier's commitments** as they read them, and their own log of incidents and tickets, with any credits due.
- **A few lines from the teams** who use the service, if they have them.
- **A short note on dependence:** what happens if the supplier stopped, whether a written fallback exists, what company data the supplier holds.

No connection to the supplier's system or the accounting system is needed, and none is asked for.

## What comes out

One page, in a fixed order:

1. **Dates:** the term end, the notice date, the date to decide by and a status.
2. **Use:** what is used against what is paid for, the trend, and the cost of what sits idle.
3. **Cost:** the price and its make-up, what has been invoiced, every extra, and the renewal quote both as quoted and at current use.
4. **Performance:** each commitment met or missed, recent misses against older ones, credits still owed, and what the teams say.
5. **Dependence:** how much the business leans on the supplier.
6. **Questions for the supplier,** each tied to a fact.
7. **Decisions,** the first always being the renewal itself with its deadline.
8. **What was not supplied or checked,** starting with the plain statement that the agreement itself was not read.

A good page can be checked against the exports with a calculator, and the decision-maker can make the call without opening another file.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/), which owns supplier relationships and the renewal calendar.
- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where the teams who depend on a supplier feel every outage first.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where software subscriptions multiply team by team and renew quietly.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where maintenance, software and service agreements keep the line running and renew on fixed dates.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/), where dispatch, tracking and fleet systems are paid by the seat or the vehicle.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where a dozen renewals a year live in one person's memory and should live on a page.

## What has to change for your company

Name the decision-maker and who confirms the dates for each supplier. Choose how many days before the notice date the decision should be made. Map the column headers of your own exports, since every supplier's admin screen names things differently. Decide which suppliers are worth a review and how early the runner starts. Agree who puts questions to the supplier and where the finished page is kept. It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried once on its invented example in Claude on 9 November 2026, and the record of that run is published with it; the record lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past renewals your team remembers, with hard cases written in advance: a notice date already passed, a notice period given in months, exports whose headers do not match, a credit never received, a supplier with no fallback. The runner checks every date and figure against the inputs before anyone relies on the page. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 9 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 9 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Supplier bill review and payment-run preparation](https://fullypowered.ai/workflows/supplier-bill-review-and-payment-run-preparation/)
- [Budget-versus-actual variance commentary](https://fullypowered.ai/workflows/budget-versus-actual-variance-commentary/)
- [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
