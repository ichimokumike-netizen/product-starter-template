# AI Agent Directives & Standard Operating Procedures
*The "Constitution" for AI Collaborators in this Repository.*

If you are an AI (LLM) working in this repository, you **MUST** adhere to these directives.

---

## 1. The Prime Directive: "Full-Stack Team" Protocol
We operate under the **7-Phase SDLC** defined in `docs/SOP_01_SDLC_PROTOCOL.md`.
*   **Do not** simply start coding upon request.
*   **Identify** which phase we are in (Discovery, Architecture, Planning, Build, Test).
*   **Adopt** the appropriate "Hat" (Product Owner, Architect, Engineer).

## 2. CI/CD & Branching Strategy
We follow **GitHub Flow** (Trunk-Based Development) as defined in `docs/SOP_02_CI_CD_STRATEGY.md`.
*   **Main Branch:** `main` (Production). Never commit directly.
*   **Feature Branches:** `feature/your-task-name`.
*   **Gates:** You must verify that `npm run test` and security audits pass before requesting a merge.

## 3. File Structure Standards
*   `docs/`: All SOPs and Strategy documents live here.
*   `.github/workflows/`: CI automation.
*   `artifacts/`: Temporary output for user review (if specific to a task).
*   `scripts/`: Automation scripts (e.g., `security-audit.js`).

## 4. Interaction Style
*   **Be Proactive:** If you see a missing test or a security hole, propose a plan to fix it.
*   **Documentation First:** Update the `README.md` or `docs/` if you change how the system works.
*   **No Fluff:** Keep artifact files clean (Markdown only, no emojis unless requested).

## 5. Security First
*   **Assume Zero Trust.**
*   Always verify Row Level Security (RLS) if touching a database.
6. The Self-Annealing Protocol (Antifragility)
*   **Improve the Process:** If you find a friction point in these SOPs (e.g., a test step is redundant), you are **REQUIRED** to propose a change to the `docs/` files.
*   **Update the Knowledge Base:** When you solve a novel problem, log the solution in `docs/KNOWLEDGE_BASE.md` (create it if missing) so future agents don't repeat the mistake.
*   **Refactor relentlessly:** If you see "fragile" code, fix it. Do not leave broken windows.
*   **Goal:** This repository should become *easier* to work in with every commit.
