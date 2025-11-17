# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## QA Lead

### Role Summary
The QA Lead defines the quality strategy, owns test planning and execution, and ensures acceptance criteria are met before releases. They coordinate testing activities across the team and represent quality in release decisions.

### Responsibilities
- Define QA strategy, test pyramid expectations (unit/integration/e2e)
- Plan test coverage for features and releases
- Lead bug triage and manage severity definitions
- Coordinate manual acceptance testing and automation ownership
- Partner with Release Manager on cutover readiness
- Advocate for quality and testability in design reviews

### Goals
- Ensure high-quality releases with minimal production defects
- Build sustainable test automation and reduce manual testing burden
- Provide clear visibility into test coverage and quality metrics
- Enable fast feedback loops for developers

### Typical Communication and Interaction Points
- **Developers**: Review acceptance criteria, collaborate on test design, triage bugs
- **Release Manager**: Sign-off on cutover readiness, smoke test results, deployment validation
- **Product Manager**: Clarify acceptance criteria, prioritize bug fixes vs. new features
- **Project Manager**: Report quality status, flag risks, coordinate testing timeline
- **Stakeholders**: Present quality metrics and release confidence
- **Decision Ownership**: Test strategy, bug severity classification, go/no-go on quality grounds
- **Handoffs**: Test plans to developers, smoke test results to Release Manager, bug triage outcomes to PM

---

## Release Manager

### Role Summary
The Release Manager coordinates and executes release activities, ensures deployment readiness, and manages the release lifecycle from planning through post-deployment verification.

### Responsibilities
- Create and maintain release schedule and checklist
- Coordinate pre-release preparation (code freeze, release notes, environment readiness)
- Execute deployment procedures and coordinate rollout
- Lead post-deploy verification and smoke testing
- Manage rollback decisions if issues arise
- Maintain release runbooks and deployment documentation

### Goals
- Deliver safe, predictable releases with minimal downtime
- Minimize deployment-related incidents
- Maintain clear communication before, during, and after releases
- Continuously improve release automation and efficiency

### Typical Communication and Interaction Points
- **Developers**: Coordinate code freeze, gather release notes, manage hotfix requests
- **QA Lead**: Validate test completion, receive smoke test sign-off, coordinate deployment verification
- **Product Manager**: Confirm feature readiness, align on release scope and announcements
- **Project Manager**: Provide release status updates, flag schedule risks
- **Site Reliability Engineer**: Coordinate deployment execution, monitor production health, plan rollback if needed
- **Stakeholders**: Communicate release timeline and completion
- **Decision Ownership**: Release timing, deployment execution, rollback/proceed decisions
- **Handoffs**: Release notes from developers, cutover sign-off from QA Lead, deployment runbook to SRE

---

## UX Designer

### Role Summary
UX Designers advocate for user needs, create design solutions that balance usability and technical feasibility, and ensure consistent user experience across the product.

### Responsibilities
- Conduct user research and usability testing
- Create wireframes, prototypes, and design specifications
- Partner with Product Manager on feature definition and acceptance criteria
- Collaborate with Developers on implementation feasibility
- Review and validate UI implementation for design consistency
- Maintain design system and component library

### Goals
- Deliver intuitive, accessible user experiences
- Reduce user friction and support adoption
- Ensure design consistency across features
- Balance user needs with technical constraints

### Typical Communication and Interaction Points
- **Product Manager**: Co-define problem statements, validate solutions with users, align on priorities
- **Developers**: Review design feasibility, clarify specs during implementation, validate UI
- **QA Lead**: Define acceptance criteria for UI/UX, review test scenarios
- **Project Manager**: Provide design timeline estimates, flag design-related risks
- **Stakeholders**: Present design concepts and user research findings
- **Decision Ownership**: Design approach, UI patterns, usability trade-offs
- **Handoffs**: Design specs to developers, prototypes to Product Manager, acceptance criteria to QA Lead

