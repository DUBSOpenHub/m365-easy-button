# 🔴 M365 Easy Button

```diff
+ ╔══════════════════════════════════════════════════════════════════════════════════════╗
+ ║                                                                                    ║
+ ║  ████████╗██╗  ██╗ █████╗ ████████╗  ██╗    ██╗ █████╗ ███████╗  ███████╗ █████╗ ███████╗██╗   ██╗██╗  ║
+ ║  ╚══██╔══╝██║  ██║██╔══██╗╚══██╔══╝  ██║    ██║██╔══██╗██╔════╝  ██╔════╝██╔══██╗██╔════╝╚██╗ ██╔╝██║  ║
+ ║     ██║   ████████║███████║   ██║     ██║ █╗ ██║███████║███████╗  █████╗  ███████║███████╗ ╚████╔╝ ██║  ║
+ ║     ██║   ██╔══██║██╔══██║   ██║     ██║███╗██║██╔══██║╚════██║  ██╔══╝  ██╔══██║╚════██║  ╚██╔╝  ╚═╝  ║
+ ║     ██║   ██║  ██║██║  ██║   ██║     ╚███╔███╔╝██║  ██║███████║  ███████╗██║  ██║███████║   ██║   ██╗  ║
+ ║     ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝      ╚══╝╚══╝ ╚═╝  ╚═╝╚══════╝  ╚══════╝╚═╝  ╚═╝╚══════╝   ╚═╝   ╚═╝  ║
+ ║                                                                                    ║
+ ║                    Google Workspace → Microsoft 365 · Your translator is ready.    ║
+ ║                                                                                    ║
+ ╚══════════════════════════════════════════════════════════════════════════════════════╝
```

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
[![Security Policy](https://img.shields.io/badge/Security-Policy-brightgreen?logo=github)](SECURITY.md)
![Version: v1.0.0](https://img.shields.io/badge/version-v1.0.0-5E5E5E.svg)
![Platform: Copilot CLI](https://img.shields.io/badge/platform-Copilot%20CLI-232F3E.svg)
![Language: Markdown](https://img.shields.io/badge/written%20in-Markdown-000000.svg)

> ⚡ **Install:**
> ```
> /skills add DUBSOpenHub/m365-easy-button
> ```
> **Then just say: `easy button`**
>
> 🔴 *That was easy.* What Microsoft 365 question can I translate for you?

---

The M365 Easy Button is a GitHub Copilot CLI skill that helps employees transition from Google Workspace to Microsoft 365. It's not generic tech support. It's a translator between two productivity ecosystems that starts every answer from where you already are: Google.

## What It Does

You ask a question about Microsoft 365. The skill answers by first connecting to the Google equivalent you already know, then giving you specific steps in the Microsoft product. Every response follows this structure:

1. **Bridge** — "In Google, you'd do X. In Microsoft, the equivalent is Y."
2. **Steps** — Numbered, specific, with exact menu paths and which app to open.
3. **Next Step** — What to do after, so you're never at a dead end.
4. **Gotcha** — Flags when something works differently than you'd expect.
5. **Power Move** — The shortcut or hidden feature that makes it faster.
6. **If This Fails** — Fallback when org policies or versions get in the way.

## Coverage

### Product Translations (30+ mappings)

| Google | Microsoft |
|---|---|
| Gmail | Outlook |
| Google Chat / Meet | Teams |
| Google Calendar | Outlook Calendar |
| Docs / Sheets / Slides | Word / Excel / PowerPoint |
| Google Drive | OneDrive + SharePoint |
| Apps Script | Power Automate + Office Scripts |
| Looker Studio | Power BI |
| Google Forms | Microsoft Forms |
| Google Tasks / Keep | To Do / OneNote |
| Google Sites | SharePoint |
| Google Admin | M365 Admin Center |
| ...and 20+ more | |

### What's Inside (854 lines)

- **Complete App Router** — "I want to do X" → "Open this app"
- **Mental Model Translations** — Why Microsoft *feels* different (ownership, Teams structure, policy-driven sharing, web vs desktop split)
- **Detailed Behavior Mappings** — Feature-by-feature tables for Email, Calendar, Files, Chat, Docs, Automation, BI, Tasks, Admin
- **Keyboard Shortcuts** — Side-by-side tables: Gmail↔Outlook, Meet↔Teams, Docs↔Word, Sheets↔Excel
- **9 Workflow Translations** — Task-by-task: standup with notes, doc review, form collection, external sharing, onboarding, project tracker, video recording, knowledge base, Apps Script migration
- **First Week Survival Guide** — 10 things to set up on day one
- **Power User Tips** — Quick Steps, Search Folders, Power Automate flows, Teams slash commands, Loop components
- **AI Comparison** — Google Workspace AI vs M365 Copilot features, licensing, and getting started
- **13 Troubleshooting Patterns** — Real-world problems with step-by-step fixes
- **Web Search Integration** — Fetches current Microsoft docs when answers need up-to-date info

## Activation

The skill responds to any of these patterns:

- `m365 [question]`
- `outlook [question]`
- `teams [question]`
- Any mention of Microsoft 365, Outlook, Teams, Word, Excel, PowerPoint, OneDrive, or SharePoint
- `how do I [task] in Microsoft...`
- `what's the Microsoft version of [Google thing]?`
- `I used to [do X] in Google, how do I...`

## Manual Install

If you prefer clipboard install:

```bash
mkdir -p ~/.copilot/skills/m365-easy-button && pbpaste > ~/.copilot/skills/m365-easy-button/SKILL.md
```

Copy the contents of [SKILL.md](SKILL.md) to your clipboard first, then run the command above.

## Persona

The skill acts as the coworker who already made the transition and is happy to show you around. Patient, zero judgment, never condescending. It never says "it's easy" or "just do X." When Microsoft is genuinely more complicated, it says so and shows the fastest path.

## Scope

**In scope:** Day-to-day M365 apps (Outlook, Teams, Word, Excel, PowerPoint, OneDrive, SharePoint, Forms, Power Automate, Power BI, To Do, OneNote, Whiteboard, Planner, Stream, Bookings)

**Out of scope:** Azure, Intune, Entra ID, and enterprise admin infrastructure. The skill refers users to IT for those.

## How It Was Built

The original spec was written by [@DUBSOpenHub](https://github.com/DUBSOpenHub) — the core architecture, persona, answer format (Bridge → Steps → Next Step → Gotcha), the complete App Router table, all behavior mapping tables (Email, Calendar, Files, Chat, Documents), the troubleshooting diagnostic flow, web search integration, and scope boundaries. That spec was then fed into a [Havoc Hackathon](https://github.com/DUBSOpenHub/awesome-copilot) where 14 AI models competed simultaneously to expand and improve it. The top 6 entries were judged across completeness, depth, usability, persona fidelity, and innovation. The final output synthesizes the winning additions on top of the original:

| Contribution | Source |
|---|---|
| Original spec: persona, answer format, app router, behavior mappings, troubleshooting, scope | **@DUBSOpenHub** |
| Expanded structure, AI comparison, additional workflows | Claude Sonnet 4.6 |
| Emotional Calibration, Voice Do/Don't table | Claude Opus 4.5 |
| Mental Model Translations (why M365 feels different) | GPT-5.2 |
| "If This Fails" fallback section | GPT-5.3 Codex |
| Structured hierarchy, tone examples | GPT-5.1 |

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines. The main thing: keep the translator persona consistent and never editorialize about Google vs Microsoft.

## License

[MIT](LICENSE)
