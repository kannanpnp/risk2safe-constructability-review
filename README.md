# 🏗️ Risk2Safe Constructability Review

**Transforming construction risk into safety — one guideword at a time.**

> A professional, AI-powered Constructability Review tool built for oil & gas EPC projects. Based on real workshop practice with node-based guideword analysis, structured findings register, recommendations tracking, and multi-sheet Excel export.

---

## ✨ Features

| Feature | Detail |
|---|---|
| **5-Tab Workflow** | Workshop Setup → Review Checklist → Recommendations Register → AI Assessment → Report & Export |
| **19 Workshop Guidewords** | Extracted from real constructability review sessions — all prompts & guidewords included |
| **Node-Based Review** | Define multiple construction nodes/packages; each reviewed independently against all 19 guidewords |
| **42 Review Prompts** | Covering Sequence, Security, Site Infrastructure, Welfare, Layout, Access, Schedule, Equipment, Utilities, Risks, Maintenance, Climate, Interfaces, Electrical, Instrument, and more |
| **Structured Reference Numbering** | Every finding gets a unique ref (e.g. `N1-01.3`); every recommendation gets `REC-001`, `REC-002`... |
| **Recommendations Register** | Separate tab with status tracking (Open / In Progress / Closed), responsibility, target date |
| **AI Assessment (GPT-4o)** | Analyses all nodes and findings; references finding codes in recommendations |
| **Manual Assessment** | Enter your own expert notes alongside (or instead of) AI output |
| **Excel Export (6 sheets)** | Cover · CR Findings · Recommendations Register · Node Summary · Workshop Questionnaire · Participants |
| **Printable Report** | Full formatted report matching workshop output format |
| **JSON Session Save** | Download full session data; use as a backup or audit record |
| **AI Node Structure Suggestion** | GPT-4o analyses your project scope and suggests an optimal node hierarchy (pre-commissioning, commissioning, startup as separate or sub-nodes) |
| **74-Question Workshop Questionnaire** | Pre-built across 9 phases: Project Setup, Design, HSE, Brownfield/SIMOPS, Construction, Pre-commissioning, Commissioning, Regulatory, Interfaces |
| **AI Project-Specific Questions** | Generates additional questions tailored to your specific project, location, and scope |
| **Manual Obs + Rec Additions** | Add unlimited manual observations and recommendations alongside AI suggestions per prompt |
| **Dark Mode** | Auto-follows OS preference |

---

## 🗂️ The 19 Guidewords

| # | Guideword | Prompts |
|---|---|---|
| 1 | Sequence | Construction/Design Sequence, Shutdown Requirements, SIMOPs, Commissioning/Handover, Demolition |
| 2 | Security | Access control, Fencing/personnel management |
| 3 | Existing Site Infrastructure | Holes/pits/foundations, Overhead lines/cables, Water table/flooding, Confined space |
| 4 | Welfare Arrangements | Hygiene, food, shared facilities, site establishment |
| 5 | Layout / Laydown | Contractor compound/carpark/laydown, Materials storage/barricading |
| 6 | Access / Egress | On/off site routes, Authority approvals, Vehicular/emergency/crane routes |
| 7 | Construction Schedule | Schedule review |
| 8 | Mobilisation / Demobilisation | Journey Management Plans, Long lead items |
| 9 | Equipment | Equipment requirements, Crane/lifting, Specialist equipment |
| 10 | Transiting Services / Utilities | Temporary power, lighting, drainage, water, telecoms |
| 11 | Risks to/from Adjacent Operations | Traffic, vehicle movements, lifting, road safety |
| 12 | Maintenance | Provision for maintenance areas |
| 13 | Climate / Environmental Risk | Flooding, wind, earthquake, humidity, nearby habitation |
| 14 | Complexity / Modularity | Construction simplification, cost saving innovations |
| 15 | Interfaces | NOC integration, systems, permits, contracts |
| 16 | Any Other Business | Project-specific items (e.g. LHD test push buttons) |
| 17 | Electrical System | Cable Route, Earthing & Bonding, Testing, Termination |
| 18 | Instrument System | Cable Route, Bonding, Testing, Termination, Junction Boxes, Well Head Control Panel |
| 19 | Project Interfaces | Potential other project interfaces |

---

## 🔢 Reference Numbering System

Every finding and recommendation gets a unique, traceable reference number:

```
Finding Reference:      N1-01.3
                        │  │  └─ Prompt number (3rd prompt under this guideword)
                        │  └──── Guideword number (01 = Sequence)
                        └─────── Node code (N1 = your first node)

Recommendation Number:  REC-007
                        └─────── Sequential global counter (padded to 3 digits)

Standalone Addition:    ADD-001
                        └─────── For recommendations not linked to a specific finding
```

This makes future follow-up checks easy — reference the code in emails, meetings, and action trackers.

---

## 📊 Excel Output — 5 Sheets

| Sheet | Contents |
|---|---|
| **Cover** | Project info, node list, generation date |
| **Constructability Review** | All 19 guidewords × all nodes — Ref No, Node, GW, Prompt, Observations (yellow), Recommendations, Responsibility, Remarks |
| **Recommendations Register** | All REC-### numbers with status, responsibility, target date, remarks |
| **Node Summary** | Per-node stats: total prompts, with observations, with recommendations, % filled |
| **Participants** | Workshop attendee list |

---

## 🚀 Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `risk2safe-constructability-review`)
2. Upload `index.html` and `README.md` to the root
3. Go to **Settings → Pages → Branch: main → / (root) → Save**
4. App live at: `https://YOUR-USERNAME.github.io/risk2safe-constructability-review/`

> **Important:** Always access via `http://` or `https://` — not as a local `file://` URL (AI features require a web server). For local testing use VS Code Live Server or `python -m http.server 8080`.

---

## 🤖 AI Assessment Setup

1. Get your OpenAI API key at **[platform.openai.com/api-keys](https://platform.openai.com/api-keys)**
2. Open the app → **AI Assessment** tab → paste key in the 🔑 field
3. Fill in your checklist findings first (the AI analyses all nodes together)
4. Click **✦ Generate AI Assessment**

The AI references your finding codes (e.g. N1-01.2) in its recommendations, making it easy to cross-reference against the register.

---

## 📁 Project Structure

```
risk2safe-constructability-review/
├── index.html      ← Complete app (single file, no dependencies except SheetJS CDN)
└── README.md       ← This file
```

---

## 👤 Author

**Rajagopal Kannan** — Senior HSE & Emergency Response Professional  
CSP · CIH · CFPS · CPSP · ICS-400 · ISO 45001 Lead Auditor · FIFireE · ADIPEC SPE-177740

---

## 📜 Licence

MIT — free to use, modify, and distribute.
