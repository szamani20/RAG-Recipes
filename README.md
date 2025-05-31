# RAG-Recipes

1. **A practical guide for building an end-to-end Retrieval Augmented Generation (RAG) system.**

2. **Ragas (RAG Assessment) to evaluate RAG performance using 9 metrics.**

---

# RAG Architecture

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

# Ragas Metrics

## LLM Context Precision With Reference
`LLMContextPrecisionWithReference` measures the proportion of relevant chunks in the retrieved_contexts by using an LLM.

## Non LLM Context Precision With Reference
`NonLLMContextPrecisionWithReference` measures the proportion of relevant chunks in the retrieved_contexts by using a non-LLM distance measure.

## LLM Context Recall
`LLMContextRecall` measures how many of the relevant documents (or pieces of information) were successfully retrieved by using an LLM.

## Non LLM Context Recall
`NonLLMContextRecall` how many of the relevant documents (or pieces of information) were successfully retrieved by using a non-LLM distance measure.

## Context Entity Recall
`ContextEntityRecall` gives the measure of recall of the retrieved context, based on the number of entities present in both reference and retrieved_contexts relative to the number of entities present in the reference alone.

## Response Relevancy
`ResponseRelevancy` measures how relevant a response is to the user input by using an LLM or embeddings to score relevance.

## Faithfulness
`Faithfulness` measures the factual consistency of the response by calculating the fraction of claims in the response that are supported by the retrieved contexts.

## Faithfulness With HHEM
`FaithfulnesswithHHEM` uses a pre-trained HHEM classifier to verify each claim in the response against the retrieved contexts and computes the fraction of supported claims.

## Semantic Similarity
`SemanticSimilarity` measures the semantic closeness between the generated response and the reference by computing an embedding-based similarity score.

---

# Notebooks

## [End-to-End-RAG.ipynb](https://github.com/szamani20/RAG-Recipes/blob/main/End-to-End-RAG.ipynb)

**In this notebook, we build a RAG pipeline based on PDF documents, focusing on the Ontario Renters' Guide and Condominium Regulations. By the end, the application will be able to answer questions about renting in Ontario while directly citing actual regulations in its responses.**

**We also compare RAG-powered responses with vanilla LLM responses to same questions to demonstrate power of RAG.**

## [RAG-Evaluation-via-Ragas.ipynb](https://github.com/szamani20/RAG-Recipes/blob/main/RAG-Evaluation-via-Ragas.ipynb)

**In this notebook, we evaluate the RAG pipeline performance using 9 `Ragas`-provided metrics. It helps us evaluate how accurate context retrieval and answer generation have performed.**

