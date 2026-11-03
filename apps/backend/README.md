# ⚙️ SignalForge Backend (`apps/backend`)

The core server and voice-pipeline orchestration service for **SignalForge**, built with **Bun**, **Express**, **Prisma ORM**, and integrations with **Groq** and **Deepgram**.

---

## ⚡ Features

* **Dual-Engine Voice Pipeline**:
  * **Aura TTS & Nova-2 STT**: Real-time bi-directional audio streaming via WebSockets with natural voice pacing (`0.92x`).
  * **OpenAI Realtime WebRTC**: Fallback low-latency WebRTC streaming interface.
* **LLM Reasoning & Evaluation**: Automated technical interview prompts and rubric generation powered by **Groq (Llama 3.1 70B / 8B)**.
* **2-Level Organization & Team Hierarchy**: Multi-tenant relational data models (`Organization` → `Teams` → `Users` / `Jobs` / `Interviews`).
* **Role-Based Access Control (RBAC)**: JWT authentication and middleware guards protecting `ADMIN`, `RECRUITER`, and `INTERVIEWER` actions.
* **Database & Migrations**: Automated PostgreSQL schema migrations and client generation via **Prisma ORM**.
* **GitHub Scraper**: Public profile context ingestion to tailor interview questions to candidate open-source work.

---

## 🛠️ Tech Stack

* **Runtime**: Bun (v1.3+)
* **Server Framework**: Express + native Bun WebSockets
* **Database**: PostgreSQL (Neon Serverless)
* **ORM**: Prisma ORM
* **AI Providers**: Groq Cloud (Llama 3.1), Deepgram (Aura TTS + Nova-2 STT)
* **Validation**: Zod

---

## 🚀 Running Locally

```bash
# Within apps/backend
bun install

# Database sync
bunx prisma db push
bunx prisma generate

# Start backend server on http://localhost:3001
bun run index.ts
```

For environment variables, copy `apps/backend/.env.example` to `apps/backend/.env` and supply your database connection and API keys.
