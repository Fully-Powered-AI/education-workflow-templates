# Learning system access review: an invented example

*Illustrative example with invented data.* The academy, the people, the email addresses, the classes and the dates below are all invented. Halden Vale Academy is an invented school; its IT administrator runs the access review for the learning system on Monday 14 December 2026, three days after the autumn term ended. First come the inputs the IT administrator supplied, in full, then the review the workflow template returned.

## The inputs

### 1. Settings

```
System: Halden Vale Learning Hub
Term: Autumn 2026 (ended Friday 11 December 2026)
Review date: Monday 14 December 2026
Dormant after: 90 days
Run by: the IT administrator, for the system owner
```

### 2. Account export

```
account_id,name,email,account_type,system_role,permissions,course_access,last_login,status
A01,Priya Nair,p.nair@haldenvale.example,staff,Teacher,view roster; edit gradebook; edit course content,MA-9A; MA-10B,2026-12-10,Active
A02,Tomas Berg,t.berg@haldenvale.example,staff,Teacher,view roster; edit gradebook; edit course content,SC-8A; SC-9C,2026-12-09,Active
A03,Grace Okoye,g.okoye@haldenvale.example,staff,Teaching assistant,view roster; edit course content,EN-9A,2026-12-08,Active
A04,Henrik Soto,h.soto@haldenvale.example,staff,Teacher,view roster; edit gradebook; edit course content; view reports,EN-10A; EN-10B,2026-12-11,Active
A05,Amara Quill,a.quill@haldenvale.example,staff,Registrar,view roster; edit enrollment; export reports,all,2026-12-12,Active
A06,Leon Marsh,l.marsh@haldenvale.example,staff,System admin,manage users; manage roles; manage integrations,all,2026-12-13,Active
A07,Dana Whitlock,d.whitlock@haldenvale.example,staff,Teacher,view roster; edit gradebook; edit course content,FR-9B; FR-10A,2026-12-10,Active
A08,Ines Calder,i.calder@haldenvale.example,staff,Teacher,view roster; edit gradebook; edit course content,HI-9A; HI-10A,2026-08-30,Active
A09,Rory Pell,r.pell@haldenvale.example,staff,Teaching assistant,view roster; edit course content,SC-8A,,Active
A10,Maud Ferreira,m.ferreira@haldenvale.example,staff,Teacher,view roster; edit gradebook; edit course content,GE-9A,2026-09-01,Active
A11,Wren Abbott,w.abbott@haldenvale.example,staff,Course builder,edit course content,MA-9A,2026-12-02,Active
A12,Front Office Shared,frontoffice@haldenvale.example,shared,Registrar,view roster; edit enrollment,all,2026-12-12,Active
A13,svc-attendance-sync,svc-attendance@haldenvale.example,service,Integration,read roster; write attendance,all,2026-12-14,Active
A14,Jonas Reith,j.reith.s@haldenvale.example,student,Student,view own courses,,2026-12-11,Active
A15,Pia Lindqvist,p.lindqvist.s@haldenvale.example,student,Student,view own courses,,2026-12-09,Active
A16,Kofi Danso,k.danso.s@haldenvale.example,student,Teaching assistant,view roster; edit course content,SC-8A,2026-12-05,Active
A17,Nadia Oduya,n.oduya@haldenvale.example,staff,Teacher,view roster; edit gradebook; edit course content,GE-8A,2026-06-30,Suspended
A18,Imre Halloran,i.halloran@haldenvale.example,staff,Teaching assistant,view roster; edit course content,SC-9C,2026-12-04,Active
```

### 3. Current staff list

```
name,email,position,department,end_date
Priya Nair,p.nair@haldenvale.example,Teacher,Mathematics,
Tomas Berg,t.berg@haldenvale.example,Teacher,Science,2026-12-11
Grace Okoye,g.okoye@haldenvale.example,Teacher,English,
Henrik Soto,h.soto@haldenvale.example,Head of Department,English,
Amara Quill,a.quill@haldenvale.example,Registrar,Administration,
Leon Marsh,l.marsh@haldenvale.example,IT Administrator,Operations,
Dana Whitlock,d.whitlock@haldenvale.example,Teacher,Languages,
Ines Calder,i.calder@haldenvale.example,Teacher,Humanities,
Rory Pell,r.pell@haldenvale.example,Teaching Assistant,Science,
Wren Abbott,w.abbott@haldenvale.example,Teacher,Mathematics,
Imre Halloran,i.halloran@haldenvale.example,Teaching Assistant,Science,
Imre Halloran,i.halloran@haldenvale.example,Teacher,Science,
```

### 4. Class assignments, Autumn 2026

```
email,class,role_in_class
p.nair@haldenvale.example,MA-9A,Teacher
p.nair@haldenvale.example,MA-10B,Teacher
t.berg@haldenvale.example,SC-8A,Teacher
t.berg@haldenvale.example,SC-9C,Teacher
g.okoye@haldenvale.example,EN-9A,Teacher
g.okoye@haldenvale.example,EN-9B,Teacher
h.soto@haldenvale.example,EN-10A,Teacher
h.soto@haldenvale.example,EN-10B,Teacher
d.whitlock@haldenvale.example,FR-10A,Teacher
d.whitlock@haldenvale.example,FR-11A,Teacher
i.calder@haldenvale.example,HI-9A,Teacher
i.calder@haldenvale.example,HI-10A,Teacher
r.pell@haldenvale.example,SC-8A,Teaching assistant
w.abbott@haldenvale.example,MA-9A,Co-teacher
i.halloran@haldenvale.example,SC-9C,Teaching assistant
```

### 5. Approved role matrix

