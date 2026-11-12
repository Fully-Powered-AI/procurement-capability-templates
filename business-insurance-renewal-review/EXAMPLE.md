# Business insurance renewal review: an invented example

*Illustrative example with invented data.* The business, the broker, the insurers, the customers, the people, the policy numbers, the dates and the amounts below are all invented. The business is an invented 46-person building-maintenance contractor, called Business C here, with its own vans. Its operations lead is preparing for the renewal of its insurance through an invented broker, Broker B, with invented insurers called Insurer K, Insurer M and Insurer N. First come the inputs the operations lead supplied, in full, then the pack the workflow template returned.

## The inputs

### 1. Renewal facts (typed by the operations lead)

```
Business: Business C, building maintenance and repairs for offices
  and shops, with its own vans
Today: Tuesday 10 November 2026
Renewal date: 1 January 2027
Broker: Broker B
Owner: Managing director
Currency: USD
Broker lead: 21 days
Change threshold: 10%
Documents supplied by: Operations lead, from Broker B's documents
```

### 2. The expiring schedules (from Broker B's documents)

```
SCHEDULE: COMMERCIAL GENERAL LIABILITY
Insurer: Insurer K
Policy number: GL-4471
Named insured: Business C
Period: 1 January 2026 to 1 January 2027
Each occurrence limit: $1,000,000
General aggregate limit: $2,000,000
Products-completed operations aggregate limit: $2,000,000
Deductible, each claim: $2,500
Endorsement: Blanket additional insured where required by written
  contract
Annual premium: $9,400
```

```
SCHEDULE: COMMERCIAL PROPERTY
Insurer: Insurer M
Policy number: PR-2290
Named insured: Business C
Period: 1 January 2026 to 1 January 2027
Premises: Location 1, the main yard and workshop
Contents limit: $350,000
Tools and equipment limit: $120,000
Business income limit: $250,000
Deductible, each loss: $1,000
Annual premium: $3,150
```

```
SCHEDULE: WORKERS COMPENSATION AND EMPLOYERS LIABILITY
Insurer: Insurer N
Policy number: WC-8812
Named insured: Business C
Period: 1 January 2026 to 1 January 2027
Workers compensation: statutory
Employers liability, each accident: $500,000
Employers liability, disease each employee: $500,000
Annual premium, estimated: $38,000
```

```
SCHEDULE: COMMERCIAL AUTO
Insurer: Insurer K
Policy number: CA-3305
Named insured: Business C
Period: 15 March 2026 to 15 March 2027
Vehicles scheduled: 9 vans
Combined single limit, each accident: $1,000,000
Physical damage deductible, each vehicle: $1,000
Annual premium: $14,600
```

### 3. The renewal terms (Broker B's renewal summary, 3 November 2026)

```
RENEWAL TERMS: COMMERCIAL GENERAL LIABILITY
Insurer: Insurer K
Policy number: GL-4471
Period: 1 January 2027 to 1 January 2028
Each occurrence limit: $1,000,000
General aggregate limit: $2,000,000
Products-completed operations aggregate limit: $2,000,000
Deductible, each claim: $5,000
Endorsement: Blanket additional insured where required by written
  contract
Exclusion: Fungi or bacteria exclusion
Annual premium: $11,280
```

```
RENEWAL TERMS: COMMERCIAL PROPERTY
Insurer: Insurer M
Policy number: PR-2290
Period: 1 January 2027 to 1 January 2028
Premises: Location 1, the main yard and workshop
Contents limit: $350,000
Tools and equipment limit: $120,000
Business income limit: $250,000
Deductible, each loss: $1,000
Annual premium: $3,465
```

```
RENEWAL TERMS: WORKERS COMPENSATION AND EMPLOYERS LIABILITY
Insurer: Insurer N
Policy number: WC-8812
Period: 1 January 2027 to 1 January 2028
Workers compensation: statutory
Employers liability, each accident: $1,000,000
Employers liability, disease each employee: $500,000
Annual premium, estimated: $41,800
```

### 4. Business changes (typed by the operations lead)

