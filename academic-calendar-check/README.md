# Academic calendar check

A draft academic calendar with every registration window tied to its term, and conflicting or missing dates listed as questions. The registrar decides.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** This is a template, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See Academic calendar check on our website](https://fullypowered.ai/workflows/academic-calendar-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check). Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Quick start**

1. Read EXAMPLE.md to see what a good result looks like.
2. Copy all of TEMPLATE.md into your assistant, then give it your own inputs, or the sample ones from EXAMPLE.md.
3. Read what comes back. It marks what it checked and what is left for you.

*Workflow template · Education · Operations and process improvement · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/academic-calendar-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check)*

## The outcome

The calendar reaches the registrar as one draft instead of a pile of proposals. Each year, term and session is listed with its dates, the term it belongs to and its registration window, so anyone can see at a glance what sits inside what.

The problems that normally surface after the dates are public are on the page before: two offices proposing different withdrawal deadlines, a grade deadline nobody supplied, a session that runs past its term, an add and drop date that falls after the withdrawal date, a deadline on a weekend or a closed day. Each arrives as a question for the registrar with the facts beside it.

Two sessions that overlap are listed too. The workflow template cannot know whether the overlap is planned, so it asks; the registrar says.

Your registrar still owns the calendar. The AI assistant picks no date between competing versions, invents none that is missing, and updates no student system, notice or web page.

## Who starts the work, and when

The registrar, or the person in the registrar's office who assembles the calendar, starts it when the proposed dates for a year are collected, and again each time an office sends a changed date. The registrar reads the draft and decides every finding before any record or notice is updated.

## What they supply

- **The structure.** Each year, term and session, and which unit it belongs to.
- **The date proposals.** Each proposed date or window: the unit, what kind of date it is, the dates, the version and who proposed it.
- **The closed days.** The days the institution is shut, such as recesses.
- **A few settings.** Today's date, the non-working weekdays and, if you want a different list, the dates each kind of unit must have.

## What comes out

One draft calendar, in date order, with each term followed by its sessions. Under it, the numbered findings in a fixed order: structure problems, conflicting versions, missing dates, dates outside their term, dates in the wrong order, overlaps to confirm, and dates on non-working days. A group with nothing in it says so.

Every date shows the proposal it came from, so each line can be checked against the file the offices sent. A conflicting date shows all its versions and no chosen one.

See the worked example in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check), where a dated calendar is a process that needs a check before it goes out.
- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check), where dated windows that depend on one another are tracked to a fixed outcome.
- [Education](https://fullypowered.ai/industries/education/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check), where the registrar publishes the year, term and session dates that students, departments and communications rely on.
- [Government](https://fullypowered.ai/industries/government/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check), where public schools and colleges publish a calendar that others plan around.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check), for a company that runs its own school or training academy and assembles the dates from several offices.

## What has to change for your company

Name your own units: year, term, session, or whatever your institution calls them. Decide which dates each kind of unit must have; the defaults are a start. Decide the order rules you accept: for example, whether registration may stay open after classes begin, and whether add and drop must come before withdrawal. Supply your closed days and non-working weekdays. Say who confirms intentional overlaps, such as staggered sessions. It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply; it needs no connection to your student system.

## What has been checked

FullyPowered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once on its example, on an earlier wording of the instructions, in Claude on 10 November 2026, and the record is published with it; that run saw the example's header counts early, which the record says. It has not been tested in a client environment or as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past year the registrar knows well, plus cases written in advance with the expected result: a withdrawal date proposed twice, a term with no grade deadline, a session that ends after its term, a deadline on a closed day. The registrar checks every date against the files before anyone relies on the draft. [Spreadsheet check before sharing](https://fullypowered.ai/workflows/spreadsheet-check-before-sharing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check) covers the same habit for any file that others will rely on.

- Written by FullyPowered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example.
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

- [Launch checklist](https://fullypowered.ai/workflows/launch-checklist/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check)
- [Event plan](https://fullypowered.ai/workflows/event-plan/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check)
- [Spreadsheet check before sharing](https://fullypowered.ai/workflows/spreadsheet-check-before-sharing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=education-academic-calendar-check&from=gh-education-academic-calendar-check).
