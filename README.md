# Overview
This Jupyter Notebook implements a hybrid document search system—combining TF‑IDF and dense‑vector (FAISS) retrieval + an LLM‑powered summarization pipeline. It was built for a project manager tasked with cross‑checking hundreds of legislative acts and corporate policy PDFs—previously a manual, time‑intensive process.

# Key Benefits
- Online via GPT API: Leverage OpenAI’s GPT‑4 for high‑quality summaries with just an API call.
- Fully offline option: Download and run Llama‑2/3 or Mistral locally (via llama.cpp) to keep sensitive documents on‑premise.
- Faster compliance checks: Instantly retrieve and summarize the most relevant sections across your policy library based on your question/query.
- Hybrid search: Balance exact keyword matching (TF‑IDF) with semantic similarity (embeddings + FAISS).
- Model comparison with ChatGPT as judge: Automatically have ChatGPT evaluate and rank each model’s summaries, so you can see at a glance which LLM delivers the best results for your cases, designed primarily for scenarios where locally hosted LLMs are preferred.

# Use Case
A project manager used to spend hours manually scanning dozens of PDF “Acts” against corporate policies. With this tool they can:
- Ingest an entire folder of PDFs in one step.
- Choose online mode (GPT‑4 API) for rapid results, or offline mode (Llama‑2/3/Mistral) for full data privacy.
- Issue a natural‑language query (e.g., “data privacy exemptions under GDPR”).
- Receive top‑ranked passages plus concise summaries from each selected model.
- Export findings for audit reports or stakeholder review.

# Tech Stack
Python 3.10+ & Jupyter Notebook
- scikit‑learn, exact word match (TF‑IDF)
- sentence‑transformers + FAISS (semantic search)
- OpenAI API (GPT‑4) & llama.cpp (Llama‑2/3) & Mistral
