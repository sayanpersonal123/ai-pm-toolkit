# Contributing to AI PM Toolkit

Thanks for your interest in contributing. This toolkit gets better when PMs share what works in their real workflows.

## How to Contribute

### Submit a New Template

1. Fork this repo
2. Create your template in the appropriate folder under `prompts/` or `workflows/`
3. Follow the template format (see below)
4. Submit a PR with a clear title: `Add: [Template Name] — [Category]`

### Improve an Existing Template

1. Fork this repo
2. Edit the template with your improvements
3. Submit a PR with: `Improve: [Template Name] — [What Changed]`
4. Include a brief before/after comparison in the PR description

### Request a Template

Open an issue with:
- **Title**: `Request: [Template Name]`
- **Description**: What artifact you need, what persona uses it, and why existing templates don't cover it

### Share a Workflow

Document your Claude + MCP tool workflow in the `workflows/` folder. Include setup steps, prompts, and tips.

---

## Template Format

Every template must include these sections:

```markdown
# Template Name

## When to Use
(Trigger conditions, best-fit scenarios, output type)

## The Prompt
(The actual copy-paste prompt with [PLACEHOLDERS])

## Example Output
(Truncated but realistic example of what Claude produces)

## Customization Tips
(3-4 variations for different use cases)

## Related Templates
(Links to complementary templates in this repo)
```

---

## Quality Standards

- Templates must produce usable output on first run (no multi-step setup)
- Prompts should work in Claude.ai free and Pro tiers
- Placeholders must be clearly marked with `[SQUARE_BRACKETS]`
- No proprietary or company-specific data in examples
- Examples should be realistic but generic enough to be universally useful

---

## Code of Conduct

Be constructive, specific, and practical. This is a toolkit for working PMs — keep contributions actionable.
