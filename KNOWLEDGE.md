# Durable Studio Knowledge

## Roblox discovery
Current Roblox discovery guidance emphasizes play-through rate, first-play bounce, play days per user, playtime, intentional co-play, qualified sessions, spend days and Robux spent per user. Do not optimize one metric by damaging the others.

## Analytics order
Roblox recommends focusing first on D1 retention and average session time, then D7/D30 retention, then monetization metrics such as payer conversion and ARPPU, then acquisition.

## Packaging
Use unique titles, icons and thumbnails. Home thumbnail personalization works with multiple active thumbnails; prepare 2–5 truthful variants for testing. Thumbnails should be 16:9 and ideally 1920x1080.

## Creator Rewards
Meaningful 10+ minute sessions can contribute to Daily Engagement rewards for qualifying active spenders. Never pad sessions artificially; build enough legitimate replay/progression value that 10 minutes happens naturally.

## Security
Treat clients as untrusted. Validate context, distance, state, types and rate limits on the server. The server is authoritative for rewards, combat/boops, stealing, purchases and critical state.

## Data
Persistent progress belongs in DataStoreService; fast ephemeral cross-server state belongs in MemoryStoreService. Buffer player data in server memory and save periodically plus leave/shutdown/critical checkpoints.

## Global reach
Roblox supports automatic localization. Keep player-facing strings centralized and localization-friendly from the start.

## Performance
Optimize for low-end mobile. Long join times, memory pressure and inconsistent frame rates directly reduce the addressable audience and can hurt retention.
