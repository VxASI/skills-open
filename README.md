# skills-open

Open, agent-portable skills from VxASI, created by Chirag Awale, for personal and enterprise projects.

## Skills

### `conversation-insights`

Analyze a conversation for evidence-based professional and personal insights, then optionally save a portable capability portfolio. It uses concise shareable entries plus separate private supporting references, avoids double-counting repeated evidence, and has no runtime dependency.

```bash
npx skills add VxASI/skills-open --skill conversation-insights
```

The portfolio is stored only when the user requests it, at `~/.agent-achievements/` by default. Set `ACHIEVEMENT_HOME` to use an approved alternate location.

### `aha-pass`

Revisit a substantive code or configuration change before handoff to find the occasional higher-leverage “aha” that appears after the first implementation. It probes realistic scenarios, simplification opportunities, coupling, and fragile assumptions, then changes course only when the alternative is clearly better and verifiable—not as a refactor reflex.

```bash
npx skills add VxASI/skills-open --skill aha-pass
```

Use it when a completed change deserves one deliberate second look for a smaller, safer, clearer, or more powerful design.

### `public-profile-intelligence`

Research a person, founder, creator, company, or your own public profile using public professional information. It resolves identity, maps the strongest public signals, separates verified evidence from self-claims and inference, and can audit how well an AI agent could discover, attribute, and understand your work from the public web.

```bash
npx skills add VxASI/skills-open --skill public-profile-intelligence
```

Use it for quick background checks, founder or hiring research, claim verification, self-audits, **agentic search readiness**, or optional two-profile comparison. Comparison Mode separates **Professional Overlap**, **Similarity**, and **Collaboration Fit** so complementary profiles are not treated as simply more or less alike.

When the user wants a shareable version, the skill checks what the current agent environment can actually create and offers only supported formats among **Site**, **Artifact**, **PDF**, and **PNG**. The canonical rich report uses a scorecard, an evidence-backed intelligence brief with identity/connections, and an optional comparison section.

In Agentic Search Mode it tests realistic discovery intents, then separates retrieval gaps, identity-linkage gaps, and evidence gaps so the recommended fixes stay concrete.

The skill uses progressive retrieval by default: quick checks stay lightweight, while deeper diligence is reserved for explicit requests or consequential decisions. It avoids private contact data, data brokers, leaked information, and personal surveillance.

#### Use without installing

Installation is optional when an agent can read GitHub or repository files directly.

Give the agent the skill directory and tell it to read `SKILL.md` first:

```text
https://github.com/VxASI/skills-open/tree/main/skills/public-profile-intelligence
```

`SKILL.md` is the portable entry point. It tells the agent which files under `references/` to read only when a deeper capability is needed, such as agentic-search testing, scoring, comparison, or artifact generation.

Installing the skill is still useful when the host supports native skill discovery or you want the workflow available repeatedly without supplying the repository link each time.

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
