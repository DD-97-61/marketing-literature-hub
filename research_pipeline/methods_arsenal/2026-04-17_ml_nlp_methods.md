# ML/NLP Methods Arsenal — 2026-04-17

> **Scan period:** April 10–17, 2026  
> **Target venues:** arXiv cs.CL / cs.SI / cs.AI / cs.LG, ACL, EMNLP, NeurIPS, ICML, WWW, ICWSM, KDD, WSDM  
> **Focus:** Methods transferable to marketing & branding research — text, image, multimodal, behavioral & e-commerce data  
> **Note on dates:** arXiv 2604.XXXXX IDs indicate April 2026. Sequence numbers ≥ ~6,000 correspond roughly to April 8–17; exact daily cutoffs are estimated. All papers are independently verifiable via the linked arXiv IDs.

---

## Ranked Methods

---

### LLM-HYPER: Generative CTR Modeling for Cold-Start Ad Personalization via LLM-Based Hypernetworks
- **Authors/Venue/Date:** arXiv:2604.12096 · April 2026 (cs.IR / cs.LG)
- **Method:** LLM-as-Hypernetwork for zero-shot CTR parameter generation
- **What it does:** Treats an LLM as a hypernetwork that *generates the weights* of a click-through-rate (CTR) estimator directly from multimodal ad content (text + creative images), using few-shot Chain-of-Thought prompting and CLIP-based retrieval of semantically similar past campaigns. Solves the cold-start problem for brand-new ads with zero user-feedback history, achieving +33.3% NDCG@10 over the best cold-start baseline.
- **Input data type:** Multimodal (text + image)
- **Marketing application ideas:**
  1. **New product launch ads:** Generate CTR score predictions for brand-new SKUs before any campaign goes live, ranking creative variants purely from their visual and copy content.
  2. **Cross-channel creative scoring:** Apply to social-media ad variants (Instagram vs. display) at brief-writing stage to flag low-performing assets before spend is committed.
- **Data requirements / Available implementation:** Requires multimodal ad creatives (image + text copy) and historical campaign metadata for few-shot retrieval; CLIP embeddings needed. Paper: https://arxiv.org/abs/2604.12096 — check paper for code release.
- **Technical complexity:** High (LLM inference + CLIP retrieval pipeline + calibration layer; GPU required for LLM)
- **Relevance:** ★★★★★

---

### Criterion Validity of LLM-as-Judge for Business Outcomes in Conversational Commerce
- **Authors/Venue/Date:** Liang Chen, Qi Liu, Wenhuan Lin, Feng Liang · arXiv:2604.00022 · April 2026 (cs.CL)
- **Method:** LLM-as-Judge rubric validation against real conversion outcomes
- **What it does:** Tests whether multi-dimensional dialogue-quality rubrics scored by an LLM-as-Judge actually predict downstream business conversion on a live matchmaking/e-commerce platform. Finds *dimension-level heterogeneity*: Need Elicitation and Pacing Strategy predict conversion after Bonferroni correction; Contextual Memory shows no detectable association. Core insight: rubric design matters more than which LLM does the scoring.
- **Input data type:** Text (dialogue transcripts)
- **Marketing application ideas:**
  1. **Chatbot quality auditing:** Build and validate business-aligned rubrics for brand chatbots, then use LLM-as-Judge at scale to score thousands of conversations and predict conversion risk.
  2. **Customer service dimension prioritization:** Identify which conversational dimensions (empathy, urgency handling, upsell pacing) actually drive purchase — and deprioritize metrics that don't.
- **Data requirements / Available implementation:** Conversational logs with business-outcome labels (e.g., purchase, sign-up). Paper: https://arxiv.org/abs/2604.00022 — methodology is reproducible with any off-the-shelf LLM judge.
- **Technical complexity:** Medium (prompt engineering + LLM API calls + statistical testing; no GPU needed for scoring)
- **Relevance:** ★★★★★

---

