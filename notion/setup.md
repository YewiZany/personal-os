# Set up the Notion reference implementation

[中文快速搭建](#中文快速搭建) · [Projects schema](projects.md) · [Daily schema](daily.md) · [Inbox schema](inbox.md)

Use one **private** top-level page named Personal OS and three databases inside it. There is no required public template URL. Do not publish the page where you operate your actual life.

## 1. Duplicate the template (recommended)

Open the [Personal OS reference template](https://even-cart-00d.notion.site/Personal-OS-Template-v0-1-0-3efb90dbc5af818ebb51c759cbb01750) and select **Duplicate** in the upper right: the icon looks like two overlapping squares. If asked, sign into Notion, then choose your workspace. All three databases, their properties, fictional records, Minimal Prompt and a blank User Profile are included. No repository download or server deployment is required.

Keep your copy private. Open Projects, Daily and Inbox; check that Daily's Main Project and Inbox's Related Project point to Projects inside your copy. If a database shows “No access,” or a relation points outside your copy, use the schema below to repair it before entering personal data. The public page and Duplicate entry have been checked without signing in; duplicating into a second workspace has not been tested.

Continue at [Add only enough state to start](#2-add-only-enough-state-to-start). If the template is unavailable or you prefer building your own structure, follow the manual route below. Notion documents duplication in [Duplicate public pages](https://www.notion.com/help/duplicate-public-pages).

### Manual fallback: create three databases

Create a full-page table database under the private page for each of Projects, Daily and Inbox. Rename each default title property first, then add the properties below. Keep these exact names so the prompt and records agree.

### Projects

| Property | Notion type | Setup |
| --- | --- | --- |
| Project | Title | Rename the default title property. |
| Status | Select | Active, Slow, Paused, Done |
| Area | Select | Product, Language, Technology, Study, Creative, Life, System |
| Current Stage | Text | Current reality in one sentence. |
| Next Action | Text | First concrete action on reopening. |
| Deadline | Date | Optional; leave empty when none. |
| Last Updated | Last edited time | Automatic; do not type a value. |

Create Projects before the other databases so their relations can target it.

### Daily

| Property | Notion type | Setup |
| --- | --- | --- |
| Day | Title | A date label such as YYYY-MM-DD. |
| Date | Date | The user's local calendar date. |
| Energy | Select | Low, Normal, High; subjective, optional. |
| Main Project | Relation | Target this copy's Projects database. |
| Main Outcome | Text | One observable result for today. |
| Actual Output | Text | What actually changed; preserve evidence. |
| Friction | Text | The obstacle that affected the work. |
| Tomorrow First Move | Text | One directly executable action. |
| Closed | Checkbox | Unchecked until daily handoff is complete. |

For Main Project, select the newly created Projects database in **your own copy**. You may limit the relation to one page. A reciprocal relation is optional; the protocol does not need one.

Paste [the blank Daily body](daily-entry.md) into a new day. Keep Personal Notes in the body, not in an extra completion property. Optionally save that body as a Notion database template after your first run.

### Inbox

| Property | Notion type | Setup |
| --- | --- | --- |
| Item | Title | One compressed idea, task or question. |
| Type | Select | Idea, Task, Question, Explore, Later |
| Status | Select | New, Converted, Archived |
| Related Project | Relation | Target this copy's Projects database; optional per item. |
| Created | Created time | Automatic. |

Converted means the item became a concrete project action. Archived means you deliberately set it aside. These select labels do not delete the page.

## 2. Add only enough state to start

Add one real project. For example, replace a fictional “Portfolio Website” with your own project, choose Active, and write a next action such as “Open the current homepage on a phone and record its first broken layout.”

Create today's Daily using your local date, relate it to that project, and leave Closed unchecked. No historic diary, scoring system or perfect profile is required.

Optional table views: Projects filtered to Active and Slow; Daily sorted by Date descending; Inbox filtered to New. They are conveniences, not startup requirements.

## 3. Connect your AI work conversation

Use the Notion integration supported by your AI client. In a client with an app or plugin catalog, select Notion, complete its normal authorization flow, and make your private copy accessible within the available permission controls.

For ChatGPT or Codex, use the available Notion app/plugin and follow its connection prompts. Availability and tools depend on the client, workspace and account. [Official plugin guidance](https://learn.chatgpt.com/docs/plugins) explains the connection model. v0.1 requires no manually created API token or backend.

Ask:

> Read my Personal OS page and confirm the names and Next Action of my projects. Then tell me whether you can create and update records in these three databases.

Read access is not write access. If write tools are available, ask the AI to create today's intended Daily record and check in Notion that it appeared. If it cannot read or write, proceed in manual mode:

1. Paste the relevant Projects, latest Daily and current Inbox items.
2. Run Boot and start the action.
3. Copy the AI's clearly labeled record updates into Notion yourself.

Do not mistake “I will save this” for a completed write. Neither this prompt nor a Notion edit enables background monitoring.

## 4. Add prompt and private profile

Use [Minimal](../prompts/minimal.md) or [Core](../prompts/personal-os.md), plus a private copy of [User Profile](../prompts/user-profile.md). Blank fields are fine.

Then say:

> Boot. My energy is normal. Today I must handle ___. I want ___ to exist by the end of the day. Read my state and give me the first action.

Stop configuring once that action is clear.

## 中文快速搭建

1. 打开[公开模板](https://even-cart-00d.notion.site/Personal-OS-Template-v0-1-0-3efb90dbc5af818ebb51c759cbb01750)，点击右上角两个重叠方框的 Duplicate / 复制按钮，登录后选择自己的工作区。三库、字段和虚构示例会一并复制。
2. 保持自己的副本私有，检查 Daily 的 Main Project、Inbox 的 Related Project 关联**副本里的 Projects**，三库都能打开。
3. Projects 先只放一个真实项目，写明确的 Next Action；Daily 新建今天，Closed 保持未勾选。正文粘贴[个人记录模板](daily-entry.md)。
4. 在 AI 客户端连接自己的 Notion，验证能读、能写。不能连接就粘贴相关记录，手动保存返回的更新。
5. 从模板下方或仓库复制 Prompt，填写私有 User Profile，开始 Boot。开始第一动作后，停止装修系统。

如果模板打不开：新建私有 Personal OS 页面，按上方三张字段表建立 Projects、Daily、Inbox。Title 是标题，Text 是文本，Select 是单选，Relation 是关联；Last edited time 和 Created time 是自动字段。先建 Projects，再配置其余两库的关联。

当天完成单项任务，在个人记录里写结果。整天结束时填 Actual Output、Friction、Tomorrow First Move，更新项目 Next Action，再勾 Closed。日内记录一次即可，不需要同时抄到会话。
