# CSP: Cognitive State Protocol

**What if a thought was portable? What if you could hand off a complex idea mid-sentence to a completely different AI — and it just continued?**

CSP is the third layer of the UAHP stack. It defines a universal format for transferring the semantic state of an AI reasoning session — the actual *meaning* of what is being thought — between any two models, on any hardware, across any network.

## The problem it solves

Every AI session is currently an island. When you switch from Claude to GPT to a local model, you start over. When your phone hands off to your PC, it might move the data but not the thought. When a session ends, the reasoning chain is gone. CSP ends that.

## How it works

CSP compresses a conversation into five semantic state vectors:

| Vector | What it captures |
|---|---|
| Intent | What the session is working toward |
| Reasoning chain | The logical steps taken so far |
| Entity graph | People, concepts, and relationships referenced |
| Uncertainty map | What the model knows it does not know |
| Momentum | The direction and velocity of the current reasoning |

These five vectors are compressed to a 50× smaller universal embedding, signed with a Fidelity Certificate, transported via UAHP v0.5.4 encrypted sessions, and reconstructed into a cognitive primer that any receiving model can use to continue the thread. Note: direct UAHP transport integration is planned for v0.3; current implementation validates the semantic compression layer independently via Groq.

## The grand challenge metric

**SCS — Semantic Continuity Score**

```
SCS = human_preference_rating(continuation_by_model_B)
      ÷
human_preference_rating(continuation_by_original_model_A)
```

Target: SCS ≥ 0.85 across all cross-model pairs. This is the number that makes the paper real. When we can show that Model B continues a thought from Model A at 85% of the quality of Model A continuing its own thought — with a 50× smaller packet — that is the result.

## The complete stack

| Layer | Protocol | What it provides |
|---|---|---|
| 1 | UAHP v0.5.4 | Who you are — identity, trust, transport |
| 2 | SMART-UAHP | Where you think — energy-optimal substrate routing |
| 3 | CSP | What you are thinking — portable semantic state |

Together: any agent, anywhere, hands off any thought to any other agent, at the lowest energy cost, with cryptographic proof that the thought survived the journey.

## Status

Version 0.2.0 — architecture and simulation complete. Semantic encoder training in progress.

## Dependencies

- [UAHP v0.5.4](https://github.com/PaulRaspey/uahp) — transport and identity
- [SMART-UAHP v0.1.0](https://github.com/PaulRaspey/SMART-UAHP) — substrate routing

## License

MIT. Part of the continuation of the universal project of knowing itself.

## Author

Paul Raspey
