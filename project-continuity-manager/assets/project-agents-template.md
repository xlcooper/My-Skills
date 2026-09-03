# Project Working Agreements

Adapt this template into the project root `AGENTS.md`. Replace general guidance with verified project-specific rules, merge existing instructions, and remove sections that do not apply.

## Project Intent

- State the project objective and scope boundaries.
- Name the authoritative design and requirement documents.
- Record important user decisions that future work must preserve.

## Start of Every Task

- Read the root overview and the project-local files relevant to the task.
- Inspect existing implementation, configuration, and instructions before editing.
- Check the current environment baseline when the task depends on toolchain or platform assumptions.
- Surface material ambiguity instead of silently changing the design.

## Architecture and Implementation

- Record the project's actual architecture, ownership, naming, and directory conventions.
- Keep changes within the requested scope.
- Preserve user-authored notes and established behavior unless the requested change requires otherwise.
- Add dependencies or abstractions only when they solve a demonstrated need and follow the project's approval rules.

## Verification

- Record the project's verified build, test, lint, formatting, and other validation commands.
- Run checks relevant to the change and report their actual outcomes.
- Do not claim success, compatibility, performance, or completed results without supporting evidence.

## Documentation and Continuity

- Keep the root overview aligned with current scope, entry points, and navigation.
- Update the environment baseline only after a material environment change.
- Update status or decision records when meaningful state or reasoning changes.
- Keep plans, observed results, inferences, and unresolved assumptions distinguishable.

## Completion and Handoff

- Summarize what changed and what was verified.
- Record unresolved blockers, assumptions, and the next reasonable step in the appropriate project file when they must survive the current conversation.
- Ensure future work can continue from project-local files without rereading the bootstrap skill.
