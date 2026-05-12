# Skill: Verify Feature

## Description
This skill enables the QA Agent to validate that a newly implemented feature meets all requirements and technical specifications.

## Steps
1. **Review Context**: Read the `feature_request` (requirements) and `tech_spec` (technical design) for the feature.
2. **Setup Test Environment**: 
    - Checkout the relevant `feature/` branch.
    - **Environment Activation**: If the application requires a running server, request the DevOps Agent to start the environment using the `manage_environment` skill.
    - Ensure all dependencies are installed and the environment is configured correctly.
3. **Acceptance Criteria Validation**: 
    - For each criterion listed in the `feature_request`, perform targeted tests to confirm it is met.
    - Test for edge cases and boundary conditions.
4. **Technical Audit**: Verify the implementation follows the `tech_spec` and the project's `style_guides`.
5. **Collect Evidence**: Capture terminal output, logs, or other evidence of successful (or failed) tests.
6. **Report Results**: 
    - Create a detailed report in `.agents/artifacts/verification_results/`.
    - If all criteria pass, mark the feature as `Verified`.
    - If any criteria fail, initiate the `Create Bug Report` skill.

## Constraints
- **Unbiased Testing**: Test from a user's perspective, but verify with a developer's technical knowledge.
- **Traceability**: Link all findings back to the original requirements and technical design.
