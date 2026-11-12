# Supplier issue notice

When a supplier bills for more than was ordered or received, or falls short of an agreed delivery or quality target, the buyer gets a formal notice ready for approval: each problem set against the record, the evidence listed, what the supplier must do and the date to reply by. A person approves and sends it.

*Workflow template · Procurement and suppliers · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/supplier-issue-notice/)*

## The outcome

A supplier problem is raised once, properly, in writing. In place of a quick email saying an invoice looks wrong, the supplier receives a notice that names each item, sets what was billed beside what was ordered and what arrived, gives the amount in question, and says exactly what would settle it and by which date. A delivery or quality problem gets the same treatment: the supplier's result for the period, worked out from your own delivery records, beside the target the supplier agreed to, and a request for a written plan to put it right.

Every figure is worked out again from your documents before a word is written, so the notice holds up when the supplier's accounts team checks it. The part of the invoice nobody disputes is stated plainly, so the supplier knows what will be paid and the relationship keeps working while the rest is sorted out.

The tone is calm and factual: no blame, no threats, no claims about what the contract means. The notice comes with a short cover sheet for the person who approves it, listing the checks made, anything deliberately left out, and anything that must stop before sending, such as an invoice asking for payment to a new bank account. The workflow template drafts; a person approves the notice and a person sends it.

## Who starts the work, and when

The buyer, the purchasing lead or the accounts-payable lead starts it when an invoice has been held for a difference against its order or its delivery, often straight from the exceptions that [supplier bill review and payment-run preparation](https://fullypowered.ai/workflows/supplier-bill-review-and-payment-run-preparation/) finds. It is also started at the end of a month or quarter when a supplier's on-time delivery or rejection rate has fallen below the target it agreed.

Whoever your rules name approves the notice before it goes: often the purchasing manager for an invoice dispute, and the head of purchasing or operations for a corrective-action request.

## What they supply

- **A short brief:** which kind of notice, the supplier and the contact there, who sends it, who approves it and the planned send date.
- **For an invoice dispute:** the invoice, the purchase order and the record of goods received, plus any earlier invoices against the same order.
- **For a corrective-action request:** the agreed target and where it is written down, the delivery records for the whole period, and any earlier notice about the same problem.
- **Your settings:** working days and closed dates, how long the supplier has to reply, any price tolerance, how an undisputed amount is paid, and who approves which notice.
- **Notes,** if any, with dates: what the warehouse confirmed, what a delivery note said, how a shortfall affected you.

No connection to your accounting or purchasing system is needed, and none is asked for.

## What comes out

Two parts, in a fixed order.

1. **For the approver,** never sent: who approves under your rules, the reply date counted in your working days, each check and its result, the issues raised, anything not raised and why, anything that must stop before sending, the decisions waiting, and the documents to attach.
2. **The notice itself,** ready to send once approved: the subject and reference, a plain opening, one block per issue with what was invoiced, your record, the difference and what would settle it, or the measured result against the target. Then what the supplier is asked to do and by when, what happens to the undisputed amount, the evidence attached, and the sign-off.

A follow-up line closes the draft: who chases if no reply arrives by the date.

Good looks like this: the supplier can check every figure against the documents attached, and the approver can see in a minute what was checked and what was left out.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/), which owns the order, the agreed price and the supplier relationship.
- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), where the accounts-payable lead holds an invoice until its differences are settled.
- [Supply chain and inventory](https://fullypowered.ai/functions/supply-chain-and-inventory/), where late or rejected deliveries hold up the work that depends on them.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where parts and materials are billed by the line and short deliveries are routine.
- [Construction](https://fullypowered.ai/industries/construction/), where materials arrive in part loads at a site and the invoice arrives whole.
- [Hospitality](https://fullypowered.ai/industries/hospitality/), where food, linen and supplies arrive several times a week and a supplier's reliability shows quickly.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where stock arrives in part shipments and a late delivery means empty shelves.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where supplier problems have been handled by phone and nobody can find what was agreed.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), where more suppliers and more orders mean problems need a standard written record.

## What has to change for your company

- **Your approval rules.** Who approves an invoice dispute, by amount, and who approves a corrective-action request.
- **Your reply periods.** The working days a supplier has to answer each kind of notice; five for a dispute and ten for a corrective-action plan are the defaults.
- **Your price tolerance.** Whether small price differences are raised at all, and where the line sits.
- **The undisputed amount.** Whether it is paid when due while the rest is settled, or held.
- **Your house style.** The sign-off, the contact details and any standard closing line.
- **Your contract reviewer.** Who answers questions about contract terms, notices that end or change a supply relationship, and any claim for compensation. This workflow template leaves all of those to them.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini. Decide which documents and exports the assistant may read.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026; the record is published with it, and lists the small edits made afterward that have not been run again. Only the invoice-dispute path was exercised: the corrective-action path, the stop conditions and the refusals were not tried. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past supplier problems your team remembers, with hard cases written in advance: a line both priced above the order and short-delivered, a charge that is not on the order, an export whose headers do not match, a supplier whose result in fact met its target, an invoice asking for payment to new bank details. The person who approves checks every figure against the documents before anything is sent. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
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
- [Vendor quote comparison](../vendor-quote-comparison/)
- [Vendor renewal review](../vendor-renewal-review/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
