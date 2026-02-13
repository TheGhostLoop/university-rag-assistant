# University Policy RAG Chatbot (LLM Project)

This is my first Retrieval-Augmented Generation (RAG) based LLM project.

The system allows users to query a university policy PDF and receive grounded, context-based answers using semantic retrieval + LLM generation.

---

## 🚀 What This Project Does

- Loads a university PDF document
- Splits it into semantic chunks
- Converts chunks into embeddings
- Stores embeddings in a vector database (ChromaDB)
- Retrieves top-k relevant chunks based on user query
- Injects retrieved context into an LLM (Groq)
- Generates answers grounded strictly in document context
- Reduces hallucination using strict prompt constraints
- Supports citation-style responses

---

## 🧠 Tech Stack

- Sentence-Transformers (`all-MiniLM-L6-v2`) — Embeddings
- ChromaDB — Vector Database
- Groq LLM (`llama-3.1-8b-instant`) — Text Generation
- PyPDF — Document Loader
- Python

---

## 🏗 Architecture Overview

PDF Document
↓
Chunking
↓
Embeddings (384-dim vectors)
↓
Chroma Vector Store
↓
Similarity Search (Top-k Retrieval)
↓
Context Injection
↓
LLM Response (Grounded Answer)


---

## 🔍 Example Query

**User:**  
> What are the rules and regulations of this university?

**System:**  
- Retrieves relevant policy chunks  
- Generates answer strictly based on context  
- Quotes exact context lines to reduce hallucination  

---

## 📌 Key Learnings

- Understanding embeddings and cosine similarity
- Why chunking strategy impacts retrieval quality
- How vector databases scale semantic search
- How prompt constraints reduce hallucination
- How RAG improves reliability of LLM systems

---

## 🎯 Why I Built This

After building strong foundations in Deep Learning, I started exploring LLM systems and Retrieval-Augmented Generation.

This project helped me understand how modern document assistants and internal knowledge bots are built.

---

## ⚙️ Future Improvements

- Add reranking for better retrieval quality
- Add conversational memory
- Add Streamlit web interface
- Add evaluation metrics for RAG performance
