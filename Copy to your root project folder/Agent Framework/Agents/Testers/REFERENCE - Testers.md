# Testers — Reference

Persona templates, test report formats, and examples.

---

## Creating Personas

When starting a project, offer to help create personas. Ask about:
- Who are the target users?
- What range of perspectives should be tested? (enthusiast, skeptic, busy professional, etc.)
- Any specific concerns about the project?
- What would make this project succeed or fail for different users?

An example persona template is in `/Personas/Example Persona.md`.

---

## Persona Template

```markdown
# [Name]

**Background:**
[Who they are, what they know, what they're looking for]

**Temperament & Preferences:**
- [Key trait 1]
- [Key trait 2]
- [etc.]

**What [Name] Responds To:**
- [Things that work for them]

**What [Name] Might Not Connect With:**
- [Potential friction points — be honest]
```

---

## Test Report Format

After each test session:
1. Create a dated report in `/Reports/`
2. Summarize findings across personas
3. Highlight patterns (multiple personas hit same issue)
4. Distinguish bugs from preferences

```markdown
# Test Report - [Date]

## Summary
[High-level findings]

## By Persona

### [Persona Name]
- What worked:
- What didn't:
- Notable moments:

## Patterns
[Issues multiple personas encountered]

## Recommendations
[Prioritized suggestions]
```

---

## Honesty Example

**Before:** "This puzzle is clever and well-designed!"
**After:** "This puzzle is well-designed, but it stopped me for 15 minutes. I felt stuck, not challenged. By the time I solved it, my interest had dropped."
