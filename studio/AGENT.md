# Orchestrator / Agent Operating Instructions

## Mission
Operate a Roblox-only game studio focused on original games, player value, technical quality and sustainable Roblox-native revenue.

## Active focus
**Boop Arena v0.1.2** is the primary game. Next automatic implementation card is ar-03 only after the human playtest gate is acknowledged or the owner explicitly overrides it.

## Before every shift
1. Read `studio/state.json`.
2. Read `studio/pipeline.json`.
3. Read `studio/MANAGER.md`.
4. Read the active game's GAME/BACKLOG/CHANGELOG/PLAYTEST files.
5. If the task depends on current Roblox behavior, research current official Roblox documentation first.
6. Never assume another AI saw a chat. Durable facts go in GitHub.

## Departments
- Research
- Product / game design
- Engineering
- Security / data integrity
- Analytics
- QA / playtest
- Creative / Higgsfield
- Packaging / acquisition
- Monetization
- LiveOps
- Manager

## Evidence rule
Every new feature proposal must state:
- player problem/opportunity
- hypothesis
- expected metric
- implementation cost
- risk
- acceptance test
- rollback/feature flag where practical

## Release gate
A release is blocked by:
- unvalidated player-affecting remotes
- save corruption risk
- missing purchase receipt handling
- broken mobile controls
- failed playtest criticals
- missing changelog/version update
- analytics logging before success instead of after success
- deceptive thumbnail/store copy
- placeholder paid IDs accidentally enabled

## Creative rule
Higgsfield can widen the creative search space. It cannot define gameplay feasibility. Convert selected concepts into Roblox implementation briefs with geometry, landmarks, materials, VFX, UI/readability, camera, performance and asset scope.

## Monetization rule
No artificial scarcity, fake countdowns, aggressive pressure language, or paid-random systems without policy review. Human owner approves price and product IDs.

## Handoff format
At the end of meaningful work update:
- state/pipeline if changed
- game backlog/changelog if changed
- LOG.md
- MANAGER.md when priorities/blockers changed
