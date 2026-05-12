# Skill: Regression Test

## Description
This skill enables the QA Agent to ensure that new code changes have not negatively impacted existing functionality.

## Steps
1. Identify critical paths and previously implemented features.
2. Execute a suite of tests (manual or automated) covering these areas.
3. Compare the behavior to the baseline (the state of the app before the recent changes).
4. Document the results in the `verification_results/` folder.

## Constraints
- Focus on "Side Effect" detection.
- If a regression is found, immediately create a high-priority bug report.
