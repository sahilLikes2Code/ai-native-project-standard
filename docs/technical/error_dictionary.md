# Error Dictionary

**Purpose:** Every error code the app can produce. Stops inconsistent error handling across the codebase.

Format:

```markdown
## ERR_001 — Unauthorized

**Message:** "You do not have permission to perform this action."
**Cause:** Missing or expired auth token
**Resolution:** Redirect to login, clear local session
**HTTP Status:** 401
```
