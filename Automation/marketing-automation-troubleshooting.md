# Marketing Automation Troubleshooting Guide

## Purpose

This guide provides a structured approach to diagnosing, resolving, and preventing common marketing automation issues across platforms such as HubSpot, Marketo, Salesforce Marketing Cloud, Mailchimp, and Adobe Campaign.

The objective is to restore reliable campaign and workflow operations while protecting data quality, audience eligibility, customer experience, and reporting accuracy.

## 1. Troubleshooting Framework

Follow a consistent sequence when investigating an issue.

1. **Identify:** Document the reported issue, affected workflow or campaign, time of occurrence, and business impact.
2. **Contain:** Pause or restrict processing when necessary to prevent incorrect sends, duplicate communications, or unwanted data changes.
3. **Investigate:** Review enrollment criteria, execution history, audience data, integrations, configuration, and recent changes.
4. **Validate:** Reproduce the issue in a controlled test where possible and identify the underlying cause.
5. **Resolve:** Apply the smallest appropriate corrective change through the team's change-control process.
6. **Retest:** Validate the affected scenario and relevant downstream processes.
7. **Monitor:** Confirm that normal processing has resumed and that no related errors remain.
8. **Prevent:** Document the root cause and implement an appropriate preventive control.

## 2. Common Issues and Diagnostic Checks

| Issue | Potential Causes | Diagnostic Checks | Corrective Action |
|---|---|---|---|
| Contact does not enter a workflow | Entry criteria not met, enrollment restrictions, missing data, re-enrollment disabled | Review contact properties, trigger history, enrollment rules, and suppression conditions | Correct the data or criteria if appropriate; test eligibility before re-enrollment |
| Contact enters repeatedly | Re-enrollment enabled, repeated trigger events, missing exit conditions | Review enrollment history, trigger frequency, and exit logic | Adjust re-entry conditions and add suitable safeguards |
| Email is not sent | Consent or suppression rules, invalid address, workflow branch, send limits, configuration issue | Inspect execution logs, subscription status, exclusions, and send eligibility | Correct the underlying issue and verify recipient eligibility |
| Duplicate emails are sent | Overlapping workflows, repeated triggers, duplicate records, multiple campaign paths | Compare contact IDs, send logs, workflow history, and timestamps | Remove the duplicate cause and implement suitable deduplication or exclusion controls |
| Personalization is incorrect | Missing property values, incorrect tokens, data mapping errors, fallback not configured | Inspect contact records and rendered test messages | Correct mappings, data quality, or fallback logic and retest |
| Lead score is inaccurate | Conflicting rules, stale data, repeated scoring events, incorrect thresholds | Review scoring rules, property history, and representative contact records | Correct the scoring model and validate against sample records |
| CRM synchronization fails | Field mapping mismatch, permissions, API limits, connector errors, invalid values | Inspect sync logs, integration status, field mappings, and error messages | Correct configuration or permissions and reprocess affected records where supported |
| Audience count changes unexpectedly | Segment logic changed, records updated, exclusions added, data synchronization | Compare segment criteria, membership changes, and counts over time | Confirm the intended audience and investigate material unexplained changes |
| Reporting numbers do not match | Different reporting windows, attribution rules, time zones, metric definitions, or data latency | Compare source reports, filters, time windows, and metric definitions | Align reporting logic and document any remaining differences |
| Landing page or tracking fails | Broken URL, redirect issue, form configuration, missing UTM parameters, tracking errors | Test links, forms, redirects, and analytics events | Repair the asset or tracking configuration and retest end to end |

These are diagnostic starting points, not definitive root causes. Platform behavior and available logs vary.

## 3. Investigation Record

Document each incident using a consistent structure.

| Field | Information to Capture |
|---|---|
| Incident ID | Unique reference |
| Date and time detected | Include time zone |
| Affected asset | Campaign, workflow, integration, segment, or report |
| Issue description | Expected behavior versus observed behavior |
| Business impact | Audience, delivery, data, reporting, or customer impact |
| Scope | Affected records, campaigns, and time period |
| Evidence | Logs, screenshots, record IDs, and error messages, excluding unnecessary personal data |
| Recent changes | Configuration, integration, data, or deployment changes |
| Root cause | Confirmed cause, or current hypothesis if not confirmed |
| Resolution | Corrective action and owner |
| Validation | Tests performed and results |
| Prevention | Monitoring, documentation, or control improvements |
| Closure | Approver and closure date, where required |

