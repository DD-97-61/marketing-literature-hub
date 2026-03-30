# Comprehensive Variable Checklist for Brand Visual Aesthetics Study
## Based on Published Papers in Top Marketing Journals (2018-2026)

---

## PAPER-BY-PAPER DATA STRUCTURE ANALYSIS

---

### 1. Liu, Dzyabura & Mizik (2020, Marketing Science) — "Visual Listening In"

**Platform:** Instagram
**Sample:** 56 brands (apparel + beverage industries); both company- and consumer-created images
**UGC vs. Brand-Generated:** YES — explicitly distinguished and compared

**Image-Level Features (BrandImageNet CNN output):**
- Multi-label brand perceptual attributes extracted per image, including:
  - "glamorous," "healthy," "rugged," "fun," and additional brand personality dimensions
- Average accuracy rate: ~90%
- Deep CNN (BrandImageNet) trained on labeled brand images

**Post Metadata:** Images tagged with brand names on Instagram

**Key Contribution to Variable List:**
- Brand perceptual attributes (multi-label classification)
- Comparison of brand image as portrayed in UGC vs. firm-generated content
- Brand-level aggregated image scores

---

### 2. Philp, Jacobson & Pancer (2022, JBR) — "Predicting Social Media Engagement with Computer Vision"
*(Note: The user referenced "Braun, Batt, Rauschnabel, Keiderling" but the JBR 2022 computer vision engagement paper is by Philp, Jacobson & Pancer)*

**Platform:** Instagram (restaurant accounts)
**Sample:** Restaurants' Instagram posts (exact N not available from abstracts)

**Dependent Variables:**
- Number of likes
- Number of comments

**Independent Variables:**
- Food typicality (operationalized via Google Vision AI confidence scores)
  - Higher confidence = more typical-appearing food

**Mediator:**
- Processing fluency / positive affect

**Computer Vision Tool:** Google Cloud Vision API
- Label detection with confidence scores

**Key Contribution to Variable List:**
- Google Vision API confidence scores as continuous IV
- Processing fluency as mediating mechanism

---

### 3. Affonso & Janiszewski (2023, Journal of Marketing) — "Marketing by Design"

**Platform:** Lab experiments + field experiments + industry data (NOT social media scraping)
**Sample:** Multiple studies — lab experiments with manipulated stimuli, field experiment with perfume ads, industry brand valuation data

**Design Variables Manipulated (Perceptual Structure Dimensions):**
- Proximity (spacing of visual elements)
- Similarity (visual consistency of elements)
- Symmetry (mirrored arrangement)
- Balance
- Geometric regularity

**Dependent Variables:**
- Ad click-through rates (field experiment)
- Consumer product/service selection behavior
- Brand financial valuation
- Customer-based brand equity

**Moderator:**
- Brand positioning (utilitarian vs. hedonic)

**Key Contribution to Variable List:**
- Perceptual structure dimensions (proximity, similarity, symmetry, balance, regularity)
- Structured vs. unstructured perceptions
- Utilitarian vs. hedonic positioning as moderator

---

### 4. Peng, Eisend & Chen (2025, Journal of Marketing) — Meta-Analysis of Product Visual Aesthetics

**Type:** Meta-analysis of 727 effect sizes from 263 independent samples (1993-2024)

**Aesthetic Properties Coded (Antecedents of PVA):**

*Organizational Properties:*
- Harmony (strongest effect)
- Balance
- Symmetry
- Proportion
- Unity/coherence

*Meaningful Properties:*
- Novelty
- Typicality

**Dependent Variables Coded:**
- Product visual aesthetics (PVA) — overall perception
- Consumer attitudes
- Consumer behaviors (purchase intention, WOM, etc.)

**Moderator Categories (5 groups):**
1. **Brand factors:** brand familiarity
2. **Product factors:** product quality level
3. **Communication factors:** aesthetic object type
4. **Consumer factors:** gender, individualism
5. **Environmental factors:** economic growth, consumption publicity, income inequality

**Methodological Control Variables:**
- Effect size type (partial vs. bivariate correlation)
- Sample type (student vs. non-student)
- Study type (between-subjects experiment or not)
- Effect size precision
- Publication status (published vs. unpublished)
- Publication quality (top journals vs. others)

