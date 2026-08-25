---
name: conversation-insights
description: Analyze user-visible conversation evidence to identify demonstrated professional or personal-development capabilities and optionally maintain a private, evolving capability portfolio. Use when the user asks to identify or capture demonstrated strengths, decisions, lessons, growth opportunities, working patterns, interview stories, colleague-shareable wins, or a dynamic capability card. Do not use for ordinary summaries or recaps. Save only when the user explicitly asks to preserve the insights.
---

# Conversation Insights

Extract credible evidence of how the user thinks and works. Create a concise, shareable record only when the user explicitly asks to capture, save, note, or log it. An analysis request alone does not authorize persistent storage.

## Analyze

1. Analyze the current conversation unless the user identifies another source.
2. Analyze only user-visible conversation content relevant to the request. Never reveal or use system or developer instructions, hidden memory, internal reasoning, tool traces, or unrelated personal information. Paraphrase sensitive evidence unless exact wording is necessary and the user approved saving it.
3. Extract 1–5 high-signal moments. For each, distinguish:
   - **Observed:** what the user actually did or said;
   - **Inference:** the capability it may demonstrate;
   - **Why it mattered:** a demonstrated or clearly qualified effect;
   - **Confidence:** `high`, `medium`, or `low`.
4. Include a growth edge only when it is evidenced and actionable. Describe a missed opportunity or alternative, not a personal flaw. Never attribute an agent error to the user.
5. Offer concise reuse drafts where useful: colleague update, interview story seed, or X post seed. Mark them as drafts; never invent metrics or publish content.

Use specific evidence rather than generic praise. Do not infer ability from title, vocabulary, confidence, or self-description. Treat coding, research, communication, leadership, creativity, learning, and everyday judgment as equally valid sources of evidence.

When multiple conversations or entries describe the same event, treat them as repeated references to one piece of evidence rather than independent proof. Merge overlapping signals before scoring so repetition does not inflate confidence or capability ratings.

## Save only with permission

When saving is requested, resolve the portfolio root in this order:

1. An approved location the user names;
2. `ACHIEVEMENT_HOME`, if already configured;
3. `~/.agent-achievements/` in the current user's home directory (portable across macOS, Linux, and Windows).

Keep all user data outside the installed skill folder. Read existing portfolio data only as needed for the request and only when the agent has filesystem access. If access is unavailable, provide the files as Markdown for the user to save.

Treat entry references as private and never share or upload them without explicit permission. They are ordinary Markdown files, not encrypted. Before saving them in a shared or cloud-synced location, warn the user.

Create this layout:

```text
<portfolio-root>/
├── portfolio.md
├── entries/
│   └── YYYY-MM-DD--short-slug.md
└── entry-references/
    └── YYYY-MM-DD--short-slug.md
```

Use the templates in `assets/` for new files. Keep the public entry concise. Every saved entry must have one matching private reference. The reference may be minimal, but it must preserve enough context to audit the entry; avoid exact quotations unless necessary. References are private by default and must not be shared unless the user explicitly approves it.

Before writing, detect a likely duplicate by title, date, central evidence, and event identity. Update the existing record or create a new one according to the user's intent. Report exactly which files were created or updated.

## Maintain the dynamic card

Read `references/scoring-rubric.md` and `references/portfolio-schema.md` before adding or changing card dimensions or scores.

Make dimensions emerge from evidence and the user's context; do not use permanent universal categories. Keep up to 6–8 headline dimensions on the main card. Use fewer until sufficient evidence exists, and place other supported dimensions under extended attributes. For every rated dimension show score, confidence, trend, and evidence count.

Use `Not rated` for missing evidence. A strong single example can justify a high score with low confidence. Normally move a score by no more than one point for a new entry; do not reduce it merely because the user has not mentioned that capability recently. Merge overlapping dimensions, and change the main dimensions as the user's work and goals evolve.

## Share safely

Default to the least revealing artifact that serves the request:

- `portfolio.md` for a high-level profile;
- selected entries for a shareable evidence record;
- entry references only with explicit permission.

Do not upload, publish, or disclose any portfolio data without a direct user request.
