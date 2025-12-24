# Sentinel AI: LLM Security Gateway & Firewall

![Status](https://img.shields.io/badge/Status-Production%20Ready-green) ![Security](https://img.shields.io/badge/Security-LLM%20Defense-red) ![Docker](https://img.shields.io/badge/Docker-Containerized-blue) ![Python](https://img.shields.io/badge/Built%20With-LangChain-orange)

> **An application-layer firewall designed to secure Large Language Models (LLMs) against Prompt Injection, Jailbreaking, and Data Exfiltration.**

## ⚠️ The Problem
As enterprises integrate LLMs (like GPT-4 or Llama 2) into production workflows, they face critical new security risks:
* **Prompt Injection:** Attackers manipulating the model to ignore instructions and perform unauthorized tasks.
* **Jailbreaking:** Using "DAN" (Do Anything Now) techniques to bypass safety filters.
* **PII Leakage:** The accidental exposure of sensitive user data in model responses.

## 🛡️ The Solution: Sentinel AI
Sentinel AI sits as a middleware gateway between the User and the LLM. It uses a **multi-stage defense pipeline** to sanitize inputs and validate outputs in real-time.

### Key Features
* **Regex Sanitization:** Instantly blocks known attack signatures and malicious patterns using a curated library of jailbreak prompts.
* **NLP Vector Analysis:** Uses semantic embeddings to detect the *intent* of a prompt, catching sophisticated attacks that bypass keyword filters.
* **PII Redaction:** Automatically detects and masks sensitive entities (Emails, Phone Numbers, Credit Cards) before they reach the model provider.
* **Low Latency:** Designed for high-throughput environments with <150ms overhead per request.

## 🛠️ Technical Architecture
* **Core Engine:** Python 3.10+
* **Orchestration:** LangChain
* **Analysis:** NumPy & OpenAI Embeddings (for vector similarity checks)
* **Deployment:** Docker & FastAPI

## 🚀 Quick Start

### Prerequisites
* Python 3.10+
* Docker (Optional)

### 1. Installation
Clone the repository and install dependencies:
```bash
git clone [https://github.com/YourUsername/Sentinel-AI.git](https://github.com/YourUsername/Sentinel-AI.git)
cd Sentinel-AI
pip install -r requirements.txt
