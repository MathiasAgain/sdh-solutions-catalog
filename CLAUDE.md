# SDH Solutions Catalog

## What This Is
Customer-facing microsite for an internal consulting team offering **Sales Data Harmonization** services to FMCG portfolio companies and business units. Built on Databricks Lakehouse (Medallion Architecture). Deployed via GitHub Pages.

- **Live**: https://mathiasagain.github.io/sdh-solutions-catalog/
- **Repo**: https://github.com/MathiasAgain/sdh-solutions-catalog
- **Branch**: `master`
- **Deploy**: Auto via `.github/workflows/pages.yml` on push

## Files

| File | Purpose | Audience |
|------|---------|----------|
| `index.html` | Landing microsite — two-card entry point | Everyone |
| `Sales_Data_Harmonization_Pitch_Deck.html` | Solutions Overview — challenge, outcomes, delivery model, tiers, architecture, investment | Decision-makers, sponsors |
| `Sales_Data_Harmonization_Project_Delivery_Overview.html` | Technical deep-dive — effort breakdowns, interactive tools, SOW, risks, prerequisites | Project managers, data leads |

## Key Context

### Who We Are
Internal consultants (not external vendors). We hand over everything — code, data, infrastructure. No licensing model. Our edge is the **inner-source accelerator**: a continuously evolving library of matching algorithms, pipeline templates, DQ rules, and source connectors refined across every engagement. Each customer gets a fork; we keep the living version.

### Delivery Model
- **SDH Accelerator** — maintained by us, forked for customer (matching engine, pipeline factory, DQ framework)
- **Configuration & Logic** — customer-owned in their Git repo (source schemas, matching rules, KPI definitions)
- **Infrastructure** — customer-owned Databricks workspace, Azure storage, all data

### Engagement Types
- **Build** — new deployment (project engagement)
- **Upgrade** — apply latest accelerator improvements
- **Support** — optional retainer for managed ops
- **Expand** — new use cases (analytics, ML, automation)

## Design System

### Colors
```
--navy:    #1B2A4A   (primary dark)
--teal:    #0D7C66   (Tier 1, ingestion, CTAs)
--blue:    #2E5090   (Tier 2, processing)
--purple:  #6B4FA0   (Tier 3, governance)
--amber:   #C17817   (add-ons, infrastructure, warnings)
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
| Power BI Semantic Model | 40–80h | $20–80 |
| Advanced DQ & Alerting | 30–60h | $20–80 |
| Stewardship Portal | 60–120h | $30–100 |
| SCD2 Historical Tracking | 30–50h | +$10–40 |
| Additional Source | 40–85h/src | +$30–100 |
| Currency & Fiscal Overlay | 120–320h | $50–200 |
| API / Data Product Layer | 40–80h | $30–100 |
| Automated Anomaly Detection | 40–80h | $20–80 |

**Removed add-ons (Feb 2026)**: FinOps (folded into support retainer), Training (included in all tiers), Data Lineage & Catalog (included in Tier 3).

**Important**: If you change a number, update it in BOTH HTML files. The same values appear in tier cards, investment tables, recommendation engines, and effort breakdowns.

## Solutions Overview Section Order
Deliberate narrative flow — do not rearrange without reason:
1. Hero
2. Challenge (FMCG-specific pain: sell-in/sell-out, distributor formats, promotional reconciliation)
3. **Outcomes** (what life looks like after harmonization)
4. **Delivery Model** (why us — the accelerator)
5. **Tiers** (scope levels with deliverables list)
6. **Architecture** (behind expand/toggle — for the curious)
7. Add-Ons
8. Timeline (Gantt)
9. Investment (cost table)
10. Recommendation Engine
11. CTA

## Interactive Tools
Both docs have JavaScript-powered tools. Keep logic in sync:
- **Tier Recommendation Engine** — 4-question scoring (sources, SCD2, governance, timeline). Same logic in both files.
- **Business Case Calculator** — Overview only. Conservative defaults (80h, $75/hr, 30% reduction).
- **Readiness Scorecard** — Overview only. 5-dimension RAG assessment.
- **BU Maturity Radar** — Overview only. SVG radar chart, score-based wave sequencing.

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

### Resolved (Feb 2026)
- Problem section → FMCG-specific (sell-in/sell-out, distributor formats, promotional reconciliation)
- Outcome framing → new "What You Get" section added
- Tiers → deliverables list added per tier
- "Tier 4" label → removed, now "Optional Overlay" in Overview
- Deliverables list → added to each tier card
- Section order → Challenge → Outcomes → Delivery → Tiers → Architecture (toggle) → ...
- "PortCo Convergence" → renamed to "Enterprise"
- "Business Hours /mo" → renamed to "Your Team's Time /mo"
- Gantt jargon → "Conformance" → "Matching", "Harden & Ops" → "Quality & Testing", "UAT & Handover" → "Testing & Handover"
- Architecture diagram → behind expand/toggle
- Landing page → updated numbers, jargon removed, "Pitch Deck" → "Solutions Overview"

## Architecture Diagram
The Pitch Deck has a full SVG blueprint-style architecture diagram (`id="architecture"`). It uses:
- SVG `<animateMotion>` on defined `<path>` elements for data flow particles
- Five zones: Data Sources → Ingestion → Lakehouse → Serving → Consumption
- Dark background (#0F1B2D) with grid overlay
- Technology labels on every node

Do NOT replace with CSS grid boxes — user explicitly rejected that style as "looking like PowerPoint."

## Reference Document
`C:\Users\medelm\Sales_Data_Harmonization_Estimate.md` — original effort estimate used as source of truth for Tier 1 numbers. Not in the repo.
