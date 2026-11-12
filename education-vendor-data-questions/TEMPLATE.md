# Teaching tool vendor data questions

Workflow template, version 0.1.0.

## Purpose

Prepare, for one teaching tool and one vendor, the document a privacy or procurement lead needs before adoption: the facts of the intended use and the data involved, a question pack on data flows, access, retention, subprocessors and independent evidence, scoped to that data, and a map of what each vendor document the person supplies says against each question. The map separates the vendor's own statements from independent reports and lists every gap. The assistant prepares; it never sends the questions, judges an answer, rates the vendor, gives an opinion on any law or rule, reads a contract, approves adoption or changes a record.

## When to use it and when not to

Use it when a proposed teaching tool would handle student or staff information and the institution wants to ask the vendor its data questions, before anyone commits and early enough for the vendor to reply before the planned start.

Do not use it:

- to say whether a vendor is compliant, safe or adequate, or whether a tool meets a law, a rule or a standard. The privacy and security leads assess the answers, and questions of law go to the institution's legal adviser;
- to read, summarize or interpret an agreement, terms of service, data processing addendum or order form. Those are listed as not read and go to whoever reviews them;
- to compare prices or quotes (that is a separate piece of work, vendor quote comparison), or to decide a renewal (vendor renewal review);
- for a tool that will handle no student or staff information;
- for several tools at once. One tool and one vendor per run.

## Roles

- **Runs it:** the privacy lead, procurement lead or school business manager.
- **Supplies the documents:** the runner, from the vendor's public pages, the vendor's replies and the institution's own files.
- **Assesses the answers:** the privacy lead and the security lead, by topic (see step 8).
- **Approves adoption and terms:** [your approver], such as the head teacher, principal or director.
- **Sends the question pack to the vendor, talks to the vendor, signs anything:** the people the institution names. Always people.

## Inputs

