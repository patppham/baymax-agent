---
id: restore-preflight
lane: local
audience: local
---
# Restore preflight

Select the configured encrypted backup and validate its manifest, checksum,
decryption path, expected files, and recovery instructions in a temporary
destination. Do not replace or mutate the live runtime, start services, restore
credentials into production, or send a production message.

Record the bounded result. Return `NO_OUTPUT` when the recovery path verifies;
route only an actionable failure through the private alert adapter.
