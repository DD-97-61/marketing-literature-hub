# Secondary Data Compatibility Report — 2026-04-19

## Preamble — No Upstream Files Found

No `*_is_methods.md` or `*_ml_nlp_methods.md` files were found in `research_pipeline/methods_arsenal/` (routines 07 and 08 have not produced output yet). This filter was applied directly to search results obtained as a proxy for what those routines would have discovered in the last 7 days. Six methods are evaluated.

---

## Summary: Methods reviewed: 6 | PASS: 3 | CONDITIONAL: 2 | FAIL: 1

---

## PASS Methods (all 4 must-haves met)

---

### 1. Double Machine Learning for Static Panel Models with Fixed Effects

| Criterion | Status |
|---|---|
| Works with observational/archival data? | ✅ YES — designed for observational panel data |
| Works with public sources (social media, govt stats, filings)? | ✅ YES — used with government labor/voting records |
| Published example with secondary data? | ✅ YES — UK National Minimum Wage effect on voting behavior (Clarke & Polselli 2026) |
| Available open-source implementation? | ✅ YES — `xtdml` R package (GitHub: `POLSEAN/xtdml`) |

**Source:** Clarke & Polselli (2026). *The Econometrics Journal*, 29(1), 69–86. DOI: 10.1093/ectj/utaf011. arXiv: 2312.08174.

**Nice-to-have score:** 3/4
- Works with Chinese data? ✅ YES — any panel data structure works
- No massive compute? ✅ YES — R package, runs on standard hardware
- Published in marketing journal? ❌ NO — Econometrics Journal
- Addresses endogeneity? ✅ YES — core purpose; Neyman orthogonality ensures valid inference under high-dimensional confounding

**Method overview:** Extends DML (Chernozhukov et al. 2018) to static panel data with fixed effects using correlated random effects, within-group, and first-differencing transformations. Handles non-linear confounding via ensemble ML. Authors recommend first-differencing + ensemble learner.

**Best data types:** Brand-level or firm-level panel data (firm × year), store-level transaction panels, platform-level ad spend panels.

**Our potential use:** Estimating causal effect of brand actions (e.g., visual rebranding, aesthetic changes, CSR disclosures) on consumer outcomes (sales, stock, social media engagement) using archival data — controlling for high-dimensional brand and market characteristics without requiring instruments.

---

### 2. LA-ABSA: LLM-as-an-Annotator for Aspect Sentiment Tuple Prediction

| Criterion | Status |
|---|---|
| Works with observational/archival data? | ✅ YES — applied to existing unlabeled review/social media text |
| Works with public sources? | ✅ YES — works on any public text corpus (reviews, social posts) |
| Published example with secondary data? | ✅ YES — evaluated on five standard ABSA datasets (Restaurant, Laptop, MAMS, etc.) drawn from existing corpora |
| Available open-source implementation? | ✅ YES — GitHub: `NilsHellwig/LA-ABSA` |

**Source:** Hellwig et al. (2026). *LLM-as-an-Annotator: Training Lightweight Models with LLM-Annotated Examples for Aspect Sentiment Tuple Prediction*. arXiv: 2603.01778.

**Nice-to-have score:** 2/4
- Works with Chinese data? ⚠️ CONDITIONAL — paper uses English datasets; method architecture supports multilingual but requires Chinese LLM annotator (e.g., Qwen-2.5)
- No massive compute? ⚠️ CONDITIONAL — annotation step uses Gemma-3-27B (requires GPU); inference step uses lightweight fine-tuned model (CPU-feasible)
- Published in marketing journal? ❌ NO — arXiv/NLP venue
- Addresses endogeneity? ❌ NO — purely a measurement/annotation method

**Method overview:** Uses a large LLM (Gemma-3-27B) to annotate unlabeled examples for aspect-level sentiment tasks (Target-Aspect-Sentiment Detection + Aspect Sentiment Quad Prediction). A small, efficient model is then fine-tuned on LLM-annotated data. Outperforms augmentation baselines and approaches full LLM prompting accuracy at a fraction of inference cost.

**Best data types:** Consumer product reviews, brand-related social media posts (Weibo, Twitter/X), app store reviews.

**Our potential use:** Annotate brand attribute sentiment at scale from secondary data — e.g., classify consumer perception of brand *aesthetics*, *quality*, *authenticity* dimensions from Tmall/JD reviews or Weibo posts without manual coding. Enables large-N brand perception measurement as dependent or independent variable.

---

### 3. Methodological Guide: LLMs for Text Annotation in Social Sciences and Humanities (Python & R)

| Criterion | Status |
|---|---|
| Works with observational/archival data? | ✅ YES — explicit purpose is annotating existing text corpora |
| Works with public sources? | ✅ YES — covers social media, news, documents |
| Published example with secondary data? | ✅ YES — guide demonstrates full workflow with SSH research examples |
| Available open-source implementation? | ✅ YES — Python and R code provided; covers open-source LLMs (LLaMA, Mistral) |

**Source:** arXiv 2604.09638 (April 2026). *A Methodological Guide on Using Large Language Models for Text Annotation in the Social Sciences and Humanities with Python and R*.

