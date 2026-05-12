# Skill: Update Task Status

## Description
This skill enables the Coder Agent to provide transparent updates on task progress.

## Steps
1. Identify the task file in `.agents/artifacts/tasks/`.
2. Update the status field (e.g., `In Progress`, `Blocked`, `Completed`).
3. Add a timestamp and a brief log of work performed or reasons for being blocked.
4. Notify other agents (if the workflow supports it) of the status change.

## Constraints
- Ensure the task file remains well-formatted markdown.
