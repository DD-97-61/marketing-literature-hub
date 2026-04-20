# Data Source Scan — 2026-04-20

**Scout run:** Daily automated scan | **Total verified sources:** 15
**Categories covered:** Social Media · E-commerce · Academic · Government/Industry · Research Tools

---

## 🔵 Social Media Data

### TikTok Research API (Official)
- **Provider:** TikTok for Developers / ByteDance
- **Type:** API (JSON)
- **Volume:** Public content, accounts, hashtags — no volume cap published; rate-limited per endpoint
- **Geographic:** US + Europe (DSA-compliant); separate Douyin API for China
- **Language:** Multilingual
- **Access method:** Application required — vetted academic status via Digital Services Coordinator (EU) or direct application (US non-profit universities)
- **Cost:** Free for approved academics
- **Recency:** Live/real-time; policy updated 2024–2025 under DSA requirements
- **URL:** https://developers.tiktok.com/products/research-api/
- **Potential research uses:**
  - Brand hashtag virality and cross-platform narrative diffusion
  - Consumer engagement patterns with branded short-video content
- **Relevance:** ★★★★★

---

### Twitter/X Academic Research API
- **Provider:** X Corp (formerly Twitter)
- **Type:** API (JSON/REST)
- **Volume:** Up to full-archive search; tweet-level with engagement metadata
- **Geographic:** Global
- **Language:** Multilingual (including Chinese)
- **Access method:** Application to X Developer Portal; academic elevated access requires institutional email
- **Cost:** Paid (commercial tiers start high ~$42K/month); academic pricing available on request — severely restricted since 2023. Pay-per-use model in closed beta as of Dec 2025.
- **Recency:** Live + historical archive
- **URL:** https://developer.x.com/en/use-cases/do-research/academic-research
- **Potential research uses:**
  - Brand sentiment tracking and crisis communication analysis
  - Consumer discourse around product launches (English/global markets)
- **Relevance:** ★★★ ⚠️ **FLAG: High cost severely limits academic use; EU DSA pressure has not meaningfully reopened free access as of 2025. Budget/institutional support required.**

---

### Instagram Graph API v25 (Meta)
- **Provider:** Meta Platforms
- **Type:** API (REST/JSON)
- **Volume:** Per-account data; analytics limited to top 45 audience segments
- **Geographic:** Global
- **Language:** Multilingual
- **Access method:** Meta for Developers app registration; Business/Creator accounts required
- **Cost:** Free (within rate limits); no academic tier
- **Recency:** Live; Graph API v25.0 released February 2026
- **URL:** https://developers.facebook.com/blog/post/2026/02/18/introducing-graph-api-v25-and-marketing-api-v25/
- **Potential research uses:**
  - Brand aesthetic/visual content analysis via media endpoints
  - Influencer marketing engagement benchmarking
- **Relevance:** ★★★★ ⚠️ Jan 2025: video_views, email_contacts, profile_views deprecated in v21+. Follower metrics hidden for accounts <100 followers.

---

### Xiaohongshu (RED) — AIGC Comments & Posts Dataset
- **Provider:** GitHub / community researcher (coralr-1)
- **Type:** Scraped/curated (CSV)
- **Volume:** User comments and posts on AIGC topics; exact count not published
- **Geographic:** China
- **Language:** Chinese (Simplified)
- **Access method:** Free download via GitHub
- **Cost:** Free
- **Recency:** Collected ~2024; static snapshot
- **URL:** https://github.com/coralr-1/Xiaohongshu-AIGC-Comments-and-Posts-Dataset
- **Potential research uses:**
  - Chinese consumer attitudes toward AI-generated brand content
  - Sentiment analysis of tech/fashion discourse on lifestyle platform
- **Relevance:** ★★★★ ⚠️ **China data privacy note:** Collection method may not fully comply with PIPL (Personal Information Protection Law, 2021). Verify IRB/ethics clearance before use.

---

