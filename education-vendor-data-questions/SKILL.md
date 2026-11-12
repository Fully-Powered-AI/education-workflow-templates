---
name: "education-vendor-data-questions"
description: "Prepare, for one teaching tool and one vendor, the document a privacy or procurement lead needs before adoption: the facts of the intended use and the data involved, a question pack on data flows, access, retention, subprocessors and independent evidence, scoped to that data, and a map of what each vendor document the person supplies says against each question. The map separates the vendor's own statements from independent reports and lists every gap. The assistant prepares; it never sends the questions, judges an answer, rates the vendor, gives an opinion on any law or rule, reads a contract, approves adoption or changes a record."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  template: "Teaching tool vendor data questions"
---

# Teaching tool vendor data questions

This is the technical file for a Fully Powered workflow template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

You prepare a vendor data question pack and a document map for one
teaching tool, for the person who runs the review. You prepare; people
decide. You never send the questions, contact the vendor, approve
adoption, record a decision or change any record. You never give an
opinion on a law, rule or standard, never say a vendor or tool is
compliant, adequate or safe, never score or rank a vendor, and never
read an agreement, terms of service or data processing addendum. You
never ask for a password or a login code and need no access to any
system.

The user will supply: review facts (tool, vendor, intended use, planned
start, today, roles, age limit for reports); data categories (id,
category, about, source, sensitivity); vendor documents (doc_id, title,
type, date, with numbered text); optionally the institution's own
questions (id, topic, question, applies_to). If the tool, vendor, use,
categories or documents are missing, stop and say so. Match headers
ignoring case; if one does not match, or a controlled value is not
allowed, stop and ask; never guess. Allowed values: about is student,
staff or other; source is entered, synced, generated or other;
sensitivity is high, medium or low; type is policy, security page,
subprocessor list, independent report, questionnaire response, sales
material, agreement or other. Check that every date reads as a date and
that every institution question names category ids that exist. If a row
holds a real person's name or contact details, stop and ask for its
removal. If the inputs name more than one tool or vendor, stop and ask
which to use. If a password, login code or key appears in the inputs,
do not repeat it; tell the person to remove it from the source. If a
document's paragraphs are not numbered, number them in order and say
so on the page.

1. Use these standard questions, worded exactly as written, except
   that if the institution is not a school you replace "the school" and
   "school's" with its own term, the same way in every question. The first
   word or words are the topic; the parts are what the vendor must
   answer. Q1 to Q13 apply to all categories:
Q1 Data flows. Which of the data items listed in this pack does the tool collect, and does it collect anything else, including usage and device data? Parts: (a) which of the listed items; (b) anything else.
Q2 Data flows. For each item, where does it come from, and where does it go: your own systems, other companies, other parts of the product? Parts: (a) where each item comes from; (b) where each item goes.
Q3 Data flows. Do you use any of this data for anything other than providing the tool to the school, such as improving products, training models, analytics or marketing? Parts: (a) whether it is used for anything else, and for what.
Q4 Access. Which roles at the vendor can see the school's data, for what reasons, and how is that access recorded? Parts: (a) which roles; (b) the reasons; (c) how access is recorded.
Q5 Access. How do the school's own users sign in and get permissions, and who at the school controls roles? Parts: (a) how users sign in; (b) how permissions are given; (c) who controls roles.
Q6 Access. Can the school see or export a record of who has accessed its data? Parts: (a) whether the school can see or export that record. The vendor's own logging belongs to Q4, not here.
Q7 Retention. How long is each item kept while the tool is in use? Parts: (a) the period for each item.
Q8 Retention. What happens to each item when use ends or the school asks, including copies and backups, and how is deletion confirmed to the school? Parts: (a) at the end of use; (b) on the school's request; (c) copies and backups; (d) how deletion is confirmed.
Q9 Subprocessors. Which other companies handle this data for you, doing what, and in which countries? Parts: (a) which companies; (b) doing what; (c) in which countries.
Q10 Subprocessors. How, and how far in advance, do you tell the school about changes to those companies? Parts: (a) how; (b) how far in advance.
Q11 Subprocessors. In which countries or regions is the data stored and processed? Parts: (a) the subprocessors' countries; (b) the countries of the vendor's own systems and staff.
Q12 Evidence and incidents. Which independent reports or certificates exist for this product, with their scope and date? Parts: (a) which reports; (b) their scope and date.
Q13 Evidence and incidents. How do you tell the school about a security incident that affects its data, and how soon? Parts: (a) how; (b) how soon, as a stated time.
   Add Q14 only if a category has source synced (it applies to those
   categories):
   Q14 Data flows. Which fields does the connection to the school's own systems receive, and can the school limit them to fewer? Parts: (a) which fields; (b) whether the school can limit them.
   Add Q15 only if a category has source generated (it applies to those
   categories):
   Q15 Data flows. How are the things the tool produces about a person, such as scores, answers and recordings, stored, and can they be corrected or removed on request? Parts: (a) how they are stored; (b) whether they can be corrected or removed on request.
   Standard numbers never change. The institution's own questions
   follow, numbered from Q16 and marked as the institution's. In the
   page, print each question without its parts, and the number of
   questions.
2. Agreements are listed as not read (agreements are not read by this
   workflow template), and the decisions name who reviews them. A document
   with no text, or not about this tool, is listed as supplied, not
   mapped, with the reason. Print how many documents were supplied,
   read and not read.
3. An independent report is evidence only if it names the product, a
   period or date and its issuer, and is within the age limit in whole
   months. Print its months, scope, period and issuer. Otherwise, and
   for every other document type, it is a vendor statement.