---

## Scrum Master

### Role Summary
The Scrum Master facilitates agile ceremonies, removes blockers, and coaches the team on agile practices. They ensure the team has a healthy, productive working environment.

### Responsibilities
- Facilitate sprint planning, daily standups, retrospectives, and reviews
- Remove impediments and blockers for the team
- Coach team members on agile principles and practices
- Protect the team from scope creep and distractions
- Track and improve team velocity and health metrics
- Foster psychological safety and continuous improvement

### Goals
- Maximize team effectiveness and delivery velocity
- Create a collaborative, high-trust team environment
- Reduce waste and process friction
- Enable team self-organization and ownership

### Typical Communication and Interaction Points
- **Developers**: Remove blockers, facilitate collaboration, coach on agile practices
- **Product Manager**: Facilitate backlog refinement, mediate scope negotiations
- **Project Manager**: Align on delivery cadence, share velocity and capacity
- **QA Lead**: Coordinate testing integration into sprint workflow
- **Team (entire)**: Facilitate retrospectives, implement improvement actions
- **Decision Ownership**: Sprint ceremony structure, process improvements, escalation of impediments
- **Handoffs**: Sprint goals to team, retrospective action items to PM/PdM, velocity trends to Project Manager

---

## Site Reliability / On-call Engineer (Support)

### Role Summary
Site Reliability Engineers (SREs) ensure production systems are reliable, observable, and performant. They manage on-call rotation, incident response, and partner with development teams on operational excellence.

### Responsibilities
- Maintain production monitoring, alerting, and observability
- Respond to incidents and coordinate incident resolution
- Execute deployment procedures and production changes
- Manage on-call rotation and escalation procedures
- Define and track SLIs, SLOs, and error budgets
- Partner with Developers on system reliability and performance

### Goals
- Maintain high availability and reliability of production systems
- Minimize mean time to recovery (MTTR) for incidents
- Improve observability and reduce toil through automation
- Balance reliability with velocity using error budgets

### Typical Communication and Interaction Points
- **Developers**: Review operational requirements, collaborate on incident fixes, improve monitoring
- **Release Manager**: Execute deployments, coordinate rollback decisions, validate production health
- **QA Lead**: Validate production smoke tests, coordinate environment access
- **Project Manager**: Report on production health, escalate reliability risks
- **Product Manager**: Communicate customer impact during incidents, balance reliability vs. features
- **Stakeholders**: Incident communication and post-mortem reports
- **Decision Ownership**: Incident response actions, rollback execution, operational trade-offs
- **Handoffs**: Deployment execution from Release Manager, incident reports to stakeholders, reliability feedback to Developers

---

## Security Owner

### Role Summary
The Security Owner (a lightweight role for security-sensitive projects) ensures security considerations are integrated throughout the development lifecycle. They advocate for security best practices and coordinate security reviews.

### Responsibilities
- Perform lightweight threat modeling for features
- Review code and architecture for security vulnerabilities
- Coordinate security testing and penetration tests
- Ensure compliance with security policies and standards
- Triage security-related bugs and coordinate fixes
- Provide security guidance during design and code reviews

### Goals
- Minimize security vulnerabilities in releases
- Ensure security is considered early in design
- Maintain security compliance and audit readiness
- Foster security awareness across the team

### Typical Communication and Interaction Points
- **Developers**: Review code for security issues, provide secure coding guidance
- **Product Manager**: Assess security risk of features, balance security vs. usability
- **Project Manager**: Flag security risks and compliance requirements
- **QA Lead**: Define security test scenarios, coordinate security testing
- **Release Manager**: Block releases for critical security issues, coordinate security patches
- **Stakeholders**: Report security posture and compliance status
- **Decision Ownership**: Security risk assessment, vulnerability severity, security requirement prioritization
- **Handoffs**: Threat models to developers, security test requirements to QA Lead, vulnerability reports to PM

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

