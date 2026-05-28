# 🏗️ Constructability Review Workshop

> A professional, AI-powered Constructability Review tool for oil & gas EPC projects. Zero build tools — one HTML file. Deploy on GitHub Pages in under 5 minutes.

---

## ✨ Features

| Feature | Detail |
|---|---|
| **4-Tab Workflow** | Workshop Setup → Review Checklist → AI Assessment → Report |
| **68-Item Checklist** | 8 engineering categories covering the full constructability spectrum |
| **AI Assessment** | Claude (Anthropic) generates structured Executive Summary, Critical Issues, HSE Observations, and a Readiness Score out of 10 |
| **Printable Report** | Professional formatted report — print to PDF from any browser |
| **Download Worksheet** | Export full session data as JSON |
| **Download Findings Register** | Export findings & action items as CSV (opens in Excel) |
| **Dark Mode** | Automatically follows your OS preference |
| **No Build Tools** | Pure HTML/CSS/JS — works by opening a file or deploying to GitHub Pages |

---

## 🚀 Deploy to GitHub Pages (5 minutes)

### Option A — Use this repository directly

1. **Fork this repository** (click Fork at top-right of GitHub)
2. Go to your fork → **Settings** → **Pages**
3. Under *Branch*, select `main` and folder `/` (root)
4. Click **Save**
5. Your app will be live at:
   ```
   https://YOUR-USERNAME.github.io/constructability-review/
   ```

### Option B — Create a new repository

1. Create a new repository on GitHub (name it e.g. `constructability-review`)
2. Upload only the `index.html` file to the root
3. Go to **Settings** → **Pages** → select `main` branch → `/` (root) → **Save**
4. Done ✅

> **Tip:** GitHub Pages may take 1–2 minutes to publish after first setup. Subsequent changes go live within seconds.

---

## 📋 Review Checklist — 8 Categories

| # | Category | Items |
|---|---|---|
| 1 | 🔷 Design & Engineering | 11 |
| 2 | 📦 Materials & Procurement | 8 |
| 3 | 🔧 Construction Methods & Sequencing | 10 |
| 4 | 📍 Site Access & Logistics | 7 |
| 5 | 🛡️ HSE & Safety in Design | 9 |
| 6 | 📅 Schedule & Cost | 8 |
| 7 | 🔁 Interfaces & Coordination | 7 |
| 8 | ⚙️ Commissioning & Startup | 8 |
| | **Total** | **68** |

Each item supports:
- One-click rating: **Satisfactory / Needs Improvement / Not Acceptable / N/A**
- Free-text finding / observation
- Recommended action
- Responsible party
- Due date
- Priority (Critical / High / Medium / Low)

---

## 🤖 AI Assessment — Setup (Required)

The AI Assessment tab uses **OpenAI GPT-4o** and requires your OpenAI API key.

### Step 1 — Get your OpenAI API key
1. Go to **[platform.openai.com/api-keys](https://platform.openai.com/api-keys)** and sign in
2. Click **Create new secret key** → give it a name → **Create**
3. Copy the key immediately — it starts with `sk-` or `sk-proj-`

> **Free credits:** New OpenAI accounts receive free credits that are sufficient for many workshop sessions.

### Step 2 — Enter the key in the app
1. Open the app → click the **AI Assessment** tab
2. Paste your key into the **🔑 OpenAI API Key** field
3. The status shows **✓ Key format looks valid** when correct
4. Select your preferred model from the dropdown (GPT-4o recommended)
5. Click **✦ Generate AI Assessment**

### Model options

| Model | Speed | Cost | Best for |
|---|---|---|---|
| **GPT-4o** | Fast | Moderate | Full constructability reviews — recommended |
| **GPT-4o Mini** | Very fast | Low | Quick checks, frequent iterations |
| **GPT-4 Turbo** | Moderate | Higher | Complex multi-category reports |

### What the AI sends to OpenAI
Your checklist ratings, findings text, video notes, and project metadata — no files, no personal data. Your API key lives only in your browser tab and is cleared when you close the page.

### Common errors and fixes

| Error | Cause | Fix |
|---|---|---|
| `Failed to fetch` / Network error | Opening `index.html` as `file://` URL | Use GitHub Pages, or run via Live Server / `python -m http.server` |
| `401 Authentication failed` | Invalid or expired API key | Re-copy the key from platform.openai.com/api-keys |
| `403 Access denied` | Key has no permission for selected model | Switch to GPT-4o Mini, or check account permissions |
| `429 Rate limit / quota exceeded` | Too many requests or free tier exhausted | Wait 60 seconds, or add credits at platform.openai.com/usage |
| `500 / 503 Server error` | OpenAI outage | Check status.openai.com, wait and retry |
| Key format warning | Key doesn't start with `sk-` | Verify you copied the complete key |

> **Important:** Always access the app via `http://` or `https://` — not as a local `file://` URL. GitHub Pages handles this automatically. For local testing, use VS Code Live Server (right-click `index.html` → Open with Live Server) or run `python -m http.server 8080` in the project folder and open `http://localhost:8080`.

---

## 🧑‍💻 Technology

- **Pure HTML5 / CSS3 / Vanilla JavaScript** — no frameworks, no build tools
- **Claude claude-sonnet-4-20250514 API** (Anthropic) for AI assessment
- **CSS Custom Properties** for theming (auto light/dark mode)
- **SVG** for the progress ring in the header
- **Browser APIs** — `Blob`, `URL.createObjectURL` for file downloads; `navigator.clipboard` for copy

---

## 🔒 Data Privacy

All checklist data, project information, and findings are stored **only in your browser's memory** for the duration of the session. Nothing is sent to any server except when you click *Generate AI Assessment* (which sends anonymised checklist summary data to the Anthropic API). Closing or refreshing the tab clears all data — use the JSON export to save your work.

---

## 📖 Background

Built for Constructability Review Workshops in the **oil & gas EPC sector**, aligned with:
- CII (Construction Industry Institute) Constructability principles
- IPA (Independent Project Analysis) best practices  
- PDRI (Project Definition Rating Index) framework concepts
- SPE / ADIPEC constructability guidance for upstream & midstream facilities

---

## 👤 Author

**Rajagopal Kannan**  
Senior HSE & Emergency Response Professional  
CSP · CIH · CFPS · CPSP · ICS-400 · ISO 45001 Lead Auditor · FIFireE  
ADIPEC Publication: SPE-177740

---

## 📜 Licence

MIT Licence — free to use, modify, and distribute. Attribution appreciated.

```
MIT License
Copyright (c) 2025 Rajagopal Kannan
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction.
```
