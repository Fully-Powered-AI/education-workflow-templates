# Learning system access review

Capability template, version 0.1.0.

## Purpose

Compare who holds an account in the learning system with who should, and put every difference in front of the person who decides. The assistant reads the account export against the current staff list, this term's class assignments and the approved role matrix, and returns one review: departed users with active accounts, role and permission differences, dormant accounts, shared and service accounts, and classes assigned without matching access, each grouped by data owner. A tie-out line accounts for every row of the export. The assistant prepares the review. It changes no permission, disables no account, contacts no one and asks for no sign-in details.

## When to use it and when not to

Use it when a term ends, after a round of staff changes, or on the access-review schedule your institution sets. It suits any system whose accounts can be exported with a role and a last sign-in date.

Do not use it to follow one person who is leaving (that is the employee offboarding and handover checklist), to review what the institution pays for (that is the software subscription and vendor spend review), or to investigate an incident. It does not judge whether a role in the matrix is right, and it makes no employment, disciplinary or legal assessment of anyone.

## Roles

- **Runs it:** the system owner or the IT administrator.
- **Decides access:** the data owner of each area, named on the system-owner list. Their decision on each flagged account is to keep it, change it or remove it, or to ask for more information.
- **Carries out the change and checks it:** the IT administrator, only for changes a data owner has approved.
- **Supplies the staff list and class assignments:** the people who keep them (HR or the registrar's office).
- **Owns the role matrix:** the data owners together, with the system owner.

## Inputs

Every export is read by header. The defaults below are the expected headers. If a header is missing or named differently, stop and list which headers differ; never guess a mapping. The person may confirm a mapping in writing, and the assistant then uses it for this run only.

1. **Account export.** Default headers: `account_id, name, email, account_type, system_role, permissions, course_access, last_login, status`. `account_type` is staff, student, shared or service. `permissions` and `course_access` are lists separated by semicolons; the value `all` in `course_access` means reach to every class, is not a class name and is never flagged as an unassigned class. `last_login` is a date as YYYY-MM-DD, or blank if the account has never signed in. If missing, stop.
2. **Current staff list.** Default headers: `name, email, position, department, end_date`. A blank `end_date` means the person is current. If missing, stop.
3. **Class assignments for the term.** Default headers: `email, class, role_in_class`. If missing, skip the class checks, say so under "Compared" and in the class list, and continue.
4. **Approved role matrix.** Default headers: `system_role, allowed_positions, permitted_permissions, scope, area`. `scope` is "class" (reach is limited to assigned classes) or "system". `allowed_positions` and `permitted_permissions` are lists separated by semicolons. If missing, stop.
5. **System-owner list.** Default headers: `area, data_owner`. If missing, every area is "owner not assigned".
6. **Settings.** The review date (required; if missing, ask for it), the number of days without a sign-in that counts as dormant (default 90), and the system and term names for the title.

Do not accept grades, student work or any column of sign-in details. If an export contains one, say so, ignore it and do not repeat it.

## The procedure

1. **Check the headers** of inputs 1 to 5 as above. Stop on a mismatch.
2. **Sort every account into one of these, in this order, and count each:**
   1. *Student account not reviewed:* `account_type` is student and `system_role` is "Student". These are counted and not reviewed further.
   2. *Not active:* `status` is anything other than Active. Counted and not reviewed.
   3. *Reviewed:* every other account, which goes through steps 3 to 8. This includes a staff, shared or service account whose `system_role` is "Student"; it is reviewed like any other and, if the matrix has no "Student" role, is flagged as a role not on the matrix.
3. **Match each reviewed staff account to the staff list by email**, comparing lower-case, exact. Shared and service accounts are never matched; go straight to step 7. A student account with any role other than "Student" is not matched either; it receives the flag in step 6.
4. **Cannot be assessed.** If an account's email appears more than once in the account export or the staff list, or its `last_login` is not a date or blank, or its `system_role` is blank, mark it "cannot be assessed", state why and take it no further.
5. **Departed.** For matched staff accounts only (never shared, service or student accounts), an account is a departed user if its email is not on the staff list, or the matching row has an `end_date` on or before the review date. An `end_date` after the review date is not flagged; the review is run again after it.
6. **Role and permission differences,** for accounts not already departed. A departed account is not checked for these, because the whole account is already in question and its data owner decides on all of it. Flag in this order, and keep every one that applies:
   1. *Role not on the matrix:* the `system_role` is not in the matrix.
   2. *Changed role:* the person's current `position` is not in the role's `allowed_positions`.
   3. *Permissions beyond the role:* any permission on the account that is not in the role's `permitted_permissions`. Name each extra one. Fewer permissions than allowed is not flagged.
   4. *Class access beyond assignments:* the role's scope is "class" and the account's `course_access` holds a class that the person is not assigned this term. Name each class.
   5. *Student account with a staff role:* the account type is student and the role is not "Student". For a student account this is the only difference checked, because it has no staff row or class assignment to compare with.
7. **Dormant.** For active reviewed accounts, count the days from `last_login` to the review date. If that is the dormant threshold or more, or `last_login` is blank, the account is dormant. Show the days, or "never signed in".
8. **Shared and service accounts** are always listed, whatever else is true. Show the role, permissions, last sign-in, and whether the role is on the matrix. Say that a staff list cannot vouch for the account, and ask the data owner who uses it and what for. These accounts are not checked for role or permission differences (step 6), and that is intended: there is no position or class assignment to compare. A permission beyond the role is shown in the permissions field, and "not on the matrix" in the role field, for the data owner to see, but neither is repeated under "Also". Dormancy is checked (step 7) and does appear under "Also".
9. **Assign one section to each flagged account,** by the first that applies: departed users; role and permission differences; dormant accounts; shared and service accounts (always for those types). Under the account, list "Also" for every other flag it carries. An account appears once in the review.
10. **Classes assigned without access (information, not counted).** For reviewed staff accounts with scope "class", list each class assigned to the person that is missing from their `course_access`. This is not a risk finding; it may mean someone cannot teach their class.
11. **Find the data owner** for each flagged account and each account that could not be assessed. Take the `area` of the account's `system_role` in the matrix, then the `data_owner` for that area on the owner list. If the role is not on the matrix, or the area has no owner, write "owner not assigned".
12. **Write the question** for each flagged account in neutral words, naming the facts: for example, "The staff list shows an end date of [date]. Does the account stay, change or go?" Make no recommendation.
13. **Tie out.** Total accounts in the export must equal student accounts not reviewed + not active + reviewed accounts with no flag + flagged accounts + accounts that could not be assessed. The number in the decisions-by-owner list must equal flagged + could not be assessed. If either fails, stop and report the figures.
14. **Group by data owner.** Count each owner's accounts and list the account IDs. "Owner not assigned" comes first, then the owners in the order of the owner list; leave out an owner with none.

## Exceptions and stop conditions

- **A header is missing or differs:** stop; list the expected and found headers.
- **An input needed to judge an account is missing (account export, staff list, role matrix, review date):** stop and say which.
- **Two staff rows share an email, or an email appears twice in the account export:** the account cannot be assessed; carry on with the others.
- **A role is not on the matrix, or an area has no owner:** the account is flagged and the owner is "owner not assigned"; the IT administrator asks the system owner who decides.
- **An export contains grades, student work or sign-in details:** ignore them, do not repeat them and tell the person.
- **Asked to disable, delete, downgrade or restore an account, to reset a password, to log in, to contact anyone, or to say who should keep access:** decline. A data owner decides and the IT administrator acts.
- **Asked to review a person's conduct, performance or employment status:** decline; the review compares accounts with records only.

## Output format

```
LEARNING SYSTEM ACCESS REVIEW: [system], [term]

For: [system owner], and the data owners listed below. Review date [date]. Dormant after [n] days. Nothing has been changed.

Compared: [n] accounts, [n] staff list rows, [n] class assignments, [n] roles on the matrix. Not supplied or not usable: [list, or "none"].

Tie-out: [n] accounts = [n] student accounts not reviewed + [n] not active + [n] with no flag + [n] flagged + [n] that could not be assessed.

Departed users with active accounts: [n]
- [account_id], [name], [email]. Role [role]; permissions [list]; last sign-in [date or never]. Reason: [end date and "on or before the review date", or "email not on the staff list"]. Also: [other flags, or none]. Data owner: [owner]. Question: [question].
[If none: "None found."]

Role and permission differences: [n]
- [account_id], [name], [email]. Position [position, or "none (student account)" for a student account]; role [role]; permissions [list]; classes [list]; last sign-in [date or never]. Difference: [which of the five flags, with the facts]. Also: [other flags, or none]. Data owner: [owner]. Question: [question].
[If none: "None found."]

Dormant accounts: [n]
- [account_id], [name], [email]. Role [role]; last sign-in [date and number of days, or "never signed in"]. Also: [other flags, or none]. Data owner: [owner]. Question: [question].
[If none: "None found."]

Shared and service accounts: [n]
- [account_id], [name]. Type [type]; role [role, and "not on the matrix" if so]; permissions [list]; last sign-in [date or never]. Also: [other flags, or none]. Data owner: [owner]. Question: who uses this account, and for what?
[If none: "None found."]

Classes assigned without access (information, not counted): [n]
- [name], [email]: [class] assigned, not in the account's class access.
[If none: "None found." If class assignments were not supplied: "Not checked: class assignments were not supplied."]

Could not be assessed: [n]
- [account_id], [name], [email]. Reason: [reason]. Data owner: [owner].
[If none: "None."]

Decisions by data owner: [n]
- [Owner]: [n] accounts: [account_ids].
("Owner not assigned" first, then the owners in the order of the owner list; owners with none are left out.)

This review compares exports. It changes no permission, disables no account,
contacts no one and recommends no decision. The data owners decide; the IT
administrator acts only on what they approve.
```

## Reviewer checklist

1. The tie-out adds up to the number of rows in the account export. (System owner)
2. Every flagged account is in the system with the facts shown, checked on a sample of at least five. (IT administrator)
3. Every departed user has an end date on or before the review date, or is truly absent from the staff list. (Staff list keeper)
4. Every difference against the matrix names the permission, class or position that causes it. (Data owner)
5. Every shared and service account is listed, and each has a question about who uses it. (IT administrator)
6. Every account appears once, and the owner list totals match. (System owner)
7. Nothing in the review recommends a decision or says anything has been changed. (System owner)

## Acceptance tests

Proposed tests. None has been run.

1. **Standard run.** Accounts of each kind, one departed, one changed role, one dormant. Expected: each in its section once; tie-out correct.
2. **Header differs.** The account export names the sign-in date `lastSeen`. Expected: stops and lists the headers; does not guess.
3. **End date in the future.** A staff end date after the review date. Expected: not flagged.
4. **Boundary day.** A last sign-in exactly 90 days before the review date with a 90-day threshold. Expected: dormant.
5. **Two flags.** A departed user who is also dormant. Expected: one entry under departed, with "Also: dormant".
6. **Duplicate email.** An email on two staff rows. Expected: the account is under "Could not be assessed"; the rest are reviewed.
7. **Role not on the matrix.** Expected: flagged, "owner not assigned", listed first under decisions.
8. **Asked to disable an account.** Expected: declines; says the data owner decides and the IT administrator acts.
9. **Class assignments missing.** Expected: class checks skipped, and said so in two places.

## Instructions for the AI assistant

```
You prepare a learning system access review for the system owner. You
never change a permission, disable or delete an account, reset a
password, log in, contact anyone, or recommend who should keep access.
Data owners decide; the IT administrator acts on what they approve.
Never ask for a password, a login code or any sign-in detail.

The user will supply: the account export (default headers: account_id,
name, email, account_type, system_role, permissions, course_access,
last_login, status); the staff list (name, email, position, department,
end_date); the term's class assignments (email, class, role_in_class);
the role matrix (system_role, allowed_positions, permitted_permissions,
scope, area); the system-owner list (area, data_owner); and the review
date, the dormant threshold (default 90 days), and the system and term
names for the title. If a header differs from these, stop and list which
differ; do not guess. If the account export, staff list, role matrix or
review date is missing, stop and say so. If class assignments are
missing, skip the class checks and say so. If the system-owner list is
missing, every area is "owner not assigned". Ignore and do not repeat
grades, student work or sign-in details.

1. Count every account into: student accounts with role "Student" (not
   reviewed); status other than Active (not reviewed); the rest, which
   you review. A staff, shared or service account with the role
   "Student" is reviewed like any other.
2. Match reviewed staff accounts to the staff list by email, lower-case,
   exact. Never match shared, service, or student accounts. A duplicated
   email, an unreadable last_login or a blank role means the account
   cannot be assessed: say why and go no further.
3. Departed, for matched staff accounts only (never shared, service or
   student accounts): email not on the staff list, or end_date on or
   before the review date. An end_date after the review date is not
   flagged.
4. Differences, for accounts that are not departed (a departed account
   is not checked for them; its whole account is already in question):
   role not on the matrix; position not in the role's allowed_positions;
   any permission beyond permitted_permissions (name each); for roles
   with scope class, any class in course_access that the person is not
   assigned (the value "all" is not a class and is never flagged); a
   student account holding a staff role. Keep every one that applies.
5. Dormant: days from last_login to the review date at or above the
   threshold, or never signed in. Show the days.
6. Shared and service accounts are always listed, with the question who
   uses the account and for what. They are not checked for role or
   permission differences; show their role (and whether it is on the
   matrix) and permissions in their entry only. Dormancy counts as an
   "Also".
7. Give each flagged account one section only: departed, differences,
   dormant, or shared and service, first match in that order (shared and
   service accounts always go to their own). List the other flags as
   "Also".
8. List classes assigned to a person but missing from their course_access
   as information, not counted.
9. For each flagged account and each account that could not be assessed,
   the data owner is the owner of the area of its role; if the role is
   not on the matrix or the area has no owner, write "owner not
   assigned". Write a neutral question naming the facts.
10. Tie out: total accounts = student accounts + not active + no flag +
    flagged + cannot be assessed. The decisions-by-owner total must equal
    flagged + cannot be assessed. If either fails, stop and report the
    figures.
11. Use the output format exactly, with "None found." for an empty list.
    End with the closing line that nothing has been changed and nothing
    recommended.

Decline requests to change an account, to say who should keep access, or
to assess a person's conduct, performance or employment. Never adjust a
figure to make it tie.
```

## What to customize

- Your role names, positions, permissions and areas in the matrix.
- The dormant threshold, and which account types are in scope.
- Whether the owner list carries a deputy for each area.
- How a student account with a staff role is treated.
- Who receives each owner's section and the date by which they answer.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini, and which columns are removed before upload.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
