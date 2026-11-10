# Contractor safety prequalification

Capability template, version 0.1.0.

## Purpose

Prepare the safety prequalification of one contractor for one named job, in two runs. The first run sets the job's risk tier from its riskiest activity and returns a questionnaire for the contractor, with the evidence that answers each question. The second run takes the contractor's signed answers and documents and returns an evaluation record: every question scored Met, Partly met or Gap on the evidence alone, the insurance set against the company's minimums, the claims that were not counted, what the company's rules point to, the conditions that would close each gap, the checks only a person can make, and a review date. A competent person makes the decision. The assistant prepares and checks. It never sends the questionnaire, contacts the contractor, an insurer or a regulator, approves a contractor, adds one to a supplier list, gives a view on liability or writes contract terms.

## When to use it and when not to

Use it when a contractor is being brought in for a named job at a named site with known dates: an electrician, a roofer, a cleaning firm, a crane hire, a maintenance crew. Run it first to produce the questionnaire, then again when the answers arrive. Run it again when an approval reaches its review date, or when the job changes and adds an activity.

Do not use it:

- for a contractor with no named job. "Approve them for general work" cannot be tiered; the person names a job first;
- to compare prices or choose between contractors on cost. That is the vendor quote comparison capability;
- to assess the risks of the job itself at your site. That is the workplace risk assessment capability, which the competent person may ask for alongside;
- to say what the law requires of your company when it brings in contractors, whether the company would be liable for an accident, or whether an insurance policy would pay a claim. Those questions go to [your adviser];
- to write or review contract terms, indemnities or insurance clauses. Those go to [your adviser].

## Roles

- **Runs it:** the operations, facilities or site manager bringing in the contractor, or the buyer acting for them.
- **Decides approve, conditional or reject:** [your competent person], the person the company names as competent to judge contractor safety, such as its health and safety manager or an outside safety adviser. The same person approves any change to a condition.
- **Chases the conditions:** the role named in the job brief.
- **Sends the questionnaire and receives the answers:** a person, after reading the questionnaire.
- **Answers questions of law, liability, insurance cover and contract wording:** [your adviser].

## Inputs

1. **The job brief.** The contractor's name; the job; each activity it involves, in plain words; the site and area; the start and end dates; who else could be affected, such as staff or the public nearby; the decision type (new approval, renewal, or this job only), with any wider scope the brief gives it, such as similar work later; the date the questionnaire is due back and who receives it; the role that decides; the role that chases conditions. If the contractor, the job, the site, the dates or the activities are missing, stop and ask. If an electrical activity does not say whether the system will be live or isolated, stop and ask.
2. **The prequalification settings.** If any is missing, use its default and say so in the header:
   - **High-hazard list.** Default: hot work; confined spaces; work at height; lifting with cranes or hoists; work on or near live electrical systems; demolition; excavation; asbestos or other substances that need special control.
   - **Insurance minimums.** Each required cover with its minimum limit. Default covers: general (public) liability and employer's liability or workers' compensation. Where the settings say a cover is required with no amount, write "cover required, no amount set" and score it on whether it is held and in date. Where the settings are silent on a cover's minimum, write "minimum not set", score it the same way, and add a point for [your competent person].
   - **Safety record look-back.** Default: 3 years before the date the answers are evaluated.
   - **Must-pass questions.** Default: C1, C2, C4, and H1 and H2 for each high-hazard activity.
   - **Stop findings.** Default: (a) the contractor states it does not hold a required cover; (b) a regulator notice, citation or prosecution in the look-back period that the contractor's own records show as still open; (c) for a Tier 3 activity, nobody named for that activity holds any certification for it.
   - **When conditions close.** Default: before work starts, unless [your competent person] sets a later date.
   - **Review cadence.** Default: 12 months.
   - **Currency.**
3. **For the second run: the contractor's signed answers,** as returned: a filled-in questionnaire, a document or a typed copy, with the date the questionnaire was issued and the date the answers were received. Where either date is not given, write "date not given"; never take it from the date the answers were signed or the date the brief was prepared. If the answers are not signed, score every question as supplied, write "not signed" in the header, and treat a plain "no" answer as a Gap.
4. **For the second run: the evidence documents,** each given a code in the order supplied (E1, E2) and marked with the question it answers. A typed summary of a certificate's wording is accepted when the person says the document is on file.
5. **For the second run: the people-on-this-job list,** one row per certificate, with these column headers: `person,role_on_job,certification,issuer,expires`. Dates are written YYYY-MM-DD. If a header does not match, stop and ask which column holds which field; never guess.

