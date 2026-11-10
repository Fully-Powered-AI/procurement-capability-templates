# Supplier risk alert brief: an invented example

*Illustrative example with invented data.* The companies, the news site, the people, the items and every figure below are invented. Company L is an invented maker of outdoor wall lights with about 70 people. Supplier B, also invented, die-casts three aluminium parts for it. On a Tuesday morning Company L's buyer reads that Supplier B's plant has had a fire, and prepares a brief for the procurement lead. People are referred to by role.

The inputs come first, in full, so the template can be run on them. The brief follows.

## The inputs

### 1. The reports

```
S1
Source: News site N (an invented regional business news site)
Kind: news publication
Published: Monday 9 November 2026
Reached us: Tuesday 10 November 2026, 08:40, found by the buyer
Text: "Fire damages casting hall at Supplier B. A fire late on Sunday
damaged the casting hall at Supplier B's plant. Fire crews were at
the site for several hours. Supplier B said casting has stopped while
the building is inspected and gave no date for a restart."

S2
Source: Supplier B's account manager, email to our buyer
Kind: the supplier in writing
Sent: Tuesday 10 November 2026, 11:15
Reached us: Tuesday 10 November 2026, 11:15
Text: "Our casting line is down after Sunday's fire. We expect to
restart in about three weeks, subject to the insurer's inspection.
Finished housings already in our warehouse will still ship. On your
PO 7712 for 1,200 LH-40 housings, 400 are finished and will go out
this week; the other 800 depend on the restart."

S3
Source: our operations lead, on a trade association call
Kind: a person
Said: Tuesday 10 November 2026
Reached us: Tuesday 10 November 2026, 13:00
Note: "Someone on the call said Supplier B's powder-coating booth was
damaged too. Not confirmed."
```

### 2. The event

```
At the supplier itself. We do not know Supplier B's own suppliers.
```

### 3. The items export (Supplier B rows, exported Tuesday 10 November 2026)

```
item,description,sole_source,spend_12m,on_hand,weekly_use,open_order_qty,open_order_due,other_source,days_to_other_supply
LH-40,Die-cast aluminium housing for the large wall light,yes,186000,520,130,1200,2026-11-20,none,98 est
LH-25,Die-cast aluminium housing for the small wall light,no,64000,900,75,0,,Supplier C,35
EB-10,Die-cast end bracket,yes,9500,300,60 est,0,,none,
```

### 4. Where each item is used

```
LH-40 goes into the WL-400 wall light.
LH-25 goes into the WL-250 wall light.
EB-10 goes into both the WL-400 and the WL-250.
```

### 5. Notes

```
- The 98 days for LH-40 is the procurement lead's estimate: about
  10 weeks to approve a new caster and 4 weeks' lead time after that.
- The 60 a week for EB-10 is the operations lead's estimate; nobody
  has pulled the usage records yet.
```

### 6. The settings

```
Date prepared: Tuesday 10 November 2026
Prepared by: buyer. Brief for: procurement lead
Working days: Monday to Friday
Closed dates: Thursday 26 and Friday 27 November 2026
Owners: contact with the supplier and open orders, buyer; other sources
  and approving new ones, procurement lead; production plan and usage
  figures, operations lead; payments, finance lead
Margin: 14 days
Action deadlines (working days after the date prepared): Not assessed
  1, High 2, Medium 5, Low at the next review
Next review (working days after the date prepared): Not assessed 1,
  High 2, Medium 5, Low 20
Contract questions: contract reviewer
Sanctions and government orders: compliance lead
Currency: US dollars
```

### 7. The last brief

```
None. This is the first brief on Supplier B.
```

## The brief

**SUPPLIER RISK ALERT BRIEF: Supplier B, fire stops casting**

For: procurement lead. Prepared: Tuesday 10 November 2026 by the buyer. Next review: Thursday 12 November 2026, or sooner if a new report arrives.
Change since last brief: first brief on this supplier.
Overall exposure: High, set by LH-40.
Stop before any order or payment: none.

**WHAT HAPPENED**

Kind of event: a site or production stopped.
Where: at the supplier.

