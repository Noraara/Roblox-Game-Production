# Roblox Game Production Skill

**Ship Roblox features you can verify in the right place.**

Roblox Game Production helps Codex and Claude Code follow a player action through Luau, the server, and Studio. It fits a local bug fix or a feature with UI, replication, or save data. Use it with your existing project layout and tools.

## Quick start

Use [GitHub CLI](https://cli.github.com/) with support for [`gh skill install`](https://cli.github.com/manual/gh_skill_install).

```sh
# Codex
gh skill install Noraara/Roblox-Game-Production roblox-game-production --agent codex --scope user

# Claude Code
gh skill install Noraara/Roblox-Game-Production roblox-game-production --agent claude-code --scope user
```

Use `--scope project` inside a project checkout for a project-only install. For manual setup, copy the complete [`skills/roblox-game-production`](skills/roblox-game-production) folder.

| Agent | One project | All projects |
| --- | --- | --- |
| Codex | `.agents/skills/` | `~/.agents/skills/` |
| Claude Code | `.claude/skills/` | `~/.claude/skills/` |

## Try it on a real task

> Use $roblox-game-production to read the starter quest brief in examples/starter-quest, identify the owning components, and prepare the smallest verification plan for a player who triggers it twice. Read only.

In Claude Code, start the request with `/roblox-game-production`. See the [worked example](examples/starter-quest/README.md).

## What it handles

| Task | What the workflow checks |
| --- | --- |
| Localized bug | The owner of the behavior, its relevant callers, and a focused regression check. |
| Feature | Player input, server decisions, state, persistence, and client feedback. |
| Studio or Rojo | Which source owns the object or script, what synced, and where the behavior ran. |
| UI or imported asset | The actual focus targets, layout, dimensions, pivot, collision, and material checks the task needs. |

Start with your project’s own code, notes and checks. Studio is needed to verify engine behavior. Rojo is used when the project owns its scripts on disk. [Roblox Creator Hub](https://create.roblox.com/docs) is the engine reference. [Awesome GameDev Agent Skills](https://github.com/gamedev-skills/awesome-gamedev-agent-skills) and project vaults are optional specialist sources.

## From a player action to a verified feature

Take the [starter quest example](examples/starter-quest/README.md). A new player interacts with a beacon and should receive one persistent badge flag. The workflow identifies who owns the beacon, where the server decides eligibility, which progression record stores the result, and how the player hears that it completed. It then prepares checks for first completion, a repeated interaction, a temporary save failure, and rejoin.

For a small bug, the same ownership check keeps the work focused. A disappearing menu item that drops gamepad focus calls for a local navigation fix and a focus-restoration check. A bug that spans scripts and place objects calls for inspecting both sources before editing.

## Match the check to the claim

- **Files and sync.** Run the project’s lint, type, or packaging checks. With Rojo, verify the relevant mapping or synced copy when the task depends on Studio seeing that source.
- **Game behavior.** Check replication in the intended Studio session. Use the relevant input device for controller or touch claims and disposable test data for persistence checks.
- **Asset integration.** Confirm that imported scale, pivot, materials, and collision work in the experience. A separate art workflow can supply the editable source and export.

Use the project’s existing notes and tools. Optional specialist skills can deepen a specific check. If Studio is unavailable, file and fixture checks can still establish progress. The result should identify which runtime observation is outstanding and where to resume.

## Help and contributing

Include your host and app version, a small original or redacted example, the expected result, and the check that exposed the issue.

## License

Released under the [MIT license](LICENSE).

## Credit

Made by [Noraara](https://github.com/Noraara).