### RedNote-Vibe Dataset (Xiaohongshu longitudinal)
- **Provider:** Academic paper release (arXiv 2509.22055)
- **Type:** Research dataset (structured)
- **Volume:** 5-year longitudinal; pre-LLM era to July 2025; includes likes, comments, collections per post
- **Geographic:** China
- **Language:** Chinese (Simplified)
- **Access method:** arXiv paper; data availability per paper supplementary
- **Cost:** Free (academic)
- **Recency:** Coverage through July 2025
- **URL:** https://arxiv.org/html/2509.22055v1
- **Potential research uses:**
  - Longitudinal brand content evolution on Chinese lifestyle platform
  - AI-generated vs. authentic consumer content discrimination
- **Relevance:** ★★★★★

---

### Weibo Open API
- **Provider:** Sina Weibo
- **Type:** API (REST/JSON)
- **Volume:** Public posts, user profiles, trending topics; rate-limited
- **Geographic:** China
- **Language:** Chinese (Simplified)
- **Access method:** Developer application at open.weibo.com; academic researchers require commercial license approval
- **Cost:** Free tier available (limited); commercial/research tier by application
- **Recency:** Live; API policies last reviewed 2023–2024
- **URL:** https://open.weibo.com/
- **Potential research uses:**
  - Chinese brand social listening and crisis tracking
  - Consumer sentiment on domestic vs. foreign brands
- **Relevance:** ★★★★ ⚠️ **China data privacy note:** PIPL compliance required. Weibo restricts bulk export; academic applications have long approval times. Third-party scraping violates ToS.

---

## 🟡 E-commerce Data

### Amazon Reviews 2023 (McAuley Lab / UCSD)
- **Provider:** McAuley Lab, UC San Diego
- **Type:** Research dataset (JSON/Parquet)
- **Volume:** ~571M reviews; May 1996 – September 2023; 33 product categories
- **Geographic:** US (primarily)
- **Language:** English
- **Access method:** Direct download (website) + Hugging Face Hub
- **Cost:** Free
- **Recency:** Static snapshot; last updated September 2023
- **URL:** https://amazon-reviews-2023.github.io/
- **Hugging Face:** https://huggingface.co/datasets/McAuley-Lab/Amazon-Reviews-2023
- **Potential research uses:**
  - Brand equity signals from large-scale product review sentiment
  - Cross-category brand loyalty and switching behavior from purchase histories
- **Relevance:** ★★★★★

---

### JD.com Product Reviews Dataset (Yongfeng Zhang)
- **Provider:** Academic release — Yongfeng Zhang (Rutgers)
- **Type:** Research dataset (CSV/JSON)
- **Volume:** ~60M reviews; ~2M users; 100K+ products; Jan 2011 – Mar 2014; 15 product categories
- **Geographic:** China
- **Language:** Chinese (Simplified)
- **Access method:** Request via researcher's website
- **Cost:** Free (academic)
- **Recency:** Historical (2011–2014); not updated
- **URL:** http://yongfeng.me/dataset/
- **Potential research uses:**
  - Chinese e-commerce brand reputation and review sentiment (structured positive/negative/overall sub-reviews)
  - Price sensitivity and consumer switching across domestic brands
- **Relevance:** ★★★★ ⚠️ Data is dated (pre-2015); valuable for longitudinal baseline but not current market analysis.

---

### Kaggle — Social Media & Consumer Behavior (2025)
- **Provider:** Kaggle / Jocelyn Dumlao (community)
- **Type:** Curated dataset (CSV)
- **Volume:** Moderate (exact row count not published)
- **Geographic:** Global (survey-style)
- **Language:** English
- **Access method:** Free download (Kaggle account required)
- **Cost:** Free
- **Recency:** Published November 2025
- **URL:** https://www.kaggle.com/datasets/jocelyndumlao/social-media-and-consumer-behavior-2025
- **Potential research uses:**
  - Algorithm influence on consumer purchase intent across platforms
  - Social commerce adoption patterns and platform preference
- **Relevance:** ★★★

---

