# Secondary Data Compatibility Report — 2026-04-20

## Summary
- **Methods reviewed:** 16 (5 from IS methods scan · 11 from ML/NLP scan)
- **PASS:** 4 — DCS, Causal ML, ML+Econometrics Hybrid Framework, DimABSA
- **CONDITIONAL:** 10 — RATER, Deep Chain-of-Preference, LLM-as-Judge (Business Validity), PeReGrINE, Media Narrative Clustering, Temporal News Dynamics, QA-MoE, MEME-Fusion, DAMA Contrastive Sentiment, Multi-Perspective LLM Annotation
- **FAIL:** 2 — Agentic Personalisation, Graph+Event Sequence SSL

---

## PASS — Fully Compatible Methods

### 1. DCS (Dimensionalization and Category Surfacing)
*Source: "Trustworthiness in Computational Theory Construction" — MISQ 2026 · DOI: 10.25300/MISQ/2026/18511*

- **Must-have check:**
  1. Observational/archival data? **Yes** — works on any text corpus; no treatment or experiment needed
  2. Public sources? **Yes** — explicitly demonstrated on consumer reviews, forum posts (Amazon, Reddit, Twitter)
  3. Published example with secondary data? **Yes** — MISQ paper applies to unstructured organizational/digital text corpora
  4. Open-source implementation? **Yes** — `bertopic` (pip), `gensim`, `sentence-transformers`, `sklearn`, `pyLDAvis` — all mature, maintained packages

- **Nice-to-have score: 2/4**
  - Chinese data? ✅ (multilingual sentence-BERT; BERTopic language-agnostic)
  - No massive compute? ✅ (CPU-feasible; single GPU for large corpora)
  - Marketing journal? ❌ (IS journal)
  - Addresses endogeneity? ❌ (descriptive/inductive; no causal claim)

- **Best suited data types:** Social media posts (Weibo, Twitter/X), consumer reviews (JD, Amazon, Yelp), brand-related forum discussions, ad copy corpora, news articles about brands

- **Example secondary data application:** Inductively surface latent brand dimensions from a corpus of Weibo posts mentioning a brand — no pre-specified categories needed; BERTopic discovers clusters, sentence-BERT generates embeddings, clustering surfaces dimensions

- **Implementation:** `pip install bertopic sentence-transformers gensim` · BERTopic docs: https://maartengr.github.io/BERTopic/

- **Our potential use:** Brand landscape mapping — feed 5–10 years of Weibo/JD reviews for a brand into a DCS pipeline to inductively discover how perceived brand dimensions have evolved. No labeling required; suitable for Chinese data; publishable in MISQ/ISR/JMR framing.

---

### 2. Causal ML (Causal Machine Learning — Causal Forests, DML, Meta-Learners)
*Source: "Causal Machine Learning in Information Systems Research" — BISE 2026 · DOI: 10.1007/s12599-026-00999-x*

- **Must-have check:**
  1. Observational/archival data? **Yes** — explicitly designed for non-experimental observational data; the entire paper addresses this use case
  2. Public sources? **Yes** — government statistics, scanner data, advertising logs, loyalty panel data, social media engagement records
  3. Published example with secondary data? **Yes** — the BISE review paper cites multiple IS applications to archival panel data; EconML/grf papers all demonstrate on observational datasets
  4. Open-source implementation? **Yes** — `EconML` (Microsoft, pip), `CausalML` (Uber, pip), `DoubleML` (pip, also CRAN), `grf` (R CRAN)

- **Nice-to-have score: 3/4**
  - Chinese data? ✅ (works on tabular/behavioral data; language-agnostic)
  - No massive compute? ✅ (runs on CPU/single GPU for academic sample sizes)
  - Marketing journal? ❌ (IS-adjacent BISE journal)
  - Addresses endogeneity? ✅ (core design purpose — estimates causal effects under unconfoundedness; DML handles high-dimensional confounders)

- **Best suited data types:** Scanner/panel data, CRM transaction records, digital advertising logs, social platform engagement data, e-commerce click/purchase logs, government economic statistics

- **Example secondary data application:** Estimate heterogeneous treatment effects of a brand crisis (event) on customer retention using CRM panel data — X-learner splits data into treated/control by exposure to the crisis event, estimates individual-level retention loss by customer segment

- **Implementation:** `pip install econml causalml doubleml` · EconML docs: https://econml.azurewebsites.net/ · `install.packages("grf")` in R

- **Our potential use:** (a) Marketing mix heterogeneity — which customer segments respond differently to brand advertising? (b) Brand event causal attribution — DML estimates causal effect of a product launch or scandal on sales, controlling for confounders via ML; publishable design for JM/JMR/MIS Quarterly.

