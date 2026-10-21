---
paths:
  - "src/api/**/*.ts"
---

# API rules
- Validate every request body at the handler boundary
- Return errors as { code, message }; never throw raw strings
- Every new endpoint gets a test in tests/api/
