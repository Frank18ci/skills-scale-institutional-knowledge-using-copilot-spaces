# OctoAcme Project Management Overview

## Purpose
Provide a concise, shareable introduction to how OctoAcme runs projects so new teammates can quickly understand our approach, roles, and key artifacts.

## Scope
Applies to all cross-functional projects that deliver product features, services, or integrations.

## Principles
- Customer-first: prioritize customer value and usability.
- Iterative delivery: deliver small, testable increments.
- Clear ownership: each project has a named Project Manager (PM) and Product Lead.
- Data-informed decisions: measure impact and iterate based on evidence.
- Psychological safety: encourage feedback and learning.

## Core Roles
- **Project Manager (PM)**: coordinates delivery, schedules, risk, communications.
- **Product Manager (PdM)**: defines outcomes, prioritizes backlog, and measures success.
- **Developers**: implement features, collaborate on design and testability.
- **QA Lead**: defines quality strategy, test planning, and ensures acceptance criteria are met.
- **Release Manager**: coordinates release activities, deployment, and cutover readiness.
- **UX Designer**: advocates for user needs and ensures consistent user experience.
- **Scrum Master**: facilitates agile ceremonies, removes blockers, coaches on agile practices.
- **Site Reliability Engineer (SRE)**: ensures production reliability, manages incidents, executes deployments.
- **Security Owner**: lightweight security advocacy and vulnerability management.
- **Stakeholders**: provide inputs and approvals.

For detailed persona definitions, responsibilities, and interaction points, see [OctoAcme Roles and Personas](octoacme-roles-and-personas.md).

## Key Artifacts
- Project Charter / One-pager
- Roadmap and Release Plan
- Sprint/Iteration Backlog
- Acceptance Criteria & Definition of Done
- Risk Register
- Retrospective notes and action items
- [Release Checklist](octoacme-release-checklist.md): comprehensive release process and readiness criteria
- [QA and Testing Guidelines](octoacme-qa-and-testing-guidelines.md): quality strategy, test pyramid, and bug triage workflow

## Lifecycle (high-level)
1. Initiation: problem statement, stakeholders, high-level timeline.
2. Planning: scope, resources, milestones, dependencies.
3. Execution: build, test, review, iterate.
4. Release: deploy, verify, announce.
5. Close & Retrospective: capture learnings and next steps.

## Communication Cadence
- Weekly sync between PM + PdM
- Twice-weekly standups for delivery team (or as agreed)
- Monthly stakeholder updates
- Ad-hoc escalations as needed

## How to use these docs
- Keep the Project Charter updated in the project repo.
- Add process-specific docs into `.copilot/` if you want Copilot Spaces to use them as context.
