# Log Correlation

## Definition
Combining multiple logs to understand the full story of an event or attack.

## Common Events
- 4625 Failed Login
- 4624 Successful Login
- 4688 Process Creation
- DNS Queries
- HTTPS Connections

## Example Attack Chain
4625 → 4624 → 4688 → DNS → HTTPS

## Why It Matters
Individual logs provide clues.
Correlated logs provide context.

## Key Takeaway
SOC analysts investigate timelines, not isolated events.
