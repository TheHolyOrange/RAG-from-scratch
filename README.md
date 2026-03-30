# RAG-from-Scratch

An end-to-end **Retrieval-Augmented Generation (RAG)** system built from scratch to evaluate the impact of **chunking strategies**, **embedding models**, and **vector databases** on retrieval performance.

This project focuses on **engineering-level experimentation**, comparing multiple components of a RAG pipeline using **Hit@k retrieval metrics**, **latency benchmarking**, and **indexing performance analysis**.

---

# Overview

Retrieval-Augmented Generation (RAG) improves language model responses by retrieving relevant context from a document corpus before generating answers. This repository implements a RAG pipeline **without relying on high-level frameworks**, allowing fine-grained evaluation of each stage:

- Document chunking
- Embedding generation
- Vector indexing
- Retrieval
- Evaluation

---

# Experiments Conducted

### 1. Baseline Without Chunking
Evaluated retrieval performance using full documents as embeddings.

### 2. Paragraph-Based Chunking
Split documents into paragraph-level chunks for improved semantic retrieval.

### 3. Chunking Strategy Comparison
Compared:
- Fixed-size chunking
- Overlapping chunking
- Section-aware chunking

### 4. Embedding Model Comparison
Compared local embedding models:
- `all-MiniLM-L6-v2`
- `BAAI/bge-small-en-v1.5`

### 5. Vector Database Benchmarking
Compared:
- FAISS
- ChromaDB

Measured:
- Retrieval accuracy
- Indexing time
- Query latency

---

# Key Findings

| Component | Observation |
|-----------|-------------|
| Chunking | Section-aware chunking improved retrieval accuracy |
| Embeddings | MiniLM and BGE-small performed similarly on structured data |
| Vector DB | FAISS and Chroma showed identical retrieval quality |
| Performance | FAISS slightly faster indexing and query latency |
| Overall | Chunking strategy had the largest impact on retrieval |

---

# Metrics Used

- Hit@1
- Hit@2
- Indexing Time
- Query Latency
- Retrieval Distance

---

# Results Summary

### Chunking Strategy Comparison

| Method | Hit@1 | Hit@2 |
|--------|------|------|
| Fixed-size | 0.8 | 0.8 |
| Overlapping | 1.0 | 1.0 |
| Section-aware | 1.0 | 1.0 |

### Embedding Comparison

| Model | Hit@1 | Hit@2 |
|------|------|------|
| MiniLM | 1.0 | 1.0 |
| BGE-small | 1.0 | 1.0 |

### Vector Database Benchmark

| Vector DB | Hit@1 | Hit@2 | Index Time (s) | Query Time (s) |
|-----------|------|------|----------------|----------------|
| FAISS | 1.0 | 1.0 | 0.0507 | 0.0224 |
| Chroma | 1.0 | 1.0 | 0.0608 | 0.0248 |

---

# Repository Structure
# RAG-from-Scratch

An end-to-end **Retrieval-Augmented Generation (RAG)** system built from scratch to evaluate the impact of **chunking strategies**, **embedding models**, and **vector databases** on retrieval performance.

This project focuses on **engineering-level experimentation**, comparing multiple components of a RAG pipeline using **Hit@k retrieval metrics**, **latency benchmarking**, and **indexing performance analysis**.

---

# Overview

Retrieval-Augmented Generation (RAG) improves language model responses by retrieving relevant context from a document corpus before generating answers. This repository implements a RAG pipeline **without relying on high-level frameworks**, allowing fine-grained evaluation of each stage:

- Document chunking
- Embedding generation
- Vector indexing
- Retrieval
- Evaluation

---

# Experiments Conducted

### 1. Baseline Without Chunking
Evaluated retrieval performance using full documents as embeddings.

### 2. Paragraph-Based Chunking
Split documents into paragraph-level chunks for improved semantic retrieval.

### 3. Chunking Strategy Comparison
Compared:
- Fixed-size chunking
- Overlapping chunking
- Section-aware chunking

### 4. Embedding Model Comparison
Compared local embedding models:
- `all-MiniLM-L6-v2`
- `BAAI/bge-small-en-v1.5`

### 5. Vector Database Benchmarking
Compared:
- FAISS
- ChromaDB

Measured:
- Retrieval accuracy
- Indexing time
- Query latency

---

# Key Findings

| Component | Observation |
|-----------|-------------|
| Chunking | Section-aware chunking improved retrieval accuracy |
| Embeddings | MiniLM and BGE-small performed similarly on structured data |
| Vector DB | FAISS and Chroma showed identical retrieval quality |
| Performance | FAISS slightly faster indexing and query latency |
| Overall | Chunking strategy had the largest impact on retrieval |

---

# Metrics Used

- Hit@1
- Hit@2
- Indexing Time
- Query Latency
- Retrieval Distance

---

# Results Summary

### Chunking Strategy Comparison

| Method | Hit@1 | Hit@2 |
|--------|------|------|
| Fixed-size | 0.8 | 0.8 |
| Overlapping | 1.0 | 1.0 |
| Section-aware | 1.0 | 1.0 |

### Embedding Comparison

| Model | Hit@1 | Hit@2 |
|------|------|------|
| MiniLM | 1.0 | 1.0 |
| BGE-small | 1.0 | 1.0 |

### Vector Database Benchmark

| Vector DB | Hit@1 | Hit@2 | Index Time (s) | Query Time (s) |
|-----------|------|------|----------------|----------------|
| FAISS | 1.0 | 1.0 | 0.0507 | 0.0224 |
| Chroma | 1.0 | 1.0 | 0.0608 | 0.0248 |

---

# Repository Structure
RAG-from-scratch/
│
├── notebooks/
│ ├── 01_without_chunking.ipynb
│ ├── 02_paragraph_based_chunking.ipynb
│ ├── 03_compare_chunking_strategies.ipynb
│ ├── 04_compare_embedding_models.ipynb
│ └── 05_faiss_vs_chroma_benchmark.ipynb
│
├── README.md
└──requirements.txt


---

# Pipeline Architecture

---

# Pipeline Architecture
Documents
↓
Chunking (fixed / overlap / section-aware)
↓
Embeddings (MiniLM / BGE)
↓
Vector Database (FAISS / Chroma)
↓
Retriever (Top-K search)
↓
Evaluation (Hit@k metrics)
↓
Performance Benchmarking


---

# Installation

Clone repository:

```bash
git clone https://github.com/TheHolyOrange/RAG-from-scratch.git
cd RAG-from-scratch

pip install -r requirements.txt
```