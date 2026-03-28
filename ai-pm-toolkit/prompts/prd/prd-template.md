# PRD Generator

## When to Use

Use this when you need to draft a Product Requirements Document for a new feature, capability, or product area. Works best when you have at least a rough problem statement and target persona.

**Best for**: New features, platform capabilities, integrations, workflow changes.
**Output**: A structured PRD ready for engineering review and stakeholder alignment.

---

## The Prompt

```
You are a senior product manager writing a PRD for an engineering and design audience.

Generate a comprehensive PRD for the following feature:

**Feature Name**: [FEATURE_NAME]
**Product/Platform**: [PRODUCT_NAME]
**Target Persona**: [e.g., Recruiters managing 50+ requisitions in enterprise ITeS companies]
**Problem Context**: [2-3 sentences on what's broken or missing today]

Structure the PRD with these sections:

### 1. Problem Statement
- What is the core problem?
- Who is affected and how frequently?
- What is the cost of inaction (quantify if possible)?

### 2. Proposed Solution
- High-level solution description
- Key capabilities (bullet list, max 7)
- What this does NOT include (explicit scope boundaries)

### 3. User Personas & Roles
- Primary persona(s) with role description
- Secondary persona(s) if applicable
- Role-based access or visibility differences

### 4. User Flows
- Happy path (numbered steps)
- Key alternate flows
- Error/edge case handling

### 5. Functional Requirements
- Organized by module or capability area
- Each requirement as a clear, testable statement
- Priority tagged as P0 (must-have), P1 (should-have), P2 (nice-to-have)

### 6. Non-Functional Requirements
- Performance expectations
- Security/compliance considerations
- Scalability and data volume assumptions

### 7. Success Metrics
- 3-5 measurable success criteria
- Each with: metric name, target value, measurement method, measurement timeline

### 8. Dependencies & Risks
- Technical dependencies
- Cross-team dependencies
- Key risks with mitigation strategies

### 9. Open Questions
- List unresolved decisions that need stakeholder input

### 10. Appendix
- Competitive references (if applicable)
- Related PRDs or design docs
- Glossary of domain-specific terms

**Formatting rules**:
- Use tables where comparisons are needed
- Use numbered lists for sequential flows
- Use bullet lists for non-sequential items
- Bold key terms on first use
- Keep language precise and jargon-free where possible
```

---

## Example Output (Truncated)

> **Feature Name**: SMS Interview Notifications
>
> ### 1. Problem Statement
> Candidates in high-volume hiring workflows (500+ candidates/month) frequently miss interview invitations sent via email, leading to 30-40% no-show rates. Recruiters at enterprise ITeS clients (Cognizant, HCL, PwC) have flagged this as a top-3 pain point in CSM interviews...
>
> ### 7. Success Metrics
> | # | Metric | Target | Measurement Method | Timeline |
> |---|---|---|---|---|
> | 1 | Interview attendance rate | +15% vs. email-only baseline | Mixpanel funnel: `candidate_interview_notification_sent` → `candidate_interview_attended` | 90 days post-launch |
> | 2 | Notification delivery rate | >95% | Twilio delivery receipts aggregated in Mixpanel | 30 days post-launch |

---

## Customization Tips

- **For API/Integration PRDs**: Add a section for "API Contract / Interface Specification" between sections 5 and 6
- **For Platform/Infra PRDs**: Replace "User Flows" with "System Interaction Diagram" and add a "Migration Plan" section
- **For AI/ML features**: Add sections for "Model Evaluation Framework", "Golden Dataset Requirements", and "Bias & Fairness Considerations"
- **Scope control**: The "What this does NOT include" line in Section 2 is critical — explicitly listing exclusions prevents scope creep in review

---

## Related Templates

- [User Story + Acceptance Criteria](../user-stories/user-story-template.md) — Generate stories from PRD requirements
- [Release Notes](../release-notes/release-notes-template.md) — Generate release notes from PRD after launch
