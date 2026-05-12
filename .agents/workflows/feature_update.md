---
description: This workflow is used to add new features or modify existing ones in an established application.
---

# Feature Update Workflow

This workflow is used to add new features or modify existing ones in an established application.

## Steps

### Phase 1: Impact Analysis (PM & Architect)
1. **Analyze Request**: The PM Agent evaluates the feature update and updates the `feature_request` artifact.
2. **Technical Delta**: The Architect Agent identifies necessary changes to the `tech_spec`.
3. **User Approval**: **GATE**: The user approves the updated requirements and technical plan.

### Phase 2: Planning (PM)
4. **Grooming**: The PM Agent creates new `backlog` items for the feature update.

### Phase 3: Execution (Coder)
5. **Implementation**: The Coder Agent implements changes on a new `feature/` branch.
6. **Style Compliance**: Ensure changes adhere to existing `style_guides`.

### Phase 4: Verification & Review (QA & DevOps)
7. **Regression Testing**: The QA Agent ensures existing features are not broken.
8. **Feature Validation**: The QA Agent validates the new feature criteria.
9. **DevOps Audit**: The DevOps Agent reviews the branch for repo standards and security.
10. **Final Approval**: **GATE**: The user reviews the summary and performs the merge.
