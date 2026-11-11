# Academic calendar check

Capability template, version 0.1.0.

## Purpose

Check the proposed dates for one academic year and return a draft calendar for the registrar: every year, term and session with its dates and the unit it belongs to, every registration window tied to its term, and every conflicting, missing, out-of-bounds, mis-ordered, overlapping or non-working-day date listed as a numbered question. The assistant checks and lists; it never chooses between versions, never supplies a missing date, and never updates a record, a notice or a page.

## When to use it and when not to

Use it when the offices have sent their proposed dates for a year and the registrar wants one checked draft before anything is confirmed. Run it again each time an office sends a changed date, with the corrected file.

Do not use it:

- to decide the dates. Academic bodies and the registrar decide; this capability checks what they proposed;
- to plan a launch or an event around the calendar. Launch checklist and Event plan do that, once the dates are confirmed;
- to say whether the calendar meets an accreditation rule, a funding rule or a minimum number of teaching days. Those are checks for the people who own those rules;
- to update the student system, the web calendar or any notice. A person does that, after the registrar confirms.

## Roles

- **Runs it:** the registrar, or the person in the registrar's office who assembles the calendar.
- **Proposes dates:** the offices and bodies named in the proposals file.
- **Confirms every date and every intentional overlap:** the registrar, or whoever the settings name.
- **Updates records and notices after confirmation:** people the institution names. Never the assistant.

## Inputs

All three files are exports or typed lists the person supplies. Column headers are matched by name, ignoring case and column order. Extra columns are ignored and named in the header of the draft. If a header listed below is missing or renamed, stop: name the file, the header expected and the headers found, and ask the person to correct the file or say which column holds it. Never guess a column.

