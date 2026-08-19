<!-- DEMO — FICTIONAL -->
# DEMO — FICTIONAL Reference: Inventory timeout remediation

## Context

A fictional inventory-service incident reported timeouts affecting approximately 18% of requests. An assistant proposed immediately doubling replicas despite 40% CPU utilization. The user instead investigated traces before changing capacity.

## Evidence

- **Observed:** The user used CPU utilization to question whether horizontal scaling addressed the actual bottleneck, compared successful and failed traces, and localized failures around a slow downstream dependency.
  - **Supports:** Systems diagnosis.
  - **Alternative interpretation:** The scenario does not establish performance across other systems or incidents.

- **Observed:** The user identified duplicate downstream calls and excessive concurrent request accumulation, proposed a duplicate-call removal and bounded semaphore, then used a 10% rollout with monitoring and rollback preparation.
  - **Supports:** Risk-aware technical delivery.
  - **Alternative interpretation:** The scenario reports the solution's result but does not independently verify implementation ownership or all contributing factors.

- **Observed:** The user reported timeouts falling from approximately 18% to 0.6% without adding pods, documented the reasoning, and created a troubleshooting guide.
  - **Supports:** Knowledge sharing and the stated incident outcome.
  - **Alternative interpretation:** The result is a reported team outcome, not evidence of sole ownership.

- **Observed:** The user rejected an unsupported $2 million claim and a solo-hero description, accurately limited the personal contribution, and acknowledged missing a pre-release alert.
  - **Supports:** Evidence discipline, collaborative attribution, and constructive accountability.
  - **Alternative interpretation:** One correction demonstrates calibration in this context but does not establish a permanent trait.

- **Observed:** The user asked a teammate to explain Kafka partitions and consumer-group rebalancing.
  - **Supports:** Curiosity or learning behavior only.
  - **Does not support:** Kafka expertise or competence.

## Sensitivity

DEMO — FICTIONAL. Private by default. Do not include this supporting reference when sharing the corresponding concise entry without explicit approval.
