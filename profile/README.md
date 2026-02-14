# AgentReadyDocs

Open-source templates, rubrics, and co-authoring skills for agent-ready documentation.

Agent-ready means explicit enough for reliable implementation by LLM agents with minimal back-and-forth.

## Start Here

- `spec-kit` (templates, rubrics, and skills): https://github.com/AgentReadyDocs/spec-kit

## How To Use This Org

1. Start from `spec-kit` and pick the closest template for your use case.
2. Fill the template with explicit entities, constraints, invariants, and acceptance tests.
3. Use rubrics and linting rules (where provided) to catch ambiguity, missing constraints, and unresolved unknowns.
4. Use skills from `spec-kit/skills/` (Claude Code, Codex, etc.) to co-author and iterate.
5. Gate changes with reviewer feedback and pass/fail criteria before implementation.

## Why

Most specs are written for humans first and leave too much implicit for LLM agents.  
This org focuses on specification artifacts that are explicit enough for reliable implementation with minimal back-and-forth.

## What We Publish

- Specification templates (use cases, NFRs, ADRs, and related formats)
- Shared quality rubrics with pass/fail gates
- Co-authoring skills for structured elicitation and iterative refinement
  (including Claude Code and Codex workflows, where provided)
- Validation and linting assets where useful

## Public Content Policy

All content here is public and intended for open collaboration.

- Do not include confidential, customer-specific, or non-public business information.
- Do not include personal data (PII), credentials, or secrets.

## Design Principles

- Schema first: define entities, fields, constraints, and interfaces explicitly.
- Unknowns are first-class: mark `[OPEN]`, `[ASSUMPTION]`, and decision owners.
- Invariants over narrative: state what must/never happen.
- Reduce variance in behavioral outcomes: constrain state transitions, errors, and side effects so independent implementations converge on the same externally observable behavior.
- Acceptance criteria as tests: make “done” machine-checkable.

## Non-goals

- Identical code or identical artifacts across implementations.
- “Guaranteed one-shot” implementation success claims.
- Any evaluation infrastructure beyond generating excellent agent-ready documentation.

## Recommended Authoring Flow

1. Author draft against a strict template.
2. Critic pass against rubric with concrete failing spans and patch guidance.
3. Revision with change log.
4. Compliance gate for binary pass/fail.

## Initial Repository Shape

- `spec-kit`: canonical templates, rubric, and validation/lint rules
  https://github.com/AgentReadyDocs/spec-kit
  (includes `skills/` for co-authoring and review workflows)

## Intended Outcomes

- Reduce ambiguity before implementation starts.
- Make unknowns explicit instead of silently assumed.
- Increase first-pass implementation success rate for LLM-assisted delivery.
- Keep review quality consistent via shared rubrics and gates.

## Contributing

Contributions are welcome: new templates, rubric improvements, validation rules, and skills in `spec-kit/skills/` that improve clarity and reliability for agent execution.