---

### 3. ML + Econometrics Hybrid Framework (Multimethod Integration)
*Source: "Advancing Next-Generation Multimethod Research in IS" — ISR Vol. 36(2) 2026 · DOI: 10.1287/isre.2025.editorial.v36.n2*

- **Must-have check:**
  1. Observational/archival data? **Yes** — the framework is explicitly built around overcoming limitations of observational data by combining ML flexibility with econometric causal identification
  2. Public sources? **Yes** — social media, financial databases, scanner data, government data — all cited as input sources in the ISR editorial
  3. Published example with secondary data? **Yes** — editorial references 15 published IS papers applying this design to observational secondary data
  4. Open-source implementation? **Yes** — `statsmodels`, `linearmodels` (panel econometrics), `EconML`, `doubleml`, `sklearn` — all open-source

- **Nice-to-have score: 3/4**
  - Chinese data? ✅ (framework is language/market-agnostic)
  - No massive compute? ✅ (econometric stage runs on CPU; ML stage is single-GPU feasible)
  - Marketing journal? ❌ (IS journal)
  - Addresses endogeneity? ✅ (explicit purpose — IV and DiD integration documented; ML generates constructs, econometrics handles identification)

- **Best suited data types:** Social media data combined with financial/stock data, scanner data combined with brand event logs, UGC text combined with sales panel data

- **Example secondary data application:** Stage 1 — Use NLP/BERTopic to extract brand perception scores from Weibo posts (ML-generated construct). Stage 2 — Use DiD or IV econometrics to estimate causal effect of brand events on sales, using the ML-generated perception scores as mediators or controls.

- **Implementation:** `pip install statsmodels linearmodels econml doubleml scikit-learn`

- **Our potential use:** This is a **design template** for the entire research programme — brand crisis studies, brand perception → sales studies, advertising effectiveness. Provides reviewer-defensible justification language for hybrid ML + causal designs. High strategic value for positioning papers in ISR/MISQ/JMR.

---

### 4. DimABSA (Dimensional Aspect-Based Sentiment Analysis)
*Source: "SemEval-2026 Task 3: Dimensional Aspect-Based Sentiment Analysis" — ACL SemEval-2026 · arXiv:2604.07066*

- **Must-have check:**
  1. Observational/archival data? **Yes** — works on product reviews, social media posts — purely text-analytic, no experiment
  2. Public sources? **Yes** — SemEval-2026 multilingual customer review datasets; Amazon, Yelp, Twitter/X archives
  3. Published example with secondary data? **Yes** — SemEval-2026 shared task uses multilingual public consumer review corpora; 112 system submissions with published results
  4. Open-source implementation? **Yes** — GitHub: https://github.com/DimABSA/DimABSA2026 · Fine-tuned XLM-RoBERTa baselines available · HuggingFace ecosystem

- **Nice-to-have score: 2/4**
  - Chinese data? ✅ (10+ languages including Chinese; XLM-RoBERTa is multilingual)
  - No massive compute? ✅ (single GPU fine-tuning; inference on CPU feasible)
  - Marketing journal? ❌ (ACL/NLP venue)
  - Addresses endogeneity? ❌ (measurement tool, not causal)

- **Best suited data types:** Product reviews (Chinese e-commerce: JD, Taobao; global: Amazon, Trustpilot), social media brand mentions, Weibo/Twitter brand posts, app store reviews

- **Example secondary data application:** Map JD.com reviews for a brand across brand attributes (quality, design, service) onto a valence×arousal grid — distinguishing "lukewarm dissatisfaction" (low arousal, mildly negative valence) from "outraged backlash" (high arousal, highly negative) for more granular brand health monitoring

- **Implementation:** `pip install transformers torch datasets` · Fine-tune XLM-RoBERTa-base with regression head · Baseline code at GitHub repo above

- **Our potential use:** (a) Brand crisis severity mapping — track where on the VA plane consumer sentiment sits over a crisis timeline. (b) Cross-cultural brand perception comparison — does "quality" elicit same valence + arousal levels in Chinese vs. US reviews? Directly compatible with JD/Amazon cross-market secondary data. Methodological contribution over standard ABSA.

---

## CONDITIONAL — Needs Adaptation

### 5. RATER / LLM Scale Validation
*Source: "AI-Augmented Content Validation in Behavioral Research" — MISQ 50(1) 2026*

- **What's missing:**
  - Criterion 2 (public sources): RATER processes measurement scale items, not social media or government data. Its natural input is survey instruments, not public secondary datasets.
  - Criterion 3 (published secondary data example): The published application validates survey scales — inherently a primary research tool. No published example of using RATER to analyze secondary archival data.

