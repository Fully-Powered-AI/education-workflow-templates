# Course sequence and workload review: an invented example

*Illustrative example with invented data.* The training provider, the course, its modules and every hour, week and outcome below are invented. The course is a six-week evening course, "Spreadsheet Analysis for Office Teams", and the course lead is the programme manager of an invented training provider. No learner is named or counted. First come the four inputs the course lead supplied, in full, then the review the workflow template returned.

## The inputs

### 1. Settings

```
Course: Spreadsheet Analysis for Office Teams
Course lead: Programme manager
Weeks: 6
Weekly hours limit: 8
Assessments due in a week, limit: 2
Entry requirements: Spreadsheet basics
Date: Tuesday 10 November 2026
```

### 2. Learning outcomes

```
Outcome ID,Outcome
O1,Build a clean data table from raw records
O2,Summarise data with formulas and lookups
O3,Present results in a chart
O4,Explain the limits of a result
O5,Record the steps taken so another person can repeat them
O6,Choose a chart type that fits the question
```

### 3. Activities

```
Week,Module,Activity,Hours,Outcome IDs,Needs
1,M1 Tables,Lecture: tables and clean data,2,O1,
1,M1 Tables,Lab: clean a sample file,3,O1,Spreadsheet basics
2,M2 Formulas,Lecture: sums and averages,2,O2,M1 Tables
2,M2 Formulas,Lab: formulas on a cleaned file,3,O2,M1 Tables
2,M2 Formulas,Reading: formula reference,,O2,
3,M3 Lookups,Lecture: lookups,2,O2,M2 Formulas
3,M3 Lookups,Lab: lookups across two tables,4,O2,M2 Formulas
3,M3 Lookups,Practice set,3,O2,M2 Formulas
3,M3 Lookups,Guest talk: analysis at work,1,,
4,M4 Charts,Lecture: choosing a chart,2,O3;O6,M2 Formulas
4,M4 Charts,Lab: build three charts,3,O3,Pivot tables
4,M4 Charts,Project work: first draft,4,O1;O3,M3 Lookups
5,M5 Reporting,Lecture: reporting results,1.5,O3;O4,M4 Charts
5,M5 Reporting,Workshop: limits of a result,3,O4,M4 Charts
5,M5 Reporting,Project work: final report,5,O1;O3;O4,M4 Charts
6,M6 Review,Presentation rehearsal,2,O3;O4,M5 Reporting
6,M6 Review,Revision session,2,O1;O2,
```

### 4. Assessments

```
Assessment,Due week,Outcome IDs
Quiz 1,2,O1;O2
Lookup test,3,O2
Chart quiz,3,O3
Project report,5,O1;O3;O4
Presentation,5,O3;O4;O8
Quiz 3,5,O4
```

## The review the workflow template returned

