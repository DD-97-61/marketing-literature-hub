# Match History — Cumulative Tracking

*Last updated: 2026-04-18*

---

## Active Matches

| ID | Title | Score | Status | Target Journal | First Seen | Last Updated | Notes |
|----|-------|-------|--------|---------------|------------|--------------|-------|
| M-001 | Visual Brand Aesthetic Style Dimensions (CLIP + NIMA, Chinese tea brands) | 14/15 | ACTIVE | JBR → IJRM | 2026-04-18 | 2026-04-18 | HIGH PRIORITY. Gap from Liu et al. 2020 (Marketing Science) + Li et al. 2025 (JBR). Can share data pipeline with M-003 and M-004. |
| M-002 | NIMA Aesthetic Scoring → Brand Engagement Across Product Categories | 14/15 | ACTIVE | JBR → Psychology & Marketing | 2026-04-18 | 2026-04-18 | HIGH PRIORITY. Pre-existing Kaggle/Dataverse datasets reduce entry barrier. Most feasible standalone study. |
| M-003 | CLIP Visual Positioning Maps: Competitive Aesthetic Differentiation | 14/15 | ACTIVE | JMR / Marketing Science → JBR | 2026-04-18 | 2026-04-18 | HIGH PRIORITY. Highest theoretical ambition of the set. Needs strong theoretical framing to reach Marketing Science. |
| M-004 | Brand Visual Consistency (CLIP Pairwise Similarity) → Engagement | 13/15 | ACTIVE | IJRM → JBR | 2026-04-18 | 2026-04-18 | HIGH PRIORITY. Can be run as extension of M-001 data collection. Reverse causality risk needs IV strategy. |
| M-005 | Eastern Aesthetic Element Detection → Brand Attitudes (Guochao) | 11/15 | ACTIVE | JBR → Journal of International Marketing | 2026-04-18 | 2026-04-18 | CONDITIONAL method (GPT-4V prompt classification). Conceptual clarity needed before proceeding. |
| M-006 | Temporal Visual Brand Evolution (CLIP Time-Series) | 9/15 | WATCHLIST | Marketing Science → JMR | 2026-04-18 | 2026-04-18 | Blocked by historical data availability. Revisit if historical platform data access improves. |
| M-007 | Cross-Industry Visual Strategy Comparison (Tea vs. Hospitality) | 10/15 | HOLD | JBR → JRCS | 2026-04-18 | 2026-04-18 | Best pursued as extension of M-001 or M-003 rather than standalone. |

---

## Retired / Abandoned Matches

*None yet.*

---

## Status Legend

| Status | Meaning |
|--------|---------|
| ACTIVE | Viable match; researcher should evaluate for development |
| WATCHLIST | Promising but blocked by data/method gap; monitor monthly |
| HOLD | Lower priority; worth revisiting if circumstances change |
| IN DEVELOPMENT | Researcher has committed to this project |
| ABANDONED | No longer viable (competitive, data unavailable, theory weak) |

---

## Score Change Log

| ID | Date | Old Score | New Score | Reason |
|----|------|-----------|-----------|--------|
| — | — | — | — | — |

---

## Data Collection Synergies

The following matches can share a single data collection effort:

- **Shared Xiaohongshu scrape (tea brands):** M-001, M-003, M-004, M-005
  - Collect once: 25–30 tea brands × ~500 posts each, with images + engagement metadata
  - Run M-001 (aesthetic style), M-003 (positioning maps), M-004 (consistency) from same dataset
  - Add Guochao/non-Guochao brand split for M-005

- **Shared Instagram multi-category scrape:** M-002
  - Independent collection; use Kaggle/Dataverse first to minimize scraping cost

---

*This file is updated by Routine #11 each time a new matching run completes.*