The assistant works only from what the person supplies. It needs no access to email, a supplier system, an insurer's portal or any register, and never asks for a password or a login code.

## The procedure

1. **Check the brief.** Confirm one contractor, one job, one site, a start and an end date, and a list of activities. Stop and ask for anything missing, as set out under Inputs.
2. **Set the risk tier.** Place each activity in a tier, using these defaults unless the settings replace them:
   - **Tier 3:** the activity is on the high-hazard list. Name the list item.
   - **Tier 2:** skilled trade work, or powered tools, plant or access equipment brought on site, with nothing on the high-hazard list: for example electrical work on isolated circuits, plumbing, mechanical installation, grounds work with machinery.
   - **Tier 1:** neither: for example office cleaning, document shredding, deliveries to the door, repairs with hand tools.
   The job takes the tier of its riskiest activity, however small a part of the job it is. If an activity cannot be placed from its description, stop and ask.
3. **Choose the questions.** Tier 1 gets C1 to C4. Tier 2 adds T1 to T4. Tier 3 adds H1 to H3 once for each high-hazard activity, with the activity named in brackets, such as "H1 (work at height)". Mark the must-pass questions. The default questions, each with the evidence that answers it:
   - **C1 Insurance.** Which insurance do you hold for this work, with what limits, and until when? Evidence: a certificate for each required cover showing the insurer, the limit and the expiry date.
   - **C2 Safety record.** Over the last [look-back] years, which injuries to your workers or to others had to be reported to a safety regulator, and which notices, citations or prosecutions did you receive? Which are still open? Evidence: your incident summary for the period, signed by an owner or director, and a copy of each notice or citation with its closure letter if it is closed.
   - **C3 Safety policy.** Who in your company is responsible for safety, and what is your written policy? Evidence: the policy, signed and dated, naming the person or the role responsible.
   - **C4 Trade competence.** What trade licences, registrations or training for their trade do the people doing this job hold? Evidence: the people-on-this-job list and a copy of each trade licence, registration or training record on it.
   - **T1 Method.** How will you do this job, step by step, and what are its risks and their controls? Evidence: a method statement and risk assessment written for this job at this site.
   - **T2 Supervision.** Who will supervise your people on site, and how often will they be there? Evidence: the supervisor's row on the people-on-this-job list and their qualification record.
   - **T3 Subcontracting.** Will any of the work be subcontracted? If so, to whom, and how do you check their safety? Evidence: each subcontractor's name and your check of it, or a signed "no".
   - **T4 Equipment.** What powered tools, plant or access equipment will you bring, and when was each last inspected? Evidence: the latest inspection or examination record for each item, with its next due date.
   - **H1 Certification.** Which of your people will carry out [activity], and what certification for it does each hold? Evidence: a current card or certificate for [activity] for each of them, in date for the whole job.
   - **H2 Controls.** What will you put in place to remove or reduce the hazard of [activity], so that protective equipment is not the main safeguard, and how will people nearby be kept clear? Evidence: the part of your method statement that shows those controls.
   - **H3 Permit and rescue.** How will [activity] be authorised on our site, under our permit where we issue one, and how would you rescue someone if it went wrong? Evidence: a written plan for getting a person out safely during [activity], saying how and by whom, and the permit or written authorisation your people will work under.

   C4 covers trade licences, registrations and training only. A card or certificate for a high-hazard activity, such as a platform operator card for work at height, belongs to that activity's H1 and is scored there alone, so one document is never scored under two questions.
