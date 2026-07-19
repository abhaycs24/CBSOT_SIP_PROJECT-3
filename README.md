# 📚 AI Research Assistant

An intelligent, agent-driven platform for exploring, summarizing, and comparing academic research papers using modern LLM and Vector Search technologies.

---

## 🛠 Tech Stack

| Component | Technology |
| :--- | :--- |
| **Language** | Python 3.12 |
| **Orchestration** | LangChain, LangGraph |
| **LLM Inference** | Groq (Llama-3.1-8b-instant) |
| **Vector Database** | FAISS (Facebook AI Similarity Search) |
| **Embeddings** | Sentence-Transformers (`all-MiniLM-L6-v2`) |
| **NLP Pipeline** | Transformers (BART-large-cnn), KeyBERT |
| **Data Source** | Hugging Face Datasets (`ML-ArXiv-Papers`) |

---

## 🏗 System Architecture

The assistant operates as a modular agentic system:

1.  **Data Ingestion**: Processes 15,000+ papers into a unified text format.
2.  **Vectorization**: Converts text into high-dimensional vectors for fast similarity search.
3.  **FAISS Indexing**: Enables rapid retrieval of top-k relevant papers.
4.  **Agentic Brain**: A Groq-powered agent that selects tools dynamically:
    *   `search_and_summarize`: Retrieves papers and generates concise summaries.
    *   `extract_keywords`: Uses KeyBERT to highlight core research themes.
    *   `compare_papers`: Evaluates and contrasts two different research contributions.

--------------------------------------------------

HOW TO RUN

1. Environment Setup: Ensure you have a GROQ_API_KEY configured in your environment or Colab Secrets.

2. Install Dependencies: Run the following command in your terminal:
   pip install langchain langchain-openai langchain-community faiss-cpu sentence-transformers keybert transformers

3. Execution: Run the notebook cells sequentially to ingest the dataset and initialize the vector store.

4. Interact: Use the provided terminal interface to begin querying your research database.

--------------------------------------------------

KEY FEATURES

- Scalable Retrieval: Leverages FAISS for sub-millisecond document matching across 15,000+ papers.
- Agentic Intelligence: Dynamically switches between retrieval, summarization, and keyword extraction.
- Context-Rich Synthesis: Moves beyond simple search to provide actionable insights and comparisons.
- Extensible Design: Modular tool architecture allows for easy integration of new capabilities.

--------------------------------------------------