### URMF: Uncertainty-aware Robust Multimodal Fusion for Multimodal Sarcasm Detection
- **Authors/Venue/Date:** Zhenyu Wang, Weichen Cheng, Weijia Li, Junjie Mou, Zongyou Zhao, Guoying Zhang (China University of Mining and Technology, Beijing) · arXiv:2604.06728 · April 2026 (cs.CL / cs.MM)
- **Method:** Uncertainty-aware multimodal fusion with learnable Gaussian posteriors per modality
- **What it does:** Detects sarcasm in social-media text+image pairs by explicitly modeling *modality reliability uncertainty*. Each modality (text, image, cross-modal interaction) is parameterized as a Gaussian posterior; estimated uncertainty dynamically weights modality contributions during fusion, suppressing noisy or irrelevant visuals. Prevents deterministic fusion from being misled by weakly relevant images — a common failure mode in brand-monitoring pipelines.
- **Input data type:** Multimodal (text + image)
- **Marketing application ideas:**
  1. **Brand sarcasm detection:** Flag sarcastic product/brand mentions on Twitter/Instagram before they are misclassified as positive sentiment, protecting brand health score accuracy.
  2. **Campaign misfire early-warning:** Detect ironic or mocking user-generated responses to ad campaigns in real time, enabling rapid creative or messaging adjustments.
- **Data requirements / Available implementation:** Social-media posts with paired images (Twitter multimodal datasets). Paper: https://arxiv.org/abs/2604.06728 — GPU required (cross-attention + uncertainty estimation layers).
- **Technical complexity:** High (multimodal encoder, uncertainty modeling, custom fusion layer; GPU required)
- **Relevance:** ★★★★

---

### StanceMoE: Mixture-of-Experts Architecture for Stance Detection
- **Authors/Venue/Date:** KUET NLP Group (StanceNakba Shared Task submission) · arXiv:2604.00878 · April 2026 (cs.CL)
- **Method:** Mixture-of-Experts (MoE) on a fine-tuned BERT encoder with context enhancement for multi-target stance detection
- **What it does:** Routes input text through specialized expert modules — each tuned to different stance-relevant patterns — then aggregates predictions for classifying stance (support / oppose / neutral) toward a specific named target. Context enhancement injects target information before routing, improving generalization to rare or unseen targets.
- **Input data type:** Text
- **Marketing application ideas:**
  1. **Brand controversy monitoring:** Track public stance toward specific brand events (product recalls, ESG announcements, executive statements) across Twitter/Reddit without fine-tuning for each new topic.
  2. **Competitor comparison analysis:** Measure stance polarization in consumer discussions comparing your brand vs. a competitor on specific product dimensions.
- **Data requirements / Available implementation:** Social-media text with target-entity labels; no images required. Paper: https://arxiv.org/abs/2604.00878 — BERT-based, runnable on a single GPU.
- **Technical complexity:** Medium (fine-tuned BERT + MoE routing; single GPU sufficient)
- **Relevance:** ★★★★

---

### Prototype-Regularized Federated Learning for Cross-Domain Aspect Sentiment Triplet Extraction
- **Authors/Venue/Date:** arXiv:2604.09123 · April 2026 (cs.CL / cs.LG)
- **Method:** Federated learning with prototype regularization for Aspect Sentiment Triplet Extraction (ASTE)
- **What it does:** Extracts structured `(aspect term, opinion term, sentiment polarity)` triplets from reviews across multiple product domains *without centralizing data*, using prototype regularization to align shared feature representations across federated clients. Enables privacy-preserving cross-retailer/cross-brand review mining — critical when first-party data sharing is restricted by legal or competitive constraints.
- **Input data type:** Text (product reviews)
- **Marketing application ideas:**
  1. **Cross-retailer attribute intelligence:** Mine fine-grained product attribute sentiments (e.g., "battery life", "packaging") across distributed retailer datasets without pooling raw reviews — useful for multi-channel brand tracking.
  2. **Privacy-preserving competitive benchmarking:** Share model weights (not data) with partner brands to jointly learn aspect-level consumer pain points across the category.
- **Data requirements / Available implementation:** Product review corpora (SemEval ABSA datasets compatible); federated setup requires at least 2 client data silos. Paper: https://arxiv.org/abs/2604.09123 — GPU required for fine-tuning.
- **Technical complexity:** High (federated training infrastructure + prototype regularization; moderate GPU per client)
- **Relevance:** ★★★★

---

