# Software subscription and vendor spend review

From a card statement or ledger export, the finance or operations lead gets every subscription on one register: what each costs a year, who owns it, what renews in the next 90 days, what looks unused, duplicated or orphaned, and the decisions to make. Nothing is cancelled or changed.

*Workflow template · Procurement and suppliers · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/software-subscription-and-vendor-spend-review/)*

## The outcome

Subscriptions stop being a list of card charges nobody can explain. Every recurring payment in the period is on one register, sorted by what it costs a year, with its owner, how it is paid, and when the annual ones renew. Design tools, video meetings, file storage, hosting, accounting software, newsletters, fonts: all of it, not only the sales stack.

Under the register sit the things worth a conversation. Seats paid for and not used. Two tools doing the same job. A charge that rose. A tool whose owner has left. A subscription someone pays on an expense claim. A charge that came twice in one month. Each one arrives as a question for the person who can answer it, and the choices that belong to the decision-maker arrive as decisions, with the renewals coming up first.

The review prepares and stops there. People talk to the owners, people decide what to keep, and people cancel or change anything that changes.

## Who starts the work, and when

The finance lead, operations lead or office manager who sees the card statements starts it once a quarter, before budget season, when the card bill looks bigger than it should, or when someone leaves who paid for tools. The owner, managing director or finance director makes the decisions it lists.

## What they supply

- **A spend export** for the period, at least three months and ideally twelve, from the company card statement, the accounting ledger or both: date, payee, description, amount and how it was paid. Exporting only the accounts or card categories where subscriptions land keeps it short.
- **Owner notes,** if they have them: last year's register or a short list saying what each tool is for, who owns it, seats paid and used, renewal dates they know, and whether the work stops without it.
- **A list of people who have left,** with the date each left, so tools still in their name come to light.
- **The settings:** today's date, the period, the currency, how far ahead to look for renewals and the size of price change worth reporting.

No connection to the card provider, the bank or the accounting system is needed, and none is asked for.

## What comes out

One review, in a fixed order:

1. **A summary:** how many subscriptions, their annual cost, what was paid in the period and how.
2. **The register,** highest annual cost first, with the subscriptions whose charges stopped listed at the end.
3. **Spend by category,** so the reader sees which kinds of tool cost the most.
4. **Renewals in the look-ahead window,** and any month where several renewals land together.
5. **Flags,** grouped by kind.
6. **Consolidation candidates:** tools in the same category, with what keeping one would save before switching costs, and a warning where a critical tool has no written fallback.
7. **Charges it could not class,** for a person to mark.
8. **Questions,** each tied to a fact and addressed to the person who can answer it.
9. **Decisions** for the decision-maker.
10. **What was not supplied or checked,** starting with the plain statement that no agreement was read.

Every figure can be checked against the export with a calculator. A renewal that needs a closer look can go on to a [vendor renewal review](https://fullypowered.ai/workflows/vendor-renewal-review/).

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/), which keeps the list of who the business pays and when each commitment comes up.
- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which sees the card statements and the ledger and owns the budget the subscriptions eat into.
- [Software and technology](https://fullypowered.ai/industries/software-technology/), where every team adds tools and the bill grows faster than headcount.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where each practice or team buys its own software and nobody sees the whole list.
- [Marketing and advertising](https://fullypowered.ai/industries/marketing-and-advertising/), where design, media and campaign tools pile up project by project.
- [Growth and scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the company has grown past the point where one person remembers every subscription.

## What has to change for your company

Map the column headers of your own card and ledger exports, and decide which accounts or card categories to export. Set the look-ahead window, the price-change size worth reporting and the period you review. Name the decision-maker, and who keeps the register between reviews. Agree the category names you use, so two tools doing the same job land in the same place. Decide how often the review runs and where the finished review is kept. It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried once on its invented example in Claude on 9 November 2026, and the record of that run is published with it; the record lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past quarter your finance lead knows well, with hard cases written in advance: an export whose headers do not match, the same charge in both the card and the ledger export, a tool whose owner left, an annual renewal charged before the period began, a usage-billed tool whose charge moves every month. The runner checks every figure against the export before anyone relies on the review. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Vendor renewal review](../vendor-renewal-review/)
- [Vendor quote comparison](../vendor-quote-comparison/)
- [Budget-versus-actual variance commentary](https://fullypowered.ai/workflows/budget-versus-actual-variance-commentary/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
