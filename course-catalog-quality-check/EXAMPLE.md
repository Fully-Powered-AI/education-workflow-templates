# Course catalog quality check: an invented example

*Illustrative example with invented data.* The college, the department, the people and every course below are invented. Harbour Lane College is an invented small college. Its Hospitality Studies department has sent the registrar's office a batch of seven course updates, and the catalog coordinator runs the check before anything is entered. People are referred to by role.

The inputs come first, in full, so the template can be run on them. The report follows.

## The inputs

### 1. The department's submission

```
Course code | Title | Credits | Description | Linked components | Change type | Submitted by
HOSP 101 | Introduction to Hospitality Operations | 3 | Overview of front-of-house and back-of-house operations in hotels, restaurants and event venues. | none | Revise | Department chair
HOSP 110 | Food Safety Fundamentals | 3 | Hygiene, storage and handling practices for food service. | HOSP 110L (lab) | Revise | Department chair
HOSP 110L | Food Safety Lab | 1 | Supervised practice in kitchen hygiene routines. | HOSP 110 (lecture) | Revise | Department chair
HOSP 205 | Event Planning | | Planning, budgeting and running small and mid-sized events. | none | Revise | Department chair
HOSP 225 | Revenue Management | 3 | Pricing and inventory control for hotel rooms and restaurant tables. | none | New | Department chair
HOSP 230 | Front Office Systems | 3 | Reservation and check-in systems used at hotel front desks. | HOSP 230L (lab) | Revise | Department chair
HOSP 240 | Hospitality Marketing | 2.5 | Marketing methods for hotels, restaurants and event venues. | none | New | Department chair
```

### 2. The current catalog export (Hospitality Studies, exported 9 November 2026)

```
Course ID | Course code | Title | Credits | Description | Linked components | Status
C-1001 | HOSP 101 | Introduction to Hospitality Operations | 3 | Overview of front-of-house and back-of-house operations in hotels and restaurants. | none | Active
C-1002 | HOSP 110 | Food Safety Fundamentals | 2 | Hygiene, storage and handling practices for food service. | HOSP 110L (lab) | Active
C-1003 | HOSP 110L | Food Safety Fundamentals Lab | 1 | Supervised practice in kitchen hygiene routines. | HOSP 110 (lecture) | Active
C-1004 | HOSP 205 | Event Planning | 3 | Planning, budgeting and running small events. | none | Active
C-1005 | HOSP 220 | Revenue Management | 3 | Pricing and inventory control for rooms and tables. | none | Active
C-1006 | HOSP 230 | Front Office Systems | 3 | Reservation and check-in systems used at hotel front desks. | none | Active
```

### 3. The institution's field definitions

```
Course code: four capital letters, a space, three digits, an optional capital L for a lab.
Title: at most 60 characters.
Credits: a whole number from 1 to 6.
Description: at most 200 characters.
Linked component types: lecture, lab.
Modality: not held in the catalog export.
```

### 4. The batch label and the run

```
Batch label: Course updates, 10 November 2026
Run on: 10 November 2026, by the catalog coordinator
```

## The report

**COURSE CATALOG QUALITY CHECK: Hospitality Studies, Course updates, 10 November 2026**

**For:** Registrar. Prepared 10 November 2026 for the catalog coordinator. Catalog export of 9 November 2026: 6 current records. Submission: 7 rows.

**Inputs read:**
- Submission headers matched: Course code, Title, Credits, Description, Linked components, Change type, Submitted by. Not used: none.
- Catalog headers matched: Course ID, Course code, Title, Credits, Description, Linked components, Status. Not used: none.
- Field definitions: code pattern, title limit, credits, description limit, component types. Modality: not held in the export.
- Not supplied: none.

**Counts:** 7 submitted rows. 5 matched to a current record. 2 with no current record. Of the matched, 5 differ in at least one field and 0 are identical. 5 conflicts for academic review.

**Course-by-course comparison:**

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

**Conflicts for academic review:**

1. **Linked credits (row 2, HOSP 110, with row 3, HOSP 110L).** HOSP 110 moves from 2 to 3 credits. Its linked lab HOSP 110L stays at 1 credit, unchanged in row 3. The pair's combined credits move from 3 to 4. Is a combined 4 intended? Decided by the academic owner; the registrar approves any change.
2. **Missing credits (row 4, HOSP 205).** The credits cell is blank. The catalog shows 3. The cell has not been filled and has not been read as "unchanged". What are the credits for HOSP 205? Decided by the academic owner; the registrar approves any change.
3. **Course identity (row 5, HOSP 225).** The row is marked New. No current record has the code HOSP 225. The current record C-1005 has the code HOSP 220 and the title "Revenue Management", the same title as the submitted row. The credits are the same (3). The submitted description is "Pricing and inventory control for hotel rooms and restaurant tables." and the current one is "Pricing and inventory control for rooms and tables." Is HOSP 225 a new course, a renumbering of HOSP 220, or a duplicate? Decided by the academic owner with the registrar; the registrar approves any change.
4. **Link target not found (row 6, HOSP 230).** The row links HOSP 230L as a lab. No current record and no submitted row has the code HOSP 230L. The current record for HOSP 230 has no linked components. Is a lab course being created, and does it arrive in a later batch? Decided by the academic owner; the registrar approves any change.
5. **Breaks a field definition (row 7, HOSP 240).** Credits are 2.5. The institution's definition is a whole number from 1 to 6. No value has been changed. What are the credits for HOSP 240? Decided by the academic owner; the registrar approves any change.

**Rows with no current record:** Row 5, HOSP 225 (see conflict 3). Row 7, HOSP 240: no current record has this code or the title "Hospitality Marketing"; no identity signal found.

**Retirements:** None in this batch.

**Not checked:** Modality variants (modality is not held in the export). Fields outside the definitions (the Status and Submitted by columns). Whether any description is accurate.

Every line traces to a submitted row and a record in the catalog export of 9 November 2026. The comparison changes no catalog record, sends nothing and concerns courses only.
