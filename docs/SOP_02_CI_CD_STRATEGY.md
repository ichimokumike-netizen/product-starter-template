# CI/CD Pipeline Strategy: GitHub Flow
*A streamlined, professional trunk-based workflow for high-velocity delivery.*

We are adopting **GitHub Flow**, the industry standard for modern web applications. This model optimizes for speed, continuous feedback, and rapid recovery.

---

## 1. The Branching Model
Instead of complex hierarchies, we use **one long-lived branch**.

| Branch | detailed Protection | Purpose |
| :--- | :--- | :--- |
| **`main`** | **Protected** | The **Production** codebase. Always deployable. Direct commits are blocked. |
| **`feature/*`** | Temporary | Short-lived workspace for a specific task (e.g., `feature/login-ui`). |

---

## 2. The Promotion Workflow (The "Loop")

### Step 1: Development
*   **Action**: Create `feature/my-task` from `main`.
*   **Env**: GitHub Codespaces (or Local).
*   **Goal**: Complete the task.

### Step 2: Investigation (The "CI Gate")
*   **Action**: Open Pull Request (PR) -> `main`.
*   **Automated Checks (GitHub Actions)**:
    1.  **Unit Tests**: `npm run test` (Verify logic).
    2.  **Security Audit**: `node scripts/security-audit.js` (Verify isolation/RLS).
    3.  **Lint/Build**: Verify no syntax errors.
*   **Preview Environment**:
    *   Vercel automatically deploys this branch to `my-task.vercel.app`.
    *   **Manual QA**: We verify the extensive functionality on this live preview URL.

### Step 3: Production (The "Release")
*   **Action**: Merge PR to `main`.
*   **Effect**:
    *   Vercel detects the push to `main`.
    *   Automatically builds and promotes to **Production** (`session-security.app`).
    *   No manual "Promotion" steps required.

---

## 3. GitHub Actions Implementation Plan

We will create a single robust checking workflow:

### `.github/workflows/ci-checks.yml`
**Triggers**:
*   Pull Request to `main`.
*   Push to `main`.

**Jobs**:
1.  **Test**: Runs `npm run dev` (health check) + `security-audit.js`.
2.  **Lint**: Runs `npm run lint`.

*Note: Deployment is handled natively by the Vercel Integration, so we usually do not need a `.github/workflows/deploy.yml` unless we migrate off Vercel.*
