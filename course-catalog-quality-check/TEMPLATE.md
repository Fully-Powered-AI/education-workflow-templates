# Course catalog quality check

Workflow template, version 0.1.0.

## Purpose

Compare a department's batch of course updates with the current catalog export and report, row by row, what differs in the course code, title, credits, description and linked components, so that every conflict reaches the registrar and the academic owners as a numbered question with its facts. The assistant prepares the comparison. It never edits a catalog record, fills a blank, merges two courses, decides whether two records are the same course, or sends anything. The comparison concerns courses only and holds nothing about any individual student.

## When to use it and when not to

Use it when a department submits a batch of course updates, before any change is entered in the catalog. Run it again when the department corrects its batch.

Do not use it:

- to profile an unfamiliar export in general. That is the work of dataset profile;
- to check a spreadsheet's formulas and hidden content before it is shared. That is the work of spreadsheet check before sharing;
- to decide course identity, approve a change or enter it in the student information system. Those are people's decisions and actions;
- to judge whether a description is well written or academically sound;
- when the catalog export is missing or comes from a different department than the submission.

## Roles

- **Runs it:** the catalog or curriculum coordinator in the registrar's office.
- **Reviews the comparison and chooses which questions go out:** the registrar.
- **Answers the questions and decides what a course is:** the academic owner, such as the department chair or the curriculum committee.
- **Submits the batch and corrects it:** the department.
- **Makes approved changes in the catalog:** student information staff, only after the registrar's approval.

## Inputs

1. **The department's submission.** One row per course. Default headers: Course code, Title, Credits, Description, Linked components, Change type, Submitted by. Optional: Course ID, Modality. Change type is New, Revise or Retire. In Linked components, "none" means no links; a blank cell means "not stated".
2. **The current catalog export** for the same department. Default headers: Course ID, Course code, Title, Credits, Description, Linked components, Status. Optional: Modality. The department's name is taken from the heading or note that comes with the export; if there is none, write "department not stated". If the submission or the export is missing, stop.
3. **The institution's field definitions.** The code pattern, the title limit, the description limit, how credits are written and the allowed types of linked component. If they are missing, run the comparison without the definition checks and write "field definitions not supplied" under Inputs read.
4. **The export date and the batch label.** If the export date is missing, write "export date not stated" and list it under "Not supplied". If the batch label is missing, write "batch label not stated" in the heading and list it under "Not supplied". Never make up a label from the date or the department.

**Header check.** Before anything else, match each header in both files with the defaults, ignoring case and spacing. If a required header does not match, stop and ask which column holds that field. Do not guess from the content of the column. If a file has extra columns, list them as "not used".

The assistant works from files and notes the person supplies. It needs no connection to the catalog or the student information system and never asks for a password or a login code.

## The procedure

1. **Read the inputs.** Check the headers as above. Count the submitted rows and the current records. Normalize codes for matching only: trim spaces, capitals, one space between letters and digits. Show codes in the report as supplied.
2. **Look for duplicate rows.** Two submitted rows with the same normalized code are duplicate rows. Compare them field by field. If they differ, that is a conflict; compare neither with the catalog until a person says which row stands. If they are identical, treat them as one row and say so.
3. **Match each row to a record.** Match on Course ID if the submission has one, otherwise on the normalized code. If both are present and point to different records, that is a conflict. A row with no match has "no current record".
4. **Check what Change type implies.** A New row whose code is in the catalog, or a Revise or Retire row whose code is not, is a conflict about course identity. Do not change the row's type.
5. **Look for identity signals on unmatched rows.** For a row with no current record, look for a current record with the same title once case, punctuation and spacing are ignored. If there is one, that is a conflict about course identity: list both codes, both credit values and both descriptions. Use no other similarity test.
6. **Compare matched rows field by field.** For each of code, title, credits, description and linked components, print "same" or print the current value and the submitted value side by side. Compare linked components as a set of code and type pairs, ignoring order. A blank cell in title, description or linked components is "not stated", is not read as a deletion, and keeps the current value. A blank credits cell on a matched or new row is a missing-credits conflict. A link that appears on only one side is shown as a difference in the linked-components line.
7. **Check linked components.** For each linked component named in a submitted row, look for its code among the submitted rows first and the current records second. If it is in neither, the conflict is "link target not found". If a linked pair is both in the batch and one side names the other while the other does not name it back, the conflict is "link not returned". A link whose target is missing is shown as a difference in step 6 and reported again here as a conflict. Never add a link, remove a link or infer a lecture and lab pair from similar codes.
8. **Check credits across a linked pair.** When the credits of one record in a linked pair change and the partner's do not, state the pair's combined credits before and after, and ask whether the change is intended. Add the figures only for the pair, and only whole numbers as supplied; if a credit value in the pair is not a whole number, give the figures as supplied, add nothing and say the combined credits were not worked out. Attach the conflict to the row whose credits changed and name the partner row; the partner row's own conflicts line stays "none" unless it has another conflict.
9. **Check the field definitions.** For every submitted value, check it against the definitions: code pattern, title length, credits form, description length, component type. A value outside a definition is a conflict, including credits that are a number but not a whole number, such as 2.5. Report the value and the definition; never correct it.
10. **Check modality.** If a Modality column is present in either file, rows with the same code and different modality are separate records and are never merged. If one file has the column and the other does not, write that modality could not be compared. If neither has it, write "modality not held in the export".
11. **List retirements.** For a Retire row, list the record, and every current record that names it as a linked component. Whether to retire is the registrar's and the academic owner's decision.
12. **Write the conflicts.** One numbered conflict per issue, in row order. Each gives the kind, the row, the facts from both files and one question. Name who decides: course identity and academic content are the academic owner's, with the registrar; approval of any catalog change is the registrar's. Recommend nothing unless the registrar asks. A plain difference, such as a changed title or description, is printed in the comparison and is not a conflict; raise a conflict only for the kinds in steps 2 to 9 and for a row with no code or a code twice in the export.
13. **Return the report** to the person who ran it, for the registrar. The registrar chooses which questions to send. Changes enter the catalog only after approval and only by student information staff.

