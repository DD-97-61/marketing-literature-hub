# IS Methods Arsenal Scan — 2026-04-17

**Journals scanned:** MISQ, ISR, JMIS, DSS, JAIS, Information & Management, EJIS  
**Keywords:** text mining, deep learning, causal inference, causal ML, network analysis, NLP, LLM, computer vision, time series, panel data, ensemble methods, design science  
**Search window:** Expanded to ~90 days (Jan–Apr 2026); no papers meeting method-novelty criteria were found in the strict 7- or 14-day windows for these journals. All papers below are verified.

---

### Causal Machine Learning in Information Systems Research
- **Authors/Journal/Year:** von Zahn M., Güler A., Pfeiffer J. et al. / *Business & Information Systems Engineering* (BISE) / 2026  
  DOI: 10.1007/s12599-026-00999-x  
  ⚠️ *BISE is not in the primary target list but is a high-ranked IS journal and this is the most methodologically significant IS paper of the search cycle.*
- **Method introduced/used:** Causal Machine Learning (Causal ML) — double/debiased ML, causal forests (Wager & Athey), meta-learners (S-, T-, X-, R-learner), heterogeneous treatment effect (HTE) estimation
- **Original application context:** IS phenomena requiring causal inference with high-dimensional covariates; sociotechnical system evaluation; organizational decision-making with algorithmic systems
- **Potential marketing application:** Estimate heterogeneous treatment effects of brand campaigns (who responds to which ad, at what exposure level); isolate causal impact of branding investment on purchase probability controlling for confounders; identify consumer segments where brand messaging has differential causal lift; complement A/B tests with observational data via double ML
- **Data requirements / Compatible with secondary data?** Yes — works with observational panel data, transaction logs, social media analytics, loyalty program data; no experiment required if rich covariates available
- **Technical complexity:** High (requires fluency in causal inference + ML; model selection non-trivial)
- **Key innovation:** Overcomes functional-form limitations of traditional econometrics; scales to high-dimensional brand attribute data; separates prediction task from causal estimation task; directly targets heterogeneous effects rather than average effects
- **Python/R packages:** `econml` (Microsoft, Python), `causalml` (Uber, Python), `DoubleML` (R/Python), `dowhy` (Python)
- **Relevance:** ★★★★★

---

### Trustworthiness in Computational Theory Construction: Dimensionalization and Category Surfacing
- **Authors/Journal/Year:** Günther W.A., Joshi M., Constantinides P., Ostern N.K., Rai A. / *MIS Quarterly* / Feb 5, 2026  
  DOI: 10.25300/MISQ/2026/18511
- **Method introduced/used:** Dimensionalization and Category Surfacing (DCS) — a computational text analytics framework for theory construction; combines NLP-based corpus analysis with structured researcher-guided category emergence; treats text corpora structure (not just content) as theoretical load-bearer
- **Original application context:** IS theory-building from large unstructured text datasets (interview transcripts, digital trace data, online archives)
- **Potential marketing application:** Derive brand perception dimensions inductively from consumer-generated text (reviews, social posts, support tickets) rather than imposing a priori scales; construct grounded brand equity theory from real consumer language; discover latent brand meaning structures in cross-cultural corpora
- **Data requirements / Compatible with secondary data?** Yes — designed for secondary text corpora (online reviews, social media, archived interviews, news)
- **Technical complexity:** Medium (requires NLP pipeline + structured qualitative reasoning; not pure ML black-box)
- **Key innovation:** Provides trustworthiness criteria for computationally-derived IS theory — fills gap between pure ML topic modeling (atheoretical) and manual grounded theory (not scalable); introduces primacy-of-lexicon vs. corpus-structure design choice as key methodological fork
- **Python/R packages:** `BERTopic` (Python), `gensim` (LDA/LSA), `spaCy`, `nltk`, `scikit-learn` for pipeline
- **Relevance:** ★★★★

---

### Data Valuation for Vertical Federated Learning: A Model-Free and Privacy-Preserving Method
- **Authors/Journal/Year:** Han X., Wang L. et al. / *MIS Quarterly* Vol. 50(1), pp. 177–210 / March 2026  
  DOI: 10.25300/MISQ/2025/19161
