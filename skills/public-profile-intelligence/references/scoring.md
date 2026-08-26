# Readiness scoring

Read this reference before assigning numeric Agentic Search Readiness scores.

Scores are explainable summaries of the public evidence reviewed. They are not reputation scores and do not guarantee ranking in any specific AI product.

## Scoring rules

Score a dimension only when enough public evidence exists to support it. Every scored dimension must include:

- score from 0–100;
- confidence: `high`, `medium`, or `low`;
- evidence count or test count;
- one concise reason for the score.

Use `Not rated` when evidence is insufficient. Never turn missing evidence into a zero.

## Suggested dimensions and weights

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

## Interpretation bands

These bands are descriptive, not normative:

- `90–100`: exceptionally clear public graph
- `75–89`: strong
- `60–74`: moderate
- `40–59`: limited
- `<40`: weak or highly fragmented

Always keep the underlying dimension scores visible so the composite is auditable.
