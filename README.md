<div align="center">

# 🧠 AI-Powered Workplace Productivity Assistant

**A modern AI workplace assistant for professionals — manage email, meetings, tasks, and your day in one premium interface.**

![Status](https://img.shields.io/badge/status-active-success)
![Stack](https://img.shields.io/badge/stack-TanStack%20Start%20%2B%20React%2019-black)
![Styling](https://img.shields.io/badge/styling-Tailwind%20v4-red)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

</div>

---

## 📖 Overview

This application is a **premium AI productivity platform** designed to help professionals work smarter — not harder. It combines AI-powered email drafting, meeting analysis, task planning, and an insights dashboard into one clean, responsive workspace built around a bold **red · black · white** design system.

> **Why it exists:** Modern professionals juggle messages, meetings, and to-dos across too many tools. This app centralizes them and adds an AI layer that drafts, summarizes, and prioritizes — so you can focus on the work that matters.

---

## ✨ Features

| Module | What it does |
|---|---|
| 📊 **Dashboard** | Quick overview of your day — pending tasks, upcoming meetings, AI suggestions. |
| ✉️ **AI Email Assistant** | Generates professional emails, replies, and follow-ups from a short prompt. |
| 🎙️ **Meeting Intelligence** | Summarizes meetings, extracts action items, and highlights key decisions. |
| ✅ **Smart Tasks** | AI-assisted task breakdown, prioritization, and daily planning. |
| 📅 **Calendar** | Unified view of upcoming events and commitments. |
| 📈 **Insights** | Productivity trends and metrics at a glance. |
| ⚙️ **Settings** | Control AI tone, output preferences, and privacy options. |
| ❓ **Help** | Documentation, tips, and onboarding guidance. |

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Framework** | [TanStack Start](https://tanstack.com/start) (React 19, SSR-ready) |
| **Build Tool** | Vite 7 |
| **Routing** | TanStack Router (file-based) |
| **Data Fetching** | TanStack Query |
| **Styling** | Tailwind CSS v4 + semantic design tokens |
| **UI Components** | shadcn/ui (Radix primitives) |
| **AI Backend** | Lovable AI Gateway via server functions |
| **Language** | TypeScript (strict mode) |
| **Runtime** | Edge-compatible (Cloudflare Workers) |

---

## 🚀 Getting Started

### Prerequisites
- [Bun](https://bun.sh) (recommended) **or** Node.js 20+

### Install & Run

```bash
# 1. Clone the repository
git clone https://github.com/KingCode7-gif/AI-powered-productivity-application.git
cd AI-powered-productivity-application

# 2. Install dependencies
bun install

# 3. Start the dev server
bun run dev
```

Open **[http://localhost:8080](http://localhost:8080)** to view the app.

### Production Build

```bash
bun run build
```

---

## 📁 Project Structure

```
src/
├── routes/                  # 📄 File-based routes (auto-registered)
│   ├── __root.tsx           #    Root layout — shared shell, sidebar, providers
│   ├── index.tsx            #    /          → Dashboard
│   ├── email.tsx            #    /email     → AI Email Assistant
│   ├── meetings.tsx         #    /meetings  → Meeting Intelligence
│   ├── tasks.tsx            #    /tasks     → Smart Task Planner
│   ├── calendar.tsx         #    /calendar  → Calendar view
│   ├── insights.tsx         #    /insights  → Productivity insights
│   ├── settings.tsx         #    /settings  → User preferences
│   └── help.tsx             #    /help      → Help & support
│
├── components/              # 🧩 Reusable UI building blocks
│   ├── app-sidebar.tsx      #    Main navigation sidebar
│   ├── page-header.tsx      #    Shared page header pattern
│   ├── ai-disclaimer.tsx    #    Transparency notice for AI outputs
│   └── ui/                  #    shadcn/ui primitives (buttons, cards, etc.)
│
├── lib/                     # 🔧 Utilities & server logic
│   ├── ai.functions.ts      #    Client-callable AI server functions
│   ├── ai-gateway.server.ts #    Server-only AI gateway integration
│   └── utils.ts             #    Shared helpers (cn, formatters, etc.)
│
├── hooks/                   # 🪝 Custom React hooks
├── styles.css               # 🎨 Global design tokens (red/black/white theme)
├── router.tsx               # 🛣️ Router configuration
└── routeTree.gen.ts         # ⚙️ Auto-generated route tree (do not edit)
```

### How the pieces fit together

1. **Routes** define each page using TanStack Router's file-based system. The Vite plugin auto-generates `routeTree.gen.ts` — never edit it manually.
2. **`__root.tsx`** wraps every page with the sidebar, providers, and the HTML shell.
3. **Server functions** in `src/lib/ai.functions.ts` are typed RPC endpoints. The client calls them; the server runs them against the Lovable AI Gateway.
4. **Design tokens** in `src/styles.css` define the entire red-black-white palette as semantic CSS variables (`--primary`, `--background`, `--sidebar`, etc.). Components reference these tokens — no hardcoded colors.
5. **shadcn/ui components** in `src/components/ui/` are headless, accessible primitives styled with the design tokens.

---

## 🎨 Design System

The app uses a **strict red, black, and white** palette defined as semantic tokens in `src/styles.css`:

| Token | Role |
|---|---|
| `--primary` | Brand red — buttons, highlights, focus rings |
| `--background` | White surface for content areas |
| `--foreground` | Near-black text |
| `--sidebar` | Deep black navigation rail |
| `--muted` | Soft off-white for secondary surfaces |
| `--border` | Subtle neutral dividers |

All components consume these tokens — guaranteeing consistent theming and seamless dark mode.

---

## 🔒 Privacy & AI Transparency

- 🏷️ AI-generated content is **clearly labeled** with disclaimers.
- 👤 **You control every output** — review, edit, or discard before sending.
- 🛡️ No sensitive data is stored or shared without consent.
- ⚠️ **Always review AI suggestions** before making business decisions or sending professional communications.

---

## 📜 License

Released under the **MIT License** — free to use, modify, and distribute.

---

<div align="center">

Built with ❤️ using [**Lovable**](https://lovable.dev) — the AI-powered app builder.

</div>
