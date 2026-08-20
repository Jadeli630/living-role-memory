# Market Research and Development Decision

**Research update: August 2026**

## Why this note exists

Living Role Memory v0.1 started as a small product experiment around one question:

> Can a system listen to a natural explanation of work, detect operational ambiguity, and ask a useful follow up before that ambiguity becomes part of the handover?

After building v0.1, I reviewed adjacent commercial products and recent research more closely. The market evidence changed my view of the opportunity.

The problem is real. The original product concept, however, is already substantially covered.

This note records that research and why I am not moving directly into v0.2.

## What I found

| Product | Publicly described approach | Overlap with Living Role Memory |
| --- | --- | --- |
| Sensay / Sophia | AI offboarding interviews with departing employees. Questions adapt as the interview progresses, focus on how work is actually done, and feed a structured knowledge base. | **Very high.** Same user moment, same conversational capture model, adaptive questioning, tacit knowledge goal, and knowledge transfer outcome. |
| Tacivo | AI moderated expert interviews for exit interviews, handovers and process mapping. Sessions become a living knowledge base and can generate handovers, SOPs and onboarding material. | **High.** Strong overlap in tacit knowledge elicitation, conversation based capture and handover use cases. |
| Transphere AI | Natural AI conversations with experts capture tacit knowledge and convert it into structured representations that preserve context and decision logic. | **High.** Strong overlap in conversational elicitation and structured knowledge output. |
| MAIA | Uses project documentation to generate handovers and systematically identify undocumented decisions, missing critical information and topics that were mentioned but not explained. | **Medium to high.** Different input model, but directly overlaps with knowledge gap detection before handover. |
| Sentra | Captures organisational interactions, decisions, rationale and commitments into persistent organisational memory with provenance and temporal structure. | **Adjacent but strategically important.** Different capture mechanism, but substantial overlap with the broader organisational memory thesis. |

### Sources

* Sensay product and workflow: https://sensay.io/product and https://blog.sensay.io/how-sensay-ai-offboarding-works
* Tacivo: https://tacivo.com/ and https://tacivo.com/solutions/handover
* Transphere AI: https://www.transphere.ai/
* MAIA project handover: https://www.getmaia.ai/en/use-cases/projektubergabe and https://docs.getmaia.ai/articles/7815567-how-to-structured-project-and-knowledge-handovers-with-maia
* Sentra organisational memory: https://www.sentra.app/manifesto and https://www.sentra.app/articles/what-is-organizational-memory

## Where v0.1 is still different

The scan did surface design choices that are less explicit in the products above.

### 1. Operational ambiguity as the trigger

The interrogation logic does not simply ask for more detail. It looks for specific reasons an explanation may not yet be actionable:

* responsibility
* decision authority
* approval
* threshold
* dependency
* exception
* escalation
* relationship
* preference
* uncertainty

For example, “larger campaigns need Rachel to look at them” contains at least two unresolved questions: what counts as larger, and what authority does Rachel actually have?

### 2. Traceable questions

A follow up should come from something the person actually said, rather than from a generic interview checklist.

### 3. Human validation

One person's experience is not automatically a company rule.

The v0.1 concept therefore includes manager or +1 validation for consequential organisational claims before they are treated as trusted Role Memory.

These are meaningful product choices. At this stage, I do not think they are enough evidence of a standalone market gap.

## Why I am not building v0.2 now

The decision is not that the problem is unimportant. The opposite is true: multiple companies are already investing in it.

The issue is differentiation.

The original concept overlaps heavily with existing products across the most important dimensions:

* the same knowledge loss problem
* the same handover or role transition moment
* conversational AI interviews
* adaptive follow up
* tacit knowledge elicitation
* structured organisational knowledge
* future reuse by colleagues or AI systems

The remaining differences are currently better described as interrogation design and knowledge governance choices than as a clearly validated standalone product opportunity.

Building more features would not answer the most important question: **is the remaining gap important enough that users need a different product?**

So the development decision is:

> **Do not move directly into v0.2. Keep v0.1 as a completed product experiment and stop additional development unless new evidence reveals a stronger unmet need.**

This is a product decision, not a technical limitation.

## What would change the decision

I would reconsider development if future research or user evidence shows a meaningful unmet need around questions such as:

* How do organisations distinguish a personal working habit from an accepted operational rule?
* Which captured claims require validation, and by whom?
* Can AI reliably detect when an explanation sounds complete but is still not actionable?
* Can an ambiguity framework materially improve knowledge quality compared with existing adaptive AI interviews?

Until then, adding functionality would create more prototype, not necessarily more product value.

## Research still worth following

Two recent academic directions are particularly relevant to the interrogation layer:

* **Large Language Models for Process Knowledge Acquisition**, published online in December 2025 and appearing in 2026, studies conversational knowledge elicitation and iterative follow up for actionable process knowledge.
* **The AI interviewer**, published in *Scientific Reports* in April 2026, evaluates adaptive follow up using criteria including necessity, context awareness, openness and justified skip.

These papers may improve how I think about question quality, even if Living Role Memory does not continue as a standalone product.

## What I learned

The useful outcome of v0.1 is not only the prototype.

It is also the decision not to overbuild after stronger market research.

**Problem → hypothesis → prototype → market scan → gap assessment → stop or continue.**

Sometimes iteration means another version. Sometimes it means deciding that the remaining gap is not strong enough yet.
