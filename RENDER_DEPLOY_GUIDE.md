# 🧪 IzerdAI Render Deployment Guide

This is a step-by-step guide for deploying IzerdAI chatbot on **Render**.

---

## 🧩 Backend Setup (server/)

- **Service type**: Web Service
- **Environment**: Node
- **Root Directory**: `server`
- **Build Command**: `npm install`
- **Start Command**: `node index.js`

### ✅ Backend Environment Variables

| Key | Description |
|-----|-------------|
| `GEMINI_API_KEY` | Your Google Gemini API key |
| `ADMIN_PASSWORD_HASH` | Bcrypt hash of your admin password |
| `DAILY_TOKEN_LIMIT` | Limit token cost (e.g., 100000) |

---

## 🎨 Frontend Setup (client/)

- **Service type**: Static Site
- **Root Directory**: `client`
- **Build Command**: `npm install && npm run build`
- **Publish Directory**: `dist`

### ✅ Frontend .env

```env
VITE_API_URL=https://your-backend-service.onrender.com/api
```

---

## ✅ Final Steps

1. Upload all code to GitHub
2. Link GitHub repo on Render (both services)
3. Ensure all environment variables are filled
4. Hit "Deploy"
5. Open your chatbot app and test file upload, admin login, chat

---

## 📎 Tips

- Secure backend with:
  - CORS Origin validation
  - JWT for admin auth
- You can extend logging to a database
- Bcrypt password hash can be generated via Node CLI

```bash
node -e "require('bcrypt').hash('yourPassword', 10).then(console.log)"
```