**Key Contribution to Variable List:**
- Complete taxonomy of aesthetic properties
- Five moderator groups for contextual variables
- Harmony, balance, symmetry, proportion, unity, novelty, typicality

---

### 5. Li & Zhang (2024, Journal of Advertising) — "Computer Vision Models for Image Analysis in Advertising Research"

**Type:** Methodological review/framework paper (not empirical data collection)

**Three Categories of Image Analysis:**
1. Content and objects
2. Style and design
3. People and emotion

**Nine Types of Image Analysis (taxonomy of extractable features):**
- Object detection / recognition
- Scene recognition / classification
- Text recognition (OCR in images)
- Color analysis (palettes, distributions)
- Style/design classification
- Aesthetic quality evaluation
- Face detection
- Emotion/sentiment detection from faces
- Action/pose recognition

**12 Computer Vision Models Reviewed:**
- 9 single-functional models (specialized for one type)
- 3 multi-functional models (GPT-4V, Gemini, etc.)
- Compared on: capability, accuracy, availability, usability

**Key Contribution to Variable List:**
- Authoritative taxonomy of 9 image feature types
- Practical model selection guide for each feature type

---

## ADDITIONAL KEY PAPERS (2020-2026)

---

### 6. Hartmann, Heitmann, Schamp & Netzer (2021, JMR) — "The Power of Brand Selfies"

**Platform:** Twitter (92%, ~214K images) + Instagram (8%, ~43K images)
**Sample:** 185 brands, 250,000+ brand-image posts

**Dependent Variables:**
- Number of likes (count)
- Number of comments (count)
- Expressed purchase intentions (from comment text, via NLP)

**Independent Variables (Image Types via CNN):**
- Brand selfie (invisible consumer holding branded product)
- Consumer selfie (consumer face + brand)
- Packshot (standalone product image)

**Statistical Model:** Negative binomial regression (count data with overdispersion)

**Key Contribution to Variable List:**
- Image type classification (selfie vs. packshot)
- Purchase intention extraction from comment text via NLP
- UGC focus with 185-brand cross-industry dataset

---

### 7. Overgoor, Rand, van Dolen & Mazloom (2022, IJRM) — "Simplicity Is Not Key"

**Platform:** Social media (firm-generated posts)

**Image Features — Six Measures in Two Categories:**

*Feature Complexity (pixel-level):*
- Color variation
- Luminance variation
- Edge density

*Design Complexity (structured/design-level):*
- Number of objects
- Irregularity of object arrangement
- Asymmetry of object arrangement

**Dependent Variable:**
- Number of likes

**Key Finding:** Inverted U-shape for feature complexity; regular U-shape for design complexity

**Key Contribution to Variable List:**
- Six interpretable visual complexity measures
- Feature vs. design complexity decomposition

---

### 8. Nanne, Antheunis, Van Der Lee, Postma, Wubben & Van Noort (2020, J. Interactive Marketing) — "Computer Vision to Analyze Brand-Related UGC"

**Platform:** Instagram
**Sample:** 21,738 Instagram images, 24 brands

**Computer Vision Models Compared:**
- YOLOV2 (object detection)
- Google Cloud Vision API (multi-label)
- Clarifai (multi-label)

**Features Extracted:** Object detection labels (object names)
**Content:** Brand-related UGC specifically

**Key Contribution to Variable List:**
- Benchmark of CV model accuracy for brand UGC
- Object detection label vocabulary from three models

---

### 9. Klostermann, Plumeyer, Boger & Decker (2018, IJRM) — "Extracting Brand Information from Social Networks"

**Platform:** Instagram
**Data Integration:** Image + Text + Social tagging data

**Features:**
- Image content analysis via computer vision
- Text analysis (captions, comments)
- Social tags (hashtags, user tags)
- Brand perceptions visualized as associative networks

**Key Contribution to Variable List:**
- Multimodal approach: image + text + tags
- Associative network visualization of brand perceptions

---

### 10. Dzyabura & Peres (2021, Journal of Marketing) — "Visual Elicitation of Brand Perception"

**Sample:** 4,743 collages from 1,851 respondents for 303 large U.S. brands

**Features:**
- Unsupervised ML on consumer-created image collages
- Brand associations extracted from visual content
- Combined with brand personality scales and brand equity measures