```
measure,at_last_renewal,now,now_from,given_to_insurer,given_in
employees,38,46,payroll system headcount,46,renewal application
annual revenue,4600000,5400000,accounts for the last 12 months,5000000,renewal application
annual payroll,1900000,2300000,payroll for the last 12 months,2050000,renewal application
sites,1,2,lease register,1,renewal application
vehicles,9,12,fleet list,,
```

```
Other changes:
- Since June 2026 the business cleans gutters and repairs roofs on
  two-storey buildings, working at height from ladders and towers.
```

### 5. New contracts that ask for cover

```
contract,signed,line,item,figure_asked_for,other_requirement,read_by
Customer P facilities maintenance agreement,2026-04-14,Commercial general liability,Each occurrence limit,2000000,Customer P named as additional insured,Operations director
Customer Q reactive repairs agreement,2026-07-01,Commercial auto,"Combined single limit, each accident",1000000,,Operations director
```

### 6. Claims history (Broker B's loss run, dated 31 October 2026, policy years 2024 to 2026)

```
line,policy_year,date_of_loss,claim_number,status,paid,reserved,description
Commercial general liability,2024,2024-06-11,K-GL-1182,closed,6200,0,Customer's floor damaged during a repair
Commercial auto,2025,2025-09-03,K-CA-2040,closed,3850,0,Van reversed into a gate post at a customer site
Workers compensation,2026,2026-02-17,N-WC-5521,closed,4300,0,"Technician Person E, back strain lifting a boiler"
Commercial general liability,2026,2026-08-21,K-GL-1307,open,1200,15000,Visitor tripped over a cable at a customer site
```

### 7. The business's own record of claims and incidents

```
date_of_loss,line,claim_number,description
2024-06-11,Commercial general liability,K-GL-1182,Floor damaged at a customer's office
2025-09-03,Commercial auto,K-CA-2040,Van hit a gate post
2026-02-17,Workers compensation,N-WC-5521,Lifting injury
2026-08-21,Commercial general liability,K-GL-1307,Visitor trip at a customer site
2026-10-02,Commercial property,,Break-in at the yard; two power tools taken
```

### 8. The managing director's own question

```
- Can the premiums be paid in instalments, and would that cost more?
```

## The output

**BUSINESS INSURANCE RENEWAL PACK: Business C, renewing Friday 1 January 2027**

