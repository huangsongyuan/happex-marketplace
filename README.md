# Happex Marketplace

A marketplace for happex plugins, distributing reusable coding skills, commands, agents, and hooks.

## Available Plugins

| Plugin | Version | Category | Description |
|--------|---------|----------|-------------|
| **andrej-karpathy-skills** | 1.0.0 | workflow | Behavioral guidelines inspired by Andrej Karpathy |

## Plugins

### andrej-karpathy-skills

**Source:** [huangsongyuan/andrej-karpathy-skills](https://github.com/huangsongyuan/happex-marketplace/tree/main/andrej-karpathy-skills)

This plugin contains behavioral guidelines inspired by Andrej Karpathy to reduce common LLM coding mistakes. It is developed and maintained by [huangsongyuan](https://github.com/huangsongyuan).

**Features:**
- `karpathy-guidelines` skill - LLM coding best practices

**Referenced Resources:**
- [Andrej Karpathy on X/Twitter](https://x.com/karpathy/status/2015883857489522876) - Original observations on LLM coding pitfalls

## Quick Start

### Register as Local Marketplace

```bash
happex marketplace add ./ --name happex-marketplace
```

### Install a Plugin

```bash
happex plugin install andrej-karpathy-skills
```

## Directory Structure

```
./
├── LICENSE                    # MIT License
├── README.md                  # This file
└── andrej-karpathy-skills/    # Plugin directory
    ├── plugin.json           # Plugin manifest (required)
    ├── HAPPEX.md             # Plugin instructions (auto-injected)
    ├── README.md             # Plugin documentation
    └── skills/              # Skill definitions
        └── karpathy-guidelines/
            └── SKILL.md     # Skill manifest + prompt
```

## Marketplace Manifest (marketplace.json)

```json
{
  "name": "my-marketplace",
  "owner": { "name": "Author Name", "url": "https://github.com/author" },
  "plugins": [
    {
      "name": "my-plugin",
      "source": "./my-plugin",
      "version": "1.0.0",
      "description": "What this plugin does",
      "author": { "name": "Author" },
      "category": "workflow"
    }
  ]
}
```

## Plugin Manifest (plugin.json)

```json
{
  "name": "my-plugin",
  "version": "1.0.0",
  "description": "Plugin description",
  "author": { "name": "Author", "url": "https://github.com/author" },
  "license": "MIT",
  "keywords": ["tag1", "tag2"],
  "skills": ["./skills/my-skill"],
  "commands": [],
  "agents": [],
  "hooks": {}
}
```

## Add New Plugin

1. Create a plugin directory with `plugin.json`
2. Add `HAPPEX.md` for plugin-level instructions
3. Add `skills/`, `commands/`, `agents/`, or `hooks/` directories
4. Update `marketplace.json` with the plugin entry
5. Submit a PR

## License

MIT