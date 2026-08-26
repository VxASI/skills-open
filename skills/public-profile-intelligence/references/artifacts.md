# Shareable artifacts

Read this reference only when the user asks for a shareable report, scorecard, visual, Site, Artifact, PDF, PNG, or another rich presentation.

The full evidence-backed analysis remains the source of truth. Rich outputs are presentation layers derived from that report.

A visual artifact is **additive, not substitutive**. Generating a Site, Artifact, PDF, PNG, or image card does not remove the requirement to produce the full report.

## Ask based on available capabilities

After the analysis is complete, if the user has not already chosen a format:

1. Inspect the output capabilities actually available in the current agent environment.
2. Offer only the supported options among:
   - **Site** — native hosted or publishable site/report experience;
   - **Artifact** — native interactive artifact or shareable rich document;
   - **PDF** — polished multi-page report;
   - **PNG** — polished image scorecard or research-board summary.
3. Ask which available format the user wants.
4. If the user already selected a supported format, create it without asking again.
5. If only one rich format is available, offer that format rather than presenting a fake menu.
6. If none are available, return the canonical report as structured Markdown.

Never advertise or claim a capability the environment does not actually provide.

Never claim a public/shareable URL exists unless the native tool actually returns one. If publishing changes visibility or requires a separate publish action, follow the host environment's approval rules.

## Preserve the report

Regardless of format, preserve the full report in the conversation or in the generated Site, Artifact, or PDF.

A standalone PNG or visual card should summarize findings but must not replace:

- the Intelligence Brief;
- evidence and citations;
- claims vs verification;
- retrieval and gap analysis;
- comparison findings when comparison was part of the run.

## Canonical information structure

### 01 / Scorecard

Designed to be immediately scannable and shareable.

Include when supported:

- identity / handle / current positioning;
- Agentic Search Readiness overall score;
- confidence;
- 5–7 scored dimensions;
- primary gap;
- strongest public signals;
- 3–5 sampled retrieval intents and results;
- one high-leverage next move;
- audit date and a short methodology note.

### 02 / Intelligence Brief

Summarize the research behind the score. Prefer concise, high-signal points over a long biography.

Include:

- **Public picture**;
- **Current positioning**;
- **Strongest findings**;
- **Known for / demonstrated work**;
- **Projects and organizations**;
- **Identity graph**;
- **Professional connections**;
- **Claims vs verification**;
- **Agent retrieval behavior**;
- **Interesting inconsistencies or gaps**;
- **Prioritized next moves**;
- **Sources / evidence**.

### 03 / Comparison

Include only when Comparison Mode was requested.

Show:

- both identities and positioning;
- Professional Overlap;
- Similarity when useful or explicitly requested;
- Collaboration Fit when useful;
- shared graph;
- complementary graph;
- strongest differences;
- best evidence-backed connection angle;
- confidence and evidence basis for every score.

For Sites or interactive Artifacts, these may become sections, tabs, accordions, or drill-downs rather than literal pages. When possible, make scores expandable to show `Why this score?` evidence.

## Visual guidance

Prefer a restrained editorial or intelligence-report aesthetic over a generic dashboard. Keep one dominant overall score, strong typography, generous whitespace, concise labels, and visibly separated evidence from inference.

When the environment can generate or design rich static visuals, prefer a **research-board / annotated audit** presentation when it improves clarity and memorability. The visual should feel like a worked-through investigation rather than a generic analytics dashboard.

Useful elements can include:

- handwritten or notebook-like headings;
- paper, research-file, or field-notes framing;
- a pinned, taped, clipped, or otherwise editorially framed public profile image when appropriate;
- sketched circles, arrows, underlines, callouts, marginal notes, and evidence annotations;
- visible sections for public-signal summary, readiness dimensions, primary gap, retrieval tests, identity or connection graph, strongest signals, and next move;
- a mix of polished layout and human research marks that communicates how the conclusion was reached.

Use this research-board style especially when the user wants something memorable, curiosity-driving, social-friendly, or visually expressive. Keep text legible and factual. Decorative marks should reinforce relationships and findings, not create unsupported implications.

## Static format behavior

- **PDF:** use the full canonical report, usually 2 pages plus optional comparison page. A designed scorecard or research-board cover may be included, but it does not replace the Intelligence Brief and evidence pages.
- **PNG:** create a shareable scorecard or research-board summary **in addition to** the full report. It should contain enough context to stand alone visually while pointing back to the deeper analysis.

If image generation is available, try a strong editorial research-board or annotated-audit treatment for the PNG when suitable rather than defaulting to a sterile dashboard. If that treatment would reduce readability or accuracy, use a cleaner intelligence-report design instead.

If the medium supports only plain text or structured output, fall back to the canonical report without pretending a visual artifact was created.

Do not include private or sensitive information merely because it would make the artifact look more complete.
