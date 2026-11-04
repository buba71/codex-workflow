# codex-workflow

Reusable, stack-neutral Codex workflow for new and existing software projects.

It provides seven bounded agent profiles, dynamic activation, planning and handoffs, G0–G5 gates, human authorization rules, and conventions for PRDs, user stories, technical plans and ADRs. It does not prescribe a programming language, framework, database, CI provider or forge.

## Contents

- `AGENTS.md` — universal operating rules and ownership matrix.
- `.codex/agents/` — Product Analyst, Planner, Software Architect, Backend, Frontend, QA and Reviewer.
- `docs/codex-workflow.md` — complexity levels, activation rules, gates and handoffs.
- `templates/AGENTS.project.md` — project-specific adapter template.

## Install in a new project

1. Review this workflow and select the relevant profiles and optional Skills.
2. Copy `AGENTS.md`, `.codex/agents/` and `docs/codex-workflow.md` into the project.
3. Copy `templates/AGENTS.project.md` to the project's `AGENTS.md` only when no project instructions exist.
4. Fill the adapter with the project's stack, architecture, paths, commands, environments, CI, forge and security constraints.
5. If `AGENTS.md` already exists, merge only the adapter sections and preserve its business and technical instructions; do not overwrite it.
6. Validate the profiles and run a safe, read-only workflow walkthrough before implementation.

## Adapt an existing project

Classify its current instructions into universal, stack-specific and project-specific rules. Keep existing business and technical conventions, add the universal workflow once, and place stack-specific commands in the project adapter. Add Skills only for relevant changed surfaces or review concerns.

## Updating the workflow

Treat this project as the source of reference. Update a consuming project's workflow deliberately after reviewing the diff, preserving local instructions and re-running its profile, permission and validation checks. Do not use an automatic installer or overwrite existing files.

## Scope

This repository contains documentation and agent profiles only. It has no application code, dependency manifest, CI pipeline or deployment configuration. No commit, push, remote repository or project migration is implied by using it.
