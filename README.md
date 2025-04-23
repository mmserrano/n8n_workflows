# 🤖 n8n Workflows – Automations with AI and External Tools

This repository contains ready-to-use workflows built for [n8n](https://n8n.io), focused on AI agents, automation with vector databases, chat interfaces, and more.

Each workflow is designed to be practical, clearly structured, and easy to integrate. As this repository grows, it will include more examples covering different use cases—from document automation to advanced AI agents and system orchestration.

---

## 📦 Current Workflows

### 🧠 AI Agent with Supabase + PostgreSQL

- Accepts user input via webhook
- Routes input through an OpenAI-powered AI Agent
- Uses Supabase vector store to retrieve contextually relevant information
- Maintains chat context via PostgreSQL memory
- Built with modular tools: embeddings, chat models, and tool invocation

---

## ⚙️ Getting Started

1. Import the JSON file into your n8n instance.
2. Set up credentials.
3. Update the webhook URLs and data mappings if needed.
4. Run the workflow and start interacting!

---

## 🔐 Notes on Security

All credentials (`id` and `name`) have been anonymized.  
Make sure to configure your own API keys and database connections within your n8n instance.

---

## 📂 Structure

```plaintext
n8n_workflows/
├── RAG_Agent.json
├── README.md
```
---

## Created By
Name: Mariola Martínez

Reach out: contacto@aiflow.es

