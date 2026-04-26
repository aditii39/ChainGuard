# 🛡️ ChainGuard (Smart Contract Security Auditor)

AI-powered smart contract auditing API built with **FastAPI**, **CrewAI**, and **LLMs**. Automatically detects vulnerabilities, suggests gas optimizations, and evaluates code quality.

🔗 **Live Demo:** [https://your-live-app-link.com](https://your-live-app-link.com)

---

## 🚀 Features

* 🔍 **Security Analysis** — Detects common vulnerabilities (reentrancy, access control, etc.)
* ⚡ **Gas Optimization** — Suggests ways to reduce transaction costs
* 📊 **Code Quality Scoring** — Rates contract quality (0–100)
* 🤖 **Multi-Agent AI System** — Uses CrewAI agents for specialized analysis
* 🌐 **REST API** — Easy integration with frontend or other tools

---

## 🧱 Tech Stack

* **FastAPI**
* **CrewAI**
* **LangChain**
* **Groq** or **Google Gemini** (LLM)
* **Python 3.10+**

---

## 📦 Installation

```bash
git clone <your-repo-url>
cd smart-contract-auditor

python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file in the root directory:

### If using Groq:
```env
GROQ_API_KEY=your_groq_api_key
```

### OR if using Google Gemini:
```env
GOOGLE_API_KEY=your_google_api_key
```

---

## ▶️ Run the Server

```bash
python main.py
```

Server will start at: `http://localhost:8000`

---

## 📡 API Endpoints

### Health Check
`GET /health`

### Audit Smart Contract
`POST /audit`

#### Request Body
```json
{
  "contract_name": "MyToken",
  "contract_language": "Solidity",
  "contract_code": "pragma solidity ^0.8.0; ..."
}
```

#### Response
```json
{
  "contract_name": "MyToken",
  "severity_score": 7,
  "code_quality_score": 80,
  "vulnerabilities": [],
  "gas_optimizations": [],
  "security_recommendations": [],
  "detailed_report": "..."
}
```
