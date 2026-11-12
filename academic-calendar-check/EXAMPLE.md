# Academic calendar check: an invented example

*Illustrative example with invented data.* The college, the offices, the units and every date below are invented. The college is an invented small community college, called the College here, whose registrar is assembling the calendar for the 2027-28 year. The registrar asks for the check on Tuesday 10 November 2026. Offices are named by role. First come the inputs the registrar supplied, in full, then the draft the workflow template returned.

## The inputs

### 1. Settings (typed by the registrar)

```
Institution: the College
Academic year: 2027-28
Today: 2026-11-10
Non-working weekdays: Saturday, Sunday
Required dates: use the defaults
Rules: use the defaults
Confirms dates and overlaps: the Registrar
```

### 2. Structure

```
unit_id,unit_name,unit_type,parent_id
Y28,Academic year 2027-28,year,
A28,Autumn term 2027,term,Y28
S28,Spring term 2028,term,Y28
A28-1,Autumn first session,session,A28
A28-2,Autumn second session,session,A28
WI28,Winter intensive session,session,
```

### 3. Date proposals

```
proposal_id,unit_id,item_type,start_date,end_date,version,proposed_by,note
P01,Y28,unit_span,2027-08-30,2028-05-05,1,Academic senate,
P02,A28,unit_span,2027-08-30,2027-12-17,1,Academic senate,
P03,A28,registration,2027-04-12,2027-08-27,1,Registrar's office,
P04,A28,add_drop,2027-09-10,,1,Registrar's office,
P05,A28,withdrawal,2027-11-05,,1,Registrar's office,
P06,A28,exams,2027-12-13,2027-12-17,1,Academic senate,
P07,A28,grades_due,2027-12-24,,1,Registrar's office,
P08,A28-1,unit_span,2027-08-30,2027-10-22,1,Academic senate,
P09,A28-1,add_drop,2027-09-03,,1,Registrar's office,
P10,A28-1,withdrawal,2027-10-01,,1,Registrar's office,
P11,A28-1,grades_due,2027-10-27,,1,Registrar's office,
P12,A28-2,unit_span,2027-10-18,2027-12-20,1,Academic senate,
P13,A28-2,add_drop,2027-11-30,,1,Registrar's office,
P14,A28-2,withdrawal,2027-11-24,,1,Registrar's office,
P15,A28-2,grades_due,2027-12-22,,1,Registrar's office,
P16,S28,unit_span,2028-01-10,2028-05-05,1,Academic senate,
P17,S28,registration,2027-11-01,2028-01-07,1,Registrar's office,
P18,S28,add_drop,2028-01-22,,1,Registrar's office,
P19,S28,withdrawal,2028-03-17,,1,Registrar's office,
P20,S28,withdrawal,2028-03-31,,2,Academic senate,senate asks for two more weeks
P21,S28,exams,2028-05-01,2028-05-09,1,Academic senate,
P22,WI28,unit_span,2028-01-03,2028-01-14,1,Academic senate,
P23,WI28,add_drop,2028-01-04,,1,Registrar's office,
P24,WI28,withdrawal,2028-01-10,,1,Registrar's office,
P25,SU28,unit_span,2028-06-05,2028-07-28,1,Academic senate,summer term not yet in the structure
```

### 4. Closed days

```
closed_id,closed_name,start_date,end_date
CL1,Harvest recess,2027-11-25,2027-11-26
CL2,Winter closure,2027-12-24,2028-01-02
CL3,Spring recess,2028-03-20,2028-03-24
```

## The draft

