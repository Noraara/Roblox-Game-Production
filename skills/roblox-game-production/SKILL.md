---
name: roblox-game-production
description: Build, debug, and verify Roblox game features and fixes in Luau, Studio, or Rojo, including player-facing UI, replication, and persistence. Use for standalone Roblox work and the Roblox integration phase of a larger task.
license: MIT
---

# Roblox Game Production

1. Establish the active Roblox project, affected system, expected player behavior and acceptance checks. Read project instructions and the relevant source or decision record. For research alone, use the project's available notes and original evidence. Route standalone 3D or pixel-art authoring to the appropriate medium when available.
2. Identify the source that owns each change. For disk-owned scripts read the Rojo mapping or equivalent and edit the source. For generated assets edit their generator or native owner. For place-owned objects identify the intended Studio session and inspect its state. Preserve an existing user playtest, project conventions, saved IDs and approved balance.
3. For a localized fix, trace the relevant input and symptom, edit the narrowest owner, and verify it. For a feature, trace player input, server validation, state transition, persistence when relevant, and client feedback. Read the matching [production checks](references/production-checks.md) for the boundaries the task touches.
4. Follow current Roblox Creator Hub contracts and project source. Optional project skills or vaults can add specialized guidance. Verify decisive claims against their original sources and observed behavior.
5. Match verification to the claim. Use project lint and types for source, Rojo checks for packaging or sync, and focused Luau tests for state transitions. Use the permitted Studio session for replication, real input for device claims and disposable authorized data for persistence tests. Check visual acceptance separately. If a tool is unavailable, run independent checks and identify the outstanding observation.
6. Report the changed owner, observed behavior, verification environment and resume point. Check actual state before retrying an interrupted operation. For asset handoffs preserve scale, pivot, collision and materials through import. Use the [handoff guide](references/handoff.md) when another workflow owns context or delivery. Publish and spend only within the task’s authorization.
