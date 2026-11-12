# Online class setup packet

Workflow template, version 0.1.0.

## Purpose

Prepare the one request the learning-platform administrator needs to set up an approved class online: the course name, code, section, term, room and meeting pattern; the responsible teacher and whether that teacher is confirmed; the roster counted and reconciled; the short list of people who can be invited; and every roster exception, each written as a question with its facts. The packet uses only what the academic office already holds. The assistant prepares; it never creates a class, creates an account, sends an invitation, edits a roster or confirms a teacher.

## When to use it and when not to

Use it once a class is approved and its roster export is available, and again if the export changes before the class opens. One packet covers one course section. For several sections, run it once for each.

Do not use it:

- to decide whether a class should run, who should teach it or who may enrol. Those decisions are made before the packet exists;
- to set up access for a new staff member's accounts, equipment and first weeks. That is employee onboarding;
- to propose where files should live in a shared drive. That is shared-folder filing;
- to review who already has access to a learning system. This packet looks at one new class, not at existing accounts;
- to hold student contact details, grades, support notes or anything beyond a student number, a name and an enrolment status.

## Roles

- **Runs it:** the academic office, the registrar's assistant or whoever holds the approved details and the roster.
- **Verifies ownership and membership, creates the class and approves invitations:** the learning-platform administrator.
- **Settles roster and status questions:** the registrar or the academic office, whoever keeps the roster.
- **Confirms the teacher assignment:** the department or academic lead who makes it.
- **Authorizes who may be invited:** the person or office the institution names for that.

## Inputs

1. **Approved class details,** one block for one section, in the words of the approval. Default fields: Course Code, Course Name, Section, Term, Room, Meeting Pattern, Enrolment Cap, Responsible Teacher, Platform Template, Approval Reference, Approved By, Approval Date. If Course Code, Course Name, Section or Responsible Teacher is missing, stop and ask. Any other missing field is printed as "not stated".
2. **Teacher assignment.** Default headers: Staff ID, Name, Course Code, Section, Role, Confirmed. If the file is missing or a header does not match, stop and ask which column holds what.
3. **Roster export** from the office's own system. Default headers: Student ID, Family Name, Given Name, Course Code, Section, Enrolment Status. If a header does not match one of these, stop and ask; never guess which column is which. Columns beyond these six are ignored, are never repeated in the packet and are not mentioned beyond saying they were ignored.
4. **Authorized invitation list:** the Student IDs and Staff IDs the institution has cleared to be invited to this class. If missing, stop. Without it, no one can be listed.
5. **Settings.** The statuses that count as enrolled (default: "Enrolled", ignoring case and spaces at the ends) and how a class over its cap is treated (default: an exception; the other choice is a note), and optionally who holds each kind of answer (default: the people named under Roles). If missing, use the defaults and say so in the packet, on the "Settings used" line.

The assistant works from files and notes the person supplies. It needs no connection to the learning platform or the student system and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm all four files are present and every header matches its default. Confirm one course code and one section in the approved details. If any header does not match, stop and ask.
2. **Match on code and section.** A row belongs to this class when its Course Code and Section equal the approved ones after trimming spaces and ignoring capitals. "BUS214" and "BUS 214" are different; ask which is meant. Rows for another code or section are set aside, counted and each named once under "Set aside". Do not treat them as exceptions.
3. **Write the class request** with the approved fields exactly as given, and the approval reference and date.
4. **Check the teacher.** Find the assignment row for this code and section with the role Teacher. Print the name and Staff ID from the assignment. Confirmed must read Yes. If it reads anything else or is blank, print "Confirmed: No" or "not stated", add an exception, and do not list the teacher among the people who can be invited. If the assignment names a different teacher from the approval, stop and ask, because ownership is in doubt. Other assignment rows for the class, such as an assistant, follow rule 8 on their confirmation.
5. **Classify each roster row.** Enrolled (status matches the setting), Not enrolled (any other filled status, such as Waitlisted, Withdrawn or Pending), or Unclear (blank, or an unknown word). A row repeated exactly (same ID, name, code, section and status) is counted once in the status counts and noted as a repeat. It is still a row of the export, so it is shown as "Repeated rows", which counts the extra copies only, never the row counted once.
6. **Find duplicate identities.** Two rows with the same Student ID but different names, or the same Family Name and Given Name under two Student IDs, are a duplicate identity. Hold back every row involved. Never choose which is correct. A pair (or group) of rows for one identity is one exception, not one per row.
7. **Reconcile with the authorized list.** A person can be invited only when all hold: the row is Enrolled; the ID is on the authorized list; no other exception involves the row. Enrolled and not authorized is an exception. Authorized and not Enrolled is an exception. An ID on the authorized list with no row in the export is an exception.
8. **Treat staff the same way.** A teacher or assistant can be invited only when the assignment says Confirmed: Yes and the Staff ID is on the authorized list. Otherwise it is an exception.
9. **Check the cap.** If the Enrolled count is above the Enrolment Cap, add an exception stating both numbers, unless the settings say a class over its cap is only a note, in which case write the note and add no exception. If the cap is not stated, write "cap not stated" and add none.
10. **Count and tie out.** Rows for this section = Enrolled + Not enrolled + Unclear + Repeated rows (extra copies only). Export rows = rows for this section + set aside. Enrolled = listed + held out. If any sum fails, stop, report the figures and draft nothing else.
11. **List the people who can be invited** by ID and name, teacher first, then students in ID order. Print only the ID and name.
12. **Number the exceptions** in this order: teacher or staff, duplicate identities, enrolled and not authorized, not enrolled but authorized, unclear status, authorized but absent, cap. Label each with its kind from this fixed set: Teacher or staff; Duplicate identity; Enrolled, not authorized; Not enrolled, authorized; Status unclear; Authorized, not on roster; Over cap. State the facts and that the person is not listed. Recommend nothing.
13. **Write what to verify.** Three items for the administrator: ownership (the teacher in the approval against the confirmed assignment), membership (how many enrolled students can be listed and which exceptions explain the rest) and template (the platform template the approval names).
14. **Write the decisions.** One numbered question per exception, naming who holds the answer. Do not recommend an answer unless asked.
15. **Return the packet** to the person who ran it, for the administrator. A person creates the class and approves invitations.

