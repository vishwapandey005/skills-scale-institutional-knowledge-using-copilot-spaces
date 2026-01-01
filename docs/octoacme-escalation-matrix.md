# OctoAcme — Escalation Matrix

## Purpose
Provide clear escalation paths for different types of issues, risks, and decisions. This ensures timely resolution and appropriate involvement of stakeholders based on impact and urgency.

## Escalation Principles
- Escalate early when you identify issues that exceed your authority or expertise
- Always inform your immediate manager before escalating beyond them
- Document the issue and attempted resolutions before escalating
- Use the appropriate escalation path based on issue type and severity

## Escalation Levels

### Level 1: Team-Level Resolution
**When to use:** Day-to-day technical blockers, minor delays, clarification needs

**Escalation path:**
1. Raise in daily standup
2. Team members collaborate on solution
3. Project Manager facilitates if needed

**Response time:** Same day or next standup

**Examples:**
- Waiting on code review
- Clarification on acceptance criteria
- Local environment issues
- Minor scope questions

### Level 2: Project Manager / Lead Escalation
**When to use:** Issues affecting sprint goals, cross-team dependencies, resource conflicts

**Escalation path:**
1. Developer/QA Lead/Release Manager → Project Manager
2. Project Manager coordinates with relevant leads
3. Project Manager updates stakeholders

**Response time:** Within 24 hours

**Examples:**
- Sprint goal at risk
- Resource shortage or competing priorities
- Cross-team dependency blockers
- Quality issues requiring scope adjustment
- Moderate technical risks identified by Technical Architect

### Level 3: Product Lead / Sponsor Escalation
**When to use:** Issues affecting project timeline, scope changes, budget impacts

**Escalation path:**
1. Project Manager → Product Manager
2. Product Manager → Product Lead / Sponsor
3. Decision communicated back to team

**Response time:** Within 2 business days

**Examples:**
- Milestone at risk
- Significant scope change needed
- Budget overrun or resource reallocation
- Strategic priority conflicts
- Customer escalation from Support/Customer Advocate

### Level 4: Executive / Crisis Escalation
**When to use:** Production incidents, security breaches, major customer impact

**Escalation path:**
1. On-call → Incident Commander
2. Incident Commander → Executive on-call
3. Crisis response team activated

**Response time:** Immediate (within 1 hour)

**Examples:**
- Production outage affecting customers
- Security incident or data breach
- Major customer contract at risk
- Regulatory compliance issue

## Escalation by Issue Type

### Technical Issues

| Issue Type | First Contact | Escalation Path |
|------------|--------------|-----------------|
| Architecture decision | Technical Architect | Tech Architect → Engineering Lead → CTO |
| Technical debt blocking feature | Developer → Project Manager | PM → Product Manager → Product Lead |
| Security vulnerability | Developer → Security Team | Security → CISO → Executive Team |
| Performance degradation | Developer → QA Lead | QA Lead → Technical Architect → Engineering Lead |
| Third-party dependency issue | Developer → Technical Architect | Tech Architect → PM → Vendor escalation |

### Quality Issues

| Issue Type | First Contact | Escalation Path |
|------------|--------------|-----------------|
| Test coverage concerns | QA Lead → Developers | QA Lead → Project Manager → Engineering Lead |
| Release quality gate failure | QA Lead → Project Manager | PM → Product Manager → Delay decision |
| Production bug | Support → QA Lead | QA Lead → PM → Product Manager (priority decision) |
| Regression in critical flow | QA Lead → Developers | QA Lead → PM → Emergency fix process |

### Release and Deployment Issues

| Issue Type | First Contact | Escalation Path |
|------------|--------------|-----------------|
| Deployment failure | Release Manager → On-call | Release Manager → Incident Response |
| Release timeline at risk | Release Manager → Project Manager | PM → Product Manager → Stakeholder notification |
| Rollback decision | Release Manager → Technical Architect | Release Manager → Incident Commander |
| Production access issues | Release Manager → IT/DevOps | Release Manager → PM → Engineering Lead |

### Customer and Support Issues

