# Release Notes Generator

## When to Use

Use this when you need to write release notes for internal stakeholders (CS, Sales, Engineering) or external customers after a product release cycle.

**Best for**: Sprint/cycle releases, major feature launches, platform updates.
**Output**: Internal and external release note variants from the same input.

---

## The Prompt

```
You are a senior product manager writing release notes.

Generate release notes for the following release:

**Release/Cycle Name**: [e.g., Cycle 34, v2.5.0, March 2026 Release]
**Release Date**: [DATE]
**Product/Module**: [e.g., Workflow Tools, Scheduling, Ivy AI]
**Target Audience**: [Internal (CS/Sales/Engineering) | External (Customers) | Both]

**Features and Changes** (paste raw list, tickets, or descriptions):
[
- Feature 1: Brief description
- Feature 2: Brief description
- Bug fix 1: Brief description
- Improvement 1: Brief description
]

Generate TWO versions:

---

### Version 1: Internal Release Notes (for CS, Sales, Solutions, Engineering)

Structure:
- **Release Summary**: 2-3 sentence overview of what shipped and why it matters
- **What's New**: Each feature with:
  - Feature name
  - What it does (functional description)
  - Who it benefits (persona/role)
  - How to demo it (for Sales/CS — 2-3 steps)
  - Known limitations or caveats
- **Improvements**: UX, performance, or workflow enhancements
- **Bug Fixes**: Grouped by module, brief description of what was broken and what's fixed
- **Migration/Action Items**: Anything CS or Sales needs to do (update talk tracks, notify customers, update documentation)
- **Known Issues**: Outstanding issues shipping with this release

---

### Version 2: External Release Notes (for customers)

Structure:
- **What's New**: Customer-friendly feature descriptions focused on benefits, not implementation
- **Improvements**: Framed as "you can now..." or "we've made X easier/faster"
- **Bug Fixes**: Only customer-facing bugs, described without technical jargon
- **Coming Soon**: 1-2 teaser items for the next cycle (optional)

---

**Rules**:
- Internal notes can be technical; external notes must be jargon-free
- Lead with the highest-impact feature
- Each feature description should be 2-4 sentences max
- Use present tense ("Recruiters can now..." not "We have added...")
- Do not overstate — if it's a minor fix, say so
```

---

## Example Output (Truncated)

> ### Version 1: Internal Release Notes
>
> **Release Summary**: Cycle 34 ships SMS interview notifications, bulk candidate template upload improvements, and 6 bug fixes across Scheduling and Workflow modules. The SMS feature is a direct response to no-show rate concerns flagged by Cognizant and HCL account teams.
>
> **What's New**:
>
> **SMS Interview Notifications**
> - Candidates now receive interview invitations via SMS (Twilio) in addition to email
> - Benefits recruiters managing high-volume workflows (500+ candidates/month)
> - **Demo steps**: Open Workflow → Schedule Interview → Toggle "Send SMS" → Confirm
> - **Limitation**: SMS delivery is India and US only at launch. International expansion in Cycle 36.

---

## Customization Tips

- **From Linear tickets**: Paste the Linear issue titles and descriptions directly as the feature list — Claude will restructure them
- **For multi-module releases**: Ask Claude to group by module with sub-headers
- **For customer-facing changelogs**: Use Version 2 and ask Claude to add a "How to access" link for each feature
- **For Slack announcements**: Ask Claude to compress the internal notes into a 5-bullet Slack-friendly format

---

## Related Templates

- [User Story + Acceptance Criteria](../user-stories/user-story-template.md) — Stories that feed into release notes
- [KB Article Generator](../kb-articles/kb-article-template.md) — Generate help docs for new features
