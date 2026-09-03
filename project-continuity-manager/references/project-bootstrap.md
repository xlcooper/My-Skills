# Project Bootstrap Reference

Use this reference only when initializing a new project or explicitly rebuilding its governance layer.

## 1. Capture the Project Design

Before deciding structure or tooling, extract the durable parts of the user's design:

- Objective, intended users, and success criteria.
- Scope and explicit non-goals.
- Functional and quality requirements.
- Preferred architecture, technologies, and delivery target.
- Important constraints, risks, and decisions still open.

Separate user decisions from AI suggestions. Do not silently convert a preference or example into a permanent requirement.

## 2. Inspect the Relevant Environment

Inspect only facts that could affect the proposed project. Typical categories include:

- Operating system, architecture, and active shell.
- Required language runtimes, SDKs, compilers, and their versions.
- Dependency managers, manifests, and lockfiles.
- Build, test, lint, formatting, database, container, or service tooling required by the design.
- Existing project configuration and runnable entry points.
- Version-control tool availability and whether the project is already a repository.
- Required environment-variable names from safe examples or documentation, never their secret values.
- Material permission, storage, network, or platform constraints.

Do not produce a generic machine inventory. Omit unrelated tools and transient process details. Prefer concise checks that answer whether the proposed design can start reliably.

Classify findings as:

- **Ready:** verified and compatible with the design.
- **Missing:** required but not available or not configured.
- **Conflict:** detected state contradicts the design or another source of truth.
- **Unknown:** relevant but not safely verifiable yet.

## 3. Produce the Visible Environment Summary

Before substantive implementation, create or update `PROJECT_ENVIRONMENT.md` using the bundled template and summarize it in the conversation.

The document must:

- be readable without inspecting command output;
- record the project path and inspection date;
- compare detected state with design requirements;
- surface missing tools, incompatibilities, and unresolved choices;
- state which files or commands support important findings;
- exclude credentials, tokens, private access details, and irrelevant machine data.

If a finding could materially change architecture, dependency choices, cost, security, or deliverability, pause for user direction after presenting the summary. Otherwise, continue with the agreed project design after making the summary visible.

Update this document only after a material toolchain, runtime, platform, or project requirement change. It is a baseline, not a per-task activity log.

## 4. Initialize Local Version Control

For a new development project, include local Git initialization in the bootstrap unless the user declines, another version-control system is already in use, or project context makes it inappropriate.

1. Verify that Git is available and record its status in `PROJECT_ENVIRONMENT.md`.
2. If a repository already exists, preserve its history, configuration, branches, and working state.
3. If no repository exists and local Git is appropriate, initialize it after the environment summary is visible.
4. Create or adapt `.gitignore` from the actual technology choices. Exclude secrets, local environments, caches, generated output, and large runtime artifacts as appropriate.
5. Do not configure a remote, publish, push, rewrite history, or change global Git configuration without explicit user instruction.
6. Create an initial commit only when the user requested a fully initialized repository or the project-specific rules explicitly require it.

Git is a bootstrap concern here, not a mandatory commit or publishing cadence for every future task.

## 5. Persist the Project Rules

Create or merge the root `AGENTS.md` so future AI sessions receive the lasting rules without depending on this skill. It should point to the project's own sources of truth and contain only project-relevant instructions.

Establish the smallest useful document set:

- `AGENTS.md`: authoritative AI working agreements and project-specific constraints.
- `README.md` or equivalent: human-facing project purpose, current entry points, and navigation.
- `PROJECT_ENVIRONMENT.md`: verified startup environment baseline.
- Optional current-status record when active state does not fit the overview.
- Optional decision record when important reasoning must survive handoff.

Merge rather than overwrite existing guidance. Resolve contradictions explicitly and preserve user-authored instructions unless the user changes them.

## 6. Transition to Development

Before beginning implementation, confirm that:

- the user has seen the environment summary;
- material blockers or design conflicts are resolved;
- persistent instructions reference real files and commands;
- the root overview and AI instructions agree about project scope and entry points;
- unverified assumptions are visibly labeled.

After this transition, future work should read and follow the root `AGENTS.md` and project documents directly. The bootstrap skill is no longer part of the normal per-task reading sequence.