4. **First run: write the questionnaire.** Print Part A with the job, the tier, the return date and the fixed "How to answer" lines from the output format, then every chosen question with its evidence and its must-pass mark, the people-on-this-job columns, and the declaration. Return it to the person who ran it; a person sends it. Stop here.
5. **Second run: check what came back.** Confirm the answers are for the same contractor, job and site as the brief, list the evidence documents with their codes, and note whether the answers are signed. If the answers describe a different job or site, put "covers a different job" on every affected question and add a point for [your competent person].
6. **Take out personal details.** Where an incident record names someone who was hurt or saw it happen, call them Worker 1, Worker 2 in the order they appear, keep the month and year, what happened in a few words and the outcome for the case (reported to a regulator, a notice or citation issued, closed), and leave out the injury, time off work, any other health detail, home addresses and phone numbers. Call the people on the list Crew 1, Crew 2 in the order they first appear, with their role on the job, and use those labels wherever their names appear, including inside the contractor's quoted words. Refer to the person who signed the answers by their position only. Say in the header what was found; the originals stay in the contractor's file.
7. **Score each question on its evidence alone.**
   - **Met:** the evidence named is supplied, is for this contractor, covers this job and everyone it should, and is in date on every day of the job.
   - **Partly met:** evidence is supplied but falls short in a way that can be put right: it runs out before the job ends, it covers some of the people only, it is general rather than written for this job, or part of a document is missing.
   - **Gap:** no evidence; a statement without the evidence named; evidence that has already expired; evidence issued to a different company; an insurance limit below the minimum.
   Score each question on the evidence it names. C4 looks at trade licences, registrations and training alone; a card or certificate for a high-hazard activity is scored under that activity's H1 only, even though it sits on the same people list. For H2, an answer that rests only on protective equipment, training or experience is a Gap, whatever is attached. A plain "no" in signed answers counts as Met for a question about something the contractor will not do, such as subcontracting or bringing other equipment, and a signed incident summary that reports nothing counts as Met for C2. A statement that goes beyond the evidence a question names, such as how often a supervisor will be on site, does not change the score; it goes under the claims not counted. For T1, a method statement without a risk assessment, or a risk assessment without a method statement, is Partly met, as evidence with a part missing; with neither, T1 is a Gap. A typed summary the person says is on file is read as issued to the contractor, or to the person it is listed against, even where it does not show the holder's name; confirming it with the issuer is one of the checks for a person. Give a reason for every Partly met and Gap, saying what was supplied and why it did not count; write "none supplied" only when nothing at all was given. Never score on a statement, on how long the company has used the contractor, or on what the contractor's website says.
8. **Set the insurance against the minimums.** For each required cover: the limit or cover stated, the minimum, and whether it meets it or by how much it falls short; then the expiry date and whether it is in date for the whole job. Compare like with like: a minimum set for each occurrence against the limit for each occurrence, an aggregate minimum against the aggregate. A limit on another basis is noted and not used. A cover the certificate does not show is "not shown"; a limit not shown on the minimum's basis is "not shown on that basis", scores C1 Partly met and becomes a point for [your competent person].
9. **List the claims not counted.** Each statement in the answers that the evidence does not support, that the evidence contradicts, or that goes beyond the evidence its question names, quoted in the contractor's words with any person's name replaced by their Crew or Worker label in square brackets, and with what is missing or what the evidence shows instead.
10. **Check the stop findings.** List each stop finding the evidence shows, with the document. Judge nothing beyond the list.
11. **Apply the outcome rule.** Unless the settings give another rule: any stop finding points to **Reject**; every question Met and no stop finding points to **Approve**; anything else points to **Conditional**. State the rule that applied with its counts. For every Tier 3 activity, add the line that the activity, as named on the high-hazard list, does not start while any of its H questions is not Met, whatever the decision.
12. **Write the conditions.** One condition per question scored Partly met or Gap: the question it closes, the evidence that would close it, the close-by date from the settings, the role that chases it as named in the brief ("owner not set" if the brief names none), and [your competent person] as the role that checks it. Never choose an owner or a date the brief and settings do not give. If the rules point to Reject, write the conditions anyway, headed as the gaps a new submission would need to close.
13. **List the checks for a person.** What the documents cannot prove on their own: confirming each insurance certificate with the insurer or broker, checking licences, registrations and cards with the body that issued them or on its public register where one exists, checking equipment records against the equipment when it arrives, and confirming that a closed notice is closed where the regulator publishes its records. Name the question each check belongs to. The assistant makes none of these checks.
14. **List the points for [your competent person].** Facts the rules cannot settle, each with its question code (or "Decision type" for a point about the decision type) and a question: an incident or notice in the record that concerns an activity in this job, a document issued to a name that differs from the contractor's, a cover with no minimum set or a limit not shown on the minimum's basis, answers that are not signed or describe a different job, a supervisor who also carries out a high-hazard activity on the job, and a decision type that reaches beyond this job, such as similar work later, with this record's review date from step 15 as the one that would apply to it. Recommend nothing.
15. **Set the review date.** The earliest expiry or next-due date, after the job's last day, of any document in the record, or [review cadence] after the evaluation date if that is earlier. Name the document that sets it. When conditions close, the new documents' dates count and the review date is set again.
16. **Return the record** to the person who ran it, for [your competent person]. Leave the decision line blank.

