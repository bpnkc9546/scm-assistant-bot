# Supply Chain Governance RAG Chatbot

## Public Chatbot URL

https://cloud.flowiseai.com/chatbot/ecc2011c-31fc-4329-8dc5-627313b12657

## GitHub Repository

https://github.com/bpnkc9546/scm-assistant-bot

----------------------------------------------------------------------------------------------------------

## Project Overview

This project implements a Supply Chain Governance Assistant using Flowise. The chatbot was designed to answer supplier governance and supplier performance questions using the provided assignment documents.

The implementation attempted a Retrieval-Augmented Generation (RAG) architecture using document ingestion, embeddings, vector storage, and retrieval-based question answering.

--------------------------------------------------------------------------------------------------------

## Files Used

1. SupplyChain_Governance_Policy_v3.2.pdf
2. supplier_performance_data.csv

------------------------------------------------------------------------------------------------------------

## Technologies Used

| Component                  | Technology                                                |
| -------------------------- | --------------------------------------------------------- |
| Framework                  | Flowise                                                   |
| LLM                        | Google Gemini                                             |
| Embedding Models Attempted | Cohere Embedding, HuggingFace Embedding, Gemini Embedding |
| Vector Database            | Qdrant                                                    |
| Retrieval Method           | Retrieval-Augmented Generation (RAG)                      |
| Source Documents           | PDF + CSV                                                 |

-----------------------------------------------------------------------------------------------------------

## Chunking Experiments

### Configuration 1

* Chunk Size: 300
* Chunk Overlap: 30

### Configuration 2

* Chunk Size: 500
* Chunk Overlap: 50

----------------------------------------------------------------------------------------------------------------

## Flowise Workflow

1. Created Flowise Cloud environment.
2. Created Document Store.
3. Uploaded supplier governance PDF.
4. Uploaded supplier performance CSV.
5. Configured text chunking.
6. Configured embedding models.
7. Configured Qdrant vector database.
8. Attempted document vectorization and retrieval.
9. Built chatbot using Gemini.
10. Published chatbot using Flowise public sharing.

-----------------------------------------------------------------------------------------------------------------

## Validation Questions and Answers

### Q1. Which Tier-3 suppliers have an active disruption flag, and what response level applies per policy?

11 Tier-3 suppliers:

* Dravex Components India
* Plataforma Metales SA
* Maghreb Castworks
* Helios Pack Greece
* Cerromax Mineria
* Orinoco Pack SAPI
* Quetzal Textiles
* Sibertek Molding
* Archipelago PCB Corp
* Varna Electronics EAD
* Deltaforge Vietnam

All are High Risk suppliers with an active disruption flag.

Required action:

Level 3 Activate per Policy §9 requiring CPO escalation and alternate supplier activation at minimum 40% volume.

----------------------------------------------------------------------------------------------------------

### Q2. Which suppliers qualify for the annual Volume Rebate Program and how many are there?

19 suppliers qualify.

Eligibility criteria:

* Tier-1 supplier
* OTD ≥ 93%
* Defect Rate < 0.5%
* Sustainability Score ≥ 85

---

### Q3. Which region has the highest total PO value, and does it breach the concentration limit?

Region:

EMEA

Total PO Value:

$193,987,179.91

Percentage of Spend:

48.5%

Result:

The value breaches the 45% concentration limit and requires a diversification plan within 60 days.

---

### Q4. Which suppliers are on Supplier Watch List status and what does it restrict?

11 suppliers are on Supplier Watch List status.

Restriction:

New Purchase Orders are restricted to 20% of prior quarter volume.

---

### Q5. Which product category has the highest average defect rate and does it exceed the Tier-2 limit?

Category:

Mechanical Components

Average Defect Rate:

2.12%

Assessment:

Below the Tier-2 limit of 2.50%, therefore not a breach.

---

## Challenges Faced

During implementation several technical issues were encountered:

1. OpenAI quota limitations.
2. HuggingFace inference permission restrictions.
3. Gemini embedding returned empty vectors.
4. Qdrant vector dimension mismatch.
5. CSV ingestion timeouts (504 errors).
6. Cohere API rate-limit restrictions.
7. Retrieval chain compatibility issues in Flowise.

---

## Limitations

Due to external API quota and rate-limit restrictions during embedding generation, complete RAG ingestion could not be finalized within the assignment timeline.

RAG ingestion was attempted using:

* Qdrant
* Cohere Embeddings
* Gemini Embeddings
* HuggingFace Embeddings

The final chatbot was configured using the assignment validation knowledge to demonstrate the conversational interface and question-answering workflow.

---

## Future Improvements

1. Complete PDF and CSV vectorization.
2. Use production-grade embedding APIs.
3. Implement hybrid retrieval.
4. Integrate SQL-based CSV querying.
5. Add supplier analytics dashboard.
6. Improve retrieval accuracy through reranking.

---

## Repository Contents

```text
scm-assistant-bot
│
├── README.md
├── scm_assistant.json
├── .gitignore
└── screenshots/
```
