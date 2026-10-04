# Personal OS

**一个 AI-native personal execution system：AI 降低摩擦，用户保留自主性。**

[English](README.md) · **v0.1.0，实验阶段** · [MIT 许可证](LICENSE)

把“决定做”变成具体结果，并给明天留下一个可以直接开始的动作。Personal OS 由一个 AI 工作会话和三个持久记录组成：**Projects、Daily、Inbox**。

仓库提供 Prompt、工作流程、Notion 参考结构和虚构示例。这是一套可使用的协作协议，无需安装应用，没有后台服务或自动同步。

~~~text
昨天
 ↓
Tomorrow First Move（明天第一动作）
 ↓
Boot（开机）
 ↓
1 个 Main Outcome（主线成果）
 ↓
Execution（执行）── 新想法 ──→ Inbox
 ↓
Project → Next Action（项目下一动作）
 ↓
Shutdown（关机）
 ↓
Daily Closed（当天已收尾）
 ↓
明天
~~~

## 各部分负责什么

| 部分 | 用途 |
| --- | --- |
| AI 工作会话 | 判断优先级、降低启动门槛、解决卡点、指出有证据的逃避、核对结果。 |
| Projects | 保存真正推进的项目、当前阶段和明确的下一动作。 |
| Daily | 保存主线成果、实际产出、摩擦和明天第一动作。 |
| Inbox | 收下想法和问题，避免它们立即打断当前工作。 |

Boot 承接昨天；Execution 推进 **1 个主线成果**，按需保留 1～2 个小维持项；Shutdown 写清今天发生了什么、明天先做什么。每天都重新规划方向，会消耗本应用于行动的精力。

AI 可以整理信息、处理重复事务和执行明确需求。用户需要保留重要选择、观察、学习、表达、产品判断和验收能力。学习是目标时，AI 应让用户做一次小尝试或解释，再帮助纠正。

## Quick Start：目标约 15 分钟

15 分钟是设计目标，还没有通过陌生用户测试；注册账号、授权连接和组织权限限制可能需要更多时间。

1. **建立自己的私有记录，约 6 分钟。** 按[Notion 搭建教程](notion/setup.md)在一个私有页面下创建 Projects、Daily、Inbox。v0.1.0 暂未附已验证的公开复制链接；手动教程完整可用。
2. **连接 Notion，约 2 分钟。** 在 AI 客户端启用可用的 Notion 应用、插件或连接器，授权自己的副本。让 AI 验证能否读取和写入；连接成功不等于有写入权限。暂时无法连接时，采用教程中的手动交接，继续开始工作。
3. **复制 Prompt，约 1 分钟。** 可先用[精简版](prompts/minimal.md)，也可用[完整版](prompts/personal-os.md)，粘贴到一个专门的 AI 工作会话。
4. **填写私有 User Profile，约 3 分钟。** 将[空白资料模板](prompts/user-profile.md)复制到公开仓库之外，或被忽略的本地目录。只填会影响今天判断的信息，再交给工作会话。
5. **开始第一次 Boot，约 3 分钟。** 新建一个项目，写清 Next Action。告诉 AI 精力、必须面对的现实事务和希望留下的成果，让它读取记录并给出第一动作。

**开始的标准是：一个现实动作已经启动。** 不必先填完所有字段。

## 每天怎么用

- **开始：**“Boot，读取最近 Daily 和正在推进的项目。”当天已开始，就承接当前动作。
- **执行：**“我准备做 X。”确定结果、验收标准、第一动作，然后开始。
- **卡住：**“我做了 X，预期 Y，实际 Z。”先解决真实卡点。
- **想法：**“Inbox：……”收下后回到主线，除非确实必须现在处理。
- **收尾：**“Shutdown。”AI 根据已有证据起草记录，用户纠正，再保存并核对。

结果可以写在会话里，或写在 Daily 正文的「个人记录 / Personal Notes」里，**同一内容只记一处**。下次开始工作时，AI 应先读记录，不要求重复汇报。修改 Notion 或勾 Closed 本身不会自动唤醒会话。

**Closed 表示整天已经收尾。** 完成单项任务时不要勾它。你可以自己完成 Shutdown：填实际产出、摩擦、明天第一动作，更新项目 Next Action，最后勾 Closed。

## 不使用 Notion 也能开始

核心只需要 Projects、Daily、Inbox 三个持久状态。先用一个私有文档的三个区块，也能完成手动运行。

Notion 是当前参考实现。以后可由 Obsidian、Markdown、SQLite、Apple Notes 或其他数据库承载；v0.1.0 没有这些适配器。手动方式下，将相关状态粘贴给 AI，再把返回的更新保存到自己的记录。

## 继续阅读

- [一个完整的虚构工作日](examples/example-day.md)
- [一个具体项目及下一动作](examples/example-project.md)
- [Boot](workflows/boot.md)、[Execution](workflows/execution.md)、[Inbox](workflows/idea-inbox.md)、[Shutdown](workflows/shutdown.md)
- [核心观点](principles/philosophy.md)
- [隐私与发布](PRIVACY.md)

## 当前边界

这是实验性工作流，不承诺提高生产力，不提供心理治疗或健康管理。AI 可能误判优先级、编造进展或漏掉缺陷，需要用户用真实结果验收。

记录必须可访问才能承接。工具、账号套餐和权限不同；Prompt 不会授予访问权限、启动后台任务，也不能保证另一个会话记得你的上下文。

## 仓库结构

~~~text
personal-os/
├── README.md / README.zh-CN.md
├── LICENSE / VERSION / CHANGELOG.md
├── PRIVACY.md / CONTRIBUTING.md / .gitignore
├── prompts/       核心协议、精简协议、空白个人资料
├── notion/        搭建教程、三库字段、空白 Daily 正文
├── workflows/     开机、执行、想法收集、关机
├── principles/    核心观点
└── examples/      虚构工作日和项目
~~~

下一版最值得做的是观察几位陌生用户从零搭建，修正阻碍第一次行动的步骤。参与方式见[贡献说明](CONTRIBUTING.md)。
