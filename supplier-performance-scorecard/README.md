# Supplier performance scorecard

Once a quarter, the buyer or operations lead scores each key supplier from the business's own order and receiving exports: on-time delivery, fill rate, defects and returns, price against agreed terms and order confirmations, with the trend, the evidence behind every score and the points to raise. A person decides.

*Workflow template · Procurement and suppliers · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/supplier-performance-scorecard/)*

## The outcome

Every key supplier gets the same honest report card each quarter, built from what actually arrived at your door. Did the goods come on the date on the order? Did the full quantity come? How much was rejected at receiving or sent back? Was each line priced at what you agreed? Did the supplier confirm your orders promptly? Each answer is a figure with its target beside it and last quarter's figure next to that, so a slide shows up before it becomes a crisis.

Every score shows its working. A late-delivery figure lists the late lines, with their due dates and the days late. A price figure lists each line charged above the agreed price and adds up what that cost. Anyone can check any number against the exports with a calculator.

Spend and dependence sit side by side and are never blended. A small supplier you cannot replace is shown as exactly that, however little you spend with it. The scorecard then writes the points to raise at each supplier review and the questions for whoever decides: a formal warning, a change of tier, a move to another supplier, or finding an alternative where there is none. A move away from a supplier is only ever raised when an alternative is already named. People decide, people talk to suppliers, and nothing is sent or changed by the scorecard.

## Who starts the work, and when

The buyer, purchasing lead or operations lead starts it once a quarter, after the quarter's deliveries are received and booked and before the quarterly supplier reviews. The owner, managing director or operations director makes the decisions it lists. The person who owns each supplier relationship raises the points at that supplier's review.

## What they supply

- **The key supplier list:** each supplier to score, its category, the tier your business gives it, whether it is your only source today, any alternative already named, and who owns the relationship.
- **A purchase-order lines export** for the quarter: order number and line, supplier, item, order date, due date, quantity, the price on the order, and the date the supplier confirmed the order.
- **A receiving export:** each receipt against its order line, with the date, the quantity that arrived and the quantity rejected at receiving, with the reason.
- **A returns export** and **your agreed-price list,** if you keep them.
- **Last quarter's figures,** to show the trend.
- **Your settings:** the targets for each measure, how many days late still counts as on time, and the few counts that decide when a question is raised.

No connection to your purchasing or accounting system is needed, and none is asked for.

## What comes out

One scorecard, in a fixed order:

1. **The targets and checks:** rows read, suppliers in the exports that are not on your key list, and any line the scorecard could not use.
2. **A summary:** targets met for each supplier, and which suppliers are your only source.
3. **One block per key supplier,** highest spend first: spend, dependence, the five measures each with its target, last quarter's figure and the evidence, and the points to raise at the next review.
4. **Decisions** for whoever decides, each with its facts.
5. **What was not supplied or checked,** starting with the plain statement that no contract or invoice was read.

The points to raise can go on to a [supplier issue notice](https://fullypowered.ai/workflows/supplier-issue-notice/) when a person decides a supplier should be told formally.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/), which chooses suppliers and holds them to what was agreed.
- [Supply chain and inventory](https://fullypowered.ai/functions/supply-chain-and-inventory/), which feels every late or short delivery on the shelf and the production line.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where one late component or a batch of rejects stops a line.
- [Ecommerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where stock that arrives late or short becomes lost sales and unhappy customers.
- [Consumer brands](https://fullypowered.ai/industries/consumer-brands/), where packaging and ingredients come from a few specialist suppliers that are hard to replace.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where supplier relationships run on habit and memory and deserve a quarterly look at the facts.
- [Growth and scaling](https://fullypowered.ai/situations/growth-and-scaling/), when order volumes rise and a supplier's slips start to cost real money.

## What has to change for your company

Map the column headers of your purchasing system's exports, and check that rejections at receiving are recorded there. Choose your key suppliers and name an owner for each. Set a target for each measure, the days of grace on a due date, the price tolerance and the confirmation window. Decide how many lines a measure needs before it is judged, what change counts as better or worse, and how many missed targets raise a question about a supplier's tier or a move away from it. Use your own tier names. Keep the agreed-price list current. Name who decides and where the finished scorecard is kept. It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026; the record is published with it. The points that run found open were settled the same day, after an independent review, without a rerun; the record lists them and says where the recorded output differs from the rules as they now stand. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past quarter your buyer knows well, with hard cases written in advance: an export whose headers do not match, a delivery that came in parts, a line with nothing received, a line priced above the agreed price, a supplier with too few orders to score, and a sole source with a small spend. The runner checks every figure against the exports before anyone relies on the scorecard. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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
- [Vendor renewal review](../vendor-renewal-review/)
- [Supplier spend analysis](../supplier-spend-analysis/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
