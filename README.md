# Roblox AI Studio

A shared, evidence-driven operating system for building, maintaining, packaging, measuring and monetizing Roblox experiences.

## Mission
Create original Roblox games that are fun first, technically solid, easy to understand on mobile, safe for broad audiences, and capable of earning sustainable Roblox-native revenue.

## Portfolio
1. **Boop Arena v0.1.2** — active development
2. **Steal a Critter v0.1.10** — maintenance / validation
3. **Sprout Market** — design
4. **Speed Escape** — design

Forest Rescue is retired.

## Shared-agent model
- **Human owner:** final authority for publishing, spending, prices, game-pass creation, policy-sensitive decisions and product direction.
- **ChatGPT:** current-platform research, product strategy, analytics design, QA, architecture, documentation, code/repo changes.
- **Claude:** implementation/review, Roblox Studio-oriented development, code migration and handoffs.
- **Higgsfield:** visual exploration, environment concepts, key art, thumbnail ideation, trailer previsualization.
- **GitHub:** durable source of truth between agents. Important decisions must be written here, not left only in chat.
- **Roblox Studio / Creator Hub:** final build, playtest, publishing, analytics and monetization environment.

## Operating loop
Research → hypothesis → backlog card → implementation → automated gate → Studio playtest → release → analytics → decision.

Start with `studio/AGENT.md`, `studio/state.json`, `studio/MANAGER.md` and the active game's folder.
