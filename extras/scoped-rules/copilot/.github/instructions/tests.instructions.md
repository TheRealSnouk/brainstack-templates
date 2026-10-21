---
applyTo: "**/*.test.ts,**/*.test.tsx"
---

# Test rules
- Use the existing test helpers in tests/helpers/ instead of new mocks
- One behavior per test, named "does X when Y"
- No network calls in unit tests
