# Personal OS

**An AI-native personal execution system. AI reduces friction, not agency.**

[简体中文](README.zh-CN.md) · **v0.1.1 — experimental** · [MIT License](LICENSE)

Turn an intention into a concrete result, then leave a clear first move for tomorrow. Personal OS combines an AI work conversation with three persistent records: **Projects, Daily and Inbox**.

This repository provides prompts, workflows, a Notion reference structure and fictional examples. It is a working protocol, not an application. It has no backend, installation process or automatic synchronization.

~~~text
Yesterday
   ↓
Tomorrow First Move
   ↓
Boot
   ↓
1 Main Outcome
   ↓
Execution ── new ideas ──→ Inbox
   ↓
Project → Next Action
   ↓
Shutdown
   ↓
Daily Closed
   ↓
Tomorrow
~~~

## How it works

| Part | Purpose |
| --- | --- |
| AI work conversation | Helps decide, start, troubleshoot, challenge avoidance and review evidence. |
| Projects | Keeps each real project's stage and the next concrete action. |
| Daily | Records the day's main outcome, actual results, friction and tomorrow's first move. |
| Inbox | Holds ideas and questions without turning them into immediate commitments. |

Boot carries yesterday forward. Execution pursues **one main outcome**, with one or two small maintenance items when appropriate. Shutdown records what changed and prepares tomorrow. A new day should not require a new life plan.

AI can organize information and handle repetitive execution. The user keeps responsibility for choices, observation, learning, product judgment and judging the result. When learning is the goal, the AI should ask for a small attempt or explanation, then help improve it.

## Quick Start — aim for about 15 minutes

This is an onboarding target, not a measured promise. Account creation, connector approval or workplace restrictions can take longer.

1. **Duplicate the template, about 2 minutes.** Open the [Personal OS Notion template](https://even-cart-00d.notion.site/Personal-OS-Template-v0-1-0-3efb90dbc5af818ebb51c759cbb01750), select **Duplicate** in the upper right (the overlapping-squares icon), sign into Notion, and choose your workspace. Projects, Daily, Inbox and the fictional examples copy together; you do not need to create each property. Keep your copy private and check that both relation properties target Projects in your copy. If the template is unavailable, use [manual setup](notion/setup.md).
2. **Connect Notion, about 2 minutes.** Enable an available Notion app, plugin or connector in your AI client and authorize your copy. Ask it to verify read and write access. A connection may be read-only. If unavailable, use the manual handoff described in setup; do not spend the session debugging integration.
3. **Copy a prompt, about 1 minute.** Start with [Minimal](prompts/minimal.md), or use the [Core Prompt](prompts/personal-os.md). Paste it into a dedicated AI work conversation.
4. **Fill your private profile, about 3 minutes.** Copy [User Profile](prompts/user-profile.md) outside the public repository or into an ignored local folder. Fill only what changes today's decisions. Give the profile to your work conversation.
5. **Run your first Boot, about 3 minutes.** Add one project with a concrete Next Action. Tell the AI your energy, unavoidable obligations and desired result. Ask it to read your records, choose one Main Outcome and give you the first action.

You have started when **one action is underway**, not when every field is perfect.

No repository download, code execution or server deployment is required. The template provides the record structure; you still connect your own Notion, copy a prompt and supply your own context. The template also includes Minimal and a blank User Profile to copy directly.

The protocol does not require ChatGPT Plus; use an AI conversation that can accept these instructions. Automatic Notion reads and writes depend on the client, plan and permissions. If no suitable connection is available, use manual handoff without upgrading a plan just to start.

## Daily use

- **Start:** “Boot. Read the latest Daily and my active projects.” If today is already underway, resume the current action.
- **Work:** “I am doing X.” Define a result, a completion check and a first move; then act.
- **Get unstuck:** “I tried X, expected Y and got Z.” Resolve the actual blocker before adding plans.
- **Capture:** “Inbox idea: …” Save it and return to the current outcome unless it is genuinely urgent.
- **Finish:** “Shutdown.” The AI drafts the record from available evidence; you correct gaps; it saves and verifies the handoff.

You can report results in the conversation **or** the Daily page's Personal Notes. Do not write them twice. At the next work turn the AI should read the notes before asking for a recap. Editing Notion or checking Closed does not automatically wake the conversation.

**Closed means the whole day has been reviewed and handed off.** Completing one task does not close a day. You may complete Shutdown yourself by filling Actual Output, Friction and Tomorrow First Move, updating the project's Next Action, and then checking Closed.

## Without Notion

The protocol needs three durable states, not a particular SaaS. A private document with Projects, Daily and Inbox sections is enough for a manual first run.

Notion is the current reference implementation. Obsidian, Markdown, SQLite, Apple Notes or another database could hold the same states. v0.1 provides no adapters for them. Paste the relevant state into your AI conversation and save the returned updates yourself.

## Read next

- [A complete fictional day](examples/example-day.md)
- [A project with a useful Next Action](examples/example-project.md)
- [Boot](workflows/boot.md), [Execution](workflows/execution.md), [Idea Inbox](workflows/idea-inbox.md), [Shutdown](workflows/shutdown.md)
- [Philosophy](principles/philosophy.md)
- [Privacy and publishing](PRIVACY.md)

## Limits

This is an experimental workflow with no demonstrated productivity benefit. It does not provide therapy or health management. AI can misread priorities, fabricate progress or miss technical defects; observed results and user judgment remain necessary.

Memory works only when records are accessible. Tools, account plans and permissions vary. The prompts cannot grant access, schedule background work or guarantee that another conversation remembers your context.

## Repository

~~~text
personal-os/
├── README.md / README.zh-CN.md
├── LICENSE / VERSION / CHANGELOG.md
├── PRIVACY.md / CONTRIBUTING.md / .gitignore
├── prompts/       core prompt, minimal prompt, blank user profile
├── notion/        setup, three schemas, blank daily body
├── workflows/     boot, execution, idea inbox, shutdown
├── principles/    philosophy
└── examples/      fictional day and project
~~~

This completes the v0.1 deliverable. Future onboarding changes can follow actual feedback; recruiting testers and promotion are not prerequisites for use. See [Contributing](CONTRIBUTING.md).
