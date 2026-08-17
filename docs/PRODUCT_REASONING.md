# Product Reasoning

## Observation

Most organisations do not suffer from a complete lack of information. They suffer from a lack of **usable context**.

Work information already exists across messaging, email, documents, presentations, calendars, project systems, knowledge bases, policies, internal portals, and people's memories. Better retrieval increases access to those information sources, but access alone does not guarantee that a future employee understands how to act.

## The workplace problem

The incoming employee often receives fragments of context and is told to ask questions when something is unclear. That instruction assumes the person already knows where the ambiguity is.

They usually do not.

The outgoing employee has the inverse problem. Repeated experience turns operational knowledge into habit. Rules, exceptions, authority relationships, escalation paths, and stakeholder preferences can become so familiar that they no longer feel like knowledge worth explaining.

## Why documentation is insufficient

Traditional documentation can fail at multiple points:

- outcomes are recorded without reasoning;
- normal processes are documented without exceptions;
- materials become outdated;
- the incoming employee does not know which documents matter;
- valuable knowledge was never written down.

More documentation therefore does not automatically create better knowledge transfer.

## Reframing the problem

The useful distinction is:

- **Information** — what exists somewhere.
- **Knowledge** — understanding how to act.
- **Organisational memory** — knowledge that remains usable after the person who originally held it leaves.

The opportunity is not simply to retrieve more information. It is to turn fragmented information and human experience into persistent, validated, usable operational memory.

## Core product insight

The product should not claim that AI can magically discover tacit knowledge.

If knowledge was never expressed and left no observable signal, the system cannot know it exists.

The prototype therefore uses a narrower and testable interaction: **identify operational ambiguity that deserves clarification while the knowledge holder is still available**.

The system should not invent the missing answer. It should ask the human.

## Smallest hypothesis worth testing

Prototype v0.1 tests one assumption:

> Can a system identify operational ambiguity in a natural handover conversation and ask follow-up questions that the knowledge holder considers genuinely useful?

This is intentionally smaller than testing enterprise retrieval, integrations, permissions, organisational graphs, onboarding workflows, or agentic execution.

## Why the interaction starts with a knowledge dump

The outgoing employee is asked:

> Tell me what the next person needs to know. Don't organise it. Don't write a handover document. Just explain it naturally.

This avoids requiring the user to understand a schema before they begin. Their own work experience becomes the demo data.

A generic AI assistant might summarise this input. The prototype instead challenges it.

## Why one question at a time

The AI Challenge screen asks one meaningful follow-up question at a time because the experience should feel like attentive interrogation rather than an onboarding questionnaire.

A useful question should be:

1. traceable to something the user actually said;
2. focused on ambiguity that affects the ability to act;
3. specific enough to reveal missing operational context.

The intended response is: “I didn't realise I hadn't explained that.”

## Why the output is structured memory

Clarification only becomes reusable if the result can be transferred. The prototype therefore transforms the conversation into a Role Memory covering operational categories such as authority, approvals, workflows, exceptions, escalation, relationships, and unresolved questions.

Unknowns remain visible. The system does not convert absence of evidence into certainty.

## Why manager validation is exception-based

A handover should not become organisational truth simply because the outgoing employee said it.

The future model includes three human roles:

- the outgoing employee provides operational knowledge;
- the incoming employee tests whether it is understandable and usable;
- the manager / +1 validates important organisational rules.

Prototype v0.1 previews this by surfacing selected high-impact statements for confirmation, correction, or clarification rather than asking a manager to reread the entire handover.

## Why the readiness score is deliberately lightweight

A readiness percentage is useful as a communication mechanism for unresolved knowledge, but the prototype does not claim scientific completeness. Unknown unknowns can still exist.

The score is therefore a surface for discussion, not a measurement of organisational truth.

## Why enterprise data is deferred

Enterprise integrations introduce a separate set of questions: access, evidence quality, permissions, freshness, privacy, historical interpretation, and governance.

Those questions matter, but they are not necessary to test whether ambiguity-focused questioning is useful.

Prototype v0.1 therefore keeps the enterprise-data architecture visible only as a future hypothesis and separates it clearly from current capability.
