# 📊 Unified Narrative Intelligence Pipeline

**Process a PDF once → Canonical Analysis Object (CAO) → Regenerate 3 tiered reports instantly**

This pipeline performs deep rhetorical analysis on any document, extracting six narrative dimensions using a hybrid lexical + NLI approach. After the initial processing, reports can be regenerated with different thresholds without re-running expensive models.

## 🔬 Key Features

- **6 Rhetorical Dimensions** – Moral, Threat, Power, Urgency, Us_vs_Them, Legitimacy
- **Hybrid Scoring** – Lexicon matching (456 curated terms) + NLI validation (BART-large-MNLI)
- **Canonical Analysis Object (CAO)** – Persisted Parquet + JSON fingerprint
- **Instant Report Generation** – Three tiers, no reprocessing after Phase A
- **Named Entity Sentiment** – DistilBERT sentiment on extracted entities
- **Rhetorical Target Extraction** – Verb–object pairs from dependency parsing
- **Topic Modeling & Clustering** – BERTopic + KMeans (with elbow diagnostic)
- **Entity Co‑occurrence Network** – NetworkX graphs and centrality analysis

## 📁 Outputs

All outputs go into a timestamped folder under `outputs/`:


## 🚀 Quick Start

### 1. Install dependencies

```bash
pip install pdfplumber spacy sentence-transformers bertopic umap-learn hdbscan \
            networkx python-docx openpyxl pandas pyarrow matplotlib transformers \
            nltk scikit-learn
python -m spacy download en_core_web_sm

jupyter notebook Unified_Pipeline.ipynb

PDF_PATH   = "path/to/your/document.pdf"
CLIENT_NAME = "ClientA"               # used for output folder
PAGE_START = 1                        # optional page range
PAGE_END   = None                     # None = end of document

┌─────────────────────────────────────────────────────────────────────┐
│  PHASE A — PROCESS ONCE                                             │
│  PDF → Chunks → Embed → Topics → Clusters → Annotate → NLI          │
│                          ↓                                          │
│              canonical_analysis_object.parquet  (CAO)               │
│                                                                     │
│  PHASE B — REPORT ANYTIME (no reprocessing)                         │
│  CAO → Tier 1  filtered high-signal patterns     (t1_report.docx)   │
│      → Tier 2  expanded context + targets        (t2_report.docx)   │
│      → Tier 3  full CAO + NLI + network          (t3_report.docx)   │
└─────────────────────────────────────────────────────────────────────┘
