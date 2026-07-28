---
id: room-climate-controller
lane: local
audience: local
---
# Local climate acquisition and control

Read one validated sensor value and append it to canonical private history
before using that same in-memory value for a decision. When control is disabled,
continue acquisition without issuing a command.

If control is enabled, choose only from the private deployment's physically
verified full-state allowlist. Enforce stability confirmations, resend
cooldowns, command caps, and separate notification thresholds. Treat attempted
commands as attempts, never proof of device state. Never synthesize an off,
toggle, mode-only, or partially specified command.

Fail closed on stale or invalid evidence, unreadable state, history-write
failure, ambiguous presence, network failure, or send failure. Keep device
identifiers and all technical alerts private. Return a local audit result only.
