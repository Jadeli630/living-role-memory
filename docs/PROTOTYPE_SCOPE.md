# Prototype v0.1 Scope

## Status

Prototype / Proof of Concept.

## Core assumption

Prototype v0.1 tests one assumption only:

> Can a system identify operational ambiguity in a natural handover conversation and ask follow-up questions that the knowledge holder considers genuinely useful?

## In scope

### 1. Knowledge Dump

A visitor can describe a real role, responsibility, or project naturally without preparing a dataset or writing a formal handover document.

### 2. AI Challenge

The prototype asks one follow-up question at a time. Questions should be traceable to something the visitor actually said and should prioritise ambiguity that affects the ability to act.

### 3. Living Role Memory

The conversation and clarifications are transformed into a structured view covering:

- Role / Responsibility
- Key People
- Decision Authority
- Approvals
- Dependencies
- Normal Workflows
- Exceptions
- Escalation Paths
- External Relationships
- Preferences
- Open Questions
- Confidence / evidence state

### 4. Unresolved knowledge gaps

Questions that the user cannot answer remain visible rather than being guessed.

### 5. Manager / +1 validation preview

The visitor can see how selected organisational rules could be confirmed, corrected, or returned for clarification.

### 6. Handover readiness

A lightweight readiness indicator surfaces unresolved areas. It is explicitly a communication mechanism, not a scientific completeness score.

### 7. Future vision separation

The interface explains the future enterprise hypothesis while clearly distinguishing it from current prototype capability.

## Explicitly out of scope

Prototype v0.1 does not build or claim:

- Microsoft 365 integration
- Teams or Outlook integration
- enterprise WeChat integration
- enterprise search
- large-scale RAG
- organisational knowledge graphs
- enterprise authentication
- permission architecture
- large document ingestion
- production compliance infrastructure
- sophisticated token optimisation
- full HR workflow
- complete onboarding system

## Definition of Done

Prototype v0.1 is complete when:

- [x] A visitor can open the product without preparing any data.
- [x] They can describe a real role, responsibility, or project naturally.
- [x] They receive context-specific follow-up questions.
- [x] They can answer conversationally.
- [x] The interaction is designed to create at least one meaningful “I hadn't explained that” moment.
- [x] The system generates a structured Role Memory.
- [x] Unresolved knowledge gaps are clearly identified.
- [x] The visitor can see how manager validation would work.
- [x] The long-term enterprise vision is understandable.
- [x] Current prototype capability and future hypotheses are clearly separated.

The fifth item is an **experience target**, not something the implementation can guarantee for every handover. It must be tested with users.

## Development priority

1. Quality of questioning
2. Quality of Role Memory structure
3. Manager validation interaction
4. Visual polish
5. Additional features

A visually polished prototype that asks generic questions fails the product test. A simple prototype that produces surprisingly relevant questions succeeds.
