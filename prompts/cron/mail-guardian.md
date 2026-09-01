---
id: mail-guardian
lane: local
audience: private
---
# Guarded inbox cleanup

Run exact private sender and message rules first. Use a bounded classifier only
for messages that remain ambiguous and expose only the minimum configured
metadata or excerpt. Apply the configured automatic action only at high
confidence; place everything else into a private review queue.

Reconcile stale entries, deduplicate reports, and continue past one malformed
message without broadening the scan. Keep credentials, addresses, bodies,
provider identifiers, and learned rules private. Return `NO_OUTPUT` when no
review or failure needs attention.
