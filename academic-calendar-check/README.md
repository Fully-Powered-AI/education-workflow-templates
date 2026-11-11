# Academic calendar check

While year, term and session dates are being assembled, your registrar gets a draft calendar with every registration window tied to its term, and every conflicting, missing or out-of-bounds date listed as a question. Nothing is published or changed.

*Capability template · Education · Operations and process improvement · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/academic-calendar-check/)*

## The outcome

The calendar reaches the registrar as one draft instead of a pile of proposals. Each year, term and session is listed with its dates, the term it belongs to and its registration window, so anyone can see at a glance what sits inside what.

The problems that normally surface after the dates are public are on the page before: two offices proposing different withdrawal deadlines, a grade deadline nobody supplied, a session that runs past its term, an add and drop date that falls after the withdrawal date, a deadline on a weekend or a closed day. Each arrives as a question for the registrar with the facts beside it.

Two sessions that overlap are listed too. The capability cannot know whether the overlap is planned, so it asks; the registrar says.

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

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where a dated calendar is a process that needs a check before it goes out.
- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/), where dated windows that depend on one another are tracked to a fixed outcome.
- [Education](https://fullypowered.ai/industries/education/), where the registrar publishes the year, term and session dates that students, departments and communications rely on.
- [Government](https://fullypowered.ai/industries/government/), where public schools and colleges publish a calendar that others plan around.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), for a company that runs its own school or training academy and assembles the dates from several offices.

## What has to change for your company

Name your own units: year, term, session, or whatever your institution calls them. Decide which dates each kind of unit must have; the defaults are a start. Decide the order rules you accept: for example, whether registration may stay open after classes begin, and whether add and drop must come before withdrawal. Supply your closed days and non-working weekdays. Say who confirms intentional overlaps, such as staggered sessions. It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply; it needs no connection to your student system.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example, on an earlier wording of the instructions, in Claude on 10 November 2026, and the record is published with it; that run saw the example's header counts early, which the record says. It has not been tested in a client environment or as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past year the registrar knows well, plus cases written in advance with the expected result: a withdrawal date proposed twice, a term with no grade deadline, a session that ends after its term, a deadline on a closed day. The registrar checks every date against the files before anyone relies on the draft. [Spreadsheet check before sharing](https://fullypowered.ai/capabilities/spreadsheet-check-before-sharing/) covers the same habit for any file that others will rely on.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete capability template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the capability drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related capabilities

- [Launch checklist](https://fullypowered.ai/capabilities/launch-checklist/)
- [Event plan](https://fullypowered.ai/capabilities/event-plan/)
- [Spreadsheet check before sharing](https://fullypowered.ai/capabilities/spreadsheet-check-before-sharing/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
