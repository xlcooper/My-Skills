---
name: conversation-daily-log
description: "用户在一天结束后选定对话并主动要求归档或预览日志时使用。把进展去重后合并到 Notion 的同日日记，有实质科研内容时按阶段参考 Supervisor-Skills 给出简短建议。"
---

# 对话进展归档到每日日志

## 使用时机与范围

工作或学习结束后，由用户选择想记录的对话并主动调用。默认处理当前对话。也可处理用户明确指定且能够读取的其他对话或选段。只从选定内容提取进展。用户要求归档时写入日记，要求预览时返回草稿。

默认归档日期为北京时间（Asia/Shanghai）的当天，用户指定日期优先。按事件实际发生日期筛选。归属不明且会实质影响记录时简短询问。只保留值得回顾的行动、结果、决策和问题，区分已完成工作、计划、假设和建议。可附真实对话链接、时间或设备，依据不足时省略。不可读取的对话不计入已整理范围。

## 创建或更新日记

1. 保存时用当前连接的 Notion 工作区定位「日历」数据库。用户明确指定目标时使用该目标。读取其最新结构，核对标题、日期和标签属性（现有命名为「名称」「日期」「标签」）。如有同名库，按结构与已有日记核对。仍不能唯一确定时询问目标。预览直接根据选定对话生成草稿。用户明确要求预览与已有日记的合并结果时，可只读查看目标页。
2. 按目标日期查询，定位标签为「日志」、名称以「日记｜」开头的当日日记。已有页先读全文。相同主题、事实和来源去重，新增事实补入对应事件，得到确认的新结论修订原描述。其他来源的有效内容和链接保留。若当天没有日记才创建，并填写实际日期与「日志」标签。有多个候选且无法判断时先确认基准页。
3. 日记用「概述」「主要事件」「总结与复盘」三个二级标题，事件用三级标题。合并后的概述和复盘覆盖全篇，通常各不超过 200 字。先写做了什么、进展和结果。来源、时间或设备可用灰色引用块。普通事务简短收尾，科研建议按下节处理。
4. 优先定向编辑。回读确认日期、内容与重复情况，回复新增或修订的事件和日记链接。内容已一致时直接返回原日记。无法读取指定来源或无法写入时说明实际范围和原因，能提取的内容以可复制草稿交付。

## 专家复盘

选定对话包含明确的科研问题、实质进展或可评估的决策时，选最贴合当前阶段的一项 [Supervisor-Skills](https://github.com/HKUSTDial/Supervisor-Skills) 方法。优先读取本地对应技能，其次读取表中链接的上游 SKILL.md。若均不可用，依据可见材料做简要复盘，并说明建议的依据。仅在整理历史资料或普通事务时，可以简短总结实际进展。

| 适用场景 | 参考方法 | 建议聚焦 |
| --- | --- | --- |
| 选题与构思 | [idea-evaluator](https://github.com/HKUSTDial/Supervisor-Skills/blob/main/skills/idea-evaluator/SKILL.md) | 找出关键假设和最小验证 |
| 文献调研 | [deep-research](https://github.com/HKUSTDial/Supervisor-Skills/blob/main/skills/deep-research/SKILL.md) | 比较最相关工作的机制、证据和适用条件 |
| 方法设计 | [tech-paper-template](https://github.com/HKUSTDial/Supervisor-Skills/blob/main/skills/tech-paper-template/SKILL.md) | 检查问题、机制和贡献是否连贯 |
| 实验设计与评估 | [benchmark-paper-template](https://github.com/HKUSTDial/Supervisor-Skills/blob/main/skills/benchmark-paper-template/SKILL.md) | 检查对照、指标和收益归因，按探索规模取舍 |
| 论文草稿 | [pre-submission-reviewer](https://github.com/HKUSTDial/Supervisor-Skills/blob/main/skills/pre-submission-reviewer/SKILL.md) | 找出最影响主张的一处证据或表达问题 |

在「总结与复盘」中用 2–4 句说明已有证据支持什么、最值得推进的一步，并标注参考方法。假设和建议按其实际状态表述。有新证据时修订原判断。本次归档调用的产出是日记中的简短建议，完整审稿、扩展调研或额外产出由用户另行发起。

需要增加专家时，在表中追加适用场景、参考方法和建议重点。所有专家复盘共用同一篇日记。