- **Method introduced/used:** FedValue — model-free, privacy-preserving data valuation for vertical federated learning using a novel MShapley-CMI (Marginal Shapley Conditional Mutual Information) metric; federated Shapley value computation without sharing raw data or running ML models
- **Original application context:** Multi-party business data collaboration (e.g., financial default prediction, recommendation systems) where organizations share predictive signals without disclosing proprietary data
- **Potential marketing application:** Quantify fair value of data contributed by different retail partners, loyalty programs, or third-party data vendors to a joint brand analytics model; enable cross-brand syndicated research where each brand contributes data and receives value attribution; opens door to privacy-safe customer data collaboration between complementary brands (e.g., airline + hotel + credit card)
- **Data requirements / Compatible with secondary data?** Yes — works with any tabular secondary data distributed across organizations; no data pooling required
- **Technical complexity:** High (requires understanding of information theory, Shapley values, federated computation)
- **Key innovation:** First model-free approach to vertical FL data valuation — does not require training any ML model to compute data value, making it computationally tractable and model-agnostic; resolves free-rider problem in multi-party marketing data consortiums
- **Python/R packages:** `PySyft` (federated learning), `Flower` (flwr), `TensorFlow Federated`; Shapley: `shap` (Python)
- **Relevance:** ★★★

---

### FAIR: A Design Theory for Artificial Intelligence Fairness
- **Authors/Journal/Year:** Rai A., Tian J., Xue L. / *MIS Quarterly* / Jan 5, 2026  
  DOI: 10.25300/MISQ/2026/17971
- **Method introduced/used:** Design Science — FAIR (Fairness Adaptation through AI-augmented Responsiveness) design theory; artifact-level adaptation through structured human-AI agent collaboration across Representation (data), Learning (model), and Calibration (decision) layers; portfolio-level risk-tiered federated governance
- **Original application context:** AI-automated decision systems (hiring, lending, healthcare) that exhibit persistent fairness tensions across regulatory and societal contexts
- **Potential marketing application:** Design framework for fair AI in consumer targeting — ensures demographic parity in ad targeting, credit scoring, algorithmic pricing; critical for brand risk management as algorithmic discrimination in marketing becomes regulatory target (EU AI Act); applicable to recommendation system design that avoids filter bubbles creating brand exclusion
- **Data requirements / Compatible with secondary data?** Partially — framework is design-oriented; empirical validation requires audit data and decision logs
- **Technical complexity:** Medium (design science framework; implementation complexity varies)
- **Key innovation:** Reframes AI fairness as dynamic sociotechnical paradox (not a one-time fix); introduces human-AI collaboration at each layer of the ML pipeline rather than post-hoc debiasing; provides actionable design principles grounded in IS design theory
- **Python/R packages:** `fairlearn` (Microsoft, Python), `aif360` (IBM, Python), `themis-ml` (Python)
- **Relevance:** ★★★

---

## Search Notes

| Journal | Issues Checked | Methods Papers Found |
|---------|---------------|---------------------|
| MISQ | Vol 50 Issue 1 (Mar 2026) + First Look (Jan–Apr 2026) | 3 verified (FAIR, CTC, FedValue) |
| ISR | Vol 37 Issue 1 (Mar 2026) + Articles in Advance | 0 within method criteria |
| JMIS | Vol 43 Issue 1 (2026) | 0 within method criteria (recent window) |
| DSS | Online first Apr 2026 | 0 verified with method novelty |
| JAIS | Vol 26 Issue 3 (2026) | 0 verified |
| Information & Management | Online first | 0 verified |
| EJIS | Vol 35 Issue 1 (2026) | 0 verified method papers |
| BISE* | Online first 2026 | 1 verified (Causal ML — highest relevance) |

*BISE not in original target list but included due to exceptional methodological relevance.

## Top Picks for Immediate Action

1. **Causal ML (BISE)** — Start with `econml` tutorial; test HTE estimation on existing loyalty/transaction panel data
2. **DCS Method (MISQ)** — Apply to brand review corpora; use BERTopic as DCS-compatible pipeline; develop brand perception dimensions
3. **FedValue (MISQ)** — Relevant if multi-party data partnerships planned; theoretical grounding for data pricing conversations
