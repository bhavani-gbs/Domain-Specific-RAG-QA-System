# Domain-Specific RAG Question Answering System

A Retrieval-Augmented Generation (RAG) based Question Answering system that retrieves relevant document chunks using FAISS and generates accurate answers using FLAN-T5.

This system reduces hallucination by grounding responses in retrieved document context instead of relying solely on pre-trained model knowledge.

## Project Overview

Large Language Models often generate answers from parametric memory, which can lead to hallucinated or inaccurate responses.

This project implements a complete RAG pipeline that:

* Splits domain documents into meaningful chunks
* Converts text chunks into dense vector embeddings
* Stores embeddings in a FAISS vector database
* Retrieves top-k relevant chunks for a user query
* Builds context within a defined token budget
* Generates grounded answers using FLAN-T5

 ## System Architecture

User Query
→ Query Embedding
→ FAISS Similarity Search
→ Top-k Retrieval
→ Context Construction (Token Budget Controlled)
→ FLAN-T5 Answer Generation

## Tech Stack

* Python
* FAISS (Vector Similarity Search)
* HuggingFace Transformers
* FLAN-T5
* Sentence Transformers
* Jupyter Notebook

## Key Features
* Domain-specific document retrieval
* Context-aware answer generation
* Token-budget controlled context building
* Reduced hallucination
* ROUGE-L based evaluation
* Modular RAG pipeline implementation
