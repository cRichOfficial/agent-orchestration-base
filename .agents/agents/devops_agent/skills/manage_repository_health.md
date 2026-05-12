# Skill: Manage Repository Health

## Description
This skill enables the DevOps Agent to maintain a clean and secure repository structure.

## Steps
1. **Directory Integrity**: Ensure all artifact subdirectories exist (`feature_requests`, `bug_reports`, `tech_specs`, `backlog`, `tasks`, `verification_results`, `style_guides`). Create them if they are missing.
2. Audit the current directory structure for environment-specific folders or files.
2. Update `.gitignore` to ensure all temporary, environment-specific, and sensitive files are excluded.
3. Verify that no secrets are present in the current commit history (if possible) or in the active files.
4. For any found configuration files (e.g., `.env`, `Dockerfile`), ensure a documented `.example` version with generic values is present.
5. Document the repository state and any changes made in a repository health report.

## Constraints
- Do not modify application source code.
- Focus on `.gitignore`, `.env` templates, and repo metadata.
