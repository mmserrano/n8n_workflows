# 🤖 n8n Workflows – Automations with AI and External Tools

This repository contains ready-to-use workflows built for [n8n](https://n8n.io), focused on AI agents, automation with vector databases, chat interfaces, and more.

Each workflow is designed to be practical, clearly structured, and easy to integrate. As this repository grows, it will include more examples covering different use cases—from document automation to advanced AI agents and system orchestration.

---

## 📦 Current Workflows

### 📍 Lead Generation from Google Maps

This workflow automates the extraction of business email addresses from Google Maps search results, using AI-powered search query generation and website scraping.

- Uses Google Gemini for intelligent search query generation
- Automatically extracts email addresses from business websites
- Stores results in Google Sheets
- Delivers results via email in CSV format
- Includes a user-friendly form interface

### 🧠 AI Agent with Supabase + PostgreSQL

- Accepts user input via webhook
- Routes input through an OpenAI-powered AI Agent
- Uses Supabase vector store to retrieve contextually relevant information
- Maintains chat context via PostgreSQL memory
- Built with modular tools: embeddings, chat models, and tool invocation

### 🌐 Brave Search via Telegram (MCP Integration)

This workflow allows users to perform Brave Search queries directly within a Telegram chat. It listens for the command `/brave your search`, cleans the query, retrieves available Brave tools, and executes the search with results sent back as a formatted Telegram message.

- Uses the [n8n-nodes-mcp](https://github.com/nerding-io/n8n-nodes-mcp) community node
- Integrates Brave Search API via MCP credentials
- Telegram bot acts as the user interface
- Search trigger is `/brave ...`
- Includes rich setup instructions via `Sticky Notes`

> 🛠 Setup Requirements:
> - Brave API Key (`BRAVE_API_KEY`)
> - MCP plugin installed on your n8n instance
> - Telegram bot access token

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

## Created By
Name: Mariola Martínez

Reach out: contacto@aiflow.es

