# # 🤖 AI Interview Automation System (n8n Workflow)

## 📌 Overview

This project is an end-to-end **AI-powered interview automation system** built using **n8n**.

It automates the full hiring pipeline:

* Creating an AI interview agent
* Collecting candidate responses
* Analyzing interview performance using AI
* Saving structured results into Google Sheets

The system is designed to help HR teams **evaluate candidates automatically and efficiently**.

---

## ⚙️ Workflow Architecture

### 🔹 Step 1: Job Setup & Configuration

* Input job details (title, company, requirements, skills)
* Initialize the workflow manually
* Prepare structured job description for the AI agent

---

### 🔹 Step 2: AI Interview Agent Creation

* Create a custom AI interview agent dynamically
* Generate a unique interview link for candidates
* Store agent information for later use

---

### 🔹 Step 3: Interview Processing & Analysis

Triggered automatically when a candidate completes the interview:

* 📥 Receive interview data via **Webhook**
* 📊 Fetch agent/job data from Google Sheets
* 🤖 Analyze candidate responses using AI

The AI generates:

* Interview score (1–10)
* Strengths & weaknesses
* Hiring recommendation
* Improvement suggestions

---

### 🔹 Step 4: Data Formatting & Storage

* Format structured output
* Save results into **Google Sheets**
* Maintain a centralized database of candidates

---

## 🛠️ Tech Stack

* **n8n** (Workflow Automation)
* **AI Model (LLM)** for interview analysis
* **Google Sheets API**
* Webhooks for real-time data processing

---

## 🔄 Workflow Flow (Simplified)

```id="flow1"
Job Setup → Create AI Agent → Generate Interview Link  
        ↓  
Candidate Takes Interview  
        ↓  
Webhook Trigger → AI Analysis → Format Data → Save to Sheets
```

---

## 🚀 Getting Started

### 1. Run n8n

```bash id="run1"
npm install n8n -g
n8n
```

---

### 2. Import Workflow

1. Open n8n (http://localhost:5678)
2. Click **Import**
3. Upload the workflow JSON file

---

### 3. Configure Integrations

#### 🔑 Required Credentials:

* Google Sheets API
* AI Model API (OpenAI / OpenRouter / etc.)

---

### 4. Setup Google Sheets

Create a sheet with:

* Candidate Name
* Score
* Strengths
* Weaknesses
* Recommendation

---

### 5. Run the System

* Execute Step 1 manually to create the agent
* Share interview link with candidates
* Results will be processed automatically

---

## 📸 Screenshots

### Workflow Overview

*Add your screenshots here*

---

## 💡 Use Cases

* HR automation systems
* AI-powered recruitment platforms
* Candidate screening tools
* Interview analytics dashboards

---

## 🔐 Security Notes

* Do NOT expose API keys in workflow exports
* Use environment variables or n8n credentials
* Protect webhook endpoints if deployed publicly

---

## 📈 Future Improvements

* Dashboard for candidate analytics
* Integration with ATS systems
* Multi-language interview support
* Voice-based interviews

---

## 🤝 Contributing

Feel free to fork and improve this project.

---

## 📄 License

MIT License
