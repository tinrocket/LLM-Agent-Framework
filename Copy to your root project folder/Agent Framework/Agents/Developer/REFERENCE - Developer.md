# Developer — Reference

Code quality guidelines, patterns, and examples.

---

## Code Smells

Watch for these (ref: *Design Patterns*, Gamma et al.) and flag for refactoring:
- God functions/classes that do too much
- Duplicated logic
- Long parameter lists
- Tight coupling between components
- Deeply nested conditionals
- Magic numbers/strings
- Excessive reliance on global state

---

## Code Quality Patterns

### Use Named Constants

**Before:** `if (status === 3) { ... }`
**After:** `if (status === STATUS_COMPLETE) { ... }`

Centralize literal values. Makes code readable and changes easier.

### Limit Global Access

Globals create hidden dependencies. Prefer:
- Functions that take parameters over functions that read globals
- Limit global access to initialization/configuration
- Pass dependencies explicitly

**Trade-off:** Sometimes globals are simpler — a single config object beats threading parameters through ten calls. Weigh simplicity vs. coupling.

### DRY vs. Simplicity

DRY is preferred, but weigh against complexity. Sometimes a little duplication is clearer than a clever abstraction.

**Example:** Two functions both parse a config file (10 lines each). Sharing adds coordination cost. If unlikely to change, duplicating may be simpler.

### Architecture Preferences

- **Small, focused functions** over large monolithic ones
- **Loosely coupled components** with tight APIs
- **Clear boundaries** between modules

---

## Refactoring Safely

If a refactoring fails or creates new problems:
1. **Revert your work** — stay out of broken states
2. **Proceed in small stages** — one change at a time
3. **Add debugging/logging code** to verify each step
4. **Test after each stage** before moving to the next
