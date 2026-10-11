# Email Campaign Operations Templates

This toolkit provides reusable templates for planning, executing, testing, and reporting on email marketing campaigns. The templates can be adapted to different marketing automation platforms, team structures, and B2B or B2C campaign requirements.

## 1. Campaign Brief Template

Use this template to document campaign objectives, audience requirements, ownership, dependencies, and success criteria before campaign production begins.

| Field | Details |
|---|---|
| Campaign name | [Enter campaign name] |
| Campaign objective | [Awareness, engagement, lead generation, conversion, retention, etc.] |
| Target audience | [Describe the intended audience or segment] |
| Exclusions and suppression rules | [Unsubscribed, ineligible, existing customers, or other exclusions] |
| Primary CTA | [Define the main action recipients should take] |
| Secondary CTA | [Optional supporting action] |
| Email and landing page requirements | [Assets, copy, forms, and destination URLs] |
| Personalization requirements | [Tokens, dynamic content, or conditional content] |
| Tracking requirements | [UTM parameters, campaign IDs, and conversion events] |
| Campaign owner | [Responsible person] |
| Reviewers and approvers | [Content, marketing operations, legal, or other stakeholders] |
| Planned deployment date and time | [Include time zone] |
| Success metrics | [Define primary and supporting KPIs] |
| Dependencies and risks | [List approvals, integrations, assets, or technical dependencies] |

## 2. Pre-Deployment QA Checklist

Complete the applicable checks before scheduling or sending a campaign.

### Content and Rendering
- [ ] Subject line and preheader reviewed.
- [ ] Email copy, spelling, grammar, and formatting checked.
- [ ] Images, alt text, and image rendering reviewed.
- [ ] Desktop and mobile rendering checked.
- [ ] Personalization tokens and dynamic content tested.
- [ ] Plain-text version reviewed where applicable.

### Links and Tracking
- [ ] All links and buttons tested.
- [ ] Landing pages and forms verified.
- [ ] UTM parameters and campaign tracking validated.
- [ ] Redirects and destination URLs checked.
- [ ] Conversion tracking verified where applicable.

### Audience and Configuration
- [ ] Target segment and estimated audience count validated.
- [ ] Suppression and exclusion rules confirmed.
- [ ] Consent, subscription status, and applicable privacy requirements checked.
- [ ] Sender name, sender address, and reply-to address verified.
- [ ] Send time, time zone, and scheduling settings confirmed.
- [ ] Frequency limits and overlapping campaigns reviewed.

### Approval and Release
- [ ] Test email reviewed by the appropriate stakeholders.
- [ ] Required business, brand, and legal approvals recorded.
- [ ] Critical issues resolved and retested.
- [ ] Final audience and campaign configuration rechecked.
- [ ] Deployment authorization received.

**Release decision:** [Approved / On hold]

**Final reviewer:** [Name]

**Approval date and time:** [Date, time, and time zone]

**Outstanding issues:** [None / Describe issues and mitigation]

## 3. A/B Testing Log

Use this template to document experiments and ensure decisions are based on a defined hypothesis and appropriate evidence.

| Field | Details |
|---|---|
| Experiment ID | [Unique reference] |
| Campaign | [Campaign name] |
| Hypothesis | [What change is expected to improve which outcome, and why?] |
| Variable tested | [Subject line, CTA, content, layout, send time, etc.] |
| Control version | [Describe version A] |
| Variant | [Describe version B] |
| Audience and allocation | [Eligibility rules and test split] |
| Primary metric | [The metric used to evaluate the hypothesis] |
| Guardrail metrics | [Unsubscribes, complaints, conversions, or other relevant measures] |
| Test duration | [Start and end dates] |
| Results | [Observed outcomes for each version] |
| Interpretation | [What the results do and do not support] |
| Decision | [Adopt, retest, iterate, or no change] |
| Follow-up action | [Next step and owner] |

**Experiment principle:** Define the hypothesis and success metric before launch. Use an appropriate sample size and test duration, avoid changing multiple variables simultaneously when causal interpretation matters, and do not declare a winner solely because one version has a higher observed result.

