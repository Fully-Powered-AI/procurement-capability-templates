# Category sourcing plan

For the buyer or operations lead who owns one spend category, such as packaging or IT hardware: its spend and suppliers on one page, where it sits on a supply-risk and spend matrix, the value levers the evidence supports, and a dated sourcing plan. A person chooses the approach.

*Capability template · Procurement and suppliers · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/category-sourcing-plan/)*

## The outcome

A category that has been bought out of habit gets looked at as a whole. Twelve months of spend are laid out by supplier and by item, with every total checked back to the rows, so the conversation starts from what was actually paid. The same box bought at five different prices, a small supplier used for rush orders, a price rise nobody explained: they are on the page, not in someone's memory.

Then comes the judgment, done in the open. The category is placed on the familiar matrix of supply risk against spend impact, and every factor behind that position is shown with its figure and its limit, so anyone can check it. Each value lever is either backed by something in the inputs or marked as having no evidence. Only one figure is given, the gap between what was paid and the lowest price the company already paid for the same item, and it is labelled for what it is: indicative, not a target.

The page ends with two or three ways forward, always including "keep things as they are and fix the named problems", and, once a person has chosen one, a step-by-step plan with owners and dates. Notice dates that land before or during the plan are flagged where nobody can miss them. The decision maker chooses; agreements go to whoever reviews them.

## Who starts the work, and when

The buyer, purchasing lead or operations lead who owns the category starts it once a year for each category that matters, when a category has grown without anyone owning it, or before the main agreements in it come up for notice. A new buyer taking a category over can run it in the first week.

It is usually run twice: once to see the position and the options, and again after the decision maker has chosen an approach, so the plan is drafted for that approach.

## What they supply

- **A short brief:** the category and what is in it, the objectives in order, the constraints that cannot change, the company's total spend for the same twelve months, the date the plan is due and the date it would start, who approves the plan and who reads agreements, and the chosen approach once there is one.
- **A spend export:** twelve months of invoice or order lines, with the date, supplier, item, quantity, unit price and amount. If the columns are named differently, the capability asks which is which before it reads anything.
- **Supplier facts:** what each supplier provides and which items it is approved to supply, agreement end and notice dates from whoever holds the agreements, lead times, payment terms and any problems in the year.
- **Market notes,** if any: other suppliers that could quote and how long approving one takes.
- **Notes from the people who use the category,** if any: what they need and what worries them.

No connection to a purchasing system, email or any supplier's portal is needed, and none is asked for.

## What comes out

One plan, in a fixed order:

1. **The category** and its objectives.
2. **Spend** by supplier and by item, with the check that every total adds up.
3. **Suppliers,** with the items each is approved for, their dates exactly as supplied, and any notice or end date close at hand flagged.
4. **The position on the matrix,** factor by factor, and any item that sits apart, such as a printed item only one supplier can make.
5. **Value levers,** each supported by evidence or marked as having none, and the indicative price gap with its arithmetic.
6. **Approach options,** with the levers each uses, its main risk and who it affects.
7. **The sourcing plan:** steps, owners and dates, with every supplier date that falls before or during it.
8. **Concerns and risks,** each matched to the step that deals with it, or marked open.
9. **For the contract reviewer:** every agreement the plan would touch, with its dates.
10. **Gaps and questions,** and **the decisions** for the person who approves.

Good looks like this: the decision maker can see in two minutes where the category stands, what could be done about it, and the one date that cannot be missed.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/), which owns each category and the case for how it is bought.
- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where the operations lead often owns packaging, maintenance supplies or equipment without a purchasing team.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where packaging, raw materials and maintenance parts are bought from a handful of suppliers year after year.
- [Consumer brands](https://fullypowered.ai/industries/consumer-brands/), where shipping and display packaging carry both cost and the brand.
- [Ecommerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where boxes, mailers and fulfilment supplies grow with every order.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where IT hardware and office services are bought by an office or operations manager.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where categories have been bought on habit for years and nobody has looked at them whole.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), where spend in a category doubles before anyone owns it.

## What has to change for your company

- **Who approves and who reads agreements.** Name the decision maker who confirms the position and chooses the approach, and the person who reviews agreements before any notice or signature.
- **Your limits.** The share of company spend that makes a category matter, the supply-risk limits and the notice window all start from sensible defaults; set them to your own.
- **Your steps.** The plan uses six standard steps with set lengths. Change them to the way your company runs sourcing, and decide how holidays are handled.
- **Your objectives.** Rank cost, supply security, quality and service the way your company ranks them for each kind of category.
- **Your records.** Decide where the approved plan lives, so next year's run starts from its baseline.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini. Decide which exports and documents the assistant may read.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. This version was tried once on its invented example in Claude on 10 November 2026, and the record of that run is published with it; the record says that the run was made by the model that revised the template, lists two small wording fixes made during the run and checked against its output, and lists the small edits made after an independent review, which were checked against the recorded output but not run again. An earlier run of the first draft, the same day, found the gaps this version fixes. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on one or two categories your buyer knows well, with hard cases written in advance: an export whose headers do not match, a row whose amount does not equal quantity times price, an item only one supplier can make, a notice date that falls before the plan starts. The buyer checks every figure and date against the export and the supplier facts before anyone relies on the plan. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete capability template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the capability drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related capabilities

- [Vendor quote comparison](../vendor-quote-comparison/)
- [Vendor renewal review](../vendor-renewal-review/)
- [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
