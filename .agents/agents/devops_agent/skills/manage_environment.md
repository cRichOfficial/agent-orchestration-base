# Skill: Manage Environment

## Description
This skill enables the DevOps Agent to start, stop, and monitor the application and its dependencies.

## Steps
1. Identify the application type (e.g., Web, Mobile, CLI).
2. Determine the necessary commands to start the servers or application (e.g., `npm run dev`, `docker-compose up`).
3. Execute the start commands and verify that the environment is healthy.
4. Provide the access URL or connection details to the requesting agent (usually QA).
5. Monitor logs for errors and provide them upon request.

## Constraints
- Do not modify application source code.
- Ensure all environment variables are correctly loaded (using `.env.example` as a reference).
