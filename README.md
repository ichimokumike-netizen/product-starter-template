# Product Starter Template
*The Foundation for High-Velocity, Secure Web Applications.*

This repository serves as the **Golden Template** for all new products in our organization. It comes pre-loaded with our standard operating procedures, CI/CD configurations, and AI collaboration directives.

> **💡 Philosophy: Self-Annealing**
> This repository is design to be **Antifragile**. Every AI agent and Human Engineer is expected to improve the processes (`docs/`) and code structure with every interaction. If you find a better way, update the Standard Operating Procedure.

## 🚀 How to Start a New Product using this Template

1.  **Clone/Use Template:**
    *   Click "Use this template" (if on GitHub) or copy this directory to `new-product-name`.
2.  **Initialize:**
    *   Run `npm create next-app .` (if building a Next.js app) or your preferred framework init command.
    *   Ensure you do *not* overwrite the `docs/` or `.github/` folders.
3.  **Read the Directives:**
    *   Open `docs/SOP_00_AI_DIRECTIVES.md`. This tells you (and your AI pair programmer) how to work.

## 📂 Repository Structure

*   `.github/workflows/`: Standard CI/CD pipelines (GitHub Flow).
*   `docs/`: Standard Operating Procedures (SOPs).
    *   `SOP_00_AI_DIRECTIVES.md`: Rules of Engagement.
    *   `SOP_01_SDLC_PROTOCOL.md`: The 7-Phase Cycle.
    *   `SOP_02_CI_CD_STRATEGY.md`: Branching & Release Strategy.
    *   `SOP_03_CLOUD_DEV_SETUP.md`: Codespaces & Docker Guide.

## 🤖 For AI Agents
If you are an AI assisting on this repo, **read `docs/SOP_00_AI_DIRECTIVES.md` immediately**.

---

## 📋 Appendix: README Template for New Apps
*Copy the markup below and overwrite this `README.md` when you initialize your new product.*

```markdown
# [Product Name]
*[One Line Value Proposition]*

## 🚀 Overview
[Product Name] is a [Type of App] that helps [Target User] solve [Pain Point] by [Solution].

## 🛠 Tech Stack
*   **Framework:** Next.js 16 (App Router)
*   **Database:** Supabase (PostgreSQL)
*   **Styling:** Tailwind CSS v3
*   **Auth:** Supabase Auth (SSR)

## ⚡ Getting Started

### 1. Environment Setup
Copy the example env file and fill in your Supabase credentials:
bash
cp .env.example .env.local

### 2. Install Dependencies
bash
npm install

### 3. Run Development Server
bash
npm run dev
# Server running at http://localhost:3000

## 🧪 Testing
*   **Unit Tests:** `npm run test`
*   **Security Audit:** `node scripts/security-audit.js`

## 📘 Documentation
This project follows strict SDLC protocols. See `docs/` for details:
*   [Product Requirements](docs/PRODUCT_REQUIREMENTS.md)
*   [Architecture](docs/ARCHITECTURE.md)
*   [SDLC Protocol](docs/SOP_01_SDLC_PROTOCOL.md)
```
