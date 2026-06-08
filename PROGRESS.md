# Progress Log

> **How to use this file:** This is the first thing to read when resuming. It tracks where things stand so any new session can pick up instantly. Update the "Current Status" block whenever something changes, and add a dated entry to the log.

---

## Current Status

- **Current Phase:** Phase 1 — Foundation (Weeks 1-2), nearly complete
- **Target Market:** **Maryland + DC primary** (no volume cap); **Virginia limited** (1-deal/yr cap — see legal-notes.md). Specific zip codes TBD.
- **Lead Strategy:** Solo wholesaling, targeting probate properties
- **Income Goal:** $3K+/month extra income, long-term upside
- **Deals Under Contract:** 0
- **Deals Closed:** 0
- **Buyers List Count:** 0
- **Leads in Pipeline:** 0

---

## Next Up (To-Do)

- [x] Phase 1: Learn core concepts (assignment vs double close, ARV, MAO, 70% rule) — covered
- [x] Phase 1: Research DC/MD/VA wholesale laws — see `legal-notes.md`
- [ ] Phase 1: Be able to explain the full process without notes (practice out loud)
- [ ] Watch 3-5 Wholesaling Inc / Jamil Damji videos
- [ ] Read "If You Can't Wholesale After This" (Todd Fleming)
- [ ] Pick 1-2 target zip codes/neighborhoods (lean MD/DC)
- [ ] Find a real estate attorney — bring the questions in `legal-notes.md`
- [ ] Identify an investor-friendly title company

---

## Tools Built

- `tools/deal-calculator.html` — 70% rule MAO calculator
- `tools/lead-tracker.html` — pipeline tracker (browser localStorage, JSON/CSV export)
- `tools/index.html` — landing page linking tools
- `templates/seller-scripts.md` — outreach + objection scripts
- `templates/buyers-list.md` — cash buyers list template
- `templates/deal-checklist.md` — lead-to-close + legal checklist
- `legal-notes.md` — DC/MD/VA wholesaling laws + attorney questions

## Key Strategic Decisions

- **Market priority shift (2026-06-08):** Lead with **Maryland + DC**, not Virginia. VA's HB 917 caps unlicensed wholesalers at 1 assignment per rolling 12 months — incompatible with a monthly-income goal unless licensed or double-closing. See `legal-notes.md`.
- **Maryland requires written disclosures** (§ 10-715, effective Oct 1, 2025) — contracts must include them.

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


### 2026-06-08 (session 2)
- Worked through Phase 1 learning: assignment vs double close, key terms, equitable interest, the 70% rule with a worked MAO example, and the full 5-step process.
- Researched current DC/MD/VA wholesaling laws — found VA's 1-deal cap (HB 917) and MD's new disclosure law (§ 10-715). Created `legal-notes.md`.
- Strategy shift: lead with Maryland + DC; treat Virginia as limited/licensed-only.
- Remaining Phase 1: practice explaining the process out loud; optional videos/book.
