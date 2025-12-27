🌐 **n8n Automation Projects**

This repository showcases all automation workflows I developed using n8n, including real-world systems like website uptime monitoring, backend API alerts, WhatsApp notifications, Google Sheet-controlled workflows, and a custom RAG AI agent that answers customer queries using website data.

This repo represents my journey into becoming an Automation Engineer — creating scalable, cloud-deployed systems that reduce manual work and give businesses superpowers 🚀

📁 **What’s Inside**

Project	Description	Tech

🟢 Website Monitoring System	Monitors multiple websites, checks status, logs uptime, sends alerts when site is down	n8n + HTTP Node + Gmail API

📊 Google-Sheet Controlled Automation	Websites/servers list managed through Google Sheet — no need to edit n8n to add/remove items	n8n + Google Sheets

🧠 AI RAG Agent (Website Support Bot)	AI chatbot that answers questions about the website using RAG + website data scraping	OpenAI + Vector DB + n8n

🔔 Alert System via Email / WhatsApp	Sends notifications when failure is detected (email + optional WhatsApp using Twilio/WA Cloud API)	Gmail API / WhatsApp Cloud API

🌩️ Cloud Deployment	n8n deployed on Google Cloud VM / Docker with persistent DB	Docker + EC2/VM hosting

🗄️ Logging System	Saves uptime / downtime logs into Google Sheets or Database	Google Sheets + Postgres

1️⃣ —**Website Monitoring System**

Instead of manually adding website URLs inside n8n,
this automation reads website list from Google Sheet, including:

✔ Website URL
✔ Check Interval
✔ Expected Keyword / Regex Pattern
✔ Notification Email
✔ Custom Alert Message

📌 Workflow Logic

Schedule Trigger → Read Google Sheet → Loop URLs → HTTP Request → 
Check Response → Match Regex/Keyword → If Fail:
  → Send Email Alert → Log Failure
Else:
  → Log Success

  🤖 2️⃣ — **AI Website Support – RAG Agent**

I built a Retrieval-Augmented Generation (RAG) Agent that:

✔ Reads website content (scraped / uploaded data)
✔ Stores chunks into a vector database
✔ Lets customers chat & ask questions
✔ Replies using context-aware AI

Example Use-Cases:

Ask: "What services does this website provide?"

Ask: "How do I contact support?"

Ask: "Is there a farmer loan feature?"


🚀 **How to Use These Workflows**
Import Steps

1️⃣ Open your n8n instance
2️⃣ Go to Workflows → Import from file
3️⃣ Select .json workflow file from this repo
4️⃣ Add your credentials (Google Sheets, Gmail, OpenAI, WhatsApp etc.)
5️⃣ Activate workflow


