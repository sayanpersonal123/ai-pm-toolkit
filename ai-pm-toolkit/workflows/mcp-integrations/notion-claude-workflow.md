# Notion + Claude MCP Workflow Guide

## Overview

This guide covers practical workflows for product managers using Claude.ai with the Notion MCP integration. Once connected, Claude can search your Notion workspace, read pages and databases, create new pages, and update existing ones.

---

## Setup

1. Go to **Claude.ai → Settings → Connected Apps**
2. Connect **Notion**
3. Authorize Claude to access your Notion workspace
4. Ensure the pages/databases you want Claude to access are shared with the integration

**Important**: Claude can only access Notion pages and databases that have been explicitly shared with the Claude integration. If Claude can't find something, check your Notion sharing settings.

---

## Workflow 1: Generate PRD in Notion from Conversation

**When to use**: You've discussed a feature in Claude and want to push the PRD directly into your Notion workspace.

**Prompt**:
```
Create a new page in my Notion workspace under [PARENT_PAGE_OR_DATABASE_NAME] with:

**Title**: PRD — [FEATURE_NAME]

**Content**:
[PASTE YOUR PRD CONTENT OR USE THE PRD TEMPLATE OUTPUT]

Format the content with Notion-compatible headings, bullet lists, and tables.
Add a "Status" property set to "Draft" and a "Last Updated" property set to today's date.
```

---

## Workflow 2: Query a Product Database and Summarize

**When to use**: You have a Notion database (e.g., Feature Tracker, Bug Log, Customer Requests) and need a summary view.

**Prompt**:
```
Query my Notion database "[DATABASE_NAME]" and provide:

1. Total items by status (e.g., Planned / In Progress / Shipped / Blocked)
2. Items with priority "P0" that are not in "Shipped" status
3. Items assigned to [PERSON_NAME] — list titles and statuses
4. Any items updated in the last 7 days

Format as a table, sorted by priority.
```

---

## Workflow 3: Create Meeting Notes Page

**When to use**: After a meeting, quickly structure and push notes into Notion.

**Prompt**:
```
Create a new page in Notion under [MEETING_NOTES_DATABASE] with:

**Title**: [MEETING_NAME] — [DATE]

**Sections**:
- **Attendees**: [List names]
- **Agenda**: [Bullet list of discussion topics]
- **Key Decisions**: [What was agreed]
- **Action Items**: [Table: Action | Owner | Due Date]
- **Open Questions**: [Items needing follow-up]
- **Next Meeting**: [Date/time if set]

Tag with: [PROJECT_TAG]
```

---

## Workflow 4: Bulk-Create Pages from Structured Data

**When to use**: You have a list (e.g., customer requirements, feature specs, onboarding tasks) and need to create individual Notion pages for each.

**Prompt**:
```
I have the following list of items to add to my Notion database "[DATABASE_NAME]":

[
- Item 1: Title, Description, Priority, Owner
- Item 2: Title, Description, Priority, Owner
- Item 3: Title, Description, Priority, Owner
]

Create a Notion page for each item with the appropriate properties.
Confirm the list before creating.
```

---

## Workflow 5: Documentation Audit

**When to use**: Need to check which docs are outdated or missing in a Notion workspace section.

**Prompt**:
```
Search my Notion workspace for all pages under "[SECTION_OR_PARENT_PAGE]".

For each page, list:
- Page title
- Last edited date
- Last edited by (if available)

Flag any pages not updated in the last 90 days as "Potentially Stale".
Format as a table sorted by last edited date (oldest first).
```

---

## Tips

- **Database vs. Page**: Know the difference — databases support properties (status, priority, tags), pages are free-form. Use databases for trackable items, pages for documentation.
- **Search first, then act**: If you're unsure of exact page/database names, ask Claude to "search Notion for pages related to [KEYWORD]" before creating or updating.
- **Combine with Slack and Linear**: Pull sprint data from Linear, create a sprint summary in Notion, and announce it in Slack — all in one Claude conversation.
- **Template pages**: If your Notion workspace has template pages, ask Claude to reference them: "Create a new page using the format of [EXISTING_PAGE_NAME]."

---

## Limitations

- Claude can only access pages/databases shared with the Notion integration — unshared pages are invisible.
- Notion API doesn't support all block types (e.g., synced blocks, embedded databases). Some content may not render perfectly.
- Bulk operations require confirmation — Claude will list items before creating them.
- Claude cannot modify Notion workspace-level settings, integrations, or permissions.
