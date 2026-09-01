---
name: device-baseline-guard
description: Detect drift from a private device baseline and apply only allowlisted corrections.
---

# Device baseline guard

## Contract

- Read authenticated device state through a private adapter and compare only
  fields covered by the configured baseline.
- Treat missing or ambiguous state as unknown, never as off or safe.
- Correct drift only with an allowlisted, idempotent command and a bounded retry.
- Record the observed state, decision, attempted correction, and verification
  result without copying device identifiers into shared output.
- Never infer occupancy or user behavior from device state unless a separate
  policy explicitly authorizes that interpretation.
- Stay local and quiet when the baseline holds; route persistent failures to a
  private alert adapter.
