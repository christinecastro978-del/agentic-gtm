# Setup

Date: 2026-10-08

## Target domains (owner-supplied)
1. aisle.com (https://aisle.com/)
2. botcity.dev (product page: https://botcity.dev/sentinel)

Both domains confirmed unchanged on 2026-10-08 (no earlier choice was replaced). Researched from owner-pasted official page text: targets/aisle.com.md, targets/botcity.dev.md. List: TARGETS.md.

## Bootstrap
Command (run from code/): `python3 -B gtm.py bootstrap --company-brief ../company-motion/COMPANY.md`
Exit code: 0

```json
{
  "setup_ready": true,
  "company_brief": "/home/user/agentic-gtm-workshop/company-motion/COMPANY.md",
  "python": {"executable": "/usr/bin/python3", "version": [3, 13, 16]},
  "python_receipt": "/home/user/agentic-gtm-workshop/company-motion/.runtime.json",
  "created": ["AUTHORITY.md", "AGENTS.md"],
  "preserved": [],
  "outreach": "paused; no authority added",
  "database_writes": 0,
  "provider_writes": 0,
  "next": "Review your company brief. Continue only when you choose the next exercise.",
  "stop": true
}
```

Saved Python for later commands and standalone scripts: /usr/bin/python3 (3.13.16), recorded in .runtime.json.
Outreach, paid research, gifts, publishing, ads and schedules: paused (AUTHORITY.md).
