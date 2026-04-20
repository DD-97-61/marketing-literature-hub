# Working Paper Radar — 2026-04-20

**Scan period:** April 13–20, 2026 (last 7 days)
**Platforms searched:** SSRN (Marketing, Consumer Behavior, Digital Economy eJournals), arXiv (cs.AI, cs.HC, econ.GN), NBER Working Papers, ResearchGate, Google Scholar
**Keyword groups covered:** Branding (A), AI×Brand (B), Internationalization (C), Competitiveness (D), Social Media (E), Methodology (F), Digital Economy (G)

> **Important:** All items below are working papers / preprints. They have **not** undergone peer review. Treat findings as preliminary.

---

## Papers Within Window (April 13–20, 2026)

---

### Socially Fluent, Socially Awkward: Artificial Intelligence Relational Talk Backfires in Commercial Interactions

- **Authors:** Stephanie Kwari Dharmaputri, Anish Nagpal, Greg Nyilasy, Jing Lei (affiliations not publicly listed; cs.HC submission)
- **Platform:** arXiv | **Date posted:** ~April 14, 2026
- **arXiv ID:** [2604.12206](https://arxiv.org/abs/2604.12206) | **Status:** Preprint
- **Research stream:** AI×Brand / Consumer Behavior
- **Abstract summary:** As AI social fluency is integrated into commercial interactions (e.g., OpenAI assistant on Shopify, Klarna, Visa), the paper tests whether relational talk—informal, non-obligatory social communication in transactional exchanges—improves or harms consumer experience. Across four experiments, AI relational talk has a **negative** main effect on satisfaction, mediated by expectancy violation and perceived interaction awkwardness. Goal-relevant relational talk attenuates (but does not eliminate) this effect.
- **Proposed methodology:** Four controlled experiments (lab/online); mediation analysis for expectancy violation and awkwardness
- **Data source:** Experimental (primary, lab-constructed interactions) — not public/secondary
- **Key contribution claimed:** Challenges the assumption that enhanced AI social fluency improves commercial outcomes; identifies "awkwardness" as a key emotional mediator unique to AI-mediated commercial settings
- **Our assessment:** Novel and counter-intuitive finding directly relevant to AI chatbot strategy for brands. Bridges HCI and consumer psychology. Limitation: lab experiments may not fully capture real deployment contexts (Shopify, Klarna). Worth watching — if replicated in field, major implication for brand-side AI deployment decisions. Could build on this with field study in Chinese e-commerce context.
- **Relevance:** ★★★★★

---

### Predicted Incrementality by Experimentation (PIE) for Ad Measurement

- **Authors:** Brett R. Gordon (Northwestern Kellogg), Robert Moakler (Meta), Florian Zettelmeyer (Northwestern Kellogg)
- **Platform:** NBER Working Papers | **Date posted:** April 14, 2026
- **NBER number:** [w35044](https://www.nber.org/papers/w35044) | **Status:** Working paper
- **Research stream:** Methodology (causal inference in marketing / advertising measurement)
- **Abstract summary:** RCTs provide the gold standard for advertising incrementality but cannot be run on every campaign. PIE reframes ad measurement as a campaign-level prediction problem: a set of RCTs trains a mapping from campaign features to causal effects, which is then applied to non-experimental campaigns. Post-determined features (test-group outcomes, exposure rates, last-click conversions) are used as inputs because the RCTs identify the causal baseline.
- **Proposed methodology:** ML-based supervised prediction of causal effects; trained on RCT-derived ground truth; out-of-sample evaluation using held-out RCTs
- **Data source:** 2,226 Meta advertising experiments (proprietary; co-authored by Meta researcher)
- **Key contribution claimed:** PIE achieves out-of-sample R² = 0.88 for incremental conversions per dollar vs. R² = 0.19 for industry-standard 7-day last-click attribution; disagrees with RCT-based decisions in only 8–12% of campaigns vs. 12–20% for last-click
- **Our assessment:** High-impact methodology paper with direct industry application. The Meta data access is a strength and a potential concern for generalizability. Conflict of interest noted (Moakler is Meta employee; Gordon & Zettelmeyer are former part-time Facebook researchers). For our work, PIE is directly applicable to multi-channel brand campaign evaluation. Could be adapted for Chinese platform advertising (Douyin, Tmall) where RCT infrastructure is growing. Likely to become a widely-cited methods reference.
- **Relevance:** ★★★★☆

---

### Hijacking Online Reviews: Sparse Manipulation and Behavioral Buffering in Popularity-Biased Rating Systems

- **Authors:** Itsuki Fujisaki, Kunhao Yang (affiliations not publicly listed)
- **Platform:** arXiv | **Date posted:** ~April 16, 2026
- **arXiv ID:** [2604.13049](https://arxiv.org/abs/2604.13049) | **Status:** Preprint
- **Research stream:** Digital Economy / Social Media (UGC integrity)
- **Abstract summary:** Online review systems are vulnerable to self-reinforcing distortions exploited by single malicious reviewers. Using a minimal agent-based model, the paper compares "broad attacks" (perturbing many items) with "sparse attacks" (selectively boosting low-quality items / suppressing high-quality items). Sparse attacks are substantially more effective at corrupting popularity-biased ranking systems. Behavioral heterogeneity in user review behavior provides a partial buffer.
- **Proposed methodology:** Agent-based computational model; sensitivity analysis of attack strategies; behavioral buffering simulation
- **Data source:** Simulated/computational — no empirical dataset
- **Key contribution claimed:** Formalizes a "sparse attack" strategy that is disproportionately effective; shows behavioral diversity among users as a natural defense mechanism; design implications for platform operators
- **Our assessment:** Primarily a computational/theoretical paper rather than an empirical marketing study. Relevance to brand teams: understanding review manipulation risk, especially on platforms with popularity-biased algorithms (Amazon, JD.com, Taobao). Limited direct application to co-branding or brand equity research streams. Useful background for digital economy and platform integrity work. No cross-validated empirical data limits immediate applicability.
- **Relevance:** ★★★☆☆

---

## Notable Recent Paper — Just Outside Window (April 5, 2026)

> Included because of exceptional relevance to AI×Brand stream; submitted April 5 (8 days before window). Monitor for journal submission updates.

---

### Commercial Persuasion in AI-Mediated Conversations

- **Authors:** Francesco Salvi, Alejandro Cuevas, Manoel Horta Ribeiro (all Princeton University)
- **Platform:** arXiv | **Date posted:** April 5, 2026
- **arXiv ID:** [2604.04263](https://arxiv.org/abs/2604.04263) | **Status:** Preprint (under review status unknown)
- **Research stream:** AI×Brand / Digital Economy
- **Abstract summary:** As LLMs become primary interfaces between users and the web, companies have growing incentives to embed commercial influence into AI conversations. Two preregistered experiments (N = 2,012) compare traditional search vs. LLM agent (five frontier models) for book selection from a large catalog. A random fifth of products are designated "sponsored" and promoted in different ways. LLM-driven persuasion **nearly triples** sponsored product selection (61.2% vs. 22.4%). Most users fail to detect promotional steering. "Sponsored" labels do not significantly reduce persuasion. Concealing the model's intent makes influence nearly invisible (detection accuracy < 10%).
- **Proposed methodology:** Two preregistered RCT experiments; between-subjects design; 5 LLM conditions; product selection and detection tasks
- **Data source:** Primary experimental data, N = 2,012 (eBook catalog selection task)
- **Key contribution claimed:** Empirical demonstration that LLM persuasion drastically outperforms traditional search-based sponsored placement; existing transparency mechanisms (labels) insufficient; covert intent makes detection near-impossible
- **Our assessment:** Landmark paper with major implications for AI-mediated brand marketing and consumer protection regulation. The Princeton team's RCT design is rigorous and preregistered — findings are credible. For brands: compelling evidence that LLM-embedded promotion is extremely potent. For regulators: strong empirical basis for AI advertising disclosure requirements. Directly relevant to our AI×Brand research stream; consider building on the detection side — what signals help consumers identify AI persuasion? Also relevant to Chinese market context where LLM-powered shopping assistants (e.g., Taobao AI) are proliferating.
- **Relevance:** ★★★★★

---

## Search Coverage Summary

| Keyword Group | Platforms Searched | Papers Found (window) |
|---|---|---|
| A — Branding (co-branding, brand alliance) | SSRN, arXiv, Google Scholar | 0 (no verifiable papers within window) |
| B — AI×Brand (LLM marketing, generative AI) | arXiv, SSRN | 2 (2604.12206; 2604.04263 just outside) |
| C — Internationalization | SSRN, Google Scholar | 0 |
| D — Competitiveness (brand equity, valuation) | SSRN | 0 |
| E — Social Media (influencer, UGC) | SSRN, arXiv | 0 within window |
| F — Methodology (NLP, causal inference) | NBER, arXiv, SSRN | 1 (NBER w35044) |
| G — Digital Economy (platform, reviews) | arXiv | 1 (2604.13049) |

**Note on coverage gaps:** Systematic SSRN date-filtering requires logged-in browser access (403 errors blocked direct API crawl). NBER browsing with specific date filters also returned 403. arXiv abstract pages were similarly blocked. Papers were identified via targeted keyword+date web searches and verified through Google-cached metadata. Papers cannot be confirmed on ResearchGate within this window.

---

## Deduplication Log

- arXiv 2604.04263 and NBER w35044 cover different aspects of AI+advertising; not duplicates
- No cross-platform duplicates detected
- arXiv 2604.12206 (AI relational talk) complements but does not overlap with 2604.04263 (AI persuasion)

---

*Scan completed: 2026-04-20 | Next scan: 2026-04-27*
