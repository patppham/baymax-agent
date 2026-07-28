---
name: surgical-questions
description: Ask at most one high-value question when deterministic checks find an unknown.
---

# Surgical questions

## Contract

- Let deterministic code decide whether an unknown is eligible.
- If there is no eligible unknown, return `wakeAgent: false` and no message.
- If there is one, ask one short routed question with the smallest useful
  choice set.
- Apply cooldown at the milestone or decision level so a sibling unknown cannot
  restate a recently asked question.
- Do not infer an answer or mutate state from silence.
- Keep the question private to the originating context.
