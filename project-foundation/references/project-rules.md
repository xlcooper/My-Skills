# Durable Project Documents

Use this reference when creating or merging the project-local files that remain after the foundation skill is no longer needed.

## Root AGENTS.md

`AGENTS.md` is the fixed entry point for future agents. Keep it concise, specific to the project, and maintainable when the user adds or changes a lasting instruction.

Include:

- a short project objective and scope boundary;
- a reading-order navigation map to real project files;
- verified architecture, directory, naming, dependency, and configuration rules that materially affect work;
- verified build, test, lint, format, run, and other validation commands;
- documentation duties for the local environment summary and change log;
- project-specific security, authorization, and external-action boundaries;
- the user's durable collaboration preferences below.

Default collaboration preferences to preserve unless the user overrides them:

- Communicate with the user in Chinese by default.
- Lead with the result, then provide concise supporting evidence, verification, blockers, and next steps.
- Proceed autonomously on a clear, scoped request; ask only when a missing choice could materially change the result or exceed authorization.
- Distinguish observed facts, user decisions, inferences, and unresolved assumptions.
- Prefer the smallest sufficient solution; avoid redundant documents, speculative abstractions, and unrequested expansion.
- Do not use a chat response as a substitute for a requested project artifact.

Do not copy the entire skill into `AGENTS.md`, include transient command output, invent commands or paths, or require future sessions to reread the skill.

## Local Dynamic Documents

`PROJECT_ENVIRONMENT.md` and `CHANGELOG.md` are ignored local documents for the user and future agents. Each must begin with an HTML-comment maintenance contract so the rendered document stays readable while its update rules remain discoverable.

### PROJECT_ENVIRONMENT.md

- Write in Chinese and keep it short enough to scan.
- Summarize device capacity only where it affects the project.
- Record verified project toolchain, configuration, Git state, remote URL or `待配置`, missing items, conflicts, and relevant unknowns.
- Update after a material change to hardware constraints, runtime, toolchain, platform, repository configuration, or project requirements.
- Replace stale facts rather than appending an activity history.

### CHANGELOG.md

- Write in Chinese for the user.
- Add one reverse-chronological timestamped entry for every completed logical project-content change. Summarize a multi-file change once rather than logging each file operation.
- Record the change direction, outcome, affected area, and actual verification. Avoid raw diffs and conversational narration.
- Maintain a small direction overview. When many entries belong to one larger direction, consolidate their durable outcome under that direction and retain only meaningful milestones in the detailed timeline.
- Preserve important decisions and regressions while pruning repetitive implementation noise.

### PROJECT_SETUP_REPORT.md

This is a temporary, ignored, detailed record of the foundation run, not an ongoing project log. Create it with status `进行中` after Git ignore setup, finalize it last, and replace it on a later re-run rather than accumulating multiple reports by default.

It must state:

- target root, starting mode, time, and overall result;
- every required artifact, its path, whether it was created, updated, preserved, skipped, or blocked, and whether Git tracks or ignores it;
- relevant environment readiness and unresolved compatibility issues;
- Git initialization, branch, remote, ignore, commit, and push state;
- checks actually run and their outcomes;
- unresolved decisions, assumptions, and concrete next steps;
- whether future work is self-contained and the copied skill source can be removed.

## Public README.md

`README.md` is for all potential readers, not just the user or developers. Create it when missing and improve it conservatively when present.

Use the project's established public language; for a new project with no language choice, default to Chinese. Include only relevant sections such as:

- project name and concise purpose;
- key capabilities or current scope;
- visual result or example when the project has one;
- prerequisites, installation, reproduction, viewing, or usage steps that are real and verified;
- public project structure or documentation navigation when useful;
- limitations, contribution, or license information only when known and appropriate.

Keep it professional, concise, and similar to a well-maintained open-source project README. Do not mention or link `PROJECT_ENVIRONMENT.md`, the local `CHANGELOG.md`, `PROJECT_SETUP_REPORT.md`, private device details, agent-user conversation rules, internal handoff notes, or the bootstrap process. Do not invent badges, compatibility claims, benchmarks, licenses, setup commands, or completed features.

## Ongoing Development Rules

- Inspect relevant code, configuration, instructions, and user-authored material before editing.
- Preserve established behavior and architecture unless the requested change requires otherwise.
- Add dependencies and abstractions only for a demonstrated need.
- Keep secrets out of source, documentation, logs, and command output.
- Run the relevant verified checks after changes and report actual outcomes.
- Update `CHANGELOG.md` after each logical content change and `PROJECT_ENVIRONMENT.md` only when its facts materially change.
- Update `README.md` only when public scope, setup, usage, results, or navigation changes.
- Leave the project understandable from its project-local files without relying on the foundation skill or prior conversation.
