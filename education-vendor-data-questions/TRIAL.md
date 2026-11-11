# Trial: Teaching tool vendor data questions, run on its invented example

- **Product:** Claude, run in Claude Code

Model: recorded as Claude Sonnet 5.5 (model ID claude-sonnet-5-5) by the session that made the run; this was not independently verified. This is the third recorded run. The first run found that the template did not give the wording of the standard questions, which part of each question had to be answered, or the order in which statuses win; the second followed those additions. A later independent review failed the template because the invented vendor document named two real companies, and raised smaller points on the instruction block and on several quotations. After that revision, this run was made by the assistant that made the revision, following the revised instruction block and output format by hand in the same session, not in a fresh session. It is therefore less independent than a run by a reader who had not seen the revision, and the example's output section holds this run's output rather than an independent expectation. A rerun in a fresh session has not been made. After a later review, two sentences of the instruction block were reworded without changing any rule (the repeated quoting rule was merged and the dates for DOCUMENTS DIFFER were stated in the gap-list item); the run was not repeated and the recorded output is unchanged.

Wording change after the second run: item 3 of D2 originally named two real account providers in its sign-in sentence. It now reads "Schools sign in with single sign-on through the accounts the school already uses." The change removes two company names from the invented inputs. The Q5 quotation changed with it, and this run was made on the changed text. The Q11 and Q12 lines now quote their passages. Statuses, totals and gaps are the same as in the second run.

Date: 2026-11-10

The inputs are the invented example in `public/example.md` (an invented secondary school, Tool A and Vendor A). No client data was used.

## Inputs used

All four inputs in the example's "The inputs" section: the review facts, the four data categories (C1 to C4), the five vendor documents (D1 to D5, with the numbered text of D1 to D4; D5 supplied only as a file name) and the school's own criteria (none supplied).

## What came out

