# Retrieval-Augmented Generation (RAG) Pipelining System for University Legal Documents

Welcome to the official documentation wiki for the **RAG Pipelining System**, a research-driven software project developed as part of the **Boğaziçi University Computer Engineering Senior Project (CMPE491)** by **Sezer Çot**.

This system leverages **Retrieval-Augmented Generation (RAG)** to provide explainable, citation-based answers to questions about **university legal and academic regulations**.

---

##  Project Overview

The RAG Pipelining System combines document retrieval and large language model (LLM) reasoning to answer natural language queries about **departmental regulations, course prerequisites, and academic rules**.

> **Goal:** Make complex legal documents searchable and understandable for students, advisors, and administrators.

###  Core Features

-  **Document Ingestion:** Extracts and cleans university PDFs  
-  **Chunking:** Splits documents into meaningful segments  
-  **Semantic Search:** Retrieves relevant regulation articles using embeddings  
-  **RAG Pipeline:** Generates human-readable answers with citations  
-  **API & Web UI:** Interactive interface for querying documents  

---

##  System Architecture

```mermaid
graph LR
A[PDF Loader] --> B[Text Preprocessor]
B --> C[Chunker]
C --> D[Embedder]
D --> E[Vector Database]
F[User Query] --> G[Query Preprocessor]
G --> H[Retriever]
H --> I[Re-Ranker]
I --> J[LLM Generator]
J --> K[Answer + Citation Renderer]
E --> H
