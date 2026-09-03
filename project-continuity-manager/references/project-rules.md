# Persistent Project Rules

Use this reference when generating or revising the project-local documents that must guide future development without requiring this skill.

## Root AGENTS.md

The root `AGENTS.md` is the durable AI operating agreement for the project. Keep it concise, concrete, and specific to the actual project.

Include relevant guidance about:

- Project objective, scope boundaries, and authoritative design documents.
- What files a new AI session should read first.
- Architecture boundaries, ownership, naming, and directory conventions.
- Current build, test, lint, formatting, and verification commands.
- Dependency and configuration rules that materially affect implementation.
- Documentation and handoff updates required after meaningful changes.
- User-authored content or design decisions that must be preserved.
- Safety, authorization, and external-action boundaries specific to the project.

Do not:

- copy this entire skill into `AGENTS.md`;
- tell future sessions to reread the bootstrap skill for ordinary tasks;
- include raw logs, temporary observations, or speculative rules;
- hard-code commands or paths that have not been verified;
- replace stronger existing project instructions without user intent.

## Root Project Overview

The root `README.md`, or an existing equivalent, should act as a reliable human-facing entry point rather than a running notebook.

Include the parts that are relevant:

- Project goal, intended users, and scope.
- Current stage and current entry points.
- Setup and usage guidance supported by the verified environment.
- Navigation to design, status, decision, and environment documents.
- Important limitations or compatibility constraints.

Put detailed implementation reasoning, long experiment analysis, and raw output in focused locations rather than the root overview.

## Current State and Decision History

- Use a separate status document only when active state is too detailed or volatile for the overview.
- Maintain a decision record only when its reasoning will matter to future work.
- Record what changed, why, important consequences, and unresolved questions.
- Prefer durable summaries over activity-by-activity narration.
- Update documents when the state they describe changes; avoid documentation churn for inconsequential edits.

## Ongoing Working Agreements

- Inspect relevant existing code, configuration, instructions, and user-authored material before editing.
- Keep changes within the requested scope and preserve established architecture unless the user changes it.
- Add abstractions and dependencies only when they solve a demonstrated need.
- Run the relevant verified checks after changes and report actual outcomes.
- Do not claim success, compatibility, metrics, or performance without supporting evidence.
- Update the overview, environment baseline, status, or decision record only when the change affects what those documents describe.
- Leave the project in a state that another person or AI session can understand from project-local files alone.

## Evidence and Reproducibility

- Separate plans, observed results, inferences, and unresolved assumptions.
- Important results should preserve enough context to reproduce them when applicable: inputs, configuration, execution method, environment, output location, and evaluation procedure.
- Keep concise summaries in project documentation and place bulky generated artifacts in storage appropriate to the project.
- Never place credentials, tokens, private keys, or private access details in general project documentation.