**Key Contribution to Variable List:**
- Visual brand association measurement methodology
- Integration with established brand perception measures

---

### 11. Color Complexity Study (2024, IJRM) — "Standing Out from the Crowd"

**Platform:** Facebook (two proprietary datasets from distinct industries)
**Method:** Field data + biometric eye-tracking experiments (4 studies)

**Independent Variable:**
- Color complexity (pixel-level color variation)

**Dependent Variable:**
- User engagement

**Control/Moderating Variables:**
- Time of day
- Image height (screen space)
- Text sentiment
- Text complexity

**Key Contribution to Variable List:**
- Color complexity measurement
- Time-of-day as moderator
- Text sentiment interaction with image features

---

### 12. "Luxury in Focus" (2025, JBR) — Image Fluency and Luxury Brand Engagement

**Platform:** Instagram
**Sample:** 30,770 Instagram posts from leading luxury brands

**Image Fluency Dimensions (4 computed metrics):**
- Simplicity
- Self-similarity (fractal-like patterns)
- Symmetry
- Contrast

**Dependent Variable:** User engagement (likes/comments)
**Method:** Explainable AI + image metrics

**Key Contribution to Variable List:**
- Four computable image fluency metrics
- Product-type moderation of symmetry effects

---

### 13. Dang, Kwan, Jia & Shi (2026, JMR) — "When Words Meet Visuals"

**Platform:** Facebook + Instagram
**Sample:** 34,610 organic brand posts

**Features Extracted:**
- Visual features (via computer vision)
- Textual features (via NLP)
- Overlay text ratio vs. pictorial content ratio
- Content composition balance

**Dependent Variables:** Likes, comments

**Method:** Confounding-and-cluster-robust causal forests model

**Key Contribution to Variable List:**
- Text-to-image ratio as key variable
- Overlay text measurement
- Causal forest methodology for engagement prediction

---

### 14. CTV-CBBE Framework (2025, JBR) — "Computer Vision in Branding"

**Type:** Conceptual framework / integrative review

**Visual Feature Typology for Branding:**
- Layout/composition
- Color (palette, harmony, contrast)
- Emotion (facial expressions, sentiment)
- Context (scene, setting, background)
- Brand elements (logo, product, packaging)
- Visual harmony
- Brand storytelling elements

**Maps to Brand Equity Levels:**
- Brand awareness
- Brand associations
- Brand responses
- Brand loyalty

---

## COMPREHENSIVE VARIABLE CHECKLIST

### A. POST-LEVEL METADATA (must collect per post)

| # | Variable | Type | Source |
|---|----------|------|--------|
| 1 | Post ID (unique identifier) | String | API/scrape |
| 2 | Platform (Instagram/Facebook/Twitter/Weibo) | Categorical | API |
| 3 | Timestamp / date posted | DateTime | API |
| 4 | Day of week | Categorical | Derived |
| 5 | Time of day / hour | Continuous | Derived |
| 6 | Post type (image/carousel/video/reel) | Categorical | API |
| 7 | Number of images in post (carousel count) | Count | API |
| 8 | Number of likes | Count | API |
| 9 | Number of comments | Count | API |
| 10 | Number of shares / reposts | Count | API (if available) |
| 11 | Number of saves | Count | API (if available) |
| 12 | Number of views (video/reel) | Count | API (if available) |
| 13 | Engagement rate (likes+comments / followers) | Continuous | Derived |
| 14 | Post URL / permalink | String | API |
| 15 | Image URL(s) | String | API |
| 16 | Caption text (full) | Text | API |
| 17 | Caption length (characters) | Count | Derived |
| 18 | Caption word count | Count | Derived |
| 19 | Number of hashtags | Count | Derived |
| 20 | List of hashtags | Text array | Derived |
| 21 | Number of user mentions (@tags) | Count | Derived |
| 22 | Number of tagged users in image | Count | API |
| 23 | Location tag (if any) | String | API |
| 24 | Contains URL in caption (binary) | Binary | Derived |
| 25 | Sponsored/paid partnership indicator | Binary | API |
| 26 | Content source: UGC vs. brand-generated | Categorical | Manual/derived |

### B. ACCOUNT/BRAND-LEVEL METADATA

