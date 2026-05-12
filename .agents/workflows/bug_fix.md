# Bug Fix Workflow

This workflow is used to resolve issues reported by users or QA.

## Steps

### Phase 1: Triage (QA or User)
1. **Report Bug**: A `bug_report` is created in `.agents/artifacts/bug_reports/`.
2. **Prioritization**: The PM Agent reviews the bug and determines priority.

### Phase 2: Root Cause & Fix (Coder)
3. **Investigation**: The Coder Agent uses the `resolve_bug` skill to perform an RCA.
4. **Branching**: All work is performed on a dedicated `bug/` branch.
5. **Implementation**: The fix is applied according to `style_guides`.

### Phase 3: Verification (QA)
6. **Fix Validation**: The QA Agent verifies the fix using the `verify_feature` skill (refocused on the bug).
7. **Regression Check**: The QA Agent ensures no new issues were introduced.

### Phase 4: DevOps Review & Merge (DevOps)
8. **Audit**: The DevOps Agent reviews the `bug/` branch.
9. **Final Approval**: **GATE**: The user reviews the fix summary and performs the merge.
