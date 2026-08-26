# Scoring, comparison, and shareable artifacts

Use this reference when producing readiness scores, comparison scores, or rich shareable outputs. Scores are explainable summaries of the public evidence reviewed, not reputation scores and not guarantees about ranking in any specific AI product.

## Agentic Search Readiness

Score a dimension only when enough public evidence exists to support it. Every scored dimension must include:

- score from 0–100;
- confidence: `high`, `medium`, or `low`;
- evidence count or test count;
- one concise reason for the score.

Use `Not rated` when evidence is insufficient. Never turn missing evidence into a zero.

Suggested dimensions and default weights:

| Dimension | Weight | Question |
| --- | ---: | --- |
| Discoverability | 15% | Can the person be found by name and by relevant work? |
| Identity coherence | 15% | Can profiles, aliases, projects, and domains be connected to the same identity? |
| Agent retrieval | 20% | Do realistic intent searches surface the person or their work without relying on their name? |
| Evidence strength | 15% | Are important claims backed by visible work or credible sources? |
| Authority | 10% | Are there independent references, contributions, citations, collaborations, or other external signals? |
| Freshness | 10% | Do prominent signals reflect current work? |
| Narrative coherence | 15% | Can an agent form one accurate, concise picture of what the person does? |

Compute an overall score only when at least four dimensions are rated. Re-normalize the weights across rated dimensions rather than treating unrated dimensions as zero. Round the final score to the nearest whole number.

Interpretation bands are descriptive, not normative:

- `90–100`: exceptionally clear public graph
- `75–89`: strong
- `60–74`: moderate
- `40–59`: limited
- `<40`: weak or highly fragmented

## Comparison Mode

Comparison is optional. Do not assume the user wants to compare the target with themselves.

If the user has not requested comparison, the agent may offer once after completing the primary profile:

`Want me to compare this profile against you or someone else?`

If the user supplies two targets up front, compare them directly after resolving both identities.

Research both profiles to a similar evidence depth before scoring. Do not compare a deeply researched profile against a thin profile without lowering confidence or gathering more evidence.

### Comparison scores

Use up to three distinct scores because they answer different questions:

**Professional Overlap** — how much the public professional graphs intersect.

Consider domains, problems, technologies, projects, communities, audiences, and current interests.

**Similarity** — how alike the two profiles are in demonstrated work, interests, role shape, and direction.

Similarity is not a personality score. Use professional public evidence only.

**Collaboration Fit** — whether shared interests plus complementary strengths create a credible reason to work, talk, research, invest, hire, or collaborate together.

High similarity does not automatically mean high collaboration fit. Complementary profiles can have high collaboration fit with only moderate similarity.

For every comparison score include:

- score from 0–100;
- confidence;
- strongest supporting overlaps;
- strongest meaningful differences;
- the evidence behind any claimed complementarity.

When useful, also provide:

- **Shared graph:** topics, projects, technologies, organizations, or ecosystems that overlap;
- **Complementary graph:** credible differences that may make the connection useful;
- **Best connection angle:** one evidence-backed reason the two people may benefit from a conversation;
- **Conversation starters:** only when requested or clearly useful.

Do not manufacture a connection merely to increase the score.

## Public professional connections

A rich report may show a connection or identity graph. Include only connections supported by public professional evidence, such as:

- person → company;
- person → project;
- person → publication;
- person → public alias or brand;
- person → coauthor or collaborator;
- person → event, interview, investment, or organization when the relationship is publicly established.

Label inferred connections as inferred. Do not imply friendship, endorsement, employment, investment, partnership, or collaboration without evidence.

## Shareable Artifact Mode

A shareable output should preserve the evidence-backed analysis while making the result easy to scan and share.

A visual artifact is **additive, not substitutive**. Generating a Site, Artifact, PDF, PNG, or image card does not remove the requirement to produce the full evidence-backed report. The canonical report is the source of truth; shareable visuals are presentation layers derived from it.

### Ask based on available capabilities

After the analysis is complete, when the user asks for a shareable version or a rich output and has not already chosen a format:

1. Inspect the output capabilities actually available in the current agent environment.
2. Offer only the supported options among:
   - **Site** — a native hosted or publishable site/report experience;
   - **Artifact** — a native interactive artifact or shareable rich document;
   - **PDF** — a polished multi-page report;
   - **PNG** — a polished image scorecard.
