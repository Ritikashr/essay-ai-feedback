# EssayAI — AI-Powered Essay Feedback Tool

A live web app that uses Claude AI to give instant, detailed feedback on essays — analyzing clarity, structure, grammar, and tone.

**🔗 Live Demo:** https://Ritikashr.github.io/essay-ai-feedback/

---

## Features

- **AI-powered analysis** — Powered by Claude (Anthropic) via the Messages API
- **4 scored dimensions** — Clarity, Structure, Grammar, Tone (scored 0–100)
- **Actionable feedback** — Specific strengths and improvement suggestions
- **Configurable settings** — Choose essay type (academic, persuasive, narrative, technical) and target audience
- **Example essays** — 3 built-in examples to try instantly
- **GitHub Pages** — No backend needed; runs entirely in the browser

---

## How It Works

1. Paste or type your essay into the editor
2. Choose the essay type and audience from the settings panel
3. Click **Analyze Essay**
4. The app calls the Anthropic Claude API and returns:
   - An overall score (0–100)
   - Individual scores for Clarity, Structure, Grammar, and Tone
   - 3 strengths with explanations
   - 3 improvement suggestions with explanations
   - Key themes detected in the essay

---

## Setup

### 1. Fork or clone this repo

```bash
git clone https://github.com/Ritikashr/essay-ai-feedback.git
cd essay-ai-feedback
```

### 2. Add your Anthropic API key

Open `index.html` and find the `fetch` call to the Anthropic API. Add your API key:

```javascript
headers: {
  'Content-Type': 'application/json',
  'x-api-key': 'YOUR_API_KEY_HERE',
  'anthropic-version': '2023-06-01',
  'anthropic-dangerous-direct-browser-access': 'true'
}
```

> ⚠️ **Note:** For production use, route API calls through a backend to protect your API key.

### 3. Deploy to GitHub Pages

Push to `main` — GitHub Actions automatically deploys to GitHub Pages.

Or enable manually: **Settings → Pages → Source → GitHub Actions**

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, Vanilla JavaScript |
| AI | Anthropic Claude API (`claude-sonnet-4-20250514`) |
| Hosting | GitHub Pages |
| CI/CD | GitHub Actions |

---

## Project Structure

```
essay-ai-feedback/
├── index.html               # Full app (single-file)
├── README.md                # This file
└── .github/
    └── workflows/
        └── deploy.yml       # GitHub Pages deploy workflow
```

---

## Built By

**Ritika Shrivastava** — Technical Writer & Documentation Engineer

- [LinkedIn](https://linkedin.com/in/ritika-shrivastava-819707240)
- [GitHub](https://github.com/Ritikashr)
