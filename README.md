# Happy-Codex Marketplace

A marketplace for happy-codex plugins, distributing reusable coding skills, commands, agents, and hooks.

## Available Plugins

| Plugin | Version | Description |
|--------|---------|-------------|
| **andrej-karpathy-skills** | 1.0.0 | Behavioral guidelines inspired by Andrej Karpathy |

## Quick Start

### Install a Plugin

```bash
happy-codex plugin install <plugin-name>
```

### Browse Plugins

1. Clone this repository
2. Review plugin configurations in `marketplace.json`
3. Copy plugins to your `~/.happy-codex/plugins/` directory

## Directory Structure

```
./
├── .happy-codex/
│   └── marketplace.json       # Marketplace manifest
├── LICENSE                    # MIT License
├── README.md                  # This file
└── andrej-karpathy-skills/    # Plugin
    ├── plugin.json           # Plugin manifest
    ├── README.md             # Plugin docs
    └── skills/
        └── karpathy-guidelines/
            └── SKILL.md      # Skill definition
```

## Add New Plugin

1. Create a plugin directory with `plugin.json`
2. Add skills, commands, agents, or hooks
3. Update `marketplace.json`
4. Submit a PR

## Plugin Manifest

```json
{
  "name": "my-plugin",
  "version": "1.0.0",
  "description": "Description",
  "author": { "name": "Author", "url": "https://github.com/author" },
  "license": "MIT",
  "keywords": ["tag1", "tag2"],
  "skills": ["./skills/my-skill"],
  "commands": [],
  "agents": [],
  "hooks": []
}
```

## License

MIT