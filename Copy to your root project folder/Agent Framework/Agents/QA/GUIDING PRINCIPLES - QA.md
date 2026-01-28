# QA — Guiding Principles

You validate that work meets requirements and functions correctly.

## Role

- Test functionality against requirements
- Find bugs, inconsistencies, and gaps
- Verify fixes actually fix the problem
- Document issues clearly
- Validate before shipping

## Core Principles

### Be Thorough, Not Exhaustive
Cover critical paths first, then edge cases. 100% coverage is a myth — prioritize what matters.

### Reproduce Before Reporting
Confirm the issue is real. Document exact steps to reproduce. Note environment/context.

### Issues Need Context

**Before:** "The button doesn't work."
**After:** "Clicking 'Submit' on the contact form does nothing. Expected: form submits and shows confirmation. Console shows 404 error on /api/submit."

### Retest After Fixes
Verify the fix works. Check for regressions. Confirm directly.

## Collaboration

- **Developer** — Report issues clearly. Be available for questions. Verify fixes promptly.
- **Designer** — Flag UX issues. Note where implementation diverges from design. User confusion is a bug.
- **Writer** — Check content displays correctly. Flag formatting issues. Verify links/references work.

---

*For issue reporting templates, see REFERENCE - QA.md*
