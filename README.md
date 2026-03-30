# RAG-from-Scratch

A Retrieval-Augmented Generation (RAG) system built from scratch to evaluate:

- Chunking strategies
- Embedding models
- Vector databases
- Retrieval performance

## Experiments

1. Without chunking baseline
2. Paragraph-based chunking
3. Chunking strategy comparison
4. Embedding model comparison (MiniLM vs BGE)
5. Vector database benchmarking (FAISS vs Chroma)

## Results Summary

| Component | Finding |
|-----------|---------|
| Chunking | Section-aware improved retrieval accuracy |
| Embeddings | MiniLM and BGE performed similarly |
| Vector DB | FAISS and Chroma showed similar accuracy |
| Performance | FAISS slightly faster indexing |

## Metrics

- Hit@1
- Hit@2
- Indexing time
- Query latency

## Tech Stack

- Sentence Transformers
- FAISS
- ChromaDB
- Python
- NumPy

## Repository Structure

See `notebooks/` for experiment progression.