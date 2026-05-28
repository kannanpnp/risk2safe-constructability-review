# 🏗️ Constructability Review Workshop

> A professional, AI-powered Constructability Review tool for oil & gas EPC projects. Zero build tools — one HTML file. Deploy on GitHub Pages in under 5 minutes.

---

## ✨ Features

| Feature | Detail |
|---|---|
| **5-Tab Workflow** | Workshop Setup → Video Review → Checklist → AI Assessment → Report |
| **68-Item Checklist** | 8 engineering categories covering the full constructability spectrum |
| **AI Assessment** | Claude (Anthropic) generates structured Executive Summary, Critical Issues, HSE Observations, and a Readiness Score out of 10 |
| **Video Tracker** | Track, annotate, and link workshop videos directly from your browser |
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

## 🎬 Adding Your Video Links

The **Video Review** tab comes pre-loaded with 5 default entries. To add your actual workshop videos:

1. Open the app and go to the **Video Review** tab
2. Click into the **Video URL / Link** field for each row
3. Paste the URL from your video source (SharePoint, YouTube, Vimeo, OneDrive, etc.)
4. Click **🔗 Open video** to verify the link
5. Watch the video, tick **Mark reviewed**, and add your notes

You can also add additional video rows using the **+ Add Video** button.

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

## 🤖 AI Assessment

The AI Assessment tab sends your checklist data, video notes, and any additional context to the **Claude claude-sonnet-4-20250514 API** and returns a structured report including:

1. Executive Summary
2. Critical Issues
3. Key Risks (schedule, cost, HSE)
4. HSE Observations
5. Prioritised Recommendations
6. Overall Constructability Readiness Score (X/10)

**The API call is made directly from your browser.** This works within the Claude.ai artifact environment automatically. If running as a standalone file or GitHub Pages app, the Anthropic API requires a valid API key passed in the `x-api-key` header. See the note below.

> **Note for standalone / GitHub Pages use:** The Anthropic API requires an API key and does not currently support direct browser calls from arbitrary origins (CORS). For production standalone deployment, route the API call through a small backend proxy (e.g., a Cloudflare Worker or Vercel serverless function) that attaches your `ANTHROPIC_API_KEY`. The rest of the app — checklist, report, CSV/JSON export — works fully offline without any API.

---

## 📄 Exporting Your Work

From the **Report** tab:

| Export | Format | Contents |
|---|---|---|
| 🖨 Print Report | PDF via browser | Full formatted report with all sections |
| ⬇ Download Worksheet | `.json` | Complete session data — re-importable |
| 📊 Download Findings Register | `.csv` | Findings & action items — opens in Excel |

The JSON export includes all project info, participants, video notes, checklist ratings, findings, and AI analysis. Keep it as a record or use it to resume a session.

---

## 🏗️ Project Structure

```
constructability-review/
│
├── index.html          ← Complete app (single file, no dependencies)
└── README.md           ← This file
```

No `node_modules`. No `package.json`. No build step. Just open `index.html`.

---

## 🛠️ Customisation

All data and checklist content lives in the `<script>` block at the bottom of `index.html`.

**To add or edit checklist items**, find the `const CATS = [...]` array and edit the `items` arrays.

**To change the default reviewer name**, find:
```js
reviewer: "Rajagopal Kannan",
designation: "Senior HSE & Emergency Response Professional"
```
and update to your own details.

**To add a new review category**, add an object to `CATS`:
```js
{
  id: "environment",
  label: "Environmental & Regulatory",
  icon: "🌿",
  items: ["Environmental permits obtained", "Waste management plan approved", ...]
}
```

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
