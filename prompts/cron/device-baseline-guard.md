---
id: device-baseline-guard
lane: local
audience: local
---
# Device baseline guard

Read authenticated device state through the private adapter and compare only
allowlisted baseline fields. Treat unavailable or ambiguous state as unknown.
If drift is unambiguous, apply at most the configured idempotent correction,
then verify once and record the attempt.

Do not invent commands, infer occupancy, broaden the baseline, or expose device
identifiers. Stay quiet when the baseline holds. Route persistent failures only
through the private alert adapter.
