# Trial: Supplier risk alert brief, run on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Opus 5.5 (model ID claude-opus-5-5)
- **Date:** 2026-11-10

The inputs for this trial are the invented example published with the template (`public/example.md`, sections 1 to 7: the three reports, the event, the items export, where each item is used, the notes, the settings and the last brief). No client data was used.

This is the second run on 10 November 2026, and the one recorded here. A first run that day, by a different model (Sonnet 5.5) that had not written the template, followed the earlier wording and found eight places where the template left a choice open. After an independent review, five of them were closed in the template and one further gap was filled: when the event is at the supplier itself, "not part of this event" is the wording even when the supplier's own suppliers are not known, and they are not listed as unknown; the decision whether to put the questions to the supplier is owned by the brief reader; the production-plan action covers any item not rated Low whose cover is known, a Not assessed item included, and "confirm an estimate" covers an estimated weekly use on a Not assessed item; the margin's default of 14 is in the pasted instructions, with the rule to use the defaults when a setting is missing; and an estimate's mark is repeated wherever the figure is repeated. Source lines now keep the time of day when it is given. The published example was brought into line with those rules: a seventh action for EB-10, the "(estimate)" mark on the gap in LH-40's rating reason, times on the source lines, and the fourth question no longer asking whether the housings are coated.

This run is not blind. It was made by the model that made those edits, which had read the template, the published example and the first run's record beforehand. It shows that the edited template can be followed on these inputs to a brief that meets it; it is weaker evidence than a run by a model that had seen neither.

## What was done

The fenced instruction block in `member/template.md`, as edited, and the output format were followed on the example's inputs, with no other guidance. The result was then compared with the published example and with the template's reviewer checklist.

## What came out

