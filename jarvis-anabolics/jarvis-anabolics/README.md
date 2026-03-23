# Jarvis Anabolics — Deployment Guide

## Deploy to Vercel in 5 steps

### 1. Install dependencies locally (optional, just to test)
```
npm install
npm run dev
```

### 2. Push to GitHub
- Create a new repo on github.com
- Upload all these files to it

### 3. Connect to Vercel
- Go to vercel.com → New Project
- Import your GitHub repo
- Vercel will auto-detect Vite

### 4. Add your API key (IMPORTANT)
- In Vercel dashboard → Your Project → Settings → Environment Variables
- Add: `ANTHROPIC_API_KEY` = your key from console.anthropic.com

### 5. Deploy
- Click Deploy — done!

## File structure
```
jarvis-anabolics/
├── api/
│   └── claude.js        ← Secure API proxy (hides your key)
├── src/
│   ├── main.jsx         ← React entry point
│   └── App.jsx          ← Main app
├── index.html
├── package.json
├── vite.config.js
└── vercel.json
```

## Get your Anthropic API key
1. Go to console.anthropic.com
2. Sign up / log in
3. API Keys → Create Key
4. Copy it into Vercel environment variables
