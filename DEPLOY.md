# 🚀 Neural Sanctum - Deployment Guide

## Quick Start (Local)

```bash
# Option 1: Double-click
index.html

# Option 2: Python Server
python -m http.server 8080

# Option 3: Node.js Server
npx serve .
```

---

## 🌐 Deploy to Web

### GitHub Pages (Free)

1. Create repo on GitHub
2. Push `neural-sanctum/` folder
3. Go to Settings → Pages
4. Select `main` branch → Save

**URL will be:** `https://yourusername.github.io/repo-name/`

---

### Vercel (Recommended)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
cd neural-sanctum
vercel

# Or drag & drop at vercel.com/dashboard
```

---

### Netlify

1. Go to [netlify.com](https://netlify.com)
2. Drag & drop `neural-sanctum/` folder
3. Done!

---

## 📱 Integration with ARCHA

### Connect to ARCHA System

The Neural Sanctum can connect to ARCHA via:

1. **WebSocket** - Real-time communication
2. **REST API** - Fetch/send status
3. **PostMessage** - If embedded in iframe

### Example: Show ARCHA Status

```javascript
// In NeuralSanctum class, add:
async fetchARCHAStatus() {
  const response = await fetch('http://localhost:3001/api/settings');
  const data = await response.json();
  // Display ARCHA status
}
```

---

## 🔒 Security Notes

- ✅ No server-side code (safe)
- ✅ No external dependencies except CDNs
- ⚠️ Don't embed sensitive data in HTML

---

## 📦 Files

```
neural-sanctum/
├── index.html      # Main application
├── README.md       # Documentation
└── deploy.sh      # Deployment script (optional)
```

---

_Deploy anywhere, run everywhere! 🧠_