| Issue Type | First Contact | Escalation Path |
|------------|--------------|-----------------|
| Customer-reported bug | Support/Customer Advocate → QA Lead | QA Lead → PM → Product Manager (priority) |
| Feature request escalation | Support/Customer Advocate → Product Manager | PM → Product Lead → Roadmap decision |
| Customer satisfaction issue | Support/Customer Advocate → Product Manager | PM → Product Lead → Executive |
| Service outage impact | Support/Customer Advocate → Release Manager | Release Manager → Incident Response |
| Customer contract risk | Support/Customer Advocate → Account Manager | Account Manager → Sales Lead → Executive |

### Project Management Issues

| Issue Type | First Contact | Escalation Path |
|------------|--------------|-----------------|
| Sprint goal at risk | Project Manager → Team | PM → Product Manager → Scope adjustment |
| Resource conflict | Project Manager → Engineering Lead | PM → Product Lead → Resource allocation decision |
| Stakeholder misalignment | Project Manager → Product Manager | PM + PdM → Stakeholders → Alignment meeting |
| Timeline slippage | Project Manager → Product Manager | PM → Product Lead → Sponsor → Communication plan |

## Communication Templates

### Escalation Email Template
```
Subject: [ESCALATION] [Severity] - Brief Issue Description

Issue Summary:
[One paragraph describing the problem]

Impact:
[What is affected - customers, timeline, quality, etc.]

Actions Taken:
[What has been tried so far]

Requested Action:
[What decision or help is needed]

Timeline:
[Urgency - when is decision needed]

Context:
[Links to relevant docs, tickets, or discussions]
```

### Escalation Meeting Request Template
```
Subject: Urgent: [Issue] - Decision Needed

Meeting purpose: [Decision or resolution needed]
Duration: [30 min suggested]
Required attendees: [List by role]
Optional attendees: [List by role]

Pre-read:
[Link to issue summary document]

Agenda:
1. Issue summary (5 min)
2. Options analysis (10 min)
3. Decision (10 min)
4. Next steps (5 min)
```

## Decision Authority Matrix

| Decision Type | Authority Level | Typical Role |
|--------------|----------------|--------------|
| Code implementation approach | Team level | Developers + Technical Architect |
| Test strategy changes | Team level | QA Lead + Project Manager |
| Sprint scope adjustment | Project level | Project Manager + Product Manager |
| Release go/no-go | Project level | Release Manager + QA Lead + PM |
| Feature prioritization | Product level | Product Manager |
| Timeline extension | Product level | Product Manager + Product Lead |
| Budget changes | Executive level | Sponsor + Finance |
| Security exception | Executive level | CISO |

## Escalation Best Practices

### Do's
- ✅ Document the issue clearly before escalating
- ✅ Bring data and context to support your escalation
- ✅ Propose potential solutions or options
- ✅ Be specific about what decision or help is needed
- ✅ Set clear timelines for when a decision is needed
- ✅ Follow up to close the loop after escalation is resolved
- ✅ Update relevant documentation with the decision

### Don'ts
- ❌ Skip levels without informing intermediate managers
- ❌ Escalate without attempting team-level resolution first
- ❌ Escalate emotional issues without cooling down first
- ❌ Use escalation as a threat or manipulation
- ❌ Escalate trivial issues that can be resolved at team level
- ❌ Forget to update stakeholders on resolution

## Integration with Other Processes

This escalation matrix integrates with:
- **Risk Management** ([Risk Management & Communication](octoacme-risks-and-communication.md)) - Risks should be escalated when mitigation fails
- **Incident Response** - Production incidents follow crisis escalation path
- **Release Process** ([Release & Deployment Guide](octoacme-release-and-deployment.md)) - Release issues follow deployment escalation paths
- **Project Planning** ([Project Planning](octoacme-project-planning.md)) - Planning issues escalate through PM → Product chain

## Feedback and Improvements

If you find this escalation matrix unclear or encounter a situation not covered here, please raise it in your retrospective or provide feedback to your Project Manager. We continuously refine these paths based on real-world usage.
