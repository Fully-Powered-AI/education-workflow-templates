# Course catalog quality check: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs for this run are the invented example in `public/example.md` (Harbour Lane College, Hospitality Studies), now including a fourth input holding the batch label "Course updates, 10 November 2026" and the line "Run on: 10 November 2026, by the catalog coordinator". No client data was used.

This is the third run. The first run, earlier the same day, gave the same five conflicts but exposed gaps in the template (listed under "What changed since the first run"). The template was then revised and run a second time. After an independent review, the instruction block, the input to the example and the example report were adjusted in small ways (listed under "What changed since the second run"), and the template was run a third time on the revised invented inputs. This record replaces the earlier ones. The run followed the fenced instruction block and the output format in `member/template.md` on the four invented inputs: the submission (seven rows), the catalog export of 9 November 2026 (six records), the field definitions, and the batch label with the run line.

One caveat on independence: the example's report had already been read, in the first run and while the example was being corrected, before this run was written, and in this third run the same reader had also seen the reviewer's notes. Agreement between this output and the example is therefore weak evidence that the template works; it shows the revised wording produces the report the example shows, not that a fresh reader would reach it unaided.

## What came out

COURSE CATALOG QUALITY CHECK: Hospitality Studies, Course updates, 10 November 2026

For: Registrar. Prepared 10 November 2026 for the catalog coordinator. Catalog export of 9 November 2026: 6 current records. Submission: 7 rows.

Inputs read:
- Submission headers matched: Course code, Title, Credits, Description, Linked components, Change type, Submitted by. Not used: none.
- Catalog headers matched: Course ID, Course code, Title, Credits, Description, Linked components, Status. Not used: none.
- Field definitions: code pattern, title limit, credits, description limit, component types. Modality: not held in the export.
- Not supplied: none.

Counts: 7 submitted rows. 5 matched to a current record. 2 with no current record. Of the matched, 5 differ in at least one field and 0 are identical. 5 conflicts for academic review.

Course-by-course comparison:

1. Row 1, HOSP 101. Matched to C-1001. Revise.
   - Code: same.
   - Title: same.
   - Credits: same (3).
   - Description: current "Overview of front-of-house and back-of-house operations in hotels and restaurants." Submitted "Overview of front-of-house and back-of-house operations in hotels, restaurants and event venues."
   - Linked components: same (none).
   - Conflicts: none.
2. Row 2, HOSP 110. Matched to C-1002. Revise.
   - Code: same.
   - Title: same.
   - Credits: current 2. Submitted 3.
   - Description: same.
   - Linked components: same (HOSP 110L, lab).
   - Conflicts: see conflict 1.
3. Row 3, HOSP 110L. Matched to C-1003. Revise.
   - Code: same.
   - Title: current "Food Safety Fundamentals Lab". Submitted "Food Safety Lab".
   - Credits: same (1).
   - Description: same.
   - Linked components: same (HOSP 110, lecture).
   - Conflicts: none.
4. Row 4, HOSP 205. Matched to C-1004. Revise.
   - Code: same.
   - Title: same.
   - Credits: current 3. Submitted: blank.
   - Description: current "Planning, budgeting and running small events." Submitted "Planning, budgeting and running small and mid-sized events."
   - Linked components: same (none).
   - Conflicts: see conflict 2.
5. Row 5, HOSP 225. No current record. New.
   - Compared with no record. Submitted: HOSP 225, "Revenue Management", 3 credits, "Pricing and inventory control for hotel rooms and restaurant tables.", no linked components.
   - Conflicts: see conflict 3.
6. Row 6, HOSP 230. Matched to C-1006. Revise.
   - Code: same.
   - Title: same.
   - Credits: same (3).
   - Description: same.
   - Linked components: current none. Submitted HOSP 230L (lab).
   - Conflicts: see conflict 4.
7. Row 7, HOSP 240. No current record. New.
   - Compared with no record. Submitted: HOSP 240, "Hospitality Marketing", 2.5 credits, "Marketing methods for hotels, restaurants and event venues.", no linked components.
   - Conflicts: see conflict 5.

Conflicts for academic review:

1. Linked credits (row 2, HOSP 110, with row 3, HOSP 110L). HOSP 110 moves from 2 to 3 credits. Its linked lab HOSP 110L stays at 1 credit, unchanged in row 3. The pair's combined credits move from 3 to 4. Is a combined 4 intended? Decided by the academic owner; the registrar approves any change.
2. Missing credits (row 4, HOSP 205). The credits cell is blank. The catalog shows 3. The cell has not been filled and has not been read as "unchanged". What are the credits for HOSP 205? Decided by the academic owner; the registrar approves any change.
3. Course identity (row 5, HOSP 225). The row is marked New. No current record has the code HOSP 225. The current record C-1005 has the code HOSP 220 and the title "Revenue Management", the same title as the submitted row. The credits are the same (3). The submitted description is "Pricing and inventory control for hotel rooms and restaurant tables." and the current one is "Pricing and inventory control for rooms and tables." Is HOSP 225 a new course, a renumbering of HOSP 220, or a duplicate? Decided by the academic owner with the registrar; the registrar approves any change.
4. Link target not found (row 6, HOSP 230). The row links HOSP 230L as a lab. No current record and no submitted row has the code HOSP 230L. The current record for HOSP 230 has no linked components. Is a lab course being created, and does it arrive in a later batch? Decided by the academic owner; the registrar approves any change.
5. Breaks a field definition (row 7, HOSP 240). Credits are 2.5. The institution's definition is a whole number from 1 to 6. No value has been changed. What are the credits for HOSP 240? Decided by the academic owner; the registrar approves any change.

Rows with no current record: Row 5, HOSP 225 (see conflict 3). Row 7, HOSP 240: no current record has this code or the title "Hospitality Marketing"; no identity signal found.

Retirements: None in this batch.

Not checked: Modality variants (modality is not held in the export). Fields outside the definitions (the Status and Submitted by columns). Whether any description is accurate.

Every line traces to a submitted row and a record in the catalog export of 9 November 2026. The comparison changes no catalog record, sends nothing and concerns courses only.

## What was observed

- Every part of the output format was produced, including "Not used: none." on both header lines and the batch label in the heading. The counts add up: 5 matched plus 2 with no record is 7, and 5 differing plus 0 identical is 5.
- Nothing in the run made the assistant stop. The headers matched, the departments agreed, no code appeared twice in the export, no row lacked a code and no student information appeared.
- The result agrees with the published example on the counts, on all five conflicts, on which rows carry them, on the combined credits (3 to 4) and on who decides. The title change on HOSP 110L and the description changes on HOSP 101 and HOSP 205 were printed in the comparison and not raised as conflicts, which the revised step now states.
- HOSP 240 (credits 2.5) was reported once, as a break of the field definition; the paired-credits sum was not needed for it. HOSP 230's missing lab was shown both as a difference in the linked-components line and as a "link target not found" conflict, as the revised steps say.
- The paired-credits conflict was attached to row 2, the row whose credits changed, and named row 3; row 3's conflicts line reads "none".
- The department name came from the export's heading. The date and the person in the "Prepared" line came from the run line in the fourth input.
- The counts line and the "Not checked" line use the wording of the output format; the second run had worded both more loosely.
- No fact appeared in the output that is not in the inputs.
- The reviewer checklist was applied to this output and every item held.

## What changed since the first run

The first run, with no batch label among the inputs, wrote "batch label not stated" and "Not supplied: batch label", which the template did not then provide for. Its other open points were: when a difference counts as a conflict; where the department name comes from; whether a link on one side only is also a field difference; which row a paired-credits conflict belongs to; and whether 2.5 credits is "not a number" or a definition break. The template now settles each of these in its procedure and instruction block, and gives the batch label its own fallback and place under "Not supplied". The example was corrected to match.

## What changed since the second run

A reviewer's minor points were applied. The instruction block now says that a linked pair is checked in both directions only when both sides are in the batch, says that the assistant never asks for a password or a login code, and lists a missing export date under "Not supplied" as it already did for the batch label. The example's inputs gained the run line, and the counts line and "Not checked" line in the example were aligned with the output format. None of this changed the figures, the five conflicts or who decides.

## What this run did not exercise

- A missing batch label, a missing export date or a missing department name. The wording for these was added after the first run and has not been run on this example. The "link not returned" case, where both sides of a pair are in the batch, also did not arise: the only pair in the batch, HOSP 110 and HOSP 110L, names each other.
- The stop conditions for different departments or terms, for a code appearing twice in the export and for a row with no code, and the case of extra columns. They are in the template and the instruction block but no run has met them.
- Retirements, duplicate rows, modality variants and the header-mismatch stop, which the proposed acceptance tests in the template cover and no run has yet done.