- A fire on Sunday at Supplier B's plant (Confirmed; S1, S2).
- The fire damaged the casting hall (Reported; S1).
- Casting has stopped (Confirmed; S1, S2).
- Supplier B expects to restart in about three weeks, subject to the insurer's inspection (supplier's statement; S2). S1, published on 9 November, gave no date for a restart.
- Finished housings already in Supplier B's warehouse will still ship (supplier's statement; S2).
- On PO 7712 for 1,200 LH-40 housings, 400 are finished and will go out this week; the other 800 depend on the restart (supplier's statement; S2).
- Supplier B's powder-coating booth was damaged too (Heard; S3).

Sources:

S1. News site N, news publication. Published or said: Monday 9 November 2026. Reached us: Tuesday 10 November 2026, 08:40. "A fire late on Sunday damaged the casting hall at Supplier B's plant … Supplier B said casting has stopped while the building is inspected and gave no date for a restart."
S2. Supplier B's account manager, the supplier in writing. Published or said: Tuesday 10 November 2026, 11:15. Reached us: Tuesday 10 November 2026, 11:15. "Our casting line is down after Sunday's fire. We expect to restart in about three weeks, subject to the insurer's inspection. Finished housings already in our warehouse will still ship. On your PO 7712 for 1,200 LH-40 housings, 400 are finished and will go out this week; the other 800 depend on the restart."
S3. Operations lead, a person. Published or said: Tuesday 10 November 2026. Reached us: Tuesday 10 November 2026, 13:00. "Someone on the call said Supplier B's powder-coating booth was damaged too. Not confirmed."

Disagreements between sources: none.

**WHAT WE BUY FROM THEM**

Spend in the last 12 months: \$259,500 across 3 items. Spend is shown for context and changes no rating.

- LH-40, die-cast aluminium housing for the large wall light. Sole source: yes. Spend: \$186,000. On hand: 520. Weekly use: 130. Open orders: 1,200 due Friday 20 November 2026. Used in: WL-400 wall light.
- LH-25, die-cast aluminium housing for the small wall light. Sole source: no. Spend: \$64,000. On hand: 900. Weekly use: 75. Open orders: none. Used in: WL-250 wall light.
- EB-10, die-cast end bracket. Sole source: yes. Spend: \$9,500. On hand: 300. Weekly use: 60 (estimate). Open orders: none. Used in: WL-400 and WL-250 wall lights.

**EXPOSURE**

Assumption: nothing more arrives from Supplier B after Tuesday 10 November 2026, open orders included. This is a planning assumption, not a forecast.

- LH-40: cover on hand 28 days (520 x 7 / 130), runs out Tuesday 8 December 2026. Another source: could supply in 98 days (none approved) (estimate). Gap: 70 days with no stock, Tuesday 8 December 2026 to Tuesday 16 February 2027 (estimate). If open orders arrive: 92 days. Rating: High: the cover on hand runs out 70 days (estimate) before another source could supply.
- LH-25: cover on hand 84 days (900 x 7 / 75), runs out Tuesday 2 February 2027. Another source: could supply in 35 days (Supplier C). Gap: cover lasts 49 days beyond. If open orders arrive: no open orders. Rating: Low: the cover lasts 49 days beyond the time Supplier C needs, more than the 14-day margin.
- EB-10: cover on hand 35 days (300 x 7 / 60), runs out Tuesday 15 December 2026 (estimate). Another source: not known. Gap: not known. If open orders arrive: no open orders. Rating: Not assessed: the time another source would need is not known. It is a sole-source item, and its spend of \$9,500 does not lower the rating.

If Supplier B's statement holds: 400 of the LH-40 housings on PO 7712 go out this week (S2), so LH-40 cover becomes 49 days ((520 + 400) x 7 / 130) and runs out Tuesday 29 December 2026; the other 800 depend on a restart in about three weeks (S2). Supplier's statement, not confirmed.
Sub-suppliers: not part of this event.

**WHAT WE DO NOT KNOW**

1. When casting restarts. S2 gives Supplier B's estimate of about three weeks, subject to an inspection with no date. Settled by the inspection date and Supplier B's confirmation in writing.
2. Whether the 400 finished LH-40 housings will ship this week, and on which day (S2). Settled by a shipping notice from Supplier B.
3. Whether the other 800 LH-40 housings on PO 7712 will ship, and when (S2). Settled by a confirmed restart date.
4. Whether the powder-coating booth was damaged (S3, Heard). Settled by Supplier B in writing.
5. How many days another source would need to supply EB-10: the export leaves it blank. Settled by the procurement lead.
6. EB-10 weekly use: the 60 a week is the operations lead's estimate. Settled by the usage records.
7. LH-40 time to another source: the 98 days is the procurement lead's estimate. Settled when a possible new caster gives its approval time and lead time.

**ACTIONS FOR A PERSON TO DECIDE**

1. Decide whether the buyer puts the questions below to Supplier B in writing. Owner: procurement lead. By: Wednesday 11 November 2026. Why: LH-40 rated High and EB-10 rated Not assessed; S2 and S3.
2. Decide whether to start approving another source for LH-40 now. Owner: procurement lead. By: Thursday 12 November 2026. Why: LH-40 rated High, with no approved other source and an estimated 98 days to another supply.
3. Confirm the 98-day estimate for LH-40 with the approval time and lead time of a possible new caster. Owner: procurement lead. By: Thursday 12 November 2026. Why: LH-40 rated High; the time to another source is an estimate.
4. Review the WL-400 production plan against an LH-40 run-out on Tuesday 8 December 2026. Owner: operations lead. By: Thursday 12 November 2026. Why: LH-40 rated High; it goes into the WL-400.
5. Find out how many days another source would need to supply EB-10. Owner: procurement lead. By: Wednesday 11 November 2026. Why: EB-10 rated Not assessed.
6. Review the WL-400 and WL-250 production plans against an EB-10 run-out on Tuesday 15 December 2026 (estimate). Owner: operations lead. By: Wednesday 11 November 2026. Why: EB-10 rated Not assessed; it goes into both lights.
7. Confirm EB-10 weekly use from the usage records. Owner: operations lead. By: Wednesday 11 November 2026. Why: EB-10 rated Not assessed; its weekly use is an estimate.

No action before the next review: LH-25.
Decided only by a person: whether and when anyone contacts Supplier B, moving or cancelling any order, any change to stock levels, and any payment.

**QUESTIONS TO PUT TO SUPPLIER B**

For the buyer, if the procurement lead agrees to contact Supplier B.

1. On which day will the 400 finished LH-40 housings on PO 7712 ship? (S2)
2. When is the insurer's inspection, and what else does the restart depend on? (S2)
3. When the line restarts, when will the other 800 LH-40 housings on PO 7712 ship? (S2)
4. Was your powder-coating booth damaged? (S3)
5. Do you hold finished EB-10 brackets in your warehouse, and how many? Your message mentions finished housings only. (EB-10, S2)

Every fact traces to a numbered source, the items export of Tuesday 10 November 2026 or the notes supplied. Estimates are labelled. Draft for the procurement lead. Nothing has been sent, ordered, paid or changed, and nobody has been contacted.
