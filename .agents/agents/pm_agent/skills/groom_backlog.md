# Skill: Groom Backlog

## Description
This skill enables the PM Agent to break down an approved technical specification into actionable backlog items.

## Steps
1. Verify that the corresponding `feature_request` has been approved by the user.
2. Analyze the `tech_spec` to identify atomic units of work.
3. Create individual markdown files for each task in `.agents/artifacts/backlog/`.
4. Each backlog item should include:
    - Title and ID
    - Description
    - Acceptance Criteria
    - Dependencies

## Constraints
- Output must be Markdown only.
- Only create items for approved features.