```
ACADEMIC CALENDAR CHECK: the College, academic year 2027-28

For: the Registrar. Prepared: Tue 2026-11-10, from the structure (6 units), the date proposals (25 rows), the closed days (3 rows) and the settings.
Column check: all headers matched.
Proposals placed on the calendar: 24. Proposals for units not in the structure: 1. Findings: 11.

DRAFT CALENDAR

Y28 Academic year 2027-28 (year): Mon 2027-08-30 to Fri 2028-05-05 (P01).
  Parent: none (a year has none).
  Registration window: not required for a year.
  Add/drop deadline: not required for a year.
  Withdrawal deadline: not required for a year.
  Exam period: not required for a year.
  Grades due: not required for a year.

A28 Autumn term 2027 (term): Mon 2027-08-30 to Fri 2027-12-17 (P02).
  Parent: Y28 Academic year 2027-28, Mon 2027-08-30 to Fri 2028-05-05. Within the parent.
  Registration window: Mon 2027-04-12 to Fri 2027-08-27 (P03).
  Add/drop deadline: Fri 2027-09-10 (P04).
  Withdrawal deadline: Fri 2027-11-05 (P05).
  Exam period: Mon 2027-12-13 to Fri 2027-12-17 (P06).
  Grades due: Fri 2027-12-24 (P07). See F10.

A28-1 Autumn first session (session): Mon 2027-08-30 to Fri 2027-10-22 (P08). See F9.
  Parent: A28 Autumn term 2027, Mon 2027-08-30 to Fri 2027-12-17. Within the parent.
  Registration window: not required for a session.
  Add/drop deadline: Fri 2027-09-03 (P09).
  Withdrawal deadline: Fri 2027-10-01 (P10).
  Exam period: not required for a session.
  Grades due: Wed 2027-10-27 (P11).

A28-2 Autumn second session (session): Mon 2027-10-18 to Mon 2027-12-20 (P12). See F6, F9.
  Parent: A28 Autumn term 2027, Mon 2027-08-30 to Fri 2027-12-17. OUTSIDE the parent, see F6.
  Registration window: not required for a session.
  Add/drop deadline: Tue 2027-11-30 (P13). See F8.
  Withdrawal deadline: Wed 2027-11-24 (P14). See F8.
  Exam period: not required for a session.
  Grades due: Wed 2027-12-22 (P15).

S28 Spring term 2028 (term): Mon 2028-01-10 to Fri 2028-05-05 (P16).
  Parent: Y28 Academic year 2027-28, Mon 2027-08-30 to Fri 2028-05-05. Within the parent.
  Registration window: Mon 2027-11-01 to Fri 2028-01-07 (P17).
  Add/drop deadline: Sat 2028-01-22 (P18). See F11.
  Withdrawal deadline: CONFLICT, no date chosen: Fri 2028-03-17 (P19, version 1, Registrar's office) against Fri 2028-03-31 (P20, version 2, Academic senate). See F3. Not checked against the term, the order or non-working days.
  Exam period: Mon 2028-05-01 to Tue 2028-05-09 (P21). See F7.
  Grades due: not supplied, see F4.

Units with no parent in the structure

WI28 Winter intensive session (session): Mon 2028-01-03 to Fri 2028-01-14 (P22). See F1.
  Parent: none in the structure. Not checked against a parent.
  Registration window: not required for a session.
  Add/drop deadline: Tue 2028-01-04 (P23).
  Withdrawal deadline: Mon 2028-01-10 (P24).
  Exam period: not required for a session.
  Grades due: not supplied, see F5.

Proposals for units not in the structure

P25 SU28: unit_span, Mon 2028-06-05 to Fri 2028-07-28, version 1, Academic senate. Not placed on the calendar. See F2.

FINDINGS FOR THE REGISTRAR

Structure
F1. WI28 Winter intensive session has no parent in the structure, so it is not placed under a year or term and its dates are not checked against one. Which term or year does it belong to?
F2. Proposal P25 names the unit SU28, which is not in the structure ("summer term not yet in the structure"). Its dates are shown and not placed. Is SU28 a unit to add to the structure, and under which year or term?

Conflicting versions
F3. S28 Spring term 2028, withdrawal deadline: P19 (version 1, Registrar's office) says Fri 2028-03-17 and P20 (version 2, Academic senate) says Fri 2028-03-31, with the note "senate asks for two more weeks". Which date stands?

Missing dates
F4. S28 Spring term 2028: grades due not supplied. Which office supplies it, and what is the date?
F5. WI28 Winter intensive session: grades due not supplied. Which office supplies it, and what is the date?

Outside the parent or the unit
F6. A28-2 Autumn second session ends Mon 2027-12-20, 3 days after its parent A28 Autumn term 2027 ends on Fri 2027-12-17. Which dates stand?
F7. S28 Spring term 2028: the exam period ends Tue 2028-05-09, 4 days after the term ends on Fri 2028-05-05. Which dates stand?

Wrong order
F8. A28-2 Autumn second session: the add/drop deadline, Tue 2027-11-30, is 6 days after the withdrawal deadline, Wed 2027-11-24. Which dates stand?

Overlaps to confirm
F9. A28-1 Autumn first session (to Fri 2027-10-22) and A28-2 Autumn second session (from Mon 2027-10-18) share 5 days, Mon 2027-10-18 to Fri 2027-10-22, both under A28 Autumn term 2027. Is the overlap intended?

Non-working days
F10. A28 Autumn term 2027: grades due on Fri 2027-12-24, which falls in CL2 Winter closure (Fri 2027-12-24 to Sun 2028-01-02). Which date stands?
F11. S28 Spring term 2028: the add/drop deadline falls on Sat 2028-01-22, a non-working weekday. Which date stands?

Also noted
No repeated identical rows. No proposal is dated before today. Closed days that no checked date falls on: CL1 Harvest recess, CL3 Spring recess.

Draft for the Registrar's confirmation. No date has been chosen, and no record, notice or page has been changed, sent or published.
```
