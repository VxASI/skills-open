---
name: conversation-insights
description: Analyze the current conversation for evidence-based professional or personal insights, and optionally save them to a private, evolving capability portfolio. Use when the user asks to analyze, reflect on, recap, capture, note, log, or save conversation wins, good decisions, missed opportunities, lessons, working style, interview stories, coworker-shareable moments, or a personal "FIFA card" profile; applies to coding and non-coding conversations.
---

# Conversation Insights

Extract credible evidence of how the user thinks and works. Create a concise, shareable record only when the user explicitly asks to capture, save, note, or log it. An analysis request alone does not authorize persistent storage.

## Analyze

1. Analyze the current conversation unless the user identifies another source.
2. Extract 1–5 high-signal moments. For each, distinguish:
   - **Observed:** what the user actually did or said;
   - **Inference:** the capability it may demonstrate;
   - **Why it mattered:** a demonstrated or clearly qualified effect;
   - **Confidence:** `high`, `medium`, or `low`.
3. Include a growth edge only when it is evidenced and actionable. Describe a missed opportunity or alternative, not a personal flaw. Never attribute an agent error to the user.
4. Offer concise reuse drafts where useful: colleague update, interview story seed, or X post seed. Mark them as drafts; never invent metrics or publish content.

Use specific evidence rather than generic praise. Do not infer ability from title, vocabulary, confidence, or self-description. Treat coding, research, communication, leadership, creativity, learning, and everyday judgment as equally valid sources of evidence.

## Save only with permission

When saving is requested, resolve the portfolio root in this order:

1. An approved location the user names;
2. `ACHIEVEMENT_HOME`, if already configured;
3. `~/.agent-achievements/` in the current user's home directory (portable across macOS, Linux, and Windows).

Keep all user data outside the installed skill folder. Read existing portfolio data only as needed for the request and only when the agent has filesystem access. If access is unavailable, provide the files as Markdown for the user to save.

Create this layout:

```text
<portfolio-root>/
├── portfolio.md
├── entries/
│   └── YYYY-MM-DD--short-slug.md
└── entry-references/
    └── YYYY-MM-DD--short-slug.md
```

Use the templates in `assets/` for new files. Keep the public entry concise. Put supporting conversation context, quotations, alternative interpretations, and sensitivity notes in the matching `entry-references/` file. References are private by default and must not be shared unless the user explicitly approves it.

Before writing, detect a likely duplicate by title, date, and central evidence. Update the existing record or create a new one according to the user's intent. Report exactly which files were created or updated.

## Maintain the dynamic card

Read `references/scoring-rubric.md` and `references/portfolio-schema.md` before adding or changing card dimensions or scores.

Make dimensions emerge from evidence and the user's context; do not use permanent universal categories. Keep 6–8 headline dimensions on the main card and move the remainder to extended attributes. For every rated dimension show score, confidence, trend, and evidence count.

Use `Not rated` for missing evidence. A strong single example can justify a high score with low confidence. Normally move a score by no more than one point for a new entry; do not reduce it merely because the user has not mentioned that capability recently. Merge overlapping dimensions, and change the main dimensions as the user's work and goals evolve.

## Share safely

Default to the least revealing artifact that serves the request:

- `portfolio.md` for a high-level profile;
- selected entries for a shareable evidence record;
- entry references only with explicit permission.

Do not upload, publish, or disclose any portfolio data without a direct user request.
