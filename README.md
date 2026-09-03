# My Skills

这个仓库用于集中保存、管理和同步个人 Skills。每个 Skill 都位于独立目录中，完整说明以对应的 `SKILL.md` 为准。

## Skill 导航

| Skill | 简介 |
| --- | --- |
| [`project-continuity-manager`](./project-continuity-manager/SKILL.md) | 根据用户的项目设计建立可持续的项目治理体系。适用于为新项目或现有开发、研究项目检查运行环境、生成可见的 `PROJECT_ENVIRONMENT.md`、初始化管理文档，并将长期协作规则写入项目级 `AGENTS.md`。当项目规则已经稳定后，不用于普通的日常开发任务，除非需要重新初始化或重组治理体系。 |

## 使用方式

打开上表中的 Skill 入口，按照其 `SKILL.md` 中的适用场景、工作流程和资源说明使用。将 Skill 安装到具体项目时，请同时保留其目录结构以及 `agents`、`assets`、`references`、`scripts` 等配套资源。

## 目录约定

- Skill 目录名与 `SKILL.md` 中的 `name` 保持一致。
- 每个 Skill 的简介以 `SKILL.md` 中的 `description` 为来源，并在本页提供中文概述。
- 仓库内文件均纳入 Git 管理，不使用 `.gitignore` 排除 Skill 内容。
