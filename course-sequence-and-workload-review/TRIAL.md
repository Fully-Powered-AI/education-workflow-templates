# Course sequence and workload review: a trial on the example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in `public/example.md` (the settings, the learning outcomes, the activities and the assessments for "Spreadsheet Analysis for Office Teams"). No client data was used. The assistant that ran this did not write the template.

## A limit on this trial

This is a second run, made after a review of the first. It was made by the same kind of assistant that edited the template, and it had already read the example's published review, so the close match below is weak evidence: the sums and classifications were worked out again from the inputs, but nobody checked the output blind. A clean rerun from the inputs alone, by a run that has not seen the example's output, has not been done. The first run's record was replaced by this one because the instruction block, the output format and the example changed after it.

## What came out

The final instruction block was followed on the inputs. Nothing triggered a stop: the headers matched, every week was a whole number from 1 to 6, every Hours value was a number or blank.

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

## What was observed

- **Every required part was produced:** the header block, the module map, the load by week, the coverage section, the unknown-ID line and ten questions, in the order the instructions give (prerequisite, crowded weeks, coverage gaps, order problem, then loose ends and the missing estimate). Every weekly sum was checked twice (5, 5+, 10, 9, 9.5, 4; total 42.5).
- **Nothing was told to stop.** No header, week or hours value failed, no limit was missing, and the inputs hold no learner data.
- **Differences from the published example:** none that were found. The output above is word for word the review in `public/example.md`. That is expected here, because the example was edited to match the wording the final instructions fix (the "Needs" order of first appearance, "No module has that name", the question kind "Outcome not in the list", the full module name after "Affects", the question order), and the same assistant had read it first. It does not show that a run from the inputs alone would produce these words.
- **Facts not in the inputs:** none found. Every hour, week, name and ID traces to the inputs.
- **Needs merging:** M4 Charts takes its Needs from the three activity rows in the order they appear: "M2 Formulas", then "Pivot tables", then "M3 Lookups". The printed line follows that order, as the instructions say.
- **Ambiguities from the first run, and where they now stand:** the instructions now state the sort order of outcome IDs, the merging and order of Needs, that an order problem is not counted as a coverage gap, that a week not judged and its missing estimate are one question, how to place the weekday, that each week in a "Taught" list is printed once, the question order, and the question kind for an outcome not in the list. These were answered in the template after the first run; this run followed them, and nothing new was ambiguous. An empty week (no activities) is not in the example's inputs, so that sentence in step 4 has not been run.
- **Shortcomings:** this was one run on one invented example. It is not a test of the twelve proposed acceptance tests; none of the stop conditions or refusals was exercised. The independence limit above applies.
