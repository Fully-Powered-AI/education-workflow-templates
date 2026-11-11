# Fully Powered Capability Templates: Education

A term that starts ready. These capability templates are written for the administrative side of education. They prepare the checking and setting up around calendars, catalogs and courses. They grade nothing and decide nothing about a student: the institution's people do.

This repository holds 6 capability templates for the administrative staff of schools, colleges and training providers. Each one is a single piece of work with its own folder: what it is for and who starts it, the complete template an AI assistant follows, a worked example with invented data, what to change for your company, what has been checked, and its sources.

## The capabilities

- **[Academic calendar check](academic-calendar-check/)**: While year, term and session dates are being assembled, your registrar gets a draft calendar with every registration window tied to its term, and every conflicting, missing or out-of-bounds date listed as a question. Nothing is published or changed.
- **[Course catalog quality check](course-catalog-quality-check/)**: The registrar's office gets one comparison of a department's course updates against the current catalog export: codes, titles, credits, descriptions and linked components, row by row, with every conflict set out as a question for academic review. No catalog record is changed.
- **[Course sequence and workload review](course-sequence-and-workload-review/)**: A course lead revising an outline for the next cohort gets a module map: learning goals, prerequisites, activities and the instructor's own time estimates, with crowded weeks and coverage gaps marked and every gap written as a question. The course lead decides what changes.
- **[Teaching tool vendor data questions](education-vendor-data-questions/)**: Before a school or college adopts a teaching tool that would handle student or staff information, the privacy or procurement lead gets a scoped question pack on data flows, access, retention and subprocessors, with each supplied vendor document mapped to the questions and the gaps listed.
- **[Learning system access review](learning-system-access-review/)**: At term end or after staff change roles, the system owner lays the learning system's user and access exports beside current staff, class assignments and the approved role matrix. Departed users, changed roles and dormant accounts come back as questions for the data owners. Nothing is changed.
- **[Online class setup packet](online-class-setup-packet/)**: The learning-platform administrator receives one complete request for an approved class: course name, section, room, responsible teacher, the people who can be invited and every roster exception, drawn from the approved details and the roster export.

## How to use one

Open a folder and start with its README. Every folder stands alone, so copy the one you want and leave the rest. The templates are written for ChatGPT, Claude, Copilot and Gemini: paste the instruction block and the output format in as custom instructions, or load the folder in a product that reads `SKILL.md` packages.

In every template a person starts the work, supplies the inputs and decides. The template prepares and checks. Anything that sends, posts, pays or changes a record waits for a person to approve it.

## What SKILL.md is

Each folder holds a file named `SKILL.md`. It is the technical file: the same instructions and output format as the template, in the packaged form that AI products which load instructions from a folder read. It is generated from `TEMPLATE.md`, so the two always agree. The capability template is the whole folder; `SKILL.md` is one way of loading it. If your AI product does not read that format, use `TEMPLATE.md`.

## What "checked" means here

Each folder says exactly what was checked and when: who wrote it, that its sources and rights were reviewed, the date of its editorial review, and whether it has been tried on its invented example in a named AI product. Nothing is described as tested for a client unless it was. Test a template on your own past work before your team relies on it; each one comes with acceptance tests for that.

## More capabilities

The [Fully Powered Capabilities Directory](https://fullypowered.ai/capabilities/) lists every capability across functions and industries, with search. A machine-readable list of this repository is in [index.json](index.json).

## Licence and credits

MIT, in [LICENSE](LICENSE) and in every folder. Each folder's SOURCES.md names what the capability drew on. Published by [Fully Powered AI](https://fullypowered.ai/).
