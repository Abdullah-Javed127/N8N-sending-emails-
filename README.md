# N8N-sending-emails-
# 📧 Generic Send Email Workflow (n8n)

A reusable **n8n workflow** for sending emails via a POST request.  
Built for easy deployment to multiple clients with **zero JSON edits** — just update environment variables and SMTP credentials.

---

## 🚀 Features
- Accepts POST requests via **Webhook**
- Uses **environment variables** for easy configuration
- Sends plain-text email with dynamic `to` and `message` fields
- Works across multiple clients with no workflow changes
- Secure — credentials stored in n8n, not hardcoded

---

## 📂 Workflow Overview
1. **Webhook Node**  
   Receives POST requests at a configurable path.
2. **Send Email Node**  
   Sends the email using configured SMTP credentials.

---

## 🛠️ Setup

### 1️⃣ Import Workflow
- Go to **n8n → Workflows → Import from File**
- Select the provided `.json` file

### 2️⃣ Configure Environment Variables
Set the following environment variables in your `docker-compose.yml`, `.env` file, or hosting platform:

```env
FROM_EMAIL=no-reply@yourdomain.com
EMAIL_SUBJECT=Message from chatbot
WEBHOOK_PATH=send_email
