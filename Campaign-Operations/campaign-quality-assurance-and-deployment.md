# Campaign Quality Assurance and Deployment Playbook

## Overview

Quality assurance (QA) is a critical control within email campaign operations. A structured QA process helps prevent incorrect audience targeting, broken links, rendering issues, tracking errors, compliance gaps, and unintended customer experiences.

This playbook outlines a repeatable approach to validating, approving, deploying, and monitoring email campaigns across marketing automation platforms.

## 1. Pre-QA Readiness

Before testing begins, confirm that the campaign requirements and dependencies are ready.

- Campaign objective and success metrics are documented.
- Campaign brief and stakeholder approvals are available.
- Target audience and exclusion criteria are confirmed.
- Email copy, subject line, preheader, and creative assets are approved.
- Landing pages and destination URLs are published or ready for testing.
- Personalization fields and dynamic content rules are defined.
- Tracking parameters and analytics requirements are documented.
- Send date, time, time zone, and audience volume are confirmed.
- Required legal, privacy, and consent checks are complete.

**Exit criterion:** The campaign is sufficiently complete to enter formal QA.

## 2. Email Content and Rendering QA

Validate the email across content, design, links, and common viewing environments.

### Content checks

- Subject line and preheader are correct.
- Sender name and sender address are approved.
- Copy, spelling, grammar, and punctuation are reviewed.
- Personalization tokens resolve correctly.
- Dynamic content displays the intended version.
- Images have appropriate alternative text where needed.
- Required disclaimers, footer details, and unsubscribe options are present.

### Design and rendering checks

- Layout displays correctly on desktop and mobile.
- Images load and scale appropriately.
- Fonts, spacing, alignment, and buttons are consistent.
- Dark-mode rendering is reviewed where relevant.
- Major email clients and supported devices are tested.
- Plain-text content is available where required.

Rendering differences can occur across email clients. Prioritize compatibility with the audience's commonly used clients and devices.

## 3. Link, Landing Page, and Tracking QA

Validate every important destination and tracking element.

| Check | Validation |
|---|---|
| Primary CTA | Opens the correct destination |
| Secondary links | Point to the intended pages |
| Landing pages | Load successfully and display the expected content |
| Redirects | Resolve to valid, intended destinations |
| UTM parameters | Match the agreed campaign naming convention |
| Analytics | Tracking parameters and required events are configured |
| Expiring URLs | Destination remains valid for the planned campaign period |
| Forms | Submission, confirmation, and follow-up behavior work as expected |

Do not assume that a link is correct simply because it opens. Confirm that its destination matches the campaign objective and remains valid for the required period.

## 4. Audience and Suppression QA

Incorrect targeting can create compliance issues, duplicate communications, or poor customer experiences.

Validate the following:

- The selected audience matches the approved campaign brief.
- Required inclusion and exclusion criteria are applied.
- Unsubscribed contacts and applicable suppression lists are respected.
- Consent and lawful communication requirements are satisfied.
- Duplicate records and overlapping audience segments are assessed.
- Regional, language, and localization rules are correct.
- Test contacts are excluded from the production audience where appropriate.
- Estimated send volume is consistent with expectations.

For large or high-risk campaigns, compare audience counts against the approved estimate and investigate material discrepancies before deployment.

## 5. Platform Configuration QA

Review campaign settings in the marketing automation platform before scheduling or sending.

- Correct email asset and campaign version are selected.
- Sender identity and reply-to address are correct.
- Audience, exclusions, and suppression rules are configured.
- Send date, time, and time zone are correct.
- Personalization and dynamic content rules are active.
- Tracking and analytics settings are enabled as required.
- Frequency controls and applicable communication limits are respected.
- Test-send results have been reviewed.
- Required approvals are recorded.
- The final production configuration matches the approved version.

Exact configuration options vary by platform, so the checklist should be adapted to the system being used.

## 6. Risk-Based QA and Approval

Not every campaign carries the same level of risk. QA effort should reflect audience size, business impact, complexity, and compliance requirements.

| Risk level | Typical characteristics | Suggested controls |
|---|---|---|
| Low | Routine campaign using an established template | Standard content, link, audience, and rendering checks |
| Medium | New creative, new audience logic, or multiple dynamic elements | Expanded testing and documented reviewer approval |
| High | Large audience, sensitive communication, complex personalization, or major business impact | Independent review, enhanced audience validation, formal sign-off, and controlled deployment |

Risk classifications should be agreed with the relevant stakeholders rather than assigned solely on send volume.

## 7. Deployment and Send-Day Controls

Before release:

1. Confirm that all mandatory QA checks have passed.
2. Resolve or formally approve any outstanding issues.
3. Obtain the required stakeholder sign-offs.
4. Confirm the final asset, audience, exclusions, and schedule.
5. Verify that no unapproved changes have been introduced after testing.
6. Record the approved campaign version and deployment details.

For high-risk campaigns, consider a controlled initial release or phased deployment when supported by the platform and campaign requirements.

After deployment:

- Confirm that the campaign was released as intended.
- Check initial delivery and bounce indicators.
- Review available engagement and error signals.
- Escalate unexpected results or customer-impacting issues.
- Follow the documented incident and communication process if intervention is needed.

## 8. Issue Management and Escalation

When a QA issue is identified, document it clearly and assign ownership.

A useful issue record includes:

- Campaign name or identifier
- Issue description and affected component
- Severity and potential impact
- Evidence, such as a screenshot or test result
- Assigned owner
- Required corrective action
- Retest result
- Resolution status and approval, where applicable

**Deployment rule:** Do not proceed with an unresolved critical issue affecting audience accuracy, consent, destination validity, or customer experience unless an authorized decision-maker has explicitly approved a documented alternative.

If an error is discovered after deployment, assess its impact, notify the appropriate stakeholders, and follow the established incident-response process. Any corrective communication should be reviewed for accuracy, compliance, and customer impact.

## 9. Post-Campaign Review

After sufficient time has passed for meaningful results to accumulate:

- Review delivery, bounce, complaint, and unsubscribe metrics.
- Assess engagement and conversion performance against the campaign objective.
- Investigate unusual results or significant deviations from expectations.
- Record issues, root causes, and corrective actions.
- Capture learnings for future campaign briefs and QA procedures.
- Update templates, checklists, or automation rules when recurring issues are identified.

A post-campaign review should distinguish between execution quality and campaign effectiveness. A technically correct deployment does not necessarily mean the campaign achieved its business objective.

## 10. Reusable QA Sign-Off Checklist

Use this checklist as a starting point for individual campaign deployments.

- [ ] Campaign brief and objective approved
- [ ] Audience and suppression logic validated
- [ ] Content and creative approved
- [ ] Personalization and dynamic content tested
- [ ] Links and landing pages validated
- [ ] Tracking parameters checked
- [ ] Rendering and mobile experience reviewed
- [ ] Consent, footer, and unsubscribe requirements checked
- [ ] Platform settings and schedule verified
- [ ] Test send reviewed
- [ ] Required approvals documented
- [ ] Final production version confirmed
- [ ] Deployment monitored
- [ ] Post-campaign results and learnings recorded

## Guiding Principles

- Treat QA as a defined operational process, not a final visual inspection.
- Validate audience logic and destinations as carefully as email content.
- Use documented approval criteria and clear ownership.
- Scale testing to campaign risk and complexity.
- Preserve a traceable record of decisions, changes, and outcomes.
- Use recurring issues to improve future campaign processes.

---

*This playbook is a platform-agnostic operational reference. Specific controls should be adapted to the organization's systems, policies, audience requirements, and approval procedures.*
