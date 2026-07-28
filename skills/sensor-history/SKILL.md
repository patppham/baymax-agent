# Read-only sensor history

Use this skill for local sensor logging that may later support analysis.

Normalize readings into a private, append-only history with timestamp, unit,
sensor identifier, source quality, and gap metadata. Keep collection separate
from interpretation. Do not turn one reading into a trend or a safety claim.

This acquisition skill is read-only. It never issues actuator commands, changes
device configuration, exposes physical location, or sends a message. A private
controller may consume the same validated in-memory reading only after the
history append succeeds; it must implement the separate climate-control safety
contract.
