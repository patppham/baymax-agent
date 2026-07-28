---
name: climate-control-safety
description: Plan deterministic local climate control behind a physically verified full-state command allowlist.
---

# Climate control safety

## Contract

- Record each validated sensor reading before evaluating that same reading.
- Continue acquisition when control is disabled.
- Select only physically verified full-state commands from private
  configuration; never construct off, toggle, or partial-state commands.
- Require stable evidence, bound resend frequency, cap ordinary commands, and
  keep control thresholds separate from notification thresholds.
- Treat sends as attempted interventions rather than confirmed device state.
- Fail closed on stale evidence, unreadable state, failed history writes,
  ambiguous presence, network errors, or send errors.
- Default ambiguous presence to occupied and keep presence checks read-only.
- Route failures privately and keep identifiers, packets, addresses, and
  calibrated thresholds outside the public contract.
- Never expand the allowlist automatically; require repeated evidence and
  physical verification before a private operator adds a command.
