# Online class setup packet: one trial on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in [example.md](example.md), the approved details for BUS 214 section 02, the teacher assignment, the ten-row roster export, the authorized invitation list and the settings. No client data was used. The model that ran the trial did not write the template. It read the template and the example's inputs first, produced the packet by following the instruction block and the output format, and only then read the example's own packet to compare.

## What came out

ONLINE CLASS SETUP PACKET: BUS 214 Small Business Bookkeeping, section 02

For: Learning-platform administrator. Prepared from AC-2027-0143, the teacher assignment, the roster export (10 rows) and the authorized invitation list. Draft for the administrator's verification. Nothing has been created or sent.

Class request: Course name: Small Business Bookkeeping. Course code: BUS 214. Section: 02. Term: Spring 2027. Room: C112. Meeting pattern: Tuesday and Thursday, 18:00 to 19:30. Enrolment cap: 8. Platform template: Evening course standard. Approval: AC-2027-0143, the dean's office, 2 November 2026.

Responsible teacher: Ms Ardell, T-0412. Confirmed: Yes, in the teacher assignment.

Roster counts: Export rows 10. Set aside as another section: 1. Rows for this section: 9. Enrolled: 7. Waitlisted: 1. Status blank: 1. Enrolled and held out of the invitation list: 3. Enrolled and listed: 4. Enrolled is within the cap of 8.

People who can be invited (enrolled, on the authorized list, no open exception): 5
- T-0412 Ms Ardell, teacher
- S2041 Quill, Imani
- S2044 Reddan, Tomas
- S2049 Ferrante, Lucia
- S2052 Pell, Owen

Roster exceptions: 6
1. Staff: T-0455 Mr Brandt, teaching assistant. Confirmed: No in the teacher assignment; on the authorized list. Not listed.
2. Duplicate identity: S2063 and S2064 both read Wirth, Jonas and are both Enrolled in section 02. S2063 is on the authorized list; S2064 is not. Neither is listed.
3. Enrolled and not authorized: S2057 Nandakar, Priya. Not on the authorized list. Not listed.
4. Not enrolled but authorized: S2070 Haskett, Mira. Status Waitlisted; on the authorized list. Not listed.
5. Unclear status: S2075 Sollis, Ahmed. Status blank; not on the authorized list. Not listed.
6. Authorized but absent: S2090. On the authorized list; no row in the export. Not listed.

Set aside: S2080 Bellamy, Noor is on the export but in BUS 214, section 01. Not part of this packet.

For the administrator to verify: (1) Ownership: the approval names Ms Ardell and the confirmed assignment row is Ms Ardell, T-0412; they match. (2) Membership: 4 of the 7 enrolled students can be listed; the 3 held out are exceptions 2 and 3. (3) Template: Evening course standard, as named in the approval.

Decisions for the administrator or the academic office: 6
1. Will the department or academic lead confirm Mr Brandt's teaching assistant assignment?
2. Which Student ID belongs to Jonas Wirth, S2063 or S2064, or are they two people? The registrar holds the answer.
3. Is S2057 Nandakar, Priya to be added to the authorized list? The person or office that authorizes invitations decides.
4. Is S2070 Haskett, Mira, Waitlisted, to stay on the authorized list? The person or office that authorizes invitations decides.
5. What is S2075 Sollis, Ahmed's enrolment status? The registrar holds the answer.
6. Is S2090 missing from the roster export, or wrongly on the authorized list? The registrar and the person or office that authorizes invitations settle it.

Every figure and name traces to the approval note, the teacher assignment, the roster export and the authorized list supplied. The packet creates no class, creates no account, invites nobody and changes no record.

## What was observed

- **Every required part was produced.** The template's output format has no part that could not be filled from these inputs. All tie-outs held: 10 export rows = 9 for the section + 1 set aside; 9 = 7 enrolled + 1 waitlisted + 1 blank; 7 enrolled = 4 listed + 3 held out.
- **Nothing made the run stop.** No header mismatch, no missing file, no teacher disagreement, no failed count, and no request to confirm, send or create anything. The stop conditions were therefore not exercised by this trial.
- **Differences from the published example.** The facts, counts, listed people and exceptions are the same. The wording differs in small ways: the label of exception 1 (the example says "Teacher unconfirmed", this run said "Staff"), the phrasing of the six decisions, and this run's addition that S2064 is not on the authorized list.
- **Facts not in the inputs.** None in this run's output. In the published example, decision 3 says the roster "shows her Enrolled" for S2057, which assumes the student's gender; the inputs do not give it. The example's decisions 1 and 4 also lean towards a suggested answer ("When will ... be confirmed", "Should ... stay") more than the template's "recommend nothing" rule strictly allows, though neither recommends an outcome.
- **Where the instructions needed a guess.**
  - The template's Inputs section still carries a placeholder, "[your enrolment cap rule]", which the instruction block does not repeat. The run used the stated default (a class over its cap is an exception), and it made no difference here because 7 is under 8.
  - The template does not say whether people held out for another exception count toward the cap. This run counted every Enrolled row, as the output format implies.
  - The template does not say whether a pair of duplicate rows is one exception or two. This run wrote one exception for the pair, as the example does. The count of six depends on that choice.
  - The exception order lists "staff" first, but the output format labels each exception only with a free "[Kind]". This run chose "Staff"; the label is not fixed.
  - A row can fall under two kinds. S2075 is both unclear and not on the authorized list; the order places it under "unclear status" and this run mentioned the authorization in the facts.
  - Procedure step 4 says the teacher is found by the role "Teacher"; the example's assistant has the role "Teaching assistant", which only step 8 covers. This run applied step 8 to the assistant, as the example does.
  - "Approved By" in the example is "the dean's office", an office rather than a person. The format has a slot for a name; the run printed the office.
- **Limits of this trial.** It is one run on one example, by a model working through the steps in its head with no code. It shows that the template can be followed and gives the expected packet on this input. It does not show how the template behaves on real exports, other header spellings or the twelve proposed acceptance tests, none of which was run.

## Edited after this run

Changed on 10 November 2026 after an independent review, and not run again. The output and the observations above are as recorded, so where they describe the template or the example they describe them as they stood at the run. The published example now differs from this record in the points below.

- **Two parts added to the output format.** The "Settings used" line and the "Repeated rows (counted once)" count were added to the output format after this run, so the output above has neither. The statement above that every required part was produced was true of the format as it stood then.
- **The example.** Exception 1 is now labelled "Teacher or staff" (this run wrote "Staff"). Decisions 1, 3 and 4 were reworded: decision 3 no longer says the roster "shows her Enrolled", and decisions 1 and 4 no longer lean towards an answer. The example's settings now name who holds each kind of answer, and its closing line now traces to the settings as well.
- **The template.** The placeholder "[your enrolment cap rule]" is gone from the Inputs section, which now says a class over its cap is an exception by default and may be set to a note. The instruction block now says that an unconfirmed or blank Confirmed value adds an exception, that a class over its cap is only a note if the settings say so, and that "cap not stated" adds no exception. "Repeated rows" is now defined as the extra copies only. The settings may now name who holds each kind of answer, and the closing line traces to the settings. The line breaks of the instruction block were tidied.
