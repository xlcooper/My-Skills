---
name: project-continuity-manager
description: Bootstrap durable project governance from a user's project design. Use when adding a repository-scoped skill to a new or existing coding/research project and asking AI to inspect the relevant environment, present a visible PROJECT_ENVIRONMENT.md before implementation, initialize the management layer, and write lasting rules into project-local AGENTS.md so future work does not depend on reloading the skill. Do not use for ordinary ongoing tasks after project-local rules exist unless asked to re-bootstrap or reorganize them.
---

# Project Bootstrap and Continuity

Use this skill once at project startup, or later for an explicit governance reset. Convert the user's project design and the observed project state into a durable, project-local operating system for future development.

For repository-scoped discovery, place this skill at:

```text
.agents/skills/project-continuity-manager/
```

Copying the skill into a project does not itself authorize changes. Invoke it when the user is ready to bootstrap or reorganize that project.

## Required Outcome

Before substantive implementation begins:

1. Create or update a concise, user-readable `PROJECT_ENVIRONMENT.md` and present its important findings to the user.
2. Create or merge a root `AGENTS.md` containing the lasting project rules that future AI sessions must follow.
3. Create or update the root project overview and only the additional status or decision records the project actually needs.
4. Address repository initialization and ignore rules when appropriate for a new development project.
5. Verify that the persistent project files agree with the user's design and the observed environment.

After bootstrap, `AGENTS.md` and the project documents are the sources of truth. Do not require future AI sessions to reload or reread this skill for ordinary work.

## Bootstrap Workflow

1. Read the user's project design, constraints, intended users, architecture preferences, delivery target, and success criteria.
2. Inspect existing project instructions, documents, configuration, manifests, lockfiles, entry points, and relevant local tooling before editing.
3. Read `references/project-bootstrap.md` and perform the environment-summary and initialization workflow described there.
4. Use `assets/project-environment-template.md` to create an adapted `PROJECT_ENVIRONMENT.md`. Include verified, relevant facts rather than raw diagnostic output.
5. Show the environment summary before implementation. Pause for the user only when a missing tool, incompatibility, security concern, or unresolved choice could materially change the design.
6. Use `assets/project-agents-template.md` to create or merge the root `AGENTS.md`. Preserve stronger existing project instructions and remove template guidance that does not apply.
7. Read `references/project-rules.md` and establish the smallest useful set of navigation, state, decision, and handoff documents.
8. Verify the resulting project rules, paths, commands, and stated environment facts against the actual project.
9. Report what was initialized, which checks were performed, what remains unverified, and the next development step.

## Ongoing-Work Boundary

If the project already has a suitable root `AGENTS.md` and current project documents, ordinary development should follow those files directly. Invoke this skill again only to:

- bootstrap a missing management layer;
- incorporate a major redesign;
- repair stale or contradictory project guidance;
- refresh the environment baseline after a material toolchain change.

Do not duplicate the entire skill into generated project documentation. Persist only the rules and facts that apply to that project.

## Evidence and Safety

- Distinguish observed facts, user-provided facts, inferences, plans, and unresolved assumptions.
- Never present tool availability, versions, test results, metrics, or completed work as verified without supporting output.
- Never record secret values. Environment summaries may name required variables but must not contain credentials or private access details.
- Start with read-only inspection. Installing software, changing global configuration, configuring remotes, publishing, or other external actions require appropriate user intent and authorization.

## Resources

- Read `references/project-bootstrap.md` for first-use environment summary, repository initialization, and persistent handoff setup.
- Read `references/project-rules.md` for ongoing project documentation and AI working agreements.
- Adapt `assets/project-environment-template.md` into the target project's `PROJECT_ENVIRONMENT.md`.
- Adapt `assets/project-agents-template.md` into the target project's root `AGENTS.md`.
