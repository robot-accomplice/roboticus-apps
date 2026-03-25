# Roboticus Apps

Ready-made agent configurations for [Roboticus](https://github.com/robot-accomplice/roboticus) — the autonomous agent runtime.

Each directory is a standalone application package containing a persona (`FIRMWARE.toml`), skills, and documentation. Copy a package into your Roboticus workspace to deploy it as an agent.

## Available Apps

| App | Description |
|-----|-------------|
| [tabletop-gm](tabletop-gm/) | Tabletop adventure RPG Game Master — collaborative storytelling with SRD-compatible d20 rules |

## Installation

```bash
# Copy an app's persona and skills to your Roboticus instance
cp apps/tabletop-gm/FIRMWARE.toml ~/.roboticus/workspace/
cp apps/tabletop-gm/skills/*.md ~/.roboticus/skills/
```

Then restart Roboticus or start a new session.

## Contributing

Each app should include:
- `FIRMWARE.toml` — Agent persona and behavioral rules
- `skills/` — Skill files that provide domain knowledge
- `README.md` — Description, setup instructions, and usage examples

## License

Apache 2.0 — same as Roboticus.
