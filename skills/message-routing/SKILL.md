---
name: message-routing
description: Preserve private and shared audiences across replaceable messaging adapters.
---

# Message routing

## Contract

- Treat the messaging provider as an adapter, not the source of audience truth.
- Resolve the audience before composing output: owner-private, another private
  recipient, shared household, or local-only.
- Include only the minimum context appropriate for that audience.
- Bind each reply to the question or proposal that produced it, apply an
  unambiguous reply once, and deduplicate handled messages.
- Keep ambiguous replies for the interactive agent instead of guessing inside
  a background reconciler.
- No-op when there is no material update or authorized recipient.
- Keep recipients, channel identifiers, credentials, and message history in
  private configuration.
