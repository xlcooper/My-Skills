# Project Foundation Execution

Read this reference whenever the skill is executed. Apply the same outcome to a project draft, a new implementation, or an existing project, while preserving useful existing state.

## 1. Identify the Target and Mode

Resolve the project root before editing. The root is the directory containing the user's draft, existing implementation, or intended new project, not the skill directory merely placed inside it.

Classify the starting point:

- **Draft:** requirements, notes, or designs exist, but implementation is absent or minimal.
- **New project:** the target is empty or contains only initial scaffolding.
- **Existing project:** source, manifests, history, or established documentation already exists.

Read root and applicable nested instructions, the project draft, existing README, manifests, lockfiles, configuration, entry points, and current Git state. On an existing project, merge changes narrowly; do not reorganize code or rewrite documentation that already serves its intended audience.

## 2. Capture Project Intent

Extract only durable information that future work needs:

- objective, intended users, and success criteria;
- current scope and explicit non-goals;
- functional and quality requirements;
- architecture or technology decisions already made;
- delivery target, constraints, risks, and unresolved decisions.

Separate user decisions, observed facts, inferences, and suggestions. Do not convert examples or tentative ideas into permanent requirements.

## 3. Inspect the Relevant Device and Environment

Start with read-only checks. Inspect enough to judge whether the current device and toolchain fit this project, without producing a generic machine inventory.

Include, when relevant:

- operating system, architecture, and active shell;
- CPU model or class and logical core count;
- total and currently available memory;
- relevant disk location and available capacity;
- GPU or accelerator only when the workload may use it;
- required runtimes, SDKs, compilers, package managers, and their versions;
- manifests, lockfiles, build, test, lint, formatting, database, container, or service tooling;
- required environment-variable names from safe examples or documentation, never secret values;
- permissions, network, storage, or platform constraints that could affect delivery.

Relate detected hardware and tools to the actual workload. Record a concise implication such as suitable, constrained, missing, conflicting, or not yet verified. Avoid raw command dumps and unrelated installed software.

Classify important findings as:

- **Ready:** verified and compatible.
- **Missing:** required but unavailable or unconfigured.
- **Conflict:** detected state contradicts a requirement or source of truth.
- **Unknown:** relevant but not safely verifiable yet.

Keep these findings available for the final environment summary, but write that document after local Git setup so its repository section reflects the resulting state without a required second pass.

## 4. Establish Git Management

Every target project must leave the run under local Git management.

1. Verify Git availability and determine whether the target is already inside a repository or worktree. Avoid creating an accidental nested repository.
2. If a repository exists, preserve history, branches, remotes, index state, worktrees, and unrelated user changes.
3. If none exists, initialize a local repository with `main` as the initial branch when supported. Do not alter global Git configuration.
4. Create or merge `.gitignore` from actual project needs. Preserve existing rules and add these root-local artifacts:

   ```gitignore
   /PROJECT_ENVIRONMENT.md
   /CHANGELOG.md
   /PROJECT_SETUP_REPORT.md
   ```

5. Verify the three files are actually ignored. If one is already tracked, preserve its working copy and remove it from the index only when doing so matches the user's requested local-only policy. If a tracked `CHANGELOG.md` is established public release history, pause rather than repurposing or untracking it silently.
6. Inspect existing remotes. If the user supplied a repository URL and no suitable remote exists, configure it locally. If an existing remote conflicts, pause before replacing it.
7. If no URL is available, plan to write `仓库地址：待配置` in `PROJECT_ENVIRONMENT.md` and `PROJECT_SETUP_REPORT.md`.
8. After the report path is confirmed ignored, create `PROJECT_SETUP_REPORT.md` from its template with execution result `进行中` and fill the known target and Git state. Update it as material stages complete so an interrupted run still leaves a useful record.
9. Do not invent Git identity, alter global configuration, stage or commit unrelated existing work, rewrite history, publish, or push without appropriate user intent.

Record the repository root, active branch, remote state, ignore verification, working-tree state, and any uncommitted or unpublished work in the final report.

## 5. Write the Environment Summary

Create or update the ignored root `PROJECT_ENVIRONMENT.md` in Chinese using the bundled template. It must describe the Git state produced by the previous step as well as the relevant device and toolchain findings. Refresh it later only after a material device, runtime, toolchain, platform, repository, or project-requirement change.

## 6. Create the Durable Project Files

Read `references/project-rules.md`, then create or merge:

- `AGENTS.md` from the agent template;
- `README.md` as a public project entry point;
- `CHANGELOG.md` from the change-log template.

For existing files, preserve correct project-specific content and stronger user-authored instructions. Add only what is missing or stale. The initial or refreshed `CHANGELOG.md` entry must record the foundation work as one logical change with a local timestamp.

## 7. Verify and Report

Before completion, verify:

- every reported path exists;
- `AGENTS.md` and `README.md` are intended for tracking;
- the three local artifacts are ignored;
- README setup and usage commands are real or clearly marked unverified;
- document links and named project entry points resolve;
- `AGENTS.md` contains enough project-local guidance for future work without this skill;
- no generated document contains secrets or raw sensitive output;
- Git status, branch, and remote claims match actual output.

Finalize `PROJECT_SETUP_REPORT.md` last from its template. It must be the detailed record of the run and include created, updated, preserved, skipped, blocked, and pending items. If execution is incomplete, set the result to `部分完成` or `阻塞` and record the last verified state rather than claiming success. The conversational response should give only the short conclusion and the report path.

Do not delete the skill source automatically. State in the report whether the generated foundation is self-contained and the copied skill can be removed safely.