## 4. Post-Campaign Reporting Template

### Campaign Summary

- **Campaign name:** [Name]
- **Objective:** [Objective]
- **Deployment date:** [Date and time zone]
- **Target audience:** [Audience description]
- **Primary KPI:** [Metric and target]
- **Overall outcome:** [Brief factual summary]

### Performance Metrics

| Metric | Result | Target or Benchmark | Interpretation |
|---|---|---|---|
| Emails sent | [Value] | [Target, if applicable] | [Notes] |
| Delivered emails | [Value] | [Target, if applicable] | [Notes] |
| Delivery rate | [Value] | [Target, if applicable] | [Notes] |
| Bounce rate | [Value] | [Target, if applicable] | [Notes] |
| Unique click-through rate | [Value] | [Target, if applicable] | [Notes] |
| Conversion rate | [Value] | [Target, if applicable] | [Notes] |
| Unsubscribe rate | [Value] | [Target, if applicable] | [Notes] |
| Spam complaint rate | [Value] | [Applicable threshold or benchmark] | [Notes] |

*Define each metric and its denominator consistently. Open rates may be distorted by privacy features and should be interpreted cautiously. Use revenue or ROI metrics only when reliable attribution and cost data are available.*

### Insights and Next Actions

1. **What worked:** [Evidence-supported observation]
2. **What underperformed:** [Gap against target or relevant benchmark]
3. **Likely contributing factors:** [Audience, content, timing, deliverability, or technical factors]
4. **Recommended optimization:** [Specific action]
5. **Owner and due date:** [Person and deadline]
6. **Follow-up measurement:** [Metric and review date]

## 5. Campaign Issue and Escalation Log

Use this log to track issues from identification through resolution.

| Field | Details |
|---|---|
| Issue ID | [Unique reference] |
| Campaign and deployment | [Campaign name and scheduled time] |
| Issue identified | [Date, time, and time zone] |
| Issue description | [What happened and how it was detected] |
| Severity | [Critical / High / Medium / Low, based on team definitions] |
| Potential impact | [Audience, links, tracking, content, compliance, or delivery] |
| Immediate action | [Pause, hold, investigate, or mitigate] |
| Owner | [Responsible person] |
| Stakeholders notified | [Relevant teams or approvers] |
| Resolution | [Corrective action taken] |
| Retest and validation | [Evidence that the issue is resolved] |
| Closure and prevention | [Closure date and any preventive action] |

**Escalation principle:** For a potentially material issue, pause the deployment when feasible, assess the impact, notify the appropriate decision-makers, and obtain authorization before proceeding. Follow the organization's incident and approval procedures.

## 6. Marketing-to-Sales Handoff Template

Use this template when a campaign generates leads that require follow-up by a sales or business development team.

| Field | Details |
|---|---|
| Lead or contact identifier | [CRM record ID] |
| Lead source and campaign | [Source and campaign attribution] |
| Qualification status | [Lifecycle stage or qualification status] |
| Qualification rationale | [Relevant fit and engagement signals] |
| Key engagement | [Relevant content, form, webinar, or other interaction] |
| Assigned owner | [Sales representative or queue] |
| Handoff timestamp | [Date and time] |
| Follow-up SLA | [Agreed response window] |
| Next action | [Call, email, qualification, or nurture] |
| Disposition | [Accepted, contacted, recycled, disqualified, or other agreed status] |
| Feedback and notes | [Reason for acceptance, recycling, or disqualification] |

**Handoff principle:** Align qualification criteria, ownership, CRM fields, routing rules, and response-time expectations between marketing and sales. Monitor acceptance, follow-up compliance, and lead progression to identify gaps.

## Adaptation Notes

- Replace placeholders with campaign-specific information before use.
- Tailor QA checks to the capabilities and risks of the selected platform.
- Apply applicable consent, privacy, accessibility, and organizational approval requirements.
- Keep a record of significant configuration changes, approvals, and deployment decisions.
- Store completed templates according to the team's documentation and data-retention policies.

These templates are starting points and should be adapted to each organization's operating procedures rather than treated as universal compliance or release standards.