| # | Variable | Type | Source |
|---|----------|------|--------|
| 27 | Brand name | String | API |
| 28 | Brand handle / username | String | API |
| 29 | Number of followers (at time of post) | Count | API |
| 30 | Number of following | Count | API |
| 31 | Number of total posts | Count | API |
| 32 | Account verified status | Binary | API |
| 33 | Business/professional account flag | Binary | API |
| 34 | Brand category / industry | Categorical | Manual coding |
| 35 | Brand positioning (utilitarian vs. hedonic) | Categorical | Manual coding |
| 36 | Brand familiarity / awareness level | Continuous | Survey or proxy |
| 37 | Brand quality tier (luxury/mass-market) | Categorical | Manual coding |
| 38 | Brand origin country | Categorical | Manual coding |
| 39 | Bio text | Text | API |
| 40 | External URL | String | API |

### C. IMAGE-LEVEL FEATURES — COMPUTATIONAL / COMPUTER VISION

#### C1. Low-Level Pixel Features

| # | Variable | Type | Source |
|---|----------|------|--------|
| 41 | Image width (pixels) | Continuous | Image metadata |
| 42 | Image height (pixels) | Continuous | Image metadata |
| 43 | Aspect ratio | Continuous | Derived |
| 44 | File size (JPEG, proxy for visual richness) | Continuous | Image metadata |
| 45 | Image resolution (DPI) | Continuous | Image metadata |
| 46 | Average brightness / luminance | Continuous | CV |
| 47 | Brightness variation (std dev) | Continuous | CV |
| 48 | Average saturation | Continuous | CV |
| 49 | Saturation variation | Continuous | CV |
| 50 | Average hue | Continuous | CV |
| 51 | Color temperature / warmth | Continuous | CV |
| 52 | Colorfulness index | Continuous | CV |
| 53 | Color complexity (pixel-level color variation) | Continuous | CV |
| 54 | Number of unique colors / color diversity | Count | CV |
| 55 | Dominant color(s) (RGB/HSV) | Categorical/Vector | CV |
| 56 | Color palette (top 5-10 colors) | Vector | CV |
| 57 | Color harmony score | Continuous | CV |
| 58 | Edge density | Continuous | CV |
| 59 | Contrast ratio | Continuous | CV |

#### C2. Visual Complexity Features (per Overgoor et al. 2022)

| # | Variable | Type | Source |
|---|----------|------|--------|
| 60 | Feature complexity — color variation | Continuous | CV |
| 61 | Feature complexity — luminance variation | Continuous | CV |
| 62 | Feature complexity — edge density | Continuous | CV |
| 63 | Design complexity — number of objects | Count | CV (object detection) |
| 64 | Design complexity — irregularity of arrangement | Continuous | CV |
| 65 | Design complexity — asymmetry of arrangement | Continuous | CV |

#### C3. Image Fluency Features (per Luxury in Focus 2025)

| # | Variable | Type | Source |
|---|----------|------|--------|
| 66 | Simplicity score | Continuous | CV |
| 67 | Self-similarity score (fractal dimension) | Continuous | CV |
| 68 | Symmetry score | Continuous | CV |
| 69 | Contrast score | Continuous | CV |

#### C4. Perceptual Structure Features (per Affonso & Janiszewski 2023)

| # | Variable | Type | Source |
|---|----------|------|--------|
| 70 | Proximity of visual elements | Continuous | CV/manual |
| 71 | Similarity of visual elements | Continuous | CV/manual |
| 72 | Symmetry (Gestalt) | Continuous | CV |
| 73 | Balance of composition | Continuous | CV |
| 74 | Geometric regularity | Continuous | CV |

#### C5. Aesthetic Quality (per Peng, Eisend & Chen 2025)

| # | Variable | Type | Source |
|---|----------|------|--------|
| 75 | Overall aesthetic quality score | Continuous | CV (NIMA/aesthetic CNN) |
| 76 | Harmony score | Continuous | CV |
| 77 | Balance score | Continuous | CV |
| 78 | Proportion score | Continuous | CV |
| 79 | Unity/coherence score | Continuous | CV |
| 80 | Novelty/originality score | Continuous | CV |
| 81 | Typicality score | Continuous | CV |

#### C6. Content Detection (per Li & Zhang 2024 taxonomy)

