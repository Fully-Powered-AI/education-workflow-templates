# Course sequence and workload review

A course lead revising an outline for the next cohort gets a module map: learning goals, prerequisites, activities and the instructor's own time estimates, with crowded weeks and coverage gaps marked and every gap written as a question. The course lead decides what changes.

*Workflow template · Education · People and HR · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/course-sequence-and-workload-review/)*

## The outcome

The course lead opens the revision with one map of the whole course instead of an outline, a spreadsheet of hours and a list of assessment dates read side by side. Every module shows what it is meant to teach, what it expects learners to know already, the activities in it and the hours the instructors have estimated for them. Week by week, the load is added up against the limit the course lead set, and the weeks that go over it are marked.

The review also looks for the quiet gaps. A learning goal that no activity teaches. A goal that is taught but never assessed, or assessed before it is first taught. A module that expects knowledge the course never provides and the entry requirements never mention. An activity linked to no goal at all. None of these is fixed or explained away: each becomes a question with the facts beside it.

Hours that were never estimated stay unknown. A week with a missing estimate is shown as "at least" its known total and is not judged until someone supplies the number.

The course lead decides the sequence, the workload and every change to the curriculum. The review does not grade, assess or evaluate any student, sets no learning standard, and makes no claim about whether a sequence teaches well.

## Who starts the work, and when

The course lead runs it when an outline is being revised for the next cohort, with the instructors' estimates and the assessment dates to hand. It suits any course that runs in weeks, with named modules and a list of outcomes: a semester unit, a short course, a training programme for staff. The course lead reads the map first, settles what can be settled with the teaching staff, and brings the rest to whoever approves curriculum changes.

## What they supply

- **Settings:** the course name, the course lead's role, the number of weeks, the limit on hours in a week and the limit on assessments due in a week, both set by the course lead, the entry requirements, and the date.
- **The learning outcomes,** as a list with the columns Outcome ID and Outcome.
- **The activities,** as an export with the columns Week, Module, Activity, Hours, Outcome IDs and Needs.
- **The assessments,** as an export with the columns Assessment, Due week and Outcome IDs.

## What comes out

One review in a fixed order: a status line with the counts; the module map; the load for each week against the course lead's limits; the coverage of each learning outcome; and the questions for the course lead, in the order they matter. Empty sections say so. The hours are the instructors' estimates, printed as supplied, and the review adds them up without adjusting any of them.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Education](https://fullypowered.ai/industries/education/), where the next cohort's outline is revised from the last one's and the pressure points are easy to miss across a spreadsheet.
- [Professional services](https://fullypowered.ai/industries/professional-services/), for the firms that run their own training programmes and certificate courses.
- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/), because a course is a sequence of dependent work with a load on each week.
- [Quality management](https://fullypowered.ai/functions/quality-management/), where the same question is asked of any programme: does what is promised have a place where it is taught and where it is checked.
- [People and HR](https://fullypowered.ai/functions/people-and-hr/), where learning and development plans what is taught, in what order and with what load on each week.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where a course has run before and is being revised rather than built.

It is different from [Project scope baseline](https://fullypowered.ai/workflows/project-scope-baseline/), which fixes what a project will deliver, and from [Training needs analysis](https://fullypowered.ai/workflows/training-needs-analysis/), which counts who on a team needs which training. This one reviews a course that already has an outline. [Recorded sessions into articles](https://fullypowered.ai/workflows/recorded-sessions-into-articles/) turns the sessions themselves into writing, once the course is running.

## What has to change for your company

Set the two limits yourself: the hours a week you consider a full load and the assessments you will allow in one week. The review applies no standard of its own. List your entry requirements as the exact phrases the Needs column uses. Decide who approves a change to the curriculum, since the review names the role but never decides. It runs in ChatGPT, Claude, Copilot or Gemini from the files you supply and needs no connection to your learning platform or student records. Do not include student names or results; it does not need them.

## What has been checked

Fully Powered AI wrote this workflow template from its own published map of the work, with no third-party text. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026 in two runs; the record of the second is published with it. The second run had already seen the example's published review, so a clean rerun from the inputs alone has not been done. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on the outline of a course you have just taught and know well, then checking the review against what the instructors and learners found hard: the week everyone said was too heavy, the outcome nobody got round to teaching, the topic that was assessed before it was covered. The course lead checks every line against the exports before the review goes to the teaching staff.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Project scope baseline](https://fullypowered.ai/workflows/project-scope-baseline/)
- [Training needs analysis](https://fullypowered.ai/workflows/training-needs-analysis/)
- [Recorded sessions into articles](https://fullypowered.ai/workflows/recorded-sessions-into-articles/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
