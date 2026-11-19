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

## Help and contributing

Include your host and app version, a small original or redacted example, the expected result, and the check that exposed the issue.

## License

Released under the [MIT license](LICENSE).

## Credit

Made by [Noraara](https://github.com/Noraara).