## Exceptions and stop conditions

- **A header does not match, or a file is missing:** stop; say which one and ask.
- **The approval names a different teacher from the assignment, or two approvals are supplied:** stop and ask.
- **Counts do not tie:** stop; report the figures and the difference.
- **Asked to confirm a teacher, choose between two identities, add a name to the authorized list, create the class, send an invitation or fix the roster:** decline; each is a person's decision or action.
- **Asked for contact details, grades or notes about a student:** decline; the packet holds only ID, name and status.
- **Asked to look at accounts that already exist:** decline; that is a different piece of work.
- **Empty sections:** print "None." for the exceptions, the set-aside rows and the decisions when there are none.

## Output format

```
ONLINE CLASS SETUP PACKET: [course code] [course name], section [section]

For: Learning-platform administrator. Prepared from [approval reference], the teacher assignment, the roster export ([n] rows) and the authorized invitation list. Draft for the administrator's verification. Nothing has been created or sent.

Class request: Course name: [name]. Course code: [code]. Section: [section]. Term: [term]. Room: [room]. Meeting pattern: [pattern]. Enrolment cap: [cap]. Platform template: [template]. Approval: [reference], [approved by], [date].

Responsible teacher: [name], [staff ID]. Confirmed: [Yes / No / not stated], in the teacher assignment.

Roster counts: Export rows [n]. Set aside as another section: [n]. Rows for this section: [n]. Enrolled: [n]. [Other status]: [n] (one entry for each status). Status blank: [n]. Repeated rows (counted once): [n]. Enrolled and held out of the invitation list: [n]. Enrolled and listed: [n]. Enrolled is [within / above / cap not stated] the cap of [cap].

Settings used: [statuses that count as enrolled] ([as supplied / default]); a class over its cap is [treated as supplied / an exception, by default].

People who can be invited (enrolled, on the authorized list, no open exception): [n]
- [staff ID] [name], teacher
- [student ID] [family name], [given name]
(or "None.")

Roster exceptions: [n]
1. [Kind, from the fixed set]: [ID and name]. [Facts]. [Not listed.]
(or "None.")

Set aside: [ID family name, given name] is on the export but in [code, section]. Not part of this packet. (or "None.")

For the administrator to verify: (1) Ownership: [the teacher in the approval against the assignment]. (2) Membership: [n] of the [n] enrolled students can be listed; the [n] held out are exceptions [numbers]. (3) Template: [template named in the approval].

Decisions for the administrator or the academic office: [n]
1. [Question, naming who holds the answer.]
(or "None.")

Every figure and name traces to [the approval note, the teacher assignment, the roster export, the authorized list and the settings] supplied. The packet creates no class, creates no account, invites nobody and changes no record.
```

## Reviewer checklist

1. Every count ties: export rows, rows for the section, enrolled, listed and held out. (Academic office)
2. The class request matches the approval word for word. (Academic office)
3. The teacher shown is the one in the approval, and the confirmation is as the assignment states it. (Department lead)
4. Everyone on the invitation list is enrolled, on the authorized list and not in an exception. (Registrar)
5. Every exception has the facts and a named person who can settle it, and no exception recommends an answer. (Registrar)
6. The packet holds only IDs, names and statuses, and nothing from columns it was meant to ignore. (Academic office)
7. Nothing in the packet says or implies that anything has been created, sent or confirmed. (Administrator)