## 4. Risk-Based Prioritization

Use the organization's incident definitions and escalation procedures. The following is an illustrative framework.

### Critical
Potentially unauthorized communication, material privacy or compliance exposure, widespread incorrect sends, or a major production failure.

**Response:** Contain the issue immediately where feasible, notify the designated incident owners, and follow established escalation procedures.

### High
Significant campaign disruption, widespread duplicate sends, substantial CRM synchronization failure, or a material data-quality issue.

**Response:** Assign an owner promptly, assess the affected scope, and agree on a recovery and communication plan.

### Medium
A localized workflow failure, inaccurate reporting, or a non-critical integration issue with a manageable workaround.

**Response:** Investigate, document the workaround, and schedule a controlled fix.

### Low
Minor formatting issues, documentation gaps, or isolated non-critical defects with limited operational impact.

**Response:** Record and resolve through normal maintenance procedures.

## 5. Safe Testing and Recovery

Before changing a production workflow or campaign:

- Review the existing configuration and document the current state.
- Identify affected records and downstream dependencies.
- Check whether a proposed fix could trigger new enrollments, duplicate sends, or unintended field updates.
- Use test records, sandbox environments, or controlled tests where available.
- Confirm consent, suppression, and eligibility rules remain intact.
- Obtain required approvals for production changes.
- Validate the original failure scenario and relevant adjacent scenarios.
- Confirm whether affected records need controlled reprocessing.
- Monitor the system after recovery.

**Important:** Do not manually re-enroll contacts, resend campaigns, or bulk-update records until the potential for duplicate communications and unintended side effects has been assessed.

## 6. Root-Cause Analysis

Distinguish the immediate symptom from the underlying cause.

**Example — Illustrative scenario**

- **Symptom:** Eligible contacts do not receive a follow-up email.
- **Initial assumption:** The email delivery system is failing.
- **Investigation:** Delivery logs show no send attempt. Workflow history indicates that contacts failed an eligibility condition.
- **Root cause:** A required property was not populated consistently after an upstream form or integration change.
- **Resolution:** Correct the mapping, validate representative records, and establish a controlled process for reviewing affected contacts.
- **Prevention:** Add a data-completeness check, monitor the relevant property, and include the integration in regression testing.

The example illustrates a troubleshooting method; it is not a claim about a specific client incident.

## 7. Preventive Controls

| Control | Purpose |
|---|---|
| Workflow documentation | Makes triggers, branches, exits, dependencies, and ownership clear |
| Data validation | Reduces missing, inconsistent, or invalid field values |
| Entry and exit safeguards | Prevents unintended enrollment and repeated processing |
| Suppression governance | Protects recipient eligibility and communication preferences |
| Integration monitoring | Detects synchronization failures and data delays |
| Change management | Reduces regression risk after configuration changes |
| Regression testing | Confirms existing scenarios still work after a fix |
| Alerting and exception reports | Helps identify failures before they become widespread |
| Periodic audits | Detects obsolete workflows, conflicting rules, and unused assets |
| Incident reviews | Converts recurring issues into preventive improvements |

## 8. Troubleshooting Closure Checklist

- [ ] Issue and business impact documented.
- [ ] Affected assets and records identified.
- [ ] Immediate risk contained where necessary.
- [ ] Evidence reviewed and root cause established, or uncertainty documented.
- [ ] Corrective change reviewed and approved as required.
- [ ] Relevant test scenarios passed.
- [ ] Audience eligibility and suppression controls revalidated.
- [ ] Downstream integrations and reporting checked.
- [ ] Recovery monitored.
- [ ] Stakeholders informed and incident record updated.
- [ ] Preventive action assigned an owner and due date.

## Operating Principle

Treat troubleshooting as a controlled operational process: establish the evidence, protect recipients and data, resolve the underlying cause, validate the fix, and prevent recurrence. Avoid making unverified production changes based only on the visible symptom.