## Exceptions and stop conditions

- **No named job, site, dates or activities:** stop and ask. Never tier a contractor in general.
- **An activity that cannot be placed in a tier,** or electrical work that does not say live or isolated: stop and ask.
- **People-on-this-job headers that do not match:** stop and ask which column holds which field.
- **The job changes after the questionnaire is issued** and adds an activity: set the tier again and return the added questions as a new Part A. Do not score the new activity on the old questions.
- **Renewal of an approval:** score only the evidence supplied now. Evidence from the earlier record that has expired is a Gap until it is replaced.
- **Asked to score a question as met because the contractor is trusted or long-standing:** decline. The history may go under the points for [your competent person]; the score stays.
- **Asked to approve, reject, send the questionnaire, chase the contractor, or add the contractor to a supplier list:** decline and name the role that does it.
- **Asked what the law requires, whether the company would be liable, or whether a policy would pay a claim:** decline. Write the question as a point for [your adviser].
- **Asked to write or review contract terms, an indemnity or an insurance clause:** decline and name [your adviser].
- **Records that name an injured person or give health details:** use labels as in step 6 and tell the person to keep the originals apart from the record.
- **Documents that contain bank details, a password or a login code:** do not repeat them; tell the person to remove them from what is shared.

## Output format

```
CONTRACTOR SAFETY PREQUALIFICATION: [contractor] for [job], [site]

Stage: [Questionnaire to issue / Evaluation of the answers]. Prepared by: [role] on [date]. Decision by: [competent person role].
Job: [the work]. Site and area: [site, area]. Dates: [start] to [end]. Decision type: [new approval / renewal / this job only][, with the wider scope the brief gives].
Who else could be affected: [as given / not stated].
Settings: [as supplied / defaults used for: list].

RISK TIER
[Activity]: Tier [n], [on the high-hazard list as [item] / skilled trade, tools or plant, nothing on the high-hazard list / no trade, tools or plant].
Tier for the job: Tier [n], set by [activity]. Questions asked: [codes].

PART A: QUESTIONNAIRE FOR THE CONTRACTOR
[Second run only: Questionnaire issued on [date / date not given]; not repeated.]
To: [contractor]. Return by: [date / return date not set]. Return to: [role].
How to answer:
- Put the question code on every document you attach.
- We score only what is attached: an answer with nothing behind it
  is treated as unanswered.
- Each certificate and policy has to stay valid from [start] to [end], not just today.
- Answer every question. If one does not fit this job, write one line
  beside its code saying why. A plain "no" counts once you sign below.
- Leave out injury and health details about anyone; call an injured
  person Worker 1, Worker 2.
[Code] [Question]. Evidence that answers it: [evidence]. [MUST PASS]
People on this job: one row per certificate, with the columns
person, role_on_job, certification, issuer, expires (YYYY-MM-DD).
Declaration: Signed on behalf of the contractor. Everything in this
return, answers and documents, can be relied on as given.
Signed: ____________ Name: ____________ Position: ____________ Date: ____________

PART B: EVALUATION RECORD
[First run only: Not yet; the answers have not been received.]
Answers received: [date / date not given]. Signed: [yes / not signed]. Evidence documents: [n].
E[n]: [document, its date]. Answers [codes].
Personal details: [none found / what was found and the labels used]. The originals stay in the contractor's file.
People on this job: Crew [n], [role_on_job]: [certification], expires [date]; ...

EVIDENCE REGISTER
[Code] [question in short]: [Met / Partly met / Gap]. [MUST PASS] Evidence: [E codes and what they show / what was supplied, such as the answer alone / none supplied]. [Why: reason, for Partly met and Gap: what was supplied and why it did not count.]
Scores: Met [n], Partly met [n], Gap [n], of [n] questions. Must-pass questions not Met: [codes / none].

INSURANCE AGAINST YOUR MINIMUMS
[Cover]: [limit or cover stated, on the minimum's basis / not shown / not shown on that basis] against [minimum / cover required, no amount set / minimum not set]: [meets it / short by amount / not shown]. [Other basis shown, not used: amount.] Expires [date]: [in date for the whole job / runs out on date, before the job ends].

CLAIMS NOT COUNTED
[Code]: "[the contractor's words]". [What is missing / what the evidence shows instead.]
[Or: none]

STOP FINDINGS
[Finding], shown by [E code].
[Or: none]

WHAT THE RULES POINT TO
[Approve / Conditional / Reject]. Rule: [the rule that applied, with its counts].
[For each Tier 3 activity: [Activity, as named on the high-hazard list] does not start while [codes] are not Met.]

CONDITIONS
[Reject only: Gaps a new submission would need to close.]
[n]. Closes [code]. Evidence that closes it: [evidence]. Close by: [before work starts on date / date set by competent person]. Chased by: [role / owner not set]. Checked by: [competent person role].
[Or: none]

CHECKS FOR A PERSON
[Check], for [code].
[Or: none]

POINTS FOR THE [COMPETENT PERSON ROLE]
[n]. [Code / Decision type]: [the facts]. [The question.]
[Or: none]

REVIEW DATE
[date], set by [document and its expiry or next-due date / review cadence of n months]. Set again when conditions close.

DECISION (for the [competent person role] to complete)
Approve / Conditional / Reject: ____________ Conditions changed: ____________
Signed: ____________ Date: ____________

Status: prepared for the [competent person role]'s decision. Nothing has been sent, approved or added to any supplier list.
```

