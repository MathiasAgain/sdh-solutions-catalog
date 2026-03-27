# Orkla Data & Analytics — Solutions Catalog

## What This Is
Customer-facing microsite for an internal Orkla team offering **data & analytics solutions** to portfolio companies and business units. The flagship offering unifies fragmented commercial data into trusted, decision-ready views. Deployed via GitHub Pages.

- **Live**: https://mathiasagain.github.io/solutions-catalog/
- **Repo**: https://github.com/MathiasAgain/solutions-catalog
- **Branch**: `master`
- **Deploy**: Auto via `.github/workflows/pages.yml` on push

## Files

| File | Purpose | Audience |
|------|---------|----------|
| `index.html` | Landing microsite — two-card entry point | Everyone |
| `solutions-overview.html` | Solutions Overview — challenge, outcomes, delivery model, tiers, investment | Business stakeholders, sponsors |
| `engagement-guide.html` | Engagement Guide — effort estimates, interactive planning tools, starter packs, roadmap | Business planners, project sponsors |

## Key Context

### Who We Are
Internal Orkla team (not external vendors). We hand over everything — code, data, infrastructure. No licensing model. Our edge is the **Orkla Accelerator**: a continuously evolving toolkit of proven methods refined across every engagement. Each customer gets a copy; we keep the evolving version.

### Delivery Model
- **Orkla Accelerator** — our toolkit, forked for each engagement (matching, processing, quality)
- **Business Rules & Configuration** — customer-owned (source definitions, matching rules, KPI formulas)
- **Infrastructure** — customer-owned environment, all data stays with the customer

### Engagement Types
- **Build** — new deployment (project engagement)
- **Upgrade** — apply latest accelerator improvements
- **Support** — optional retainer for managed ops
- **Expand** — new use cases (analytics, automation, additional sources)

## Design System

### Colors (Orkla-branded)
```
--navy:    #7E0626   (Orkla burgundy — primary brand color)
--navy2:   #5A0419   (darker burgundy — gradients)
--teal:    #0D7C66   (Tier 1)
--blue:    #2E5090   (Tier 2)
--purple:  #6B4FA0   (Tier 3)
--amber:   #C17817   (add-ons, infrastructure)
--bg:      #FAF8F6   (warm off-white background)
--line:    #E6DED6   (warm border)
```

### Tier Colors (consistent across both docs)
- Tier 1 Foundation → **teal**
- Tier 2 Multi-Source → **blue**
- Tier 3 Enterprise → **purple**
- Currency & Fiscal Overlay → **amber** (add-on, NOT "Tier 4")

## Canonical Numbers

### Tiers
| Tier | Hours | Timeline | Platform/mo | Eng Support/mo |
|------|-------|----------|-------------|----------------|
| Foundation | 180–220h | ~5.5 weeks | $50–300 | 8–20h |
| Multi-Source | 290–685h | 9–14 weeks | $150–600 | 16–40h |
| Enterprise | 820–1,900h | 27–36+ weeks | $400–1,500 | 40–120h |

### Add-Ons
| Add-On | Hours | Monthly |
|--------|-------|---------|
| Power BI Reports | 40–80h | $20–80 |
| Advanced Quality & Alerting | 30–60h | $20–80 |
| Business Review Portal | 60–120h | $30–100 |
| Historical Tracking | 30–50h | +$10–40 |
| Additional Data Source | 40–85h/src | +$30–100 |
| Currency & Fiscal Overlay | 120–320h | $50–200 |
| Data Integration Layer | 40–80h | $30–100 |
| Automated Anomaly Detection | 40–80h | $20–80 |

**Important**: If you change a number, update it in BOTH HTML files. The same values appear in tier cards, investment tables, recommendation engines, and effort breakdowns.

## Solutions Overview Section Order
Deliberate narrative flow — do not rearrange without reason:
1. Hero
2. Challenge (FMCG-specific pain: sell-in/sell-out, distributor formats, promotional reconciliation)
3. **Outcomes** (what life looks like after unification)
4. **Tiers** (scope levels with deliverables list)
5. **Delivery Model** (why us — the accelerator, full handover)
6. Add-Ons
7. Timeline (Gantt)
8. Investment (cost table)
9. Recommendation Engine
10. CTA

**Removed**: Architecture diagram section (saved for future internal technical twin)

## Interactive Tools
Both docs have JavaScript-powered tools. Keep logic in sync:
- **Tier Recommendation Engine** — 4-question scoring (sources, history, governance, timeline). Same logic in both files.
- **Business Case Calculator** — Engagement Guide only. Conservative defaults (80h, $75/hr, 30% reduction).
- **Readiness Scorecard** — Engagement Guide only. 5-dimension RAG assessment.
- **BU Maturity Radar** — Engagement Guide only. SVG radar chart, score-based wave sequencing.

## Design & Tone Guidelines
- **Business-first language** — no technical jargon (no Bronze/Silver/Gold, no SCD2, no crosswalks, no schema contracts, no Delta Live Tables)
- **Orkla branded** — burgundy primary color (#7E0626), warm backgrounds, professional tone
- **Outcome-focused** — lead with what the business gets, not how the technology works
- **No overselling** — confident but understated

## Known Issues / Pending Work

### Placeholder
- `contact@example.com` appears in 3 places (2 files). Replace when real email provided.

### Remaining Content Gaps
- **No competitive positioning** — why us vs SI, MDM tool, or DIY
- **No social proof** — no past engagement references
- **Calculator needs guidance** — benchmark ranges / tooltips for inputs
- **Missing content**: before/after visual, post-handover guide, FAQ section
- **No mobile hamburger nav on Solutions Overview** — nav overflows on small screens
- **No print stylesheet** — documents won't PDF cleanly (fixed navs, hidden reveal elements)
- **Technical twin** — architecture diagram and deep technical content to be developed as separate internal doc

### Resolved (Mar 2026)
- Full rebrand from "SDH / Sales Data Harmonization" to "Orkla Data & Analytics"
- Color palette → Orkla burgundy (#7E0626)
- Architecture diagram → removed from Solutions Overview (for technical twin)
- Mapping workstream, SOW, Risks, Prerequisites → removed from Engagement Guide (for technical twin)
- All technical jargon stripped from both documents
- File renamed: Pitch_Deck → solutions-overview.html
- File renamed: Project_Delivery_Overview → engagement-guide.html
- Repo renamed from sdh-solutions-catalog → solutions-catalog

## Reference Document
`C:\Users\medelm\Sales_Data_Harmonization_Estimate.md` — original effort estimate used as source of truth for Tier 1 numbers. Not in the repo.