For: Operations lead. Decided by: Managing director, with Broker B. Prepared Tuesday 10 November 2026 from the renewal facts, 4 expiring schedules, renewal terms for 3 policies (Broker B's renewal summary of 3 November 2026), the business changes table (5 rows) and 1 other change, the new contracts table (2 rows), the loss run (4 rows), the business's own record (5 rows) and 1 question from the managing director.

**DATES**

- **Renewal date:** Friday 1 January 2027, 52 days from today.
- **Questions to the broker by:** Friday 11 December 2026, 31 days from today (21 days before the renewal date).
- **Status:** ON TRACK.
- **Policies ending on another date:** Commercial auto, Insurer K, ends Monday 15 March 2027, 125 days from today.

**THE POLICIES: 4 expiring, 3 with renewal terms supplied**

1. **Commercial general liability.** Insurer: Insurer K → Insurer K (SAME). Policy GL-4471. Period: 1 January 2026 to 1 January 2027 → 1 January 2027 to 1 January 2028 (starts the day the expiring period ends).
   - Each occurrence limit: \$1,000,000 → \$1,000,000. SAME
   - General aggregate limit: \$2,000,000 → \$2,000,000. SAME
   - Products-completed operations aggregate limit: \$2,000,000 → \$2,000,000. SAME
   - Deductible, each claim: \$2,500 → \$5,000. CHANGED, +\$2,500 (+100.0%)
   - Endorsement, Blanket additional insured where required by written contract: listed → listed. SAME
   - Exclusion, Fungi or bacteria exclusion: none → listed. NEW
   - Premium: \$9,400 → \$11,280. CHANGED, +\$1,880 (+20.0%)
   - Changes marked: 3.
2. **Commercial property.** Insurer: Insurer M → Insurer M (SAME). Policy PR-2290. Period: 1 January 2026 to 1 January 2027 → 1 January 2027 to 1 January 2028 (starts the day the expiring period ends).
   - Premises: Location 1, the main yard and workshop → Location 1, the main yard and workshop. SAME
   - Contents limit: \$350,000 → \$350,000. SAME
   - Tools and equipment limit: \$120,000 → \$120,000. SAME
   - Business income limit: \$250,000 → \$250,000. SAME
   - Deductible, each loss: \$1,000 → \$1,000. SAME
   - Premium: \$3,150 → \$3,465. CHANGED, +\$315 (+10.0%)
   - Changes marked: 1.
3. **Workers compensation and employers liability.** Insurer: Insurer N → Insurer N (SAME). Policy WC-8812. Period: 1 January 2026 to 1 January 2027 → 1 January 2027 to 1 January 2028 (starts the day the expiring period ends).
   - Workers compensation: statutory → statutory. SAME
   - Employers liability, each accident: \$500,000 → \$1,000,000. CHANGED, +\$500,000 (+100.0%)
   - Employers liability, disease each employee: \$500,000 → \$500,000. SAME
   - Premium (annual premium, estimated): \$38,000 → \$41,800. CHANGED, +\$3,800 (+10.0%)
   - Changes marked: 2.
4. **Commercial auto.** Insurer: Insurer K. Policy CA-3305. Period: 15 March 2026 to 15 March 2027. Renewal terms not supplied.
   - Vehicles scheduled: 9 vans.
   - Combined single limit, each accident: \$1,000,000.
   - Physical damage deductible, each vehicle: \$1,000.
   - Premium: \$14,600.

Expiring premiums: \$65,150, 4 policies. For the 3 policies with renewal terms: expiring \$50,550, renewal \$56,545, +\$5,995 (+11.9%).

**WHAT CHANGED IN THE BUSINESS**

- **Employees:** 38 → 46 (from the payroll system headcount), +8 (+21.1%). Given to the insurer: 46, in the renewal application (equals the figure now).
- **Annual revenue:** \$4,600,000 → \$5,400,000 (from the accounts for the last 12 months), +\$800,000 (+17.4%). Given to the insurer: \$5,000,000, in the renewal application (differs by \$400,000).
- **Annual payroll:** \$1,900,000 → \$2,300,000 (from the payroll for the last 12 months), +\$400,000 (+21.1%). Given to the insurer: \$2,050,000, in the renewal application (differs by \$250,000).
- **Sites:** 1 → 2 (from the lease register), +1 (+100.0%). Given to the insurer: 1, in the renewal application (differs by 1).
- **Vehicles:** 9 → 12 (from the fleet list), +3 (+33.3%). Given to the insurer: not supplied.
- **Other changes:** Since June 2026 the business cleans gutters and repairs roofs on two-storey buildings, working at height from ladders and towers.

**NEW CONTRACTS THAT ASK FOR COVER**

- **Customer P facilities maintenance agreement,** signed 14 April 2026, as read by the operations director: asks for each occurrence limit of \$2,000,000 on commercial general liability; the renewal schedule prints \$1,000,000, so the figure asked for is higher than the figure printed. Other requirement: Customer P named as additional insured. Whether the request is met is for Broker B to confirm.
- **Customer Q reactive repairs agreement,** signed 1 July 2026, as read by the operations director: asks for combined single limit, each accident of \$1,000,000 on commercial auto; the expiring schedule prints \$1,000,000, so the figure asked for is equal to the figure printed. Other requirement: none. Whether the request is met is for Broker B to confirm.

**CLAIMS HISTORY: loss run dated 31 October 2026, policy years 2024 to 2026**

- **Commercial general liability:** 2 claims, 1 open. Paid \$7,400, reserved \$15,000, incurred \$22,400.
- **Commercial auto:** 1 claim, 0 open. Paid \$3,850, reserved \$0, incurred \$3,850.
- **Workers compensation:** 1 claim, 0 open. Paid \$4,300, reserved \$0, incurred \$4,300.
- **All lines:** 4 claims, 1 open. Paid \$15,550, reserved \$15,000, incurred \$30,550.
- **Largest incurred:** K-GL-1307, commercial general liability, 21 August 2026, \$16,200, open.
- **Open claims:** K-GL-1307, commercial general liability, 21 August 2026, visitor tripped over a cable at a customer site, reserved \$15,000.
- **In the business's own record, not in the loss run:** 2 October 2026, commercial property, break-in at the yard; two power tools taken.

**QUESTIONS FOR THE BROKER: 15, for the operations lead to decide whether to send**

1. The renewal premiums rise on all three policies with terms: commercial general liability \$9,400 to \$11,280 (+20.0%), commercial property \$3,150 to \$3,465 (+10.0%), workers compensation and employers liability \$38,000 to \$41,800 (+10.0%). What is each increase based on?
2. The commercial general liability deductible goes from \$2,500 to \$5,000 each claim. What led to the change, and what would the renewal premium be with the deductible kept at \$2,500?
3. "Fungi or bacteria exclusion" is listed in the commercial general liability renewal terms and not on the expiring schedule. What does it change for Business C?
4. Employers liability, each accident, goes from \$500,000 to \$1,000,000. What led to the change, and how much of the premium change comes from it?
5. The commercial auto policy ends on Monday 15 March 2027, not on the renewal date, and no renewal terms were supplied for it. When will its renewal terms arrive, and how will its renewal be handled beside the other policies?
6. Annual revenue is \$5,400,000 for the last 12 months; the renewal application gave \$5,000,000. What, if anything, do the insurers need about the current figure, and by when?
7. Annual payroll is \$2,300,000 for the last 12 months; the renewal application gave \$2,050,000. What, if anything, do the insurers need about the current figure, and by when?
8. Business C has 2 sites; the renewal application gave 1, and the property schedule lists Location 1 only. What, if anything, do the insurers need about the second site, and by when?
9. Business C has 12 vehicles, up from 9 at the last renewal (+33.3%); the auto schedule lists 9 vans, and no vehicle figure given to the insurer was supplied. Has Insurer K been told about the other 3?
10. Since June 2026 Business C cleans gutters and repairs roofs on two-storey buildings, working at height from ladders and towers. Have the insurers been told, and does it change any terms?
11. Customer P's agreement, signed 14 April 2026, asks for a \$2,000,000 each occurrence limit on commercial general liability and for Customer P to be named as additional insured; the renewal schedule prints \$1,000,000 each occurrence. Does the renewal meet Customer P's request, and if not, what would it take and cost?
12. Customer Q's agreement, signed 1 July 2026, asks for a \$1,000,000 combined single limit, each accident, on commercial auto; the expiring auto schedule prints \$1,000,000. Does the auto policy meet Customer Q's request?
13. Claim K-GL-1307 of 21 August 2026 is open, with \$15,000 reserved. Where does it stand, and has the insurer taken it into account in the renewal terms?
14. The business's own record shows a break-in at the yard on 2 October 2026 with two power tools taken, which is not in the loss run dated 31 October 2026. Does Insurer M hold any record of it?
15. Can the premiums be paid in instalments, and would that cost more?

**DECISIONS FOR THE MANAGING DIRECTOR: 3**

1. Should questions 1 to 15 go to Broker B by Friday 11 December 2026, and who sends them?
2. Annual revenue (\$5,400,000), annual payroll (\$2,300,000) and sites (2) differ from the figures given to the insurer in the renewal application (\$5,000,000, \$2,050,000 and 1). No figure given to the insurer was supplied for vehicles (12 now). Who gives Broker B the current figures for annual revenue, annual payroll, sites and vehicles, and by when?
3. The renewal of commercial general liability, commercial property, and workers compensation and employers liability: \$56,545 in renewal premiums against \$50,550 expiring. Renew on the terms offered, ask Broker B for changes, or ask Broker B to look for other terms? To be decided with Broker B before Friday 1 January 2027.

**NOT SUPPLIED OR NOT CHECKED**

The policy wordings were not read or interpreted; nothing in this pack says whether any loss is or is not covered; figures are as printed on the schedules supplied by the operations lead. Renewal terms for commercial auto were not supplied. The workers compensation and employers liability schedule and its renewal terms show no deductible. No figure given to the insurer was supplied for vehicles.

Every figure traces to the documents and files supplied for Business C on 10 November 2026. Nothing has been sent, accepted, bound, paid, reported or changed.
