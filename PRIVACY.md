# Privacy boundary

The public project is a protocol and a blank structure. A personal instance is private data. Keep them separate from the first day.

## For users

- Copy User Profile into an ignored local folder or outside this repository. Keep real Projects, Daily, Inbox and conversation exports there too.
- Use the AI client's normal authorization flow. Never put access tokens, keys or passwords in prompts, notes, issues or commits.
- Give the AI only the context needed for the current decision. Review the client and connector permissions.
- Keep your personal Notion copy private. A public template is not a place to operate your day.
- Report bugs with fictional reproductions. Remove names, contact details, account identifiers, private links, paths and screenshots of unrelated content.

## For template maintainers

Create a fresh template page and new databases. Use fictional records. Relations, linked views and mentions must resolve entirely inside that template; do not reuse a private data source or duplicate a populated personal workspace.

Publishing a Notion page also publishes its descendants by default. Notion states that contributor names, profile photos and email addresses can appear in the published page's metadata. Use an identity intended for public attribution, inspect every descendant and relation, and review the public version before sharing it. See [Notion's publishing guidance](https://www.notion.com/help/public-pages-and-web-publishing).

v0.1.1 links to the standalone public reference template supplied by its maintainer. That public URL is intentional; private instance links and identifiers must stay out of the repository. The template's public content and Duplicate entry were checked without signing in. This is not a guarantee about contributor metadata or a completed duplicate in another workspace. The manual setup path remains usable if the template disappears.

## Before a public commit

Review both files and Git history for credentials, personal records, account data, private URLs and local paths. Review commit author metadata too. An ignore rule does not protect an already tracked file or erase old commits.

Examples in this repository are explicitly fictional. Do not “make them realistic” by pasting your own logs.

## 中文要点

公开的是协议和空白结构，自己的实例始终私有。个人资料和真实记录放在仓库外或被忽略的目录；不要在 Prompt、Issue 或提交中放凭据。公开 Notion 模板应新建数据源，关联全部留在模板内部，并检查发布元数据和所有子页面。
