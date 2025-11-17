# OctoAcme QA and Testing Guidelines

This document defines the quality assurance strategy, testing expectations, and bug management workflow for OctoAcme projects.

---

## QA Strategy Overview

### Purpose
Establish a consistent, sustainable approach to quality that balances automated testing, manual validation, and fast feedback cycles.

### Guiding Principles
- **Shift-left testing**: Catch issues early in development through unit tests and code reviews
- **Test automation first**: Automate repetitive tests to enable faster releases
- **Risk-based testing**: Prioritize testing effort based on business impact and technical risk
- **Continuous quality**: Integrate quality checks throughout the development process, not just at the end
- **Collaboration**: Quality is a team responsibility, not just QA's

---

## Test Pyramid Expectations

OctoAcme follows the test pyramid model to ensure efficient, maintainable test coverage:

### Unit Tests (Base of Pyramid - 70%)
- **Ownership**: Developers
- **Purpose**: Validate individual functions, methods, and components in isolation
- **Characteristics**: Fast, isolated, no external dependencies
- **Tools**: Language-specific frameworks (e.g., Jest, JUnit, pytest, Go test)
- **Coverage Target**: 80%+ code coverage for business logic
- **When**: Written before or alongside implementation (TDD encouraged)

### Integration Tests (Middle of Pyramid - 20%)
- **Ownership**: Developers with QA Lead guidance
- **Purpose**: Validate interactions between components, services, and external systems
- **Characteristics**: Test multiple components together, may use test databases or mocked external services
- **Tools**: API testing frameworks (e.g., Supertest, RestAssured, pytest), contract testing (e.g., Pact)
- **Coverage Target**: All critical integration points and API contracts
- **When**: During feature development and before release

### End-to-End (E2E) Tests (Top of Pyramid - 10%)
- **Ownership**: QA Lead with Developer support
- **Purpose**: Validate complete user workflows through the UI or public APIs
- **Characteristics**: Slower, more brittle, tests entire stack
- **Tools**: UI automation (e.g., Playwright, Selenium), API test suites
- **Coverage Target**: Critical user journeys and happy paths
- **When**: Before release and on staging environment

### Manual Acceptance Testing
- **Ownership**: QA Lead, Product Manager, Developers
- **Purpose**: Exploratory testing, usability validation, edge cases
- **When**: During feature review and pre-release sign-off
- **Scope**: Focus on new features, changed workflows, and high-risk areas

---

## Testing Environments

### Local Development
- **Purpose**: Developer unit and integration testing
- **Data**: Mocked or local test data
- **Access**: All developers

### CI/CD Pipeline
- **Purpose**: Automated test execution on every commit/PR
- **Data**: Test fixtures and ephemeral test databases
- **Access**: Automated via CI/CD

### Staging / Pre-Production
- **Purpose**: Integration testing, E2E testing, manual acceptance testing
- **Data**: Anonymized production-like data
- **Access**: Developers, QA Lead, Product Manager
- **Refresh Cadence**: Weekly or before major releases

### Production
- **Purpose**: Smoke testing post-deploy, monitoring
- **Data**: Live customer data (read-only for testing)
- **Access**: SRE, Release Manager, QA Lead (limited)
- **Testing**: Smoke tests only, no destructive operations

---

## Test Automation Ownership

### Responsibility Matrix

| Test Type | Develop Tests | Maintain Tests | Run Tests | Review Results |
|-----------|---------------|----------------|-----------|----------------|
| Unit | Developers | Developers | CI/CD, Developers | Developers |
| Integration | Developers | Developers, QA Lead | CI/CD, Developers | Developers, QA Lead |
| E2E | QA Lead, Developers | QA Lead, Developers | CI/CD, QA Lead | QA Lead, Release Manager |
| Manual | QA Lead | QA Lead | QA Lead, Team | QA Lead, Product Manager |

### Automation Guidelines
- All new features must include unit tests
- Critical user flows require E2E test coverage
- Flaky tests must be fixed or disabled within one sprint
- Test code is production code: apply same quality standards
- Test execution time: unit tests <5 min, integration tests <15 min, E2E tests <30 min

---

## Bug Triage Workflow

