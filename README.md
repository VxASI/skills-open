# skills-open

Open, agent-portable skills from VxASI, created by Chirag Awale, for personal and enterprise projects.

## Skills

### `conversation-insights`

Analyze a conversation for evidence-based professional and personal insights, then optionally save a portable capability portfolio. It uses concise shareable entries plus separate private supporting references, avoids double-counting repeated evidence, and has no runtime dependency.

```bash
npx skills add VxASI/skills-open --skill conversation-insights
```

The portfolio is stored only when the user requests it, at `~/.agent-achievements/` by default. Set `ACHIEVEMENT_HOME` to use an approved alternate location.

### `public-profile-intelligence`

Research a person, founder, creator, company, or your own public profile using public professional information. It resolves identity, maps the strongest public signals, separates verified evidence from self-claims and inference, and can audit how well an AI agent could discover, attribute, and understand your work from the public web.

```bash
npx skills add VxASI/skills-open --skill public-profile-intelligence
```

Use it for quick background checks, founder or hiring research, claim verification, self-audits, or **agentic search readiness**. In Agentic Search Mode it tests realistic discovery intents, then separates retrieval gaps, identity-linkage gaps, and evidence gaps so the recommended fixes stay concrete.

The skill uses progressive retrieval by default: quick checks stay lightweight, while deeper diligence is reserved for explicit requests or consequential decisions. It avoids private contact data, data brokers, leaked information, and personal surveillance.

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
