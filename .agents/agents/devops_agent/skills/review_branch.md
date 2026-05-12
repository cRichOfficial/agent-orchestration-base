# Skill: Review Branch

## Description
This skill enables the DevOps Agent to review the Coder's changes and prepare them for user approval.

## Steps
1. Checkout the branch created by the Coder Agent (`feature/*` or `bug/*`).
2. Review the commit messages for quality and clarity.
3. Perform a diff analysis to summarize the changes.
4. Verify that no secrets or environment-specific files were added in the branch.
5. Create a "Review Summary" markdown file and present it to the user.

## Constraints
- Do not perform the merge yourself.
- Focus on security, repo standards, and clarity of the contribution.
