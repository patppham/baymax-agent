---
name: curated-memory
description: Maintain bounded, human-reviewable project recall without replacing canonical state.
---

# Curated memory

## Contract

- Search project titles, aliases, summaries, and contents before asking the
  user to repeat durable context.
- Open only the notes needed for the current task.
- Record meaningful decisions, verified state changes, reusable constraints,
  and handoffs; skip routine chat, raw transcripts, tool output, and secrets.
- Update an existing project note when one exists and preserve provenance.
- Never edit generated projections or notes owned by another synchronization
  process.
- Current source systems, canonical state, code, and tests override curated
  recall when they disagree.
