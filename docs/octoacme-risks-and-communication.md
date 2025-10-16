# OctoAcme — Risk Management & Communication

> Related to [Issue #4](https://github.com/MJakubecCrif/skills-scale-institutional-knowledge-using-copilot-spaces/issues/4)

## Purpose
Explain how to identify, manage, and communicate risks and dependencies effectively to minimize surprises and enable proactive decision-making.

## Risk Register

Maintain a simple table with:
- **ID**: Unique identifier (e.g., RISK-001)
- **Description**: Clear description of the risk
- **Impact** (High/Med/Low): Potential impact on timeline, quality, or scope
- **Likelihood** (High/Med/Low): Probability of occurrence
- **Owner**: Person responsible for monitoring and mitigating
- **Mitigation plan**: Specific actions to reduce impact or likelihood
- **Status**: Open, Monitoring, Mitigated, Closed
- **Last updated**: Date of last status change

### Risk Register Template

| ID | Description | Impact | Likelihood | Owner | Mitigation Plan | Status | Last Updated |
|----|-------------|--------|------------|-------|----------------|--------|--------------|
| RISK-001 | Example: Third-party API dependency may have rate limits | High | Medium | @dev-lead | Implement caching layer and fallback mechanism | Open | 2025-10-16 |

## Risk Lifecycle

### 1. Identify
**When**: During planning and ongoing execution (weekly risk reviews)

**How to identify risks**:
- Review dependencies on external teams or systems
- Analyze technical complexity and unknowns
- Consider resource availability and expertise gaps
- Review past project retrospectives for common issues
- Consult with subject matter experts

**Common risk categories**:
- Technical: Architecture decisions, technical debt, integration complexity
- Resource: Team availability, skill gaps, budget constraints
- External: Third-party dependencies, regulatory changes, market shifts
- Organizational: Competing priorities, stakeholder alignment, change management

### 2. Assess
**Estimate impact and likelihood**:

**Impact levels**:
- **High**: Could cause major timeline delay (>2 weeks), quality degradation, or scope cut
- **Medium**: Could cause moderate delay (3-10 days) or require workarounds
- **Low**: Minor impact, easily absorbed by team

**Likelihood levels**:
- **High**: Very likely to occur (>60% probability)
- **Medium**: May occur (30-60% probability)
- **Low**: Unlikely to occur (<30% probability)

**Priority**: High impact + High likelihood = Top priority for mitigation

### 3. Mitigate
**Reduce risk via actions and contingency plans**:

**Mitigation strategies**:
- **Avoid**: Change approach to eliminate the risk
- **Reduce**: Take actions to lower likelihood or impact
- **Transfer**: Shift responsibility (e.g., use managed service)
- **Accept**: Acknowledge and plan contingency if it occurs

**Example mitigations**:
- Technical spikes to reduce uncertainty
- Early integration testing with dependencies
- Buffer time in schedule for high-uncertainty work
- Cross-training team members to reduce single-person dependencies
- Regular check-ins with external teams

### 4. Monitor
**Review at weekly syncs and update status**:

**Weekly risk review checklist**:
- [ ] Review all open risks for status changes
- [ ] Add newly identified risks
- [ ] Update mitigation actions and owners
- [ ] Escalate high-priority risks that need leadership attention
- [ ] Close resolved or no-longer-relevant risks
- [ ] Communicate top 3 risks in status updates

## Stakeholder Communication

### Identifying Stakeholders
**Stakeholder groups** and their communication needs:
- **Engineering teams**: Technical details, dependencies, API changes
- **Sales & Marketing**: Feature availability, customer benefits, go-to-market timing
- **Support & Success**: Known issues, troubleshooting guides, customer impact
- **Compliance & Legal**: Security, privacy, regulatory requirements
- **Executive/Leadership**: Business impact, timeline, budget, risks

### Communication Planning
For each stakeholder group, define:
- **Key contacts**: Primary and backup
- **Communication frequency**: Weekly, monthly, milestone-based, as-needed
- **Communication method**: Email, Slack, meetings, dashboards
- **Information needs**: What they need to know and when
- **Feedback mechanism**: How they can provide input

### Regular Updates
**Provide regular updates** (weekly or milestone-based):
- Use a single source of truth (project README or release doc) for status
- Keep updates consistent in format and timing
- Highlight changes since last update
- Clearly mark action items and decisions needed

### Communication Templates

#### Weekly Status Template
```markdown
## Project Status Update - [Date]

### Progress This Week
- [Completed work items with links]
- [Key achievements or milestones]

### Next Steps
- [Planned work for coming week]
- [Upcoming milestones]

### Risks & Blockers
- [Active risks from risk register]
- [Current blockers and impact]

### Asks / Decisions Needed
- [Specific requests for stakeholder input]
- [Pending decisions and deadline]

### Metrics
- [Relevant KPIs or progress indicators]
- [Burndown/velocity if applicable]
```

#### Stakeholder Update Email Template
```markdown
Subject: [Project Name] - [Milestone] Update

Hi [Stakeholder Group],

Quick update on [Project Name]:

**Status**: [On Track / At Risk / Delayed]

**Recent Progress**:
- [Key accomplishments]

**What's Next**:
- [Upcoming deliverables]
- [Timeline for next milestone]

**What We Need From You**:
- [Specific asks or decisions]

**Risk Highlights**:
- [Top 1-2 risks if any]

Questions? Reply here or join our weekly sync [day/time].

Thanks,
[PM Name]
```

#### Incident Communication Template
```markdown
## Incident Summary - [Date/Time]

### Status
[Identified / Investigating / Mitigating / Resolved]

### Impact
- [Affected systems/users]
- [Severity level]

### Triage Summary
- [What happened]
- [When it was detected]
- [Current understanding of root cause]

### Actions Being Taken
- [Immediate mitigation steps]
- [Team members involved]

### Expected Timeline
- [ETA for resolution]
- [Next update scheduled]

### Follow-up
- Post-incident blameless retrospective scheduled for [date/time]
- Action items will be tracked in [location]
```

## Escalation Paths

Clear escalation paths ensure blockers and risks are addressed at the appropriate level without unnecessary delays.

### Escalation Levels

#### Level 1: Team-level Resolution
**When to use**: Blockers that can be resolved within the delivery team

**Examples**:
- Technical questions or design decisions
- Code review delays
- Test environment issues
- Minor scope clarifications

**Process**:
- Raise in daily standup
- Team discusses and assigns owner
- Resolution expected within 1-2 days

**Owner**: Engineering Lead or Tech Lead

---

#### Level 2: PM/Product Lead Escalation
**When to use**: Issues requiring cross-team coordination, resource allocation, or scope decisions

**Examples**:
- Dependencies on other teams causing delays
- Resource constraints (people unavailable, skills gap)
- Scope changes or competing priorities
- External vendor delays
- Risks becoming more likely or severe

**Process**:
- PM escalates to Product Lead and dependent teams
- Joint discussion to determine resolution approach
- Document decision and communicate to affected parties
- Resolution expected within 3-5 days

**Owner**: Project Manager + Product Manager

---

#### Level 3: Sponsor/Executive Escalation
**When to use**: Business-impacting issues requiring executive decision or resources

**Examples**:
- Major timeline slips (>2 weeks)
- Budget overruns or need for additional resources
- Critical production incidents affecting customers
- Scope changes requiring business approval
- Organizational conflicts or priority disputes
- Security incidents (follow security runbook)

**Process**:
- PM prepares escalation brief (impact, options, recommendation)
- Present to sponsor/executive with Product Lead
- Document decision and cascade communication
- Resolution timeline varies by complexity

**Owner**: Executive Sponsor + Product Lead

### Escalation Guidelines

**When escalating, always include**:
- Clear description of the issue
- Impact on timeline, quality, or scope
- Options considered and recommendation
- What decision or resource is needed
- Urgency and deadline for decision

**Best practices**:
- Escalate early - don't wait until it's a crisis
- Come with options and a recommendation
- Document the decision and rationale
- Communicate the resolution to all affected parties
- Update risk register with resolution

### Special Escalations

#### Security Incidents
- Follow the security incident runbook
- Notify Security on-call immediately
- Do not delay for normal escalation process
- Post-incident review required

#### Customer-Impacting Production Issues
- Follow incident response playbook
- Notify on-call and leadership immediately
- Prioritize customer communication
- Post-incident blameless retrospective required

---

## Dependency Management

### Identifying Dependencies
**Types of dependencies**:
- **Technical**: APIs, shared services, infrastructure
- **Resource**: Shared team members, tools, environments
- **Sequential**: One task must complete before another starts
- **Cross-team**: Work owned by another team

### Tracking Dependencies
- Mark dependencies clearly in project board
- Assign dependency owner on both sides
- Document expected delivery dates
- Include in risk register if high-impact

### Managing Dependencies
- **Early identification**: Surface dependencies in planning
- **Regular check-ins**: Weekly status updates with dependency owners
- **Buffer time**: Add buffer for external dependencies
- **Escalation**: Escalate delays that impact critical path
- **Documentation**: Keep dependency list updated and visible

### Dependency Tracking Template

| Dependency | Description | Depends On | Owner | Expected Date | Status | Risk Level |
|------------|-------------|------------|-------|---------------|--------|------------|
| DEP-001 | Auth API integration | Platform team API | @platform-lead | 2025-11-01 | On Track | Medium |

---

## Communication Best Practices

### Principles
- **Transparency**: Share information openly and proactively
- **Consistency**: Use standard formats and regular cadence
- **Clarity**: Be specific about asks and decisions needed
- **Timeliness**: Don't let stakeholders be surprised
- **Two-way**: Create channels for feedback and questions

### Meeting Effectiveness
- **Clear agenda**: Share in advance with goals and topics
- **Time management**: Start/end on time, keep discussions focused
- **Action items**: Document decisions and next steps with owners
- **Follow-up**: Share notes within 24 hours

### Written Communication
- **Subject lines**: Clear and specific
- **Structure**: Use headings, bullets, and formatting
- **Action-oriented**: Be clear about what you need
- **Links**: Reference relevant docs, issues, or dashboards
- **Audience**: Tailor detail level to recipient needs

---

## Tools and Dashboards

### Recommended Tools
- **Project tracking**: GitHub Projects, Jira, Asana
- **Communication**: Slack, Teams, Email
- **Documentation**: GitHub, Confluence, Google Docs
- **Metrics**: Dashboards for KPIs, velocity, quality

### Dashboard Guidelines
- Keep dashboards simple and focused
- Update automatically when possible
- Make data accessible to all stakeholders
- Review and refine metrics regularly