3. Ask the user which available format they want. Do not advertise an option that the current environment cannot create.
4. If the user already selected a supported format, create it without asking again.
5. If only one rich format is available, briefly offer that format rather than presenting a fake menu.
6. If none of these formats are available, return the canonical report as structured Markdown.

Regardless of format, preserve the full report in the conversation or in the generated Site / Artifact / PDF. A standalone PNG or visual card should summarize the findings, not replace the Intelligence Brief, evidence, citations, gap analysis, or comparison when those were part of the run.

Never claim a public/shareable URL was created unless the native tool actually returns one. If publishing a native Site or Artifact changes visibility, requires a separate publish action, or makes the content accessible beyond the conversation, obtain the user approval required by that environment before publishing.

### Canonical report structure

Keep the underlying information architecture stable across output formats.

#### 01 / Scorecard

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

#### 02 / Intelligence Brief

Summarize the research behind the score. Prefer concise high-signal points over a long biography.

Include:

- **Public picture:** what an agent or informed stranger would likely conclude;
- **Current positioning:** what the person appears to be focused on now;
- **Strongest findings:** the most consequential discoveries;
- **Known for / demonstrated work:** strongest public proof;
- **Projects and organizations:** only material associations;
- **Identity graph:** aliases, brands, domains, profiles, and projects and how confidently they connect;
- **Professional connections:** relevant people, organizations, projects, or ecosystems with the relationship type and confidence;
- **Claims vs verification:** only meaningful distinctions;
- **Agent retrieval behavior:** where discovery works and where it fails;
- **Interesting inconsistencies or gaps:** only material ones;
- **Prioritized next moves:** normally three or fewer;
- **Sources / evidence:** concise links or citations sufficient to audit the report.

#### 03 / Comparison

Include only when Comparison Mode was requested.

Show:

- both identities and positioning;
- Professional Overlap score;
- Similarity score when useful or explicitly requested;
- Collaboration Fit score when useful;
- shared graph;
- complementary graph;
- strongest differences;
- best evidence-backed connection angle;
- confidence and evidence basis for every score.

For Sites or interactive Artifacts, render these as sections, tabs, accordions, drill-downs, or another native interaction pattern instead of forcing literal pages. Scores should be expandable to show `Why this score?` evidence when the medium supports interaction.

### Visual guidance

Prefer a restrained editorial or intelligence-report aesthetic over a generic dashboard. Keep one dominant overall score, strong typography, generous whitespace, concise labels, and visibly separated evidence from inference.

When the environment can generate or design rich static visuals, prefer a **research-board / annotated audit** presentation when it improves clarity and memorability. The visual should feel like a worked-through investigation rather than a generic analytics dashboard.

Useful elements can include:

- handwritten or notebook-like headings;
- paper, research-file, or field-notes framing;
- a pinned, taped, clipped, or otherwise editorially framed public profile image when appropriate;
- sketched circles, arrows, underlines, callouts, marginal notes, and evidence annotations;
- visible sections for the public-signal summary, readiness dimensions, primary gap, retrieval tests, identity or connection graph, strongest signals, and next move;
- a mix of polished layout and human research marks that communicates how the conclusion was reached.

Use this research-board style especially when the user wants something memorable, curiosity-driving, social-friendly, or visually expressive. Keep text legible and factual. Decorative marks should reinforce relationships and findings, not create unsupported implications.

For static formats:

- PDF: use the full canonical report, usually 2 pages plus optional comparison page. A designed scorecard or research-board cover may be included, but it does not replace the Intelligence Brief and evidence pages.
- PNG: create a shareable scorecard or research-board summary **in addition to** the full report. It should contain enough context to stand alone visually while pointing back to the deeper analysis.

If image generation is available, the agent should try a strong editorial research-board or annotated-audit treatment for the PNG when suitable rather than defaulting to a sterile dashboard. If that treatment would reduce readability or accuracy, use a cleaner intelligence-report design instead.

If the medium supports only plain text or structured output, fall back to the canonical report without pretending a visual artifact was created.

Do not include private or sensitive information merely because it would make the artifact look more complete.