## Acceptance tests

Proposed tests. None has been run.

1. **Clean class.** All rows enrolled, authorized, one confirmed teacher. Expected: every name listed, no exceptions, "None." printed.
2. **Header mismatch.** The roster uses "Status" in place of "Enrolment Status". Expected: stops and asks which column holds the status.
3. **Unconfirmed teacher.** Assignment reads Confirmed: No. Expected: not listed; exception; ownership flagged for verification.
4. **Different teacher.** Approval names one teacher, the assignment another. Expected: stops and asks.
5. **Two IDs, one name.** Expected: both held out; no choice made; a decision naming the registrar.
6. **Waitlisted but authorized.** Expected: exception; not listed.
7. **Blank status.** Expected: unclear; not listed; no guess.
8. **Authorized but absent.** An ID on the list with no roster row. Expected: exception.
9. **Another section's rows.** Expected: set aside and counted, not exceptions.
10. **Over the cap.** Enrolled 9 against a cap of 8. Expected: an exception stating both numbers.
11. **Extra columns.** The export carries an email column. Expected: ignored; no email appears.
12. **Asked to send.** Expected: declines; invitations are the administrator's approval.

## Instructions for the AI assistant

```
You prepare an online class setup packet for the learning-platform
administrator. You never create a class, create an account, send an
invitation, edit a roster, add a name to a list or confirm a teacher.
A person verifies and approves each of those. You never ask for a
password or a login code.

The user will supply: the approved class details for one course section;
the teacher assignment; the roster export; the authorized invitation
list; and optionally settings (which statuses count as enrolled; the cap
rule; who holds each kind of answer).
Default roster headers: Student ID, Family Name, Given Name, Course Code,
Section, Enrolment Status. Default teacher headers: Staff ID, Name,
Course Code, Section, Role, Confirmed. If a file is missing or a header
does not match, stop and ask. Never guess which column is which.

1. Keep only roster rows whose Course Code and Section equal the
   approved ones (trim spaces, ignore capitals). "BUS214" and "BUS 214"
   are different codes: ask which is meant. Set other rows aside, count
   them and name each once.
2. Print the class request exactly as approved. A missing field is "not
   stated". If the code, name, section or teacher is missing, stop.
3. Find the teacher in the assignment. Confirmed must read Yes to be
   listed. If Confirmed reads anything else or is blank, print "Confirmed: No"
   or "not stated", add a teacher or staff exception and do not list the
   teacher. If the assignment names a different teacher from the
   approval, stop and ask.
4. Classify each row: Enrolled (status matches the setting, default
   "Enrolled"), Not enrolled (any other filled status) or Unclear
   (blank or unknown). Count an exactly repeated row once and note it as
   a repeated row; it still counts as an export row. "Repeated rows"
   counts the extra copies only, not the row counted once.
5. Duplicate identities (same ID with different names, or the same name
   under two IDs): hold back every row involved and choose nothing. One
   identity is one exception, however many rows.
6. A person can be listed only if enrolled, on the authorized list and in
   no exception. Report enrolled-not-authorized, authorized-not-enrolled
   and authorized-but-absent as exceptions. Staff follow the same rule
   using the Confirmed column.
7. If the enrolled count exceeds the cap, add an exception with both
   numbers, unless the settings say a class over its cap is only a note.
   If the cap is not stated, write "cap not stated" and add no exception.
8. Tie out: rows for the section = enrolled + not enrolled + unclear +
   repeated rows (extra copies only); export rows = rows for the section
   + set aside; enrolled = listed + held out. If any sum fails, stop and
   report the figures.
9. List invitees by ID and name only, teacher first, students in ID order.
   Number exceptions: teacher or staff, duplicate identity, enrolled not
   authorized, not enrolled authorized, status unclear, authorized not on
   roster, over cap; use those words as the kind. State facts and
   recommend nothing unless asked.
10. Write the three things to verify and one decision for each exception,
    naming who holds the answer (from the settings if supplied, otherwise
    the registrar, the academic lead or the authorizing office).
11. Print a "Settings used" line saying which settings were supplied
    and which were defaults. Use the output format exactly. Print "None."
    for an empty section. Ignore columns beyond the defaults and never
    repeat them. Include nothing about a student beyond ID, name and
    status.
12. Decline to confirm, choose, send, create or fix; say it is a person's
    decision. End with the trace line.
```

## What to customize

- Your roster and teacher column headers, if you would rather rename the defaults once.
- The statuses that count as enrolled, and how your system names the others.
- The platform templates you use, so the approval can name one.
- The cap rule: an exception, or a note.
- Who authorizes invitations, and where their list comes from.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
