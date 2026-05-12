# Skill: Resolve Bug

## Description
This skill enables the Coder Agent to diagnose and fix issues reported in a bug report.

## Steps
1. **Analyze Bug Report**: Thoroughly read the `bug_report` in `.agents/artifacts/bug_reports/`.
2. **Setup Environment**: Checkout a new `bug/[bug-id]` branch.
3. **Reproduce & Investigate**: 
    - Reproduce the bug using the steps provided.
    - Identify the root cause by examining logs, state, and code logic.
4. **Root Cause Analysis (RCA)**: Document the root cause in the `tasks/` entry for this bug before applying the fix.
5. **Implement Fix**: 
    - Apply the fix within the `/src/` directory.
    - Adhere to the `style_guide` and `tech_spec`.
6. **Verify Fix**: 
    - Confirm the bug is no longer reproducible.
    - Ensure no new issues were introduced.
7. **Document & Hand-off**: 
    - Commit with a message like `fix: resolve [bug-id] - [summary]`.
    - Update the `bug_report` in `.agents/artifacts/bug_reports/` to `Fixed` and link to the fix details.

## Constraints
- **Scope**: Only fix the reported bug; do not refactor unrelated code.
- **Approval**: If the fix requires architectural changes, consult the Architect Agent first.