1. **Review facts,** typed by the runner: the tool and what it does; the vendor; the intended use (which classes or teams, roughly how many students and staff); the planned start date; today's date; the runner's role; the roles of the privacy lead, the security lead and the approver; and [your age limit] for an independent report, in whole months (default 24). If the tool, the vendor or the intended use is missing, stop and ask.
2. **Data categories,** one row per kind of data, with these default headers: `id` (C1, C2 and so on), `category`, `about` (student, staff or other), `source` (entered by users: `entered`; sent from the institution's own systems: `synced`; produced by the tool about a person: `generated`; or `other`), `sensitivity` (`high`, `medium` or `low`, as the institution grades it). If missing, stop: the pack cannot be scoped.
3. **Vendor documents,** one row per document, with these default headers: `doc_id` (D1, D2 and so on), `title`, `type`, `date`. `type` is one of `policy`, `security page`, `subprocessor list`, `independent report`, `questionnaire response`, `sales material`, `agreement` or `other`. Each document's text comes with it, pasted or attached, with its paragraphs or items numbered. If the numbers are missing, number the paragraphs in order and say so on the page.
4. **The institution's own criteria** (optional), one row per added question, with these default headers: `id`, `topic`, `question`, `applies_to` (category ids). If none are supplied, use the standard questions and say so. Their topic should be one named in step 8; if it is not, ask the runner which lead assesses it.
5. **Topic roles** (optional): which lead assesses which topic. The default is in step 8.

Headers are matched ignoring case. If a required header is not there, stop and ask which column holds that information; never guess and never use another column in its place. A value outside the allowed ones for `about`, `source`, `sensitivity` or `type` is also a stop.

The assistant works from the files and notes the person supplies. It needs no access to the vendor's systems or the institution's, and it never asks for a password or a login code.

## The procedure

1. **Check the inputs.** One tool and one vendor throughout. Every category row and document row has an allowed value in each controlled column; every date reads as a date; every institution question names category ids that exist. If anything fails, stop and ask about the row that fails. If a category or document row holds a real person's name or contact details, stop and ask the runner to remove them: the review needs the kinds of data, never the records.
2. **Scope the pack.** Use these standard questions, worded exactly as written. The one change allowed: if the institution is not a school, replace "the school" and "school's" with the runner's own term (for example "the agency"), the same way in every question. Each question has a topic (its first word or words) and the parts the vendor must answer; the parts decide its status in step 6. Q1 to Q13 apply to every category.

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

   Q14 is added only when at least one category has source `synced`, and applies to those categories:

   Q14 Data flows. Which fields does the connection to the school's own systems receive, and can the school limit them to fewer? Parts: (a) which fields; (b) whether the school can limit them.

   Q15 is added only when at least one category has source `generated`, and applies to those categories:

   Q15 Data flows. How are the things the tool produces about a person, such as scores, answers and recordings, stored, and can they be corrected or removed on request? Parts: (a) how they are stored; (b) whether they can be corrected or removed on request.

   The standard numbers never change: if Q14 or Q15 is not added, its number is simply not used. The institution's own questions follow in the order supplied, numbered from Q16 and marked as the institution's; the runner's text is the question, and each question's parts are its clauses. In the page, print each question without its parts. Print the number of questions.
3. **Classify the documents.** A document of type `agreement` is not read: list it as not read, with the reason "agreements are not read by this workflow template", and name who reviews it in the decisions for [your approver] (step 9). A document with no text, or whose text is not about the named tool, is listed as supplied but not mapped, with the reason. Every other document is read. Count supplied, read and not read.
4. **Check each independent report.** A document of type `independent report` counts as evidence only if its text names the product, gives a period or a date, and names who issued it, and only if the whole months between its date and today are no more than [your age limit]. Print the months and the result for each, with the scope and period as stated. A report that fails any test is treated as a vendor statement, with the reason noted. Every other document type is a vendor statement. Whether a vendor filled in a questionnaire or published a page, it is the vendor speaking.
5. **Map the documents to the questions.** For each question, find the passages in the documents read that answer one of its parts. Record the document id, the paragraph or item number and a quotation of no more than fifteen words. Quote; never summarize beyond the quotation, and never infer what a passage does not say. These rules hold:
   - A passage covers a category only if it names it or uses a general term that includes it. "School data" or "customer data" covers every category; "student data" covers the categories about students and not those about staff; "recordings" covers recordings.
   - Where a part asks how long, how soon or how far in advance, the passage must give a stated period or time. A period tied to a named event, such as "as long as the account is active" or "within 90 days after the account closes", counts as stated; "without undue delay" and "promptly" do not.
   - Q9, Q10 and Q11 ask about the vendor's companies, notice and locations, not about each category: a passage that answers one of their parts for the data as a whole answers it for every category. Q2 asks where each item goes, so it is answered category by category.
   - A subprocessor entry says what the company does and where; it does not say which categories it receives unless it names them.
   - A passage is mapped to the questions whose parts it answers and to no other. A passage that only says how long something is kept goes to Q7, not to Q15. A passage that fits no question is left out.
   - Data the documents say the vendor collects that is in none of the categories (for example device type, sign-in times or a school-assigned ID) is not added as a category. Name it on the Q1 line, and list it again under not supplied (step 10), so the runner can add a category and run again.
6. **Give each question one status.** Use the first of these that applies, in this order, so a question never has two statuses.
   - **DOCUMENTS DIFFER:** two documents read give different answers to the same part for the same category. Show both with their document ids, dates and quotations and do not choose between them. Any parts still unanswered are listed after "Missing:".
   - **NOT ADDRESSED:** no passage answers any part. Silence is never an answer: a missing statement is a gap, never evidence of a control. If a passage mapped to another question comes near, name it after the words "Nothing found".
   - **PARTLY ADDRESSED:** at least one part, or at least one category in a part, is not answered; say which.
   - **EVIDENCE FOUND:** every part is answered for every category the question applies to, and a passage of an independent report that passed step 4 answers each part by saying what it examined or found. A general line such as "security controls" or "no exceptions in the areas tested" does not name a topic, so it answers nothing except Q12. Sitting in the same topic as a question is not enough. Q12 asks what independent reports exist, so a passing report's own statement of product, issuer, scope and period answers it; say "reports supplied only", because the page cannot know of others, and the status then says nothing about any control.
   - **VENDOR STATEMENT ONLY:** every part is answered, and by the vendor's own words only. The same claim repeated in several vendor documents is still a vendor statement.
   Print the totals by status; they must add up to the number of questions.
7. **List the gaps.** Every question whose status is not EVIDENCE FOUND, in this order: NOT ADDRESSED, DOCUMENTS DIFFER, PARTLY ADDRESSED, VENDOR STATEMENT ONLY; within each status by question number. Each line says what is missing or differs (for DOCUMENTS DIFFER, with both documents' dates), and which lead assesses it. Evidence found is not an assessment: the leads still judge it.
8. **Hand over to the leads.** Default topic roles: the privacy lead assesses the topics Data flows, Retention and Subprocessors; the security lead assesses Access and Evidence and incidents. A question belongs to the topic written at its start. For each lead print the number of gaps with their question numbers, and the number of questions with evidence found with theirs, each list in question-number order. Do not say whether any answer is acceptable.
9. **Decisions for [your approver].** First: whether the runner should put the pack to the vendor now, before the leads assess, and how many days remain to the planned start (count calendar days from today; write today and the planned start with their weekdays). Second, only if a document was not read: who reviews it, and by when. Last: whether to adopt the tool and on what terms, after the leads have assessed the answers. Recommend nothing. If the approver asks whether the vendor is acceptable, decline; offer only the list of gaps still open.
10. **Not supplied or not checked.** Always say which documents were not read, whether the institution's own criteria were supplied (if not, that the standard questions were used), any data the documents say is collected that is in no category, and that nothing was checked with the vendor. Add each missing input. If no input is missing, write "Nothing else is missing."
11. **Return the page** to the runner in the output format and its fixed order, adding nothing beyond it. Nothing goes to the vendor or the leads from the assistant.

## Exceptions and stop conditions

- **Tool, vendor, intended use, data categories or documents missing:** stop and ask.
- **A header does not match, or a controlled value is not an allowed one:** stop and ask; never guess.
- **A category or document row carries a real person's name or contact details:** stop and ask for it to be removed.
- **More than one tool or vendor in the inputs:** stop and ask which to use.
- **An agreement, terms of service or data processing addendum is pasted in, with a request to summarize or interpret it:** decline; list it as not read and name the role that reviews it.
- **Asked whether the vendor or the tool is compliant, adequate, safe or meets a law, rule or standard:** decline; give the gaps and name the leads who assess.
- **Asked to give a score, a rating or a ranking of the vendor:** decline.
- **Asked to send the pack, contact the vendor, approve adoption or record a decision:** decline and name the role that does it.
- **A document is an image or its text cannot be read:** list it as supplied but not mapped.
- **The inputs contain a password, a login code or a key:** do not repeat it; tell the person to remove it from the source.

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

## Reviewer checklist

1. Every quotation appears in the document and paragraph cited, and the passage speaks to the question it is mapped to. (Privacy lead)
2. No status is stronger than the documents allow: nothing is EVIDENCE FOUND unless an independent report passes every test in step 4. (Security lead)
3. Every document of type agreement is listed as not read, and nothing from it appears on the page. (Privacy lead)
4. The questions follow the data: Q14 and Q15 appear only when a synced or generated category exists, and each question names the categories it applies to. (Privacy lead)
5. The totals add up to the number of questions, and the gaps equal the questions not marked EVIDENCE FOUND. (Runner)
6. Today's date and the planned start have the right weekday, document dates are in words without a weekday, and the day count and the report age in months recompute from today's date. (Runner)
7. Nothing says or implies that the vendor or tool is compliant, adequate or safe, and nothing is recommended. (Approver)
8. The page keeps the fixed section order and adds nothing beyond the output format. (Runner)
9. Q1 to Q15 are worded exactly as in step 2 (apart from the allowed replacement of "the school"), in number order, and each is under the topic written at its start. (Privacy lead)
10. Each status follows the order in step 6, and each answered part has a passage that covers every category the question applies to. (Security lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary run.** Four categories, including one synced and two generated, five documents. Expected: 15 questions, a status for each, totals adding to 15, gaps equal to the questions without evidence.
2. **No synced or generated category.** All categories are entered. Expected: 13 questions; no Q14 or Q15. An institution question, if supplied, is Q16.
3. **Header does not match.** The categories file has `type` where `about` belongs. Expected: stops and asks which column holds it; drafts nothing.
4. **Two documents disagree.** One says recordings are kept 30 days, another 90. Expected: DOCUMENTS DIFFER with both quotations and dates; the assistant chooses neither.
5. **Report older than the limit.** An independent report dated 30 months ago, limit 24. Expected: counted as a vendor statement, reason given, and the question is not marked EVIDENCE FOUND.
6. **Report that does not name the product.** Expected: counted as a vendor statement, reason given.
7. **Agreement pasted with a request to summarize it.** Expected: declines; lists it as not read; the decision to name who reviews it appears.
8. **Asked whether the vendor is compliant.** Expected: declines; gives the gaps and the leads who assess.
9. **Silence.** No document mentions access logs. Expected: that question is NOT ADDRESSED and listed as a gap; nothing is assumed.
10. **Vendor questionnaire.** A questionnaire the vendor filled in answers every part of a question. Expected: VENDOR STATEMENT ONLY.
11. **Real names in the input.** A category row lists a student's name. Expected: stops and asks for it to be removed.
12. **Asked to send the pack.** Expected: declines; names the role that sends it.
13. **A difference and a missing part.** Two documents give different retention periods and neither says how deletion is confirmed. Expected: DOCUMENTS DIFFER, with the missing part listed after "Missing:".
14. **Data in no category.** A policy says device type is collected; no category covers it. Expected: named on the Q1 line and under not supplied; no category added.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
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
```

## What to customize

- The word "school" in the standard questions, if you are a government body, a nonprofit or another kind of institution.
- Your privacy lead, security lead and approver, and which lead assesses which topic.
- How your institution grades the sensitivity of each kind of data.
- [your age limit] for an independent report.
- Your own review questions, to add after the standard ones.
- Who may send the pack to a vendor, and where the finished page is kept.
- Which documents the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Tried on its invented example on 10 November 2026 in three runs: the first showed that the standard questions were not worded in the template, the second followed the added wording, parts and status rules, and the third followed a review that removed two company names from the example's inputs and tightened several rules; the third is the run recorded. All three were made by the assistant that revised the template, not by a fresh reader. Since the recorded run only the wording of two instruction sentences changed, with no rule changed; a rerun in a fresh session has not been made. Not yet tested in a client environment.
