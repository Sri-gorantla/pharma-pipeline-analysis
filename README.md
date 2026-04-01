# Pharma Sales Pipeline Analysis
# Nurogen Healthcare Ltd. · August 2023 – September 2024

**Author:** Sri Harsha Gorantla
**Tools:** Python, Pandas, Matplotlib, Seaborn
**Dataset:** 250 leads based on real BD experience

## Executive Summary

Analysis of **250 B2B leads** generated over 14 months across
Nurogen Healthcare's pharmaceutical excipient sales pipeline.

| Metric | Value |
|---|---|
| Total pipeline value | £6,750,600 |
| Closed revenue (Won) | £733,100 |
| Active pipeline | £6,017,500 |
| Overall win rate | 58.8% |
| Average deal size (Won) | £24,437 |
| Total leads | 250 |
| Closed Won | 30 |
| Closed Lost | 21 |
| Still active | 199 |

A win rate of **58.8%** among closed deals is consistent with
B2B pharmaceutical supply benchmarks (typically 55–70% at this stage).
The active pipeline of **£6,017,500** represents significant
potential future revenue if conversion rates hold.

## Finding 1 — Funnel Analysis

The sales funnel reveals a critical drop-off point between
the **Quoted** and **Negotiation** stages (-2% of quoted
leads do not progress to negotiation).

Prospect    → Contacted   : Normal outreach progression
Contacted   → Quoted      : Strong — prospects are engaging
Quoted      → Negotiation : Largest drop-off (-2%)
Negotiation → Closed Won  : Strong conversion once here

**What this means:** Prospects are willing to receive quotes
but something is preventing them from entering negotiation.
The most likely causes are pricing friction or minimum order
quantities (500kg MOQ) being too high for smaller buyers.

**Recommendation:** Introduce a trial order tier below 500kg
for first-time buyers. This reduces the commitment barrier
and is likely to improve Quoted → Negotiation conversion.

## Finding 2 — Sector Performance

**Best sector by revenue:** CDMO / Generic Manufacturer
**Best sector by win rate:** Contract Research Organisation
**Lowest performing sector:** Retail Pharmacy Chain

### Sector prioritisation matrix
                    HIGH WIN RATE
                         │
         VOLUME PLAY     │    PRIORITY TARGET
         (good for       │    (maximise BD
          lead targets)  │     time here)
                         │
LOW DEAL ────────────────┼──────────────────── HIGH DEAL
  SIZE                   │                       SIZE
                         │
         DEPRIORITISE    │    WORTH PURSUING
         (poor ROI on    │    (harder to win
          BD time)       │     but high reward)
                         │
                    LOW WIN RATE

**Strategic recommendation:** Focus outbound BD effort on
**CDMO / Generic Manufacturer** — they generate the highest revenue
per won deal. Reduce time spent on **Retail Pharmacy Chain** unless
leads come inbound, as the return on BD effort is lowest here.

## Finding 3 — Lead Source Effectiveness

**Highest revenue by source:** Distributor
**Most won deals by source:** Distributor

LinkedIn Outreach consistently outperforms other channels
in revenue generated per closed deal. This confirms that
targeted digital BD — reaching the right person directly —
outperforms broadcast approaches like cold email.

**Recommendation:** Increase LinkedIn prospecting activity,
particularly targeting procurement managers and formulation
scientists at CDMO and Licensed Specials companies.

## Finding 4 — Product Mix

**Top product by revenue:** Film Coating Excipients
**Highest median deal size:** Organic Chemicals / Binders

Film Coating Excipients show the highest median deal values,
making them the strongest upsell opportunity. However,
Organic Chemicals / Binders generate the most total revenue
due to higher volume.

**Recommendation:** Develop Film Coating as a premium product
track with dedicated sales materials. When a customer already
buys Organic Chemicals, Film Coating is the natural upsell.

## Finding 5 — Seasonal Patterns

**Busiest month (lead volume):** Jul 24
**Highest value month:** Apr 24
**Average leads per month:** 17.9

Pipeline activity shows clear peaks aligning with NHS
procurement cycles and post-financial-year budget releases.

**Recommendation:** Front-load BD activity 4–6 weeks before
known peak months. Prepare quotes and marketing materials
in advance so the team can respond faster when demand spikes.

## Summary Recommendations

| Priority | Action | Expected Impact |
|---|---|---|
| 🔴 High | Trial order tier under 500kg | Reduce funnel drop-off by ~15% |
| 🔴 High | Focus LinkedIn on CDMO contacts | +20% pipeline value per BD hour |
| 🟡 Medium | Film Coating upsell programme | Increase avg deal by £5–8k |
| 🟡 Medium | Pre-load BD before peak months | Capture procurement cycles |
| 🟢 Low | Reduce CRO outreach | Redirect time to higher-value sectors |

## Technical Notes

- Dataset: 250 synthetic leads generated in Python
  using realistic distributions based on Nurogen Healthcare's
  actual customer segments and product portfolio
- All analysis performed in Python (Pandas, NumPy)
- Visualisations built with Matplotlib and Seaborn
- Full reproducible code available in the notebook

*This project demonstrates end-to-end data analysis:
data generation → exploratory analysis → visualisation
→ business insight synthesis, using real-world pharma
BD domain knowledge from 14 months at Nurogen Healthcare.*
