# Boop Arena Analytics Spec

## North-star questions
1. Do new players understand Boop quickly?
2. Do they survive long enough to experience the collapsing arena?
3. Do they immediately requeue?
4. Which arena shape creates the best replay/retention without excessive round length?
5. Do cosmetics/Double Coins add value without hurting early-session trust?

## Funnel A — First session
1. join
2. lobby_loaded
3. boop_input_seen
4. first_round_started
5. first_boop_attempt
6. first_successful_boop
7. first_round_finished
8. reward_screen_seen
9. second_round_started

Track completion rate and median time between steps.

## Custom events
Use stable events with fields rather than map-specific event names:
- BoopAttempt {arena_shape, input_type, round_age_bucket}
- BoopSuccess {arena_shape, input_type}
- Knockout {arena_shape, cause}
- PlayerEliminated {arena_shape, survival_time_bucket}
- RoundCompleted {arena_shape, player_count_start, duration_bucket}
- Requeue {arena_shape_previous}
- PowerupCollected {powerup_type, arena_shape}
- CosmeticEquipped {cosmetic_type}

## Economy
Currency: Coins
Sources:
- participation
- KO
- survival/win
- daily reward (future)
Sinks:
- cosmetic purchase
- future reroll only if deterministic/policy-safe

## Dashboard review
After each update compare:
- first-play bounce
- D1 retention
- average session time
- first→second round conversion
- successful boops per new player
- average round duration
- D7 when traffic allows
- payer conversion after monetization ships

## ar-05 acceptance
- events are server-sent
- logging happens after success
- event names/fields documented
- published test shows events in View Events
