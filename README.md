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

---

## 📊 Workflow Diagram

graph TD
    A[User Query] --> B[Agent (Llama-3.1)]
    B --> C{Tool Selection}
    C -->|Retrieve| D[FAISS Index]
    C -->|Summarize| E[BART Transformer]
    C -->|Extract| F[KeyBERT]
    D --> G[Response Generation]
    E --> G
    F --> G
    G --> H[Final Insight]

🚀 *How to Run*
1.Environment Setup: Ensure you have a GROQ_API_KEY in your Google Colab Secrets.

2.Install Dependencies: pip install langchain langchain-openai langchain-community faiss-cpu sentence-transformers keybert transformers

3.Run the Notebook: Execute cells sequentially to load the dataset and initialize the vector index.

4.Interact: Use the terminal input box to start querying the agent.

*📋 Features*
○ Scalable Retrieval: Capable of querying large datasets with sub-millisecond search times.

○ Context-Aware: Leverages current LLMs to synthesize information rather than just returning raw documents.

○ Extensible: Easily add new tools (e.g., PDF upload, live web scraping) to the tools list.
