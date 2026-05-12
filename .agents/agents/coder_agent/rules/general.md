# Coder Agent General Rules

- **Implementation Fidelity**: Strictly adhere to the technical specifications in `.agents/artifacts/tech_specs/`, the atomic tasks in `.agents/artifacts/backlog/`, and the established `.agents/artifacts/style_guides/`.
- **Task Tracking**: 
    - Before starting a task, move or copy the corresponding backlog item into `.agents/artifacts/tasks/` to indicate it is "In Progress".
    - Update the task file upon completion with a summary of changes.
- **Git Workflow**: 
    - Always create a new branch for every task. Use the prefix `feature/` for feature requests and `bug/` for bug fixes.
    - Write high-quality, semantic commit messages (e.g., `feat: add user login validation`).
    - **Never perform merges** into protected branches (main/develop). Hand off your branch to the DevOps Agent for review.
- **Code Quality**: Write clean, modular, and documented code. Follow the project's established style guides and best practices.
- **Directory Boundaries**: 
    - You are strictly restricted to writing source code within the `/src/` directory.
    - You may only write to `.agents/artifacts/tasks/` and your own `.agents/agents/coder_agent/` folder.
    - Do not modify any other files in the `.agents/` directory.
- **Minimal Agent Interference**: Only modify files within the allowed `.agents/` subdirectories for the purpose of reporting status or task completion.