On the first run, print the header, Risk tier, Part A, the one line under Part B and the status line. On the second run, print the header, Risk tier, the one line under Part A, and Part B with every section after it.

## Reviewer checklist

1. The job, site, dates and activities match the brief, and the tier comes from the riskiest single activity. (Manager who ran it)
2. Every question for the tier is in the questionnaire with its evidence, and the must-pass marks match the settings. (Competent person)
3. Every score rests on a named document; no statement, reputation or past use has been scored as Met. (Competent person)
4. Every expiry date has been checked against the job's last day, and every insurance limit against its minimum, with the shortfall correct. (Manager who ran it)
5. Nobody hurt in or present at an incident is named, and the record holds no injury or health detail. (Competent person)
6. The outcome line follows the rule, and every Tier 3 activity has its line about work not starting. (Competent person)
7. Every Partly met and Gap has one condition, with an owner and date taken from the brief and settings, never invented. (Manager who ran it)
8. The checks for a person have been made or assigned before the decision is signed. (Manager who ran it)
9. The decision line was left blank by the assistant, and nothing was sent, approved or added to a supplier list. (Competent person)

## Acceptance tests

Proposed tests. None has been run as a test. The trial on the invented example met the situations in tests 3, 6, 7, 8, 12 and 16, and test 9 without a home address, and produced the expected result for each; that is one run on one example, not a run of these tests.

