# Linear + Claude MCP Workflow Guide

## Overview

This guide covers practical workflows for product managers using Claude.ai with the Linear MCP integration. Once connected, Claude can read your Linear workspace — teams, projects, issues, cycles, labels — and create/update issues directly from conversation.

---

## Setup

1. Go to **Claude.ai → Settings → Connected Apps**
2. Connect **Linear**
3. Authorize Claude to access your Linear workspace

Once connected, Claude can access your Linear data in any conversation without additional setup.

---

## Workflow 1: Generate Sprint Release Notes from a Cycle

**When to use**: End of sprint/cycle, need to compile what shipped.

**Prompt**:
```
List all completed issues in the current cycle for the [TEAM_NAME] team in Linear.

Then generate internal release notes grouped by:
- New Features
- Improvements
- Bug Fixes

For each item, include: issue title, brief description (1 sentence), and the assignee.
Format as a Slack-ready message with sections.
```

---

## Workflow 2: Create User Stories in Linear from a PRD

**When to use**: After PRD approval, need to decompose into Linear issues.

**Prompt**:
```
Here is a PRD for [FEATURE_NAME]:

[PASTE PRD OR PRD SUMMARY]

Decompose this into Linear issues for the [TEAM_NAME] team with:
- Issue title (action-oriented)
- Description (user story format: As a... I want... so that...)
- Labels: [feature], [PRIORITY_LABEL]
- Estimate: S/M/L based on complexity

Create each issue in Linear under the project "[PROJECT_NAME]".
```

**Note**: Claude will ask for confirmation before creating issues. Review the list before confirming.

---

## Workflow 3: Sprint Planning Context Pull

**When to use**: Before sprint planning, need a summary of backlog state.

**Prompt**:
```
For the [TEAM_NAME] team in Linear, give me:

1. All issues in "Backlog" status, grouped by label/priority
2. Any issues that have been in "In Progress" for more than 7 days
3. Issues with no assignee
4. Total issue count by status (Backlog, Todo, In Progress, Done)

Format as a table I can paste into a planning doc.
```

---

## Workflow 4: Search and Summarize Issues by Topic

**When to use**: Preparing for a feature review or stakeholder update.

**Prompt**:
```
Search Linear for all issues related to "[FEATURE_OR_KEYWORD]" across all teams.

Summarize:
- Total count by status
- Key blockers or stalled items
- Most recent activity
- Any open questions in comments
```

---

## Tips

- **Be specific about team names**: Linear workspaces often have multiple teams. Always specify which team.
- **Use project names for scoping**: If your feature spans multiple cycles, reference the Linear project name for continuity.
- **Combine with Slack MCP**: After generating release notes from Linear, draft a Slack message in the relevant channel — all in one conversation.
- **Batch operations**: Claude can create multiple issues in one conversation. List them all, review, then confirm.

---

## Limitations

- Claude reads your current Linear state — it does not have access to historical snapshots or deleted items.
- Issue creation requires your confirmation before Claude executes.
- Complex Linear automations (e.g., auto-assignment rules, webhook triggers) are not controlled via MCP.
