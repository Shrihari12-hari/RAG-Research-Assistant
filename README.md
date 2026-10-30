# RAG Research Assistant

An AI-powered Research Paper Assistant built using **Retrieval-Augmented Generation (RAG)**. It allows users to ask questions about research papers and receive context-aware answers with source references.

## Project Overview

This project uses three research papers related to Retrieval-Augmented Generation, REALM, and Atlas. It extracts PDF content, splits it into smaller chunks, generates embeddings, and stores them in a vector database.

When a user asks a question, the system retrieves relevant passages and uses a Large Language Model (LLM) to generate an answer based on the retrieved research content.

## Features

- PDF text extraction using PyMuPDF
- Text chunking using LangChain
- Semantic embeddings using Jina AI
- Vector storage and similarity search using ChromaDB
- AI-powered answers using Groq LLM
- Source references with paper titles, page numbers, and chunk IDs
- Multiple question-and-answer interactions

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| PyMuPDF | PDF text extraction |
| LangChain | Document processing and integration |
| Jina AI | Text embeddings |
| ChromaDB | Vector database |
| Groq API | LLM-based answer generation |
| Jupyter Notebook | Development environment |
| python-dotenv | API key management |

## System Architecture

```text
Research Paper PDFs
        |
        v
   PDF Extraction
        |
        v
   Text Chunking
        |
        v
   Jina AI Embeddings
        |
        v
     ChromaDB
        |
        v
    User Question
        |
        v
  Query Embedding
        |
        v
  Semantic Retrieval
        |
        v
   Retrieved Context
        |
        v
     Groq LLM
        |
        v
  Generated Answer
        |
        v
  Answer with Sources
```

## Research Papers

The project uses three research papers:

1. **Atlas:** Few-shot Learning with Retrieval Augmented Language Models
2. **RAG:** Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks
3. **REALM:** Retrieval-Augmented Language Model Pre-Training

## Project Results

| Metric | Result |
|---|---:|
| Research papers | 3 |
| Pages extracted | 64 |
| Text chunks generated | 305 |
| Embedding dimensions | 1024 |
| Vector records stored | 305 |
| Retrieved passages per question | 3 |

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/Shrihari12-hari/RAG-Research-Assistant.git
cd RAG-Research-Assistant
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate on Windows:

```powershell
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure API keys

Create a `.env` file in the project root:

```env
JINA_API_KEY=your_jina_api_key
GROQ_API_KEY=your_groq_api_key
```

Never share or upload your API keys.

### 5. Run the notebook

Open `main.ipynb` in VS Code or Jupyter Notebook and execute the cells in order.

## Project Structure

```text
RAG-Research-Assistant/
│
├── research_papers/
├── vectorstore/
├── main.ipynb
├── requirements.txt
├── README.md
├── .gitignore
└── .env
```

The `.env`, `venv/`, and `vectorstore/` directories are excluded from Git using `.gitignore`. The vector database is generated locally when the notebook runs.

## Future Improvements

- Streamlit-based web interface
- Conversation history
- Improved inline source citations
- Support for uploading new research papers
- Advanced retrieval and reranking
- Research paper comparison

## Author

**Shrihari Gajul**

GitHub: https://github.com/Shrihari12-hari

---

*Developed as an academic project exploring Retrieval-Augmented Generation, semantic search, and Large Language Models.*