```
system_role,allowed_positions,permitted_permissions,scope,area
Teacher,Teacher; Head of Department,view roster; edit gradebook; edit course content,class,Gradebook
Teaching assistant,Teaching Assistant,view roster; edit course content,class,Courses and content
Registrar,Registrar,view roster; edit enrollment; export reports,system,Student records
System admin,IT Administrator,manage users; manage roles; manage integrations,system,System administration
```

### 6. System-owner list

```
area,data_owner
Gradebook,Deputy Head Academic
Courses and content,Head of Curriculum
Student records,Registrar
System administration,Head of Operations
```

## The output

**LEARNING SYSTEM ACCESS REVIEW: Halden Vale Learning Hub, Autumn 2026**

**For:** the system owner, and the data owners listed below. Review date 2026-12-14. Dormant after 90 days. Nothing has been changed.

**Compared:** 18 accounts, 12 staff list rows, 15 class assignments, 4 roles on the matrix. Not supplied or not usable: none.

**Tie-out:** 18 accounts = 2 student accounts not reviewed + 1 not active + 3 with no flag + 11 flagged + 1 that could not be assessed.

**Departed users with active accounts: 2**

- A02, Tomas Berg, t.berg@haldenvale.example. Role Teacher; permissions view roster, edit gradebook, edit course content; last sign-in 2026-12-09. Reason: end date 2026-12-11, on or before the review date. Also: none. Data owner: Deputy Head Academic. Question: the staff list shows an end date of 2026-12-11 and the account is active. Does the account stay, change or go?
- A10, Maud Ferreira, m.ferreira@haldenvale.example. Role Teacher; permissions view roster, edit gradebook, edit course content; last sign-in 2026-09-01, 104 days before the review date. Reason: email not on the staff list. Also: dormant. Data owner: Deputy Head Academic. Question: this email is not on the staff list and the account is active. Does the account stay, change or go?

**Role and permission differences: 5**

- A03, Grace Okoye, g.okoye@haldenvale.example. Position Teacher; role Teaching assistant; permissions view roster, edit course content; classes EN-9A; last sign-in 2026-12-08. Difference: changed role. The Teaching assistant role allows only the position Teaching Assistant. Also: none. Data owner: Head of Curriculum. Question: the position is now Teacher but the account holds the Teaching assistant role. Should the account hold a different role?
- A04, Henrik Soto, h.soto@haldenvale.example. Position Head of Department; role Teacher; permissions view roster, edit gradebook, edit course content, view reports; classes EN-10A, EN-10B; last sign-in 2026-12-11. Difference: permission beyond the role: view reports is not in the Teacher role's permitted permissions. Also: none. Data owner: Deputy Head Academic. Question: the account holds view reports, which the Teacher role does not allow. Does the permission stay, or does the matrix change?
- A07, Dana Whitlock, d.whitlock@haldenvale.example. Position Teacher; role Teacher; permissions view roster, edit gradebook, edit course content; classes FR-9B, FR-10A; last sign-in 2026-12-10. Difference: class access beyond assignments: FR-9B is not among the assigned classes this term. Also: none. Data owner: Deputy Head Academic. Question: the account reaches FR-9B, which is not assigned this term. Does that access stay?
- A11, Wren Abbott, w.abbott@haldenvale.example. Position Teacher; role Course builder; permissions edit course content; classes MA-9A; last sign-in 2026-12-02. Difference: role not on the matrix: Course builder. Also: none. Data owner: owner not assigned. Question: the Course builder role is not on the approved matrix and no owner is named for it. Who decides whether it stays?
- A16, Kofi Danso, k.danso.s@haldenvale.example. Position: none (student account); role Teaching assistant; permissions view roster, edit course content; classes SC-8A; last sign-in 2026-12-05. Difference: student account with a staff role. Also: none. Data owner: Head of Curriculum. Question: this is a student account holding the Teaching assistant role. Does the role stay, change or go?

**Dormant accounts: 2**

- A08, Ines Calder, i.calder@haldenvale.example. Role Teacher; last sign-in 2026-08-30, 106 days before the review date. Also: none. Data owner: Deputy Head Academic. Question: no sign-in for 106 days. Does the account stay, change or go?
- A09, Rory Pell, r.pell@haldenvale.example. Role Teaching assistant; never signed in. Also: none. Data owner: Head of Curriculum. Question: the account has never signed in. Does the account stay, change or go?

**Shared and service accounts: 2**

- A12, Front Office Shared. Type shared; role Registrar (on the matrix); permissions view roster, edit enrollment; last sign-in 2026-12-12. Also: none. Data owner: Registrar. Question: who uses this account, and for what?
- A13, svc-attendance-sync. Type service; role Integration (not on the matrix); permissions read roster, write attendance; last sign-in 2026-12-14. Also: none. Data owner: owner not assigned. Question: who uses this account, and for what?

**Classes assigned without access (information, not counted): 2**

- Grace Okoye, g.okoye@haldenvale.example: EN-9B assigned, not in the account's class access.
- Dana Whitlock, d.whitlock@haldenvale.example: FR-11A assigned, not in the account's class access.

**Could not be assessed: 1**

- A18, Imre Halloran, i.halloran@haldenvale.example. Reason: the email appears twice on the staff list, as Teaching Assistant and as Teacher. Data owner: Head of Curriculum.

**Decisions by data owner: 12**

- Owner not assigned: 2 accounts: A11, A13.
- Deputy Head Academic: 5 accounts: A02, A04, A07, A08, A10.
- Head of Curriculum: 4 accounts: A03, A09, A16, A18.
- Registrar: 1 account: A12.

This review compares exports. It changes no permission, disables no account, contacts no one and recommends no decision. The data owners decide; the IT administrator acts only on what they approve.
