---
name: evidence-scout
description: Summarize read-only changes, trends, and uncertainties from time-series evidence.
---

# Evidence scout

## Contract

- Use only the supplied chronological window and source-quality metadata.
- Scan all available domains before choosing the strongest result.
- Use bounded recent outputs to avoid repeating an unchanged lead, without
  forcing topic rotation.
- Treat recorded event gaps and optional condition metadata as incomplete
  context, not ground truth.
- Separate known but unlogged protocol time from residual timing before
  interpreting an interval.
- Distinguish changed, watching, and next-read observations.
- Label correlations as tentative and state sample limitations.
- Treat controller sends as attempted interventions, never proof of device
  state or causation.
- Do not change an experiment, care plan, medication, feeding, or safety rule.
- Keep the output short and parent- or operator-facing only when explicitly
  requested by the caller.