```
SUPPLIER RISK ALERT BRIEF: Supplier B, fire stops casting

For: procurement lead. Prepared: Tuesday 10 November 2026 by the buyer. Next review: Thursday 12 November 2026, or sooner if a new report arrives.
Change since last brief: first brief on this supplier.
Overall exposure: High, set by LH-40.
Stop before any order or payment: none.

WHAT HAPPENED
Kind of event: a site or production stopped.
Where: at the supplier.
- A fire on Sunday at Supplier B's plant (Confirmed; S1, S2). S1 says it was late on Sunday.
- The fire damaged the casting hall (Reported; S1).
- Fire crews were at the site for several hours (Reported; S1).
- Casting has stopped (Confirmed; S1, S2). S1 says it stopped while the building is inspected.
- Supplier B expects to restart in about three weeks, subject to the insurer's inspection (supplier's statement; S2). S1, published on 9 November, said Supplier B gave no date for a restart.
- Finished housings already in Supplier B's warehouse will still ship (supplier's statement; S2).
- On PO 7712 for 1,200 LH-40 housings, 400 are finished and will go out this week; the other 800 depend on the restart (supplier's statement; S2).
- Supplier B's powder-coating booth was damaged too (Heard; S3).
Sources:
S1. News site N, news publication. Published or said: Monday 9 November 2026. Reached us: Tuesday 10 November 2026, 08:40. "A fire late on Sunday damaged the casting hall at Supplier B's plant. Fire crews were at the site for several hours. Supplier B said casting has stopped while the building is inspected and gave no date for a restart."
S2. Supplier B's account manager, the supplier in writing. Published or said: Tuesday 10 November 2026, 11:15. Reached us: Tuesday 10 November 2026, 11:15. "Our casting line is down after Sunday's fire. We expect to restart in about three weeks, subject to the insurer's inspection. Finished housings already in our warehouse will still ship. On your PO 7712 for 1,200 LH-40 housings, 400 are finished and will go out this week; the other 800 depend on the restart."
S3. Operations lead, a person. Published or said: Tuesday 10 November 2026. Reached us: Tuesday 10 November 2026, 13:00. "Someone on the call said Supplier B's powder-coating booth was damaged too. Not confirmed."
Disagreements between sources: none.

WHAT WE BUY FROM THEM
Spend in the last 12 months: $259,500 across 3 items. Spend is shown for context and changes no rating.
- LH-40, die-cast aluminium housing for the large wall light. Sole source: yes. Spend: $186,000. On hand: 520. Weekly use: 130. Open orders: 1,200 due Friday 20 November 2026. Used in: WL-400 wall light.
- LH-25, die-cast aluminium housing for the small wall light. Sole source: no. Spend: $64,000. On hand: 900. Weekly use: 75. Open orders: none. Used in: WL-250 wall light.
- EB-10, die-cast end bracket. Sole source: yes. Spend: $9,500. On hand: 300. Weekly use: 60 (estimate). Open orders: none. Used in: WL-400 and WL-250 wall lights.

EXPOSURE
Assumption: nothing more arrives from Supplier B after Tuesday 10 November 2026, open orders included. This is a planning assumption, not a forecast.
- LH-40: cover on hand 28 days (520 x 7 / 130), runs out Tuesday 8 December 2026. Another source: could supply in 98 days (none approved) (estimate). Gap: 70 days with no stock, Tuesday 8 December 2026 to Tuesday 16 February 2027 (estimate). If open orders arrive: 92 days ((520 + 1,200) x 7 / 130). Rating: High: the cover on hand runs out 70 days (estimate) before another source could supply.
- LH-25: cover on hand 84 days (900 x 7 / 75), runs out Tuesday 2 February 2027. Another source: could supply in 35 days (Supplier C). Gap: cover lasts 49 days beyond. If open orders arrive: no open orders. Rating: Low: the cover lasts 49 days beyond the 35 days Supplier C needs, more than the 14-day margin.
- EB-10: cover on hand 35 days (300 x 7 / 60), runs out Tuesday 15 December 2026 (estimate). Another source: not known. Gap: not known. If open orders arrive: no open orders. Rating: Not assessed: days to other supply is blank in the export. Its spend of $9,500 does not lower the rating.
If Supplier B's statement holds: 400 of the LH-40 housings on PO 7712 go out this week (S2), so LH-40 cover would become 49 days ((520 + 400) x 7 / 130) and run out Tuesday 29 December 2026; the other 800 depend on a restart in about three weeks (S2). Supplier's statement, not confirmed.
Sub-suppliers: not part of this event.

WHAT WE DO NOT KNOW
1. When casting restarts. S2 gives about three weeks, subject to the insurer's inspection, which has no date. Settled by the inspection date and Supplier B's confirmation in writing.
2. Whether the 400 finished LH-40 housings ship this week, and on which day (S2). Settled by a shipping notice from Supplier B.
3. When the other 800 LH-40 housings on PO 7712 ship (S2). Settled by a confirmed restart date.
4. Whether the powder-coating booth was damaged (S3, Heard). Settled by Supplier B in writing.
5. How many days another source would need to supply EB-10: blank in the export. Settled by the procurement lead.
6. EB-10 weekly use: the 60 a week is the operations lead's estimate. Settled by the usage records.
7. LH-40 time to another source: the 98 days is the procurement lead's estimate. Settled by a possible new caster's approval time and lead time.

ACTIONS FOR A PERSON TO DECIDE
1. Decide whether to put the questions below to Supplier B, and who does it. Owner: procurement lead. By: Wednesday 11 November 2026. Why: LH-40 rated High and EB-10 rated Not assessed; S2, S3.
2. Decide whether to start approving another source for LH-40 now. Owner: procurement lead. By: Thursday 12 November 2026. Why: LH-40 rated High, with no approved other source.
3. Review the WL-400 production plan against an LH-40 run-out on Tuesday 8 December 2026. Owner: operations lead. By: Thursday 12 November 2026. Why: LH-40 rated High; it goes into the WL-400.
4. Confirm the 98-day estimate for LH-40. Owner: procurement lead. By: Thursday 12 November 2026. Why: LH-40's gap and rating rest on it.
5. Review the WL-400 and WL-250 production plans against an EB-10 run-out on Tuesday 15 December 2026 (estimate). Owner: operations lead. By: Wednesday 11 November 2026. Why: EB-10 rated Not assessed; it goes into both lights.
6. Find out how many days another source would need to supply EB-10. Owner: procurement lead. By: Wednesday 11 November 2026. Why: EB-10 rated Not assessed; the figure is blank in the export.
7. Confirm EB-10 weekly use from the usage records. Owner: operations lead. By: Wednesday 11 November 2026. Why: EB-10 rated Not assessed; its cover rests on an estimated weekly use.
No action before the next review: LH-25.
Decided only by a person: whether and when anyone contacts Supplier B, moving or cancelling any order, any change to stock levels, and any payment.

QUESTIONS TO PUT TO SUPPLIER B
For the buyer, if the procurement lead agrees to contact Supplier B.
1. On which day will the 400 finished LH-40 housings on PO 7712 ship? (S2)
2. When is the insurer's inspection, and what else does the restart depend on? (S2)
3. Once casting restarts, when will the other 800 LH-40 housings on PO 7712 ship? (S2)
4. Was your powder-coating booth damaged? (S3)
5. Do you hold finished EB-10 brackets in your warehouse, and how many? (EB-10, S2)

Every fact traces to a numbered source, the items export of Tuesday 10 November 2026 or the notes supplied. Estimates are labelled. Draft for the procurement lead. Nothing has been sent, ordered, paid or changed, and nobody has been contacted.
```

