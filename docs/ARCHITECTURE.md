# Architecture

This document separates the architecture that exists in **Prototype v0.1** from the enterprise architecture that remains a **future hypothesis**.

## Prototype v0.1 — implemented

```text
Natural handover input
        ↓
Sentence / signal detection
        ↓
Ambiguity categories
        ↓
Traceable follow-up question
        ↓
Human clarification
        ↓
Structured Role Memory
        ↓
Unresolved gaps + readiness view
        ↓
Manager validation preview
```

### Runtime model

Prototype v0.1 is a dependency-free static browser application:

```text
index.html
   ├── styles.css
   └── app.js
```

`app.js` contains the current proof-of-concept questioning and structuring logic.

### Ambiguity detection

The local engine searches the user's own language for signals related to:

- responsibility;
- decision authority;
- approval;
- thresholds;
- dependencies;
- exceptions;
- escalation;
- relationships;
- preferences;
- uncertainty.

The generated question stores the source statement so the UI can show why the challenge was asked.

### Role Memory generation

The prototype groups the original handover and subsequent clarifications into operational categories. It preserves unresolved challenges as open questions and labels content as conversation-supported rather than manager-validated organisational truth.

### Manager validation preview

High-impact clarifications, particularly approvals, thresholds, exceptions, and escalation rules, can be surfaced for a simulated manager action:

- Confirm
- Correct
- Request clarification

This is an interaction preview only. Prototype v0.1 has no identity, workflow, persistence, or approval backend.

## Future enterprise hypothesis — not implemented

A future architecture could combine authorised sources such as:

```text
Enterprise IM        Email         Calendar
      \                |             /
       Documents — Knowledge Bases — Project Systems
                    |
          Organisational Directory
                    |
          Historical Role Memory
                    ↓
          Enterprise Context Layer
                    ↓
             Pattern Detection
                    ↓
          Knowledge Gap Detection
                    ↓
           Human Clarification
                    ↓
           Manager Validation
                    ↓
          Living Role Memory
```

The future question is not “can AI retrieve enterprise information?” It is whether authorised work traces can reveal **unexplained patterns, dependencies, and exceptions** that lead to better clarification questions.

The system should remain evidence-led. If formal documentation shows `A → B → C` but observed execution repeatedly shows `A → D → B → C`, a future system should not infer what `D` means. It should ask why `D` appears and what role it plays.

## Boundary

None of the following exist in v0.1:

- enterprise connectors;
- enterprise retrieval;
- RAG;
- knowledge graphs;
- authentication;
- permissions;
- production persistence;
- enterprise governance;
- production AI-agent execution.

They are intentionally outside the prototype architecture.
