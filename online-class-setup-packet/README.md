# Online class setup packet

The learning-platform administrator receives one complete request for an approved class: course name, section, room, responsible teacher, the people who can be invited and every roster exception, drawn from the approved details and the roster export.

*Capability template · Education · IT and systems · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/online-class-setup-packet/)*

## The outcome

Setting up an online class stops being a chain of emails. The administrator opens one page and sees what the class is, who is responsible for it, who is cleared to be invited and which names need a person to settle before anything happens. The questions that usually surface halfway through setup, such as a teacher nobody has confirmed, a student listed twice or a status that says nothing, are already on the page with the facts.

The administrator still checks ownership and membership, creates the class and approves the invitations. The packet creates nothing and invites nobody.

## Who starts the work, and when

The academic office or the registrar's assistant starts it once a class is approved and its roster export is available, and hands the packet to the learning-platform administrator. It is run again when the roster export changes before the class opens.

## What they supply

- The approved class details: course code and name, section, term, room, meeting pattern, enrolment cap, the platform template to use and the approval reference.
- The teacher assignment, showing who is confirmed.
- The roster export the office already keeps, with its default column headers.
- The authorized invitation list: the people the school has cleared to be invited.
- Optionally, the statuses your office counts as enrolled, if they differ from the default.

## What comes out

One packet in a fixed order: the class request, the responsible teacher with confirmation status, counts that add up, the list of people who can be invited, numbered roster exceptions and the decisions left to the administrator. If an input does not match, the work stops and says which one and why.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [IT and systems](https://fullypowered.ai/functions/it-and-systems/), where the administrator receives class requests that arrive piecemeal and incomplete.
- [Executive and office support](https://fullypowered.ai/functions/executive-and-office-support/), where an academic office assembles the approved details and the roster.
- [Education](https://fullypowered.ai/industries/education/), where schools, colleges and training providers open classes every term.
- [Government](https://fullypowered.ai/industries/government/), where public training bodies and agencies run classes for staff or the public.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the same work repeats every term and a fixed packet saves the retelling.

## What has to change for your company

Use your own column headers for the roster and teacher files, or rename the defaults once. Decide which enrolment statuses count as enrolled. Name the platform templates you use so the packet can name the right one. Decide whether a class over its cap is an exception or only a note, and who may approve an invitation list. Keep the roster to what the office already holds: the packet needs a student number and a name, not contact details, grades or notes.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026; the record is published with it, and lists the points where the instructions were ambiguous. Edits made afterward to settle those points, and to add two parts to the output format, have not been run again; the trial record lists them. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a class the administrator has already set up by hand, plus hard cases written in advance: a teacher not yet confirmed, a student listed under two numbers, a blank enrolment status, a name on the invitation list who is not on the roster, a header that does not match. The administrator checks every line against the approval and the export before anyone relies on the packet. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Employee onboarding plan](https://fullypowered.ai/capabilities/employee-onboarding-plan/)
- [Shared folder filing plan](https://fullypowered.ai/capabilities/shared-folder-filing-plan/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
