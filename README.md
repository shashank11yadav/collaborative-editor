<div align="center">
  <br />
  <a href="https://youtu.be/y5vE8y_f_OM" target="_blank">
    <img src="https://github.com/user-attachments/assets/eaaeb1f0-22da-46be-9e29-9bef70e0039d" alt="Project Banner" />
  </a>
  <br />
  <div>
    <img src="https://img.shields.io/badge/-Next_JS-black?style=for-the-badge&logoColor=white&logo=nextdotjs&color=61DAFB" alt="Next.js" />
    <img src="https://img.shields.io/badge/-TypeScript-black?style=for-the-badge&logoColor=white&logo=typescript&color=3178C6" alt="TypeScript" />
    <img src="https://img.shields.io/badge/-Tailwind_CSS-black?style=for-the-badge&logoColor=white&logo=tailwindcss&color=06B6D4" alt="Tailwind CSS" />
  </div>

  <h3 align="center">SyncScribe — a Multiplayer Document Platform</h3>

  <p align="center">
    Real‑time collaboration, comments, presence indicators, and rich‑text editing&mdash;all in one lightning‑fast Next.js application.<br/>
    <sup>(Built during <a href="https://www.youtube.com/@javascriptmastery/videos" target="_blank">JavaScript Mastery</a> live‑coding sessions.)</sup>
  </p>
</div>

---

## 📚 Table of Contents
1. [Introduction](#introduction)  
2. [Tech Stack](#tech-stack)  
3. [Features](#features)  
4. [Quick Start](#quick-start)  
5. [Code Snippets](#code-snippets)  
6. [Helpful Links](#helpful-links)  
7. [Credits &amp; License](#credits--license)

## 🤔 Introduction
SyncScribe is a **Google Docs‑style web app** that showcases how to glue together modern web technologies—**Next.js 14** for routing &amp; React Server Components <!-- :contentReference[oaicite:0]{index=0} -->, **TypeScript** for type‑safe development <!-- :contentReference[oaicite:1]{index=1} -->, **Tailwind CSS** for utility‑first styling <!-- :contentReference[oaicite:2]{index=2} -->, and **Liveblocks** to handle real‑time data sync, presence, and comments <!-- :contentReference[oaicite:3]{index=3} -->.  
Under the hood, rich‑text editing is powered by **Lexical**, Meta’s high‑performance editor framework <!-- :contentReference[oaicite:4]{index=4} -->, while UI primitives come from **shadcn/ui** to keep the component markup minimal yet accessible <!-- :contentReference[oaicite:5]{index=5} -->.

## ⚙️ Tech Stack
| Layer | Technology | Why it’s here |
|-------|------------|---------------|
| **Framework** | Next.js (App Router) | Hybrid rendering (SSR + RSC) out of the box <!-- :contentReference[oaicite:6]{index=6} --> |
| **Language** | TypeScript | Safer code &amp; editor IntelliSense <!-- :contentReference[oaicite:7]{index=7} --> |
| **Realtime** | Liveblocks | Presence, optimistic updates, conflict‑free CRDTs <!-- :contentReference[oaicite:8]{index=8} --> |
| **Editor** | Lexical | Composable, accessible rich‑text editing <!-- :contentReference[oaicite:9]{index=9} --> |
| **Styling** | Tailwind CSS + shadcn/ui | Rapid theming plus pre‑styled headless components <!-- :contentReference[oaicite:10]{index=10} --> |
| **Auth** | Clerk &amp;/or NextAuth (GitHub provider) <!-- :contentReference[oaicite:11]{index=11} --><!-- :contentReference[oaicite:12]{index=12} --> | Password‑less, OAuth‑based sign‑in |
| **CI Badges** | Shields.io | Make your README pop while following badge best‑practices <!-- :contentReference[oaicite:13]{index=13} --> |

## 🔋 Features
- **Secure Authentication** – Sign in/out with GitHub via Clerk or NextAuth.  
- **Live Co‑Editing** – Every keystroke syncs to collaborators instantly with conflict‑free merges.  
- **Document CRUD** – Create, search, sort, share, and delete documents, all backed by granular access rules.  
- **Inline &amp; Threaded Comments** – Start discussions at any text range, with inbox notifications.  
- **Presence Indicators** – Avatars and live cursors show who’s online and where they’re editing.  
- **Notifications** – Inbox feed for shares, mentions, and activity.  
- **Responsive Design** – Works great on mobile, tablet, and desktop.  
- **Extensible Architecture** – Strict folder conventions, reusable React hooks, fully typed helpers.

## 🚀 Quick Start
```bash
# 1· Clone
git clone https://github.com/<your‑handle>/syncscribe.git
cd syncscribe

# 2· Install deps
npm install    # or pnpm / yarn

# 3· Environment
cp .env.example .env.local
# → fill in Clerk & Liveblocks keys

# 4· Run dev server
npm run dev
# open http://localhost:3000
