# Business insurance renewal review

Before the business insurance renews, the owner gets one pack: every policy with insurer, limits, deductibles, premium and dates; renewal terms beside expiring ones, every change marked; what changed in the business; claims; and questions for the broker. The broker and the owner decide all cover.

*Capability template · Procurement and suppliers · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/business-insurance-renewal-review/)*

## The outcome

The renewal meeting with the broker starts from the facts instead of from a stack of PDFs. The owner sees every policy on one page, with what it costs and when it ends, and every line where the renewal differs from this year: a higher deductible, a new exclusion, a changed limit, a rise in premium, each marked and measured.

Beside the policies sits what the insurers may not yet know: more people, more revenue, a second site, extra vans, a new kind of work, and customer contracts that ask for a set amount of cover. The claims history is totalled by line, and any incident in the business's own records that the insurer's list does not show is picked out. Every fact that deserves an answer is already written as a question for the broker.

The pack reads what the schedules print and stops there. It never says whether a loss would be covered and never recommends cover. The broker advises, the owner decides, and a person sends every question and every figure.

## Who starts the work, and when

The owner, operations lead, finance lead or office manager who looks after the insurance starts it a month or two before the renewal date: when the broker's renewal terms arrive, or earlier with this year's schedules alone, so that the business's changes reach the broker in time. The finance lead confirms the business's figures. The owner decides, with the broker.

## What they supply

- **The renewal facts:** the renewal date, the broker, who decides, and how far ahead of the renewal the questions should be with the broker.
- **This year's schedules:** the schedule or declarations page of each policy, as the broker sent it.
- **The renewal terms:** the renewal schedules or the broker's renewal summary, if they have arrived.
- **What changed in the business:** headcount, revenue, payroll, sites and vehicles then and now, with the figures the renewal application gave, and any new kind of work.
- **New contracts that ask for cover,** as whoever read each contract states the requirement.
- **The claims history** from the broker or insurer, and the business's own record of incidents if it keeps one.
- **The owner's own questions** for the broker.

No connection to the broker's or the insurer's systems is needed, and none is asked for.

## What comes out

One pack, in a fixed order:

1. **Dates:** the renewal date, the date to have questions with the broker, a status, and any policy that ends on another date.
2. **The policies:** each one with its insurer, number and period, and every limit, deductible, endorsement, exclusion and premium set beside the renewal terms, marked same, changed, new or removed.
3. **What changed in the business,** with each figure given to the insurer set beside today's.
4. **New contracts that ask for cover:** the amount asked for beside the amount the schedule prints, for the broker to confirm.
5. **Claims history,** totalled by line, with open claims and anything missing from the insurer's list.
6. **Questions for the broker,** each tied to a fact.
7. **Decisions for the owner.**
8. **What was not supplied or checked,** starting with the plain statement that no policy wording was read or interpreted.

A good pack can be checked against the schedules with a calculator, and the owner can walk into the broker meeting without opening another file.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/), which buys the insurance and keeps the broker relationship.
- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which pays the premiums and holds the revenue and payroll figures the insurers ask for.
- [Compliance, risk and privacy](https://fullypowered.ai/functions/compliance-risk-and-privacy/), where the business keeps track of what it has insured and what its customers require.
- [Construction](https://fullypowered.ai/industries/construction/), where customer contracts set the cover a contractor must carry and vans and sites change year to year.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where premises, stock and payroll move the renewal.
- [Logistics and trade](https://fullypowered.ai/industries/logistics-and-trade/), where the vehicle count changes between renewals.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where client contracts often ask for set amounts of cover.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the renewal comes round every year and last year's pack is the starting point.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the business has grown faster than the figures the insurers hold.

## What has to change for your company

Name who decides and who talks to the broker. Choose how many days before the renewal the questions should be with the broker, and the size of change in a business figure worth raising. List the figures you track at each renewal and where each comes from. Map the column headers of your claims history and your own incident record. Decide who reads new customer contracts for insurance requirements and keeps them between renewals. It runs in ChatGPT, Claude, Copilot or Gemini, from documents and files you supply.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026; the record of that run is published with it, and lists the small edits made afterward that have not been run again. That run covered an ordinary renewal and did not reach the refusals or the stop conditions. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on last year's renewal, which your team remembers, with hard cases written in advance: an item renamed between the two schedules, a new exclusion, a contract asking for more than the schedule prints, a claims export whose headers do not match, and a question asking whether a loss would be covered. The runner checks every figure against the schedules before anyone relies on the pack. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Vendor renewal review](../vendor-renewal-review/)
- [Vendor quote comparison](../vendor-quote-comparison/)
- [Workplace risk assessment](https://fullypowered.ai/capabilities/workplace-risk-assessment/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
