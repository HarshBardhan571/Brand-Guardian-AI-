# 🛡️ Brand Guardian AI
### Enterprise Multimodal LLMOps Compliance Pipeline using Azure AI

> Automatically audits marketing videos using speech recognition, OCR, Retrieval-Augmented Generation (RAG), and Large Language Models to detect regulatory and brand compliance violations.

---

# 🚀 Overview

Brand Guardian AI is an enterprise-grade Multimodal LLMOps application that automatically reviews marketing videos before publication.

Instead of manually watching every advertisement, the system automatically:

- Downloads a YouTube video
- Extracts speech using Azure Video Indexer
- Extracts on-screen text (OCR)
- Retrieves compliance guidelines from Azure AI Search
- Uses GPT-5.1 to compare video content against regulations
- Generates a structured compliance report

---

# 🎯 Problem Statement

Manual compliance review is expensive, slow and inconsistent.

This project automates the review process by combining:

- Video Intelligence
- OCR
- Retrieval Augmented Generation
- Azure AI
- LLM reasoning

to identify regulatory violations before an advertisement is published.

---

# 🎬 Demo

> Input

```
https://youtu.be/dT7S75eYhcQ
```

↓

Azure Video Indexer

↓

Transcript + OCR

↓

Azure AI Search

↓

GPT-5.1

↓

Compliance Report

---

# 🏗 Architecture

<p align="center">
<img src="images/architecture.png" width="900">
</p>

---

# ⚙ Workflow

```
YouTube Video
      │
      ▼
Download using yt-dlp
      │
      ▼
Azure Video Indexer
      │
      ├── Speech to Text
      ├── OCR
      └── Metadata
              │
              ▼
Azure AI Search
(Vector Knowledge Base)
              │
              ▼
Azure OpenAI GPT-5.1
              │
              ▼
Compliance Report
```

---

# ✨ Features

- 🎥 YouTube video ingestion
- 🎙 Automatic speech transcription
- 📝 OCR extraction
- 📚 Retrieval-Augmented Generation
- 🔍 Azure AI Search Knowledge Base
- 🤖 GPT-5.1 reasoning
- 🔄 LangGraph workflow orchestration
- 📈 LangSmith tracing
- ☁ Azure Application Insights monitoring
- 📊 Structured JSON compliance report

---

# ☁ Azure Services Used

| Service | Purpose |
|----------|----------|
| Azure Video Indexer | Speech-to-Text + OCR |
| Azure AI Search | Vector Knowledge Base |
| Azure OpenAI | Compliance Analysis |
| Azure Blob Storage | Video Storage |
| Azure Identity | Authentication |
| Azure Application Insights | Monitoring |

---

# 🧠 AI Stack

- GPT-5.1
- text-embedding-3-small
- LangChain
- LangGraph
- LangSmith
- Azure AI Search

---


# 📊 Sample Compliance Report

```
Status: FAIL

Violations

CRITICAL
Claim Validation

MAJOR
Invisible Finish Claim

MAJOR
Trademark Compliance

MINOR
Brand Messaging Alignment

Overall Result

FAIL
```

The system identified:

- Unsupported SPF claim
- Invisible finish claim requiring substantiation
- Trademark compliance concerns
- Brand messaging inconsistency

---

# 📸 LangSmith Observability

## Workflow Trace

![LangSmith Trace](images/langsmith-trace.png)

The complete LangGraph execution is monitored using LangSmith including:

- Workflow execution
- Token usage
- Latency
- Prompt tracing
- Node execution
- LLM calls

---

## Prompt & LLM Output

![LangSmith Output](images/langsmith-output.png)

Every LLM interaction is fully traceable including:

- System Prompt
- User Prompt
- Retrieved Context
- JSON Output
- Execution Time

---

# 🔍 Challenges Solved

During development the following production issues were resolved:

- Azure region restrictions
- Azure OpenAI deployment limitations
- Azure CLI authentication
- Azure Managed Identity configuration
- Storage Blob IAM permissions
- Azure Video Indexer authentication
- Transcript extraction failures
- OCR integration
- Prompt engineering
- JSON response validation

---

# 🛠 Installation

Clone repository

```bash
git clone https://github.com/<jatinvandranki>/Brand_Guardian.git
```

Install dependencies

```bash
uv sync
```

Run

```bash
uv run python main.py
```

---

# 🔑 Environment Variables

```
AZURE_OPENAI_ENDPOINT=
AZURE_OPENAI_API_KEY=
AZURE_OPENAI_CHAT_DEPLOYMENT=

AZURE_SEARCH_ENDPOINT=
AZURE_SEARCH_API_KEY=
AZURE_SEARCH_INDEX_NAME=

AZURE_VI_NAME=
AZURE_VI_LOCATION=
AZURE_VI_ACCOUNT_ID=
AZURE_SUBSCRIPTION_ID=
AZURE_RESOURCE_GROUP=

APPLICATIONINSIGHTS_CONNECTION_STRING=

LANGCHAIN_API_KEY=
LANGCHAIN_PROJECT=
```

---

# 🚀 Future Improvements

- Multi-language support
- Batch video auditing
- Real-time streaming
- Human review dashboard
- Confidence scoring
- Docker deployment
- Kubernetes deployment
- CI/CD Pipeline
- FastAPI REST API
- Web UI

---

# 👨‍💻 Author

## Harsh Bardhan Singh

AI/ML Engineer | Python | Azure AI | LLMOps | LangChain | LangGraph

GitHub: https://github.com/HarshBardhan571

LinkedIn: https://www.linkedin.com/in/harsh-bardhan-singh-618179291/
