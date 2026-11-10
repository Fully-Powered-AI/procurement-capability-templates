# Supplier spend analysis

From one accounts-payable export, the finance or operations lead sees where the money goes: spend cleaned and grouped by category and supplier, the few suppliers that take most of it, the tail, needs bought from several suppliers and consolidation opportunities, each with its figures. A person decides what to act on.

*Capability template · Procurement and suppliers · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/supplier-spend-analysis/)*

## The outcome

The business finally sees its supplier spend whole. Every bill in the period, from flour and freight to rent and repairs, lands in one analysis: sorted into the categories the business uses, ranked by supplier, and boiled down to the handful of suppliers that take most of the money and the long list of everyone else.

The cleaning is done in the open. Accounts that are not supplier spend, such as sales tax or loan repayments, are set aside with their totals. Three spellings of one supplier become one line, and the merge is shown so anyone can undo it. Credit notes are netted. Names that only look alike are kept apart and raised as a question.

Then come the conversations worth having. Where the business buys the same thing from two, three or four suppliers, the analysis shows how the money splits, and where that spend is big enough to matter, it becomes a consolidation opportunity with its figures. Each one arrives as a question for the budget holder and a decision for whoever leads the business. Nobody is told which supplier to keep. People talk to suppliers, people choose, and people move the spend.

## Who starts the work, and when

The finance lead, finance manager or operations lead who can export accounts payable starts it once or twice a year: before budget season, before a sourcing round, after an acquisition brings in a second set of suppliers, or whenever the owner asks where the money goes. The owner, managing director or finance director makes the decisions it lists.

## What they supply

- **An accounts-payable export** for the period, at least three months and ideally twelve: bill date, supplier, bill number, description, the account each bill was coded to, and the amount, with credit notes as negative amounts.
- **A category map,** if they have one: each supplier with the need it meets and the budget holder for that need. Without one, the analysis groups by the accounts the bills were coded to.
- **The settings:** today's date, the period, the currency, the accounts to leave out, the share that counts as concentration (80% unless they choose otherwise), the category spend worth calling an opportunity, and, only if they want saving figures, the low and high percent they are willing to assume.

No connection to the accounting system or the bank is needed, and none is asked for.

## What comes out

One analysis, in a fixed order:

1. **Cleaning:** rows read and left out, credit notes, names merged, look-alike names kept apart, bills with no account, and suppliers missing from the map.
2. **A summary** of the spend, the concentration and the tail.
3. **Spend by category,** with the budget holder for each.
4. **Spend by supplier,** ranked, with each supplier's share and the running total.
5. **Concentration:** how few suppliers take most of the spend.
6. **The tail:** how many suppliers share the rest, in how many bills, and how many were used only once.
7. **Needs bought from more than one supplier,** with how the money splits.
8. **Consolidation opportunities,** each with its spend, its suppliers and, only when an assumption was given, a saving range clearly labelled as that assumption.
9. **Questions** for the budget holders, each resting on a fact.
10. **Decisions** for whoever leads the business.
11. **What was not supplied or checked,** starting with the plain statement that no contract or price list was read.

Every figure can be checked against the export with a calculator. An opportunity that needs a closer look can go on to a [vendor quote comparison](https://fullypowered.ai/capabilities/vendor-quote-comparison/).

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/), which decides who the business buys from and on what terms.
- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which holds the accounts-payable ledger and owns the budget the suppliers are paid from.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where materials, packaging and freight are most of the cost and often come from more suppliers than anyone planned.
- [Construction](https://fullypowered.ai/industries/construction/), where each project picks its own suppliers and the same materials end up bought from many of them.
- [Hospitality](https://fullypowered.ai/industries/hospitality/), where food, drink, linen and cleaning arrive from a long list of suppliers, site by site.
- [Growth and scaling](https://fullypowered.ai/situations/growth-and-scaling/), when buying has spread across teams and nobody sees the whole supplier list.
- [Acquisitions and integration](https://fullypowered.ai/situations/acquisitions-and-integration/), when two businesses bring two sets of suppliers for the same needs.
- [Private equity and portfolios](https://fullypowered.ai/situations/private-equity-and-portfolios/), where owners want to know early how supplier spend is spread across a portfolio company.

## What has to change for your company

Map the column headers of your accounting system's export, and decide whether you export bills or payments. List the accounts that are not supplier spend in your books. Build the category map with your budget holders, naming each need finely enough that two suppliers in one category really meet the same need. Set the concentration share, the spend worth calling an opportunity and, if you want saving figures at all, the percentages your business is willing to assume. Name who decides, who keeps the map between analyses, and where the finished analysis is kept. It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026, and the record of that run is published with the template; it lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past period your finance lead knows well, with hard cases written in advance: an export whose headers do not match, one bill exported twice, a supplier spelled three ways, two names that look alike but are different businesses, a credit note larger than the bills it offsets, and a category that sits just under the floor. The runner checks every figure against the export before anyone relies on the analysis. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Software subscription and vendor spend review](../software-subscription-and-vendor-spend-review/)
- [Supplier bill review and payment-run preparation](https://fullypowered.ai/capabilities/supplier-bill-review-and-payment-run-preparation/)
- [Vendor quote comparison](../vendor-quote-comparison/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
