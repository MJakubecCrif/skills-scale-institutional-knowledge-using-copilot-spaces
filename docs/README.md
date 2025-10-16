# OctoAcme Project Management Documentation

Welcome to the OctoAcme Project Management documentation! This guide provides an overview of how OctoAcme runs projects, including our workflows, roles, communication practices, and quality standards.

## Overview

OctoAcme follows a structured yet flexible approach to project management that emphasizes customer value, iterative delivery, and continuous improvement. Our processes are designed to help cross-functional teams deliver features, services, and integrations efficiently while maintaining high quality standards.

## Core Principles

- **Customer-first**: Prioritize customer value and usability
- **Iterative delivery**: Deliver small, testable increments
- **Clear ownership**: Each project has a named Project Manager (PM) and Product Lead
- **Data-informed decisions**: Measure impact and iterate based on evidence
- **Psychological safety**: Encourage feedback and learning

## Key Roles and Responsibilities

### Project Manager (PM)
- Coordinates delivery, schedules, risk, and communications
- Manages project plans, timelines, and resource constraints
- Facilitates meetings (kickoff, planning, retrospectives)
- Ensures transparent project documentation and status reporting

### Product Manager (PdM)
- Defines outcomes, prioritizes backlog, and measures success
- Owns the product vision and roadmap
- Validates solutions through user research and metrics
- Collaborates on trade-offs with stakeholders and engineering

### Developers
- Implement features and collaborate on design and testability
- Write and maintain tests and documentation
- Participate in design and code reviews
- Help estimate work and identify technical risks

### QA/Testing
- Validate quality and acceptance criteria
- Ensure comprehensive test coverage
- Conduct manual testing when needed

### Stakeholders
- Provide inputs, requirements, and approvals
- Receive regular updates on project progress

[Learn more about roles →](octoacme-roles-and-personas.md)

## Project Lifecycle

Our project lifecycle consists of five key phases:

### 1. Initiation
Define the problem, validate business need, identify stakeholders, and create initial timeline.

**Key deliverables:**
- Project One-pager (Problem, Goal, Success Metrics)
- Stakeholder list & communication plan
- High-level timeline and key milestones
- Initial risk list

[Learn more about Project Initiation →](octoacme-project-initiation.md)

### 2. Planning
Transform the approved initiative into an actionable plan and backlog.

**Key activities:**
- Kickoff meeting with stakeholders and delivery team
- Create prioritized backlog with acceptance criteria
- Define Definition of Done (DoD)
- Identify dependencies and create release plan

[Learn more about Project Planning →](octoacme-project-planning.md)

### 3. Execution & Tracking
Day-to-day execution and progress tracking toward milestones.

**Team rhythm:**
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

**Workflows:**
- Use project boards with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Small PRs (<= 400 lines when possible)
- Automated tests and linting in CI
- At least one approval before merging

[Learn more about Execution & Tracking →](octoacme-execution-and-tracking.md)

### 4. Release & Deployment
Standardized release process to reduce risk and improve observability.

**Release types:**
- **Patch**: Hotfixes addressing critical production issues
- **Minor**: Incremental features and improvements
- **Major**: Significant functionality or breaking changes

**Pre-release requirements:**
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback plan documented

[Learn more about Release & Deployment →](octoacme-release-and-deployment.md)

### 5. Retrospective & Continuous Improvement
Capture learnings and convert them into actionable improvements.

**Structure:**
- What went well
- What could be improved
- Action items (owner, due date)
- Follow-up on previous action items

[Learn more about Retrospectives →](octoacme-retrospective-and-continuous-improvement.md)

## Communication & Collaboration

### Communication Cadence
- **Weekly sync** between PM + PdM
- **Twice-weekly standups** for delivery team (or as agreed)
- **Monthly stakeholder updates**
- **Ad-hoc escalations** as needed

### Status Reporting
Weekly status template includes:
- Progress this week
- Next steps
- Risks & blockers
- Ask / decisions needed

### Escalation Paths
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

[Learn more about Communication & Risk Management →](octoacme-risks-and-communication.md)

## Quality Assurance Practices

### Testing Requirements
- **Unit tests** for new logic
- **Integration tests** where applicable
- **End-to-end smoke tests** for critical flows before release
- **Security scanning** in CI
- **Manual QA** for feature acceptance when needed

### Pull Request Standards
- Small, focused PRs (ideally <= 400 lines)
- Include issue link and acceptance criteria in PR description
- Run automated tests and linting in CI before requesting review
- Require at least one approval before merging (or team-defined policy)

### Definition of Done
Each project defines its own Definition of Done, typically including:
- Code complete and reviewed
- Tests written and passing
- Documentation updated
- Acceptance criteria met
- Deployed to staging and verified

## Key Artifacts

Throughout the project lifecycle, we maintain these important documents:

- **Project Charter / One-pager** — Problem statement, goals, success metrics
- **Roadmap and Release Plan** — Timeline and milestones
- **Sprint/Iteration Backlog** — Prioritized work items
- **Acceptance Criteria & Definition of Done** — Quality standards
- **Risk Register** — Identified risks and mitigation plans
- **Retrospective notes** — Learnings and action items

## Risk Management

We proactively identify and manage risks throughout the project:

- **Identify**: During planning and ongoing execution
- **Assess**: Estimate impact and likelihood
- **Mitigate**: Reduce via actions and contingency plans
- **Monitor**: Review at weekly syncs and update status

Risk Register includes:
- ID, Description, Impact (High/Med/Low), Likelihood (High/Med/Low)
- Owner, Mitigation plan, Status

[Learn more about Risk Management →](octoacme-risks-and-communication.md)

## Getting Started

### For New Team Members
1. Review this README to understand our overall approach
2. Read the [Project Management Overview](octoacme-project-management-overview.md) for core principles
3. Familiarize yourself with your [role and responsibilities](octoacme-roles-and-personas.md)
4. Review relevant phase documents based on current project stage
5. Ask your PM or team lead for project-specific artifacts

### For Project Managers
1. Use the [Project Initiation Guide](octoacme-project-initiation.md) to start new projects
2. Follow the [Project Planning](octoacme-project-planning.md) process to create actionable plans
3. Implement [Execution & Tracking](octoacme-execution-and-tracking.md) practices for day-to-day management
4. Plan releases using the [Release & Deployment Guide](octoacme-release-and-deployment.md)
5. Schedule [Retrospectives](octoacme-retrospective-and-continuous-improvement.md) to drive improvement

### Using These Docs with Copilot Spaces
- Keep process-specific docs in the `.copilot/` directory for Copilot Spaces context
- Maintain project artifacts in the project repository
- Update the Project Charter regularly to reflect current status

## Additional Resources

- [Project Management Overview](octoacme-project-management-overview.md) — High-level introduction to our approach
- [Roles and Personas](octoacme-roles-and-personas.md) — Detailed role definitions
- [Project Initiation](octoacme-project-initiation.md) — Starting new projects
- [Project Planning](octoacme-project-planning.md) — Creating actionable plans
- [Execution & Tracking](octoacme-execution-and-tracking.md) — Day-to-day management
- [Release & Deployment](octoacme-release-and-deployment.md) — Production releases
- [Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md) — Learning and improving
- [Risk Management & Communication](octoacme-risks-and-communication.md) — Managing risks and stakeholder communication

---

For questions or suggestions about these processes, please reach out to your Project Manager or Product Lead.
