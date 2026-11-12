# Learning system access review

At term end or after staff change roles, the system owner lays the learning system's user and access exports beside current staff, class assignments and the approved role matrix. Departed users, changed roles and dormant accounts come back as questions for the data owners. Nothing is changed.

*Workflow template · Education · Information security · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/learning-system-access-review/)*

## The outcome

The people who decide who may see student records get one list instead of a hunch. Every account that no longer fits is on it, with the reason in plain words: the person has left, the person now holds a different position, the permissions go beyond what the role allows, the class access does not match this term's classes, or nobody has signed in for months. Each item is addressed to the data owner whose decision it is.

Shared and service accounts are listed every time, because no staff list can vouch for them. Anything the assistant cannot judge, such as an account with two possible matches, a role missing from the matrix or an area with no owner, is listed as a gap and left unguessed.

The data owners decide who keeps what. The IT administrator carries out whatever they approve and checks it. The assistant changes no permission, disables no account and asks for no sign-in details.

## Who starts the work, and when

The system owner or IT administrator starts it when a term ends, after a round of staff changes, or on the schedule your institution sets for access reviews. They supply the exports and decide the review date. The data owners read their part of the result and answer each question. The IT administrator acts only on what the owners have approved.

## What they supply

- **The account export:** one row per account, with the person's email, the account type, the system role, the permissions, the classes the account can reach, the last sign-in date and the status.
- **The current staff list:** each person's email, position, department and, if they are leaving or have left, an end date.
- **This term's class assignments:** which staff member teaches or supports which class.
- **The approved role matrix:** for each system role, the positions that may hold it, the permissions it allows, whether its reach is by class or across the system, and the area it belongs to.
- **The system-owner list:** who decides access in each area.
- **The settings:** the review date and the number of days without a sign-in that counts as dormant.

The export holds accounts and permissions only. No grades, no student work and no passwords belong in it.

## What comes out

One dated review in a fixed order, with a tie-out line that accounts for every row of the export: student accounts not reviewed, accounts not active, accounts with no flag, accounts flagged and accounts that could not be assessed. Then five lists: departed users with active accounts; role and permission differences; dormant accounts; shared and service accounts; and classes assigned without matching access. A cannot-be-assessed list and the decisions grouped by data owner close it.

Each flagged account is shown once, with its facts, any other flag it carries, its data owner and the question for that owner. The assistant recommends nothing and changes nothing.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Education](https://fullypowered.ai/industries/education/), where student records sit in the learning system and access should follow the term.
- [Nonprofits](https://fullypowered.ai/industries/nonprofits/), where volunteers and short-term staff hold accounts in the program and learning systems.
- [Government](https://fullypowered.ai/industries/government/), where training platforms and records systems need a periodic access check.
- [Information security](https://fullypowered.ai/functions/information-security/), which owns the question of who can reach what.
- [IT & systems](https://fullypowered.ai/functions/it-and-systems/), whose administrator carries out the approved changes.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where staff changes and role changes leave access out of step with the people who now hold the work.

It is a different piece of work from [the employee offboarding and handover checklist](https://fullypowered.ai/workflows/employee-offboarding-and-handover-checklist/), which follows one leaving person, and from [the software subscription and vendor spend review](https://fullypowered.ai/workflows/software-subscription-and-vendor-spend-review/), which looks at what is paid for rather than who can sign in.

## What has to change for your company

Use your own role names, positions and areas in the matrix, and agree it with the data owners before the first review. Set the dormant threshold your policy gives. Decide which account types are in scope and how a student account with a staff role is handled. Name an owner for every area, and a deputy for when the owner is away. Map your system's export columns to the default headers, or ask the assistant to stop and tell you which differ. Decide who receives each owner's list and by what date they answer.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026, and the record of that run is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past term your IT administrator already knows, with cases written in advance: a departed user, an account with two possible matches, a shared account, a role that is not on the matrix. The IT administrator checks every flagged account against the system itself before an owner relies on the list. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up.

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

- [Employee offboarding and handover checklist](https://fullypowered.ai/workflows/employee-offboarding-and-handover-checklist/)
- [Software subscription and vendor spend review](https://fullypowered.ai/workflows/software-subscription-and-vendor-spend-review/)
- [Employee onboarding plan](https://fullypowered.ai/workflows/employee-onboarding-plan/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
