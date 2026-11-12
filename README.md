# My Skills

这个仓库用于集中保存、管理和同步个人 Skills。每个 Skill 都位于独立目录中，完整说明以对应的 `SKILL.md` 为准。

## Skill 导航

| Skill | 简介 |
| --- | --- |
| [`project-foundation`](./project-foundation/SKILL.md) | 为项目草案、新项目或已有项目建立可持续的个性化开发基础：检查设备与项目环境、配置本地 Git、创建或优化公共 `README.md`、建立根目录 `AGENTS.md`，并留下可动态维护的中文环境摘要、变更摘要和执行报告。基础建立后，日常开发无需再次依赖该 Skill。 |
| [`conversation-daily-log`](./conversation-daily-log/SKILL.md) | 手动归档选定对话，去重后创建或更新 Notion 当日日记。科研内容按阶段参考 Supervisor-Skills，给出简短复盘建议。 |

## 使用方式

1. **选择技能。** 从导航打开对应的 `SKILL.md`，了解它的适用场景、调用方式和依赖。
2. **按使用范围安装。** 跨项目自用时，安装到客户端的个人技能目录。需要随项目共享时，按客户端支持的方式放入项目。安装所选技能的整个目录，保留其中已有的配套资源。
3. **在对应场景调用。** 例如，在想记录的对话中调用 `$conversation-daily-log`，保存时使用 Notion 连接。初始化或整理项目时，在目标项目中调用 `project-foundation`，后续开发按该项目生成的说明开展。

## 目录约定

- Skill 目录名与 `SKILL.md` 中的 `name` 保持一致。
- 每个 Skill 的简介以 `SKILL.md` 中的 `description` 为来源，并在本页提供中文概述。
- 在本仓库维护 `SKILL.md` 及配套资源。其他客户端按需从这里安装或更新各自使用的技能目录。
