---
id: encrypted-backup
lane: local
audience: local
---
# Encrypted runtime backup

Collect only the private deployment's documented durable files. Exclude
credentials that are not explicitly covered by the backup policy, transient
state, caches, locks, logs, unsafe live database copies, and dependencies.
Create a manifest and checksum, encrypt before transfer, and verify the stored
artifact without printing secrets.

Do not modify the live runtime. Return `NO_OUTPUT` after a verified backup and a
bounded local failure result otherwise.
