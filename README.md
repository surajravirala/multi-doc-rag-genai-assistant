# multi-doc-rag-genai-assistant
Production-ready Multi-Document RAG system using LangChain, Hugging Face embeddings, ChromaDB, and Gemini Flash with Gradio UI.


An end-to-end Retrieval-Augmented Generation (RAG) system that enables users to query multiple PDF documents using natural language.

Built with LangChain, Hugging Face embeddings, ChromaDB, and Gemini Flash, with an interactive Gradio interface.

---

## 🔍 Problem Statement

Organizations store large volumes of unstructured documents (PDFs), making knowledge retrieval slow and inefficient. Traditional keyword search fails to capture semantic meaning.

---

## 💡 Solution Overview

This project implements a Multi-Document RAG pipeline that:

- Ingests multiple PDFs
- Splits documents into semantic chunks
- Generates embeddings using Hugging Face
- Stores vectors in ChromaDB
- Retrieves relevant context using MMR search
- Generates grounded answers using Gemini Flash
- Provides an interactive Gradio UI

---

## 🧠 Architecture

Pipeline flow:

PDFs → Text Splitter → Embeddings → Chroma Vector DB → Retriever (MMR) → Gemini LLM → Answer

(Add architecture.png here)

---

## 🛠 Tech Stack

- LangChain
- Hugging Face Sentence Transformers
- ChromaDB
- Gemini Flash (Google Generative AI)
- Gradio
- Python

---

## ⚙️ Key Features

✅ Multi-document ingestion  
✅ Semantic chunking (chunk_size=1000, overlap=400)  
✅ MMR-based retrieval  
✅ Persistent vector database  
✅ Grounded answer generation  
✅ Interactive UI with Gradio  

---

## 📊 Sample Query

**Query:**  
> What are additional endpoints in Azure Arc scenarios?

**Result:**  
The system retrieves relevant chunks and generates a grounded response with source documents.

---

## 🚀 How to Run

```bash
pip install -r requirements.txt
python app.py
