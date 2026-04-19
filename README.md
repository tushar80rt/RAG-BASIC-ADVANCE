# RAG Basic to Advanced

A hands-on collection of Retrieval-Augmented Generation (RAG) examples, progressing from basic pipelines to advanced and agentic workflows using LangChain, LangGraph, Groq, Chroma/FAISS, Typesense, MongoDB, and LangSmith evaluation.

## What this repository contains

- **Basic RAG pipeline** (data ingestion, chunking, embedding, retrieval, generation)
- **Agentic RAG** with LangGraph stateful workflow
- **Typesense-backed RAG** using JSONL book data
- **MongoDB-backed RAG** with vector search flow
- **RAG and LLM evaluation** with LangSmith + Anthropic tooling

Most implementation work is in Jupyter notebooks.

## Project structure

```text
.
├── notebook/Basic_RAG.ipynb
├── agentic_rag/agenticrag.ipynb
├── RAGwithMongoDB/rag.ipynb
├── EvalutionS_RAG_&_LLM/1-rag_evaluation.ipynb
├── typesense.ipynb
├── data/
│   ├── pdf/
│   ├── text_files/
│   └── vector_store/
├── books.jsonl
├── requirements.txt
├── pyproject.toml
└── main.py
```

## Requirements

- Python **3.10+**
- API keys/services depending on notebook:
  - `GROQ_API_KEY` (used in most RAG notebooks)
  - `MONGODB_URI` (MongoDB notebook)
  - `LANGSMITH_API_KEY`, `LANGSMITH_TRACING`, `ANTHROPIC_API_KEY` (evaluation notebook)
  - Typesense connection settings (`HOST`, `PORT`, `KEY`) for Typesense notebook

## Setup

### Option 1: pip + requirements.txt

```bash
python -m venv .venv
source .venv/bin/activate   # On Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

### Option 2: uv (pyproject-based)

```bash
uv sync
```

Create a `.env` file in the project root for required keys:

```env
GROQ_API_KEY=...
MONGODB_URI=...
LANGSMITH_API_KEY=...
LANGSMITH_TRACING=true
ANTHROPIC_API_KEY=...
HOST=...
PORT=...
KEY=...
```

## How to use

1. Install dependencies.
2. Configure required environment variables.
3. Open notebooks and run cells in order:
   - `notebook/Basic_RAG.ipynb`
   - `agentic_rag/agenticrag.ipynb`
   - `typesense.ipynb`
   - `RAGwithMongoDB/rag.ipynb`
   - `EvalutionS_RAG_&_LLM/1-rag_evaluation.ipynb`

## Notes

- `main.py` is a minimal placeholder entrypoint.
- Precomputed vector-store artifacts exist under `data/vector_store/`.
- Included sample assets (`data/text_files`, `data/pdf`, `books.jsonl`) are used by notebook demos.
