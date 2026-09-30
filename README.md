# 🤖 AI-Powered Investor Intelligence Platform

An end-to-end AI-powered financial document intelligence platform that transforms annual reports into searchable, structured, and conversational investor insights.

The platform combines **document processing, semantic chunking, vector-based retrieval, financial KPI extraction, Retrieval-Augmented Generation (RAG), Azure OpenAI, Azure AI Search, PostgreSQL, and FastAPI** into a modular application architecture.

---

## 📌 Overview

Financial annual reports contain large amounts of structured and unstructured information, including financial statements, business performance information, management discussions, operating metrics, and company-specific financial indicators.

Extracting useful information from these reports manually can be time-consuming.

This project provides an automated workflow for processing annual reports and making their information accessible through:

- 📄 Document ingestion
- 🔄 PDF-to-Markdown conversion
- 🧩 Semantic document chunking
- 🧠 Azure OpenAI embeddings
- 🔎 Azure AI Search
- 📊 Financial KPI extraction
- 🗄️ PostgreSQL persistence
- 💬 Retrieval-Augmented Generation
- 🤖 Azure OpenAI-powered responses
- 📊 Investor dashboard
- 🚀 Docker-based deployment
- ☸️ Kubernetes deployment configuration

---

# 🎯 Problem Statement

Financial reports are often large documents containing hundreds of pages of information.

Traditional approaches require users to:

1. Open the annual report.
2. Search manually for relevant information.
3. Read multiple sections.
4. Extract financial metrics.
5. Compare information manually.
6. Interpret the retrieved information.

This project automates a significant part of that workflow.

The system converts annual reports into machine-processable content, indexes the information for semantic retrieval, extracts structured financial KPIs, and provides a conversational interface for querying the processed information.

---

# 💡 Solution

The platform follows an end-to-end document intelligence pipeline:

```text
                  Annual Report PDF
                         │
                         ▼
               ┌──────────────────┐
               │ PDF Processing    │
               └────────┬─────────┘
                        │
                        ▼
               ┌──────────────────┐
               │ PDF → Markdown   │
               │   PyMuPDF4LLM    │
               └────────┬─────────┘
                        │
                        ▼
               ┌──────────────────┐
               │ Semantic Chunking│
               │  LangChain       │
               └────────┬─────────┘
                        │
                        ▼
               ┌──────────────────┐
               │ Azure OpenAI     │
               │ Embeddings       │
               └────────┬─────────┘
                        │
                        ▼
               ┌──────────────────┐
               │ Azure AI Search  │
               │ Vector Index     │
               └────────┬─────────┘
                        │
              ┌─────────┴─────────┐
              │                   │
              ▼                   ▼
      Financial KPI           User Query
       Extraction                 │
              │                   ▼
              ▼             Semantic Retrieval
        PostgreSQL                │
                                  ▼
                           Retrieved Context
                                  │
                                  ▼
                            RAG Pipeline
                                  │
                                  ▼
                           Azure OpenAI
                                  │
                                  ▼
                       Investor Intelligence
