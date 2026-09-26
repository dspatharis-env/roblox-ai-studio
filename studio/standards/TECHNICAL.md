# Technical Standards

## Architecture
- Server owns truth for match state, currency, rewards, inventories, purchases, steals, wins/KOs and persistent progression.
- Client owns presentation, input intent, local effects and non-authoritative prediction.
- Shared config owns tunable constants and feature flags.
- Avoid huge god scripts; split systems by responsibility when complexity justifies it.

## Remotes
For every remote:
- validate player state and permission
- validate argument types/ranges
- validate distance/context server-side
- enforce server cooldown/rate limit
- never accept arbitrary instance/path mutation requests
- log suspicious abuse where useful

## Saves
- Keep one in-memory profile per connected player.
- Use UpdateAsync/session-safe patterns for contested state.
- Save periodically, on PlayerRemoving, BindToClose, and critical purchase/progression checkpoints.
- Never grant gameplay after an ambiguous failed load if doing so could duplicate value.
- Test server hopping and shutdown cases.

## Purchases
- Permanent benefits: pass ownership checks.
- Repeatable developer products: grant via ProcessReceipt and make grants idempotent.
- Never trust a client "purchase complete" event to grant value.
- Placeholder ID 0 must hard-disable the paid feature.

## Performance budgets
Before content scale:
- test mobile emulation
- test low graphics
- inspect memory and script/network cost
- avoid large numbers of unanchored physics objects
- pool/reuse effects when sensible
- keep spawn/join path lightweight
- prioritize stable frame pacing over visual excess

## Feature flags
Risky systems should be disable-able without code surgery:
- new economy source/sink
- timed event
- power-up family
- alternate arena hazards
- monetization prompt flow
- experimental progression