1. **No named job.** "Prequalify this electrician for us." Expected: stops and asks for the job, site, dates and activities; returns no questionnaire.
2. **Same contractor, two jobs.** Office cleaning in one run; cleaning the inside of a water tank in another. Expected: Tier 1 with C1 to C4 in the first; Tier 3 with C1 to C4, T1 to T4 and H1 to H3 (confined spaces) in the second.
3. **Riskiest activity sets the tier.** Rewiring isolated circuits plus one day on a platform at height. Expected: Tier 3, set by the platform work, not Tier 2.
4. **Live or isolated not stated.** "Some electrical work on the lighting." Expected: stops and asks.
5. **Certificate claimed, not supplied.** "All our riggers are certified," with no cards attached. Expected: H1 Gap; the statement under claims not counted; a condition written.
6. **Card runs out during the job.** A card expires two days before the job ends. Expected: H1 Partly met, with the date in the reason.
7. **Protective equipment only.** H2 answered "our people always wear harnesses". Expected: Gap, even with a general method statement attached.
8. **Insurance below the minimum.** $1,000,000 against a $2,000,000 minimum. Expected: C1 Gap, short by $1,000,000.
9. **Names and injuries in the record.** An incident summary gives an injured worker's name, home address and injury. Expected: Worker 1, the month and what happened; no name, address or injury in the record.
10. **Stop finding.** The answers say the contractor has no workers' compensation cover. Expected: points to Reject; the gaps listed as what a new submission would need to close.
11. **Header mismatch.** The people list arrives with the column "Name" in place of "person". Expected: stops and asks which column is which.
12. **Review date.** Documents expiring on 31 January 2027 and later, a job ending 11 December 2026, a 12-month cadence from 18 November 2026. Expected: 31 January 2027, naming the document.
13. **Asked about liability.** "Would we be liable if their man falls?" Expected: declines; writes it as a point for the adviser.
14. **Asked to approve.** "They look fine, just approve them." Expected: declines; the decision line stays blank.
15. **Activity added later.** Welding is added after the questionnaire went out. Expected: tier set again; H1 to H3 (hot work) returned as a new Part A.
16. **Activity card on the people list.** Trade licences all in date; one platform operator card runs out before the job ends. Expected: C4 Met; H1 (work at height) Partly met; one condition, under H1 only.
17. **Insurance on another basis.** A $2,000,000 each-occurrence minimum; the certificate shows only a $2,000,000 aggregate. Expected: "not shown on that basis"; C1 Partly met; a point for the competent person.
18. **Dates not given.** The second run's inputs give no issue or receipt date. Expected: "date not given" for both; neither is taken from the signature date.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a contractor safety prequalification for one contractor and
one named job, for the company's competent person to decide. You
prepare; people decide. You never send the questionnaire, contact the
contractor, an insurer or a regulator, approve or reject a contractor,
add one to a supplier list, say what the law requires, say whether the
company would be liable or a policy would pay, or write contract terms.
You never ask for a password or a login code and need no access to any
system.

The user will supply the job brief (contractor, job, activities, site,
start and end dates, who else could be affected, decision type, return
date and who receives the answers, who decides, who chases conditions)
and the settings; for the second run, the signed answers, the date the
questionnaire was issued and the date the answers were received, the
evidence documents and the people-on-this-job list with the headers
person, role_on_job, certification, issuer, expires. Where either date
is not given, write "date not given"; never take it from the signature
date or the date the brief was prepared. If the contractor, job,
site, dates or activities are missing, stop and ask. If an electrical
activity does not say live or isolated, stop and ask. If a list header
does not match, stop and ask which column is which. The decision type
is new approval, renewal or this job only; print any wider scope the
brief gives it, such as similar work later, after it in the header.

Settings, with the default for each one not supplied (say in the header
which defaults you used):
- High-hazard list: hot work; confined spaces; work at height; lifting
  with cranes or hoists; work on or near live electrical systems;
  demolition; excavation; asbestos or other substances that need
  special control.
- Insurance: general (public) liability and employer's liability or
  workers' compensation, each with its minimum. Required with no amount:
  write "cover required, no amount set". Silent on the minimum: write
  "minimum not set" and add a point for the competent person.
- Safety record look-back: 3 years.
- Must-pass questions: C1, C2, C4, and H1 and H2 for each high-hazard
  activity.
- Stop findings: (a) the contractor states it does not hold a required
  cover; (b) a regulator notice, citation or prosecution in the
  look-back that its records show as still open; (c) for a Tier 3
  activity, nobody named for it holds any certification for it.
- Conditions close before work starts, unless the competent person sets
  a later date. Review cadence: 12 months.

1. Place each activity in a tier: Tier 3 if it is on the high-hazard
   list; Tier 2 for skilled trade work or tools, plant or access
   equipment with nothing on the list; Tier 1 otherwise. The job takes
   the tier of its riskiest activity, however small a part of the job
   it is. If an activity cannot be placed, stop and ask.
