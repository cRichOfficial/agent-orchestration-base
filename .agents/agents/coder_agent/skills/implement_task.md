# Skill: Implement Task

## Description
This skill enables the Coder Agent to take a backlog item and transform it into functional source code.

## Steps
1. **Analyze Input**: Read the assigned task in `.agents/artifacts/backlog/` and the associated `tech_spec` in `.agents/artifacts/tech_specs/`.
2. **Setup Workspace**: 
    - Determine if the task is a `feature` or a `bug`.
    - Create a new Git branch: `feature/[task-id]` or `bug/[task-id]`.
    - Move/Copy the backlog file to `.agents/artifacts/tasks/` and set status to `In Progress`.
3. **Review Standards**: Read the relevant style guides in `.agents/artifacts/style_guides/`.
4. **Implementation**: 
    - Write code strictly within the `/src/` directory.
    - Follow the naming conventions and architectural patterns defined in the `tech_spec`.
    - Ensure code is well-commented and self-documenting.
5. **Commit Progress**: 
    - Commit changes using semantic messages (e.g., `feat(api): implement user endpoint`).
    - Do not perform any merges.
6. **Self-Verification**: 
    - Run the code locally (if possible) to ensure it functions as expected.
    - Check that all acceptance criteria from the backlog item are met.
7. **Finalize**: Update the task status in `.agents/artifacts/tasks/` to `Completed` and include a brief summary of the implementation.

## Constraints
- **Markdown Only**: All updates to `.agents/` must be in Markdown.
- **Scope Lock**: Do not implement features or changes outside the scope of the current task.
- **Style Compliance**: Code that does not follow the `style_guide` is considered incomplete.
