# IzerdAI 🤖

> A full-featured AI chatbot project powered by Google Gemini API.  
> Developed by **cwcbox**

---

## 🧠 What is IzerdAI?

IzerdAI is a modern, intelligent chatbot web application built with:

- 🔧 **React (frontend)** with Vite
- 🚀 **Node.js + Express (backend)**
- ☁️ **Google Gemini API** for AI capabilities
- 📦 **Render** for deployment
- 🔐 **Secure admin login**, daily token cost control, and more!

This is a lightweight yet powerful platform where you can chat with AI, upload documents, switch models, and manage usage securely.

---

## 🌐 Platform & Stack

| Layer      | Tech Used          |
|------------|--------------------|
| Frontend   | React + Tailwind + Vite |
| Backend    | Node.js + Express.js |
| AI API     | Google Gemini API (via `@google/generative-ai`) |
| Hosting    | Render (Static Site + Web Service) |
| Security   | bcrypt + JWT, CORS origin checks |
| Upload     | Multer (60MB max), automatic Gemini summarizer |

---

## 🧩 Core Features

| Feature | Description |
|--------|-------------|
| ✅ Model Selection | Choose among `gemini-pro`, `gemini-1.5-pro`, etc., and view their capabilities |
| ✅ Daily Token Limit | Set token cost caps (e.g., 100,000 tokens/day) to avoid high bills |
| ✅ File Upload (60MB) | Upload files, trigger **Gemini summary** automatically |
| ✅ Admin Login | Protected by bcrypt + JWT, set password via environment |
| ✅ Theme Toggle | Switch between **Dark / Light** theme |
| ✅ CORS Security | API only allows specific frontends via Origin + Referer check |
| ✅ Request Logging | Tracks usage for every request with timestamp, model, cost |
| ✅ Frontend UI | Minimalist chat UI with file upload, tone setting, model menu |
| ✅ Secure Key Storage | All secrets via Render **environment variables** |
| ✅ Deployment Ready | Complete guide and deploy buttons for Render

---

## 📁 Project Structure

```
izerd-ai/
├── client/                # React frontend
│   ├── public/
│   ├── src/
│   ├── vite.config.js
│   ├── package.json
│   └── .env.example
├── server/                # Express backend
│   ├── index.js
│   ├── package.json
│   └── .env.example
├── public/assets/         # Logo / Cover
│   ├── favicon.png
│   └── cover.png
├── README.md
└── RENDER_DEPLOY_GUIDE.md
```

---

## 🔑 API Integration

This project uses Google Gemini API via:

```bash
npm install @google/generative-ai
```

Used models:

- `gemini-pro`
- `gemini-1.5-pro`
- Model-specific prompt templates
- Token usage tracked via `usageMetadata`

See official API docs:  
[![Google Gemini API Docs](https://img.shields.io/badge/View%20Gemini%20Docs-Google-blue?style=for-the-badge)](https://ai.google.dev/gemini-api/docs)

---

## 🧪 Local Development

```bash
# Frontend
cd client
npm install
npm run dev

# Backend
cd server
npm install
node index.js
```

---

## 🔐 Admin Auth

You can set your admin login via bcrypt hash in `.env`:

```env
ADMIN_PASSWORD_HASH=$2b$10$hashedPasswordHere
```

Login is via `/admin` with JWT authentication.

---

## 📦 Deploy to Render

[![Deploy Backend to Render](https://img.shields.io/badge/Deploy%20Backend-Render-blue?style=for-the-badge)](https://render.com)
[![Deploy Frontend to Render](https://img.shields.io/badge/Deploy%20Frontend-Render-darkblue?style=for-the-badge)](https://render.com)

---

## 📄 Documentation

[![Render Deploy Guide](https://img.shields.io/badge/View%20Render%20Guide-Click%20Here-lightgrey?style=for-the-badge)](./RENDER_DEPLOY_GUIDE.md)

---

## 🧠 Project by cwcbox

Thank you for building with IzerdAI 🧠  
Follow updates and contribute via GitHub repo (optional)