# Customer Segmentation Analysis — RFM Model
## Nurogen Healthcare Ltd.

**Author:** Sri Harsha Gorantla
**Method:** RFM Analysis (Recency, Frequency, Monetary)
**Tools:** Python, SQLite, Pandas, Matplotlib, Seaborn
**Dataset:** 250 customers from pharma excipient pipeline

## What is RFM Segmentation?

RFM is an industry-standard customer segmentation method
used across pharma, retail, finance and SaaS companies.
Every customer is scored 1–4 on three dimensions:

| Dimension | What it measures | Score 4 = |
|---|---|---|
| Recency (R) | How recently did they engage? | Very recent |
| Frequency (F) | How many interactions? | Highly engaged |
| Monetary (M) | How much are they worth? | High deal value |

Combined scores classify each customer into a named segment
that drives specific BD and account management actions.

---

## Segment Overview

| Segment | Customers | % of Total | Avg Deal Value |
|---|---|---|---|
| Champion | 18 | 7.2% | £60,139 |
| Big Spender | 24 | 9.6% | £54,067 |
| At Risk | 18 | 7.2% | £48,406 |
| Loyal Customer | 30 | 12.0% | £41,100 |
| Promising | 61 | 24.4% | £18,936 |
| Needs Attention | 66 | 26.4% | £18,467 |
| Lost | 33 | 13.2% | £15,327 |

**Total pipeline value across all segments:**
£7,364,100

---

## Finding 1 — Champions (18 customers,
7.2% of base)

Champions score 4 on all three RFM dimensions —
they are the most recent, most engaged, and highest
value customers in the pipeline.

**Champion pipeline value:** £1,082,500

**Dominant sector:** CDMO / Generic Manufacturer

These customers require white-glove account management.
They should never be left without contact for more than
30 days. Priority actions:

- Assign dedicated account manager
- Offer early access to new product lines
- Request referrals and testimonials
- Invite to product development feedback sessions

---

## Finding 2 — At Risk Customers (18 customers)

At Risk customers were previously high value but their
recency score has dropped — they are going cold.

**At Risk pipeline value:** £871,300

This represents revenue that is actively being lost.
Without intervention, At Risk customers typically
convert to Lost within 60–90 days.

**Recommended re-engagement actions:**
- Personal outreach from senior BD within 2 weeks
- Offer a pricing review or loyalty discount
- Share new product availability relevant to their sector
- Invite to site visit or technical consultation

**Priority:** Urgent — time-sensitive revenue recovery.

---

## Finding 3 — Promising Customers (61 customers)

Promising customers are recent and engaged but have
not yet reached high monetary scores. These represent
the highest growth potential in the pipeline.

**Recommended nurture actions:**
- Increase contact frequency to 2x per month
- Send targeted product samples or technical data sheets
- Introduce to Film Coating Excipients as upsell
- Invite to webinars or industry events

---

## Finding 4 — RFM Score Patterns

**Overall average scores:**

| Dimension | Average Score | Interpretation |
|---|---|---|
| Recency | 2.49 / 4.00 | Needs improvement |
| Frequency | 2.49 / 4.00 | Needs improvement |
| Monetary | 2.49 / 4.00 | Needs improvement |

The heatmap reveals that high Recency (R=4) customers
tend to have higher Monetary scores regardless of
Frequency — suggesting that recently re-engaged
customers quickly become higher spenders.

This supports prioritising re-engagement campaigns
over pure volume prospecting.

---

## Strategic Recommendations

| Priority | Segment | Action | Expected Outcome |
|---|---|---|---|
| 🔴 Urgent | At Risk | Personal senior outreach | Recover £871,300 pipeline |
| 🔴 High | Champion | Dedicate account manager | Protect £1,082,500 revenue |
| 🟡 Medium | Promising | Increase contact frequency | Convert to Loyal/Champion |
| 🟡 Medium | Needs Attention | Targeted email campaign | Re-activate engagement |
| 🟢 Low | Lost | Quarterly check-in only | Minimal BD resource |

---

## Technical Approach

**Database:** SQLite (3 normalised tables —
customers, deals, interactions)

**SQL techniques used:**
- Multi-table JOINs (2 and 3 table)
- Aggregate functions (COUNT, SUM, AVG)
- CASE WHEN conditional logic
- Common Table Expressions (CTEs)
- NTILE() window function for score banding
- IS NOT NULL filtering
- HAVING clause for group filtering

**Segmentation logic:**
Each customer scored 1–4 per dimension using NTILE(4).
Segments assigned via nested CASE WHEN on combined scores.

---

## Project Files
```
pharma-pipeline-analysis/
├── data/
│   ├── leads.csv              ← source data (from P1)
│   └── rfm_segments.csv       ← RFM scored customers
├── charts/
│   ├── chart5_segment_distribution.png
│   ├── chart6_segment_value.png
│   └── chart7_rfm_heatmap.png
└── notebooks/
    └── 02_customer_segmentation_sql.ipynb
```

---

*This project demonstrates SQL database design,
multi-table querying, window functions, and RFM
segmentation — applied to real pharma BD experience
from 14 months at Nurogen Healthcare Ltd.*
