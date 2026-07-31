# Ahmad Alkabra

I'm a product leader and zero-to-one builder working across product strategy,
operating design, and technical execution. I build AI products and operating
systems that make agent work inspectable—not just impressive in a demo. My
[public career profile](https://www.linkedin.com/in/aalkabra) describes how I
lead products from concept to market; the repositories below show the technical
depth behind that product/operator work.

## The sixty-second brief

- **Problem — the release decision:** whether agent work may advance cannot rest
  on an agent's own success message. Teams need to know what happened, what
  proves it, and what authority was exercised.
- **Point of view:**
  1. **Decision:** external evaluation. **Rejected:** self-grading.
     **Consequence:** evidence crosses a trust boundary.
  2. **Decision:** separate release authority. **Rejected:** authority embedded
     in the agent or evaluator. **Consequence:** advancement stays explicit.
  3. **Decision:** local proof for this alpha. **Deferred:** live models.
     **Consequence:** failures repeat.
  These are concrete product tradeoffs: each rejected or deferred alternative
  buys the consequence named beside it.
- **Run now:** run the cross-repository proof for the evaluator and bounded
  reference implementation, then run the Maestro quick proof for the operating
  controls.
- **Limits:**
  - **Proof boundary:** deterministic/local fixtures only.
  - **No claims of:** live-model performance, production readiness or scale,
    customer adoption, or business outcomes.

## Three products, three jobs

1. **[Agent Evals Lab](https://github.com/ahmadalkabra/agent-evals-lab)** is
   the independent acceptance gate. It runs deterministic black-box evaluations,
   then re-verifies persisted evidence and artifact integrity.
2. **[Verified Agent Reference](https://github.com/ahmadalkabra/verified-agent-reference)**
   is the inspectable implementation. It makes bounded read/write authority,
   canonical output, and fail-closed behavior concrete.
3. **[Maestro Spine](https://github.com/ahmadalkabra/maestro-spine)** is the
   operating layer. It applies ownership, approval, review, and evidence gates
   to agent-assisted delivery.

## What you can run now

Run the cross-repository proof to exercise the evaluator and bounded reference
together. Run the Maestro quick proof to exercise the operating controls.
Inspect the two versioned releases and Maestro's implementation trail:

- [Cross-repository proof](https://github.com/ahmadalkabra/agent-evals-lab#cross-repo-proof)
- [Evaluator v0.1.0 release](https://github.com/ahmadalkabra/agent-evals-lab/releases/tag/v0.1.0)
- [Reference v0.1.0 release](https://github.com/ahmadalkabra/verified-agent-reference/releases/tag/v0.1.0)
- [Maestro quick proof](https://github.com/ahmadalkabra/maestro-spine#quick-proof)
- [Maestro implementation trail](https://github.com/ahmadalkabra/maestro-spine/pull/1)

## Deterministic/local limits and non-claims

The proof makes no claim beyond deterministic/local fixtures and therefore no
claim of live-model performance. The reference is not production-ready
autonomous software and makes no claim of production scale. Maestro is a
portable methodology layer, not a hosted runtime. This alpha does not claim
customers, adoption, or business outcomes.

Contact: [LinkedIn](https://www.linkedin.com/in/aalkabra)
