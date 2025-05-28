# RAG-Recipes

**A practical guide for building an end-to-end Retrieval Augmented Generation (RAG) system.**

---

# Architecture

## PDF Loader
Loads and extracts text from one or more PDF documents.

## PDF Chunker
Splits the extracted text into smaller, manageable chunks for better indexing and retrieval.

## Embedder
Converts each text chunk into a numerical vector using a pre-trained embedding model.

## Vector Store
Stores the vectors in a searchable index for efficient similarity-based retrieval.

## Retrieval
Finds the most relevant chunks from the vector store based on a user's query.

## Generation
Uses a language model to generate a final answer by grounding it in the retrieved chunks.

---

**In this notebook, we build a RAG pipeline based on PDF documents, focusing on the Ontario Renters' Guide and Condominium Regulations. By the end, the application will be able to answer questions about renting in Ontario while directly citing actual regulations in its responses.**

**We also compare RAG-powered responses with vanilla LLM responses to same questions to demonstrate power of RAG.**

## [End-to-End-RAG.ipynb](https://github.com/szamani20/RAG-Recipes/blob/main/End-to-End-RAG.ipynb)

