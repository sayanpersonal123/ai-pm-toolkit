# AI PM Toolkit

**Production-ready prompt templates and workflows for product managers using Claude.ai**

PRDs, user stories, competitive analysis, release notes, KB articles - structured, repeatable, production-grade.

---

## Templates

| Template | What It Does |
|---|---|
| [PRD Generator](https://github.com/sayanpersonal123/ai-pm-toolkit/blob/main/ai-pm-toolkit/prompts/prd/prd-template.md) | Structured PRD with problem statement, solution, metrics, edge cases, and trade-offs |
| [User Story + Acceptance Criteria](https://github.com/sayanpersonal123/ai-pm-toolkit/blob/main/ai-pm-toolkit/prompts/user-stories/user-story-template.md) | User stories with Given/When/Then acceptance criteria and Mixpanel event definitions |
| [Competitive Analysis](https://github.com/sayanpersonal123/ai-pm-toolkit/blob/main/ai-pm-toolkit/prompts/competitive-analysis/competitive-analysis-template.md) | Feature-level competitive comparison with scoring matrix and strategic takeaways |
| [Release Notes](https://github.com/sayanpersonal123/ai-pm-toolkit/blob/main/ai-pm-toolkit/prompts/release-notes/release-notes-template.md) | Internal and external release notes from raw feature lists or tickets |
| [KB Article Generator](https://github.com/sayanpersonal123/ai-pm-toolkit/blob/main/ai-pm-toolkit/prompts/kb-articles/kb-article-template.md) | Step-by-step knowledge base articles with tips, warnings, and role-based guidance |

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

### Template Format

All templates follow this structure:

```
# Template Name

## When to Use
## The Prompt
## Example Output
## Customization Tips
## Related Templates
```

---

## Star History

If this toolkit saves you time, star it so other PMs can find it.

---

## License

MIT - use it, fork it, adapt it, share it.

---

## About

Built by [Sayan Gupta](https://www.linkedin.com/in/sayangupta07/) — Lead Product Manager working on AI-native hiring automation and workflow tools for enterprise customers. I use Claude.ai daily for PRDs, user stories, competitive analysis, and cross-tool workflows.

This repo is a distillation of what actually works in production PM work, not what sounds good in a blog post.

**Find me on**: [LinkedIn](https://www.linkedin.com/in/sayan-gupta007/) · [Substack](https://sayangupta.substack.com/) · [Portfolio](https://www.sayangupta.in/)