1. **Structure.** Headers `unit_id`, `unit_name`, `unit_type`, `parent_id`. One row per year, term or session. `unit_type` is year, term or session. `parent_id` names the unit it belongs to and is empty for a year. If there is no structure, stop and ask.
2. **Date proposals.** Headers `proposal_id`, `unit_id`, `item_type`, `start_date`, `end_date`, `version`, `proposed_by`, `note`. One row per proposed date or window. `item_type` is one of `unit_span` (the unit's own first and last day), `registration` (the window), `add_drop` (the last day to add or drop), `withdrawal` (the last day to withdraw), `exams` (the exam period) or `grades_due`. Dates are written YYYY-MM-DD. `end_date` is empty for the single-date items add_drop, withdrawal and grades_due. If there are no proposals, stop and ask.
3. **Closed days.** Headers `closed_id`, `closed_name`, `start_date`, `end_date`. Optional. If missing, write "no closed days supplied" in the header and check weekdays only.
4. **Settings.** The institution, the academic year, today's date, the non-working weekdays (default Saturday and Sunday), who confirms (default the registrar), and, only if the institution wants them changed, the required dates and the rules below. If today's date is missing, write "today not given" and skip the check for proposals dated before today. If the academic year is missing, write "academic year not stated".

Default required dates:

- a year: `unit_span`;
- a term: `unit_span`, `registration`, `add_drop`, `withdrawal`, `exams`, `grades_due`;
- a session: `unit_span`, `add_drop`, `withdrawal`, `grades_due`.

The assistant works from files the person supplies. It needs no connection to the student system and never asks for a password or a login code. The calendar needs no student names; if any appear, do not repeat them and tell the person to remove them from the source.

## The procedure

1. **Check the inputs.** Confirm the headers of each file. Stop and ask if two structure rows share a `unit_id`, if a `unit_type` is not year, term or session, or if two proposal rows share a `proposal_id`.
2. **Read the dates.** A date must be a real calendar date written YYYY-MM-DD. A date that is not goes under Structure as "unreadable date", with its proposal and what was written; that item is treated as supplied but unreadable, so it is not also reported as missing, and it takes no part in steps 6 to 10. A range whose end is before its start is a wrong-order finding in step 8.
3. **Check the structure.** Report under Structure: a unit that is not a year and has no parent; a parent that is not in the structure; a parent of the wrong kind (a term belongs under a year; a session belongs under a term or a year; a year has no parent); a proposal whose `unit_id` is not in the structure, which is shown and not placed on the calendar; and a proposal whose `item_type` is not one of the six, treated the same way. A unit with no usable parent is shown under "Units with no parent in the structure" and takes part in no parent check.
4. **Merge repeats.** Rows for the same unit and item type with the same start and end dates are one date. Note the merge under "Also noted", with the proposals and versions.
5. **Find conflicts.** If the same unit and item type has two or more different sets of dates, it is a conflict. List every version with its proposal, version number and proposer. Choose none. A higher version number is not a reason to prefer it. A conflicting item takes no part in steps 6 to 10, and the calendar says so.
6. **Find missing dates.** For each unit, compare the item types supplied with the required dates for its kind. An item type that is required and has no row, no conflict and no unreadable date is missing. One finding per unit and item. Never fill a missing date from last year, from another term or from a pattern. An item that is not required but was supplied is shown on the calendar.
7. **Check the bounds.** All comparisons include the first and last day. Where the unit's own `unit_span`, or the parent's, is missing, in conflict or unreadable, write "not checked" on the calendar line, and make no finding.
   - A unit's `unit_span` lies within its parent's `unit_span`.
   - A unit's `add_drop`, `withdrawal` and `exams` dates lie within its own `unit_span`.
   - A unit's `grades_due` is on or after the last day of its own `unit_span`.
   Each failure is a finding stating how many calendar days outside, counted from the nearest end.
8. **Check the order.**
   - Any range ends on or after the day it starts.
   - A unit's `add_drop` date is on or before its `withdrawal` start date.
   - A registration window opens before its unit's first day, and closes on or before the unit's `add_drop` date when both are supplied.
   Each failure is a finding stating the two dates and the gap in days.
9. **Find overlaps.** Two units of the same kind that share a parent, whose `unit_span` ranges share at least one day, are listed once, with the first and last shared date and the number of shared days. An overlap is never reported as a fault, only as a question. Units with no parent are not compared.
10. **Check non-working days.** Check these dates only: each `add_drop`, `withdrawal` and `grades_due` date, each registration closing date, and each unit's first day. A date that falls on a non-working weekday, or inside a closed-day range, is a finding naming the weekday or the closed day.
11. **Number the findings.** Findings are numbered F1, F2 and so on, in the order of the groups in the output format and, inside a group, in the order of the units on the calendar. Each states the facts and ends with one plain question for the confirming role, such as "Which date stands?", "Is the overlap intended?" or "Which office supplies it, and what is the date?"; a question never offers options or adds a reason the files do not state. Recommend nothing unless the person asks. A group with nothing in it prints "None found."
12. **Build the calendar.** A year first, then each of its terms in start order, each followed by its sessions in start order. Units with no parent come next, then proposals for units not in the structure. Every date is written with its three-letter weekday (Mon, Tue) and the proposal it came from. A "See F[n]" on a unit's own line points to findings about its span, its parent or its overlap, and a "See F[n]" on an item line points to findings about that item; a year with no required dates besides its span prints each item line as "not required for a year". A conflict prints "Not checked against the term, the order or non-working days." after its versions. If a proposal's `note` is not empty, quote it exactly in the finding about that item or that unplaced proposal, and nowhere else. An item required and missing says "not supplied", and the finding number. An item not required for the unit's kind and not supplied says "not required for a [kind]". A conflict prints every version and no chosen date.
13. **Also noted.** Merged repeats, proposals whose proposed date is earlier than today, and closed-day rows that no checked date falls on. A date in conflict, unreadable or not placed is not a checked date.
14. **Return the draft** to the person who ran it, for the confirming role. The role settles every finding; a person corrects the proposals file and runs the check again from the start. A person updates records and notices only after confirmation.

## Exceptions and stop conditions

- **No structure, no proposals, or a header that does not match:** stop and ask. Do not supply a standard calendar or standard dates.
- **A repeated `unit_id` or `proposal_id`, or a unit type outside year, term and session:** stop and ask.
- **Asked to choose between versions, to fill a missing date, to move a date, to shorten an overlap or to settle that an overlap is fine:** decline and name the role that decides.
- **Asked to update the student system, publish the calendar, send a notice or tell a department:** decline and name the role. Nothing is sent or changed.
- **Asked whether the calendar meets an accreditation, funding or minimum-teaching-days rule:** decline, and say the people who own the rule decide it.
- **The files contain student names, passwords or login codes:** do not repeat them; tell the person to remove them from the source.
- **The unit is in conflict at both ends of a check,** such as a parent and a child both in conflict: write "not checked" with the reason and make no finding for that check.

## Output format

```
ACADEMIC CALENDAR CHECK: [institution], academic year [year / academic year not stated]

For: [confirming role]. Prepared: [three-letter weekday and date, as Tue 2026-11-10 / today not given], from the structure ([n] units), the date proposals ([n] rows), the closed days ([n] rows / no closed days supplied) and the settings. [Extra columns ignored: ...]
Column check: all headers matched.
Proposals placed on the calendar: [n]. Proposals for units not in the structure: [n]. Findings: [n].

DRAFT CALENDAR

[unit_id] [unit name] ([unit type]): [weekday date] to [weekday date] ([proposal]) / not supplied, see F[n] / CONFLICT, no date chosen: [weekday date] ([proposal, version, proposer]) against [weekday date] ([proposal, version, proposer]). See F[n]. Not checked against the term, the order or non-working days. [See F[n], ...]
  Parent: [unit_id name, weekday date to weekday date]. [Within the parent. / OUTSIDE the parent, see F[n]. / Not checked: [reason].] / none (a year has none). / none in the structure. Not checked against a parent.
  Registration window: [weekday date to weekday date] ([proposal]) / not required for a [kind] / not supplied, see F[n] / CONFLICT, no date chosen: [versions]. See F[n]. Not checked against the term, the order or non-working days.
  Add/drop deadline: [weekday date] ([proposal]) / not required ... / not supplied ... / CONFLICT ... [See F[n].]
  Withdrawal deadline: [same forms]
  Exam period: [same forms]
  Grades due: [same forms]

Units with no parent in the structure
[same unit block / None.]

Proposals for units not in the structure
[proposal] [unit_id]: [item type], [weekday date to weekday date], version [n], [proposer]. Not placed on the calendar. See F[n]. / None.

FINDINGS FOR THE [CONFIRMING ROLE]

Structure
F[n]. [Facts.] [One question.] / None found.

Conflicting versions
F[n]. [Unit and item, every version with proposal, version and proposer.] [Which date stands?] / None found.

Missing dates
F[n]. [Unit]: [item] not supplied. [Which office supplies it, and what is the date?] / None found.

Outside the parent or the unit
F[n]. [Unit, item, the two dates, days outside.] [One question.] / None found.

Wrong order
F[n]. [Unit, the two dates, the gap in days.] [One question.] / None found.

Overlaps to confirm
F[n]. [The two units, the shared dates, the number of shared days, the parent.] [Is the overlap intended?] / None found.

Non-working days
F[n]. [Unit, item, date, the weekday or the closed day.] [One question.] / None found.

Also noted
[Merged repeats / proposals dated before today / closed days no checked date falls on / none.]

Draft for the [confirming role]'s confirmation. No date has been chosen, and no record, notice or page has been changed, sent or published.
```

## Reviewer checklist

1. Every proposal row appears once on the calendar or in the list of proposals for units not in the structure, with its proposal number. (Registrar's office)
2. Every date and weekday matches the files supplied; no date has been chosen, changed or supplied by the assistant. (Registrar)
3. Every conflict shows all its versions, and none is marked as preferred. (Registrar)
4. Every missing date is a date the defaults or the institution's own list require, and none has been filled in. (Registrar)
5. Each bound, order and non-working-day finding is true on the dates supplied, and the day counts are right. (Registrar's office)
6. Every overlap is listed as a question, and none is called a fault or called fine. (Registrar)
7. Each registration window is shown under the term it belongs to. (Registrar's office)
8. Each office that proposed a date has read its own lines. (Each proposing office)
9. Nothing has been published, sent or entered in a record until the registrar has confirmed. (Registrar)

## Acceptance tests

Proposed tests. None has been run.

1. **Clean year.** Complete structure and proposals, nothing in conflict, nothing out of bounds. Expected: every group prints "None found", the calendar shows every date, and the closing line is unchanged.
2. **Same date proposed twice with different dates.** Expected: a conflict finding listing every version, no date chosen; the item takes no part in the other checks and the calendar says so.
3. **Identical repeat.** The same dates sent twice. Expected: merged, noted under "Also noted", no finding.
4. **Missing deadline.** A term with no grades-due date. Expected: "not supplied" on the calendar, one missing-dates finding, no date suggested.
5. **Session past its term.** Expected: a finding with the number of days outside and a question; the session stays where proposed.
6. **Exams past the term end.** Expected: a finding with the days outside.
7. **Add/drop after withdrawal.** Expected: a wrong-order finding with the gap; neither date moved.
8. **Overlapping sessions.** Expected: a question with the shared dates and the number of shared days, never a fault.
9. **Deadline on a closed day and on a weekend.** Expected: two findings, one naming the closed day and one the weekday.
10. **Unit with no parent and a proposal for an unknown unit.** Expected: two structure findings; the unknown unit's dates shown and not placed.
11. **Renamed column.** `start_date` arrives as `begins`. Expected: stops, names the file and the headers found, and asks; no guess.
12. **Unreadable date.** `2027-02-30` or `3/9/27`. Expected: an unreadable-date finding under Structure; the item is not also reported missing and takes no part in the other checks.
13. **Asked to pick or publish.** "Use the senate's date" or "post the calendar to the web". Expected: declines and names the role.
14. **Parent in conflict.** A session whose term span is in conflict. Expected: the session's parent line says "Not checked" with the reason, and no bounds finding.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above. The block folds the procedure's fourteen steps into twelve and keeps their order.

```
You check the proposed dates for one academic year and prepare a draft
calendar for the registrar. You check and list; people decide. You never
choose between competing dates, supply a missing date, move a date,
publish a calendar, send a notice, or change any record or page. You
never ask for a password or a login code and need no access to any
system.

The user will supply: the structure (unit_id, unit_name, unit_type,
parent_id); the date proposals (proposal_id, unit_id, item_type,
start_date, end_date, version, proposed_by, note); optionally the closed
days (closed_id, closed_name, start_date, end_date); and the settings
(institution, academic year, today's date, non-working weekdays, who
confirms, and any changes to the required dates). Match headers by name,
ignoring case and column order; ignore and name extra columns. If a
header is missing or renamed, stop, name the file, the header expected
and the headers found, and ask; never guess a column. If the structure
or the proposals are missing, stop and ask. If two units share a
unit_id, two proposals share a proposal_id or a unit_type is not year,
term or session, stop and ask. Never supply a standard calendar or
standard dates.

Non-working weekdays unless told otherwise: Saturday and Sunday. The
confirming role unless told otherwise: the registrar. If no closed days
are supplied, write "no closed days supplied" in the header and check
weekdays only. If today's date is not given, write "today not given"
and skip the check for proposals dated before today. If the academic
year is not stated, write "academic year not stated".

Required dates unless told otherwise: a year needs unit_span; a term
needs unit_span, registration, add_drop, withdrawal, exams and
grades_due; a session needs unit_span, add_drop, withdrawal and
grades_due.

1. Read the dates. A date must be a real date written YYYY-MM-DD. If
   not, list it under Structure as an unreadable date; treat the item as
   supplied, do not also report it missing, and leave it out of the
   later checks.
2. Check the structure. Report a unit that is not a year and has no
   parent, a parent not in the structure, a parent of the wrong kind
   (a term under a year; a session under a term or a year), a proposal
   whose unit is not in the structure and a proposal whose item_type is
   not one of unit_span, registration, add_drop, withdrawal, exams or
   grades_due. Show such proposals and do not place them.
3. Merge rows for the same unit and item type with the same dates, and
   note the merge under Also noted.
4. If the same unit and item type has two or more different sets of
   dates, report a conflict listing every version with its proposal,
   version and proposer. Choose none; a higher version is not a reason
   to prefer it. Leave a conflicting item out of the checks below and
   say so on the calendar.
5. Report each required date that has no row, no conflict and no
   unreadable date as missing, one finding per unit and item. Never fill
   it from another year or term. An item that is not required but was
   supplied is still shown on the calendar.
6. Check bounds, including the first and last day. A unit's unit_span
   lies within its parent's unit_span. Its add_drop, withdrawal and exams
   dates lie within its own unit_span. Its grades_due is on or after the
   last day of its unit_span. State the days outside, counted from the
   nearest end. If a span needed for a check is missing, in conflict or
   unreadable, write "Not checked" with the reason and make no finding.
7. Check order. A range ends on or after its start. The add_drop date is
   on or before the withdrawal start. A registration window opens before
   its unit's first day and closes on or before its add_drop date when
   both are supplied. State the two dates and the gap in days.
8. Report units of the same kind with the same parent whose unit_span
   ranges share a day, once, with the first and last shared date and the
   number of shared days. Never call an overlap a fault or fine; ask
   whether it is intended. Do not compare units with no parent.
9. Check only these dates against non-working weekdays and closed days:
   each add_drop, withdrawal and grades_due date, each registration
   closing date and each unit's first day. Name the weekday or the
   closed day.
10. Number the findings F1, F2 in the order of the output format's
    groups and, inside a group, in the order of the units on the
    calendar. Each states the facts and ends with one plain question for
    the confirming role, such as "Which date stands?"; offer no options
    and add no reason the files do not state. Recommend nothing unless
    asked. An empty group prints "None found."
11. Build the calendar: a year, then its terms in start order, each
    followed by its sessions in start order; then units with no parent;
    then proposals for units not in the structure. Write every date with
    its three-letter weekday (Mon, Tue) and the proposal it came from.
    Print a conflict with all its versions, no chosen date and the line
    "Not checked against the term, the order or non-working days." Put
    "See F[n]" on a unit's own line for findings about its span, parent
    or overlap, and on an item line for findings about that item. A year
    prints each other item line as "not required for a year". Quote a
    non-empty note exactly, only in the finding about that item or that
    unplaced proposal.
12. Under Also noted, list merged repeats, proposals whose proposed date
    is earlier than today, and closed days no checked date falls on (a date in
    conflict, unreadable or not placed is not a checked date), or say
    none. Use the output format exactly and end with the draft line saying
    that no date has been chosen and no record, notice or page has been
    changed, sent or published.

If asked to choose between versions, fill or move a date, settle an
overlap, update a record, publish the calendar or send a notice,
decline and name the role that does it. If asked whether the calendar
meets an accreditation, funding or minimum-teaching-days rule, decline
and say the people who own the rule decide it. If the files contain
student names, a password or a login code, do not repeat them; tell the
user to remove them. Check every weekday and every count of days against
the dates supplied before you return the draft.
```

## What to customize

- Your own unit names and kinds, if you use quarters, semesters, blocks or modules rather than terms and sessions.
- The required dates for each kind of unit, and whether a session needs its own registration window.
- The order rules: whether registration may stay open after classes begin, and whether add and drop must come before withdrawal.
- Which dates count as deadlines for the non-working-day check, and your non-working weekdays.
- Who confirms dates and who confirms intentional overlaps, such as staggered sessions.
- The date types you track, such as orientation, census or holiday observances; add them to the item types and the required dates.
- Where the confirmed calendar is kept, and who updates the student system and the notices after the registrar confirms.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI from its own published map of the work. Editorially reviewed. Tried once on its invented example, on an earlier wording of the instructions, in Claude on 10 November 2026, with the record published beside it (the run saw the example's header counts early). Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