```
TEACHING TOOL VENDOR DATA QUESTIONS: Tool A, from Vendor A

For: school business manager. Assessed by: privacy lead, security lead. Approved by: head teacher. Prepared Tuesday 10 November 2026 from 4 data categories and 5 documents.

INTENDED USE
Online reading practice with read-aloud recording, for Year 7 to 9 English classes, about 420 students and 28 teachers. Planned start Tuesday 12 January 2027, 63 days from today.

DATA IN SCOPE (4 categories)
C1 Student name and class, about student, synced, sensitivity medium.
C2 Reading scores and answers, about student, generated, sensitivity high.
C3 Teacher name and work email, about staff, entered, sensitivity medium.
C4 Student voice recordings, about student, generated, sensitivity high.

DOCUMENTS (5 supplied: 4 read, 1 not read)
D1 Privacy policy, policy, 14 August 2026: read.
D2 Security overview page, security page, 2 September 2026: read.
D3 Subprocessor list, subprocessor list, 2 September 2026: read.
D4 Independent audit summary, independent report, 30 March 2025: read.
D5 Master services agreement, agreement, 1 August 2026: not read (agreements are not read by this capability).
Independent reports: D4: issued 30 March 2025, 19 months before today, within the age limit of 24 months. Scope and period as stated: the hosted Tool A service, 1 January 2024 to 31 December 2024; issuer Auditor X; counted as evidence.

QUESTION PACK (15 questions, to put to Vendor A)
Q1 Data flows. Which of the data items listed in this pack does the tool collect, and does it collect anything else, including usage and device data? Applies to: C1, C2, C3, C4.
Q2 Data flows. For each item, where does it come from, and where does it go: your own systems, other companies, other parts of the product? Applies to: C1, C2, C3, C4.
Q3 Data flows. Do you use any of this data for anything other than providing the tool to the school, such as improving products, training models, analytics or marketing? Applies to: C1, C2, C3, C4.
Q4 Access. Which roles at the vendor can see the school's data, for what reasons, and how is that access recorded? Applies to: C1, C2, C3, C4.
Q5 Access. How do the school's own users sign in and get permissions, and who at the school controls roles? Applies to: C1, C2, C3, C4.
Q6 Access. Can the school see or export a record of who has accessed its data? Applies to: C1, C2, C3, C4.
Q7 Retention. How long is each item kept while the tool is in use? Applies to: C1, C2, C3, C4.
Q8 Retention. What happens to each item when use ends or the school asks, including copies and backups, and how is deletion confirmed to the school? Applies to: C1, C2, C3, C4.
Q9 Subprocessors. Which other companies handle this data for you, doing what, and in which countries? Applies to: C1, C2, C3, C4.
Q10 Subprocessors. How, and how far in advance, do you tell the school about changes to those companies? Applies to: C1, C2, C3, C4.
Q11 Subprocessors. In which countries or regions is the data stored and processed? Applies to: C1, C2, C3, C4.
Q12 Evidence and incidents. Which independent reports or certificates exist for this product, with their scope and date? Applies to: C1, C2, C3, C4.
Q13 Evidence and incidents. How do you tell the school about a security incident that affects its data, and how soon? Applies to: C1, C2, C3, C4.
Q14 Data flows. Which fields does the connection to the school's own systems receive, and can the school limit them to fewer? Applies to: C1 (asked because C1 is synced).
Q15 Data flows. How are the things the tool produces about a person, such as scores, answers and recordings, stored, and can they be corrected or removed on request? Applies to: C2, C4 (asked because they are generated).

WHAT THE DOCUMENTS SAY
Q1 PARTLY ADDRESSED. D1 para 1: "collects the name, class and school-assigned ID that a school sends us", "the answers and scores a student produces", "audio a student records during read-aloud tasks"; also "device type and the times a student signs in". Missing: teacher name and work email (C3) are not mentioned.
Also collected, in no category supplied: school-assigned ID, device type, sign-in times (D1 para 1).
Q2 PARTLY ADDRESSED. Sources: D1 para 1 ("that a school sends us", "a student produces", "a student records"). Destinations: D3 item 2 ("speech-to-text for recordings, United States"), D3 item 3 ("sending sign-in and notification emails, United States"), D3 item 1 ("cloud hosting, Ireland"). Missing: where C1, C2 and C3 go, since the subprocessor entries do not name them; where C3 comes from.
Q3 PARTLY ADDRESSED. D1 para 2: "to provide the service and to improve our products. We do not sell student data." Missing: whether teacher data (C3) is used for anything other than providing the tool; the statement names student data only.
Q4 PARTLY ADDRESSED. D2 para 2: "limited to the support and engineering teams, and that access is logged". Missing: the reasons for access.
Q5 VENDOR STATEMENT ONLY. D2 para 3: "single sign-on through the accounts the school already uses", "School administrators assign teacher and student roles".
Q6 NOT ADDRESSED. Nothing found in the documents read that answers it; D2 para 2 says access "is logged" and speaks to Q4 only, as it does not say the school can see or export the record.
Q7 DOCUMENTS DIFFER. Recordings (C4): D1 para 4 (14 August 2026) says "stored for 30 days"; D2 para 4 (2 September 2026) says "retained for 90 days". Neither is chosen. Other items: D1 para 3, "as long as the school's account is active".
Q8 PARTLY ADDRESSED. D1 para 3: "delete it within 90 days after the account closes". Missing: deletion on the school's request, copies and backups, and confirmation of deletion.
Q9 VENDOR STATEMENT ONLY. D3 item 1: "Hosting Company B: cloud hosting, Ireland."; D3 item 2: "Speech Company C: speech-to-text for recordings, United States."; D3 item 3: "Email Company D: sending sign-in and notification emails, United States."
Q10 VENDOR STATEMENT ONLY. D3 item 4: "30 days' notice before adding a subprocessor, by email to the account administrator".
Q11 PARTLY ADDRESSED. D3 item 1: "cloud hosting, Ireland"; D3 item 2: "speech-to-text for recordings, United States"; D3 item 3: "sending sign-in and notification emails, United States". Missing: where the vendor's own systems and staff process the data.
Q12 EVIDENCE FOUND. D4 para 1: "Auditor X examined the security controls of the hosted Tool A service", "for the period 1 January 2024 to 31 December 2024", "The report is dated 30 March 2025"; D4 para 2: "no exceptions were noted in the areas tested". Reports supplied only.
Q13 PARTLY ADDRESSED. D2 para 5: "we tell affected schools without undue delay". Missing: how the school is told, and a stated time, which "without undue delay" does not give.
Q14 PARTLY ADDRESSED. D1 para 1: "the name, class and school-assigned ID that a school sends us". Missing: whether the school can limit the fields.
Q15 NOT ADDRESSED. Nothing found in the documents read that answers it; D1 para 4 and D2 para 4 speak to Q7 only, as they say how long recordings are kept, not how they are stored or whether they can be corrected or removed on request.
Totals: evidence found 1; vendor statement only 3; partly addressed 8; documents differ 1; not addressed 2; total 15.

GAPS (14), in order
1. Q6 NOT ADDRESSED: whether the school can see or export a record of who accessed its data is not described. Assessed by security lead.
2. Q15 NOT ADDRESSED: how generated items are stored, and whether they can be corrected or removed on request, are not described. Assessed by privacy lead.
3. Q7 DOCUMENTS DIFFER: recordings kept 30 days (D1, 14 August 2026) or 90 days (D2, 2 September 2026). Assessed by privacy lead.
4. Q1 PARTLY ADDRESSED: C3 not mentioned. Assessed by privacy lead.
5. Q2 PARTLY ADDRESSED: destinations for C1, C2 and C3, and the source of C3, not stated. Assessed by privacy lead.
6. Q3 PARTLY ADDRESSED: other uses of C3 not stated. Assessed by privacy lead.
7. Q4 PARTLY ADDRESSED: reasons for vendor access not stated. Assessed by security lead.
8. Q8 PARTLY ADDRESSED: deletion on request, backups and confirmation not stated. Assessed by privacy lead.
9. Q11 PARTLY ADDRESSED: the vendor's own processing locations not stated. Assessed by privacy lead.
10. Q13 PARTLY ADDRESSED: method and stated time for telling the school not given. Assessed by security lead.
11. Q14 PARTLY ADDRESSED: limiting the synced fields not stated. Assessed by privacy lead.
12. Q5 VENDOR STATEMENT ONLY: vendor's own words; no independent support supplied. Assessed by security lead.
13. Q9 VENDOR STATEMENT ONLY: vendor's own words; no independent support supplied. Assessed by privacy lead.
14. Q10 VENDOR STATEMENT ONLY: vendor's own words; no independent support supplied. Assessed by privacy lead.

FOR THE LEADS TO ASSESS
Privacy lead: 10 gaps (Q1, Q2, Q3, Q7, Q8, Q9, Q10, Q11, Q14, Q15); 0 questions with evidence found.
Security lead: 4 gaps (Q4, Q5, Q6, Q13); 1 question with evidence found (Q12).

DECISIONS FOR THE HEAD TEACHER: 3
1. Whether the school business manager puts the question pack to Vendor A now, before the leads assess, with 63 days to the planned start, Tuesday 12 January 2027, counted from Tuesday 10 November 2026.
2. Who reviews D5, the master services agreement, which was not read, and by when.
3. Whether to adopt Tool A, and on what terms, after the privacy lead and the security lead have assessed the answers and the gaps above. Nothing is recommended.

NOT SUPPLIED OR NOT CHECKED
D5 was not read. The school's own criteria were not supplied, so the standard questions were used. Collected but in no category supplied: school-assigned ID, device type, sign-in times. Statements were not checked with Vendor A. Nothing else is missing.

Every statement traces to the documents supplied on 10 November 2026. The assistant gave no legal or regulatory opinion, rated no vendor and read no contract. Nothing has been sent, approved or changed.
```