**Nice-to-have score:** 2/4
- Works with Chinese data? ✅ YES — covers multilingual models; guide is model-agnostic
- No massive compute? ✅ YES — covers API-based (GPT-4o) and local open-source models; scalable
- Published in marketing journal? ❌ NO — arXiv preprint
- Addresses endogeneity? ❌ NO — measurement method only

**Method overview:** Step-by-step guide covering: (1) prompt design, (2) annotation quality evaluation (inter-rater reliability with LLM), (3) iterative refinement, (4) integration of LLM annotations into downstream statistical models while accounting for annotation uncertainty/error. Covers cost, reproducibility, and scaling considerations.

**Best data types:** Any text: social media, firm disclosures, news articles, customer reviews, earnings call transcripts.

**Our potential use:** Use as the operational blueprint for converting secondary text corpora (e.g., brand social media posts, Weibo comments, firm press releases) into structured variables for quantitative analysis. Particularly useful for scaling up content analysis that would otherwise require student coders.

---

## CONDITIONAL Methods (adaptation needed)

---

### 4. Self-Reflection in Automated Qualitative Coding via Secondary LLM Critique

**Source:** arXiv 2601.09905 (January 2026). *Self-reflection in Automated Qualitative Coding: Improving Text Annotation through Secondary LLM Critique*.

| Criterion | Status |
|---|---|
| Works with observational/archival data? | ✅ YES |
| Works with public sources? | ✅ YES |
| Published example with secondary data? | ✅ YES — qualitative coding of existing text |
| Available open-source implementation? | ❌ UNVERIFIED — no confirmed public GitHub repo found in searches |

**Verdict: CONDITIONAL** — method is sound and the approach (recall-first LLM → precision-focused critique pass) is well-described, but no confirmed open-source implementation was found. A researcher would need to implement from the paper description.

**Adaptation needed:** Implement the two-pass critique pipeline using available LLM APIs (OpenAI, Anthropic, or local Ollama). Estimated effort: 1–2 days for a researcher with Python experience.

---

### 5. Zero-Shot Multilingual ABSA with LLMs

**Source:** arXiv 2412.12564 (December 2024). *Evaluating Zero-Shot Multilingual Aspect-Based Sentiment Analysis with Large Language Models*. Also published in *International Journal of Machine Learning and Cybernetics* (Springer, 2025).

| Criterion | Status |
|---|---|
| Works with observational/archival data? | ✅ YES |
| Works with public sources? | ✅ YES |
| Published example with secondary data? | ✅ YES — multilingual review datasets |
| Available open-source implementation? | ⚠️ PARTIAL — relies on GPT-4, LLaMA, Mixtral APIs; no single-package implementation |

**Verdict: CONDITIONAL** — method itself is straightforward (prompt-based zero-shot), but "implementation" is API calls rather than a packaged library. The paper's key finding — that simpler zero-shot prompts outperform complex chain-of-thought for ABSA — is directly actionable.

**Adaptation needed:** Write structured ABSA prompts for your specific brand dimensions; use open-source LLM (Qwen-2.5 for Chinese; LLaMA-3 for English) to avoid API costs at scale. Estimated effort: 1 day.

**Chinese data:** ✅ HIGH PRIORITY — paper explicitly tests Chinese, French, Dutch, Spanish. Strong multilingual results.

---

## FAIL Methods

---

### 6. Multimodal Vision-Language Models for Brand Aesthetic Analysis

**Candidate papers considered:** arXiv 2503.06141 (*Next Token Is Enough: Realistic Image Quality and Aesthetic Scoring*); arXiv 2402.13022 (*SoMeLVLM: A Large Vision Language Model for Social Media Processing*).

**Verdict: FAIL (for this round)**

| Criterion | Status |
|---|---|
| Works with observational/archival data? | ✅ YES |
| Works with public sources? | ✅ YES |
| Published example with secondary data? | ❌ FAIL — arXiv 2503.06141 uses UGC images but the annotation is manual (14,715 images, human-labeled); SoMeLVLM (2402.13022) is from 2024 and does not have a verified marketing/brand secondary data application |
| Available open-source implementation? | ⚠️ PARTIAL — SoMeLVLM has a repo but is 2024 and untested for brand research; 2503.06141 code availability unconfirmed |

**Reason for FAIL:** No paper found in this search cycle that (a) applies a VLM to brand/product image analysis, (b) uses purely secondary/public image data, and (c) has a confirmed open-source implementation, all verified together. The building blocks exist but no single integrated method meets all 4 criteria in recent publications. **Revisit in next cycle** — this space is moving fast and a qualifying paper likely exists or will appear shortly.

---

## Methodological Note

- **DML + Panel FE** is the highest-priority method for our IS-side pipeline. It directly addresses the endogeneity concern that reviewers raise when using archival brand data, and the `xtdml` package makes it immediately usable.
- **LA-ABSA + LLM SSH Guide (Methods 2 + 3)** work in tandem: Method 3 provides the operational framework; Method 2 provides a specific, efficient implementation for aspect-level sentiment annotation. Together they form a complete secondary-data measurement pipeline for brand perception constructs.
- **Chinese data readiness:** Method 1 (DML) is fully ready; Methods 2–3 require pairing with a Chinese-capable LLM (Qwen-2.5-72B recommended); Method 5 (CONDITIONAL) explicitly supports Chinese.
