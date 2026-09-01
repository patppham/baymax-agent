---
name: mail-guardian
description: Automate only high-confidence inbox cleanup with deterministic rules and bounded classification.
---

# Mail guardian

## Contract

- Apply exact deterministic sender and message rules before invoking a model.
- Give a bounded classifier only the metadata or short excerpt required to
  resolve ambiguity; never send an entire mailbox or thread by default.
- Automate only the configured high-confidence action and place uncertain
  messages into a private review queue.
- Learn new exact rules only from an explicit keep or remove decision.
- Reconcile stale queue entries and deduplicate reports.
- Continue safely past one malformed or stale message without broadening scope.
- Keep mailbox credentials, addresses, message bodies, provider identifiers,
  and learned private rules outside the public contract.
