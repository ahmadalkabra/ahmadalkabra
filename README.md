# Ahmad Alkabra

I'm a senior product leader and hands-on zero-to-one builder. I work across
product strategy, operating design, and technical execution, especially on AI
products where a polished result can arrive before a trustworthy release
decision.

My [LinkedIn profile](https://www.linkedin.com/in/aalkabra) covers the products
and teams I've led from concept to market. These repositories show how I turn
that product judgment into working, inspectable systems.

## What I'm building

I keep coming back to three questions: What did the agent actually do? What was
it allowed to do? Who decides whether the result moves forward?

- **[Agent Evals Lab](https://github.com/ahmadalkabra/agent-evals-lab)** checks
  an agent from the outside. It can run a local command against a disposable
  snapshot of a real repository, save the report, and re-verify the evidence.
- **[Verified Agent Reference](https://github.com/ahmadalkabra/verified-agent-reference)**
  is a small offline agent with explicit read/write permissions and fail-closed
  behavior that can be inspected end to end.
- **[Maestro Spine](https://github.com/ahmadalkabra/maestro-spine)** is the
  operating rulebook around the work: ownership, review, human approval, and
  evidence before release.

Together, the three projects separate implementation, evaluation, and release
authority. The system doing the work does not also get to grade itself and
decide to ship.

## Start here

1. Run the [real-project starter](https://github.com/ahmadalkabra/agent-evals-lab#real-project-starter)
   against a selected local Git repository.
2. Reproduce the [cross-repository proof](https://github.com/ahmadalkabra/agent-evals-lab#cross-repo-proof)
   with the evaluator and bounded reference agent.
3. Run the [Maestro quick proof](https://github.com/ahmadalkabra/maestro-spine#quick-proof)
   to inspect the operating controls.

Versioned releases:
[Agent Evals Lab v0.1.1](https://github.com/ahmadalkabra/agent-evals-lab/releases/tag/v0.1.1)
and
[Verified Agent Reference v0.1.0](https://github.com/ahmadalkabra/verified-agent-reference/releases/tag/v0.1.0).

## Evidence boundary

The current evidence covers deterministic local fixtures and one bundled
offline adapter applied to a disposable snapshot of committed repository state.
It does not establish live-model performance, independent third-party adapter
compatibility, production readiness, customer adoption, or business outcomes.
The reference agent is deliberately narrow, and Maestro is a portable
methodology rather than a hosted runtime.

Contact: [LinkedIn](https://www.linkedin.com/in/aalkabra)
