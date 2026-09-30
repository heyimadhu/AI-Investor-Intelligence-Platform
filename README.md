# 🤖 AI-Powered Investor Intelligence Platform

An AI-powered platform for processing annual reports, extracting financial KPIs, performing semantic search, and generating investor-oriented insights using **Azure OpenAI, Azure AI Search, PostgreSQL, and RAG**.

The platform combines document processing, information retrieval, structured KPI extraction, and generative AI into a modular backend architecture designed for scalable deployment.

---

## 📌 Overview

Financial reports contain large amounts of structured and unstructured information that can be difficult to analyze manually.

This project provides an end-to-end workflow for transforming annual reports into an intelligent investor information system.

The platform supports:

- 📄 Annual report ingestion
- 🔍 Document processing and indexing
- 📊 Financial KPI extraction
- 🧠 AI-powered semantic search
- 💬 Retrieval-Augmented Generation (RAG)
- 🗄️ PostgreSQL-based KPI storage
- ☁️ Azure AI service integration
- 🚀 Containerized deployment
- ☸️ Kubernetes deployment architecture

### High-Level Workflow

```text
                 Annual Reports
                       │
                       ▼
              ┌─────────────────┐
              │ Document        │
              │ Ingestion       │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Document        │
              │ Processing      │
              └────────┬────────┘
                       │
             ┌─────────┴─────────┐
             │                   │
             ▼                   ▼
      ┌──────────────┐    ┌────────────────┐
      │ KPI          │    │ Azure AI       │
      │ Extraction   │    │ Search         │
      └──────┬───────┘    └───────┬────────┘
             │                     │
             ▼                     ▼
      ┌──────────────┐      ┌───────────────┐
      │ PostgreSQL   │      │ Semantic       │
      │              │      │ Retrieval      │
      └──────────────┘      └───────┬───────┘
                                    │
                                    ▼
                             ┌───────────────┐
                             │ RAG Pipeline  │
                             └───────┬───────┘
                                     │
                                     ▼
                              ┌─────────────┐
                              │ Azure       │
                              │ OpenAI      │
                              └──────┬──────┘
                                     │
                                     ▼
                              Investor Insights
