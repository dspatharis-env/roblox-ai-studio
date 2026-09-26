# Boop Arena — v0.1.2

## Pitch
A kid-safe party game on a floating arena of tiles. Players use a friendly **boop** to push rivals off the edge while the arena collapses ring by ring. No damage system; the last player standing wins.

## Current game loop
1. Wait 12 seconds in the grass lobby.
2. Teleport to an 11x11 floating tile arena.
3. Boop nearby players with F, gamepad X, or the pink mobile button.
4. From 20 seconds onward, outer rings glow red and fall every 12 seconds.
5. Survive until the arena reaches the centre 3x3 or one player remains.
6. Earn coins for playing, KOs and survival, then return to the lobby.

## Current systems
- Server-authoritative nearest-target Boop within 10 studs, 1.5 s cooldown.
- KO credit when a player falls within 4 s of a Boop.
- Rewards: +5 participation, +10 KO, +25 survival.
- Leaderboard: Coins, Wins, KOs.
- Autosave every 60 s with retry and session-safe locking.
- HUD: timer, players left, Boop button, messages.
- Feature switches for falling rings and KO rewards.

## Version history
- 0.1.0: first version
- 0.1.1: fixed rings falling too early
- 0.1.2: made saving session-safe

## Current cards
- ar-03: 3 arena shapes, random each round
- ar-05: analytics events
- ar-08: kid-safe power-up tiles
- ar-06: Double Coins pass + Shop
- ar-04: coin cosmetics
- ar-07: daily reward + win streak

## Human gate
ar-02 Studio playtest is required before treating the build as validated.
