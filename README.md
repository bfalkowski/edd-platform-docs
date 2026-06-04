# EDD Platform Docs

Documentation for EDD Platform, an Eval-Driven Design platform for AI agents.

EDD Platform is the workflow/control plane for designing agents, defining scenarios and eval contracts, running versions, diagnosing failures, proposing bounded fixes, comparing candidates, and making gate decisions. Langfuse is treated as the trace/eval evidence data plane.

## Docs site

The Mintlify documentation site lives in [`docs/`](docs/).

```bash
cd docs
npx mint dev
```

The local preview usually runs at `http://localhost:3000`. If that port is already in use, choose another port:

```bash
npx mint dev --port 3333
```

## Structure

- `docs/home.mdx` introduces the product thesis and canonical EDD loop.
- `docs/concepts/` explains the core domain model.
- `docs/architecture/` describes the platform, lab, and Langfuse boundaries.
- `docs/guides/` covers local development and intended contributor workflows.
- `docs/reference/` contains glossary and contract reference material.

## Canonical EDD loop

```text
AgentDesign -> AgentVersion -> Scenario -> EvalContract -> Run
  -> EvalResult / JudgeOutput -> FailurePacket -> FixProposal
  -> candidate AgentVersion -> Comparison -> GateDecision
```