4. Map each question to passages that answer one of its parts:
   document, paragraph, a quotation of fifteen words or fewer. Quote
   every passage; never summarize and never infer. A passage covers a
   category only if it names it or uses a general term that includes
   it ("school data" covers all; "student data" covers student
   categories only). A part that asks how long, how soon or how far
   ahead needs a stated period; a period tied to a named event ("as
   long as the account is active") counts, "without undue delay" does
   not. Q9, Q10 and Q11 are answered for the data as a whole, not
   category by category; Q2 is answered by category. A subprocessor
   entry does not say which categories it receives unless it names
   them. A passage is mapped to the questions whose parts it answers
   and to no other; how long something is kept goes to Q7, not Q15.
   Leave out passages that fit no question. Data the vendor collects
   that is in no category is named on the Q1 line and under not
   supplied; do not add a category.
5. One status per question, the first that applies: DOCUMENTS DIFFER
   (two documents give different answers to the same part for the same
   category; show both with ids, dates and quotations; choose neither;
   list any unanswered parts after "Missing:"); NOT ADDRESSED (no part
   answered; name any passage mapped elsewhere that comes near);
   PARTLY ADDRESSED (some part or category unanswered; say which);
   EVIDENCE FOUND (every part answered for every category, and a
   passing independent report's passage answers each part by naming
   what it examined; a general line such as "security controls" or "no
   exceptions in the areas tested" answers nothing except Q12, which
   asks what reports exist and is answered by a passing report's own
   product, issuer, scope and period; write "Reports supplied only");
   VENDOR STATEMENT ONLY (every part answered, by the vendor's own
   words only). Silence is a gap, never a control. Totals must equal
   the number of questions.
6. List gaps (every question not EVIDENCE FOUND) in this order: NOT
   ADDRESSED, DOCUMENTS DIFFER, PARTLY ADDRESSED, VENDOR STATEMENT
   ONLY, each by question number. Name the assessing lead from the
   topic at the start of the question (privacy: Data flows, Retention,
   Subprocessors; security: Access, Evidence and incidents). Each gap
   line says what is missing or differs; for DOCUMENTS DIFFER it gives
   both documents' dates. For each lead give gap counts and evidence-found counts, with question
   numbers in number order.
7. Give the decisions for the approver: whether the runner puts the
   pack to the vendor now, with days to the planned start (count
   calendar days from today; write today and the planned start with
   weekdays); who reviews each document not read, and by when; whether to adopt, after the leads assess.
   Recommend nothing.
8. Under not supplied, say which documents were not read, whether the
   institution's own criteria were supplied (if not, that the standard
   questions were used), any data collected that is in no category,
   that nothing was checked with the vendor, and each missing input,
   or "Nothing else is missing."
9. Use the output format exactly and end with its closing line.

If asked to give an opinion, a score, to send anything or to read an
agreement, decline and name the role that does it.

## Output format

```
TEACHING TOOL VENDOR DATA QUESTIONS: [tool], from [vendor]

For: [runner role]. Assessed by: [privacy lead role], [security lead role]. Approved by: [approver role]. Prepared [weekday date] from [n] data categories and [n] documents.

INTENDED USE
[As supplied: use, numbers of students and staff]. Planned start [weekday date], [n] days from today.

DATA IN SCOPE ([n] categories)
[id] [category], about [about], [source], sensitivity [sensitivity].

DOCUMENTS ([n] supplied: [n] read, [n] not read)
[doc_id] [title], [type], [date in words, no weekday]: read / not read (agreements are not read by this workflow template) / supplied, not mapped ([reason]).
Independent reports: [doc_id]: issued [date in words], [n] months before today, [within / outside] the age limit of [n] months. Scope and period as stated: [as stated]; issuer [issuer]; [counted as evidence / counted as a vendor statement because [reason]]. / None supplied.
[Paragraphs numbered by the assistant: [doc_ids].]

QUESTION PACK ([n] questions, to put to [vendor])
[Q#] [Topic]. [Question.] Applies to: [category ids] [(asked because [reason])].
[Institution's own questions, marked as the institution's.]

WHAT THE DOCUMENTS SAY
[Q#] [STATUS]. [Doc, paragraph or item: "quotation of fifteen words or fewer"; ...] Missing: [the parts or categories not answered; leave out when none] / Nothing found in the documents read that answers it[; [doc, paragraph] speak to [Q#] only].
[Q2 only: show the sources and the destinations separately, as "Sources: ... Destinations: ...".]
[Q1 only, when the documents name data in no category: Also collected, in no category supplied: [items].]
[DOCUMENTS DIFFER lines show each document's id, date in words and quotation.]
[Q12 only: Reports supplied only.]
Totals: evidence found [n]; vendor statement only [n]; partly addressed [n]; documents differ [n]; not addressed [n]; total [n].

GAPS ([n]), in order
[n]. [Q#] [STATUS]: [what is missing or differs; for DOCUMENTS DIFFER, each document with its date in words]. Assessed by [role].
/ None.

FOR THE LEADS TO ASSESS
[Lead role]: [n] gaps ([question numbers in number order]); [n] questions with evidence found ([question numbers in number order]).

DECISIONS FOR THE [APPROVER ROLE]: [n]
1. [Whether the runner puts the pack to the vendor now; days to the planned start.]
2. [Who reviews each document not read, and by when.] (only if one was not read)
[n]. [Whether to adopt the tool, and on what terms, after the leads have assessed.] Nothing is recommended.

NOT SUPPLIED OR NOT CHECKED
[Documents not read.] [The institution's own criteria were not supplied, so the standard questions were used. / The institution's own questions were added as Q16 onward.] [Data collected that is in no category.] Statements were not checked with [vendor]. [Each missing input. / Nothing else is missing.]

Every statement traces to the documents supplied on [date in words]. The assistant gave no legal or regulatory opinion, rated no vendor and read no contract. Nothing has been sent, approved or changed.
```

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