## What was observed

Every part of the output format was produced, and nothing in the instructions told the assistant to stop: all three reports named a source and a date, the export headers matched, each item appeared once, the date prepared and working days were given, every setting was supplied, and no report mentioned a sanctions listing.

Figures. Cover, run-out dates, gaps, the open-order figure and the supplier's-statement case were recalculated from the export and agree with the published example: LH-40 28 days (High, 70-day gap, 8 December 2026 to 16 February 2027; 92 days if open orders arrive; 49 days and 29 December 2026 if the 400 ship), LH-25 84 days (Low, 49 days beyond), EB-10 35 days (Not assessed). Deadlines and the next review were counted in working days from Tuesday 10 November; no closed date falls before them. The reviewer checklist's recalculation check (item 3) passed.

The points closed after the first run were followed without a choice to make: the sub-suppliers line reads "not part of this event" and the supplier's own suppliers are not listed as unknown; the first action's owner is the procurement lead; EB-10 gets the production-plan action and the action to confirm its weekly use; the 70 days in LH-40's rating reason carry "(estimate)"; and the source lines keep the times given.

Differences from the published example:
- Fact list: this run added "fire crews were at the site for several hours" (Reported; S1), and noted S1's wording where it adds to a Confirmed fact ("late on Sunday", "while the building is inspected"). The example leaves these out and shortens the S1 quote accordingly.
- Actions: the same seven, in a different order within each item. This run followed the order of the action list in the instructions (production plan before confirming an estimate; for EB-10, the production plan before finding the missing figure); the example lists them otherwise. The instructions fix the order of items, not the order of actions within an item. The "Why" lines differ in wording.
- Rating reasons and not-known items differ only in wording.

No fact in this output is missing from the inputs, and none goes beyond them.

Where the template still leaves a choice open, as found in this run:
1. **Order of actions within one item.** "Order them by item, the questions decision first" does not say how to order several actions about the same item.
2. **Which source numbers to cite for a fact.** For the fire, the strongest source is S2, but this run cited S1 and S2 together, as the example does; the template does not say whether to cite every source or only the strongest.
3. **The source tag on a question** when it follows from neither a source nor an item. It did not arise here.
4. **Which items the decision about questions addresses,** for its deadline. This run, like the example, took all items the questions concern, giving EB-10's one working day.

Nothing in the output was beyond what the template permits: it contacted no one, changed no record, rated no item on spend, and judged neither the supplier's health nor the length of the stoppage. The acceptance tests in the template were not run separately; this trial covers only the invented example (it exercises tests 1, 2, 3 and 4 and, in part, 6).
