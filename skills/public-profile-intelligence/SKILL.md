---
name: public-profile-intelligence
description: Research a person, founder, creator, company, or the user's own public profile using public professional information. Build a concise, evidence-backed picture of identity, work, projects, claims, credibility, discoverability, relevant overlap, agentic search readiness, and optional professional comparison. Use when the user asks to research someone, verify a professional claim, understand a new connection, evaluate a public profile, audit their own public footprint, test how well an AI agent could discover and understand them from the public web, compare two public professional profiles, or create a shareable intelligence report.
---

# Public Profile Intelligence

Turn scattered public information into a concise, evidence-backed profile.

The goal is not to collect everything about someone. Answer:

**Who does the public internet think this person is, what can actually be verified, and what matters to the user?**

For self-audits, also ask:

**If an AI agent were looking for someone with this person's actual capabilities, would it find and correctly understand them?**

## Progressive loading

Use this file as the core workflow. Read deeper references only when that capability is needed:

- `references/agentic-search.md` — self-audits, intent-based retrieval tests, public-graph gaps, machine-readable identity.
- `references/scoring.md` — numeric Agentic Search Readiness scoring.
- `references/comparison.md` — Professional Overlap, Similarity, Collaboration Fit, connection graphs.
- `references/artifacts.md` — Site / Artifact / PDF / PNG behavior, canonical report structure, research-board visual guidance.

Do not load optional references for a simple quick background check unless they materially help the task.

## Principles

- Use public professional information only.
- Prefer primary sources, then credible independent sources.
- Separate claims from verification.
- Do not infer sensitive personal attributes.
- Do not search for private addresses, phone numbers, family information, private accounts, leaked data, or data-broker records.
- Never merge profiles based on name alone.
- Cite important conclusions and say when something cannot be verified.
- Optimize for signal, not completeness.
- For agentic-search audits, optimize for accurate machine discoverability rather than keyword stuffing or generic SEO advice.
- For scores and comparisons, use explainable public evidence rather than vibes. Missing evidence is `Not rated`, not zero.

## Inputs

Accept any useful starting point:

- name
- screenshot
- professional profile URL
- GitHub or social handle
- personal website
- company
- project
- a second person or profile for comparison
- any combination of the above

If identity is ambiguous, resolve identity before deeper research.

## Core workflow

Stop when additional searching is unlikely to materially change the answer.

### 1. Resolve identity

Establish likely identity using multiple matching signals when possible:

- name
- role or company
- linked websites
- usernames
- project ownership
- education or employment when publicly stated
- broad professional location when relevant

Assign `Identity confidence: High | Medium | Low`.

### 2. Map the primary footprint

Prioritize sources in this order when available:

1. personal website
2. GitHub and project repositories
3. company website
4. LinkedIn or other professional profiles
5. publications, talks, documentation, podcasts, and interviews
6. reputable independent sources

Determine:

- what they appear to do now
- what they build or publish
- strongest publicly demonstrated work
- organizations and projects associated with them
- how aliases, brands, projects, and identities connect

### 3. Verify consequential claims

Do not fact-check every sentence. Verify claims that materially affect credibility, relevance, or a decision.

Classify evidence as:

- **Verified** — supported by a strong primary source or credible independent evidence.
- **Self-claimed** — stated by the person or company but not independently confirmed.
- **Inferred** — reasonable conclusion from multiple public signals but not explicitly established.
- **Unverified** — searched for but insufficient evidence was found.

Absence of evidence is not evidence of absence.

### 4. Find relevance

When researching another person, identify genuine overlap with the user's stated context when available:

- technologies
- research interests
- products
- problems being explored
- potential collaboration
- complementary expertise

Explain why the overlap matters. Do not invent a networking reason merely to fill the section.

## Modes

### Quick Mode

Use for a quick check, quick background, or screenshot-led lookup.

1. Resolve identity.
2. Run a shallow primary-source search.
3. Find 2–4 strongest signals.
4. Verify only consequential claims.
5. Explain relevance.
6. Stop.

Target a report readable in under one minute.

### Deep Mode

Use when requested or when a consequential decision needs stronger verification.

Expand into relevant areas such as career timeline, company history, repository activity, publications, partnerships, customer claims, funding, patents, talks, interviews, independent mentions, and inconsistencies.

Explicitly separate confirmed information from unresolved claims.

### Self-Audit / Agentic Search Mode

Read `references/agentic-search.md`.

Use when the target is the user, or when the goal is to test how AI agents discover and understand the person from the public web.

If numeric readiness scores are requested or useful, also read `references/scoring.md`.

### Comparison Mode

Read `references/comparison.md`.

Use when the user asks to compare two public professional profiles, asks how similar they are professionally, wants to understand overlap, or wants a collaboration-fit view.

Do not assume comparison against the user unless requested.

### Shareable Artifact Mode

Read `references/artifacts.md`.

Use when the user asks for a shareable report, scorecard, visual, Site, Artifact, PDF, PNG, or another rich presentation.

Complete the full evidence-backed analysis first. The visual or artifact is a presentation layer, not a replacement for the report.

Inspect the current environment and offer only output types it can actually create. Never claim a public URL exists unless the host tool actually returns one.

## Default output

### Public Signal
One paragraph describing what a stranger would likely conclude.

### Confidence
Identity: High / Medium / Low
Professional footprint: Strong / Moderate / Thin

### Known For
Maximum 3–5 high-signal items.

### Evidence
The strongest evidence supporting the profile.

### Claims vs Verification
Include only when meaningful claims need qualification.

### Relevant Overlap
Include when researching someone for a conversation, collaboration, hire, investment, partnership, or similar professional relationship.

### Agentic Search Readiness
Include for agentic-search audits. Read `references/agentic-search.md`; read `references/scoring.md` before assigning numeric scores.

### Comparison
Include only when requested. Read `references/comparison.md`.

### Gaps
Important missing connections, weak evidence, conflicting information, or discoverability problems.

### Next Move
Recommend the single most useful next action. For self-audits, optionally include up to three prioritized improvements.

## Safety

This skill is for professional public-profile intelligence, not personal surveillance.

Never:

- locate someone's home
- collect private contact information
- investigate family members without a clear public professional reason
- use leaked credentials or breached datasets
- infer protected or sensitive traits
- construct psychological profiles
- facilitate harassment or stalking

When uncertain, collect less.

## Standard

Every meaningful conclusion should be traceable to evidence.

**Search broadly. Verify selectively. Report only signal.**