### CASE: Cadence-Aware Set Encoding for Large-Scale Next Basket Repurchase Recommendation
- **Authors/Venue/Date:** arXiv:2604.06718 · April 2026 (cs.IR / cs.LG)
- **Method:** Calendar-time multi-scale temporal convolution + induced set attention for repurchase prediction
- **What it does:** Models item-specific purchase *cadences* (weekly grocery replenishment, monthly subscription boxes, quarterly seasonal buys) using multi-scale temporal convolutions over calendar-time signals, then captures cross-item dependencies via sub-quadratic induced set attention. Production-scalable; evaluated on large retail datasets showing strong next-basket prediction.
- **Input data type:** Time series (transaction/purchase history)
- **Marketing application ideas:**
  1. **Personalized re-engagement timing:** Predict the optimal moment to trigger a repurchase reminder or loyalty offer for each customer–SKU pair, reducing over-communication and cart abandonment.
  2. **Promotional calendar optimization:** Identify category-level cadence clusters to time category promotions when natural repurchase intent peaks, maximizing incremental lift.
- **Data requirements / Available implementation:** Transaction logs with timestamps and item IDs; no text needed. Paper: https://arxiv.org/abs/2604.06718 — CPU-runnable for inference, GPU for training at scale.
- **Technical complexity:** High (temporal convolution + set attention; scalable but requires careful cadence feature engineering)
- **Relevance:** ★★★★

---

### PeReGrINE: Evaluating Personalized Review Fidelity with User–Item Graph Context
- **Authors/Venue/Date:** arXiv:2604.07788 · April 2026 (cs.CL / cs.IR)
- **Method:** Temporally-consistent bipartite user–item graph for personalized review fidelity evaluation
- **What it does:** Restructures the Amazon Reviews 2023 dataset as a temporally-consistent bipartite graph; evaluates whether generated or existing reviews are *faithful* to a specific user's purchase history and an item's neighborhood context, under strict temporal cutoffs. Provides a rigorous benchmark and scoring method for detecting reviews that are generic, implausible, or inconsistent with verified buyer profiles.
- **Input data type:** Text + network (user–item interaction graph)
- **Marketing application ideas:**
  1. **Fake/astroturf review detection:** Score incoming reviews against user purchase history graphs to flag implausible reviews that don't align with the reviewer's known behavior — key for brand reputation management.
  2. **AI-generated content quality gate:** Validate LLM-generated product descriptions or testimonials against real customer profile graphs before publishing, ensuring personalization fidelity.
- **Data requirements / Available implementation:** User–item interaction data with timestamps (compatible with Amazon Reviews 2023 format). Paper: https://arxiv.org/abs/2604.07788 — graph construction pipeline is described; GPU needed for LLM-based evaluation.
- **Technical complexity:** High (graph construction + temporal filtering + LLM-based scoring; GPU required)
- **Relevance:** ★★★

---

## Summary Table

| # | Paper | arXiv ID | Method Type | Input | Complexity | Relevance |
|---|-------|----------|-------------|-------|------------|-----------|
| 1 | LLM-HYPER | 2604.12096 | LLM-as-hypernetwork | Multimodal | High | ★★★★★ |
| 2 | LLM-as-Judge Validity | 2604.00022 | Rubric validation | Text | Medium | ★★★★★ |
| 3 | URMF | 2604.06728 | Multimodal fusion | Text+Image | High | ★★★★ |
| 4 | StanceMoE | 2604.00878 | MoE stance detection | Text | Medium | ★★★★ |
| 5 | Federated ASTE | 2604.09123 | Federated NLP | Text | High | ★★★★ |
| 6 | CASE | 2604.06718 | Temporal recommendation | Time series | High | ★★★★ |
| 7 | PeReGrINE | 2604.07788 | Graph review eval | Text+Graph | High | ★★★ |

---

## Implementation Notes

- **GPU requirements:** Papers 1, 3, 5, 6, 7 require GPU for training; papers 2 and 4 can run inference via LLM API or a single GPU.
- **Quickest to prototype:** LLM-as-Judge Validity (#2) and StanceMoE (#4) — both usable with HuggingFace BERT checkpoints and LLM APIs.
- **Observational data compatibility:** All 7 methods are designed for observational data; no interventional/experimental setup required.
- **Open-source status:** All papers link to arXiv with methodology fully described. Code repos should be checked at time of use; federated ASTE (#5) and CASE (#6) authors typically release code alongside arXiv submissions.

---

*Generated by Claude Code methodology scout · 2026-04-17*