## What was observed

Every part of the output format was produced, in order. Nothing in the inputs triggered a stop: headers matched, controlled values were allowed, no row held a person's name, and no password or key was present. D5 was listed as not read and nothing from it was used. The question wording is the template's own, so the pack is the same for anyone running it on this school. The totals add up (1 + 3 + 8 + 1 + 2 = 15), the 14 gaps equal the questions without evidence found, 63 days and the weekdays were checked against the calendar, and D4 is 19 whole months old. Every quotation was counted and is 15 words or fewer, and each was found in the document and paragraph cited. The invented names are letters (School A, Tool A, Vendor A, Auditor X) or obviously invented companies (Hosting Company B, Speech Company C, Email Company D); no real company is named.

Judgment calls and places the rules still leave open:

- **Staff data in Q3.** D1 paragraph 2 says "student data", so the coverage rule leaves teacher data (C3) unanswered and Q3 is PARTLY ADDRESSED. A reader who treats the sentence as covering all data would reach VENDOR STATEMENT ONLY.
- **Q2 destinations.** The hosting entry (D3 item 1) is listed as a destination for the data in general, but it does not name a category, so the missing part still says where C1, C2 and C3 go. The rule that subprocessor entries do not name categories decided this.
- **Q6 and Q15.** D2 paragraph 2 (access "is logged") answers Q4's third part and is mapped there only; Q6 asks about the school's own view of the record. D1 paragraph 4 and D2 paragraph 4 say how long recordings are kept, so they go to Q7 and the Q15 line names them as nearby passages. Both questions are NOT ADDRESSED.
- **Q12.** It is EVIDENCE FOUND because a passing report's own statement of product, issuer, scope and period answers a question about which reports exist. The line says "Reports supplied only". This is deliberately narrow: no other question reached EVIDENCE FOUND, because the audit summary does not name what it examined.
- **Q7.** DOCUMENTS DIFFER applies to recordings only. The other items are answered by D1 paragraph 3 and nothing conflicts with it.
- **Event-bound periods.** "As long as the school's account is active" is accepted as a stated period for the other items in Q7, because it is tied to a named event. The template now says so; a reader who wants a calendar period would mark those items missing and Q7 would still be DOCUMENTS DIFFER.
- **Q9 to Q11 across categories.** These are answered for the data as a whole, so Q9 is VENDOR STATEMENT ONLY for C1 to C4 although the subprocessor entries do not say which categories each company receives. Q2, which asks where each item goes, is answered by category and is PARTLY ADDRESSED for that reason. A reader who applied the category rule to Q9 would reach PARTLY ADDRESSED.
- **Data in no category.** The school-assigned ID, device type and sign-in times are named on the Q1 line and under not supplied, and no category was added.
- **Q13.** "Without undue delay" is not a stated time, so the second part is unanswered.
- **Q5 parts (b) and (c).** "School administrators assign teacher and student roles" is read as answering both how permissions are given and who controls roles. A reader who wanted separate statements would mark part (c) unanswered and Q5 PARTLY ADDRESSED.
- **Q10 and removal of a subprocessor.** D3 item 4 gives notice only for "adding a subprocessor", while the question asks about "changes to those companies". Removal or replacement is not covered by the quotation. The run treated notice of an addition as answering the question, so Q10 is VENDOR STATEMENT ONLY; a strict reader would mark it PARTLY ADDRESSED, missing notice of removal or replacement.
- **Not a clean test of the rules.** Some rules were written after the first run to settle what it had left open, and this run applied them. The example's output is the output of this run, not an independent expectation.

No instruction was refused or stopped for. Nothing was sent, and no fact was added beyond the documents.

## Differences from the earlier runs

This run, against the second, changes only the wording of one invented input and the quotations on the Q5, Q11 and Q12 lines; the totals are the same (1 / 3 / 8 / 1 / 2).

The first run (replaced) used its own question wording and got 1 / 5 / 8 / 1 / 0 for evidence / vendor statement only / partly / differ / not addressed. This run, with the template's wording, gets 1 / 3 / 8 / 1 / 2. Dates are in words and the closing line has no weekday, the unread agreement carries the template's fixed reason, and the leads' question numbers are in number order.