```
COURSE REVIEW (DRAFT): Spreadsheet Analysis for Office Teams

For: Programme manager (course lead). Prepared Tuesday 10 November 2026 from: the settings, the learning outcomes, the activities, the assessments.
Status: draft, for the course lead to decide. Questions: 10. Crowded weeks: 3 of 6. Coverage gaps: 2. Prerequisite problems: 1.
Counts: 6 modules, 17 activities (16 with an hours estimate), 6 outcomes, 6 assessments, 6 weeks.
Hours are the instructors' estimates, as supplied.
Nothing here measures learning or judges any learner.

Module map
M1 Tables. Week 1. Hours: 5. Outcomes: O1.
   Needs: Spreadsheet basics (entry requirement).
   - Lecture: tables and clean data. Week 1. 2 h. O1.
   - Lab: clean a sample file. Week 1. 3 h. O1.
M2 Formulas. Week 2. Hours: at least 5 (1 activity without an estimate). Outcomes: O2.
   Needs: M1 Tables (taught week 1).
   - Lecture: sums and averages. Week 2. 2 h. O2.
   - Lab: formulas on a cleaned file. Week 2. 3 h. O2.
   - Reading: formula reference. Week 2. no estimate. O2.
M3 Lookups. Week 3. Hours: 10. Outcomes: O2.
   Needs: M2 Formulas (taught week 2).
   - Lecture: lookups. Week 3. 2 h. O2.
   - Lab: lookups across two tables. Week 3. 4 h. O2.
   - Practice set. Week 3. 3 h. O2.
   - Guest talk: analysis at work. Week 3. 1 h. No outcome (question 9).
M4 Charts. Week 4. Hours: 9. Outcomes: O1, O3, O6.
   Needs: M2 Formulas (taught week 2); Pivot tables (not placed, question 1); M3 Lookups (taught week 3).
   - Lecture: choosing a chart. Week 4. 2 h. O3, O6.
   - Lab: build three charts. Week 4. 3 h. O3.
   - Project work: first draft. Week 4. 4 h. O1, O3.
M5 Reporting. Week 5. Hours: 9.5. Outcomes: O1, O3, O4.
   Needs: M4 Charts (taught week 4).
   - Lecture: reporting results. Week 5. 1.5 h. O3, O4.
   - Workshop: limits of a result. Week 5. 3 h. O4.
   - Project work: final report. Week 5. 5 h. O1, O3, O4.
M6 Review. Week 6. Hours: 4. Outcomes: O1, O2, O3, O4.
   Needs: M5 Reporting (taught week 5).
   - Presentation rehearsal. Week 6. 2 h. O3, O4.
   - Revision session. Week 6. 2 h. O1, O2.

Load by week (limit: 8 hours; 2 assessments)
Week 1: 5 h. Assessments due: 0. Within the limits.
Week 2: at least 5 h (1 activity without an estimate). Assessments due: 1 (Quiz 1). Not judged until the estimate is supplied (question 10).
Week 3: 10 h, over by 2. Assessments due: 2 (Lookup test, Chart quiz). CROWDED, hours.
Week 4: 9 h, over by 1. Assessments due: 0. CROWDED, hours.
Week 5: 9.5 h, over by 1.5. Assessments due: 3 (Project report, Presentation, Quiz 3), over by 1. CROWDED, hours and assessments.
Week 6: 4 h. Assessments due: 0. Within the limits.
Total across the course: 42.5 h of estimated activity, plus 1 activity without an estimate.

Coverage of learning outcomes
O1 Build a clean data table from raw records. Taught: weeks 1, 4, 5, 6. Assessed by: Quiz 1 (week 2), Project report (week 5).
O2 Summarise data with formulas and lookups. Taught: weeks 2, 3, 6. Assessed by: Quiz 1 (week 2), Lookup test (week 3).
O3 Present results in a chart. Taught: weeks 4, 5, 6. Assessed by: Chart quiz (week 3), Project report (week 5), Presentation (week 5). Earliest assessment is before the first teaching (question 7).
O4 Explain the limits of a result. Taught: weeks 5, 6. Assessed by: Project report (week 5), Presentation (week 5), Quiz 3 (week 5).
O5 Record the steps taken so another person can repeat them. Taught: nowhere in the outline. Assessed by: no assessment. GAP (question 5).
O6 Choose a chart type that fits the question. Taught: week 4. Assessed by: no assessment. GAP (question 6).
Not in the outcome list: O8, cited by Presentation (question 8).

Questions for the course lead: 10
1. Prerequisite not placed. "Lab: build three charts" (week 4, M4 Charts) needs "Pivot tables". No module has that name and the entry requirements list only "Spreadsheet basics". Where is it taught, or is it an entry requirement? Affects: M4 Charts.
2. Crowded week. Week 3 holds 10 h against your limit of 8, over by 2 ("Lecture: lookups" 2 h, "Lab: lookups across two tables" 4 h, "Practice set" 3 h, "Guest talk: analysis at work" 1 h). What, if anything, changes? Affects: M3 Lookups.
3. Crowded week. Week 4 holds 9 h against your limit of 8, over by 1 ("Lecture: choosing a chart" 2 h, "Lab: build three charts" 3 h, "Project work: first draft" 4 h). What, if anything, changes? Affects: M4 Charts.
4. Crowded week. Week 5 holds 9.5 h against 8, over by 1.5, and 3 assessments against your limit of 2 (Project report, Presentation, Quiz 3). What, if anything, changes? Affects: M5 Reporting.
5. Outcome not taught and not assessed. O5 "Record the steps taken so another person can repeat them" is in the outcome list and in no activity or assessment. Is it taught somewhere the outline does not show, or should it leave the list? Affects: O5.
6. Outcome taught but not assessed. O6 "Choose a chart type that fits the question" is taught in the week 4 "Lecture: choosing a chart" and is in no assessment. Is that intended? Affects: O6.
7. Assessed before first taught. Chart quiz is due in week 3 and cites O3, which the outline first teaches in week 4. Which is right, the due week or the outcome? Affects: O3.
8. Outcome not in the list. Presentation cites O8, which is not in the outcome list. Which outcome is meant? Affects: Presentation.
9. Activity without an outcome. "Guest talk: analysis at work" (week 3, 1 h) cites no outcome. Which outcome does it serve, or is it extra to the course? Affects: M3 Lookups.
10. Missing estimate. "Reading: formula reference" (week 2) has no hours. What is the instructors' estimate? Week 2 is not judged until it is given. Affects: M2 Formulas.

Internal working document for Spreadsheet Analysis for Office Teams. Nothing has been changed, sent or approved; the course lead decides every change.
```

## What to notice

Every hour in the review is one the course lead supplied. Week 3 is 2 + 4 + 3 + 1 = 10 hours, week 4 is 2 + 3 + 4 = 9, and week 5 is 1.5 + 3 + 5 = 9.5; against a limit of 8 those are over by 2, 1 and 1.5. Week 2 shows 2 + 3 = 5 hours and is not called crowded or fine, because one activity has no estimate. The six weeks add to 5 + 5 + 10 + 9 + 9.5 + 4 = 42.5 hours. The review never suggests moving anything; each problem is a question, and the Guest talk, the missing "Pivot tables" and the unknown outcome O8 are printed as found rather than corrected.
