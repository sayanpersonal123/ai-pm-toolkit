# Slack + Claude MCP Workflow Guide

## Overview

This guide covers practical workflows for product managers using Claude.ai with the Slack MCP integration. Once connected, Claude can search messages, read channels/threads, draft messages, and create canvases in your Slack workspace.

---

## Setup

1. Go to **Claude.ai → Settings → Connected Apps**
2. Connect **Slack**
3. Authorize Claude to access your Slack workspace

---

## Workflow 1: Synthesize a Channel into Action Items

**When to use**: A Slack channel has 50+ messages of discussion and you need to extract decisions and action items.

**Prompt**:
```
Search the #[CHANNEL_NAME] Slack channel for messages from the last 7 days.

Synthesize into:
1. **Key Decisions Made**: What was agreed upon (with who decided)
2. **Open Questions**: Unresolved items that need follow-up
3. **Action Items**: Who owes what, with any mentioned deadlines
4. **Blocked Items**: Anything explicitly called out as blocked

Format as a table I can paste into a standup doc or Notion page.
```

---

## Workflow 2: Draft a Feature Announcement

**When to use**: Feature shipped, need to announce in a product or CS channel.

**Prompt**:
```
Draft a Slack message for #[CHANNEL_NAME] announcing the following feature:

**Feature Name**: [FEATURE_NAME]
**What it does**: [2-3 sentences]
**Who benefits**: [Target persona]
**How to access**: [Steps or link]
**Known limitations**: [Any caveats]

Tone: Professional but approachable. No emojis in headers. Max 10 lines.
Include a "Questions?" closing line tagging @[YOUR_NAME].

Save as a draft in the channel — do not send.
```

**Note**: Claude creates a draft in Slack's "Drafts & Sent" — it does not send the message until you review and hit send yourself.

---

## Workflow 3: Search for Customer Feedback Mentions

**When to use**: Preparing for a product review or discovery session.

**Prompt**:
```
Search Slack for messages mentioning "[CUSTOMER_NAME]" or "[FEATURE_KEYWORD]" across public channels.

Summarize:
- Total messages found
- Top themes (group by topic)
- Sentiment (positive / neutral / negative per theme)
- Any specific feature requests or complaints quoted (keep under 10 words each)
- Channels where most discussion happened
```

---

## Workflow 4: Create a Sprint Recap Canvas

**When to use**: End of sprint, need a shareable recap.

**Prompt**:
```
Create a Slack Canvas in #[CHANNEL_NAME] with:

**Title**: Sprint [NUMBER] Recap — [DATE RANGE]

**Sections**:
- What We Shipped (bullet list of features/fixes)
- Key Metrics This Sprint (table: metric | target | actual)
- What Slipped and Why (brief explanation per item)
- Next Sprint Focus (3-5 priorities)
- Shoutouts (team/individual callouts)

Keep it concise — this is a skim-read doc, not a report.
```

---

## Workflow 5: Pre-Meeting Context Pull

**When to use**: Before a meeting, need to quickly catch up on a topic discussed in Slack.

**Prompt**:
```
Search Slack for recent messages about "[TOPIC]" in #[CHANNEL_NAME].

Give me a 5-bullet briefing:
- What's the current state
- Who's involved
- What decisions were made
- What's still open
- Any deadlines mentioned
```

---

## Tips

- **Draft first, send manually**: Always use the draft workflow for announcements. Review tone and accuracy before sending.
- **Public vs. private channels**: The `slack_search_public` tool only searches public channels. For private channels, use `slack_search_public_and_private`.
- **Combine with Linear**: Pull completed issues from Linear, then draft a release announcement in Slack — one conversation, two tools.
- **Thread reading**: If a discussion lives in a thread, ask Claude to "read the thread at [thread link]" for full context.

---

## Limitations

- Claude cannot send messages without your confirmation (drafts only by default).
- DM search requires finding the user ID first via `slack_search_users`.
- Externally shared channels (Slack Connect) do not support draft creation.
- Claude cannot delete or edit existing messages — only create new ones or drafts.
