# Academic calendar check: tried once on its example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs were the invented example in [example.md](example.md): the settings, the structure, the date proposals and the closed days for the invented College's 2027-28 year. No client data was used. The assistant that ran the template did not write it. It was given the template's instruction block and output format and the example's inputs, and it was kept away from the example's published draft until its own draft was finished. One slip in that: while opening the example file it also displayed the first lines of the published draft, which include the header counts (24 proposals placed, 1 for a unit not in the structure, 11 findings). Those counts were not used to build the draft, but the reader should know they were seen first.

## What came out

```
ACADEMIC CALENDAR CHECK: the College, academic year 2027-28

For: the Registrar. Prepared: Tuesday 2026-11-10, from the structure (6 units), the date proposals (25 rows), the closed days (3 rows) and the settings.
Column check: all headers matched.
Proposals placed on the calendar: 24. Proposals for units not in the structure: 1. Findings: 11.

DRAFT CALENDAR

Y28 Academic year 2027-28 (year): Monday 2027-08-30 to Friday 2028-05-05 (P01).
  Parent: none (a year has none).
  Registration window: not required for a year
  Add/drop deadline: not required for a year
  Withdrawal deadline: not required for a year
  Exam period: not required for a year
  Grades due: not required for a year

A28 Autumn term 2027 (term): Monday 2027-08-30 to Friday 2027-12-17 (P02). See F10.
  Parent: Y28 Academic year 2027-28, Monday 2027-08-30 to Friday 2028-05-05. Within the parent.
  Registration window: Monday 2027-04-12 to Friday 2027-08-27 (P03)
  Add/drop deadline: Friday 2027-09-10 (P04)
  Withdrawal deadline: Friday 2027-11-05 (P05)
  Exam period: Monday 2027-12-13 to Friday 2027-12-17 (P06)
  Grades due: Friday 2027-12-24 (P07). See F10.

A28-1 Autumn first session (session): Monday 2027-08-30 to Friday 2027-10-22 (P08). See F9.
  Parent: A28 Autumn term 2027, Monday 2027-08-30 to Friday 2027-12-17. Within the parent.
  Registration window: not required for a session
  Add/drop deadline: Friday 2027-09-03 (P09)
  Withdrawal deadline: Friday 2027-10-01 (P10)
  Exam period: not required for a session
  Grades due: Wednesday 2027-10-27 (P11)

A28-2 Autumn second session (session): Monday 2027-10-18 to Monday 2027-12-20 (P12). See F6, F9.
  Parent: A28 Autumn term 2027, Monday 2027-08-30 to Friday 2027-12-17. OUTSIDE the parent, see F6.
  Registration window: not required for a session
  Add/drop deadline: Tuesday 2027-11-30 (P13). See F8.
  Withdrawal deadline: Wednesday 2027-11-24 (P14). See F8.
  Exam period: not required for a session
  Grades due: Wednesday 2027-12-22 (P15)

S28 Spring term 2028 (term): Monday 2028-01-10 to Friday 2028-05-05 (P16).
  Parent: Y28 Academic year 2027-28, Monday 2027-08-30 to Friday 2028-05-05. Within the parent.
  Registration window: Monday 2027-11-01 to Friday 2028-01-07 (P17)
  Add/drop deadline: Saturday 2028-01-22 (P18). See F11.
  Withdrawal deadline: CONFLICT, no date chosen: Friday 2028-03-17 (P19, version 1, Registrar's office) against Friday 2028-03-31 (P20, version 2, Academic senate), see F3. Not checked against the other dates.
  Exam period: Monday 2028-05-01 to Tuesday 2028-05-09 (P21). See F7.
  Grades due: not supplied, see F4

Units with no parent in the structure

WI28 Winter intensive session (session): Monday 2028-01-03 to Friday 2028-01-14 (P22). See F1, F5.
  Parent: none in the structure. Not checked against a parent.
  Registration window: not required for a session
  Add/drop deadline: Tuesday 2028-01-04 (P23)
  Withdrawal deadline: Monday 2028-01-10 (P24)
  Exam period: not required for a session
  Grades due: not supplied, see F5

Proposals for units not in the structure
P25 SU28: unit_span, Monday 2028-06-05 to Friday 2028-07-28, version 1, Academic senate. Not placed on the calendar. See F2.

FINDINGS FOR THE REGISTRAR

Structure
F1. WI28 Winter intensive session is a session with no parent in the structure. Which term or year does it belong to?
F2. P25 proposes dates for SU28, which is not in the structure ("summer term not yet in the structure"). Is SU28 to be added to the structure, and under which year?

Conflicting versions
F3. S28 Spring term 2028, withdrawal deadline: two versions. P19, version 1, Registrar's office: Friday 2028-03-17. P20, version 2, Academic senate: Friday 2028-03-31 (note: "senate asks for two more weeks"). Which date stands?

Missing dates
F4. S28 Spring term 2028: grades due not supplied. Which office supplies it, and what is the date?
F5. WI28 Winter intensive session: grades due not supplied. Which office supplies it, and what is the date?

Outside the parent or the unit
F6. A28-2 Autumn second session, unit span: ends Monday 2027-12-20; the parent A28 ends Friday 2027-12-17. 3 calendar days outside the parent. Is the session meant to run past the term's last day, or should one of the two dates change?
F7. S28 Spring term 2028, exam period: ends Tuesday 2028-05-09; the term's own span ends Friday 2028-05-05. 4 calendar days outside the term. Which dates stand?

Wrong order
F8. A28-2 Autumn second session: the add/drop deadline, Tuesday 2027-11-30, is 6 days after the withdrawal deadline, Wednesday 2027-11-24. Which of the two dates is right?

Overlaps to confirm
F9. A28-1 Autumn first session (Monday 2027-08-30 to Friday 2027-10-22) and A28-2 Autumn second session (Monday 2027-10-18 to Monday 2027-12-20), both under A28 Autumn term 2027, share Monday 2027-10-18 to Friday 2027-10-22, 5 days. Is the overlap intended?

Non-working days
F10. A28 Autumn term 2027, grades due: Friday 2027-12-24 falls inside the closed days "Winter closure" (CL2, 2027-12-24 to 2028-01-02). Which date stands?
F11. S28 Spring term 2028, add/drop deadline: Saturday 2028-01-22 is a Saturday, a non-working weekday. Which date stands?

Also noted
No repeated rows were merged. No proposal is dated before today. No checked date falls on the closed days CL1 (Harvest recess) or CL3 (Spring recess); the two S28 withdrawal dates in conflict were not checked.

Draft for the Registrar's confirmation. No date has been chosen, and no record, notice or page has been changed, sent or published.
```

