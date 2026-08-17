# Interrogation Logic

## Behaviour principle

The prototype must not behave like a generic onboarding questionnaire.

Every question should ideally be **traceable to something the user actually said**.

Weak:

> Who are your key stakeholders?

Better:

> You mentioned Michelle when discussing product launches. What specifically requires her involvement?

Weak:

> Are there any exceptions?

Better:

> You said Finance normally reviews the budget. When would Finance not be involved?

The intended experience is that the system feels like it is **listening**, not running through a checklist.

## What the system looks for

### Responsibility

Question: who owns the outcome rather than simply performing part of the work?

Typical signals: `responsible`, `own`, `handle`, `manage`, `lead`.

### Decision authority

Question: who can decide, override, or make the final call?

This can be implied by urgency, thresholds, approvals, or named stakeholders.

### Approval

Question: is a person reviewing, advising, approving the work, approving budget, or simply being informed?

Typical signals: `approve`, `sign-off`, `review`, `look at`, `check`.

### Threshold

Question: at what point does the rule change, and how can the next person recognise that threshold?

Typical signals: `large`, `larger`, `major`, `significant`, `urgent`, `critical`.

### Dependency

Question: what must happen first, and what happens when that dependency is missing or late?

Typical signals: `before`, `after`, `depends on`, `once`, `until`, `then`.

### Exception

Question: when does the normal rule not apply, and who is allowed to use the exception?

Typical signals: `normally`, `usually`, `if`, `unless`, `except`, `skip`, `bypass`, `without`.

### Escalation

Question: what happens when the normal process fails, and when should escalation move to the next level?

Typical signals: `blocked`, `delay`, `fails`, `goes wrong`, `problem`, `escalate`.

### Relationship

Question: why is a named person involved, and what is the trigger for contacting them?

The existence of a name alone is not sufficient operational context.

### Preference

Question: is this a formal organisational rule or a stakeholder preference, and what happens if it is handled differently?

Typical signals: `prefer`, `likes`, `informal`, `formal`, `less formal`.

### Uncertainty

Question: what has been described but still cannot reliably guide action?

When no stronger signal is detected, v0.1 uses a fallback question asking what part would be easiest for a newcomer to misunderstand or act on incorrectly.

## Question priority

The current prototype prioritises ambiguity that is more likely to affect action:

- high: urgency, exceptions to normal rules, escalation;
- medium-high: approvals, dependencies, conditional exceptions;
- medium: preferences, responsibility;
- lower: named relationships when no stronger ambiguity is present.

This prioritisation is heuristic and should be evaluated, not treated as a universal rule.

## Traceability

For every generated challenge, the prototype retains:

```text
category
the user's source statement
the generated question
why the ambiguity matters
priority
```

The UI exposes the source statement under **Based on what you said**.

## Non-goal

The engine must not manufacture missing operational facts. If an answer is unknown, the gap should remain open.