### Kaggle — Marketing Campaign Performance Dataset
- **Provider:** Kaggle / Manisha Bhatt (community)
- **Type:** Curated dataset (CSV)
- **Volume:** Moderate
- **Geographic:** Mixed
- **Language:** English
- **Access method:** Free download (Kaggle account required)
- **Cost:** Free
- **Recency:** 2024–2025
- **URL:** https://www.kaggle.com/datasets/manishabhatt22/marketing-campaign-performance-dataset
- **Potential research uses:**
  - Cross-channel marketing ROI benchmarking
  - Campaign effectiveness modeling for brand awareness metrics
- **Relevance:** ★★★

---

## 🟢 Academic Repositories

### ICPSR — Survey of Consumer Attitudes & Behavior (Michigan/Thomson Reuters)
- **Provider:** ICPSR, University of Michigan
- **Type:** Survey microdata (SAS/SPSS/Stata/R)
- **Volume:** Longitudinal panel; monthly waves; continuous since 1940s
- **Geographic:** US
- **Language:** English
- **Access method:** Free ICPSR account (institutional membership required for some studies)
- **Cost:** Free with ICPSR membership (most universities)
- **Recency:** Ongoing monthly releases; 2025 waves available
- **URL:** https://www.icpsr.umich.edu/web/ICPSR/series/00054/variables
- **Potential research uses:**
  - Consumer sentiment index as macro control variable in brand studies
  - Longitudinal tracking of discretionary purchase intention
- **Relevance:** ★★★★

---

### Harvard Dataverse — IRI Marketing Data Set
- **Provider:** Harvard Dataverse / IRI (Information Resources Inc.)
- **Type:** Scanner/panel data (structured)
- **Volume:** 5–6 years; 30 CPG categories; 49 markets (store level); 2 markets (consumer panel)
- **Geographic:** US
- **Language:** English
- **Access method:** Free download via Harvard Dataverse (registration required)
- **Cost:** Free
- **Recency:** Historical (approx. 2001–2011 vintage); static
- **URL:** https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/YQQSLM
- **Potential research uses:**
  - Brand-level price elasticity and promotional response
  - Market structure and competitive positioning for CPG brands
- **Relevance:** ★★★★

---

### WRDS (Wharton Research Data Services)
- **Provider:** Wharton School, University of Pennsylvania
- **Type:** Multi-database hub (financial, marketing, consumer)
- **Volume:** Varies by dataset; DMEF dataset ~100K customers with full purchase histories
- **Geographic:** US/Global depending on dataset
- **Language:** English
- **Access method:** Institutional subscription required; individual registration via affiliated university
- **Cost:** Institutional subscription (free for users at subscribing universities)
- **Recency:** Ongoing; datasets updated continuously
- **URL:** https://wrds-www.wharton.upenn.edu/
- **Potential research uses:**
  - Direct marketing response modeling and CLV estimation
  - Linking financial brand value data with consumer behavior outcomes
- **Relevance:** ★★★★

---

## 🔴 Government / Industry Rankings

### China National Bureau of Statistics (NBS) — Household Income & Consumption
- **Provider:** National Bureau of Statistics of China (国家统计局)
- **Type:** Official statistics (Excel/PDF tables)
- **Volume:** 160,000 households; 2,000 counties; 31 provinces; quarterly releases
- **Geographic:** China (national + provincial)
- **Language:** Chinese + English (key releases)
- **Access method:** Free direct download from official portal
- **Cost:** Free
- **Recency:** Q1 2026 data released April 2026; continuous quarterly updates
- **URL (English):** https://www.stats.gov.cn/english/PressRelease/
- **URL (Data portal):** https://data.stats.gov.cn/
- **Potential research uses:**
  - Macro consumer spending patterns as context for brand market sizing
  - Regional consumption inequality affecting brand penetration strategies
- **Relevance:** ★★★★

---

### Interbrand Best Global Brands 2025
- **Provider:** Interbrand
- **Type:** Brand valuation report (PDF + structured data)
- **Volume:** Top 100 global brands; annual valuation + strength score
- **Geographic:** Global
- **Language:** English
- **Access method:** Free download (registration/email required)
- **Cost:** Free (report); raw data not released
- **Recency:** 2025 report published; total portfolio value $3.6 trillion (+4.4% YoY)
- **URL:** https://interbrand.com/best-global-brands/global-2025-report-download/
- **Potential research uses:**
  - Brand valuation longitudinal trends for event studies
  - Correlating brand strength scores with financial/consumer metrics
