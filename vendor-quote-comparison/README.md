# Vendor quote comparison

Before anyone signs, the person choosing a vendor gets one sheet: the criteria agreed first, every quote costed the same way, and each vendor eliminated with its reason, on hold with the question that settles it, or shortlisted with its trade-offs. A person chooses; contract terms go to your reviewer.

*Workflow template · Procurement and suppliers · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/vendor-quote-comparison/)*

## The outcome

Choosing between quotes stops being a matter of whichever sales call went best. The criteria are written down and agreed before a single quote is compared, so nobody quietly moves the goalposts toward a favorite. Every quote is costed over the same months, with one-off charges, price rises and separately priced extras counted, so a low monthly fee cannot hide a higher bill.

Then the field narrows in plain steps. A vendor that misses a must-have is out, with its own words quoted. A vendor over the budget is out, with the amount. A vendor that costs more and is no better on anything that matters is out, with the vendor that beats it named. What is left is a short list and a clear trade-off: this one is cheaper and faster, that one services more often.

Nobody is eliminated for something their quote simply does not mention; they are put on hold with a question ready to send. Promises made on a call count for nothing until they are in writing. The person who owns the budget makes the choice, and whoever reviews your contracts reads the terms before anything is signed.

## Who starts the work, and when

The office manager, buyer or owner who gathered the quotes starts it once at least two are in, and runs it again whenever a vendor answers a question or sends a revised quote.

Before any of that, the owner or budget holder agrees the criteria: what would rule a vendor out, which qualities count among those that qualify, the most they will spend, and how long they want to commit for. If those are not written down yet, the workflow template asks those questions and stops there.

## What they supply

- **A short brief:** what is being bought and what prompted it, the start date wanted and the date the choice must be made.
- **The agreed criteria:** the must-haves, the measures that matter with which way is better, the budget ceiling, the number of months to cost over, and what every price must include.
- **The quotes,** as the vendors sent them.
- **Notes from calls and emails,** if there are any, so verbal promises can be set aside rather than counted.

No connection to email, a purchasing system or any vendor portal is needed, and none is asked for.

## What comes out

One comparison sheet, in a fixed order:

1. **The quotes and the criteria,** with the date the criteria were agreed and any quote that expires before the decision date.
2. **Cost over the term** for every vendor, with the arithmetic shown.
3. **Side by side:** what each quote says against each criterion, or "not stated".
4. **Not counted:** promises that appear only in call notes, and claims a vendor makes about itself with nothing behind them.
5. **Three rounds:** must-haves, then budget, then outperformed, each naming who went out and why.
6. **Where each vendor stands,** in one line each, and the shortlist with what each vendor is better and worse on.
7. **For the contract reviewer:** renewal, notice, price-change and similar terms, quoted word for word.
8. **Questions for vendors** drafted for a person to send, and the decisions for the person who chooses.

Good looks like this: anyone can point at a vendor and find, in one line, why it is still in or why it is out.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/), which owns choosing vendors and keeping the record of why.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where an office manager buys cleaning, IT support and equipment with no purchasing team.
- [Construction](https://fullypowered.ai/industries/construction/), where subcontractor and equipment-hire quotes arrive in different shapes and have to be read on one basis.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where a supplier of a regular material or a maintenance contract is chosen on price, lead time and service together.
- [Hospitality](https://fullypowered.ai/industries/hospitality/), where linen, waste, pest-control and food-supply contracts come up for choice every year.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where purchases have been chosen on habit and a written reason makes the next choice easier.

## What has to change for your company

- **Who chooses and who reads contracts.** Name the budget holder who agrees the criteria and makes the choice, and the person who reviews contract terms.
- **Your standing must-haves.** Insurance cover, start dates or service hours you always require can start each list, edited each time.
- **Your cost period.** Twelve months for a service contract is common; equipment may be costed over its expected life.
- **What every price must include,** for each kind of purchase you make often.
- **Your budget rule.** Whether a ceiling is always set, and who may raise it.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini. Decide which documents the assistant may read.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried once on its invented example in Claude on 9 November 2026, and the record of that run is published with the template; it lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past purchases your team remembers, with hard cases written in advance: a quote silent on a must-have, a price rise halfway through the year, an extra priced separately, a promise made only on a call. The person who chooses checks every figure against the quotes before anyone relies on the sheet. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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
