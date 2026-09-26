# Analytics Standard

## Studio KPI hierarchy
### Acquisition
- impressions (Creator Hub)
- play-through rate
- source mix
- new users

### First-session quality
- first-play bounce
- tutorial/onboarding completion
- time-to-first-core-action
- time-to-first-success
- first-session length

### Retention
- D1
- D7
- D30
- play days per user

### Engagement
- average session time
- qualified sessions
- rounds/loops per session
- social/co-play participation

### Monetization
- payer conversion
- ARPPU
- ARPDAU
- spend days per user
- product funnel completion
- currency sources/sinks/balances

## Event design rules
- Log after successful state change, never on attempted-but-failed action.
- Prefer stable event names + custom fields.
- Include game_version, platform bucket and content/map variant where practical.
- Do not log personally sensitive data.
- Verify events in published test before relying on dashboards.

## Experiment discipline
Every experiment needs:
- hypothesis
- primary metric
- guardrail metric
- start/end version or dates
- audience/content variant
- interpretation
- keep/rollback decision

## Example guardrails
A feature that improves session length but worsens D1 retention is not automatically a win.
A shop that improves payer conversion but increases first-session bounce is not automatically a win.
