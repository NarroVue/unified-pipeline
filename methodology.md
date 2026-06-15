# Methodology

## Overview

This repository implements a reproducible text analysis framework for extracting, organizing, and evaluating narrative patterns within large document collections.

The methodology combines computational linguistics, natural language processing (NLP), semantic similarity analysis, rhetorical signal detection, and network-based relationship mapping to transform unstructured text into structured analytical outputs.

The system is designed to support research, policy analysis, journalism, communications studies, organizational audits, and other domains that require systematic examination of large bodies of text.

---

## Research Objectives

The pipeline is designed to answer several categories of questions:

* What themes dominate a document or corpus?
* Which rhetorical strategies appear most frequently?
* Which entities, concepts, and institutions are most interconnected?
* How are narratives constructed and reinforced?
* Which sections exhibit unusually strong semantic signals?
* How do documents compare structurally across time or sources?

The methodology is descriptive and exploratory rather than predictive.

---

## Analytical Framework

The pipeline consists of two primary stages:

### Phase A: Canonical Analysis Object (CAO) Generation

Documents are processed once to generate a persistent analytical representation called the **Canonical Analysis Object (CAO)**.

The CAO serves as a reusable analytical foundation from which multiple report types can be generated without repeating computationally expensive operations.

### Phase B: Report Generation

Reports are derived from the CAO and may emphasize different levels of analysis.

Examples include:

* Rapid Signal Audit
* Structural Narrative Audit
* Comparative Narrative Analysis
* Network Analysis
* Entity Relationship Analysis

---

## Methodological Workflow

### 1. Document Ingestion

Source documents are imported and normalized.

Tasks include:

* PDF ingestion
* Text extraction
* Character normalization
* Removal of unnecessary formatting artifacts
* Preservation of source traceability

Metadata retained includes:

* Document name
* Section identifiers
* Page references (when available)

---

### 2. Semantic Chunking

Documents are segmented into smaller analytical units.

Chunking is performed to:

* Preserve contextual coherence
* Improve embedding quality
* Reduce noise introduced by arbitrary token limits

Each chunk becomes the fundamental unit of analysis.

---

### 3. Text Embedding

Each chunk is transformed into a numerical representation using sentence-transformer models.

Embeddings enable:

* Semantic similarity calculations
* Topic discovery
* Cluster generation
* Comparative analysis

Semantic distance is measured in vector space rather than through keyword matching alone.

---

### 4. Topic Modeling

Topic modeling groups semantically related chunks into thematic categories.

The objective is to identify emergent structures rather than impose predefined categories.

Outputs may include:

* Dominant themes
* Topic frequencies
* Topic distributions
* Topic representative terms

---

### 5. Rhetorical Signal Detection

The pipeline evaluates text across multiple rhetorical dimensions.

Examples include:

* Institutional language
* Conflict language
* Urgency signals
* Moral framing
* Threat framing
* Collective identity language

Signal intensity is measured across chunks and aggregated throughout the corpus.

---

### 6. Natural Language Inference (NLI)

Natural Language Inference is used to evaluate semantic alignment between text and predefined hypotheses.

NLI provides probabilistic assessments regarding whether text:

* Supports a hypothesis
* Contradicts a hypothesis
* Is unrelated to a hypothesis

These scores are used as analytical indicators rather than definitive classifications.

---

### 7. Named Entity Recognition (NER)

Named entities are extracted using NLP pipelines.

Entities may include:

* People
* Organizations
* Locations
* Governments
* Institutions
* Events

Entity frequencies and relationships are preserved for downstream analysis.

---

### 8. Network Construction

Entity co-occurrence relationships are transformed into graph structures.

Nodes represent entities.

Edges represent relationships based on shared contextual appearances.

Network analysis enables identification of:

* Central actors
* Influential concepts
* Highly connected entities
* Structural clusters

---

### 9. Signal Aggregation

Chunk-level metrics are aggregated into higher-order summaries.

Examples include:

* Section-level scores
* Topic-level scores
* Entity-level scores
* Document-level scores

Aggregation enables comparison across multiple scales.

---

## Canonical Analysis Object (CAO)

The Canonical Analysis Object is the repository's central analytical artifact.

The CAO stores:

* Source metadata
* Chunked text
* Embeddings
* Topic assignments
* Entity annotations
* Rhetorical signals
* NLI outputs
* Network relationships

The CAO separates expensive computation from report generation.

Once created, additional reports can be generated without reprocessing source documents.

---

## Outputs

The pipeline may produce:

### Structured Data

* CSV
* JSON

### Visualizations

* Topic distributions
* Entity networks
* Signal rankings
* Frequency charts

### Analytical Reports

* Rapid Signal Audits
* Narrative Audits
* Comparative analyses

---

## Reproducibility

The methodology emphasizes reproducibility through:

* Deterministic processing stages where possible
* Persistent intermediate outputs
* Configurable parameters
* Modular notebook architecture
* Document traceability

All analyses should be reproducible when executed against identical source documents and configuration settings.

---

## Limitations

Several limitations should be considered.

### Model Dependence

Results depend on the behavior and training data of underlying NLP models.

### Semantic Approximation

Embeddings represent semantic approximations rather than objective truth.

### Topic Instability

Topic modeling may vary depending on corpus size and parameter selection.

### Context Sensitivity

Meaning may shift when text is segmented into smaller chunks.

### Human Interpretation Required

Outputs are analytical indicators and should not be interpreted as factual determinations without expert review.

---

## Recommended Applications

This methodology is suitable for:

* Policy analysis
* Government oversight research
* Public communications analysis
* Journalism
* Academic research
* Narrative intelligence
* Organizational document audits
* Comparative corpus studies

The framework is intended to augment human analysis rather than replace subject matter expertise.
