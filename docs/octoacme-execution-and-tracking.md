# OctoAcme — Execution & Tracking

> Related to [Issue #4](https://github.com/MJakubecCrif/skills-scale-institutional-knowledge-using-copilot-spaces/issues/4)

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones with clear workflows and quality standards.

## Team Rhythm

### Daily Standups (15 minutes)
**Focus**: Progress, blockers, dependencies

**Format**:
- Each team member shares:
  - What I completed yesterday
  - What I'm working on today
  - Any blockers or dependencies
- Keep it timeboxed and focused
- Defer detailed discussions to after standup

**Best practices**:
- Use project board as visual guide
- Flag blockers early for quick resolution
- Highlight cross-team dependencies
- Take detailed discussions offline

### Weekly Delivery Sync (30-45 minutes)
**Focus**: Show progress, updates, and flagged risks

**Agenda**:
- Demo completed work
- Review project board and upcoming priorities
- Review risk register and top 3 risks
- Discuss any scope or timeline adjustments
- Address cross-team coordination needs

**Attendees**: Delivery team + PM + Product Manager

### Demo/Review (End of sprint or milestone)
**Focus**: Showcase work and gather feedback

**Agenda**:
- Demo new features or improvements
- Gather stakeholder feedback
- Review acceptance criteria completion
- Discuss any changes for next iteration

**Attendees**: Team + stakeholders + sponsors (as appropriate)

## Workflows

### Project Board Setup
**Columns**: Backlog → Ready → In Progress → In Review → QA → Done

**Column definitions**:
- **Backlog**: All work items, prioritized from top to bottom
- **Ready**: Items with clear acceptance criteria, ready to start
- **In Progress**: Actively being worked on (limit WIP)
- **In Review**: Code review in progress
- **QA**: Testing and validation in progress
- **Done**: Meets Definition of Done, deployed to staging/production

**Board hygiene**:
- Update status daily (in or before standup)
- Limit work-in-progress to maintain flow
- Move items left-to-right only (no rework without discussion)
- Archive completed items weekly or monthly

### Pull Request Workflow

#### PR Size Guidelines
- **Target**: ≤ 400 lines of changes
- **Small PRs** (<200 lines): Fast review, low risk
- **Medium PRs** (200-400 lines): Standard review
- **Large PRs** (>400 lines): Break down if possible or schedule deep review

**Benefits of small PRs**:
- Faster review cycles
- Easier to understand and test
- Lower risk of introducing bugs
- Simpler to rollback if needed

#### PR Best Practices

**Before creating PR**:
- [ ] Ensure code meets Definition of Done
- [ ] Run all tests locally and verify they pass
- [ ] Run linter and fix any issues
- [ ] Self-review the diff for obvious issues

**PR Description must include**:
- Link to issue (e.g., "Closes #123")
- Summary of changes and approach
- Acceptance criteria checklist (copied from issue)
- Screenshots/videos for UI changes
- Testing performed
- Any deployment notes or considerations

**PR template example**:
```markdown
## Description
[Brief description of what this PR does]

Closes #[issue-number]

## Changes
- [List key changes]

## Acceptance Criteria
- [ ] [Criterion 1 from issue]
- [ ] [Criterion 2 from issue]

## Testing
- [ ] Unit tests added/updated
- [ ] Integration tests pass
- [ ] Manual testing completed
- [ ] Edge cases considered

## Screenshots
[If applicable]

## Deployment Notes
[Any special considerations for deployment]
```

#### Review Process
- Request review from at least one team member
- Address review comments promptly
- Resolve conversations explicitly
- Require at least one approval before merging (or team-defined policy)
- Squash or rebase commits per team convention

#### After Merge
- Delete feature branch (if not auto-deleted)
- Verify deployment to staging/production
- Update issue/project board status
- Monitor for any errors or issues

## Quality & Testing

### Testing Strategy
Ensure comprehensive coverage at multiple levels:

#### Unit Tests
- **Purpose**: Test individual functions/methods in isolation
- **Coverage target**: 80%+ for new code
- **When**: Written alongside implementation
- **Ownership**: Developer writing the feature

#### Integration Tests
- **Purpose**: Test interaction between components/services
- **Coverage**: Critical integration points and APIs
- **When**: Before merge for features involving multiple components
- **Ownership**: Developer or QA depending on complexity

#### End-to-End (E2E) Tests
- **Purpose**: Test critical user flows from start to finish
- **Coverage**: Happy path and critical edge cases
- **When**: Before release for changes to critical flows
- **Ownership**: QA or dedicated test engineer

#### Manual QA
- **Purpose**: Exploratory testing, UX validation, edge cases
- **When**: Feature acceptance testing before marking Done
- **What to test**:
  - Feature meets acceptance criteria
  - Edge cases and error handling
  - Cross-browser/device compatibility (if applicable)
  - Accessibility requirements
  - Performance under realistic conditions

### Testing Checklist (per feature)
- [ ] Unit tests written and passing (80%+ coverage)
- [ ] Integration tests added where applicable
- [ ] E2E tests updated for critical flows
- [ ] Manual testing completed against acceptance criteria
- [ ] Edge cases and error scenarios tested
- [ ] Performance impact assessed
- [ ] Security scanning passed (SAST/DAST)
- [ ] Accessibility review completed (if UI changes)

### Continuous Integration (CI)
**Required checks before merge**:
- [ ] All automated tests passing
- [ ] Linting rules satisfied
- [ ] Security scans passed (no high/critical vulnerabilities)
- [ ] Code coverage maintained or improved
- [ ] Build successful

**CI best practices**:
- Keep CI runs fast (<10 minutes when possible)
- Fail fast on critical issues
- Provide clear error messages
- Run most critical tests first

## Reporting & Metrics

### Key Metrics to Track

#### Velocity and Throughput
- **Story points completed per sprint** (if using points)
- **Number of items completed per week**
- **Trend over time** to predict capacity

#### Cycle Time
- **Time from start to Done** for work items
- **Target**: Minimize cycle time while maintaining quality
- **Use**: Identify bottlenecks in workflow

#### Burndown
- **Remaining work vs. time** for sprint or milestone
- **Use**: Track progress toward deadline
- **Red flag**: Burndown not trending toward zero

#### Quality Metrics
- **Test coverage percentage**
- **Number of bugs found in production** (escaped defects)
- **Time to resolve bugs**
- **CI failure rate**

#### Success Metrics (from Project Charter)
- Track the specific KPIs identified in project initiation
- Review monthly or at milestones
- Use to validate impact and iterate

### Dashboards
**Project dashboard should include**:
- Current sprint/milestone progress
- Top 3 risks and status
- Blockers requiring attention
- Key metrics (velocity, burndown, quality)
- Links to important documents

**Monitoring dashboard** (for released features):
- Error rates and latency
- Usage metrics and adoption
- User feedback and support tickets
- Performance metrics (if applicable)

### Status Reporting

**Weekly status update** (see Communication doc for template):
- Progress this week
- Next steps and priorities
- Risks & blockers
- Asks / decisions needed
- Key metrics snapshot

**Monthly stakeholder report**:
- Milestone progress and timeline
- Feature delivery summary
- Success metrics review
- Upcoming priorities
- Resource or support needs

## Blocker Escalation

### Escalation Levels
(See [Risk Management & Communication](octoacme-risks-and-communication.md) for detailed escalation paths)

#### Level 1: Team-level Triage
**When**: Blockers that can be resolved within the team
- Raise in daily standup
- Team discusses and assigns owner
- Expected resolution: 1-2 days

#### Level 2: PM Escalation
**When**: Cross-team dependencies, resource constraints, scope issues
- PM escalates to Product Lead and dependent teams
- Joint discussion to determine approach
- Expected resolution: 3-5 days

#### Level 3: Sponsor-level Escalation
**When**: Business-impacting issues, major timeline/budget impacts
- Executive decision or resources needed
- Present with impact analysis and options
- Resolution timeline varies

### Identifying Blockers Early
**Signs of a blocker**:
- Work item stuck in same status >2 days
- Waiting on external team with no response
- Technical issue with no clear path forward
- Resource unavailability affecting timeline
- Unclear requirements or acceptance criteria

**Don't wait to escalate**:
- Escalate as soon as you realize it's a blocker
- Come with context and if possible, suggested solutions
- Update stakeholders on impact and ETA

## Execution Checklist

### Sprint/Iteration Start
- [ ] Sprint goal clearly defined
- [ ] Backlog prioritized and sized appropriately
- [ ] Team capacity confirmed and respected
- [ ] All items have clear acceptance criteria
- [ ] Dependencies identified and coordinated
- [ ] Definition of Done reviewed and agreed

### Daily/Ongoing
- [ ] Project board updated daily (before or during standup)
- [ ] Blockers raised and addressed promptly
- [ ] PRs reviewed within 24 hours
- [ ] Tests passing in CI before merge
- [ ] Risk register reviewed weekly
- [ ] Status updates sent on schedule

### Sprint/Iteration End
- [ ] Demo prepared and conducted
- [ ] Acceptance criteria validated for all completed items
- [ ] Incomplete items moved to next sprint or backlog
- [ ] Retrospective scheduled and conducted
- [ ] Metrics reviewed and documented
- [ ] Next sprint/iteration planned

### Project Setup (One-time)
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Project board created with appropriate columns
- [ ] Definition of Done documented
- [ ] Regular demos scheduled (recurring calendar invite)
- [ ] Risk register template set up
- [ ] Communication plan established

---

## Definition of Done Template

Each project should define its own Definition of Done. Include criteria such as:

**Code Complete**:
- [ ] Feature implemented per acceptance criteria
- [ ] Code reviewed and approved
- [ ] No unresolved review comments
- [ ] Follows coding standards and conventions

**Testing Complete**:
- [ ] Unit tests written and passing (80%+ coverage)
- [ ] Integration tests added/updated where applicable
- [ ] Manual QA completed and documented
- [ ] Edge cases tested
- [ ] Security scans passed

**Documentation Complete**:
- [ ] Code comments added for complex logic
- [ ] API documentation updated (if applicable)
- [ ] User-facing documentation updated
- [ ] Release notes entry added

**Ready for Release**:
- [ ] Deployed to staging and verified
- [ ] Performance acceptable
- [ ] No critical bugs
- [ ] Stakeholder approval received (if required)
- [ ] Rollback plan documented

**Customize this checklist** based on your project's specific requirements and context.
