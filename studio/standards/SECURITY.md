# Security / Anti-Exploit Standard

## Threat model
Assume exploiters can:
- fire remotes at arbitrary frequency
- forge client arguments
- alter local UI/state
- move locally owned physics assemblies
- call prompts/remotes outside intended context
- rejoin/server-hop strategically

## Required protections
- server-authoritative target selection for Boop
- server-authoritative steal ownership and delivery checks
- rate limits on all player-affecting remotes
- sanity checks on movement-dependent rewards
- idempotent purchase grants
- session-safe persistent data
- no reward on mere client claim
- no admin/debug remotes exposed in production

## Boop Arena specific
- client requests "attempt boop", never target identity
- server determines target in cone/range
- cooldown enforced server-side
- KO credit window stored server-side
- falling/out state confirmed server-side
- power-ups cannot let client directly set force/reward

## Steal a Critter specific
- steal start validates ownership, lock state, distance and availability
- carry token is server-issued and time-limited
- delivery validates current carrier, destination and token
- reclaim invalidates stale carry state
- anti-teleport logic must tolerate normal lag without duping
