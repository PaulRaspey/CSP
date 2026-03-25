# CSP Validation Results

## Semantic Continuity Score (SCS) Runs

| Run | Topic | CDS (1–5) | Session B SCS | Cold Start SCS | Gain |
|-----|-------|-----------|---------------|----------------|------|
| 1 | Consciousness / substrate | 5 | 0.90 | 0.60 | 1.50x |
| 2 | Math proof | 2 | 0.80 | 0.80 | 1.00x |
| 3 | Free will concession | 4 | 0.85 | 0.65 | 1.31x |

## Context Dependency Score (CDS) Rubric

CDS is rated 1–5 **before** each run, blind to the expected outcome.

| Score | Meaning |
|-------|---------|
| 1 | Final message is fully self-contained. A cold start handles it perfectly. |
| 2 | Minor shared vocabulary, but the message is mostly standalone. |
| 3 | Final message references prior conclusions but could be partially reconstructed. |
| 4 | Final message only makes sense if you have accepted the prior reasoning chain. |
| 5 | Final message is the product of accumulated epistemic state that cannot be reconstructed from the message alone. |

## Key Finding

CSP gain correlates with context-dependency of the final message. Self-contained messages (CDS 1–2) show no gain. Contextually dependent messages (CDS 4–5) consistently hit or exceed target SCS.

This suggests CSP is compressing **epistemic preconditions**, not content — meaning the value of the packet scales with how much prior reasoning is required to interpret the final exchange.

## Next Runs

- Run 4: High CDS target (score 5) — collaborative creative decision or negotiated ethical position
- Run 4 control: Low CDS (score 1) — standalone factual question, same session