| # | Variable | Type | Source |
|---|----------|------|--------|
| 82 | Object labels (full list) | Multi-label | Google Vision / YOLO |
| 83 | Object confidence scores | Continuous per label | CV API |
| 84 | Scene/setting classification | Categorical | Scene recognition model |
| 85 | Face detected (binary) | Binary | CV |
| 86 | Number of faces | Count | CV |
| 87 | Face emotion/sentiment | Categorical | CV (emotion model) |
| 88 | Person/people present (binary) | Binary | CV |
| 89 | Number of people | Count | CV |
| 90 | Text in image detected (binary) | Binary | OCR |
| 91 | Text in image content | Text | OCR |
| 92 | Overlay text area ratio (text pixels / total) | Continuous | CV |
| 93 | Brand logo detected (binary) | Binary | Logo detection |
| 94 | Brand logo area / prominence | Continuous | CV |
| 95 | Product visible (binary) | Binary | CV/manual |
| 96 | Product centrality in frame | Continuous | CV |
| 97 | Background type (indoor/outdoor/studio) | Categorical | Scene model |
| 98 | Food item detected (if applicable) | Binary | CV |
| 99 | Food typicality score | Continuous | Google Vision confidence |

#### C7. Image Type Classification (per Hartmann et al. 2021)

| # | Variable | Type | Source |
|---|----------|------|--------|
| 100 | Image type: packshot | Binary | CV/CNN |
| 101 | Image type: consumer selfie | Binary | CV/CNN |
| 102 | Image type: brand selfie | Binary | CV/CNN |
| 103 | Image type: lifestyle/scene | Binary | CV/CNN |
| 104 | Image type: text-only / quote | Binary | CV |
| 105 | Image type: meme / user-generated | Binary | Manual |

#### C8. Brand Perceptual Attributes (per Liu et al. 2020 BrandImageNet)

| # | Variable | Type | Source |
|---|----------|------|--------|
| 106 | "Glamorous" attribute score | Continuous | CNN |
| 107 | "Healthy" attribute score | Continuous | CNN |
| 108 | "Rugged" attribute score | Continuous | CNN |
| 109 | "Fun" attribute score | Continuous | CNN |
| 110 | Additional brand personality dimensions | Continuous | CNN |
| 111 | Brand image consistency score (across posts) | Continuous | Derived |

### D. TEXT / CAPTION FEATURES (NLP)

| # | Variable | Type | Source |
|---|----------|------|--------|
| 112 | Caption sentiment (positive/negative/neutral) | Categorical | NLP |
| 113 | Caption sentiment polarity score | Continuous | NLP |
| 114 | Caption text complexity | Continuous | NLP |
| 115 | Caption topic / theme | Categorical | LDA / topic model |
| 116 | Emoji count | Count | Derived |
| 117 | Call-to-action present | Binary | NLP/manual |
| 118 | Question in caption | Binary | NLP |
| 119 | Image-text congruence score | Continuous | Multimodal model |
| 120 | Promotional language indicator | Binary | NLP/manual |

### E. COMMENT-LEVEL FEATURES (if collecting comments)

| # | Variable | Type | Source |
|---|----------|------|--------|
| 121 | Number of comments per post | Count | API |
| 122 | Average comment sentiment | Continuous | NLP |
| 123 | Purchase intention expressed in comments | Binary/count | NLP (per Hartmann 2021) |
| 124 | Brand mention in comments | Count | NLP |

### F. CONTROL VARIABLES (commonly used across studies)

| # | Variable | Type | Justification |
|---|----------|------|---------------|
| 125 | Post age at time of data collection | Continuous | Likes/comments accumulate over time |
| 126 | Follower count at time of post | Count | Normalizes engagement |
| 127 | Day of week | Categorical | Posting timing effects |
| 128 | Hour of day | Continuous | Time-of-day engagement patterns |
| 129 | Post type (image vs video vs carousel) | Categorical | Format effect |
| 130 | Caption length | Continuous | Text effort signal |
| 131 | Number of hashtags | Count | Discovery/reach |
| 132 | Brand category / industry | Categorical | Industry norms |
| 133 | Brand quality tier (luxury vs mass) | Categorical | Per Gao et al. 2026 |
| 134 | Brand positioning (utilitarian vs hedonic) | Categorical | Per Affonso & Janiszewski 2023 |
| 135 | Brand familiarity | Continuous | Per Peng et al. 2025 |
| 136 | UGC vs brand-generated content | Binary | Per Liu et al. 2020 |
| 137 | Sponsored/paid indicator | Binary | Disclosure effects |
| 138 | Number of images in post (carousel) | Count | Multi-image effect |
| 139 | Image height / screen prominence | Continuous | Per color complexity paper |
| 140 | Text sentiment of caption | Continuous | Interacts with visual features |
| 141 | Economic indicators (for cross-country) | Continuous | Per Peng et al. 2025 |

