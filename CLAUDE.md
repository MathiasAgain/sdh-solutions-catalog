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
| `Sales_Data_Harmonization_Pitch_Deck.html` | Executive pitch — value prop, tiers, delivery model, architecture, investment | Decision-makers, sponsors |
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
- Tier 3 PortCo Convergence → **purple**
- Currency & Fiscal Overlay → **amber** (add-on, NOT "Tier 4")

## Canonical Numbers

### Tiers
| Tier | Hours | Timeline | Platform/mo | Eng Support/mo |
|------|-------|----------|-------------|----------------|
| Foundation | 180–220h | ~5.5 weeks | $300–1,200 | 8–20h |
| Multi-Source | 290–685h | 9–14 weeks | $800–3,500 | 16–40h |
| PortCo Convergence | 820–1,900h | 27–36+ weeks | $3,000–15,000 | 40–120h |

### Add-Ons
| Add-On | Hours | Monthly |
|--------|-------|---------|
| Power BI Semantic Model | 40–80h | $200–600 |
| Advanced DQ & Alerting | 30–60h | $100–400 |
| Stewardship Portal | 60–120h | $150–500 |
| SCD2 Historical Tracking | 30–50h | +$50–150 |
| Additional Source | 40–85h/src | +$100–400 |
| Data Lineage & Catalog | 40–80h | $100–400 |
| Currency & Fiscal Overlay | 120–320h | $200–800 |
| FinOps Package | 20–40h | Net savings |
| Training & Enablement | 20–40h | One-time |

**Important**: If you change a number, update it in BOTH HTML files. The same values appear in tier cards, investment tables, recommendation engines, and effort breakdowns.

## Pitch Deck Section Order
Deliberate narrative flow — do not rearrange without reason:
1. Hero
2. Problem (pain points)
3. **Tiers** (what you can buy)
4. **Delivery Model** (why us — the accelerator)
5. **Architecture** (how it works — for the curious)
6. Add-Ons
7. Timeline (Gantt)
8. Investment (cost table)
9. Recommendation Engine
10. CTA

## Interactive Tools
Both docs have JavaScript-powered tools. Keep logic in sync:
- **Tier Recommendation Engine** — 4-question scoring (sources, SCD2, governance, timeline). Same logic in both files.
- **Business Case Calculator** — Overview only. Conservative defaults (80h, $75/hr, 30% reduction).
- **Readiness Scorecard** — Overview only. 5-dimension RAG assessment.
- **BU Maturity Radar** — Overview only. SVG radar chart, score-based wave sequencing.

## Known Issues / Pending Work

### Placeholder
- `contact@example.com` appears in 3 places (2 files). Replace when real email provided.

### Content Gaps (from deep review, not yet addressed)
1. **Problem section too generic** — needs FMCG-specific pain (sell-in vs sell-out, distributor format variance, promotional reconciliation)
2. **No outcome framing** — missing "what life looks like after harmonization"
3. **Tiers lead with tech, not business value** — should lead with outcomes ("one set of numbers for commercial reviews")
4. **Delivery model claims unsubstantiated** — "5 weeks vs 4 months" needs evidence or softening
5. **No competitive positioning** — why us vs SI, MDM tool, or DIY
6. **Add-on descriptions feature-focused** — should be benefit-focused
7. **No social proof** — no past engagement references
8. **"Tier 4" label confusing** — Currency overlay is an add-on, not a tier. Consider dropping "Tier 4" framing in Overview.
9. **Calculator needs guidance** — benchmark ranges / tooltips for inputs
10. **Missing content**: deliverables list, before/after visual, post-handover guide, FAQ section
11. **Federated Autonomy section operationally thin** — needs detail on what each wave actually delivers
12. **No mobile hamburger nav on Pitch Deck** — nav overflows on small screens
13. **No print stylesheet** — documents won't PDF cleanly (fixed navs, hidden reveal elements)

## Architecture Diagram
The Pitch Deck has a full SVG blueprint-style architecture diagram (`id="architecture"`). It uses:
- SVG `<animateMotion>` on defined `<path>` elements for data flow particles
- Five zones: Data Sources → Ingestion → Lakehouse → Serving → Consumption
- Dark background (#0F1B2D) with grid overlay
- Technology labels on every node

Do NOT replace with CSS grid boxes — user explicitly rejected that style as "looking like PowerPoint."

## Reference Document
`C:\Users\medelm\Sales_Data_Harmonization_Estimate.md` — original effort estimate used as source of truth for Tier 1 numbers. Not in the repo.
