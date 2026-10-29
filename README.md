# ro-engineer

A Claude skill for Roblox/Luau development and game design. One router
(`SKILL.md`) sends the model to small, lazy-loaded reference files, guided
workflows and templates.

It covers:

- **Engineering:** modern Luau, strict typing, composition, OOP, ECS, state
  management, object pooling, client/server boundaries, networking, cleanup,
  performance and testing.
- **Game design:** core/session/meta loops, player incentives and hooks,
  onboarding, progression and economy, live ops.
- **Workflows:** planner, game designer, architect and implementer roles as
  phases with explicit stop points, plus code, performance, retention and
  economy audits.

## Layout

```
SKILL.md        router: tool detection, routing table, core rules
references/     one topic per file, loaded only when routed to
workflows/      phased procedures (plan, design-game-loop, design-system, implement, audits)
templates/      output skeletons for plans, loop docs, design docs and modules
```

## Modes

The skill detects its environment and adapts:

| Mode | When | Behaviour |
|---|---|---|
| `studio` | Roblox Studio MCP tools available | Reads real scripts, runs Luau, playtests, reads console |
| `rotex` | ROTEX MCP tools available | Queries existing systems and libraries, validates generated code |
| `offline` | No MCP tools (e.g. claude.ai chat) | Copy-paste-ready modules with placement instructions |

## Install

- **Claude Code, personal:** clone or copy this repo to `~/.claude/skills/ro-engineer/`.
- **Claude Code, per project:** copy to `<project>/.claude/skills/ro-engineer/` and commit it.
- **claude.ai chat:** zip the repo contents so `SKILL.md` is at the top level of
  the zip, then upload it under Settings > Features. Skills do not sync across
  surfaces, so re-upload after changes. Expect `offline` mode there.
- **As a plugin:** place this folder under a plugin's `skills/` directory. No
  changes needed.

Build a chat-upload zip from the repo root (PowerShell):

```powershell
Compress-Archive -Path SKILL.md, references, workflows, templates -DestinationPath ro-engineer.zip -Force
```

## Usage

Invoke it with `/ro-engineer`, or just ask a Roblox question: the description
triggers it. Typical flow for a new feature:

```
plan -> design-game-loop (if it changes player behaviour) -> design-system -> implement
```

Each design phase stops and asks for approval before the next.

## Keep it current

Some claims age quickly. Re-check these periodically and update the
reference files:

- Luau syntax and features (`const`, type solver changes) against the Luau
  release notes: `references/luau-modern.md`, `references/luau-types.md`.
- Community library names and maintenance status (ECS, networking, state,
  cleanup, data): `references/ecs.md` and others.
- Roblox policies on paid random items, odds disclosure and time-limited offers:
  `references/player-incentives.md`, `references/progression-economy.md`.
- MCP tool names used for mode detection: `SKILL.md`.

Add real incidents to `references/sharp-edges.md` as you hit them.