## Exceptions and stop conditions

- **A required header does not match:** stop and ask which column holds the field.
- **The submission and the export are for different departments or different terms:** stop and say so.
- **The same normalized code appears twice in the catalog export:** stop on that code and report both records. Do not choose one.
- **A row has no code:** list it as a conflict, "no code", and compare nothing for it.
- **A lecture and lab pair, or any linked set, is partly in the batch:** compare what is there and report the rest under "link not returned" or "link target not found". Never merge the records and never fill a missing side.
- **Credits are blank:** a missing-credits conflict. **Credits are present but not a whole number, or are text:** a conflict, reported as a break of the field definition (step 9), or as "credits not a whole number" if no definitions were supplied. Never fill, round or correct them, and never fill them from the catalog or from a linked record.
- **Asked to correct a value, merge records, decide identity, approve a batch or enter a change:** decline. The registrar and the academic owners decide, and student information staff make approved changes.
- **A row or note contains information about an individual student:** stop reading it, tell the person, and leave it out of the report.

## Output format

```
COURSE CATALOG QUALITY CHECK: [Department], [batch label, or "batch label not stated"]

For: [Registrar]. Prepared [date] for [person who ran it]. Catalog export of [date]: [n] current records. Submission: [n] rows.

Inputs read:
- Submission headers matched: [list]. Not used: [extra columns, or "none"].
- Catalog headers matched: [list]. Not used: [extra columns, or "none"].
- Field definitions: [what was supplied, or "field definitions not supplied"]. Modality: [column present in both files / present in one / "not held in the export"].
- Not supplied: [anything missing, such as "batch label" or "export date", or "none"].

Counts: [n] submitted rows. [n] matched to a current record. [n] with no current record. Of the matched, [n] differ in at least one field and [n] are identical. [n] conflicts for academic review.

Course-by-course comparison:
[n]. Row [n], [code]. [Matched to [Course ID] / No current record]. [Change type].
   - Code: [same / current X, submitted Y].
   - Title: [same / current X, submitted Y].
   - Credits: [same ([value]) / current X, submitted Y].
   - Description: [same / current "X", submitted "Y"].
   - Linked components: [same ([list]) / current X, submitted Y].
   - Conflicts: [none / see conflict [n]].
   [For a row with no current record, replace the five field lines with: "Compared with no record. Submitted: [all five values]."]
   [Print "No rows." if the submission is empty.]

Conflicts for academic review:
[n]. [Kind] (row [n], [code]). [Facts from both files.] [One question.] Decided by [role]; the registrar approves any change.
   [Print "None." if there are no conflicts.]

Rows with no current record: [row, code, and whether an identity signal was found; or "None."]

Retirements: [record, and the records that link to it; or "None in this batch."]

Not checked: [modality if not held; fields outside the definitions; accuracy of descriptions; anything else not compared].

Every line traces to a submitted row and a record in the catalog export of [date]. The comparison changes no catalog record, sends nothing and concerns courses only.
```

## Reviewer checklist

1. Every header was matched, and any mismatch was asked about, not guessed. (Catalog coordinator)
2. Counts add up: matched plus no-record equals submitted rows, and differing plus identical equals matched. (Catalog coordinator)
3. Every "same" and every current/submitted pair agrees with the two files. (Catalog coordinator)
4. No blank was filled, no records were merged, no value was corrected. (Registrar)
5. Every conflict has the facts from both files, one question and the right decider. (Registrar)
6. Linked components were checked in both directions, and combined credits are correct. (Catalog coordinator)
7. Nothing about any individual student appears. (Registrar)

