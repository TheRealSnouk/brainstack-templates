---
trigger: model_decision
description: "Use when writing or reviewing database migrations or schema changes."
---

# Database rules
1. Never drop or rename a column in one release; add the new one first
2. Every migration must be reversible