### G. DERIVED / COMPUTED VARIABLES

| # | Variable | Type | Source |
|---|----------|------|--------|
| 142 | Engagement rate = (likes + comments) / followers | Continuous | Standard metric |
| 143 | Like-to-comment ratio | Continuous | Engagement quality |
| 144 | Visual consistency across brand feed | Continuous | Brand-level aggregate |
| 145 | Posting frequency (posts per week/month) | Continuous | Brand activity level |
| 146 | Brand image gap (firm vs UGC portrayal) | Continuous | Per Liu et al. 2020 |

---

## RECOMMENDED COMPUTER VISION TOOLS (per Li & Zhang 2024)

| Task | Recommended Models |
|------|--------------------|
| Object detection | YOLO (v5/v8), Google Cloud Vision API |
| Scene recognition | Places365-CNN |
| Face detection + emotion | Azure Face API, DeepFace |
| Text recognition (OCR) | Google Vision OCR, Tesseract |
| Color analysis | Custom (OpenCV HSV extraction) |
| Aesthetic quality | NIMA (Neural Image Assessment) |
| Style classification | Fine-tuned CNN |
| Multi-purpose (all above) | GPT-4V, Gemini, Claude Vision |
| Brand/logo detection | LogoDet-3K models, Google Vision |

---

## DATA COLLECTION PRIORITY TIERS

### TIER 1 — MUST COLLECT (used in nearly all studies)
- Post ID, timestamp, platform
- Number of likes, number of comments
- Follower count (at time of post or time of scrape)
- Caption text (full)
- Post type (image/carousel/video)
- Image file(s) (full resolution)
- Brand name, category, verified status

### TIER 2 — STRONGLY RECOMMENDED (used in most studies)
- Hashtag list and count
- UGC vs. brand-generated indicator
- Location tag
- Number of tagged users
- Image dimensions and file size
- Caption sentiment
- Image-text congruence

### TIER 3 — IMPORTANT FOR VISUAL AESTHETICS (computed post-collection)
- Color features (dominant colors, complexity, harmony, warmth, saturation, brightness)
- Visual complexity (feature + design components)
- Image fluency (simplicity, self-similarity, symmetry, contrast)
- Aesthetic quality score (NIMA)
- Object detection labels
- Face/person detection
- Scene classification
- Brand logo presence and prominence

### TIER 4 — ADVANCED / STUDY-SPECIFIC
- Brand perceptual attributes (BrandImageNet-style)
- Overlay text ratio
- Perceptual structure measures (proximity, similarity, balance)
- Purchase intentions from comment text
- Food typicality (if food context)
- Cross-post brand visual consistency

---

## NOTES ON SCRAPING METHODOLOGY

1. **Instagram API limitations**: Instagram Graph API requires business account authorization; academic researchers typically use CrowdTangle (now deprecated) or approved academic access
2. **Historical follower counts**: Most studies collect follower counts at time of scraping; some use Wayback Machine or third-party trackers for historical data
3. **Post age correction**: All engagement counts must be normalized by post age (time since posting)
4. **Image storage**: Download and store full-resolution images for CV processing; do NOT rely on thumbnail URLs
5. **Rate limiting**: Collect data in batches with appropriate delays to avoid blocking
6. **Ethics/IRB**: Most published studies note IRB exemption for publicly available social media data; check institution policy
7. **Carousel handling**: Decide whether to analyze first image only, all images, or treat carousel as a single unit

---

*Generated: 2026-03-29*
*Based on systematic review of 14 published papers (2018-2026) from Marketing Science, Journal of Marketing, JMR, IJRM, JBR, J. Advertising, and J. Interactive Marketing*
