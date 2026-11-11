# Teaching tool vendor data questions

Before a school or college adopts a teaching tool that would handle student or staff information, the privacy or procurement lead gets a scoped question pack on data flows, access, retention and subprocessors, with each supplied vendor document mapped to the questions and the gaps listed.

*Capability template · Education · Compliance, risk and privacy · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/education-vendor-data-questions/)*

## The outcome

The people who must judge a teaching tool stop starting from a blank page. They get a short set of questions fitted to the data this tool would actually touch, ready to put to the vendor. Beside it, they get a map of what the vendor's own papers already say, question by question, and a plain list of what is still unanswered.

The map keeps two things apart that vendors often blur: what the vendor says about itself, and what an independent report supports. A silence in the documents is listed as a gap. It is never read as reassurance.

## Who starts the work, and when

A privacy lead, procurement lead or school business manager starts it when a teacher or department wants to adopt a tool and the proposal says student or staff information would go into it. It runs before anyone signs, and early enough that the vendor can answer before the planned start date.

## What they supply

- The tool, the vendor and the intended use: which classes or teams, how many students and staff, the planned start date.
- A list of the data categories involved: who each is about, where it comes from and how sensitive your institution treats it.
- The vendor documents you hold, with their type and date, and their text.
- Your own review criteria, if you have extra questions to add.
- The names of the roles that assess the answers and approve adoption.

## What comes out

One document in a fixed order: the intended use and data in scope, the documents and which were read, the question pack to put to the vendor, what each document says against each question and how strong that support is, the gaps in order, what each lead has to assess, and the decisions for leadership. Counts at the end of the mapping add up to the number of questions.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Compliance, risk and privacy](https://fullypowered.ai/functions/compliance-risk-and-privacy/), which owns the data questions a tool must answer before adoption.
- [Information security](https://fullypowered.ai/functions/information-security/), which assesses access, incident handling and the independent reports a vendor supplies.
- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/), where a teaching tool arrives as a purchase request.
- [Education](https://fullypowered.ai/industries/education/), where tools reach students and staff one department at a time.
- [Government](https://fullypowered.ai/industries/government/), for public bodies that adopt tools on behalf of citizens or pupils.
- [Nonprofits](https://fullypowered.ai/industries/nonprofits/), for training and youth programmes that hold personal information about the people they serve.

## What has to change for your company

Name your privacy lead, security lead and the person who approves adoption. Set how your institution grades the sensitivity of each kind of data, and how old an independent report may be before you ask for a newer one. Add the questions your own review criteria require, and decide which lead assesses which topic. Decide who may send the pack to a vendor. It runs in ChatGPT, Claude, Copilot or Gemini, from documents you supply.

This capability gives no legal or regulatory opinion, never declares a vendor compliant, and reads no contract. Those stay with the people and advisers your institution already relies on.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried on its invented example on 10 November 2026 in three runs, all made by the assistant that revised the template rather than by a fresh reader; the record of the third is published with it, and since then only the wording of two instruction sentences has changed, with no rule changed. A rerun in a fresh session has not been made. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a tool you have already assessed, with cases written in advance: two documents that disagree, an audit report older than your limit, an agreement pasted in, a header that does not match. The privacy lead checks every mapped quotation against the vendor's document before anyone relies on the page. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Vendor quote comparison](https://fullypowered.ai/capabilities/vendor-quote-comparison/)
- [Vendor renewal review](https://fullypowered.ai/capabilities/vendor-renewal-review/)
- [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
