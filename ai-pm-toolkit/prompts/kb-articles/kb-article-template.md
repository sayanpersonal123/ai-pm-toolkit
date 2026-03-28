# Knowledge Base Article Generator

## When to Use

Use this when you need to create customer-facing or internal help documentation for a feature, workflow, or process.

**Best for**: New feature documentation, onboarding guides, troubleshooting articles, admin configuration guides.
**Output**: Step-by-step KB article with role-based guidance, tips, and warnings.

---

## The Prompt

```
You are a senior product manager writing a knowledge base article for a B2B SaaS platform.

Generate a KB article for the following:

**Article Topic**: [e.g., How to schedule interviews for new candidates]
**Product/Module**: [e.g., Workflow Tools — Scheduling]
**Target Reader**: [e.g., Recruiters and Master Recruiters]
**Prerequisite Knowledge**: [e.g., Reader has access to the Workflow dashboard and has created at least one workflow]

**Feature Context** (paste raw description, PRD excerpt, or bullet points):
[
- What the feature does
- Key steps involved
- Any configuration or setup required
]

Structure the article as follows:

### Article Format

**Opening paragraph**: 1-2 sentences explaining what this article covers, who it's for, and what the reader will be able to do after reading it.

**Step-by-step Guide**:

For each major step:
- **Step N: [Action Title]**
  - Clear instruction (imperative mood: "Click", "Select", "Navigate to")
  - Sub-steps as indented bullets where needed
  - **Tip**: Helpful shortcut or best practice (where relevant)
  - **Warning**: Common mistake or gotcha (where relevant)
  - **Note**: Role-specific behavior or permission differences (where relevant)

**Troubleshooting** (if applicable):
- Common error → Cause → Resolution (table format)

**Related Articles**:
- Links to related KB articles

---

**Rules**:
- Use imperative mood for instructions ("Click Schedule" not "You should click Schedule")
- Keep sentences short — max 20 words per instruction line
- Use exact UI labels in **bold** (e.g., Click **Schedule**, Select **Download Template**)
- One action per step — don't combine multiple clicks in one instruction
- Include role-based callouts if behavior differs by role (Recruiter vs. Master Recruiter vs. Admin)
- Add a Tip or Warning for any step where users commonly make mistakes
- Do not assume technical knowledge — explain acronyms on first use
```

---

## Example Output (Truncated)

> This article explains how recruiters and master recruiters can schedule interviews for new candidates within the Workflow platform. After reading, you'll be able to download the candidate template, add candidate information, and confirm interview schedules.
>
> **Step-by-step Guide**:
>
> **Step 1: Access the Workflow Dashboard**
> - From the main menu, navigate to **Workflows**.
> - Select the workflow where you want to schedule interviews.
>
> **Step 2: Configure Interview Details**
> - Click **Schedule** to begin organizing interviews.
> - From the Schedule side panel:
>   - Choose the **Provider** (platform where the interview will be conducted).
>   - Select the **Interview Duration**.
>   - Click **Download Template** to get the candidate spreadsheet.
> - Open the downloaded file, fill in candidate details, and save it.
> - Click **Upload** to import the completed spreadsheet.
> - Manually choose the **Interviewer**, **Date**, and **Time**.
>
> **Tip**: Ensure candidate details match the required format in the template before uploading. Incomplete or incorrect data may cause scheduling errors.

---

## Customization Tips

- **For admin/config articles**: Add a "Prerequisites" section with required permissions and settings
- **For troubleshooting-focused articles**: Expand the troubleshooting table and reduce the step-by-step section
- **For multi-role articles**: Use callout blocks like `> **Master Recruiter only**: This option is visible only to users with Master Recruiter permissions`
- **For video-supported articles**: Add a "Video Walkthrough" section placeholder at the top

---

## Related Templates

- [Release Notes](../release-notes/release-notes-template.md) — Ship release notes alongside KB articles for new features
- [User Story + Acceptance Criteria](../user-stories/user-story-template.md) — Reference acceptance criteria for accurate KB content
