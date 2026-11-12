# Course catalog quality check

The registrar's office gets one comparison of a department's course updates against the current catalog export: codes, titles, credits, descriptions and linked components, row by row, with every conflict set out as a question for academic review. No catalog record is changed.

*Workflow template · Education · Operations and process improvement · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/course-catalog-quality-check/)*

## The outcome

When a department sends in a batch of course updates, the registrar's office sees, before anyone edits anything, exactly what differs from the catalog: which fields change on which courses, which rows match no current record, which links point nowhere, which values break the institution's own field definitions. The plain differences are listed as differences. Everything that needs a judgment is written as a numbered question, with its facts, for the people who decide.

Nothing is merged, filled in or guessed. A lecture and its lab stay two records, a modality variant stays its own record, and a blank credits cell stays blank. The registrar and the academic owners approve changes and decide what counts as the same course. The comparison is about courses only; it holds no information about any individual student.

## Who starts the work, and when

A member of the registrar's office, usually the catalog or curriculum coordinator, starts it when a department submits a batch of updates and before any change is entered in the catalog. The registrar reviews the comparison, sends the questions the registrar chooses to the department and academic owners, and passes approved changes to the student information staff who make them.

## What they supply

- The department's submission: one row per course, with code, title, credits, description, linked components and the kind of change.
- The current catalog export for the same department, with the same fields and the catalog's own record ID.
- The institution's field definitions: code pattern, title and description limits, how credits are written, the types of linked component.

## What comes out

One report in a fixed order: what was read, counts, a course-by-course comparison field by field, the conflicts for academic review as numbered questions each naming who decides, rows with no current record, and what was not checked. Every line traces to a submitted row and a catalog record.

See the worked example for what a finished report looks like.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Education](https://fullypowered.ai/industries/education/), in the registrar's office and the academic departments that feed it.
- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), because it turns a batch of updates into a clean, reviewable step before records change.
- [Quality management](https://fullypowered.ai/functions/quality-management/), as the check that catches missing credits, broken links and unclear course identity early.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where catalogs have grown over many years and the same course may exist under more than one code.

## What has to change for your company

Set your field definitions: the code pattern, title and description limits, how credits are written and the component types you use. Fix the column headers of your catalog export once, so the workflow template reads them without questions. Decide which differences go straight to the registrar and which go to the department chair or curriculum committee, and who decides questions of course identity. Decide whether modality is a column in your export or part of the code. Keep the catalog export as the single source: when a department's note and the export disagree, the export is the current record until a person approves a change.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026; the record is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past batch your registrar's office already worked through, with cases written in advance: a blank credits cell, a lecture whose lab is missing from the catalog, a new code with the title of an existing course. The registrar's office checks every line of the comparison against the catalog export before anyone relies on it.

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

- [Dataset profile](https://fullypowered.ai/workflow templates/dataset-profile/)
- [Spreadsheet check before sharing](https://fullypowered.ai/workflow templates/spreadsheet-check-before-sharing/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
