# Limitations

Prototype v0.1 is designed to test a product interaction, not to represent a production enterprise knowledge system.

## 1. It cannot discover truly unexpressed knowledge

If knowledge has never been expressed and has left no observable signal, the prototype cannot know that it exists. The product concept is therefore based on identifying **ambiguity in what has been expressed**, not claiming complete tacit-knowledge discovery.

## 2. The questioning engine is heuristic

The current build uses transparent local pattern detection rather than a production LLM. This makes the prototype easy to run and inspect, but question quality is constrained by the implemented signals and templates.

The engine can miss ambiguity, misclassify language, or ask a question that is less useful than a strong human interviewer would ask.

## 3. The Role Memory is conversation-supported, not organisational truth

The output reflects what the user said and clarified. It is not independently verified. Manager validation in v0.1 is only an interaction preview.

## 4. The readiness score is not completeness

The readiness percentage reflects challenged questions and response state inside the prototype. It cannot measure unknown unknowns and should not be treated as a scientifically valid handover-completeness metric.

## 5. There is no enterprise data access

Prototype v0.1 does not connect to messaging, email, calendars, documents, project tools, knowledge bases, directories, or historical role memory.

Any enterprise-context architecture shown in the project is a future hypothesis only.

## 6. There is no production governance model

The prototype does not implement authentication, permissions, access controls, retention policy, compliance infrastructure, source governance, validation history, ownership, or superseded-state management.

## 7. Role Memory is not yet truly “living”

The long-term concept requires version history, last validated date, source, owner, confidence, superseded status, and current-versus-historical distinctions. v0.1 demonstrates the memory structure and validation idea but does not implement that lifecycle.

## 8. Browser-local prototype

The prototype has no server-side persistence. Refreshing or restarting the experience resets the current state unless the user exports the generated JSON.

## What these limitations mean for evaluation

The correct evaluation question is not “Is this ready for enterprise deployment?”

It is:

> Does ambiguity-focused questioning reveal important context that a normal handover would otherwise leave unexplained?
