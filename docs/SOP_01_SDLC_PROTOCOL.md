# The AI-Human Collaboration Protocol
*Standard Operating Procedure for Full-Stack Development*

To deliver high-value software efficiently, we operate as a unified "Full-Stack Team" following this structured SDLC. This protocol ensures clarity, quality, and maintainability at every stage.

---

## Phase 1: Product Discovery (The "What", "Who" & "Why")
**Role:** Product Owner (PO)
**Goal:** Define valuable outcomes, not just features.
**Output:** `PRODUCT_REQUIREMENTS.md`

1.  **The "Who" (ICP & Persona)**:
    *   **Ideal Customer Profile (ICP)**: Define the specific market segment or company type we are targeting.
    *   **User Persona**: Create a named persona (e.g., "Security Admin Sarah") representing the end-user. *From this point on, we design for this specific person.*
2.  **The "What" (Pain & Solution)**:
    *   **User Pain Point**: What specifically is frustrating or costing the user money?
    *   **The Solution**: High-level description of how we solve this.
3.  **Success Metrics**: 
    *   **Value Proposition**: What are they willing to pay for?
    *   **Measurable Goals**: (e.g., "Reduces session audit time by 90%").
4.  **Scope Definition**: Explicitly list **Non-Goals** to prevent scope creep.
5.  **PRD Consolidation (PO)**:
    *   Synthesize all above points into the formal `PRODUCT_REQUIREMENTS.md`.
    *   Ensure it answers: What, Who, Why, and Success Metrics.
6.  **Business Systems Analysis (BSA)**:
    *   **Role**: Business Systems Analyst (BSA).
    *   **Goal**: Translate the PRD into actionable engineering units.
    *   **Action**: Write **Agile User Stories** (`As a <persona>, I want <feature>, so that <benefit>`).
    *   **Output**: `USER_STORIES.md` (Input for the System Architect).

---

## Phase 2: System Architecture (The "How")
**Role:** System Architect
**Goal:** Blueprint a scalable, secure, and logical structure.
**Output:** `ARCHITECTURE.md` (Diagrams & Schemas)

1.  **Tech Stack Selection**: Choose the right tools for the job (e.g., Next.js vs. Svelte, Supabase vs. AWS).
2.  **Data Modeling**: Design the Database Schema (Tables, Relationships, Types). *Critical Step.*
3.  **Data Flow Design**: Map how data moves (Client ↔ API ↔ DB).
4.  **Security Modeling**: Define Authentication flows, RLS policies, and Access Controls.

---

## Phase 3: Project Management (The "Plan" & "Cost")
**Role:** Project Manager (PM)
**Goal:** Structure delivery, estimate ROI, and manage the Backlog.
**Output:** `PROJECT_INTAKE.md` (Timeline, Budget, Backlog)

1.  **Cost Estimation**:
    *   Review `ARCHITECTURE.md`.
    *   **Identify Costs**: Calculate price of selected services (e.g., "AWS RDS is $40/mo", "Supabase Pro is $25/mo").
    *   **ROI Check**: Does the Solution (Phase 1) justify the Architecture Cost (Phase 2)?
2.  **Timeline & Roadmap**:
    *   Create the roadmap based on the complexity revealed in the Architecture.
3.  **Backlog Creation**:
    *   Initialize the **Product Backlog** (using a tool or `BACKLOG.md`) with the User Stories + Technical Tasks.

---

## Phase 4: Tactical Planning (The "When")
**Role:** Engineering Manager
**Goal:** Break the project into executable, sequential steps.
**Output:** `task.md` (The Master Checklist)

1.  **Task Chunking**: Break backlog items into atomic implementation steps (max 3-5 tool calls per task).
2.  **Dependency Mapping**: Order tasks logically (Database → API → UI).
3.  **Definition of Done**: Define specific exit criteria for each task.

---

## Phase 5: Implementation Loop (The "Build")
**Role:** Senior Software Engineer
**Goal:** Write clean, maintainable, self-documenting code.
**Output:** `implementation_plan.md` & Source Code

*Cycle per Task:*
1.  **Plan**: Draft `implementation_plan.md` for the specific feature.
2.  **Review**: User confirms approach. (Critical Checkpoint)
3.  **Code**: Execute the build.
4.  **Refactor**: Clean code, fix lints, ensuring type safety immediately.

---

## Phase 6: Quality Assurance (The "Test")
**Role:** QA Engineer
**Goal:** Verify correctness, security, and performance.
**Output:** Automated Test Scripts (e.g., `load-test.js`, `security-audit.js`)

1.  **Unit/Integration Testing**: Verify logic and data flow.
2.  **Security Auditing**: actively probe for vulnerabilities (RLS checks, API abuse).
3.  **Performance Testing**: Verify system handles expected load.

---

## Phase 7: Delivery (The "Release")
**Role:** DevOps / SRE
**Goal:** Ensure reliability in production environments.
**Output:** CI/CD Configs, Dockerfiles, Monitoring Dashboards

1.  **Environment Sync**: Verify production secrets and variables.
2.  **Build Verification**: Confirm completely clean production builds.
3.  **Observability**: Setup logging (Grafana/Prometheus) to monitor health.

---

## Phase 8: Postmortem & Iteration (The "Learn")
**Role:** The Whole Team
**Goal:** Continuous Improvement and Knowledge Transfer.
**Output:** `BUILD_POSTMORTEM.md` & `walkthrough.md`

1.  **Documentation**: Update `walkthrough.md` (The User Manual).
2.  **Retrospective**: Update `BUILD_POSTMORTEM.md` with lessons learned, bugs encountered, and ecosystem gotchas.
3.  **Loop**: Return to Phase 1 for the next iteration.
