# Changelog

All notable changes to this project will be documented in this file.

The format is based on Keep a Changelog and follows semantic project progression rather than software release numbering.

---

## [0.7.0] - Research Audit Pipeline

### Added

* End-to-end reproducible narrative analysis workflow.
* Structured JSON and CSV export system.
* Claim traceability framework.
* Dataset validation and integrity checks.
* Methodology appendix generation.
* Standardized output schemas for downstream analysis.

### Improved

* Audit reproducibility across multiple document sources.
* Export compatibility with dashboards and external tools.
* Pipeline modularization and phase separation.

### Components

| Component         | Purpose                                       |
| ----------------- | --------------------------------------------- |
| Jupyter Notebook  | Interactive research and analysis environment |
| Pandas            | Structured dataset management                 |
| JSON Export Layer | Machine-readable analysis outputs             |
| CSV Export Layer  | Tabular reporting outputs                     |
| Git/GitHub        | Version control and reproducibility           |

---

## [0.6.0] - Narrative Intelligence Metrics

### Added

* Lexical signal scoring framework.
* Semantic signal analysis workflow.
* Narrative intensity metrics.
* Section-level scoring.
* High-signal chunk identification.
* Entity co-occurrence analysis.

### Added Experimental

* Zero-shot Natural Language Inference (NLI).
* Contradiction and support scoring.
* Narrative relationship mapping.

### Components

| Component             | Purpose                                |
| --------------------- | -------------------------------------- |
| Sentence Transformers | Semantic embeddings                    |
| NLI Models            | Entailment and contradiction detection |
| Network Analysis      | Relationship and co-occurrence mapping |
| Custom Scoring Engine | Narrative signal measurement           |

---

## [0.5.0] - Semantic Analysis Layer

### Added

* Named Entity Recognition (NER).
* Semantic similarity analysis.
* Topic modeling workflow.
* Corpus-level thematic extraction.
* Entity frequency tracking.

### Components

| Component             | Purpose                                  |
| --------------------- | ---------------------------------------- |
| spaCy                 | Entity extraction and linguistic parsing |
| Sentence Transformers | Vector embeddings                        |
| BERTopic              | Topic discovery and clustering           |

### Improvements

* Reduced dependence on keyword-only approaches.
* Introduced semantic representation of document content.
* Enabled concept-level comparison across text segments.

---

## [0.4.0] - Document-Aware Ingestion

### Added

* Section-aware document parsing.
* Table of contents handling.
* Page-range targeting.
* Header and footer suppression.
* Document structure preservation.

### Components

| Component            | Purpose                            |
| -------------------- | ---------------------------------- |
| pdfplumber           | Layout-aware PDF extraction        |
| PyMuPDF (fitz)       | High-performance PDF processing    |
| Custom Parsing Logic | Structural document interpretation |

### Improvements

* Improved extraction fidelity.
* Reduced structural noise.
* Enhanced downstream sentence segmentation accuracy.

---

## [0.3.0] - Claim Extraction Framework

### Added

* Sentence-level claim extraction.
* Claim normalization.
* Claim taxonomy system.
* Rule-based classification framework.

### Claim Categories

* Descriptive
* Predictive
* Causal
* Policy-Predictive
* Weakly Falsifiable
* Unfalsifiable Predictive
* Normative
* Unspecified

### Components

| Component                    | Purpose                  |
| ---------------------------- | ------------------------ |
| Python Classification Engine | Claim categorization     |
| Regular Expression Framework | Pattern extraction       |
| Validation Layer             | Claim consistency checks |

### Improvements

* Formalized analytical units.
* Established traceable claim structure.

---

## [0.2.0] - Structured Text Processing

### Added

* Sentence tokenization pipeline.
* Corpus cleaning workflow.
* Metadata preservation.
* Dataset-oriented processing model.

### Components

| Component               | Purpose                               |
| ----------------------- | ------------------------------------- |
| NLTK                    | Sentence segmentation                 |
| Pandas                  | Tabular data management               |
| Python Standard Library | Data transformation and preprocessing |

### Improvements

* Transitioned from raw text processing to structured datasets.
* Enabled sentence-level analysis workflows.

---

## [0.1.0] - Initial PDF Extraction

### Added

* PDF ingestion capability.
* Raw text extraction.
* Multi-page document processing.
* Initial cleanup routines.

### Components

| Component               | Purpose                           |
| ----------------------- | --------------------------------- |
| PyPDF2                  | PDF text extraction               |
| Python Standard Library | File handling and text processing |

### Scope

Initial proof-of-concept for extracting analyzable text from policy documents.

---

# Technology Stack

## Core Language

* Python

## Data Processing

* Pandas
* NumPy

## Document Processing

* PyPDF2
* pdfplumber
* PyMuPDF (fitz)

## Natural Language Processing

* NLTK
* spaCy

## Semantic Analysis

* sentence-transformers
* BERTopic
* Zero-Shot NLI Models

## Research Environment

* Jupyter Notebook
* Anaconda

## Version Control

* Git
* GitHub

---

# Current Capabilities

* PDF ingestion and parsing
* Document structure preservation
* Sentence-level extraction
* Claim extraction and classification
* Semantic similarity analysis
* Topic modeling
* Named entity recognition
* Narrative signal scoring
* Evidence mapping
* Traceability auditing
* Structured exports (CSV/JSON)
* Reproducible analysis workflows

---

# Planned Development

* Neo4j integration
* Temporal narrative evolution analysis
* Contradiction tracking
* Multi-document corpus analysis
* Streamlit dashboard
* Automated citation verification
* Narrative drift monitoring
* Public comment intelligence workflows
