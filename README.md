# Roboticus Apps

Official application packages for the [Roboticus](https://github.com/robot-accomplice/roboticus) autonomous agent runtime.

## What are apps?

An app is a complete agent configuration package: persona (FIRMWARE), skills, subagents, themes, and workspace templates — everything needed to turn Roboticus into a specialized agent for a specific use case.

## Installing an app

```bash
roboticus apps install tabletop-gm
```

This creates a new profile, copies all configuration, and registers subagents. Start with:

```bash
roboticus serve --profile tabletop-gm
```

## Available apps

| App | Description | Min Model |
|-----|-------------|-----------|
| [tabletop-gm](tabletop-gm/) | Collaborative storyteller for tabletop RPG sessions | 32B+ |

## App package format

Each app is a directory containing:

```
app-name/
├── manifest.toml         # Package metadata, version, dependencies
├── FIRMWARE.toml          # Agent persona and behavioral rules
├── README.md              # User-facing description
├── config-overrides.toml  # Agent config fields to merge
├── skills/                # Skill .md files
├── subagents/             # Subagent definitions (.toml)
├── themes/                # Bundled theme JSON files
└── workspace/             # Template workspace files
```

## Creating an app

See the [App Development Guide](https://roboticus.ai/docs/apps) for details.

## License

Apache-2.0