## What was observed

- Every required part was produced: the header with its three counts, the calendar for all six units, the unplaced proposal, the eight finding groups, "Also noted" and the closing line. The counts match the files: 6 units, 25 proposals, 3 closed-day rows, 24 placed, 1 not placed, 11 findings.
- Nothing in the instructions made the assistant stop. All headers matched, no id repeated, no date was unreadable, no student name appeared, and nobody asked it to choose, fill, publish or send.
- No date was chosen or supplied. The two competing Spring withdrawal dates are both shown, with the senate's later version not preferred. The two missing grades-due dates are marked "not supplied".
- Compared with the published example, the findings are the same eleven, in the same order, with the same facts and the same day counts (3, 4, 6 and 5). The differences are in form only:
  - The example writes weekdays as Mon, Tue and so on; this run wrote them in full. The format only says "weekday".
  - For the year, the example prints one line, "Other dates: not required for a year"; this run printed the five item lines each with "not required for a year", following the format as written.
  - This run added "See F10" to the Autumn term's own line and "See F5" to the winter session's line; the example does not. The format allows "See F[n]" on the unit line but does not say which findings belong there.
  - The example's conflict line ends "Not checked against the term, the order or non-working days"; this run wrote "Not checked against the other dates".
  - The example's questions for the order and non-working-day findings add "or is this order intended" and "or is the deadline met while the College is closed". This run asked one plain question each, as step 11 says. The example's extra clauses come close to offering options, and "while the College is closed" is an inference, since the files say only that CL2 is a closed-day range.
  - Wording of "Also noted": this run added that the two conflicting Spring withdrawal dates were left out of the closed-day check, which the example does not say.
- Facts not in the inputs: none in this run's draft. In the example's draft, the phrase "while the College is closed" in F10 goes slightly beyond what the files state. The weekdays and day counts in both drafts are derived from the dates, and the weekdays were computed with a small script rather than by hand.

## Where the instructions were ambiguous

- The output format says "[weekday date]" without saying whether to abbreviate the weekday.
- The format's unit line ends "[See F[n], ...]" but does not say whether that covers findings about the unit's other items (the Autumn term's late grades-due date) or only the unit's own span.
- The format has separate lines for registration, add/drop, withdrawal, exams and grades due, but a year needs none of them. It is unclear whether to print five "not required" lines or one.
- A conflicting item "takes no part in steps 6 to 10". The note to print on the calendar for that is not worded, so each run will word it differently. It is also unclear whether a conflicting date's closed-day rows should count as "no checked date falls on" in "Also noted".
- The proposals file's `note` column is not mentioned in the procedure. Whether to quote a note in a conflict finding, or on an unplaced proposal, is left to the assistant. This run quoted the senate's note in the conflict finding and the unknown-unit note in the structure finding.
- Step 11 says to recommend nothing, and ends each finding with one question; how much of an "or" alternative a question may carry is not said.
- The instruction block has twelve steps and the procedure fourteen; they agree in substance, but the numbering differs, which makes cross-checking harder.

## Shortcomings

- It was tried once, by one assistant, on one invented year. This does not show how it behaves with a real export, a renamed column, an unreadable date or a longer calendar; those acceptance tests were not run.
- Weekday and day-count arithmetic is the likeliest place for a slip; a person should check it, as the reviewer checklist says.

## Changes to the template after this run

This record is of the run described above, on the template's earlier wording; its output and observations are unchanged. After the independent review, the template was edited without a second run: it now says that weekdays are written as three letters, which "See F[n]" references go where, how a conflict's "not checked" line and a proposal's note are worded, that a finding's question is plain and offers no options, and what the defaults are for non-working weekdays, the confirming role, missing closed days and a missing today's date; the example now prints the year's five "not required" lines, names the item type on the unplaced proposal and asks plain questions. Further small edits followed, also without a second run: the note on an unplaced proposal is quoted in its finding (the example's F2 now does so, as this run's F2 already did); the conflict form in the output format carries the "Not checked against the term, the order or non-working days." sentence after "See F[n]."; a supplied but not required item is shown on the calendar; and a date in conflict, unreadable or not placed is not a "checked date" for the closed-day note. A person running the template again should expect the draft to follow those lines; that has not been tried.
