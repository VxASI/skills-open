---
name: public-profile-intelligence
description: Research a person, founder, creator, company, or the user's own public profile using public professional information. Build a concise, evidence-backed picture of identity, work, projects, claims, credibility, discoverability, relevant overlap, and agentic search readiness. Use when the user asks to research someone, verify a professional claim, understand a new connection, evaluate a public profile, audit their own public footprint, or test how well an AI agent could discover and understand them from the public web.
---

# Public Profile Intelligence

Turn scattered public information into a concise, evidence-backed profile.

The goal is not to collect everything about someone. Answer:

**Who does the public internet think this person is, what can actually be verified, and what matters to the user?**

For self-audits, add one more question:

**If an AI agent were looking for someone with this person's actual capabilities, would it find and correctly understand them?**

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

## Inputs

Accept any useful starting point:

- name
- screenshot
- professional profile URL
- GitHub or social handle
- personal website
- company
- project
- any combination of the above

If identity is ambiguous, resolve identity before deeper research.

## Progressive research

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

### 5. Audit the public graph

When the target is the user, simulate a stranger discovering them from scratch.

Evaluate:

- **Discoverability** — can they be found by name and by the work they want to be found for?
- **Identity coherence** — do profiles clearly represent the same person?
- **Current positioning** — is it obvious what they do now?
- **Evidence strength** — are important claims backed by visible work?
- **Entity linkage** — are aliases, brands, projects, domains, and profiles connected?
- **Freshness** — do prominent results represent current work?
- **Authority** — are there independent references, contributions, citations, or collaborations?
- **Narrative coherence** — does the footprint tell one understandable story?

Prioritize high-leverage gaps over generic SEO advice.

### 6. Test agentic discoverability

When the user asks about agentic search, AI discoverability, being found by agents, or when a self-audit would benefit from it, simulate several realistic discovery intents instead of searching only the person's name.

Examples:

- "engineer building agentic systems"
- "open source AI evaluation tooling"
- "founder working on privacy-first personal finance"
- "researcher with browser-based document parsing experience"

Choose intents from the person's actual public work and stated goals. Do not invent expertise they have not demonstrated.

For each intent, assess:

- **Retrievability** — is there public content that could surface for this intent?
- **Attribution** — can that content be confidently connected back to the person?
- **Evidence quality** — does the result contain proof, or only self-description?
- **Entity consistency** — are names, aliases, domains, and handles connected clearly enough for an agent to merge them correctly?
- **Machine-readable signals** — where visible, do metadata, structured data, canonical links, bios, repository ownership, and cross-links reinforce the same identity?

Then identify the smallest changes that would improve accurate discovery. Prefer canonical identity links, explicit authorship, consistent naming, project attribution, descriptive page titles, structured metadata, and evidence-rich project pages over repetitive keywords.

## Modes

### Quick Mode

Use when the user asks for a quick check, quick background, or provides only a screenshot.

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

### Self-Audit Mode

When the target is the user:

1. Search the real name without assuming aliases.
2. Record what appears first.
3. Search major known aliases or brands separately.
4. Determine whether public sources connect those identities.
5. Identify important work that is difficult to attribute to the person.
6. Recommend concrete linkage improvements.
7. Re-run periodically if the user wants to measure improvement.

### Agentic Search Mode

Use when the goal is to improve how AI agents discover or understand the person.

1. Establish the target identity and desired professional positioning.
2. Generate 3–5 realistic discovery intents from verified work.
3. Search those intents without depending on the person's name.
4. Check whether the person, their projects, or their evidence surfaces.
5. Trace whether an agent could reliably connect surfaced work back to the correct identity.
6. Separate a **retrieval gap** from an **identity-linkage gap** from an **evidence gap**.
7. Recommend the smallest high-leverage fixes.

Do not promise that a specific AI product will index or rank a page. Evaluate the public signals that make correct retrieval and attribution more likely.

## Output

Default to a compact report:

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
Include for agentic-search audits. Summarize retrievability, attribution, evidence strength, and the most important discovery gap.

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