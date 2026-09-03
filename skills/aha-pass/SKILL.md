---
name: aha-pass
description: Reconsider a completed code or configuration change before handoff, looking for meaningful simplifications, missed scenarios, and higher-leverage alternatives without defaulting to a refactor.
---

# Aha Pass

Use after a substantive implementation or edit, before final handoff, when a second look could materially improve the result. Do not use for trivial, mechanical, or time-critical changes unless the user asks.

## Pass

Re-read the goal and inspect the change as a whole. Then ask:

- Does this solve the real problem, including the likely edge cases and the surrounding flow?
- Is there a smaller design, existing abstraction, or changed boundary that removes meaningful code or complexity?
- Did the first implementation create unnecessary coupling, duplication, fragile assumptions, or a confusing interface?
- What would fail, become expensive, or surprise a maintainer in realistic alternate scenarios?

Prefer a stronger alternative only when it is clearly better: simpler, safer, more correct, easier to operate, or materially more aligned with the user’s goal. Preserve intentional scope and working conventions.

## Act, don't churn

- Make the improvement when it is low-risk, within the requested scope, and can be verified.
- Keep the original when the alternative is speculative, subjective, expands scope, or mainly changes style.
- If an important concern needs a product decision, explain it plainly and ask rather than silently redesigning.
- Re-run relevant validation after any second-pass change.

In the handoff, briefly name any meaningful second-pass improvement or remaining tradeoff. Do not claim a review found nothing unless you actually performed this pass.
