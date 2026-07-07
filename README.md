# 🤖 WhatsApp AI Agent - n8n Workflow

[![n8n](https://img.shields.io/badge/n8n-Advanced_Workflow-blueviolet)](https://n8n.io)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT4-green)](https://openai.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-Business_API-green)](https://business.whatsapp.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **Transform your WhatsApp Business into an intelligent, AI-powered conversational agent.** Automate customer interactions, handle queries, and provide instant support 24/7.

<img width="1679" height="821" alt="Whatsapp Agent" src="https://github.com/user-attachments/assets/ea017a84-40a7-4e3a-9bfe-f4bfdd1a99a9" />

---

### ✨ Features

- **AI-Powered Conversations** – Uses OpenAI GPT-4 to understand and respond to user intents naturally.
- **WhatsApp Business Integration** – Seamless connection to your WhatsApp Business Cloud API.
- **Smart Intent Routing** – Automatically detects if a user is sending a text message, an image, or an audio file.
- **Contextual Memory** – Retains conversation history to provide coherent, multi-turn interactions.
- **Image & Audio Analysis** – Ability to analyze media inputs and respond appropriately.
- **Modular Architecture** – Cleanly separated input parsing, AI processing, and output formatting.
- **Scalable & Extensible** – Easily integrate with external APIs, calendars, or CRM tools.

---

### 📋 Workflow Overview

This workflow acts as the central brain for your WhatsApp Business account. It listens for incoming messages, routes them through a specialized AI Agent equipped with tools and memory, and generates high-quality responses.

1. **Incoming Webhook:** Captures messages from WhatsApp.
2. **Intent Router:** Classifies the message type (Text, Image, Audio).
3. **Agent Processing:** Sends data to an AI Agent (OpenAI GPT-4) with relevant context.
4. **Decision Loop:** The Agent decides if a tool (Calculator, Search) is needed.
5. **Response:** The AI generates a final, customized reply sent back to the user.

---

### 🧠 How It Works

The workflow uses a **Switch Node** to handle different message types.
*   **Text Input:** Passes directly to the AI Agent along with existing memory.
*   **Media Input:** Downloads media via HTTP requests and forwards it to OpenAI's vision/audio models for analysis before injecting the context into the AI Agent.
*   **Memory:** The `Simple Memory` node ensures the AI remembers the user's previous messages, allowing for natural back-and-forth conversations.
*   **Tools:** The AI can decide to use tools like a `Calculator` or `SerpAPI` (for internet search) to augment its knowledge before finalizing a response.

---

### 🔧 Requirements

*   **n8n Version:** 1.0.0 or higher (Self-hosted or Cloud).
*   **OpenAI API Key:** For the Chat Model and Image Analysis.
*   **WhatsApp Business Cloud API:** Requires an approved Meta Developer app.
*   **SerpAPI Key:** Optional, but required for web search capabilities.
*   **Redis/In-Memory Database:** To support the "Simple Memory" node (if enabled).

---

### 🔑 Environment Variables

Create a `.env` file or configure these directly in your n8n credentials:

```ini
OPENAI_API_KEY=sk-XXXXXXXXXXXXXXXXXXXXXXXX
WHATSAPP_ACCESS_TOKEN=XXXXXXXXXXXXXXXXXX
WHATSAPP_PHONE_NUMBER_ID=XXXXXXXXXXXXXX
WHATSAPP_VERIFY_TOKEN=XXXXXXXXXXXXXXXXXX
SERPAPI_API_KEY=XXXXXXXXXXXXXXXXXXXXXXXX
💼 Business Use Cases
24/7 Customer Support: Instantly answer FAQs, guide users through troubleshooting, and route complex issues to a human.

Lead Qualification: Gather user information, qualify leads, and automatically schedule follow-ups with CRM integration.

Internal Knowledge Base: Connect to a Knowledge Base (RAG) to provide accurate company-specific information instantly.

🛠 Future Improvements
Integration with Google Calendar for automated appointment scheduling.

Adding a dedicated Knowledge Base (Pinecone/Weaviate) for specific industry data (RAG).

Multi-language detection and automatic translation responses.

📝 License
Distributed under the MIT License. See LICENSE for more information.

💼 Portfolio Description
This project demonstrates advanced AI automation by combining n8n's powerful workflow engine with OpenAI's language models and the WhatsApp Business API. It showcases my ability to build complex, conditional logic systems, integrate third-party APIs, and design "No-Code" AI agents that solve real-world communication challenges.

📈 Client Pitch
Transform your business communication instantly. This AI-powered WhatsApp agent automates customer support, filters leads, and provides 24/7 intelligent responses, reducing your operational overhead while significantly increasing your response speed and customer satisfaction.

text

---


Repository Structure
text
whatsapp-ai-agent-n8n/
│
├── workflow.json
├── screenshot.png
├── README.md
├── LICENSE
└── .gitignore
GitHub Topics
text
n8n
automation
ai-agent
whatsapp
openai
chatbot
workflow
langchain
llm
api
integration
customer-support
nocode
lowcode
webhook
business-api
gpt-4
conversational-ai
whatsapp-business
productivity
Portfolio Description
This project showcases a fully functional, enterprise-ready AI agent built entirely within n8n. By integrating WhatsApp Business, OpenAI's GPT-4, and custom routing logic, the workflow demonstrates advanced skills in event-driven architecture, media processing, and stateful conversational AI, proving expertise in modern "No-Code" automation.

Client Pitch
Stop losing leads to slow response times. This AI agent automates your entire WhatsApp support and sales pipeline, instantly answering queries, analyzing images, and engaging customers in natural dialogue—turning your phone number into your most powerful business asset, running 24/7 without additional headcount.
