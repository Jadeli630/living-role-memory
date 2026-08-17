# Prototype Evaluation

## Research question

Prototype v0.1 tests one assumption:

> Can ambiguity-focused questioning in a natural handover conversation produce follow-up questions that the knowledge holder considers genuinely useful?

## Primary success signal

The strongest qualitative signal is the participant reacting with something equivalent to:

- “That's a good question.”
- “I didn't realise I hadn't explained that.”

This is the core prototype outcome.

## Suggested test format

### Participants

Use people who can describe a real role, project, or recurring responsibility from their own experience.

No prepared dataset is required.

### Session

1. Ask the participant to describe what the next person needs to know in their own words.
2. Do not ask them to organise the handover into categories first.
3. Let the prototype challenge the handover one question at a time.
4. Capture whether each question revealed context the participant had not initially explained.
5. Review the generated Role Memory.
6. Ask whether the result would help an incoming person act more effectively than the original handover alone.

## Question-level evaluation

For each generated challenge, record:

| Measure | Question |
|---|---|
| Traceability | Was the question clearly connected to something the participant actually said? |
| Relevance | Did the question matter for acting effectively? |
| Novelty | Did it surface context missing from the original explanation? |
| Specificity | Was it more useful than a generic onboarding question? |
| Answerability | Could the knowledge holder answer it from real experience? |
| Actionability | Would the answer change or improve what the next person knows to do? |

A simple 1–5 rating can be used for each measure, but the qualitative explanation matters more than the numeric score at this stage.

## Session-level evaluation

Ask the participant:

1. Which question was the most useful, and why?
2. Which question felt generic or unnecessary?
3. Did any question make you realise you had omitted something important?
4. Did the prototype misunderstand any statement?
5. Does the final Role Memory reflect how the work actually operates?
6. What important context is still missing?
7. Which statements would require manager validation before another employee should rely on them?

## Failure modes to watch

The prototype is weak if:

- questions could have been asked without listening to the user's input;
- the same generic checklist appears for every handover;
- low-impact details crowd out authority, exceptions, dependencies, or escalation;
- the system guesses answers rather than preserving uncertainty;
- the final memory looks structured but would not help someone act;
- the readiness score is interpreted as proof of completeness.

## What v0.1 evaluation does not prove

A successful prototype test does not establish that:

- the system can discover all tacit knowledge;
- enterprise integrations will work;
- organisational data can be interpreted safely;
- the Role Memory is organisational truth;
- production governance, permissions, compliance, or scale are solved.

Those are later questions.

## Decision rule for the next development phase

Continue beyond v0.1 only if real users repeatedly find the ambiguity-focused questions meaningfully better than a normal summary or generic handover questionnaire.

If they do not, improving enterprise architecture would be premature. The core interaction should be revised first.
