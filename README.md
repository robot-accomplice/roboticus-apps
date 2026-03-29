# Roboticus Apps

Official application packages for the [Roboticus](https://github.com/robot-accomplice/roboticus) autonomous agent runtime.

## What are apps?

An app is a complete agent configuration package — persona, skills, subagents, themes, and workspace templates — everything needed to turn Roboticus into a **specialized agent** for a specific use case.

Apps are installed as isolated **profiles**. Each profile has its own database, workspace, and configuration. Switching between profiles switches the entire agent identity — from a personal assistant to a game master to a trading desk operator — with full data isolation.

## Quick Start

```bash
# Install an app
roboticus apps install tabletop-gm

# Launch with the new profile
roboticus serve --profile tabletop-gm

# Switch profiles (from dashboard or CLI)
roboticus profile switch tabletop-gm
```

## Available Apps

| App | Description | Min Model | Tested On |
|-----|-------------|-----------|-----------|
| [Tabletop GM](tabletop-gm/) | Collaborative storyteller for tabletop RPG sessions | 32B+ | qwen2.5:32b (96%), Kimi K2 (96%) |

## What's in an App Package

Every app ships as a self-contained directory:

```
app-name/
├── manifest.toml          # Identity, version, requirements, test results
├── FIRMWARE.toml           # Agent persona — voice, rules, behavioral contract
├── config-overrides.toml   # Agent config fields merged during install
├── README.md               # User-facing documentation
├── skills/                 # Skill .md files (behavioral directives)
│   ├── core-rules.md
│   ├── session-management.md
│   └── ...
├── subagents/              # Specialist definitions (.toml)
│   ├── lore_keeper.toml
│   └── combat_referee.toml
├── themes/                 # Bundled dashboard themes (JSON)
│   ├── parchment.json
│   └── dragonscale.json
└── workspace/              # Template files seeded into the profile workspace
```

### Package Manifest (`manifest.toml`)

```toml
[package]
name = "tabletop-gm"
version = "1.0.0"
description = "Collaborative storyteller for tabletop RPG sessions"
min_roboticus_version = "0.11.1"

[requirements]
min_model_params = "32B"
recommended_model = "ollama/qwen2.5:32b"
delegation_enabled = true

[profile]
agent_name = "The Narrator"
agent_id = "narrator"
default_theme = "parchment-and-ink"

[[tested]]
model = "ollama/qwen2.5:32b"
hardware = "MacBook Air M3 32GB"
gm_pass_rate = 0.96
```

### How Install Works

1. Downloads the app package and validates the manifest
2. Creates a new profile directory: `~/.roboticus/profiles/<app-name>/`
3. Copies FIRMWARE, skills, and themes into the profile
4. Merges `config-overrides.toml` into the profile's `roboticus.toml`
5. Creates a fresh database for the profile
6. Inserts subagent records from `subagents/*.toml`
7. Seeds workspace template files

Your existing profiles are never modified. Each app is fully isolated.

### How Uninstall Works

```bash
roboticus apps uninstall tabletop-gm
```

Removes the app configuration (FIRMWARE, skills, subagents, themes). Your **data is preserved** by default — campaign journals, session history, and memories stay in the profile directory. You'll be asked explicitly if you want to delete data too.

## Creating an App

Want to build your own Roboticus app? Here's the minimum:

1. Create a directory with your app name
2. Write a `manifest.toml` with package metadata
3. Write a `FIRMWARE.toml` defining the agent persona
4. Add skills as `.md` files in `skills/`
5. Optionally add subagents, themes, and workspace templates
6. Test with the soak framework: `python3 scripts/run-gm-soak.py`
7. Submit a PR to this repository

See the [App Development Guide](https://roboticus.ai/docs/apps) for a complete walkthrough.

## Profile System

Apps install as profiles — isolated agent configurations that share the Roboticus runtime but nothing else:

```
~/.roboticus/
├── roboticus.toml          # Default profile config
├── state.db                # Default profile database
├── profiles/
│   ├── tabletop-gm/
│   │   ├── roboticus.toml  # GM profile config
│   │   ├── narrator.db     # GM profile database
│   │   ├── workspace/      # GM workspace
│   │   └── skills/         # GM skills
│   └── trading-desk/
│       ├── roboticus.toml
│       ├── trader.db
│       └── ...
```

Switch between profiles from the dashboard header or via CLI:

```bash
roboticus profile list       # Show all installed profiles
roboticus profile switch gm  # Switch to the GM profile
roboticus profile create x   # Create a new empty profile
roboticus profile delete x   # Remove a profile
```

## Contributing

We welcome app contributions. Please ensure your app:

- Has a complete `manifest.toml` with tested model results
- Includes a FIRMWARE.toml with clear behavioral boundaries
- Ships skills that are specific to the use case
- Documents model requirements honestly (don't claim 7B works if it doesn't)
- Has been soak-tested with at least one model family

## License

Apache-2.0
