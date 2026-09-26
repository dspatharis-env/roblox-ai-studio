# Orchestrator / Agent Operating Instructions

## Hard scope
This repository is in **Boop Arena only** mode.

**Boop Arena v0.1.2 is the only active product.**

Do not use autonomous shifts on Steal a Critter, Sprout Market, Speed Escape or new games. Do not research, code, package, monetize or generate Higgsfield concepts for those projects unless the owner explicitly reactivates them.

## Before every shift
1. Read `studio/FOCUS.md`.
2. Read `studio/state.json`.
3. Read `studio/pipeline.json`.
4. Read `studio/MANAGER.md`.
5. Read `games/arena/GAME.md`, `PRODUCT.md`, `BACKLOG.md`, `ANALYTICS.md`, `PLAYTEST.md`, `CHANGELOG.md`.
6. Ask whether the work materially improves Boop Arena.
7. If current Roblox behavior matters, verify it against current official Roblox documentation.

## Current gates
The next owner-dependent gate is **ar-02: Studio playtest**.
After critical fixes, preferred sequence:
ar-03 arena variety → ar-05 analytics → controlled published test → retention review → power-ups/cosmetics → monetization.

## Departments
Every department serves Boop Arena:
- Research
- Product/game design
- Engineering
- Security/data integrity
- Analytics
- QA/playtest
- Creative/Higgsfield
- Packaging/acquisition
- Monetization
- LiveOps
- Manager

## Evidence rule
Every feature proposal must state:
- player problem/opportunity
- hypothesis
- expected metric
- implementation cost
- risk
- acceptance test
- rollback/feature flag where practical

## Release blockers
- unvalidated player-affecting remotes
- save corruption risk
- broken mobile/gamepad controls
- failed critical playtest checks
- analytics logged before successful state change
- deceptive packaging
- placeholder paid IDs accidentally enabled
- performance regression severe enough to hurt low-end mobile

## Higgsfield rule
Higgsfield is used **only for Boop Arena** during this focus phase. Concepts must map to shipped or clearly scheduled mechanics and must be translated into Roblox-feasible implementation briefs.

## Handoff
Update durable state in GitHub. Never assume another AI has seen the same chat.
