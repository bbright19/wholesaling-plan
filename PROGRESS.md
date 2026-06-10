# Progress Log

> **How to use this file:** This is the first thing to read when resuming. It tracks where things stand so any new session can pick up instantly. Update the "Current Status" block whenever something changes, and add a dated entry to the log.

---

## ▶️ START HERE TOMORROW — Next Steps (Phase 2)

1. **Tighten to a real comp set** — in `comp-analyzer.html`, pick a representative subject sqft (e.g. a 1,400–1,800 sqft SFR you'd actually chase), click **"Select similar (±20% sqft)"**, and uncheck the renovated/condition outliers. Goal: get the $/sqft range to tighten from $100–$452 down to a believable band, and note the **renovated** $/sqft (that's your ARV basis).
2. **Drive the target area** — note distressed properties (overgrown yards, boarded windows, code notices, full mailboxes) and where the good/rough block lines are. Log them in `comps-log.md` (Driving for Dollars table).
3. **Ask 1–2 cash buyers for their per-sqft rehab budgets** in 20748/20745 — start the "buyer repair cheat sheet" so your MAO math uses real (conservative) repair numbers.

*Resume cue: "Pull up my wholesaling repo, read PROGRESS.md, let's do the next steps."*

**Baseline locked (2026-06-10):** 20748 SFR sold ~**$225/sqft median** (avg $243, range $100–$452 across 42 comps). See `market-research/comps-log.md`.

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
- [~] Phase 2: Run comps + estimate ARV (milestone) — **market baseline done** (20748 SFR ~$225/sqft median, 42 comps). Next: tighten to a similar-sqft comp set + isolate renovated $/sqft for true ARV.
- [ ] Phase 2: Drive the target area, note distressed properties
- [ ] Watch 3-5 Wholesaling Inc / Jamil Damji videos
- [ ] Read "If You Can't Wholesale After This" (Todd Fleming)
- [ ] Find a real estate attorney — bring the questions in `legal-notes.md`
- [ ] Identify an investor-friendly title company

---

## Tools Built

- `tools/deal-calculator.html` — 70% rule MAO calculator
- `tools/comp-analyzer.html` — comp/ARV estimator ($/sqft averaging across sold comps); **imports Redfin "Download All" CSV** (drag/drop), shows sold date + beds/baths + type per comp, auto-selects comps within ±20% of subject sqft, and reports avg + median $/sqft
- `tools/lead-tracker.html` — pipeline tracker (browser localStorage, JSON/CSV export)
- `tools/weekly-scorecard.html` — weekly leading-indicator tracker (contacts/convos/offers) with trend + "is it working?" signal
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


### 2026-06-10
- Honest gut-check convo (prompted by cousin/RE agent): wholesaling is relationship- and consistency-driven, not part-time/on-off friendly; dropshipping considered but rejected (same consistency demands, no durable asset, no local moat). Decision: stick with wholesaling IF consistent.
- Key self-insight from user: "I can be consistent if the process is working." Reframed "working" = leading indicators (activity), not lagging (money). First deal can take 3-6+ months, so we need weekly proof-of-progress to sustain consistency.
- Built `tools/weekly-scorecard.html` — logs weekly leads/contacts/conversations/offers/contracts, shows trend chart + week-over-week deltas + an "is it working?" signal based on activity. This is the feedback loop that fixes the consistency risk.


### 2026-06-10 (strategy lock)
- Reviewed an automated/co-wholesaling plan (mass SMS + 50/50 partner). Flagged mass cold-SMS as a TCPA legal landmine; co-wholesaling partner idea was strong but carries circumvention risk.
- DECISION: User chose to go SOLO. Rationale: if solo works, upside is huge — keeps 100% of fee (~$10K avg vs ~$5K split), owns full acquisition + disposition skillset, no partner risk, builds the real long-term business.
- Solo approach within a full-time AWS job = hardest path; mitigate with async-friendly lead gen (direct mail + weekend driving for dollars + probate records), evening/weekend seller calls via a separate Google Voice line, NO cold mass-SMS (legal risk), and the weekly scorecard to confirm the process is working through the pre-money stretch.
- Confirmed market: base 22315 (Kingstowne), target PG County MD 20748 + 20745. Back to Phase 2 Step 2 (run comps on 10 sales).



### 2026-06-10 (comp-analyzer upgrade)
- Confirmed Redfin's native CSV export works: filter to Sold + last 3 months + area, scroll to bottom of results, click "(Download All)". User successfully downloaded a CSV.
- Upgraded `tools/comp-analyzer.html` to import the Redfin CSV directly (drag/drop or click). Parses Address/Price/Square Feet/$ per sqft/Sold Date/Beds/Baths/Property Type, handles quoted addresses with commas, sorts newest-sold first, and skips rows missing price or sqft.
- Imported comps start UNCHECKED so 300 rows don't pollute the average. Added helpers: "Select similar (±20% sqft)", Check all, Uncheck all, Clear all. Result now shows both average and median $/sqft (median is more robust when the spread is wide).
- Next: actually run the Phase 2 milestone — import a real 20748/20745 sold CSV, pick a subject, select 3-5 tight comps, and lock an ARV.



### 2026-06-10 (comp-analyzer + first market baseline)
- Confirmed Redfin native CSV export works ("Download All" at bottom of sold results). User downloaded a real 20748 sold CSV.
- Shipped two comp-analyzer upgrades (both merged to main):
  - PR #1: Redfin CSV import (drag/drop), parses address/price/sqft/$ per sqft/sold date/beds/baths/type, robust quoted-comma parsing, avg + median $/sqft.
  - PR #2: On import, auto-check ONLY single-family comps with complete data; Townhouses, Condos, Land, and rows with any blank field stay unchecked (matches SFR-focus strategy + skips junk data).
- Product focus decision: **lead with SFR**, townhomes only opportunistically (low/no HOA + strong spread). Rationale: matches probate stock, wider buyer pool, no HOA closing friction.
- **First market baseline (20748 SFR):** 42 sold comps → median **$225/sqft**, avg $243, range $100–$452. Logged in `market-research/comps-log.md`. Takeaways: median is the trustworthy number; wide spread is mixed condition/size; $/sqft inversely tracks size; median ≠ ARV (ARV = renovated value, lean to upper cluster).
- Noted: image attachments in chat don't always reach Kiro — fall back to pasting numbers/text.
- Next session: tighten to a similar-sqft comp set, isolate renovated $/sqft (true ARV basis), start driving-for-dollars + buyer rehab-budget asks.
