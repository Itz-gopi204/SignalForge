# 🖥️ SignalForge Frontend (`apps/frontend`)

The client interface for **SignalForge**, built with **React 19**, **Tailwind CSS**, **Lucide Icons**, and custom interactive components powered by the **Bun** runtime.

---

## ⚡ Features

* **Recruiter & Org Management Dashboard**: 2-level expandable hierarchy (`Organization` → `Teams`) with candidate pipeline monitoring, team-scoped job postings, and bulk interview invitation links.
* **Live Interactive Voice Room**: Full-duplex conversational UI displaying real-time speech-to-text transcriptions and live session countdown timers.
* **Canvas VoiceOrb Visualizer**: Dynamic reactive audio orb that pulsates with user mic input and incoming synthetic assistant audio.
* **Client-Side PDF Resume Ingestion**: In-browser document text extraction using **PDF.js**, ensuring fast parsing without storing sensitive documents.
* **Automated Candidate Scorecards**: Structured performance rubric cards showing categorized ratings (out of 10), technical strengths, and improvement suggestions.
* **Built-in APITester Utility**: Standalone diagnostic interface (`APITester.tsx`) to verify WebSocket connectivity, speech synthesis, and backend status.

---

## 🛠️ Tech Stack

* **Framework**: React 19
* **Styling**: Tailwind CSS, CSS Animations, Radix UI Primitives
* **Icons**: Lucide React
* **Runtime / Bundler**: Bun (`build.ts` custom bundler)
* **Audio**: Web Audio API (`AudioContext`, `AnalyserNode`)

---

## 🚀 Running Locally

From either the repository root or this package directory:

```bash
# Within apps/frontend
bun install
bun run dev      # Runs dev server on http://localhost:3000
```

To create an optimized production bundle:

```bash
bun run build    # Bundles client assets to apps/frontend/dist/
```
