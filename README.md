# AI PM Toolkit

Copy-paste prompt templates and MCP workflow guides for product managers using Claude.ai.

PRDs, user stories, competitive analysis, release notes, KB articles - structured, repeatable, production-grade.

---

## Templates

| Template | What You Get |
|---|---|
| [PRD Generator](prompts/prd/prd-template.md) | 10-section PRD with requirements (P0/P1/P2), success metrics, dependencies |
| [User Stories](prompts/user-stories/user-story-template.md) | Given/When/Then acceptance criteria + Mixpanel event definitions |
| [Competitive Analysis](prompts/competitive-analysis/competitive-analysis-template.md) | Feature matrix, scoring, competitor deep dives, sales talk tracks |
| [Release Notes](prompts/release-notes/release-notes-template.md) | Internal (CS/Sales/Eng) + external (customer-facing) variants |
| [KB Articles](prompts/kb-articles/kb-article-template.md) | Step-by-step articles with tips, warnings, role-based callouts |

## MCP Workflows

Guides for using Claude.ai with connected tools — pull live data, create artifacts, chain actions in one conversation.

| Guide | What You Can Do |
|---|---|
| [Linear + Claude](https://github.com/sayanpersonal123/ai-pm-toolkit/blob/main/ai-pm-toolkit/workflows/mcp-integrations/linear-claude-workflow.md) | Sprint release notes from tickets, PRD → Linear issues, backlog summaries |
| [Slack + Claude](https://github.com/sayanpersonal123/ai-pm-toolkit/blob/main/ai-pm-toolkit/workflows/mcp-integrations/slack-claude-workflow.md) | Channel → action items, feature announcements, feedback mining |
| [Notion + Claude](https://github.com/sayanpersonal123/ai-pm-toolkit/blob/main/ai-pm-toolkit/workflows/mcp-integrations/notion-claude-workflow.md) | Push PRDs to Notion, query databases, meeting notes, doc audits |

---

## How to Use

1. Open any template `.md` file
2. Copy the prompt
3. Paste into Claude.ai
4. Replace `[PLACEHOLDERS]` with your context

Works on Claude.ai free and Pro. No setup.

**Tip**: Stack templates — PRD → User Stories → KB Articles → Release Notes. One feature, four artifacts, one conversation.

---

## Roadmap

- [ ] Mixpanel event taxonomy generator
- [ ] Sprint retrospective synthesizer
- [ ] Customer feedback clustering prompt
- [ ] RICE/ICE scoring prompt
- [ ] OKR drafting prompt
- [ ] Stakeholder update email generator

Request a template → [open an issue](../../issues).

---

## Contributing

Fork → add your template in `prompts/` or `workflows/` → PR. See [CONTRIBUTING.md](CONTRIBUTING.md) for format.

## License

MIT

## Author

**[Sayan Gupta](https://www.linkedin.com/in/sayan-gupta007/)** — Lead PM, enterprise B2B SaaS. [Substack](https://sayangupta.substack.com/) · [Portfolio](https://www.sayangupta.in/)

⭐ Star if useful.
