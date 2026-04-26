# 🧠 FairMind AI — Bias Detection & Fairness Platform
**No-code AI bias detection platform. Upload dataset → Detect bias → Auto-fix → Get Gemini AI report.**
---
## 🚨 The Problem

AI systems in **hiring, loans, and healthcare** silently discriminate. A resume-screening AI might reject women 39% more often. A loan approval model might disadvantage minorities. These systems operate as black boxes — organizations have no way to audit them.

> 📌 **FairMind AI solves this: making AI fairness auditing accessible to everyone, no coding required.**

---

## ✅ Solution Overview

FairMind AI is a **no-code bias detection and auto-mitigation platform** that:

1. 📂 Accepts any CSV dataset (hiring, loans, healthcare, criminal justice)
2. 🔍 Auto-detects protected attributes (gender, race, age)
3. 📊 Computes **6 fairness metrics** (Demographic Parity, Equalized Odds, etc.)
4. 🤖 Uses **Google Gemini 1.5 Pro** to generate plain-English audit reports
5. 🔧 Applies **3 mitigation strategies** to auto-fix detected bias
6. 📈 Shows **Before vs After** fairness score comparison

### 🎯 Real Results
| Dataset | Before | After | Time |
|---------|--------|-------|------|
| UCI Adult Income (48,842 records) | 42/100 ⚠️ | 89/100 ✅ | 8 sec |
| COMPAS Recidivism | 45/100 ⚠️ | 92/100 ✅ | 11 sec |

---

## 🌟 Key Features

| Feature | Description |
|---------|-------------|
| 🚫 **No-Code Dashboard** | Upload CSV, get audit in 60 seconds |
| 🤖 **Gemini AI Reports** | Plain-English bias explanations + fix recommendations |
| 📏 **6 Fairness Metrics** | Demographic Parity, Equalized Odds, Calibration, and more |
| 🔧 **Auto-Mitigation** | Reweighing / Adversarial Debiasing / Calibrated Odds |
| 📊 **Before vs After** | Visual fairness score comparison |
| 🌍 **Multi-Domain** | Hiring, loans, healthcare, criminal justice |
| 🔌 **REST API** | Plug into any existing AI pipeline |
| 📄 **PDF Reports** | Downloadable audit reports for compliance |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        FairMind AI                          │
├──────────────┬──────────────────────────┬───────────────────┤
│   Frontend   │        Backend           │    AI Engine      │
│  React.js    │   FastAPI + Docker       │  IBM AIF360       │
│  Tailwind    │   Google Cloud Run       │  Fairlearn        │
│  Chart.js    │   Firebase Hosting       │  scikit-learn     │
│              │                          │  SHAP             │
├──────────────┴──────────────────────────┴───────────────────┤
│                     Google AI Stack                         │
│  Gemini 1.5 Pro │ Cloud Run │ Firebase │ Firestore │ BigQuery│
└─────────────────────────────────────────────────────────────┘
```

### Process Flow

```
Upload CSV Dataset
      ↓
Auto-detect protected attributes (gender, race, age)
      ↓
Compute 6 Fairness Metrics
      ↓
Gemini AI generates plain-English audit report
      ↓
Apply mitigation → retrain model
      ↓
View Before vs After fairness scores
```

---

## 🛠️ Tech Stack

### Google / Cloud
- **Gemini 1.5 Pro** — Natural language bias audit reports
- **Google Cloud Run** — Serverless backend deployment
- **Firebase Hosting** — Frontend hosting
- **Firestore** — Session management
- **Cloud Storage** — Dataset storage
- **BigQuery** — Analytics
- **Google Cloud IAM** — Security

### AI / ML
- IBM AIF360
- Fairlearn
- scikit-learn
- SHAP (model explainability)

### Frontend
- React.js
- Tailwind CSS
- Chart.js

### Backend
- Python 3.11
- FastAPI
- Docker

---

## 🚀 Getting Started

### Prerequisites
- Python 3.11+
- Node.js 18+
- Google Cloud account
- Gemini API key


## 📡 API Reference

### Analyze Dataset
```http
POST /api/analyze
Content-Type: multipart/form-data

file: <csv_file>
target_column: "income"
protected_attributes: ["gender", "race"]
```

**Response:**
```json
{
  "fairness_score": 42,
  "metrics": {
    "demographic_parity": -0.198,
    "equalized_odds": -0.143
  },
  "gemini_report": "Gender bias detected. Women are 30% less likely...",
  "recommendations": ["Apply Reweighing algorithm"]
}
```

### Apply Mitigation
```http
POST /api/mitigate
Content-Type: application/json

{
  "session_id": "abc123",
  "strategy": "reweighing"
}
```

---

## 📊 Demo Datasets

The following public datasets are included for testing:

| Dataset | Domain | Records | Protected Attributes |
|---------|--------|---------|---------------------|
| UCI Adult Income | Hiring | 48,842 | Gender, Race |
| COMPAS | Criminal Justice | 7,214 | Race, Age |
| German Credit | Finance | 1,000 | Gender, Age |

---

## 💰 Pricing

| Plan | Price | Features |
|------|-------|----------|
| **Free** | $0/mo | 5 audits/month, basic metrics |
| **Pro** | $29/mo | Unlimited audits, Gemini reports, API access |
| **Enterprise** | $299/mo | Custom domains, SOC 2, dedicated support |

> 🎓 **Free for researchers and NGOs** — open-source core library available

---

## 🗺️ Roadmap

- **Q3 2026** — Mobile app + NLP/Image bias support + Hugging Face integration
- **Q4 2026** — Slack/Teams alerts, scheduled audits, SOC 2 compliance
- **2027** — Real-time monitoring, HIPAA & Fair Lending templates, multi-language support

**Goal: 1,000+ organizations using fair AI by 2027** 🎯

---

## 👥 Team

**Team B2Boys** — FairMind AI Solution Challenge 2026

| Name | Role |
|------|------|
| **Vishal** | Team Leader |

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- [IBM AIF360](https://github.com/Trusted-AI/AIF360) — Fairness metrics library
- [Microsoft Fairlearn](https://fairlearn.org/) — ML fairness toolkit
- [Google Gemini](https://deepmind.google/technologies/gemini/) — AI report generation
- [UCI ML Repository](https://archive.ics.uci.edu/) — Demo datasets

---

<div align="center">

Built with ❤️ for **Google Solution Challenge 2026**

[![Google Solution Challenge](https://img.shields.io/badge/Google-Solution%20Challenge%202026-4285F4?style=for-the-badge&logo=google)](https://developers.google.com/community/gdsc-solution-challenge)

</div>
