# Supplier risk alert brief

When something happens to a supplier you depend on, the buyer gets a dated brief the same day: what happened and who reported it when, what you buy from them, how many days of stock you hold against how long another source would take, how exposed you are, and actions with owners and dates.

*Workflow template · Procurement and suppliers · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/supplier-risk-alert-brief/)*

## The outcome

Bad news about a supplier arrives in pieces: a headline, a short email from the account manager, something a colleague heard on a call. This workflow template turns those pieces into one page the procurement lead can act on.

Every fact on the page says where it came from and how firm it is: confirmed by the supplier in writing or an official record, reported in the press, or only heard. Promises the supplier makes about restarting or shipping are shown as promises. Nothing is added that the sources do not say, so nobody walks into a meeting repeating a rumour as fact.

Then the page does the arithmetic that matters. For each item you buy from that supplier it works out how many days your stock lasts, the date it runs out, and how that compares with the time another source would need. Each item is rated High, Medium, Low or Not assessed, and a missing figure is never treated as good news. Estimates are labelled wherever they are used.

The brief ends with the actions a person should decide, each with an owner and a date, and the questions worth putting to the supplier. The assistant contacts nobody and changes nothing: your procurement lead decides whether anyone calls the supplier and whether any order moves.

## Who starts the work, and when

The buyer, or whoever first sees the report, starts it as soon as news reaches the business: a news item, a registry filing, a regulator's notice, a message from the supplier, or something a colleague heard. The usual triggers are signs of money trouble, a site or production line stopped, a regulator's or certifier's action, or a failure at one of the supplier's own suppliers. It runs again when a new report arrives, and on the review date the brief sets.

The procurement lead reads the brief and decides what happens next.

## What they supply

- **The reports.** Each one with who published or said it, when, and when it reached you, with its text pasted in or a short note of what was said.
- **The items you buy from that supplier,** as an export from your item list or stock system: stock on hand, weekly use, open orders, spend, whether it is your only source, and how long another source would take. The template states the column headers it expects and stops to ask when yours differ.
- **Where each item is used,** if you want actions about products or customer orders.
- **Your settings:** who reads the brief, who owns each kind of action, your working days, the margin you want between stock and the time to another source, and your deadlines.
- **The last brief on this supplier,** if there is one.

No connection to a news service, a credit agency or your stock system is needed, and none is asked for.

## What comes out

One brief, dated, in a fixed order:

1. **What happened,** fact by fact, each with its source and how firm it is, and any point where the sources disagree.
2. **What you buy from them,** item by item, with spend shown for context only.
3. **Exposure:** days of stock, run-out dates, the time to another source, the gap between them and a rating for each item, plus what changes if the supplier's own promises hold.
4. **What is not known yet,** and what would settle each point.
5. **Actions for a person to decide,** each with an owner and a date, and the items that need nothing before the next review.
6. **Questions to put to the supplier,** for whoever your procurement lead chooses to make contact.

Good looks like this: the procurement lead can see at a glance which item runs out first, by when, and who is doing what about it this week.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/), which owns the supplier relationship and the search for another source.
- [Supply chain and inventory](https://fullypowered.ai/functions/supply-chain-and-inventory/), which holds the stock figures and the production plan the brief depends on.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where one supplier's stopped line can stop yours within weeks.
- [Consumer brands](https://fullypowered.ai/industries/consumer-brands/), where a single packaging or component supplier often sits behind a best-selling product.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where a supplier's trouble shows up as empty shelves and late orders.
- [Construction](https://fullypowered.ai/industries/construction/), where a materials supplier's problem moves a whole project's dates.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where long-standing suppliers have never had their exposure written down.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), where more products depend on more suppliers than anyone can keep in their head.

## What has to change for your company

- **Who reads the brief** and decides whether anyone contacts the supplier.
- **Who owns each kind of action:** contact with the supplier and open orders, other sources, the production plan, payments.
- **Your margin:** how many days of stock beyond the time to another source you count as comfortable. The default is 14.
- **Your deadlines and review intervals** for each rating.
- **Your export's column headers,** and how your team marks an estimate.
- **How you count the time to another source:** whether it includes approving a new supplier, samples or tooling.
- **Who answers questions about your supply agreements,** and who clears any report that dealing with a supplier is barred. The workflow template leaves both to them.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini. Decide which reports and exports the assistant may read.

## What has been checked

Fully Powered AI wrote this workflow template in its own words, drawing on a published supplier risk method credited with it. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026 in two runs; the record of the second, made on the current wording, is published with it. That record says plainly that the second run was made by the model that revised the template after the first, so it was not blind to the published example. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past supplier scares your team remembers, with hard cases written in advance: a news report the supplier never confirmed, a supplier's promise that later slipped, an item with no known time to another source, an export whose headers do not match, a problem at the supplier's own supplier. The procurement lead checks every figure and date against the export before anyone acts on the brief. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Supplier issue notice](../supplier-issue-notice/)
- [Inventory reorder plan](https://fullypowered.ai/workflow templates/inventory-reorder-plan/)
- [Supplier spend analysis](../supplier-spend-analysis/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
