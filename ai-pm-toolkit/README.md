# AI PM Toolkit

**Production-ready prompt templates and workflows for product managers using Claude.ai**

Stop writing prompts from scratch. Start shipping better product artifacts in minutes.

---

## What This Is

A practical, open-source collection of prompt templates, workflow patterns, and MCP integration guides built for product managers who use Claude.ai daily.

Every template here has been battle-tested in real B2B SaaS product work — PRDs, user stories, competitive analysis, release notes, KB articles, and cross-tool workflows using Claude's MCP integrations (Slack, Linear, Notion, Mixpanel, and more).

**This is not theory. It's copy-paste-and-ship.**

---

## Who This Is For

- Product managers using Claude.ai (free or Pro) who want structured, repeatable outputs
- AI PMs building workflows across Claude + Linear + Notion + Slack + Mixpanel
- PMs transitioning into AI-first product work and want a reference toolkit
- Anyone tired of getting generic AI output and wants PM-grade artifacts

---

## What's Inside

### Prompt Templates

| Template | What It Does | Status |
|---|---|---|
| [PRD Generator](prompts/prd/prd-template.md) | Structured PRD with problem statement, solution, metrics, edge cases, and trade-offs | ✅ Ready |
| [User Story + Acceptance Criteria](prompts/user-stories/user-story-template.md) | User stories with Given/When/Then acceptance criteria and Mixpanel event definitions | ✅ Ready |
| [Competitive Analysis](prompts/competitive-analysis/competitive-analysis-template.md) | Feature-level competitive comparison with scoring matrix and strategic takeaways | ✅ Ready |
| [Release Notes](prompts/release-notes/release-notes-template.md) | Internal and external release notes from raw feature lists or tickets | ✅ Ready |
| [KB Article Generator](prompts/kb-articles/kb-article-template.md) | Step-by-step knowledge base articles with tips, warnings, and role-based guidance | ✅ Ready |

### MCP Workflow Guides

| Guide | What It Covers | Status |
|---|---|---|
| [Linear + Claude Workflow](workflows/mcp-integrations/linear-claude-workflow.md) | Creating issues, syncing sprint data, generating release notes from Linear tickets | ✅ Ready |
| [Slack + Claude Workflow](workflows/mcp-integrations/slack-claude-workflow.md) | Drafting announcements, searching threads, synthesizing channel insights | ✅ Ready |
| [Notion + Claude Workflow](workflows/mcp-integrations/notion-claude-workflow.md) | Creating pages, querying databases, building documentation from Notion data | ✅ Ready |

### Coming Soon

- [ ] Mixpanel event taxonomy generator
- [ ] Sprint retrospective synthesizer
- [ ] Customer feedback clustering prompt
- [ ] Figma-to-PRD bridge workflow
- [ ] Stakeholder update email generator
- [ ] OKR drafting and alignment prompt
- [ ] RICE/ICE scoring prompt with weighted criteria

---

## How to Use

### Quick Start (30 seconds)

1. Open any template `.md` file
2. Copy the prompt
3. Paste into Claude.ai
4. Replace the `[PLACEHOLDERS]` with your context
5. Get a production-grade artifact

### With MCP Integrations

1. Connect your tools in Claude.ai → Settings → Connected Apps
2. Follow the workflow guide for your tool combination
3. Use the prompts with live data from your connected tools

### Pro Tips

- **Stack prompts**: Use the PRD template first, then feed the output into the User Story template for a complete spec chain
- **Add context**: The more specific your placeholders, the better the output. "Enterprise BFSI customers with 500+ hires/month" beats "large customers"
- **Iterate in conversation**: These prompts are designed for multi-turn refinement, not one-shot generation

---

## Template Design Principles

Every template in this repo follows these principles:

1. **Structured output** — Tables, sections, checklists. No walls of text.
2. **Role-aware** — Templates account for who's reading (engineers, designers, leadership, CS).
3. **Metric-driven** — Every artifact includes success criteria and measurement methods.
4. **Edge-case conscious** — Prompts explicitly ask Claude to surface edge cases and trade-offs.
5. **Copy-paste ready** — Zero setup. Works in Claude.ai immediately.

---

## Contributing

This toolkit grows with community input. Here's how to contribute:

1. **Submit a template**: Fork → add your template in the appropriate folder → PR
2. **Improve existing templates**: Found a better prompt pattern? Submit a PR with before/after examples
3. **Share a workflow**: Document how you chain Claude + MCP tools for a specific PM task
4. **Request a template**: Open an issue with the artifact type and use case

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

MIT — use it, fork it, adapt it, share it.

---

## About

Built by [Sayan Gupta](https://www.linkedin.com/in/sayangupta07/) — Lead Product Manager working on AI-powered hiring automation and workflow tools for enterprise customers. I use Claude.ai daily for PRDs, user stories, competitive analysis, and cross-tool workflows.

This repo is a distillation of what actually works in production PM work, not what sounds good in a blog post.

**Find me on**: [LinkedIn](https://www.linkedin.com/in/sayangupta07/) · [Substack](https://sayangupta.substack.com/) · [Portfolio](https://sayan-gupta-portfolio.vercel.app/)
