# Roblox Platform Research — 2026-09-26

Primary sources are current Roblox Creator Hub documentation.

## Discovery signals
Roblox currently identifies the following as important recommendation signals:
- play-through rate
- first-play bounce rate (including very short sessions)
- play days per user
- playtime per user
- intentional co-play days
- qualified play sessions
- spend days per user
- Robux spent per user

Implication: packaging alone is not enough. A click that bounces quickly can be worse than fewer but better-qualified clicks.

Source: https://create.roblox.com/docs/discovery

## Analytics sequence
Roblox recommends:
1. D1 retention + average session time first
2. D7/D30 retention
3. payer conversion + ARPPU
4. acquisition / play-through after product health is stronger

Similar-experience benchmarks become especially useful at 100+ DAU and are updated regularly.

Sources:
- https://create.roblox.com/docs/production/analytics
- https://create.roblox.com/docs/production/analytics/analytics-dashboard

## Analytics instrumentation
AnalyticsService supports economy, funnel and custom events.
Important limits include:
- up to 10 funnels
- up to 100 steps per funnel
- up to 100 custom event names
- up to 3 custom fields
- server-side published games only for custom event reporting

Use custom fields rather than creating dozens of event names.

Sources:
- https://create.roblox.com/docs/production/analytics/event-types
- https://create.roblox.com/docs/production/analytics/custom-events
- https://create.roblox.com/docs/production/analytics/custom-fields

## Packaging
- thumbnails: 16:9, ideally 1920x1080
- Home thumbnail personalization: activate 2–5 variants
- personalization allocates more impressions to stronger variants while retaining exploration traffic
- authentic gameplay video can be used on detail/Home surfaces (not supported on some console/VR surfaces)

Source: https://create.roblox.com/docs/production/publishing/thumbnails

## Monetization
Current supported paths include passes, developer products, subscriptions, private servers, paid access, Roblox Plus-related systems, Creator Rewards and more.
- passes are one-time permanent benefits
- developer products are repeatable
- paid random items have explicit odds/policy requirements
- Roblox warns against pressure tactics and misleading urgency

Sources:
- https://create.roblox.com/docs/production/monetization
- https://create.roblox.com/docs/production/monetization/developer-products
- https://create.roblox.com/docs/production/monetization/paid-random-items

## Creator Rewards
Daily Engagement: qualifying experiences can receive 5 Robux for a qualifying active spender who plays 10+ minutes, subject to program rules.
Audience Expansion can reward attributed new/reactivated users under eligibility and DAU conditions.

Source: https://create.roblox.com/docs/creator-rewards

## Ads
Ads Manager supports Plays, Earnings (limited) and Engagement goals, audience segmentation, and up to 10 creatives. Roblox explicitly notes that non-unique experiences may perform poorly in ads/search/recommendations.

Source: https://create.roblox.com/docs/production/promotion/ads-manager

## LiveOps
Experience events and updates can be surfaced on experience pages, notifications and trending event surfaces. High-quality visuals and clear metadata matter for event featuring.

Source: https://create.roblox.com/docs/production/promotion/experience-events

## Notifications / social
Experience notifications are opt-in and primarily for age-eligible users; each experience has throttles. Invite prompts and friend co-play can support social growth.

Sources:
- https://create.roblox.com/docs/production/promotion/experience-notifications
- https://create.roblox.com/docs/production/promotion/invite-prompts

## Security
Roblox recommends validating all client-triggered requests on the server: context, permissions, state, distance, types and rate limits. Network ownership can invalidate naive distance assumptions around unanchored parts.

Source: https://create.roblox.com/docs/scripting/security/client-server-boundary

## Data / cross-server
- DataStoreService: durable player state
- MemoryStoreService: frequent ephemeral cross-server state, useful for matchmaking/queues
- buffer state in memory; save periodically + leave/shutdown/critical checkpoints

Sources:
- https://create.roblox.com/docs/cloud-services/data-stores
- https://create.roblox.com/docs/cloud-services/data-stores/best-practices
- https://create.roblox.com/docs/cloud-services/memory-stores

## Performance
Roblox targets smooth 60 FPS where possible. High memory use, server heartbeat problems and long join times reduce experience quality and can exclude lower-end mobile users.

Source: https://create.roblox.com/docs/performance-optimization

## Localization
Automatic translation can broaden global reach. Keep strings translatable and avoid baking essential text into images.

Source: https://create.roblox.com/docs/production/localization
