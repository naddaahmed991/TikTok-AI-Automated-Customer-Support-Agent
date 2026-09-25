# TikTok-AI-Automated-Customer-Support-Agent
An end-to-end automated workflow built with **n8n**, integrating **TikTok API**, **Groq LLM**, and **Telegram** to provide intelligent, real-time responses to incoming TikTok messages and comments with human-in-the-loop fallback.
🌟 Overview
This project automates customer support for TikTok by instantly processing incoming direct messages and comments. Powered by Groq LLM, the AI Agent evaluates the context of each message, formulates appropriate replies, and seamlessly routes complex inquiries to a Telegram channel for human review.

🚀 Key Features
🔐 OAuth 2.0 Authentication: Handles TikTok OAuth callback logic to securely request and retrieve Access Tokens.

📬 Webhook Event Listener: Captures real-time incoming events (Messages/Comments) from TikTok.

🧹 Data Normalization: Cleans and standardizes JSON payloads for reliable processing.

🧠 AI-Powered Decision Making: Evaluates user intent and sentiment using Groq Chat Model.

👨‍💻 Human-in-the-Loop (HITL): Automatically flags edge cases and routes them to a Telegram channel for manual intervention.

📤 Automated TikTok Response: Prepares and dispatches contextual replies back to TikTok via REST HTTP Requests.

🛠️ Tech Stack
Workflow Engine: n8n

AI Model: Groq API (LLaMA-3)

Integrations: TikTok API (Webhooks, Direct Messages, OAuth 2.0), Telegram Bot API

Tunneling / Webhook: ngrok 
🔄 Workflow Architecture
[TikTok Incoming Webhook]
           │
           ▼
[Normalize Event] ──► [Message Check] ──► [TikTok AI Agent (Groq)]
                                                      │
                                           ┌──────────┴──────────┐
                                           ▼                     ▼
                                  (Needs Human Review)     (Auto-Reply)
                                           │                     │
                                           ▼                     ▼
                                  [Telegram Alert]      [TikTok Send Reply]
<img width="1280" height="680" alt="image" src="https://github.com/user-attachments/assets/91e6bbfe-e36d-4fe1-b66f-8fb65af91c64" />
