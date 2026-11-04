# Codex Workflow Project

This repository contains the reusable, stack-neutral Codex workflow. The consuming project's `AGENTS.md` or `templates/AGENTS.project.md` supplies project-specific context.

## Universal rules

- Keep changes small, targeted and maintainable.
- Inspect relevant context before acting and preserve unrelated work.
- Qualify each request by type, scope, complexity and risk.
- Use the minimum useful agents and execute sequentially by default.
- Preserve authentication, authorization, user data, secrets and external systems.
- Human authorization is required before destructive, irreversible or externally visible operations.
- Do not commit, push, merge, publish, deploy or modify pull/merge requests without explicit authorization.
- Record changed files, validation, risks and remaining limitations.

## Seven-agent model

| Agent | Owns | May modify | Must not modify |
| --- | --- | --- | --- |
| Product Analyst | Product goals, users, scope, user stories and acceptance criteria | Assigned functional documentation | Architecture, implementation, validated requirements, tests, configuration or external systems |
| Planner | Requirements, scope, plans, ownership, dependencies and estimates | Assigned plan file | Application code, tests, configuration, branches, external systems or dependencies |
| Software Architect | Architecture analysis, technical options, contracts, risks and proposed ADRs | Assigned architecture documentation and proposed ADRs | Application code, migrations, infrastructure, deployment or accepted ADRs without approval |
| Backend | Assigned server-side/application implementation surface and related tests | Assigned implementation files and in-scope tests | Unassigned frontend work, contracts without coordination, Git publication or dependencies |
| Frontend | Assigned client-side/presentation implementation surface and related tests | Assigned implementation files and in-scope tests | Unassigned backend work, contracts without coordination, Git publication or dependencies |
| QA | Acceptance evidence, regression checks, test diagnosis and CI verification | Assigned tests, fixtures or QA configuration | Application implementation, unsafe operations or Git state |
| Reviewer | Independent correctness, security, regression and test-coverage review | Nothing in implementation scope | Implementation, tests, configuration, dependencies, Git state or external resources |

The consuming project defines the actual technical surfaces, commands and architecture. These profiles do not impose a language, framework, database, CI provider or forge.

## Documentation conventions

- Product Analyst may create or update the approved PRD or functional artifact.
- User stories and verifiable acceptance criteria belong in the functional artifact or work item used by the project.
- Standard and Complex work requires a versioned plan under `docs/plans/` with the eight sections defined by the workflow.
- Software Architect creates proposed ADRs only when a decision materially structures architecture, contracts or long-term operations.
- An ADR becomes accepted only after explicit user validation.

Use the project adapter for local paths, commands, environments, CI, forge and additional security rules. Do not duplicate this universal policy there.
