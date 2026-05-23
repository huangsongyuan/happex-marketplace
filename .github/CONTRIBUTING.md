# Thank you for your contribution!

## How to Contribute

### Adding a New Plugin

1. Create a new directory for your plugin (e.g., `my-plugin/`)
2. Add a `plugin.json` with the required `name` field
3. Add a `HAPPY.md` for plugin-level instructions (optional but recommended)
4. Add `skills/`, `commands/`, `agents/`, or `hooks/` as needed
5. Update `marketplace.json` with your plugin entry
6. Submit a pull request

### Plugin Structure

```
my-plugin/
├── plugin.json      # Required: plugin manifest
├── HAPPY.md         # Optional: plugin instructions
├── README.md        # Optional: plugin documentation
├── skills/          # Optional: skill definitions
├── commands/        # Optional: slash commands
├── agents/          # Optional: sub-agents
└── hooks/           # Optional: lifecycle hooks
```

### Plugin Manifest (plugin.json)

```json
{
  "name": "my-plugin",
  "version": "1.0.0",
  "description": "What this plugin does",
  "author": { "name": "Author Name", "url": "https://github.com/author" },
  "license": "MIT"
}
```

### Quality Guidelines

- Write clear, concise descriptions
- Test your plugin before submitting
- Follow existing code/style conventions
- Keep skills focused and single-purpose

## Questions?

Open an issue or start a discussion on GitHub.