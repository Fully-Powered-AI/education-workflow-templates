# Learning system access review: one trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs were the invented example in [example.md](example.md), the settings, account export, staff list, class assignments, role matrix and system-owner list for the invented Halden Vale Academy. No client data was used. The run was a single attempt, made after the template and the example had been edited following an independent review. It was made by the same model that applied those edits, so it is not an independent run. It read the edited template and the inputs first and compared its output with the published example only afterwards.

## What came out

LEARNING SYSTEM ACCESS REVIEW: Halden Vale Learning Hub, Autumn 2026

Review date 2026-12-14. Dormant after 90 days. Nothing has been changed.

Compared: 18 accounts, 12 staff list rows, 15 class assignments, 4 roles on the matrix. Not supplied or not usable: none.

Tie-out: 18 accounts = 2 student accounts not reviewed + 1 not active + 3 with no flag + 11 flagged + 1 that could not be assessed.

Departed users with active accounts: 2
- A02, Tomas Berg. End date 2026-12-11, on or before the review date. Data owner: Deputy Head Academic.
- A10, Maud Ferreira. Email not on the staff list. Also: dormant, last sign-in 2026-09-01, 104 days. Data owner: Deputy Head Academic.

Role and permission differences: 5
- A03, Grace Okoye. Changed role: position Teacher, role Teaching assistant, which allows only Teaching Assistant. Data owner: Head of Curriculum.
- A04, Henrik Soto. Permission beyond the role: view reports is not permitted for Teacher. Data owner: Deputy Head Academic.
- A07, Dana Whitlock. Class access beyond assignments: FR-9B is not assigned this term. Data owner: Deputy Head Academic.
- A11, Wren Abbott. Role not on the matrix: Course builder. Owner not assigned.
- A16, Kofi Danso. Student account with a staff role (Teaching assistant). Data owner: Head of Curriculum.

Dormant accounts: 2
- A08, Ines Calder. Last sign-in 2026-08-30, 106 days. Data owner: Deputy Head Academic.
- A09, Rory Pell. Never signed in. Data owner: Head of Curriculum.

Shared and service accounts: 2
- A12, Front Office Shared. Role Registrar, on the matrix. Data owner: Registrar.
- A13, svc-attendance-sync. Role Integration, not on the matrix. Owner not assigned.

Classes assigned without access (information, not counted): 2
- Grace Okoye: EN-9B. Dana Whitlock: FR-11A.

Could not be assessed: 1
- A18, Imre Halloran. The email appears twice on the staff list. Data owner: Head of Curriculum.

Decisions by data owner: 12
- Owner not assigned: 2 (A11, A13). Deputy Head Academic: 5 (A02, A04, A07, A08, A10). Head of Curriculum: 4 (A03, A09, A16, A18). Registrar: 1 (A12).

Each entry in the full run also carried the account's role, permissions, last sign-in, an "Also" line and a neutral question, as the output format requires. They are shortened here. The closing line (the review changes nothing and recommends nothing) was included.

## What was observed

- Every required part of the output format was produced, in the right order. Nothing in the run called for a stop: all headers matched, all five inputs were supplied, and no request to change an account was made.
- The tie-out worked on the first count (18 = 2 + 1 + 3 + 11 + 1), and the decisions-by-owner total (12) equalled flagged plus could not be assessed.
- The run matched the published example on every account, every section, every count and every owner. The only differences were wording: the published example's "For" line names the IT administrator and the system owner, where this run used the format's placeholder for the system owner; and its questions are worded a little differently.
- No fact in this run's output was missing from the inputs. An earlier version of the published example used a pronoun for Dana Whitlock and called the academy a secondary school; the inputs give neither, and both have since been removed from the example.

Places where the instructions left a choice, and what this run decided:

- Whether a student account with a staff role (A16) is "departed" when its email is not on the staff list. Step 3 says it is not matched and step 6 gives it the student flag; step 5 says an email not on the staff list is departed. This run followed step 3, as the example does. The template should say so in step 5.
- Whether a departed account also gets the step 6 differences. Step 6 says "for accounts not already departed", so this run did not check them. A departed account with extra permissions would then not say so under "Also". The template should say whether that is intended.
- Whether shared and service accounts get the role and permission checks. This run listed whether the role is on the matrix and stopped there, as the output line allows. Step 8 of the edited template now says this is intended.
- Which owner a service or shared account goes to when its role is not on the matrix. This run wrote "owner not assigned", from step 11.
- Whether "Also" for a shared or service account should include "role not on the matrix". This run showed it in the role field only. Step 8 of the edited template now says this is intended.
- Whether a person's class assignment with no matching class access (Grace Okoye, EN-9B) means a gap to fix or just information. The template says information only, and this run kept to that.
- The "For" line has no field for the system owner's name, and the settings give only a role. The run used the role.
- The output has no place to record that a Head of Department position was accepted for the Teacher role; this was a match, not a flag, and nothing was lost.

Shortcomings: the acceptance tests in the template are marked as proposed and none was run here. One run on one invented example shows the instructions can be followed to the published answer. It does not show how the template behaves with a real export, odd headers or large files.

## Edits after this run

After an independent review, small clarifications were made that the run above did not use and that have not been run again. The template now says that the departed test applies to matched staff accounts only, that a departed account is not checked for role and permission differences because the whole account is already in question, and that a staff account holding the role "Student" is reviewed like any other. The instruction block now also names the missing owner list, the system and term names, and the data owner for accounts that could not be assessed. In the published example, the "For" line now names the system owner as the output format does, and the introduction no longer calls the academy a secondary school. The output recorded above is unchanged for the earlier run's accounts except as follows.

After a second review, further small edits were made: step 3 now reads "reviewed staff account"; step 8 and the instruction block say that shared and service accounts are not checked for role or permission differences, on purpose; the template says that the value "all" in course access is not a class name and is never flagged; the output format notes "none (student account)" for the position of a student account; and the instruction block was re-wrapped. In the example, one invented date changed: Maud Ferreira's last sign-in (A10) is now 2026-09-01 instead of 2026-11-20, so that she is both a departed user and dormant, which shows the "Also" line in use. The counts and the tie-out do not change. The enrolment and programme spellings were changed to the American forms. The trial above was then run again on the edited example. Its only difference from the first run's recorded output is the "Also: dormant" line on A10, which is what the template says should happen, and the output recorded above is the re-run's.