- **Relevance:** ★★★★

---

### Kantar BrandZ Most Valuable Global Brands 2025
- **Provider:** Kantar / WPP
- **Type:** Brand equity report + BrandSnapshot data explorer
- **Volume:** Top 100 global brands; brand value + equity decomposition
- **Geographic:** Global (separate China, India, LatAm rankings)
- **Language:** English
- **Access method:** Free report download; interactive BrandSnapshot tool (free, registration)
- **Cost:** Free (public report); premium data subscription for full dataset
- **Recency:** 2025 report; total top-100 value $10.7 trillion (record high)
- **URL:** https://www.kantar.com/Campaigns/BrandZ/Global
- **Potential research uses:**
  - Brand equity decomposition (meaningful, different, salient dimensions) for academic modeling
  - China-specific brand ranking for local vs. global brand competition research
- **Relevance:** ★★★★★

---

### Brand Finance Global 500 2025
- **Provider:** Brand Finance
- **Type:** Brand valuation ranking (PDF preview; full data licensed)
- **Volume:** 500 most valuable global brands; financial brand value + brand rating
- **Geographic:** Global
- **Language:** English
- **Access method:** Preview PDF free; full data requires purchase/license
- **Cost:** Free preview; paid full data
- **Recency:** 2025 edition
- **URL:** https://static.brandirectory.com/reports/brand-finance-global-500-2025-preview.pdf
- **Potential research uses:**
  - Financial brand valuation as dependent variable in marketing mix studies
  - Cross-method triangulation with Interbrand and BrandZ valuations
- **Relevance:** ★★★★

---

## 🟣 Research Tools & Paper-Released Data

### ChineseNLP (Didi) — Chinese Sentiment Analysis Benchmark Hub
- **Provider:** Didi Research / open source community (GitHub)
- **Type:** NLP benchmark collection (multiple formats)
- **Volume:** Multiple datasets: ChnSentiCorp (1,021 docs), IT168TEST (20K+ reviews), Dianping restaurant reviews, JD Full (shopping reviews), NLPCC 2023 DiaASQ
- **Geographic:** China
- **Language:** Chinese (Simplified)
- **Access method:** Free download via GitHub
- **Cost:** Free
- **Recency:** Repository active; datasets from various years; DiaASQ from 2023
- **URL:** https://github.com/didi/ChineseNLP/blob/master/docs/sentiment_analysis.md
- **Potential research uses:**
  - Chinese consumer review sentiment benchmarking for brand studies
  - Fine-tuning LLMs for Chinese brand perception analysis
- **Relevance:** ★★★★★

---

### SnowNLP — Chinese Text Processing Library
- **Provider:** Open source (GitHub)
- **Type:** Python NLP library
- **Volume:** N/A (tool, not dataset)
- **Geographic:** China-focused
- **Language:** Chinese (Simplified)
- **Access method:** pip install snownlp
- **Cost:** Free (MIT license)
- **Recency:** Maintained; compatible with Python 3.x
- **URL:** https://github.com/isnowfy/snownlp
- **Potential research uses:**
  - Rapid sentiment scoring of Chinese consumer reviews and social posts
  - Preprocessing pipeline for Weibo/RED/Douyin text corpora
- **Relevance:** ★★★★

---

### Kimola NLP Datasets — Customer Feedback (Multi-platform)
- **Provider:** Kimola (GitHub)
- **Type:** Curated NLP datasets (CSV/JSON)
- **Volume:** Reviews from Amazon, Google Business, Trustpilot, Tripadvisor, App Store, Google Play
- **Geographic:** Global
- **Language:** English (primarily)
- **Access method:** Free download via GitHub
- **Cost:** Free
- **Recency:** Ongoing updates
- **URL:** https://github.com/Kimola/nlp-datasets
- **Potential research uses:**
  - Cross-platform brand review sentiment comparison
  - NLP model training for brand perception extraction
- **Relevance:** ★★★

---

*Scan date: 2026-04-20 | Sources verified via web search | 15 datasets/tools cataloged*
