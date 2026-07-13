# NexusScore 🏦📊

[![IDBI Innovate 2026](https://img.shields.io/badge/IDBI_Innovate-2026-green?style=for-the-badge)](https://hack2skill.com/event/idbinnovate)
[![Problem Statement](https://img.shields.io/badge/Problem_Statement-3_Financial_Health_Score-orange?style=for-the-badge)]()
[![Team](https://img.shields.io/badge/Team-NexusFin_AI-blue?style=for-the-badge)]()

> *Empowering credit-invisible MSMEs with AI-driven financial intelligence.*

---

## 📖 Overview

**NexusScore** is an AI-driven, multidimensional **MSME Financial Health Card** built for **IDBI Innovate 2026**.

India has over 63 million MSMEs. Most are **New-to-Credit (NTC)** or **New-to-Bank (NTB)** — they lack formal credit histories and get rejected by traditional scoring systems. NexusScore solves this by aggregating rich **alternate data streams** (GST, UPI, EPFO, Account Aggregator) and modeling them as a **live graph network** to compute a real-time, multidimensional Financial Health Score.

---

## 🚨 The Problem

- Banks rely on **traditional financial documents** that most MSMEs lack or maintain inadequately.
- Despite rich alternate data (GST, UPI, AA, EPFO), there's **no unified assessment framework**.
- This leads to **high rejection rates**, **missed viable borrowers**, and **slower financial inclusion**.

---

## 💡 Our Solution

NexusScore aggregates alternate data streams into a **Neo4j Graph Database**, maps B2B supply-chain relationships, and runs an **ML scoring engine** to generate a dynamic **Financial Health Score (300–900)**.

```
MSME applies for loan
        ↓
Consent via Account Aggregator
        ↓
Auto-pull GST + UPI + EPFO + Bank data
        ↓
Graph Modeling in Neo4j (supplier-buyer-transaction network)
        ↓
ML Scoring Engine (XGBoost + Scikit-Learn)
        ↓
IDBI Underwriter Dashboard → Approve / Reject
```

---

## 🚀 Key Features

| Feature | Description |
|---|---|
| 🔄 **Alternate Data Ingestion** | Auto-parses GSTIN returns, UPI volume, EPFO stability via AA framework |
| 📊 **Multidimensional Scoring** | ML-weighted score (300–900) across cash flow, supply chain, compliance |
| 🚦 **Visual Risk Dashboard** | Traffic Light UI for loan officers with drill-down into risk signals |
| 🕸️ **Supply Chain Graphing** | Maps B2B transactions to detect over-reliance on failing buyers |
| ⚡ **OCEN Integration** | API-ready for Open Credit Enablement Network one-click disbursement |

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | React.js, Next.js, Tailwind CSS |
| **Backend** | Node.js, Python (FastAPI) |
| **Graph Database** | Neo4j AuraDB |
| **Relational DB** | PostgreSQL (AWS RDS) |
| **AI / ML** | Scikit-Learn, XGBoost, Pandas |
| **Cloud & DevOps** | AWS EC2, Docker, GitHub Actions |
| **Integrations** | Account Aggregator APIs, OCEN APIs, ULI Ecosystem |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────┐
│           React.js Underwriter UI           │
│         (Traffic Light Score Card)          │
└──────────────────┬──────────────────────────┘
                   │
┌──────────────────▼──────────────────────────┐
│         Node.js API Gateway                 │
│    (Auth + Routing + Webhooks)              │
└──────┬───────────────────────┬──────────────┘
       │                       │
┌──────▼───────┐    ┌──────────▼──────────────┐
│  AA / OCEN   │    │   Python FastAPI ML      │
│  Data Pull   │    │   (XGBoost Scoring)      │
└──────┬───────┘    └──────────┬──────────────┘
       │                       │
┌──────▼───────────────────────▼──────────────┐
│      Neo4j AuraDB + PostgreSQL              │
│   (Graph Relationships + Metrics Store)     │
└─────────────────────────────────────────────┘
```

---

## 📈 Roadmap

- **Phase 1 (MVP):** Aggregate UPI + GST data → Basic alternate credit score. Validate against CIBIL.
- **Phase 2 (Integration):** Full ULI + OCEN integration → One-click loan disbursement. Pilot with 100 IDBI branches.
- **Phase 3 (Scale):** WhatsApp Financial Health Bot → Weekly AI-driven tips to help MSMEs improve their NexusScore and unlock better interest rates.

---

## 💰 Estimated Cost

| Resource | Cost/Month |
|---|---|
| AWS (EC2, RDS, API Gateway) | ~$500 |
| Neo4j AuraDB Professional | ~$65 |
| AA/OCEN API Calls | ~$0.05/query |
| **Total MVP** | **~$600–800** |

---

## 👩‍💻 Team

**Team Name:** NexusFin AI  
**Team Leader:** Swati Gupta  
**Hackathon:** IDBI Innovate 2026 — Problem Statement 3: Financial Health Score  

---

## 📄 License

[MIT License](./LICENSE)
