# User Story + Acceptance Criteria Generator

## When to Use

Use this when you need to break down a feature or PRD into engineering-ready user stories with testable acceptance criteria and analytics event definitions.

**Best for**: Sprint planning, backlog grooming, handoff to engineering.
**Output**: Structured user stories with Given/When/Then acceptance criteria and Mixpanel event specs.

---

## The Prompt

```
You are a senior product manager writing user stories for an engineering team.

Generate user stories for the following feature:

**Feature Name**: [FEATURE_NAME]
**Module/Area**: [e.g., Candidate Scheduling, Dashboard, Proctoring]
**Primary Persona**: [e.g., Recruiter managing 20+ open workflows]
**Context**: [Brief description of the feature — 2-3 sentences]

For each user story, provide:

### User Story Format

**Title**: [Concise action-oriented title]

**Description**:
As a [specific role/persona with context]
I want [specific functionality]
so that [measurable or observable benefit]

**Acceptance Criteria** (minimum 3 per story):

Given [precondition / initial state]
When [specific user action]
Then [observable outcome]

**Mixpanel Event Definitions** (for each story):

For each event, provide:
- **Event Name**: Format as `persona_module_action` (e.g., `recruiter_dashboard_viewed`)
- **Goal**: What this event measures (1 sentence)
- **Description**: When this event fires (trigger condition)
- **Key Properties**: List of event properties to capture (e.g., workflow_id, candidate_count, source)

**Story Sizing Guidance**:
- Tag each story as S (< 2 days), M (2-5 days), or L (5+ days, consider splitting)

**Dependencies**:
- List any API, design, or cross-team dependencies

**Edge Cases**:
- List 2-3 edge cases or failure scenarios per story

---

**Rules**:
- Each story should be independently deliverable
- Avoid compound stories (one story = one capability)
- Acceptance criteria must be testable — no subjective language
- Event names use snake_case, lowercase only
- Properties should include at least: user_role, timestamp, and one context-specific property
```

---

## Example Output (Truncated)

> **Title**: Recruiter Schedules Interview via Workflow
>
> **Description**:
> As a recruiter managing 20+ open workflows
> I want to schedule an interview for a candidate directly from the workflow detail view
> so that I can reduce scheduling time from 5 minutes to under 1 minute per candidate
>
> **Acceptance Criteria**:
>
> Given the recruiter is on the workflow detail page with candidates in "Shortlisted" status
> When the recruiter clicks "Schedule Interview" on a candidate card
> Then the scheduling side panel opens with pre-filled workflow context (provider, duration, interviewer pool)
>
> Given the recruiter has uploaded a candidate template with 10 candidates
> When 2 candidates have invalid email formats
> Then the system highlights the invalid rows, blocks scheduling for those candidates, and allows the remaining 8 to proceed
>
> Given the recruiter confirms the interview schedule
> When the schedule is saved successfully
> Then the candidate moves to "Interview Scheduled" status and an email/SMS notification is triggered
>
> **Mixpanel Event Definitions**:
>
> | Event Name | Goal | Description | Key Properties |
> |---|---|---|---|
> | `recruiter_interview_scheduled` | Measure scheduling adoption and volume | Triggered when recruiter confirms an interview schedule from workflow detail | `workflow_id`, `candidate_count`, `provider`, `scheduling_method` (manual/template), `user_role` |
> | `recruiter_template_uploaded` | Track template-based scheduling usage | Triggered when recruiter uploads a candidate spreadsheet | `workflow_id`, `row_count`, `error_count`, `user_role` |

---

## Customization Tips

- **For bulk operations**: Add a "Batch Behavior" section specifying how the story handles 1 vs. N items
- **For role-based features**: Create one story per role if the behavior diverges (don't overload a single story with role conditionals)
- **For AI-powered features**: Add acceptance criteria for confidence thresholds, fallback behavior, and human-in-the-loop escalation
- **Chaining from PRD**: Paste the "Functional Requirements" section of your PRD as context and ask Claude to decompose into stories

---

## Related Templates

- [PRD Generator](../prd/prd-template.md) — Generate the PRD first, then decompose into stories
- [Release Notes](../release-notes/release-notes-template.md) — Generate release notes from completed stories
