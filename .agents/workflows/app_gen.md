---
description: This workflow is used to generate a new application from scratch based on a user prompt.
---

# App Generation Workflow

This workflow is used to generate a new application from scratch based on a user prompt.

## Steps

### Phase 1: Requirement Analysis (PM)
1. **Refine Prompt**: The PM Agent translates the user's request into a structured `feature_request` artifact in `.agents/artifacts/feature_requests/`.
2. **User Approval**: **GATE**: The user must review and approve the `feature_request` before proceeding.

### Phase 2: Technical Design (Architect & DevOps)
3. **Repository Setup**: The DevOps Agent initializes the repository state (`.gitignore`, `.env.example`, etc.) using the `manage_repository_health` skill.
4. **Architecture Design**: The Architect Agent creates a `tech_spec` in `.agents/artifacts/tech_specs/`.
5. **Establish Standards**: The Architect Agent defines project-specific `style_guides`.
6. **Backlog Creation**: The PM Agent decomposes the approved `tech_spec` into atomic `backlog` items.
7. **User Approval**: **GATE**: The user must review and approve the `tech_spec` and the initial `backlog`.

### Phase 3: Implementation (Coder)
8. **Development**: The Coder Agent implements backlog items using `feature/` branches.
9. **Status Reporting**: The Coder Agent updates task status in `.agents/artifacts/tasks/`.

### Phase 4: Verification & DevOps Review (QA & DevOps)
10. **QA Testing**: The QA Agent verifies the implementation against requirements and specs.
11. **DevOps Audit**: The DevOps Agent reviews the branch for security and repo standards.
12. **Review Summary**: The DevOps Agent presents a summary of changes to the user.
13. **Final Approval**: **GATE**: The user reviews the DevOps summary and performs the final merge into the main branch.

### Phase 5: Remediation
14. **Bug Handling**: If QA or DevOps identifies issues, the **Bug Fix Workflow** is triggered.
