# Role Memory Schema

Prototype v0.1 transforms the handover conversation into a structured operational memory.

## Human-readable structure

### Role / Responsibility

What the role or project owns, handles, manages, or leads.

### Key People

People named in the operational context and the clarified reason they matter.

### Decision Authority

Who can decide, make the final call, or apply thresholds and overrides.

### Approvals

Who must review or approve what, and what the approval actually covers.

### Dependencies

What must happen before another step can happen.

### Normal Workflows

The usual sequence or operating pattern.

### Exceptions

When the normal workflow changes, who can use the exception, and whether it is legitimate practice or historical habit.

### Escalation Paths

What happens when the normal process fails or becomes blocked.

### External Relationships

Agencies, vendors, clients, customers, partners, suppliers, and other external dependencies.

### Preferences

Stakeholder preferences that should not be confused with formal policy.

### Open Questions

Unresolved knowledge gaps that remain visible rather than being guessed.

### Confidence / evidence state

Prototype v0.1 uses lightweight states such as:

- `Conversation-supported`
- `Open`
- `Not established`

These states do not imply organisational validation.

## Exported JSON

The prototype can export a local JSON file with this conceptual shape:

```json
{
  "prototype": "Living Role Memory v0.1",
  "created": "<ISO timestamp>",
  "source_handover": "<original natural-language handover>",
  "clarifications": [
    {
      "gap_type": "Exception",
      "question": "<traceable challenge>",
      "answer": "<human clarification>",
      "trace": "<source statement>"
    }
  ],
  "unresolved": [
    {
      "gap_type": "Escalation",
      "question": "<open challenge>",
      "trace": "<source statement>"
    }
  ],
  "role_memory": {
    "Role / Responsibility": [],
    "Key People": [],
    "Decision Authority": [],
    "Approvals": [],
    "Dependencies": [],
    "Normal Workflows": [],
    "Exceptions": [],
    "Escalation Paths": [],
    "External Relationships": [],
    "Preferences": [],
    "Open Questions": []
  },
  "note": "Prototype output. Conversation-supported, not manager-validated organisational truth."
}
```

## Future lifecycle fields — not implemented

A genuinely living organisational memory would eventually need fields such as:

- version history;
- last validated date;
- source;
- owner;
- confidence;
- superseded status;
- current-versus-historical state.

These are part of the product vision but are intentionally not implemented in Prototype v0.1.