- **What adaptation needed:** Repurpose RATER to validate whether inductively-discovered text clusters (from DCS/BERTopic applied to secondary UGC) meaningfully correspond to theoretical brand constructs. E.g., "does this Weibo topic cluster represent 'brand warmth'?" — RATER evaluates convergent/discriminant validity of the cluster-to-construct mapping without requiring a survey.

- **Effort estimate:** Low (web tool is free; adaptation is conceptual, not technical)

---

### 6. Deep Chain-of-Preference Learning
*Source: "Deep Chain-of-Preference" — MISQ online-first 2026*

- **What's missing:**
  - Criterion 2 (public sources): Requires large-scale user interaction logs (purchase/click sequences). Truly public datasets at sufficient scale are rare; most come from proprietary retailer APIs or NDA-protected industry partnerships.
  - Criterion 4 (implementation): RecBole framework exists but the specific "mixed-grained" chain-of-preference architecture requires substantial custom implementation; no standalone package.

- **What adaptation needed:** Access to a retailer's transaction log via data sharing agreement (academic partnership with JD.com or Alibaba Research), or use Amazon Reviews 2023 interaction sequences (semi-public). Re-implement using RecBole + custom preference chain module.

- **Effort estimate:** High (data access + engineering effort)

---

### 7. LLM-as-Judge (Business Outcome Validity)
*Source: arXiv:2604.00022 — anonymous preprint*

- **What's missing:**
  - Criterion 4 (open-source implementation): Paper provides rubric + protocol but no code repository. Preprint is anonymous — no confirmed authorship or associated GitHub.
  - Criterion 2 (public sources): The calibration step requires labeled outcome data (conversion/engagement labels) linked to text — typically proprietary. Public calibration datasets for this exact task don't exist.

- **What adaptation needed:** (a) Implement the bias-control rubric using any frontier LLM API (implementable from paper description). (b) For calibration, use publicly available conversation quality benchmarks or substitute with a small expert-labeled holdout from public review data. The bias-mitigation protocol is directly replicable from the paper.

- **Effort estimate:** Medium (re-implementation from paper description + sourcing calibration data)

---

### 8. PeReGrINE (Graph-Augmented Review Fidelity)
*Source: arXiv:2604.07788 — anonymous preprint*

- **What's missing:**
  - Criterion 4 (open-source implementation): "Graph construction code expected on arXiv repo page" — not yet confirmed publicly available. Anonymous preprint; no guaranteed code release.

- **What adaptation needed:** Wait for code release (typical arXiv → ACL camera-ready cycle: 2–4 months). Core data (Amazon Reviews 2023) is already public. If code remains unavailable, re-implement bipartite graph construction using `networkx`/`torch_geometric` — the architecture is fully described.

- **Effort estimate:** Low-to-Medium (wait + possibly reconstruct graph pipeline from paper description)

---

### 9. Media Narrative Clustering (Structured Event/Character Clustering)
*Source: arXiv:2604.10368 — anonymous preprint*

- **What's missing:**
  - Criterion 4 (open-source implementation): "Code/data links on arXiv page" mentioned but anonymous preprint with no confirmed repo. Implementation availability is unverified.

- **What adaptation needed:** Data (news corpora) is available via GDELT/MediaCloud. If code is not released, the structured clustering approach can be approximated using existing event extraction tools (AllenNLP SRL, Stanford CoreNLP) + scikit-learn clustering — describable in paper as "following [paper]'s framework." Full re-implementation is Medium effort.

- **Effort estimate:** Medium

---

### 10. Temporal News Dynamics (Frame Evolution Analysis)
*Source: arXiv:2604.14315 — anonymous preprint*

- **What's missing:**
  - Criterion 4 (open-source implementation): Anonymous preprint; code availability unconfirmed. Method described as "word importance + temporal segmentation" — lightweight enough to reconstruct.

- **What adaptation needed:** Data is public (GDELT, MediaCloud). Core method (word-importance tracking over time windows) can be re-implemented with `sklearn` TF-IDF + temporal aggregation in ~100 lines of Python. Lower reconstruction effort than deep learning methods.

- **Effort estimate:** Low (lightweight, reconstructable method)

---

### 11. QA-MoE (Multimodal Sentiment — Quality-Aware Mixture of Experts)
*Source: arXiv:2604.05704*

- **What's missing:**
  - Criterion 4 (open-source implementation): "Code link not yet confirmed." Pre-print with 7 authors — code likely forthcoming but not yet released.
  - Nice-to-have concern: Multi-GPU compute recommended for video encoding (high barrier for solo researcher).

