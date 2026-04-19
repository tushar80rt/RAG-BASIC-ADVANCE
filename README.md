<div align="center">

# 🔍 RAG: Basic to Advanced

### A hands-on progression through Retrieval-Augmented Generation —<br/>from foundational pipelines to agentic, multi-backend workflows.

<br/>

<!-- Core Stack Badges -->
![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-Orchestration-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-Agentic%20Workflows-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-LPU%20Inference-F55036?style=for-the-badge&logo=groq&logoColor=white)

<br/>

![MongoDB](https://img.shields.io/badge/MongoDB-Atlas%20Vector%20Search-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![FAISS](https://img.shields.io/badge/FAISS-Meta%20AI-0467DF?style=for-the-badge&logo=meta&logoColor=white)
![Typesense](https://img.shields.io/badge/Typesense-Hybrid%20Search-D72B3F?style=for-the-badge)
![Anthropic](https://img.shields.io/badge/Anthropic-Claude-CC785C?style=for-the-badge)

<br/>

![LangSmith](https://img.shields.io/badge/LangSmith-Evaluation%20&%20Tracing-FF6B35?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

</div>

---

## 📖 Overview

This repository is a structured, notebook-driven exploration of RAG systems — designed to teach each pattern in isolation so you can study, run, and adapt any piece independently.

```
Basic Pipeline ──► Vector Stores ──► Hybrid Search ──► Agentic Workflows ──► Evaluation
```

Each module targets a distinct backend or architectural pattern, progressively building toward production-grade agentic RAG systems.

---

## 🗂️ Modules

| # | Module | Notebook | Description |
|---|--------|----------|-------------|
| 1 | **Basic RAG** | `notebook/Basic_RAG.ipynb` | Document ingestion, chunking, embedding, retrieval, and generation |
| 2 | **Agentic RAG** | `agentic_rag/agenticrag.ipynb` | Stateful multi-step reasoning with a LangGraph graph-based agent |
| 3 | **Typesense RAG** | `typesense.ipynb` | Keyword + vector hybrid search over JSONL book data |
| 4 | **MongoDB RAG** | `RAGwithMongoDB/rag.ipynb` | Atlas Vector Search integration with a complete retrieval flow |
| 5 | **RAG Evaluation** | `EvalutionS_RAG_&_LLM/1-rag_evaluation.ipynb` | Automated quality scoring with LangSmith tracing and Claude |

---

## 🏗️ Tech Stack

<div align="center">

| Layer | Technology | Purpose |
|-------|-----------|---------|
| ![LangChain](https://img.shields.io/badge/-LangChain-1C3C3C?logo=langchain&logoColor=white&style=flat-square) | **LangChain** | Chain orchestration & document loaders |
| ![LangGraph](https://img.shields.io/badge/-LangGraph-1C3C3C?logo=langchain&logoColor=white&style=flat-square) | **LangGraph** | Stateful agentic workflows |
| ![Groq](https://img.shields.io/badge/-Groq-F55036?logo=groq&logoColor=white&style=flat-square) | **Groq** | Ultra-fast LLM inference |
| ![ChromaDB](https://img.shields.io/badge/-ChromaDB-FF6B6B?style=flat-square) | **ChromaDB** | Local persistent vector store |
| ![FAISS](https://img.shields.io/badge/-FAISS-0467DF?logo=meta&logoColor=white&style=flat-square) | **FAISS** | High-performance similarity search |
| ![Typesense](https://img.shields.io/badge/-Typesense-D72B3F?style=flat-square) | **Typesense** | Hybrid keyword + vector search |
| ![MongoDB](https://img.shields.io/badge/-MongoDB_Atlas-47A248?logo=mongodb&logoColor=white&style=flat-square) | **MongoDB Atlas** | Cloud-native vector search |
| ![LangSmith](https://img.shields.io/badge/-LangSmith-FF6B35?style=flat-square) | **LangSmith** | Tracing, evaluation & monitoring |
| ![Anthropic](https://img.shields.io/badge/-Anthropic_Claude-CC785C?style=flat-square) | **Anthropic Claude** | LLM evaluation & scoring |
| ![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?logo=jupyter&logoColor=white&style=flat-square) | **Jupyter** | Interactive exploration notebooks |

</div>

---

## 📁 Repository Structure

```text
rag-basic-to-advanced/
│
├── 📓 notebook/
│   └── Basic_RAG.ipynb                    # Core RAG pipeline
│
├── 🤖 agentic_rag/
│   └── agenticrag.ipynb                   # LangGraph stateful agent
│
├── 🍃 RAGwithMongoDB/
│   └── rag.ipynb                          # MongoDB Atlas Vector Search
│
├── 📊 EvalutionS_RAG_&_LLM/
│   └── 1-rag_evaluation.ipynb             # LangSmith + Anthropic evaluation
│
├── 🔍 typesense.ipynb                     # Typesense hybrid search
│
├── 📦 data/
│   ├── pdf/                               # Sample PDF source documents
│   ├── text_files/                        # Sample plain text documents
│   └── vector_store/                      # Precomputed ChromaDB / FAISS artifacts
│
├── 📚 books.jsonl                         # Book dataset for Typesense demo
├── ⚙️  main.py                            # Minimal entrypoint placeholder
├── requirements.txt
└── pyproject.toml
```

---

## ⚙️ Prerequisites

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)

API credentials required vary by notebook:

| Notebook | Required Environment Variables |
|----------|-------------------------------|
| All RAG notebooks | `GROQ_API_KEY` |
| `RAGwithMongoDB/rag.ipynb` | `MONGODB_URI` |
| `EvalutionS_RAG_&_LLM/` | `LANGSMITH_API_KEY` · `LANGSMITH_TRACING` · `ANTHROPIC_API_KEY` |
| `typesense.ipynb` | `HOST` · `PORT` · `KEY` |

> **Tip:** You only need to configure credentials for the notebooks you intend to run.

---

## 🚀 Installation

### Option A — pip

```bash
# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Option B — uv *(recommended, faster)*

```bash
uv sync
```

---

## 🔑 Configuration

Create a `.env` file in the project root and populate the keys for the module(s) you want to run:

```env
# ── LLM Inference ───────────────────────────────────────
GROQ_API_KEY=your_groq_api_key

# ── MongoDB Atlas ────────────────────────────────────────
MONGODB_URI=your_mongodb_connection_string

# ── LangSmith Evaluation ─────────────────────────────────
LANGSMITH_API_KEY=your_langsmith_api_key
LANGSMITH_TRACING=true
ANTHROPIC_API_KEY=your_anthropic_api_key

# ── Typesense ────────────────────────────────────────────
HOST=localhost
PORT=8108
KEY=your_typesense_api_key
```

---

## ▶️ Usage

Run the notebooks in order for the best learning progression:

| Step | Notebook | Focus |
|------|----------|-------|
| **1** | `notebook/Basic_RAG.ipynb` | ← Start here |
| **2** | `agentic_rag/agenticrag.ipynb` | Agent design |
| **3** | `typesense.ipynb` | Hybrid search |
| **4** | `RAGwithMongoDB/rag.ipynb` | Cloud vector DB |
| **5** | `EvalutionS_RAG_&_LLM/1-rag_evaluation.ipynb` | Quality scoring |

Each notebook is self-contained — it loads environment variables, initializes its own retriever and chain, and walks through the entire workflow step by step with inline explanations.

---

## 📝 Notes

- `data/vector_store/` ships with precomputed embeddings so you can run retrieval steps without re-indexing from scratch.
- `main.py` is a lightweight placeholder; the primary interface is the Jupyter notebooks.
- Sample assets in `data/text_files/`, `data/pdf/`, and `books.jsonl` are included for demo purposes — replace them with your own documents when building custom pipelines.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/add-weaviate-module`
3. Commit your changes: `git commit -m 'Add Weaviate RAG module'`
4. Push to the branch: `git push origin feature/add-weaviate-module`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<div align="center">

**Built with ❤️ for the RAG community**

<br/>

![LangChain](https://img.shields.io/badge/-LangChain-1C3C3C?logo=langchain&logoColor=white&style=flat-square)
![Groq](https://img.shields.io/badge/-Groq-F55036?logo=groq&logoColor=white&style=flat-square)
![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?logo=mongodb&logoColor=white&style=flat-square)
![FAISS](https://img.shields.io/badge/-FAISS-0467DF?logo=meta&logoColor=white&style=flat-square)
![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?logo=jupyter&logoColor=white&style=flat-square)
![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white&style=flat-square)
![Anthropic](https://img.shields.io/badge/-Anthropic-CC785C?style=flat-square)

<br/>

*Star ⭐ this repo if you found it helpful!*

</div>
