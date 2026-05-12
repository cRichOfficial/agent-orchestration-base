# Skill: Generate Technical Specification

## Description
This skill enables the Architect Agent to design the technical architecture for an approved feature request.

## Steps
1. Review the approved `feature_request` artifact.
2. Design the system architecture, including data flow and component interactions.
3. Define the directory structure and file names.
4. Document API interfaces or internal function signatures.
5. Create a new markdown file in `.agents/artifacts/tech_specs/` following the naming convention `[feature_name]_spec.md`.

## Constraints
- Output must be Markdown only.
- Do not write source code; use code blocks for interface definitions or pseudo-structure only.
- Ensure the design follows established project patterns.
