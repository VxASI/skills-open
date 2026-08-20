# skills-open

Open, agent-portable skills for personal and enterprise projects.

## Skills

### `conversation-insights`

Analyze a conversation for evidence-based professional and personal insights, then optionally save a portable capability portfolio. It uses concise shareable entries plus separate private supporting references, and has no runtime dependency.

```bash
npx skills add VxASI/skills-open --skill conversation-insights
```

The portfolio is stored only when the user requests it, at `~/.agent-achievements/` by default. Set `ACHIEVEMENT_HOME` to use an approved alternate location.

## Versions

The default install command follows `main`, so it always installs the newest published repository version.

The current stable release is [v0.1.0](https://github.com/VxASI/skills-open/releases/tag/v0.1.0). Pin that exact release when you need a reproducible install:

```bash
npx skills add https://github.com/VxASI/skills-open/tree/v0.1.0/skills/conversation-insights
```

Releases use Semantic Versioning. Patch releases contain compatible fixes, minor releases add compatible capability, and major releases may change stored-output or workflow behavior.

To update an existing installation that follows the repository source:

```bash
npx skills update conversation-insights
```

## License

Apache-2.0
