<!-- DEMO — FICTIONAL -->
# DEMO — FICTIONAL: Inventory timeout remediation

Investigated the actual dependency bottleneck before scaling capacity, then used a controlled rollout to reduce reported inventory-service timeouts from approximately 18% to 0.6%.

## Signals

- **Observed:** Questioned whether more pods would help when CPU was only 40%, compared successful and failed traces, found a slow downstream dependency, duplicate downstream calls, and excessive concurrent accumulation.
- **Inference:** Demonstrated strong systems diagnosis in this incident.
- **Why it mattered:** The response addressed the reported bottleneck without adding pods.
- **Confidence:** low — this is one detailed incident.

- **Observed:** Proposed removing the duplicate call, bounded downstream concurrency, released to 10% of traffic, monitored latency and errors, and prepared rollback before expansion.
- **Inference:** Demonstrated strong risk-aware technical delivery in this incident.
- **Why it mattered:** The change used a limited, observable blast radius.
- **Confidence:** low — this is one detailed incident.

- **Observed:** Rejected unsupported financial and individual-credit claims, identified the result as a team outcome, and scoped the personal contribution to investigation, validation, and rollout proposal.
- **Inference:** Demonstrated evidence discipline and collaborative attribution.
- **Why it mattered:** The impact statement remains credible and fair.
- **Confidence:** low — this is one detailed incident.

## Card impact

- Systems diagnosis: supporting evidence added; 8/10, low confidence, ↑
- Risk-aware technical delivery: supporting evidence added; 8/10, low confidence, ↑
- Evidence discipline and collaborative attribution: supporting evidence added; 8/10, low confidence, ↑
- Knowledge sharing: supporting evidence added; 6/10, low confidence, ↑
- Kafka expertise: not rated; a learning question alone does not demonstrate competence.

## Growth edge

- **Opportunity:** Alert coverage was not created before the original release.
- **Next time:** Include dependency alert coverage and a monitoring/rollback readiness check before release.

## Reuse drafts

- **Colleague:** I helped reduce inventory-service timeouts from ~18% to 0.6% by tracing the failing path, removing a duplicate downstream call, bounding concurrency, and using a monitored 10% canary with rollback ready.
- **Interview:** When a service had high timeouts, I challenged a capacity-first assumption with CPU data, used traces to identify a downstream bottleneck, and rolled out a targeted concurrency fix safely. I also documented the learning and improved alert coverage afterward.
- **X:** A useful incident habit: before scaling, compare successful and failed traces. In one case that exposed a duplicate dependency call and uncontrolled concurrency—fixing those cut timeouts from ~18% to 0.6% with a cautious canary rollout.

## Reference

Private supporting context: `../entry-references/2026-08-18--inventory-timeout-remediation.md`
