---
name: "online-class-setup-packet"
description: "Prepare the one request the learning-platform administrator needs to set up an approved class online: the course name, code, section, term, room and meeting pattern; the responsible teacher and whether that teacher is confirmed; the roster counted and reconciled; the short list of people who can be invited; and every roster exception, each written as a question with its facts. The packet uses only what the academic office already holds. The assistant prepares; it never creates a class, creates an account, sends an invitation, edits a roster or confirms a teacher."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  template: "Online class setup packet"
---

# Online class setup packet

This is the technical file for a Fully Powered workflow template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

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

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