## Acceptance tests

Proposed tests. None has been run.

1. **Clean description change.** A matched row differs only in description. Expected: the two descriptions side by side, no conflict.
2. **Blank credits.** A Revise row with an empty credits cell. Expected: missing-credits conflict; the catalog value is shown but not used.
3. **Header mismatch.** The submission calls the credits column "Units". Expected: stops and asks which column holds credits.
4. **New code, existing title.** A New row with an unused code and the title of a current record. Expected: course identity conflict naming both codes.
5. **Link target absent.** A row links a lab found in neither file. Expected: link-target-not-found conflict; no link added.
6. **Paired credits.** A lecture goes from 2 to 3 credits and its lab stays at 1. Expected: combined credits 3 to 4 stated, with a question.
7. **Duplicate rows that differ.** Two rows with one code and different titles. Expected: duplicate-row conflict; neither compared with the catalog.
8. **Modality variants.** Two catalog records share a code and differ in modality. Expected: kept separate, never merged.
9. **Asked to fix.** The person asks the assistant to correct 2.5 credits to 3. Expected: declines and leaves the value as submitted.

## Instructions for the AI assistant

```
You prepare the course catalog quality check for the registrar's office. You
never edit a catalog record, fill a blank, merge courses, decide whether two
records are the same course, approve a change or send anything. The registrar
and the academic owners decide, and student information staff make any
approved change. You concern courses only; if anything about an individual
student appears, stop reading it and tell the person. You work only from the
files and notes the person supplies, and never ask for a password or a login
code.

The user will supply: the department's submission, the current catalog export
for the same department, the institution's field definitions, and the export
date and batch label. If the submission or the export is missing, stop. If the
field definitions are missing, skip the definition checks and write "field
definitions not supplied". Take the department's name from the export's heading
or the person's note, else write "department not stated". If the batch label
is missing, write "batch label not stated" in the heading and list it under
"Not supplied"; if the export date is missing, write "export date not stated"
and list it under "Not supplied" as well. Never invent either.

Default headers. Submission: Course code, Title, Credits, Description,
Linked components, Change type, Submitted by (optional: Course ID, Modality).
Export: Course ID, Course code, Title, Credits, Description, Linked
components, Status (optional: Modality). If a required header does not match,
stop and ask which column holds the field. Never guess from the contents.
List extra columns as "Not used", or write "Not used: none."
Also stop, and say so, if the submission and the export are for different
departments or terms, or if a code appears twice in the export (report both
records and choose neither). A row with no code is a conflict, "no code";
compare nothing for it.

1. Count rows and records. Normalize codes for matching only; show codes as
   supplied.
2. Find duplicate rows. If they differ, report a conflict and compare neither.
3. Match each row on Course ID if present, otherwise on code. No match means
   "no current record". A New row whose code exists, or a Revise or Retire
   row whose code does not, is a course identity conflict.
4. For a row with no record, look for a current record with the same title
   (ignoring case, punctuation, spacing). If one exists, report a course
   identity conflict with both codes, credits and descriptions.
5. For matched rows compare code, title, credits, description and linked
   components, printing "same" or current beside submitted. A blank title,
   description or links cell means "not stated", not a deletion. A blank
   credits cell is a missing-credits conflict; never fill it. A link on only
   one side is shown as a difference in the linked-components line.
6. Check every linked component exists in the batch or the catalog; a missing
   target is also a conflict. When both sides of a linked pair are in the
   batch, check that each names the other. Never add or remove a link.
7. When one side of a linked pair changes credits, give the pair's combined
   credits before and after and ask if it is intended. Attach the conflict to
   the row whose credits changed and name the partner row. Add whole numbers
   only; otherwise give the figures as supplied and say the sum was not worked
   out.
8. Check every submitted value against the field definitions; report breaks,
   never correct them. Credits that are not a whole number, such as 2.5, are a
   break; blank credits are a missing-credits conflict.
9. Keep records that differ only in modality separate. Say if modality could
   not be compared.
10. List each retirement with the records that link to it.
11. Write one numbered conflict per issue with the facts from both files, one
    question and who decides. A plain difference, such as a changed title or
    description, is shown in the comparison and is not a conflict. Recommend
    nothing unless asked.
12. Use the output format exactly. Print "None." for an empty section. End
    with the trace line.

If asked to fix a value, merge records, decide identity or enter a change,
decline and say the registrar and the academic owners decide.
```

## What to customize

- Your column headers, if they differ from the defaults, so they are matched once and not asked about.
- Your field definitions: code pattern, title and description limits, how credits are written, component types.
- Whether modality is a column, part of the code, or not held.
- Which conflicts go to the department chair and which to a curriculum committee, and who decides course identity.
- Who receives the report and which questions go back to the department.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
