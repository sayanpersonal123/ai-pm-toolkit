# Competitive Analysis Framework

## When to Use

Use this when you need to compare your product against competitors at the feature level, evaluate market positioning, or prepare competitive intelligence for sales/CS enablement.

**Best for**: Feature gap analysis, sales battlecards, strategic planning, investor decks.
**Output**: Structured comparison matrix with scoring, strategic takeaways, and actionable recommendations.

---

## The Prompt

```
You are a senior product manager conducting a competitive analysis.

Analyze the competitive landscape for the following:

**Product/Feature Area**: [e.g., AI-powered interview scheduling, Resume shortlisting]
**Our Product**: [YOUR_PRODUCT_NAME]
**Competitors to Analyze**: [COMPETITOR_1, COMPETITOR_2, COMPETITOR_3, ... up to 5]
**Target Buyer Persona**: [e.g., VP of Talent Acquisition at ITeS companies with 1000+ hires/year]
**Analysis Goal**: [e.g., Identify feature gaps for Q3 roadmap, Prepare sales battlecard, Evaluate build-vs-buy]

Structure the analysis as follows:

### 1. Executive Summary
- 3-sentence competitive positioning summary
- Our strongest differentiators (top 3)
- Our biggest gaps (top 3)

### 2. Feature Comparison Matrix

Create a table with:
- Rows: Key feature capabilities (minimum 12-15 features)
- Columns: Our Product | Competitor 1 | Competitor 2 | ... 
- Cell values: ✅ Full support | 🟡 Partial / Limited | ❌ Not available | 🔜 On roadmap
- Group features by category (e.g., Core Workflow, AI/Automation, Integrations, Reporting, Compliance)

### 3. Scoring Matrix

Rate each product on a 1-5 scale across these dimensions:
- Feature completeness
- AI/Automation depth
- Enterprise readiness (SSO, RBAC, audit logs, compliance)
- Integration ecosystem
- UX/Ease of use
- Pricing competitiveness
- Customer support & documentation

Present as a table with total weighted scores.

### 4. Competitor Deep Dives (per competitor)
- **Positioning**: How they describe themselves (1 sentence)
- **Primary ICP**: Who they sell to
- **Strengths**: Top 3
- **Weaknesses**: Top 3
- **Recent moves**: Notable launches, acquisitions, funding (last 12 months)
- **Threat level**: Low / Medium / High with reasoning

### 5. Strategic Takeaways
- Where we win today (and how to amplify)
- Where we lose today (and whether to address or concede)
- Whitespace opportunities (capabilities no one offers well)
- Recommended roadmap implications (prioritized list)

### 6. Sales Enablement Summary
- 3-5 "When they say X, we say Y" talk tracks
- Key objection handling for each competitor
- Proof points to reference (customer logos, metrics, case studies)

---

**Rules**:
- Be specific — reference actual feature names, not vague categories
- If information is uncertain, mark it as "[Unverified]" rather than guessing
- Prioritize recent data (last 12 months)
- Distinguish between "GA feature" vs. "beta/early access" vs. "announced but not shipped"
```

---

## Example Output (Truncated)

> ### 2. Feature Comparison Matrix
>
> | Capability | Talview | HireVue | Phenom | iCIMS |
> |---|---|---|---|---|
> | **AI/Automation** | | | | |
> | AI Interview (async video) | ✅ | ✅ | 🟡 | ❌ |
> | Conversational AI Interviewer | ✅ | ❌ | 🟡 | ❌ |
> | AI Resume Shortlisting | ✅ | 🟡 | ✅ | 🟡 |
> | Deepfake Detection | 🔜 | ❌ | ❌ | ❌ |
> | **Workflow** | | | | |
> | Configurable hiring workflows | ✅ | 🟡 | ✅ | ✅ |
> | Bulk candidate scheduling | ✅ | ✅ | ✅ | 🟡 |

---

## Customization Tips

- **For sales battlecards**: Focus sections 2, 4, and 6. Strip sections 1, 3, and 5.
- **For roadmap planning**: Focus sections 2, 3, and 5. Ask Claude to rank gaps by customer request frequency.
- **For investor decks**: Focus sections 1 and 5. Ask for a TAM/SAM/SOM overlay.
- **With web search**: Enable Claude's web search and ask it to pull competitor pricing pages, recent blog posts, and G2/Gartner reviews for real-time data.

---

## Related Templates

- [PRD Generator](../prd/prd-template.md) — Convert competitive gaps into feature PRDs
- [Release Notes](../release-notes/release-notes-template.md) — Communicate competitive wins in release notes
