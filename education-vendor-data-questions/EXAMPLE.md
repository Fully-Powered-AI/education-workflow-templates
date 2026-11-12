# Teaching tool vendor data questions: an invented example

*Illustrative example with invented data.* The school, the tool, the vendor, the companies, the people, the dates and the documents below are all invented. The school is an invented secondary school, School A, whose English department wants to adopt Tool A, an online reading-practice tool from Vendor A. The business manager is preparing the review for the privacy lead and the security lead, with the head teacher approving. First come the inputs the business manager supplied, in full, then the document the workflow template returned.

## The inputs

### 1. Review facts (typed by the business manager)

```
Tool: Tool A, online reading practice with read-aloud recording
Vendor: Vendor A
Intended use: Year 7 to 9 English classes, about 420 students and 28 teachers
Planned start: Tuesday 12 January 2027
Today: Tuesday 10 November 2026
Runner: school business manager
Privacy lead: privacy lead
Security lead: security lead
Approver: head teacher
Age limit for independent reports: 24 months
```

### 2. Data categories (5 columns)

```
id,category,about,source,sensitivity
C1,Student name and class,student,synced,medium
C2,Reading scores and answers,student,generated,high
C3,Teacher name and work email,staff,entered,medium
C4,Student voice recordings,student,generated,high
```

### 3. Vendor documents

```
doc_id,title,type,date
D1,Privacy policy,policy,2026-08-14
D2,Security overview page,security page,2026-09-02
D3,Subprocessor list,subprocessor list,2026-09-02
D4,Independent audit summary,independent report,2025-03-30
D5,Master services agreement,agreement,2026-08-01
```

Text of D1 (paragraphs numbered by the business manager):

```
1. Tool A collects the name, class and school-assigned ID that a school sends us, the answers and scores a student produces, and audio a student records during read-aloud tasks. We also collect device type and the times a student signs in.
2. We use student data to provide the service and to improve our products. We do not sell student data.
3. We keep school data for as long as the school's account is active and delete it within 90 days after the account closes.
4. Voice recordings are stored for 30 days and then removed.
```

Text of D2:

```
1. Data is encrypted in transit and at rest.
2. Vendor staff access to customer data is limited to the support and engineering teams, and that access is logged.
3. Schools sign in with single sign-on through the accounts the school already uses. School administrators assign teacher and student roles.
4. Recordings are retained for 90 days to support teacher review.
5. If we confirm a security incident affecting school data, we tell affected schools without undue delay.
```

Text of D3:

```
Subprocessors
1. Hosting Company B: cloud hosting, Ireland.
2. Speech Company C: speech-to-text for recordings, United States.
3. Email Company D: sending sign-in and notification emails, United States.
4. We give schools 30 days' notice before adding a subprocessor, by email to the account administrator.
```

Text of D4:

```
1. Auditor X examined the security controls of the hosted Tool A service for the period 1 January 2024 to 31 December 2024. The report is dated 30 March 2025.
2. The summary states that no exceptions were noted in the areas tested.
```

D5 was supplied as a file; its text is not pasted here.

### 4. The school's own criteria

None supplied.

## What the workflow template returned

The page below is the output of the run recorded in `trial.md`, on exactly these inputs.

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
D5 Master services agreement, agreement, 1 August 2026: not read (agreements are not read by this workflow template).
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
