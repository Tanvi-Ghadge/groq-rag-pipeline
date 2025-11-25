Hybrid RAG powered by Groq:
This project implements a sophisticated Retrieval-Augmented Generation (RAG) system designed to answer complex questions by drawing information directly from a set of proprietary academic documents (e.g., PDFs). It utilizes a hybrid search approach for maximized information retrieval and integrates with the high-speed Groq API for ultra-low latency LLM responses.

Key Features:
Hybrid Search Implementation: Employs an EnsembleRetriever to combine the precision of vector search (Pinecone) with the high recall of keyword-based search (BM25), ensuring comprehensive and accurate context retrieval.

High-Performance LLM: Integrates with the Groq API for rapid inference using the openai/gpt-oss-20b model, significantly reducing latency compared to traditional cloud LLM providers.

Efficient Document Processing: Utilizes PyPDFLoader and the RecursiveCharacterTextSplitter for robust handling and chunking of large PDF files.

Semantic Understanding: Leverages HuggingFace's BGE-Small-EN model for creating highly relevant document embeddings.

Scalable Architecture: Built on the LangChain framework, allowing for easy component swapping and future scalability.


## ⚙️ Technologies Used

| Category | Technology | Purpose |
| :--- | :--- | :--- |
| **LLM Inference** | **Groq API** (`langchain-openai`) | Fast, cost-effective LLM processing. |
| **RAG Framework** | **LangChain** | Orchestrating the RAG pipeline components. |
| **Vector Store** | **Pinecone** | Storing and retrieving vector embeddings (Dense Search). |
| **Embedding Model** | **HuggingFace BGE-Small-EN** | Generating high-quality, normalized embeddings. |
| **Keyword Search** | **BM25** (`rank_bm25`) | Providing sparse keyword-based retrieval. |
| **Data Loading** | `pypdf`, `TextLoader` | Loading and processing PDF and text documents. |
| **Environment** | `python-dotenv` | Secure management of API keys and environment variables. |