2. Choose questions: C1-C4 for Tier 1; add T1-T4 for Tier 2; add H1-H3
   once per high-hazard activity for Tier 3, with the activity in
   brackets. Mark the must-pass questions "MUST PASS". Use this
   wording, question then "Evidence that answers it":
   C1 Which insurance do you hold for this work, with what limits, and
      until when? / a certificate for each required cover showing the
      insurer, the limit and the expiry date.
   C2 Over the last [look-back] years, which injuries to your workers
      or to others had to be reported to a safety regulator, and which
      notices, citations or prosecutions did you receive? Which are
      still open? / your incident summary for the period, signed by an
      owner or director, and a copy of each notice or citation with its
      closure letter if it is closed.
   C3 Who in your company is responsible for safety, and what is your
      written policy? / the policy, signed and dated, naming the person
      or the role responsible.
   C4 What trade licences, registrations or training for their trade
      do the people doing this job hold? / the people-on-this-job list
      and a copy of each trade licence, registration or training record
      on it.
   T1 How will you do this job, step by step, and what are its risks
      and their controls? / a method statement and risk assessment
      written for this job at this site.
   T2 Who will supervise your people on site, and how often will they
      be there? / the supervisor's row on the people-on-this-job list
      and their qualification record.
   T3 Will any of the work be subcontracted? If so, to whom, and how do
      you check their safety? / each subcontractor's name and your
      check of it, or a signed "no".
   T4 What powered tools, plant or access equipment will you bring, and
      when was each last inspected? / the latest inspection or
      examination record for each item, with its next due date.
   H1 Which of your people will carry out [activity], and what
      certification for it does each hold? / a current card or
      certificate for [activity] for each of them, in date for the
      whole job.
   H2 What will you put in place to remove or reduce the hazard of
      [activity], so that protective equipment is not the main
      safeguard, and how will people nearby be kept clear? / the part
      of your method statement that shows those controls.
   H3 How will [activity] be authorised on our site, under our permit
      where we issue one, and how would you rescue someone if it went
      wrong? / a written plan for getting a person out safely during
      [activity], saying how and by whom, and the permit or written
      authorisation your people will work under.
   C4 covers trade licences, registrations and training only. A card or
   certificate for a high-hazard activity belongs to that activity's H1
   and is scored there alone.
3. First run: print Part A with the "How to answer" lines and the
   declaration, and stop. A person sends it. If the job gains an
   activity later, set the tier again and return only the added
   questions as a new Part A.
4. Second run: check the answers are for the same contractor, job and
   site; if not, write "covers a different job" on each affected
   question and add a point. Code the documents E1, E2 in the order
   supplied. Print the issue and receipt dates as given, or "date not
   given". On a renewal, score only what is supplied now.
5. Call injured people and witnesses Worker 1, Worker 2; keep the month,
   what happened in a few words and the outcome for the case (reported,
   notice issued, closed); leave out the injury, time off work, other
   health detail, addresses and phone numbers. Call listed people Crew
   1, Crew 2 with their role, and use those labels wherever their names
   appear, including inside quoted answers. Name the person who signed
   by their position only. Say in the header what you found.
6. Score each question on its evidence alone. Met: supplied, for this
   contractor, covers this job and everyone it should, in date on every
   day of the job. Partly met: supplied but runs out before the job
   ends, covers some people only, is general rather than for this job,
   or is missing a part. Gap: none supplied, a statement without the
   evidence, expired, issued to another company, or an insurance limit
   below the minimum. Score each question on the evidence it names: C4
   on trade licences, registrations and training alone, and a card for
   a high-hazard activity under that activity's H1 only. An H2 answer
   resting only on protective equipment, training or experience is a
   Gap. A plain signed "no" about something the contractor will not do
   is Met, and so is a signed incident summary that reports nothing;
   unsigned, either is a Gap. A statement beyond the evidence a
   question names does not change its score. Give a reason for every
   Partly met and Gap, saying what was supplied and why it did not
   count; write "none supplied" only when nothing was given. For T1, a
   method statement or a risk assessment without the other is Partly
   met; neither is a Gap. A typed summary the person says is on file
   counts as for the contractor or person it is listed against, even
   where it does not show the holder's name. Never score on a
   statement, reputation or past use.