### How Bugs Are Reported
1. **Discovery**: Bugs found via automated tests, manual testing, production monitoring, or user reports
2. **Logging**: Create a bug ticket with:
   - Clear title and description
   - Steps to reproduce
   - Expected vs. actual behavior
   - Environment and version information
   - Screenshots or logs if applicable
3. **Initial Assessment**: Reporter assigns preliminary severity

### Severity Definitions

| Severity | Definition | Example | Response Time |
|----------|------------|---------|---------------|
| **P0 - Critical** | Production outage, data loss, security breach | Service down, data corruption | Immediate response, all-hands |
| **P1 - High** | Major feature broken, blocks release, significant degradation | Critical workflow broken, major performance issue | Fix within 24 hours |
| **P2 - Medium** | Feature partially broken, workaround available | Minor workflow issue, non-critical bug | Fix in current or next sprint |
| **P3 - Low** | Cosmetic, low-impact, edge case | UI glitch, typo, rare edge case | Fix in backlog, prioritize with other work |

### Triage Cadence and Process
- **Daily**: P0/P1 bugs triaged immediately upon discovery
- **Weekly**: P2/P3 bugs triaged in weekly triage meeting (QA Lead, Product Manager, Project Manager, Dev Lead)

### Triage Meeting Steps
1. **Review new bugs**: QA Lead presents new bugs since last triage
2. **Confirm severity**: Team validates or adjusts severity based on business impact and technical risk
3. **Assign priority**: Product Manager prioritizes bugs relative to backlog
4. **Assign owner**: Developers or QA Lead assigned to investigate or fix
5. **Update status**: Tickets updated with severity, priority, owner, and target sprint

### Bug Triage Owners
- **QA Lead**: Facilitates triage, validates technical severity, recommends prioritization
- **Product Manager**: Final decision on priority and business impact
- **Developers**: Provide technical feasibility and effort estimates
- **Project Manager**: Tracks bug resolution and communicates status

---

## QA and Release Readiness

### QA Lead Interaction with Release Manager

**Pre-Release (1-2 weeks before)**:
- QA Lead shares test plan and coverage status with Release Manager
- Identify any testing gaps or risks
- Coordinate test environment access and data refresh

**Code Freeze to Deployment**:
- QA Lead executes final acceptance testing
- Reports blockers or critical bugs to Release Manager
- Provides cutover readiness sign-off (written approval)

**Post-Deployment**:
- QA Lead executes smoke tests on production
- Validates critical workflows and reports results to Release Manager
- Monitors for issues and triages any production bugs

### QA Lead Interaction with Developers

**During Development**:
- Review acceptance criteria and test scenarios early
- Pair on test design for complex features
- Provide feedback on testability in design reviews

**Before Release**:
- Execute manual acceptance tests
- Report bugs and work with developers on fixes
- Validate bug fixes before release sign-off

**Post-Release**:
- Collaborate on production bug triage and root cause analysis
- Partner on test automation improvements

### QA Lead Interaction with Product Manager

**Feature Planning**:
- Review acceptance criteria for clarity and testability
- Provide input on testing scope and timeline
- Flag quality risks early

**Bug Prioritization**:
- Present bug triage recommendations
- Advocate for quality when prioritizing bug fixes vs. features

**Release Decision**:
- Provide quality metrics and test coverage status
- Recommend go/no-go based on quality criteria

---

## Quality Metrics and Reporting

### Key Metrics
- **Test Coverage**: Percentage of code covered by automated tests (target: 80%+)
- **Test Pass Rate**: Percentage of automated tests passing (target: 95%+)
- **Defect Density**: Bugs found per feature or lines of code
- **Escaped Defects**: Production bugs found post-release (target: minimize)
- **Mean Time to Detect (MTTD)**: Time from bug introduction to detection
- **Mean Time to Resolve (MTTR)**: Time from bug detection to fix

### Reporting Cadence
- **Daily**: Test pass rates shared in CI/CD dashboard
- **Weekly**: Bug triage summary shared with team
- **Per Release**: Quality report with test coverage, defect density, and risk assessment
- **Retrospective**: Quality trends and improvement actions

---

## How to Use These Guidelines
- QA Lead customizes this template for specific project needs
- Review and update guidelines during project retrospectives
- Use as onboarding material for new team members
- Reference during sprint planning to ensure adequate testing time
