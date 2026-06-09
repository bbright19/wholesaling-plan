# Progress Log

> **How to use this file:** This is the first thing to read when resuming. It tracks where things stand so any new session can pick up instantly. Update the "Current Status" block whenever something changes, and add a dated entry to the log.

---

## ▶️ START HERE TOMORROW — Next 3 Steps (Phase 2)

1. **Pick your target area** — choose 1-2 MD/DC zip codes or neighborhoods to focus on.
2. **Run comps on 10 recent sales** — use `tools/comp-analyzer.html`; pull sold comps from Zillow/Redfin, calc $/sqft, estimate ARV. This is the Phase 2 milestone.
3. **Drive the target area** — note distressed properties (overgrown yards, boarded windows, code notices, full mailboxes) and where the good/rough block lines are.

*Resume cue: "Pull up my wholesaling repo, read PROGRESS.md, let's do the next 3 steps."*

---

## Current Status

- **Current Phase:** Phase 2 — Know Your Market (Weeks 3-4)
- **Target Market:** **PG County, MD** — 20748 (Temple Hills/Hillcrest Heights/Marlow Heights) + 20745 (Glassmanor/older Oxon Hill). Older modest stock near MGM National Harbor, avoiding upscale waterfront. ~$250K-$400K band, close to home (22315). VA stays limited (1-deal cap).
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
- [x] Phase 2: Pick target area — 20748 + 20745 (older pockets near MGM, PG County MD)
- [ ] Phase 2: Run comps + estimate ARV on 10 recent sales (milestone)
- [ ] Phase 2: Drive the target area, note distressed properties
- [ ] Watch 3-5 Wholesaling Inc / Jamil Damji videos
- [ ] Read "If You Can't Wholesale After This" (Todd Fleming)
- [ ] Find a real estate attorney — bring the questions in `legal-notes.md`
- [ ] Identify an investor-friendly title company

---

## Tools Built

- `tools/deal-calculator.html` — 70% rule MAO calculator
- `tools/comp-analyzer.html` — comp/ARV estimator ($/sqft averaging across sold comps)
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


### 2026-06-08 (session 3)
- Started Phase 2 (Know Your Market). Covered: retail vs investor price, what ARV is, the comp method ($/sqft from 3-5 tight sold comps), rough repair estimating by condition, local property types, and driving the area.
- Discussed why wholesalers use free comps instead of paid appraisals (speed, volume economics, ARV vs as-is, buyer does final diligence).
- Built `tools/comp-analyzer.html` — enter sold comps, auto-calc $/sqft, average, and estimate ARV; flags wide spreads/outliers.
- Next: practice on 10 real sales in target MD/DC area to hit the Phase 2 milestone.


### 2026-06-08 (session 3 cont.)
- Covered deal protection: anti-circumvention rules and contract exclusivity (ratified contract = time-limited exclusive right to buy, contingent on performance). Saved to deal-checklist.md and legal-notes.md.
- Paused here. Saved next 3 Phase 2 steps for tomorrow (see START HERE TOMORROW block).
