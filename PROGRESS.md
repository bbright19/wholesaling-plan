# Progress Log

> **How to use this file:** This is the first thing to read when resuming. It tracks where things stand so any new session can pick up instantly. Update the "Current Status" block whenever something changes, and add a dated entry to the log.

---

## Current Status

- **Current Phase:** Phase 1 — Foundation (Weeks 1-2)
- **Target Market:** DC / MD / VA area (specific zip codes TBD)
- **Lead Strategy:** Solo wholesaling, targeting probate properties
- **Income Goal:** $3K+/month extra income, long-term upside
- **Deals Under Contract:** 0
- **Deals Closed:** 0
- **Buyers List Count:** 0
- **Leads in Pipeline:** 0

---

## Next Up (To-Do)

- [ ] Phase 1: Learn core concepts (assignment vs double close, ARV, MAO, 70% rule)
- [ ] Phase 1: Research DC/MD/VA wholesale laws
- [ ] Phase 1: Be able to explain the full process without notes
- [ ] Pick 1-2 target zip codes/neighborhoods
- [ ] Find a real estate attorney to review contracts
- [ ] Identify an investor-friendly title company

---

## Tools Built

- `tools/deal-calculator.html` — 70% rule MAO calculator
- `tools/lead-tracker.html` — pipeline tracker (browser localStorage, JSON/CSV export)
- `tools/index.html` — landing page linking tools
- `templates/seller-scripts.md` — outreach + objection scripts
- `templates/buyers-list.md` — cash buyers list template
- `templates/deal-checklist.md` — lead-to-close + legal checklist

## Tech / Infra Decisions

- **Cloud (S3/DynamoDB/Lambda):** Decided to HOLD OFF until after first deal or until browser storage causes real friction. Lead data currently lives in browser localStorage — back up via "Export JSON" regularly.
- When ready to go cloud: DynamoDB (leads) + Lambda + API Gateway + S3/CloudFront (host tools) + Cognito (auth) + EventBridge (automated follow-up). Est. <$5/mo at this scale.

---

## Session Log

### 2026-06-08
- Set up GitHub repo and pushed the full learning plan.
- Built deal calculator, lead tracker, and template docs (scripts, buyers list, deal checklist).
- Discussed cloud architecture — decided to stay browser-based for now, revisit after first deal.
- Created this PROGRESS.md tracker.
