---
name: backup-recovery
description: Create encrypted runtime backups and verify a non-destructive restore path.
---

# Backup and recovery

## Contract

- Select only documented durable configuration and state; exclude caches,
  locks, generated artifacts, active databases that cannot be copied safely,
  and vendored dependencies.
- Encrypt the archive before any remote transfer and never log keys or secrets.
- Produce a manifest and checksum for every archive.
- Run restore preflight against a temporary destination: verify decryption,
  checksums, expected files, permissions, and the documented restore sequence.
- Never overwrite the live runtime during a scheduled drill.
- Report success locally and route only actionable failures through a private
  alert adapter.
