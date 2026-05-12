# Agent Orchestration Framework for Antigravity

This repository implements a structured, multi-agent Software Development Life Cycle (SDLC) automation framework specifically designed for **Google's Antigravity IDE**. It utilizes specialized AI agents and orchestrated workflows to transform high-level requirements into verified, version-controlled code.

## 🏗️ Architecture Overview

The framework is organized into three core pillars located within the `.agents/` directory:

### 1. Agents
Specialized roles with dedicated **Rules** (behavioral constraints) and **Skills** (operational procedures):
- **PM Agent**: Manages requirements, user value, and the product backlog.
- **Architect Agent**: Designs technical specifications and establishes coding standards (style guides).
- **Coder Agent**: Implements features and bug fixes within isolated `feature/` and `bug/` branches.
- **QA Agent**: Validates implementations against requirements and designs; manages bug reporting.
- **DevOps Agent**: Ensures repository health, security, and performs final branch audits before user approval.

### 2. Workflows
Standardized processes for common SDLC tasks:
- **App Generation**: End-to-end creation of new applications with built-in approval gates.
- **Feature Update**: Managed process for enhancing existing applications.
- **Bug Fix**: Disciplined triage, root cause analysis (RCA), and verification flow.

### 3. Artifacts
The shared knowledge base used for inter-agent communication:
- `feature_requests/`: High-level requirements.
- `tech_specs/`: Technical blueprints.
- `backlog/`: Atomic tasks ready for development.
- `tasks/`: Real-time status of ongoing work.
- `bug_reports/`: Detailed defect documentation.
- `style_guides/`: Technical standards and best practices.

---

## 📁 Directory Structure

```text
.agents/
├── agents/            # Agent-specific rules and skills
├── workflows/         # SDLC process definitions
└── artifacts/         # Shared state and communication files
src/                   # Application source code (managed by Coder)
```

## 🚀 How It Works

1. **Initiation**: The PM Agent captures a user request as a `feature_request`.
2. **Design**: Once approved, the Architect creates a `tech_spec` and the PM creates the `backlog`.
3. **Execution**: The Coder picks up backlog items, creates a branch, and implements the code in `/src/`.
4. **Verification**: The QA Agent verifies the branch and logs results or bugs.
5. **Review**: The DevOps Agent audits the branch and presents a summary to the user.
6. **Completion**: The User performs the final merge into the main branch.

---

## 🛡️ Key Principles
- **Directory Isolation**: Agents are strictly restricted to their authorized directories.
- **Branch-Based Development**: No direct commits to protected branches; all work happens on feature/bug branches.
- **Security First**: Secrets and environment configurations are strictly managed and excluded via the DevOps Agent.
- **Approval Gates**: Critical milestones require explicit manual approval from the user.