- **What adaptation needed:** Wait for code release. Data (CMU-MOSI, CMU-MOSEI) is public. GPU access via Colab Pro or university HPC is feasible. If video modality is dropped and only text+audio used, single-GPU inference is achievable.

- **Effort estimate:** Medium (wait for code + GPU resource planning)

---

### 12. MEME-Fusion (Cross-Modal Attention for Social Memes)
*Source: arXiv:2604.14218 — anonymous preprint · CHiPSAL @ COLING 2026*

- **What's missing:**
  - Criterion 4 (open-source implementation): CLIP and BGE-M3 are open-source, but the specific cross-modal attention fusion + gating network is from an anonymous workshop paper with no confirmed code repo.

- **What adaptation needed:** The fusion architecture is described in sufficient detail to re-implement using `transformers` (HuggingFace) + CLIP. A working re-implementation is feasible in ~3–5 days of engineering. Workshop papers at COLING are typically published with code; expect release within 1–3 months.

- **Effort estimate:** Low-to-Medium (re-implement from paper or wait for camera-ready release)

---

### 13. DAMA Contrastive Sentiment (Dynamic Adaptive Multi-Head Attention + SCL)
*Source: arXiv:2604.10459 — anonymous preprint*

- **What's missing:**
  - Criterion 4 (open-source implementation): "Code likely forthcoming" — not yet available. Anonymous preprint.

- **What adaptation needed:** Standard BERT fine-tuning with a custom attention head. The method is a moderately complex modification of BERT — re-implementable from the paper using `transformers`. Data (SST-2, IMDB, Yelp) is fully public.

- **Effort estimate:** Medium (requires BERT fine-tuning expertise; wait for code or re-implement)

---

### 14. Multi-Perspective LLM Annotation (PPI + LLM)
*Source: arXiv:2603.21404 — March 2026 preprint*

- **What's missing:**
  - Criterion 4 (open-source implementation): "Code referenced in paper" — not confirmed as a released open-source repository. The PPI component has a standalone package (`ppi_py` on PyPI); the LLM multi-perspective framework does not have a confirmed standalone repo.

- **What adaptation needed:** Combine `ppi_py` (PPI framework) + any LLM API (e.g., Claude, GPT-4o) with the perspective prompting protocol from the paper. The statistical framework is implementable without paper-specific code; requires only a small expert-labeled holdout (~100–200 items) from the target corpus for calibration.

- **Effort estimate:** Low-to-Medium (assemble from existing tools; `pip install ppi_py` + LLM API)

---

## FAIL — Not Compatible

| Method | Source | Reason |
|--------|--------|--------|
| **Agentic Marketing Personalisation** | arXiv:2604.08621 | Requires active A/B deployment — interventional, not observational. Data is proprietary internal engagement logs (no public equivalent). No code released. Fails criteria 1, 2, 3, 4. |
| **Graph+Event Sequence SSL (Beyond Isolated Clients)** | arXiv:2604.09085 | Code explicitly "not yet released" — criterion 4 is a hard NO. Datasets are partially proprietary. Cannot be adopted until code release and public data availability are confirmed. |

---

## Priority Recommendations

### Immediate Use (PASS methods, deployable now)

| Priority | Method | Best Dataset | Action |
|----------|--------|-------------|--------|
| 🥇 | **Causal ML (EconML/grf)** | Scanner panel, CRM logs, ad logs | Start with DML on any existing panel dataset; `pip install econml` |
| 🥈 | **ML + Econometrics Hybrid** | Weibo/news + financial/sales panel | Use as research design template for next paper; no new software needed |
| 🥉 | **DimABSA** | JD/Amazon reviews (Chinese-compatible) | Fine-tune XLM-RoBERTa on DimABSA2026 baseline; brand VA mapping |
| 4 | **DCS (BERTopic)** | Any brand text corpus | `pip install bertopic`; can start today on existing review data |

### Watch List (CONDITIONAL — upgrade when code releases)

- **Multi-Perspective LLM Annotation**: Highest utility-to-effort ratio; `ppi_py` already installable; most likely to be re-activated quickly
- **Temporal News Dynamics**: Lightweight, reconstructable; immediate value for brand crisis timeline research
- **Media Narrative Clustering**: High strategic value for brand narrative framing research; watch for code release

---

*Generated by Routine #9 (Secondary Data Filter) | 2026-04-20*
*Input files: `2026-04-20_is_methods.md` (5 methods) · `2026-04-20_ml_nlp_methods.md` (11 methods)*