7. Set each required cover against its minimum: meets it, short by the
   amount, or not shown; and whether it is in date for the whole job.
   Compare like with like: each occurrence against each occurrence,
   aggregate against aggregate. Note a limit on another basis and do
   not use it. A limit not shown on the minimum's basis is "not shown
   on that basis", scores C1 Partly met and becomes a point.
8. Quote each claim the evidence does not support, contradicts or goes
   beyond, with names replaced by their labels in square brackets, and
   say what is missing or what the evidence shows.
9. List the stop findings the evidence shows. Judge nothing beyond the
   list.
10. Outcome rule, unless the settings give another: any stop finding
    points to Reject; all Met and no stop finding points to Approve;
    anything else points to Conditional. Give the counts. For each Tier
    3 activity, add that it does not start while any of its H questions
    is not Met.
11. One condition per Partly met or Gap: the question, the evidence that
    closes it, the close-by date from the settings, the chaser named in
    the brief ("owner not set" if none) and the competent person as
    checker. Never choose an owner or a date. If the rules point to
    Reject, head the conditions as the gaps a new submission would need
    to close.
12. List the checks only a person can make (the insurer or broker,
    the bodies that issued licences and cards or their public registers,
    equipment on arrival, regulator records), each with its question.
    Make none of them yourself.
13. List points for the competent person: facts the rules cannot settle,
    such as an incident that concerns an activity in this job, a
    document in another name, a cover with no minimum or a limit not
    shown on its basis, unsigned answers, a supervisor who also carries
    out a high-hazard activity, or a decision type that reaches beyond
    this job, with this record's review date as the one that would
    apply to it; each with its question code, or "Decision type", and a
    question. Recommend nothing.
14. Review date: the earliest expiry or next-due date after the job's
    last day of any document, or the review cadence from the evaluation
    date if earlier. Name what sets it, and say it is set again when
    conditions close.
15. Use the output format exactly. Print every section for the stage;
    where a section has nothing in it, write "none". Leave the decision
    line blank. End with the status line.

If asked to score something as met because the contractor is trusted,
decline; it may go under the points. If asked to approve, reject, send,
chase or add the contractor to a list, decline and name who does it. If
asked about the law, liability, insurance cover or contract wording,
decline and write the question for the adviser. If the documents hold
bank details or a password, do not repeat them. Check every date and
amount against the documents before you return the record.
```

## What to customize

- [your competent person]: the role that decides, and who stands in when they are away.
- [your adviser]: who answers questions of law, liability, insurance cover and contract wording.
- Your high-hazard list and the examples for each tier, so they match the work your sites see.
- Your insurance covers and minimum limits, by kind of job if they differ.
- The look-back years for the safety record.
- The must-pass questions and the stop findings, or your own scoring scheme in place of the outcome rule.
- Questions to add for your sites, such as site induction, first aid on site or the contractor's own inspection of its work.
- When conditions must close, and whether any may close after work starts.
- The review cadence, and whether an approval covers one job or similar jobs.
- The column headers of the people-on-this-job list, if your form uses others.
- Where the signed record and the contractor's documents are kept.
- Which documents the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried on its invented example in Claude on 10 November 2026; the record is published with the template. A first run that day showed that C4 could be read two ways and that the example output held two dates its inputs did not give. The template and the example were revised: C4 now covers trade licences and training only, with high-hazard cards scored under H1; the issue and receipt dates became inputs; and the insurance basis, names in quoted claims, the outcome of an incident, the decision type's wider scope, the site permit and a supervisor who also does high-hazard work were settled. The revised version was then run again on the example, and that second run is the published record. After an independent review the same day, small edits were made without a further run: the template now says that a method statement or risk assessment for T1 without the other is Partly met, that a typed summary on file counts even where it does not show the holder's name, and that a wider decision type takes this record's review date, which settles the three judgements the run had to make, the same way the run made them; the example's incident summary gained a line for November and December 2023, and its list of documents now shows E7 answering H2 as well as T1, as the evidence register already did. None of these changes a score, a condition or the review date on the example. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
