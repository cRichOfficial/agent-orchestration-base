# Skill: Create Bug Report

## Description
This skill enables the QA Agent to formalize a defect or missing requirement into a structured bug report.

## Steps
1. **Isolate Issue**: Confirm the defect is reproducible and not a configuration error.
2. **Assign Severity**:
    - **Blocker**: App is unusable.
    - **High**: Major feature broken.
    - **Medium**: Minor feature broken or significant UI issue.
    - **Low**: Trivial UI issue or suggestion.
3. **Draft Report**: Create `bug_[id]_[summary].md` in `.agents/artifacts/bug_reports/` with the following:
    - **Summary**: Concise description of the issue.
    - **Reproduction Steps**: Numbered list to reliably trigger the bug.
    - **Expected Behavior**: What should have happened according to requirements.
    - **Actual Behavior**: What actually happened (include logs/errors).
    - **Environment**: OS, browser, version, branch, etc.
4. **Linkage**: Reference the failing `feature_request` or `tech_spec` section.

## Constraints
- **Clarity**: Use precise technical language.
- **Evidence**: Attach relevant log snippets or terminal output within the markdown file.
