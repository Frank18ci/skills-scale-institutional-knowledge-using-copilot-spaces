# OctoAcme Project Management Processes

OctoAcme runs projects through a lightweight lifecycle of Initiation, Planning, Execution, Release, and Retrospective. Projects begin with a Project One-pager that defines the problem, objective, and measurable success criteria; stakeholders and a sponsor are identified; and an initial risk list and timeline are created to decide whether to move into planning. Planning breaks approved initiatives into shippable increments, produces a prioritized backlog with acceptance criteria, and documents a Definition of Done and draft QA approach. Execution is board-driven (Backlog → Ready → In Progress → In Review → QA → Done) and emphasizes small pull requests, CI checks, and iterative delivery. Releases follow a standard checklist (pre-release checks, smoke tests, rollback plan and release notes) to reduce deployment risk.

Workflows and quality assurance are integrated end-to-end. The team uses a project board and a disciplined pull request process: small PRs that reference issues and acceptance criteria, automated tests and linting in CI, and at least one approval before merging. Testing includes unit and integration tests, end-to-end smoke tests for critical flows, security scanning in CI, and manual QA where required. Reporting tracks velocity, burndown, and success metrics defined in the Project One-pager; dashboards surface key signals like errors and latency.

Roles and responsibilities are explicit: Project Managers coordinate delivery, schedules, risks, and stakeholder communications; Product Managers own outcomes, prioritization, and success metrics; Developers implement code, tests, and documentation; QA validates acceptance criteria; and stakeholders provide input and approvals. Role clarity reduces single-person dependency and makes owners explicit for backlog items, risks, and retrospective action items.

Communication and risk practices emphasize a regular cadence and single sources of truth. Team rhythm includes daily standups, weekly delivery syncs, PM–PdM alignment, demos at milestone ends, and monthly stakeholder updates. Risks are tracked in a simple register (ID, impact, likelihood, owner, mitigation) and reviewed weekly; blocker escalation follows a three-level path from team triage to sponsor escalation. Retrospectives prioritize a few actionable improvements and convert action items into tracked issues so the team can measure impact and close the loop.

## How to use these docs

This README lives in docs/ as the overview for anyone onboarding or referencing OctoAcme processes. The docs/ directory contains the detailed process documents; link to them in the table below.

## Table of contents

- [octoacme-project-management-overview.md](octoacme-project-management-overview.md)
- [octoacme-project-initiation.md](octoacme-project-initiation.md)
- [octoacme-project-planning.md](octoacme-project-planning.md)
- [octoacme-execution-and-tracking.md](octoacme-execution-and-tracking.md)
- [octoacme-release-and-deployment.md](octoacme-release-and-deployment.md)
- [octoacme-risks-and-communication.md](octoacme-risks-and-communication.md)
- [octoacme-retrospective-and-continuous-improvement.md](octoacme-retrospective-and-continuous-improvement.md)
- [octoacme-roles-and-personas.md](octoacme-roles-and-personas.md)
