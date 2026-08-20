# Living Role Memory

**An experimental AI-native approach to organisational knowledge transfer.**

> **Project status, August 2026:** v0.1 is complete. After a post-build market scan, I found substantial overlap with existing AI knowledge transfer products. I am not moving directly into v0.2. See [`docs/MARKET_RESEARCH_AND_DECISION.md`](docs/MARKET_RESEARCH_AND_DECISION.md) for the evidence and decision.

Enterprise AI is becoming increasingly capable of accessing organisational information. This prototype explores the next problem: **how do we turn information into operational memory?**

> Prototype v0.1 is a proof of concept. It tests one assumption only: can a system identify operational ambiguity in a natural handover and ask follow-up questions that the knowledge holder considers genuinely useful?

## The problem

A typical handover often sounds reasonable:

- “Marketing normally goes through Michelle.”
- “Ask David if anything comes up with PR.”
- “Most of the history is in the group chat.”
- “Have a look and ask me if anything is unclear.”

The structural problem is that the incoming person **does not yet know what they do not know**. The outgoing person has the opposite problem: after working in an environment for long enough, important operational rules can feel too obvious to recognise as knowledge that needs to be transferred.

Documentation helps, but documentation is not the same as knowledge transfer. Outcomes may be recorded without reasoning, normal processes without exceptions, and policies without the informal context needed to act effectively.

## The hypothesis

Instead of asking AI only to summarise a handover, what if it **challenged the ambiguity**?

If someone says “normally”, when does the normal rule not apply? If something is “urgent”, who decides what qualifies as urgent? If a person “needs to look at” a campaign, are they approving the work, approving the budget, or simply being informed?

The intended moment is simple:

> “I didn’t realise I hadn’t explained that.”

The system should not pretend to know missing tacit knowledge. It should identify where an answer may be missing and ask the human while the knowledge holder is still available.

## The prototype

Prototype v0.1 is deliberately small and self-contained. A visitor can use their own experience as the demo data; no prepared corporate dataset is required.

1. **Knowledge Dump** — describe a real role, responsibility, or project naturally.
2. **AI Challenge** — receive one context-specific follow-up question at a time, traceable to something actually said.
3. **Living Role Memory** — turn the handover and clarifications into a structured operational memory while keeping unresolved gaps visible.
4. **Manager / +1 Validation Preview** — show how high-impact organisational rules could be confirmed, corrected, or sent back for clarification without rereading the full handover.

## What it produces

The generated Role Memory is organised around:

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

The prototype also surfaces a lightweight **handover readiness** indicator. It is a communication mechanism for unresolved knowledge, not a scientific completeness score.

## What v0.1 tests

**One assumption only:** can ambiguity detection produce follow-up questions that feel genuinely useful to the knowledge holder?

A successful test is not “the interface looks polished.” A successful test is when the user thinks:

- “That’s a good question.”
- “I didn’t realise I hadn’t explained that.”

The development priority is therefore:

1. Quality of questioning
2. Quality of Role Memory structure
3. Manager validation interaction
4. Visual polish
5. Additional features

See [`evaluation/TESTING.md`](evaluation/TESTING.md) for the proposed evaluation method.

## How the questioning works in v0.1

This build uses a **transparent local ambiguity-detection engine**, not a production LLM integration. It looks for signals such as responsibility, authority, approvals, thresholds, dependencies, exceptions, escalation, named relationships, preferences, and uncertainty.

Each challenge is generated from the user's own statement and displays the source text that triggered the question. This keeps the interaction traceable and lets the prototype test the product hypothesis without requiring an API key or synthetic enterprise dataset.

See [`prompts-or-skill/INTERROGATION_LOGIC.md`](prompts-or-skill/INTERROGATION_LOGIC.md) for the reasoning framework and [`prompts-or-skill/ROLE_MEMORY_SCHEMA.md`](prompts-or-skill/ROLE_MEMORY_SCHEMA.md) for the output structure.

## Try it

### Local

Clone or download this repository and open `index.html` in a modern browser.

No build step, account, API key, server, or prepared dataset is required.

You can either:

- describe a real role/project in your own words, or
- click **Load example** to test the interaction immediately.

### GitHub Pages

Because the prototype is a static site, the repository can also be published with GitHub Pages directly from the repository root. In GitHub, enable Pages for the branch containing the prototype and use the root directory as the publishing source.

## What this prototype does **not** test

Prototype v0.1 deliberately does **not** implement:

- Microsoft 365, Teams, Outlook, or enterprise WeChat integration
- enterprise search
- large-scale RAG
- organisational knowledge graphs
- enterprise authentication or permission architecture
- large document ingestion
- production compliance infrastructure
- sophisticated token optimisation
- a full HR workflow
- a complete onboarding system

These are future enterprise-development questions, not capabilities claimed by this prototype.

## Future hypothesis — not implemented

**This section records the original product direction. It is not an active v0.2 roadmap.**

A future enterprise version could ask a different question:

> If AI is given appropriately authorised access to enterprise work traces, can it detect unexplained patterns, dependencies, and exceptions and use them to generate better knowledge-transfer questions?

For example, if formal documentation repeatedly describes `A → B → C`, while historical execution repeatedly shows `A → D → B → C`, the system should **not guess what D means**. It should ask why D appears and what operational role it plays.

That enterprise-data layer is explicitly a **future hypothesis**. Prototype v0.1 does not connect to enterprise systems or claim to infer organisational truth from them.

## Why “Living” Role Memory

Operational knowledge changes. A future Role Memory would need version history, validation dates, source, owner, confidence, superseded status, and a clear current-versus-historical distinction.

The goal is not merely to archive a handover. It is to preserve **usable memory**.

## Repository map

```text
.
├── index.html                         # Runnable prototype
├── app.js                             # Interaction + ambiguity-detection logic
├── styles.css                         # Prototype UI
├── docs/
│   ├── PRODUCT_REASONING.md           # Problem → hypothesis → design decisions
│   ├── PROTOTYPE_SCOPE.md             # v0.1 boundaries and Definition of Done
│   ├── ARCHITECTURE.md                # Current prototype architecture vs future hypothesis
│   └── LIMITATIONS.md                 # What the prototype cannot claim
├── prompts-or-skill/
│   ├── INTERROGATION_LOGIC.md         # Ambiguity categories and questioning principles
│   └── ROLE_MEMORY_SCHEMA.md          # Structured output model
├── examples/
│   └── EXAMPLE_HANDOVER.md            # Example input and challenge patterns
├── evaluation/
│   └── TESTING.md                     # Prototype evaluation method
├── GITHUB_UPLOAD.md                   # Repository publishing checklist
└── .gitignore
```

## Product reasoning

This project is intentionally framed around the reasoning chain rather than “AI wrote the code”:

**observe a problem → challenge the obvious solution → reframe the problem → identify the smallest hypothesis worth testing → design the human–AI interaction → build the prototype → test it → identify what would be required to scale**

The code is evidence of implementation. The product reasoning is evidence of architecture.

Start with [`docs/PRODUCT_REASONING.md`](docs/PRODUCT_REASONING.md) for the full prototype rationale.

---

**Status:** Prototype / Proof of Concept · v0.1 complete · further development paused after market review

