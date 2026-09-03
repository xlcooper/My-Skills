---
name: project-foundation
description: Bootstrap or retrofit a project with a durable, personalized working foundation. Use for a project draft, new project, or existing project when the user wants local Git, a public README, root AGENTS.md guidance, and concise Chinese environment, change-log, and execution-report artifacts that let future work continue without this skill. Do not use for ordinary project work once these foundations exist unless asked to repair or rebuild them.
---

# Project Foundation

Use this skill once to turn a project draft or an existing project into a durable, project-local working foundation. The resulting root documents, not this skill, must support future development.

For repository-scoped discovery, place this skill at:

```text
.agents/skills/project-foundation/
```

The user may instead provide the skill from another path. Treat the directory containing the draft or existing project as the target root; do not mistake the skill's own directory for the project root.

## Execution Contract

Inspect first, preserve useful existing material, and produce or update these root artifacts:

| Artifact | Audience and purpose | Git treatment |
| --- | --- | --- |
| `AGENTS.md` | Agent-facing project entry point, navigation, user collaboration preferences, and durable development rules | Track |
| `README.md` | Concise, professional public project overview and reproducible usage entry point | Track |
| `PROJECT_ENVIRONMENT.md` | Concise Chinese device and project environment summary, maintained when material conditions change | Ignore |
| `CHANGELOG.md` | Chinese, user-facing timestamped summary of every logical project-content change, periodically consolidated by direction | Ignore |
| `PROJECT_SETUP_REPORT.md` | Detailed Chinese report of this skill run: actions, locations, Git state, verification, unresolved items, and next steps | Ignore |

Always establish local Git management. If no repository exists, initialize one without changing global Git configuration. If no remote URL is available, finish the safe local setup and record `待配置` for the repository address in both the environment summary and setup report. Never invent a remote or publish without user authorization.

Merge rather than overwrite. Preserve repository history, useful README content, user-authored instructions, and unrelated ignore rules. If an existing tracked public `CHANGELOG.md` conflicts with the required ignored local change summary, pause for the user to choose a compatible filename or policy instead of silently untracking public release history.

## Workflow

1. Identify the target root and classify it as a draft, new implementation, or existing project. Read the user's design and existing project-local instructions before changing anything.
2. Read `references/project-bootstrap.md`. Inspect only device, toolchain, project, and Git facts that affect this project.
3. Establish Git management and merge the required local-only entries into `.gitignore`. Preserve existing history and working state. Once the report path is ignored, create `PROJECT_SETUP_REPORT.md` with status `进行中` so partial execution still leaves a record.
4. Create or update `PROJECT_ENVIRONMENT.md` from `assets/project-environment-template.md` after Git setup so it records the resulting state in one pass. Keep it concise, Chinese, evidence-based, and project-relevant.
5. Read `references/project-rules.md`. Create or merge `AGENTS.md` from `assets/project-agents-template.md`, create or update `CHANGELOG.md` from `assets/project-changelog-template.md`, and create or improve the public `README.md`.
6. Verify real paths, commands, links, ignore behavior, repository state, and agreement among the generated documents.
7. Finalize `PROJECT_SETUP_REPORT.md` last using `assets/project-setup-report-template.md`. Record completed and blocked work even when the run is only partially successful. Keep the conversational response brief and point to the report.

Pause only when a missing choice or conflict could materially change architecture, security, user-authored content, public release history, or repository state. Otherwise make conservative project-specific decisions and record any remaining assumptions.

## Durable Handoff

At completion:

- `AGENTS.md` must tell future agents what to read and maintain without referring them back to this skill.
- `PROJECT_ENVIRONMENT.md` and `CHANGELOG.md` must begin with concise maintenance instructions for future agents.
- `README.md` must remain public-facing and must not mention or link the local environment summary, local change log, setup report, or private agent-user collaboration process.
- The initial `CHANGELOG.md` entry must record this foundation setup with a timestamp.
- The setup report must state whether the skill source can now be safely removed, while never deleting it unless the user explicitly requests deletion.

Ordinary future work reads the generated project files directly. Re-run this skill only to repair or deliberately rebuild the foundation after a major change.

## Evidence and Safety

- Distinguish observed facts, user-provided facts, inferences, plans, and unresolved assumptions.
- Never present tool availability, versions, test results, metrics, or completed work as verified without supporting output.
- Never record secret values. Documents may name required variables but must not contain credentials or private access details.
- Do not install software, change global configuration, replace a remote, commit unrelated existing work, publish, or push without appropriate user intent and authorization.
- Avoid generic inventories, speculative rules, unnecessary documents, and abstractions unsupported by the actual project.

## Resources

- Read `references/project-bootstrap.md` for target detection, environment inspection, Git setup, ignore behavior, and final verification.
- Read `references/project-rules.md` for the durable document roles, collaboration defaults, README boundary, and maintenance behavior.
- Adapt `assets/project-environment-template.md` into the target project's `PROJECT_ENVIRONMENT.md`.
- Adapt `assets/project-agents-template.md` into the target project's root `AGENTS.md`.
- Adapt `assets/project-changelog-template.md` into the target project's ignored `CHANGELOG.md`.
- Adapt `assets/project-setup-report-template.md` into the target project's ignored `PROJECT_SETUP_REPORT.md`.
