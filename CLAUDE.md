from pathlib import Path

content = """# Javan Marketing Agent — Claude Instructions

## Mission

Javan Marketing Agent is an AI-assisted marketing system focused on discovering potential leads, scoring them transparently, preparing outreach for human approval, maintaining platform-independent CRM data, and learning from controlled feedback.

## Current Focus

The current development phase focuses on the internal core of the agent:

- Lead discovery and normalization
- Lead scoring
- Lead qualification
- Internal CRM data and services
- Orchestration of agent workflows
- Controlled learning and feedback
- Automated tests and code quality

## Development Principles

1. Keep the code modular, testable, and maintainable.
2. Prefer explicit, deterministic behavior over hidden assumptions.
3. Use type hints throughout the Python codebase.
4. Validate external and user-provided data before processing it.
5. Keep business logic separate from API, database, and external-integration layers.
6. Write tests for important business rules and scoring logic.
7. Do not introduce unnecessary dependencies.
8. Do not expose secrets, API keys, credentials, or personal data in source code or logs.

## Safety and Approval Rules

- Do not send messages to leads automatically without an explicit human-approval workflow.
- Do not impersonate people or organizations.
- Do not collect or expose unnecessary personal information.
- Do not add external integrations unless they are explicitly planned, documented, and implemented with appropriate authorization.
- External communication channels must remain disabled until their integration and approval workflow are deliberately implemented.

## Out of Scope for the Initial Core

The initial core does not include:

- Automatic WhatsApp messaging
- Automatic Telegram messaging
- Automatic email campaigns
- Unapproved social-media automation
- Voice cloning or impersonation
- Autonomous purchasing or financial transactions
- Uncontrolled self-modifying behavior

These may be considered later as separate, explicitly authorized integrations.

## Project Structure

Application code belongs under `src/javan_agent`.

Tests belong under `tests`.

Configuration and project documentation belong at the repository root.

## Code Quality

Use Python 3.11 or newer.

Use Ruff for linting and formatting where configured.

Use pytest for tests.

Use strict type checking where configured.

Before considering a feature complete:

1. Implement the smallest correct change.
2. Add or update tests.
3. Run the relevant test suite.
4. Run linting and type checking when applicable.
5. Review the change for security, privacy, and unintended side effects.

## Change Policy

Do not make broad architectural changes without documenting the reason.

Do not remove existing functionality merely to make a test pass.

When requirements are ambiguous, prefer the safest interpretation and document the assumption.

Every new external integration should be isolated behind a service/interface so the core agent remains platform-independent.

## Definition of Done

A change is considered complete only when:

- The implementation is coherent and maintainable.
- Relevant tests pass.
- No secrets are committed.
- Documentation is updated when behavior or architecture changes.
- The change does not bypass required human approval or authorization.
"""
path = Path("/mnt/data/CLAUDE.md")
path.write_text(content, encoding="utf-8")
print(path)

