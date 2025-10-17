# Operational Workflows Automation

> AI-powered automation for operations, monitoring, and incident management

## Table of Contents

1. [Incident Management](#incident-management)
2. [Monitoring & Alerting](#monitoring--alerting)
3. [Documentation & Runbooks](#documentation--runbooks)
4. [Reporting & Analytics](#reporting--analytics)
5. [Process Automation](#process-automation)
6. [Infrastructure Management](#infrastructure-management)
7. [Compliance & Auditing](#compliance--auditing)
8. [Best Practices](#best-practices)

## Incident Management

### Incident Response Coordination

```
Coordinate incident response for:

INCIDENT: [Title/ID]
SEVERITY: [Critical/High/Medium/Low]
DETECTED AT: [Timestamp]

SITUATION:
- Affected systems: [list]
- User impact: [description]
- Error rates: [metrics]
- Recent changes: [deployments/config]

GENERATE:

## Incident Response Plan

### Immediate Actions (Next 5 minutes)
1. [Action 1]: [Owner]
2. [Action 2]: [Owner]
3. [Action 3]: [Owner]

### Team Assembly
- **Incident Commander**: [Name]
- **Technical Lead**: [Name]
- **Communications**: [Name]
- **Support**: [Names]

### Communication Plan
- **Internal**: [Slack channel #incident-xxx]
- **Stakeholders**: [List to notify]
- **Customers**: [Status page update template]

### Investigation Strategy
1. **Check First**:
   - Logs: [which systems]
   - Metrics: [which dashboards]
   - Recent changes: [deployment history]

2. **Hypotheses** (in order of likelihood):
   - H1: [Hypothesis and how to test]
   - H2: [Hypothesis and how to test]
   - H3: [Hypothesis and how to test]

3. **Diagnostic Commands**:
   ```bash
   [Command 1 to check system state]
   [Command 2 to check logs]
   [Command 3 to check metrics]
   ```

### Rollback Plan
If needed:
- [ ] Identify safe rollback point
- [ ] Prepare rollback command
- [ ] Communicate intention
- [ ] Execute rollback
- [ ] Verify recovery

### Success Criteria
- [ ] Error rate < [threshold]
- [ ] Response time < [threshold]
- [ ] All core features operational
- [ ] Customer communication sent

### Next Update
Schedule next status update in: [timeframe]
```

**Use Case**: Real-time incident coordination and response planning.

---

### Post-Incident Review

```
Generate post-incident review for:

INCIDENT: [Title]
DATE: [Date]
DURATION: [Hours:Minutes]
SEVERITY: [Level]

TIMELINE:
[Paste detailed timeline of events]

ROOT CAUSE:
[Describe identified root cause]

RESOLUTION:
[Describe how it was resolved]

GENERATE:

# Post-Incident Review

## Executive Summary
[3-4 sentences for leadership: what happened, impact, resolution, prevention]

## Incident Details

| Attribute | Value |
|-----------|-------|
| Incident ID | [ID] |
| Start Time | [Timestamp] |
| Detection Time | [Timestamp] |
| Resolution Time | [Timestamp] |
| Total Duration | [Duration] |
| Severity | [Level] |
| Incident Commander | [Name] |

## Impact Assessment

### User Impact
- **Users Affected**: [Number/Percentage]
- **Services Impacted**: [List]
- **Degradation Level**: [Complete outage/Partial/Degraded]
- **Customer Complaints**: [Number]

### Business Impact
- **Revenue Impact**: [If applicable]
- **SLA Impact**: [Breach status]
- **Reputation Impact**: [Assessment]
- **Recovery Time**: [Actual vs. Target]

## What Happened

### Detection
- **How Detected**: [Monitoring alert/User report/Other]
- **Time to Detect**: [Minutes from start to detection]
- **Detection Quality**: [Good/Could improve]

### Timeline of Events
[Detailed minute-by-minute or hour-by-hour timeline]

**Example Format**:
- **14:30 UTC**: Initial alerts triggered for elevated error rates
- **14:32 UTC**: On-call engineer acknowledged alert
- **14:35 UTC**: Incident chat room created, team assembled
- **14:45 UTC**: Root cause identified (database connection pool exhaustion)
- **15:00 UTC**: Mitigation deployed (increased connection pool size)
- **15:15 UTC**: Service recovered, monitoring for stability
- **15:30 UTC**: Confirmed resolution, incident marked as resolved

### Root Cause Analysis

**Immediate Cause**:
[What directly triggered the incident]

**Contributing Factors**:
1. [Factor 1: e.g., Insufficient connection pool sizing]
2. [Factor 2: e.g., Unexpected traffic spike]
3. [Factor 3: e.g., Missing alerting on pool exhaustion]

**Why It Wasn't Caught Earlier**:
[Analysis of prevention and detection gaps]

### Resolution

**Immediate Mitigation**:
[Quick fix to restore service]

**Permanent Solution**:
[Long-term fix to prevent recurrence]

**Verification**:
[How we confirmed the fix worked]

## Analysis

### What Went Well
- ✅ [Positive aspect 1, e.g., Quick detection and alerting]
- ✅ [Positive aspect 2, e.g., Effective team coordination]
- ✅ [Positive aspect 3, e.g., Clear communication with stakeholders]

### What Went Poorly
- ❌ [Issue 1, e.g., Delayed root cause identification]
- ❌ [Issue 2, e.g., Unclear rollback procedures]
- ❌ [Issue 3, e.g., Insufficient monitoring]

### Lessons Learned
1. [Learning 1]
   - **Context**: [Situation]
   - **Lesson**: [What we learned]
   - **Application**: [How to apply going forward]

2. [Learning 2]
3. [Learning 3]

## Prevention Measures

### Technical Improvements
| Improvement | Description | Priority | Effort | Owner | Due Date |
|-------------|-------------|----------|--------|-------|----------|
| [Improvement 1] | [Details] | P0/P1/P2 | S/M/L | [Name] | [Date] |

### Process Improvements
| Improvement | Description | Priority | Effort | Owner | Due Date |
|-------------|-------------|----------|--------|-------|----------|
| [Improvement 1] | [Details] | P0/P1/P2 | S/M/L | [Name] | [Date] |

### Monitoring & Alerting
| Enhancement | Description | Priority | Effort | Owner | Due Date |
|-------------|-------------|----------|--------|-------|----------|
| [Enhancement 1] | [Details] | P0/P1/P2 | S/M/L | [Name] | [Date] |

## Action Items

### Prevention (Keep it from happening)
- [ ] [Action 1]
- [ ] [Action 2]

### Detection (Find it faster next time)
- [ ] [Action 1]
- [ ] [Action 2]

### Mitigation (Reduce impact if it happens)
- [ ] [Action 1]
- [ ] [Action 2]

## Supporting Information
- Incident Channel: [Link]
- Metrics Dashboard: [Link]
- Related Tickets: [Links]
- Code Changes: [PR links]

---

**Review Date**: [30 days from incident]
**Reviewers**: [Names]
```

**Use Case**: Comprehensive post-mortem documentation and learning.

---

## Monitoring & Alerting

### Alert Configuration

```
Create monitoring alert configuration for:

SERVICE: [Service name]
METRIC: [What to monitor]
OBJECTIVE: [What you're trying to detect]

GENERATE:

## Alert Configuration

### Alert Definition

**Alert Name**: [Descriptive name]

**Description**: [What this alert detects and why it matters]

**Metric**:
```yaml
metric: [metric name]
aggregation: [sum/average/percentile]
dimensions:
  - [dimension1]
  - [dimension2]
```

**Threshold**:
- **Warning**: [value] for [duration]
- **Critical**: [value] for [duration]

**Evaluation**:
- Check interval: [frequency]
- Evaluation window: [time period]
- Data points to alarm: [number out of number]

### Alert Severity

**Severity Level**: [Critical/High/Medium/Low]

**Criteria**:
- **Critical**: [When to page someone]
- **High**: [When to create ticket immediately]
- **Medium**: [When to investigate within hours]
- **Low**: [Informational only]

### Response Procedures

**Immediate Actions**:
1. [First thing to check]
2. [Second thing to check]
3. [Third thing to check]

**Investigation Steps**:
```bash
# Check system status
[command 1]

# Check logs
[command 2]

# Check related metrics
[command 3]
```

**Escalation**:
- **Level 1**: [Team/Person, when to escalate]
- **Level 2**: [Manager/Senior, when to escalate]
- **Level 3**: [Director/Executive, when to escalate]

### Alert Routing

**Recipients**:
- **Primary**: [Team/Person]
- **Backup**: [Team/Person]
- **Notifications**: [Channels - Slack, PagerDuty, etc.]

**Schedule**:
- **Business hours**: [Recipients]
- **After hours**: [On-call rotation]
- **Weekends**: [On-call rotation]

### False Positive Prevention

**Common False Positives**:
1. [Scenario 1]: [How to distinguish]
2. [Scenario 2]: [How to distinguish]

**Filters**:
- Exclude: [Conditions to filter out]
- Include: [Conditions that must be present]

### Documentation Links
- Runbook: [Link]
- Dashboard: [Link]
- Related alerts: [Links]
- Past incidents: [Links]

### Alert Testing

**Test Scenario**:
```bash
# How to trigger this alert for testing
[Command or procedure]
```

**Expected Behavior**:
- Alert should fire within: [timeframe]
- Recipients should receive: [notification type]
- Alert should clear when: [condition]

### Review Schedule
- **Effectiveness Review**: [Frequency]
- **Threshold Tuning**: [Frequency]
- **Owner Review**: [Frequency]
```

**Use Case**: Creating effective, actionable monitoring alerts.

---

### Dashboard Creation

```
Design monitoring dashboard for:

SYSTEM: [System/Service name]
AUDIENCE: [Who will use this - engineers/ops/leadership]
PURPOSE: [What decisions this supports]

GENERATE:

## Dashboard Design

### Overview Section

**Purpose**: At-a-glance system health

**Metrics** (2-4 key indicators):
1. **[Metric 1]**: [e.g., Request Rate]
   - Visualization: [Single stat/Gauge/Graph]
   - Threshold indicators: [Good/Warning/Critical ranges]
   - Time range: [Last 24h/7d]

2. **[Metric 2]**: [e.g., Error Rate]
   - Visualization: [Type]
   - Alert: [When to show red]

3. **[Metric 3]**: [e.g., Response Time P99]
4. **[Metric 4]**: [e.g., System Availability]

### Performance Section

**Charts**:

1. **Request Latency**:
   - Lines: P50, P95, P99
   - Time range: Last 6 hours
   - Y-axis: Milliseconds
   - Alert threshold line: [value]

2. **Throughput**:
   - Metric: Requests per second
   - Aggregation: Sum
   - Visualization: Area chart
   - Comparison: vs. previous period

3. **Error Rates**:
   - Metric: Errors per minute
   - Breakdown: By error type
   - Visualization: Stacked area
   - Alert threshold: [value]

### Infrastructure Section

**System Resources**:

1. **CPU Usage**:
   - Metric: CPU percentage
   - Per: Host/Container
   - Visualization: Heatmap
   - Alert: > 80%

2. **Memory Usage**:
   - Metric: Memory percentage
   - Alert: > 85%

3. **Disk I/O**:
   - Metrics: Read/Write IOPS
   - Visualization: Line chart

4. **Network**:
   - Metrics: In/Out bandwidth
   - Unit: MB/s

### Application Section

**Business Metrics**:

1. **[Business Metric 1]**: [e.g., Active Users]
   - Current value
   - Trend: vs. yesterday, vs. last week
   - Visualization: Time series

2. **[Business Metric 2]**: [e.g., Conversion Rate]
3. **[Business Metric 3]**: [e.g., Revenue Impact]

### Dependency Section

**External Services**:

For each dependency:
- Health status: [Green/Yellow/Red]
- Response time: [P99]
- Error rate: [%]
- Last successful call: [Timestamp]

### Alerts Section

**Active Alerts**:
- List of firing alerts
- Severity
- Duration
- Affected components

### Dashboard Features

**Time Controls**:
- Default: Last 1 hour
- Quick ranges: 15m, 1h, 6h, 24h, 7d
- Custom range picker
- Auto-refresh: Every 30s

**Filters**:
- Environment: [Production/Staging/Dev]
- Region: [All/Specific]
- Component: [All/Specific]

**Variables**:
- `$service`: Service selector
- `$host`: Host selector
- `$environment`: Environment selector

### Panel Layout

```
Row 1: System Health (4 single-stat panels)
[Availability] [Error Rate] [Latency P99] [Request Rate]

Row 2: Performance (2 panels)
[Latency Graph - Full Width] [Throughput - Full Width]

Row 3: Resources (4 panels)
[CPU] [Memory] [Disk] [Network]

Row 4: Business Metrics (3 panels)
[Metric 1] [Metric 2] [Metric 3]

Row 5: Dependencies (1 table panel)
[External Services Status]

Row 6: Alerts (1 panel)
[Active Alerts List]
```

### Annotations

Add annotations for:
- Deployments
- Configuration changes
- Known issues
- Maintenance windows

### Usage Guidelines

**How to Read This Dashboard**:
1. [Instruction 1: Start with overview]
2. [Instruction 2: Check for red/yellow indicators]
3. [Instruction 3: Drill into problem areas]

**Common Patterns**:
- **High CPU + High Latency**: [Likely cause and action]
- **High Error Rate**: [Where to look first]
- **Memory Growth**: [What to check]
```

**Use Case**: Designing effective monitoring dashboards for different audiences.

---

## Documentation & Runbooks

### Runbook Creation

```
Create operational runbook for:

PROCEDURE: [Procedure name]
FREQUENCY: [How often performed]
COMPLEXITY: [Simple/Medium/Complex]

GENERATE:

# Runbook: [Procedure Name]

## Overview

**Purpose**: [What this procedure accomplishes]

**When to Use**: [Scenarios for using this runbook]

**Frequency**: [How often this is performed]

**Duration**: [Expected time to complete]

**Risk Level**: [Low/Medium/High]

## Prerequisites

### Access Required
- [ ] [System/Tool 1]: [Permission level]
- [ ] [System/Tool 2]: [Permission level]
- [ ] [System/Tool 3]: [Permission level]

### Knowledge Required
- [Skill/Knowledge 1]
- [Skill/Knowledge 2]

### Tools Needed
- [Tool 1]: [Version/Access URL]
- [Tool 2]: [Version/Access URL]

### Pre-flight Checks
- [ ] [Condition 1 must be true]
- [ ] [Condition 2 must be true]
- [ ] [Backup/Safety measure taken]

## Procedure

### Step 1: [Step Name]

**What**: [What you're doing in this step]

**Why**: [Why this step is necessary]

**How**:
```bash
# [Explanation of command]
[command to execute]
```

**Expected Output**:
```
[What you should see]
```

**If Something Goes Wrong**:
- **Symptom**: [What you might see]
- **Cause**: [Likely reason]
- **Fix**: [What to do]

**Duration**: ~[X minutes]

**Safety Notes**: [Any warnings or cautions]

---

### Step 2: [Step Name]

[Same structure as Step 1]

---

[Continue for all steps]

## Verification

Check that the procedure was successful:

- [ ] **Check 1**: [How to verify]
  ```bash
  [Verification command]
  ```
  Expected: [Result]

- [ ] **Check 2**: [How to verify]
- [ ] **Check 3**: [How to verify]

## Rollback Procedure

If things go wrong, follow these steps to undo changes:

### When to Rollback
- [Condition 1]
- [Condition 2]

### Rollback Steps

1. **[Rollback Step 1]**:
   ```bash
   [Rollback command]
   ```

2. **[Rollback Step 2]**:
3. **[Rollback Step 3]**:

### Verify Rollback
- [ ] [Check system is in pre-procedure state]
- [ ] [Check no lasting side effects]

## Troubleshooting

### Issue 1: [Common Problem]

**Symptoms**:
- [What you'll see]

**Cause**:
- [Why it happens]

**Solution**:
```bash
[Fix command or procedure]
```

### Issue 2: [Common Problem]
[Same structure]

## Success Criteria

The procedure is successful when:
- [ ] [Measurable outcome 1]
- [ ] [Measurable outcome 2]
- [ ] [No errors in logs]
- [ ] [Monitoring shows healthy state]

## Post-Procedure Tasks

- [ ] Update change log: [Where]
- [ ] Notify stakeholders: [Who]
- [ ] Update documentation: [If procedure changed]
- [ ] File post-execution report: [If required]

## Emergency Contacts

**Primary Contact**:
- Name: [Name]
- Role: [Role]
- Contact: [Phone/Email/Slack]

**Escalation**:
- Name: [Name]
- Role: [Role]
- Contact: [Phone/Email/Slack]

**After Hours**:
- On-call: [How to reach]
- Emergency: [Escalation path]

## References

- **Related Runbooks**: [Links]
- **System Documentation**: [Links]
- **Architecture Diagrams**: [Links]
- **Previous Executions**: [Ticket/Log links]
- **Change Tickets**: [Links]

## Runbook Metadata

| Attribute | Value |
|-----------|-------|
| **Owner** | [Name/Team] |
| **Last Updated** | [Date] |
| **Last Executed** | [Date] |
| **Success Rate** | [X/Y executions] |
| **Next Review** | [Date] |
| **Version** | [Version number] |

## Change History

| Date | Version | Changes | Author |
|------|---------|---------|--------|
| [Date] | [v1.0] | [Changes] | [Name] |

## Testing

**How to Test This Runbook**:
1. [Test in non-prod environment]
2. [Specific test scenarios]
3. [Validation steps]

**Last Tested**: [Date]
**Test Results**: [Pass/Fail, notes]
```

**Use Case**: Creating comprehensive, executable runbooks for operations teams.

---

### SOP (Standard Operating Procedure) Template

```
Create Standard Operating Procedure for:

PROCESS: [Process name]
SCOPE: [What this covers]
DEPARTMENT: [Who uses this]

GENERATE:

# Standard Operating Procedure

## Document Control

| Attribute | Value |
|-----------|-------|
| **SOP ID** | [Unique identifier] |
| **Title** | [Process name] |
| **Department** | [Department] |
| **Effective Date** | [Date] |
| **Review Date** | [Date] |
| **Version** | [Version] |
| **Owner** | [Name/Role] |
| **Approved By** | [Name/Role] |

## Purpose

[2-3 sentences explaining why this SOP exists and what it accomplishes]

## Scope

**Applies To**:
- [Team/Department 1]
- [Team/Department 2]

**Does Not Apply To**:
- [Exclusions]

## Definitions

| Term | Definition |
|------|------------|
| [Term 1] | [Definition] |
| [Term 2] | [Definition] |

## Roles and Responsibilities

| Role | Responsibilities |
|------|------------------|
| [Role 1] | [What they're responsible for] |
| [Role 2] | [What they're responsible for] |

## Procedure

### [Process Step 1]

**Responsible**: [Role]
**Frequency**: [When performed]

**Steps**:
1. [Action 1]
   - Details: [Explanation]
   - Tools: [What to use]
   - Documentation: [What to record]

2. [Action 2]
3. [Action 3]

**Deliverable**: [What output is produced]

**Quality Checks**:
- [ ] [Check 1]
- [ ] [Check 2]

---

### [Process Step 2]

[Same structure]

---

## Quality Standards

**Acceptance Criteria**:
- [Criterion 1]
- [Criterion 2]

**Key Performance Indicators**:
- [KPI 1]: [Target]
- [KPI 2]: [Target]

**Compliance Requirements**:
- [Requirement 1]
- [Requirement 2]

## Documentation Requirements

**Required Records**:
- [Record 1]: [Where stored, retention period]
- [Record 2]: [Where stored, retention period]

**Templates**:
- [Template 1]: [Link]
- [Template 2]: [Link]

## Training Requirements

**Required Training**:
- [Training 1]: [Before performing task]
- [Training 2]: [Annual refresher]

**Competency Assessment**:
- [How competency is verified]

## Risk Management

**Potential Risks**:
| Risk | Impact | Mitigation |
|------|--------|------------|
| [Risk 1] | [High/Med/Low] | [How to prevent/handle] |

## Exception Handling

**When to Deviate**:
- [Scenario 1]: [Approval required from whom]
- [Scenario 2]: [Process to follow]

**Exception Documentation**:
- [What must be recorded]
- [Where to record it]

## Related Documents

- [Related SOP 1]
- [Related Policy 1]
- [Related Form 1]

## Review and Revision

**Review Schedule**: [Frequency]

**Review Triggers**:
- [Change in regulation]
- [System change]
- [Process improvement identified]

**Revision History**:
| Version | Date | Changes | Author |
|---------|------|---------|--------|
| [v1.0] | [Date] | [Initial creation] | [Name] |

## Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| [Preparer] | [Name] | | [Date] |
| [Reviewer] | [Name] | | [Date] |
| [Approver] | [Name] | | [Date] |
```

**Use Case**: Formal operational procedures for compliance and standardization.

---

## Reporting & Analytics

### Operational Report Template

```
Generate operational report for:

PERIOD: [Time period]
TEAM/SYSTEM: [What's being reported on]
AUDIENCE: [Who will read this]

DATA:
[Paste or describe available metrics and data]

GENERATE:

# [Period] Operations Report

**Report Date**: [Date]
**Reporting Period**: [Start Date] - [End Date]
**Prepared By**: [Name/Team]

## Executive Summary

[3-4 paragraphs summarizing key points, changes, and priorities]

## Key Metrics

### System Health

| Metric | Current Period | Previous Period | Change | Target | Status |
|--------|---------------|-----------------|--------|--------|--------|
| Uptime | [99.9%] | [99.8%] | [+0.1%] | [99.9%] | ✅ |
| Availability | [99.95%] | [99.90%] | [+0.05%] | [99.9%] | ✅ |
| MTTR | [15 min] | [20 min] | [-25%] | [<30 min] | ✅ |
| MTBF | [720 hrs] | [600 hrs] | [+20%] | [>500 hrs] | ✅ |

### Performance Metrics

| Metric | Current | Previous | Change | Target | Status |
|--------|---------|----------|--------|--------|--------|
| Avg Response Time | [145ms] | [160ms] | [-9%] | [<200ms] | ✅ |
| P99 Response Time | [650ms] | [750ms] | [-13%] | [<1000ms] | ✅ |
| Request Rate | [12.5M/day] | [11.8M/day] | [+6%] | [Growth] | ✅ |
| Error Rate | [0.3%] | [0.4%] | [-25%] | [<0.5%] | ✅ |

### Business Metrics

| Metric | Current | Previous | Change | Target | Status |
|--------|---------|----------|--------|--------|--------|
| Active Users | [45,678] | [43,210] | [+5.7%] | [Growth] | ✅ |
| New Signups | [1,234] | [1,180] | [+4.6%] | [1,200] | ✅ |
| Conversion Rate | [3.2%] | [3.0%] | [+6.7%] | [>3%] | ✅ |

## Achievements & Highlights

### Major Accomplishments

✅ **[Achievement 1]**: [Description]
- **Impact**: [What improved]
- **Metrics**: [Quantifiable results]

✅ **[Achievement 2]**: [Description]
- **Impact**: [What improved]
- **Metrics**: [Quantifiable results]

✅ **[Achievement 3]**: [Description]

### System Improvements

- **Performance**: [Optimization completed]
  - Result: [Improvement in metrics]
  
- **Reliability**: [Enhancement made]
  - Result: [Impact on uptime/availability]
  
- **Cost**: [Cost reduction initiative]
  - Result: [Savings achieved]

## Incidents & Issues

### Incident Summary

**Total Incidents**: [Number]
- Critical: [Number]
- High: [Number]
- Medium: [Number]
- Low: [Number]

### Significant Incidents

#### Incident #1: [Title]
- **Date**: [Date and time]
- **Duration**: [Time]
- **Severity**: [Level]
- **Impact**: [Brief description]
- **Root Cause**: [Summary]
- **Status**: [Resolved/Mitigated]
- **Prevention**: [Action taken]

#### Incident #2: [Title]
[Same structure]

### Trends

- [Observation about incident patterns]
- [Recurring issues]
- [Improvement areas]

## Deployments & Changes

### Deployment Summary

**Total Deployments**: [Number]
- Successful: [Number] ([Percentage]%)
- Rolled back: [Number] ([Percentage]%)
- Emergency fixes: [Number]

### Significant Changes

| Date | Change | Type | Impact | Status |
|------|--------|------|--------|--------|
| [Date] | [Description] | [Feature/Fix/Config] | [High/Med/Low] | [Success/Rollback] |

### Change Success Rate

[Chart or metrics showing deployment reliability]

## In Progress & Planned

### Current Focus Areas

1. **[Initiative 1]**: [Description]
   - Status: [X% complete]
   - Expected completion: [Date]
   - Blocking issues: [If any]

2. **[Initiative 2]**: [Description]
3. **[Initiative 3]**: [Description]

### Upcoming Week

**Planned Activities**:
- [Activity 1]: [Date]
- [Activity 2]: [Date]
- [Activity 3]: [Date]

**Scheduled Maintenance**:
- [Maintenance 1]: [Date, Duration, Impact]

## Risks & Concerns

### Current Risks

⚠️ **[Risk 1]**: [Description]
- **Impact**: [High/Medium/Low]
- **Probability**: [High/Medium/Low]
- **Mitigation**: [Current plan]
- **Owner**: [Name]

⚠️ **[Risk 2]**: [Description]

### Technical Debt

- **[Tech Debt Item 1]**: [Description, Impact, Plan]
- **[Tech Debt Item 2]**: [Description, Impact, Plan]

## Resource Utilization

### Infrastructure

| Resource | Usage | Capacity | Utilization | Trend | Action Needed |
|----------|-------|----------|-------------|-------|---------------|
| Compute | [X units] | [Y units] | [Z%] | [↑↓→] | [Yes/No] |
| Storage | [X TB] | [Y TB] | [Z%] | [↑↓→] | [Yes/No] |
| Network | [X Gbps] | [Y Gbps] | [Z%] | [↑↓→] | [Yes/No] |

### Team Capacity

- **On-call shifts**: [Coverage status]
- **Available capacity**: [% of team time]
- **Unplanned work**: [% of time spent]

## Costs

### Infrastructure Costs

| Category | Current Month | Previous Month | Change | Budget | Status |
|----------|--------------|----------------|--------|--------|--------|
| Compute | [$X,XXX] | [$X,XXX] | [±X%] | [$X,XXX] | [✅/⚠️] |
| Storage | [$XXX] | [$XXX] | [±X%] | [$XXX] | [✅/⚠️] |
| Network | [$XXX] | [$XXX] | [±X%] | [$XXX] | [✅/⚠️] |
| **Total** | **[$X,XXX]** | **[$X,XXX]** | **[±X%]** | **[$X,XXX]** | **[✅/⚠️]** |

### Cost Optimization

- [Initiative 1]: [Savings achieved or projected]
- [Initiative 2]: [Savings achieved or projected]

## Recommendations

1. **[Recommendation 1]**:
   - **Reason**: [Why needed]
   - **Impact**: [Expected benefit]
   - **Effort**: [Resource requirement]
   - **Priority**: [High/Medium/Low]

2. **[Recommendation 2]**:
3. **[Recommendation 3]**:

## Appendix

### Detailed Metrics
[Link to detailed dashboards or reports]

### Supporting Documentation
[Links to incidents, change tickets, etc.]

### Glossary
| Term | Definition |
|------|------------|
| MTTR | Mean Time To Recovery |
| MTBF | Mean Time Between Failures |
| P99 | 99th percentile |

---

**Next Report**: [Date]
**Questions**: [Contact information]
```

**Use Case**: Regular operational reporting for stakeholders and management.

---

## Process Automation

### Automated Workflow Design

```
Design automated workflow for:

PROCESS: [Process name]
CURRENT STATE: [How it's done now]
PAIN POINTS: [What's inefficient]

GENERATE:

## Workflow Automation Design

### Process Overview

**Process Name**: [Name]

**Current Process**:
1. [Manual step 1]
2. [Manual step 2]
3. [Manual step 3]

**Pain Points**:
- [Pain point 1]: [Impact]
- [Pain point 2]: [Impact]

**Automation Goals**:
- Reduce time from [X] to [Y]
- Eliminate [Z] manual steps
- Improve accuracy to [target]%

### Automated Workflow

#### Trigger

**Event**: [What starts the workflow]

**Conditions**:
- [Condition 1 that must be true]
- [Condition 2 that must be true]

**Source**: [Where the trigger comes from]

#### Workflow Steps

**Step 1: [Automated Action]**
- **Action**: [What happens]
- **Tool/System**: [What performs it]
- **Input**: [Data needed]
- **Output**: [Data produced]
- **Error Handling**: [What happens if it fails]
- **Duration**: [Expected time]

**Step 2: [Decision Point]**
- **Condition**: [What's evaluated]
- **If True**: [Go to Step X]
- **If False**: [Go to Step Y]
- **Default**: [What happens if condition can't be evaluated]

**Step 3: [Automated Action]**
[Same structure as Step 1]

[Continue for all steps]

#### Completion

**Success Criteria**:
- [ ] [Criterion 1]
- [ ] [Criterion 2]

**Notifications**:
- **On Success**: [Who gets notified, how]
- **On Failure**: [Who gets notified, how]

**Output**:
- [What's produced by the workflow]
- [Where it's stored]

### Implementation

#### Tools Required

| Tool | Purpose | Cost | Integration Effort |
|------|---------|------|-------------------|
| [Tool 1] | [What it does] | [Cost] | [Effort] |
| [Tool 2] | [What it does] | [Cost] | [Effort] |

#### Integration Points

**System Integrations**:
- [System 1]: [API/Webhook/File]
- [System 2]: [Integration method]

**Data Flow**:
```
[Source] → [Transformation] → [Destination]
```

#### Configuration

```yaml
# Workflow configuration
workflow:
  name: [workflow-name]
  trigger:
    type: [event/schedule/manual]
    config: [configuration]
  steps:
    - name: [step-1]
      action: [action-type]
      parameters: [params]
```

### Error Handling

**Retry Logic**:
- Max retries: [number]
- Retry delay: [time]
- Backoff: [exponential/linear]

**Failure Actions**:
- [Failure scenario 1]: [What to do]
- [Failure scenario 2]: [What to do]

**Manual Intervention**:
- When required: [Conditions]
- Process: [How to handle]

### Monitoring

**Metrics to Track**:
- Execution count
- Success rate
- Average duration
- Error rate
- Cost per execution

**Alerts**:
- [Alert 1]: [Condition]
- [Alert 2]: [Condition]

**Dashboard**:
- [Metric 1 visualization]
- [Metric 2 visualization]

### Testing Plan

**Test Scenarios**:
1. Happy path
2. Error conditions
3. Edge cases
4. Load testing

**Test Data**:
- [Test data requirements]

**Validation**:
- [ ] [Validation 1]
- [ ] [Validation 2]

### Rollout Plan

**Phase 1: Pilot** ([Timeframe])
- Run in parallel with manual process
- Limited scope: [Criteria]
- Monitor and tune

**Phase 2: Gradual Rollout** ([Timeframe])
- Expand to [X]% of cases
- Continue manual process for edge cases
- Gather feedback

**Phase 3: Full Automation** ([Timeframe])
- 100% automated
- Manual process only for exceptions
- Full monitoring in place

### Success Metrics

**Before Automation**:
- Time: [X hours/days]
- Error rate: [Y%]
- Cost: [$Z]

**After Automation** (Target):
- Time: [A hours/days] ([B%] improvement)
- Error rate: [C%] ([D%] improvement)
- Cost: [$E] ([F%] savings)

### Maintenance

**Ongoing Tasks**:
- Monitor performance
- Update as systems change
- Review and optimize
- Handle exceptions

**Review Schedule**: [Frequency]

**Owner**: [Team/Person]
```

**Use Case**: Designing and documenting workflow automation.

---

## Best Practices

### 1. Incident Response

**Do**:
- ✅ Have clear runbooks
- ✅ Establish command structure
- ✅ Communicate proactively
- ✅ Document timeline during incident
- ✅ Conduct blameless post-mortems

**Don't**:
- ❌ Skip documentation
- ❌ Blame individuals
- ❌ Rush to conclusions
- ❌ Neglect communication
- ❌ Ignore prevention measures

### 2. Runbook Creation

**Effective Runbooks**:
- Clear step-by-step instructions
- Expected outputs documented
- Error handling included
- Recently tested
- Easy to find

**Avoid**:
- Assuming knowledge
- Skipping verification steps
- Outdated procedures
- Missing rollback plans

### 3. Monitoring & Alerting

**Good Alerts**:
- Actionable
- Appropriate severity
- Clear context
- Low false positive rate
- Linked to runbooks

**Alert Fatigue Prevention**:
- Tune thresholds
- Remove noisy alerts
- Aggregate related alerts
- Use proper severity levels

### 4. Documentation

**Documentation Standards**:
- Keep current
- Clear structure
- Searchable
- Version controlled
- Regularly reviewed

### 5. Automation

**Automation Principles**:
- Start small
- Test thoroughly
- Monitor closely
- Have fallbacks
- Document well

## Related Resources

- [Software Development Automation](../software-development/README.md)
- [Content Creation Automation](../content-creation/README.md)
- [Workflows Guide](../../workflows/README.md)
- [Templates Library](../../../templates/README.md)
- [Examples](../../../examples/README.md)
- [Best Practices](../../best-practices/README.md)

---

**Operationalize your workflows!** Use these prompts to create robust operational procedures and automation.
