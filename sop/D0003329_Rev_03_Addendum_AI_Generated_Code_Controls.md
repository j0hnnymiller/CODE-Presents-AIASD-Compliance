---
ai_generated: true
model: "openai/gpt-5.3-codex@2026-04-03"
operator: "github-copilot"
chat_id: "create-ai-code-controls-addendum-artifacts-20260403"
prompt: |
  Follow instructions in #prompt:create-ai-code-controls-addendum-sop.prompt.md
started: "2026-04-03T00:34:00Z"
ended: "2026-04-03T00:58:00Z"
task_durations:
  - task: "source review and control mapping"
    duration: "00:08:00"
  - task: "addendum authoring"
    duration: "00:14:00"
  - task: "quality and provenance checks"
    duration: "00:02:00"
total_duration: "00:24:00"
ai_log: "ai-logs/2026/04/03/create-ai-code-controls-addendum-artifacts-20260403/conversation.md"
source: ".github/prompts/create-ai-code-controls-addendum-sop.prompt.md"
---

# GLOBAL WORK INSTRUCTION ADDENDUM: AI-GENERATED CODE CONTROLS

## 1. Purpose and Scope

1.1 This addendum defines mandatory additional controls for AI-assisted software development activities performed under D0003329 and associated design control procedures.

1.2 This addendum applies to all software lifecycle phases where AI-generated artifacts may influence requirements, architecture, detailed design, implementation, verification, maintenance, risk management, configuration management, or problem resolution.

1.3 This addendum applies to all software safety classes and shall be applied proportionately using the risk-tiered model in Section 5.

1.4 This addendum applies to internal development and outsourced development performed on behalf of Acme.

1.5 This addendum complements and does not replace existing requirements in D0003329 and D0003098.

IEC 62304 alignment: Clauses 4.1, 4.2, 5, 6, 7, 8, and 9.

## 2. Definitions

2.1 AI-assisted code: Source code, scripts, tests, or configuration content created in whole or in part by an AI system.

2.2 AI-generated artifact: Any file or content (code, tests, documentation, analysis, configurations) produced by an AI system and retained as a project deliverable.

2.3 Operator: A trained individual who prompts an AI system and proposes AI-generated outputs for project use.

2.4 Independent verifier: A qualified reviewer not responsible for originating the change and accountable for objective verification of change correctness and safety impact.

2.5 High-risk change: A change that can affect safety-related functions, risk controls, clinical functionality, cybersecurity controls, alarm handling, or release gating.

2.6 Provenance record: Required metadata and linked records showing who generated content, with which model, using which prompt, when, and with what review and approval outcomes.

2.7 AI-origin defect: A defect attributed to AI-generated or AI-modified content, including functional, safety, security, privacy, or compliance defects.

## 3. Roles and Responsibilities

3.1 Code author/operator shall:

- Use only approved AI tools and approved model endpoints.
- Provide sufficient prompt context without exposing prohibited sensitive data.
- Mark all AI-generated artifacts and initiate required traceability entries.
- Submit all AI-generated changes for mandatory review and verification.

  3.2 Technical reviewer shall:

- Perform line-level technical review of AI-generated changes.
- Confirm coding standards, architecture constraints, and maintainability.
- Confirm required tests are present and appropriate for risk tier.

  3.3 Independent verifier shall:

- Perform independent verification activities according to risk tier.
- Confirm objective evidence supports acceptance criteria and risk controls.
- Reject changes when evidence is incomplete or contradictory.

  3.4 Approver/release authority shall:

- Confirm release gate criteria are complete before approving deployment.
- Confirm unresolved AI-origin anomalies are dispositioned.

  3.5 QA/RA oversight shall:

- Confirm this addendum is implemented and auditable.
- Review metrics and nonconformance trends for management review.

IEC 62304 alignment: Clauses 4.1, 5.1, 6.1, 7.1, 8.1, 9.1.

## 4. AI Usage Boundaries and Prohibited Practices

4.1 AI-generated code shall not be promoted directly to production without human review, independent verification (as applicable), and approval gate completion.

4.2 AI may support safety-related implementation only when enhanced scrutiny controls for high and safety-impacting tiers are applied.

4.3 Operators shall not submit controlled unredacted PHI, PII, credentials, proprietary algorithms, or unreleased regulatory strategy content to non-approved AI endpoints.

4.4 Auto-acceptance of AI suggestions without documented review is prohibited.

4.5 AI tools shall not be used to bypass configuration control, change approval workflows, or validation evidence requirements.

## 5. Risk-Tiered Control Model

5.1 Each AI-assisted change shall be assigned one of four tiers before implementation:

- Tier 1 (Low): No safety impact, no security/privacy impact, no risk-control logic impact.
- Tier 2 (Moderate): Indirect impact to functional behavior or reliability.
- Tier 3 (High): Direct impact to risk controls, software architecture, interface behavior, or regulated calculations.
- Tier 4 (Safety-Impacting): Potential impact to hazardous situations, alarms, treatment logic, or clinical decision pathways.

  5.2 Minimum controls by tier:

- Tier 1: peer review, unit tests, provenance record.
- Tier 2: peer review, independent verification sample, unit and integration tests, traceability update.
- Tier 3: full independent verification, regression testing, risk review update, approval gate sign-off.
- Tier 4: independent verification with safety reviewer, risk file update, formal verification protocol/report, release board approval.

  5.3 Tier assignments shall be documented in change records and approved by the technical reviewer.

IEC 62304 alignment: Clauses 5.1, 5.5, 5.6, 5.7, 6.1, 7.1.

## 6. Human Review and Independent Verification Controls

6.1 Human review is mandatory for all AI-generated code and shall include correctness, boundary handling, error handling, maintainability, and standards conformance.

6.2 Independent verification is mandatory for Tiers 2-4 and shall be performed by qualified personnel independent of code authorship.

6.3 For Tiers 3-4, reviewer and verifier shall confirm traceability to requirements and risk controls prior to approval.

6.4 Segregation of duties shall be enforced such that the same individual cannot originate, independently verify, and approve a Tier 4 change.

## 7. Design Control and Traceability Requirements

7.1 AI-assisted changes shall map to one or more approved input artifacts: user need, system requirement, software requirement, risk control, or defect/CAPA source.

7.2 Traceability shall be maintained from requirement to implementation to verification evidence to release record.

7.3 Changes generated by AI shall reference the applicable configuration item and version description documentation.

7.4 Traceability matrices shall explicitly identify AI-assisted code segments and linked verification evidence.

IEC 62304 alignment: Clauses 5.2, 5.3, 5.5, 5.7, 8.2.

## 8. Verification and Validation Expectations

8.1 Minimum test expectations by tier:

- Tier 1: Unit tests and static analysis results.
- Tier 2: Unit tests plus integration tests.
- Tier 3: Unit, integration, and regression tests.
- Tier 4: Unit, integration, regression, and safety-impact verification with documented acceptance rationale.

  8.2 Test evidence shall demonstrate positive, negative, boundary, and failure-mode coverage for high and safety-impacting changes.

  8.3 Unresolved failed tests shall block release until disposition and approval are documented.

IEC 62304 alignment: Clauses 5.5, 5.6, 5.7, 6.2.

## 9. Security and Privacy Controls

9.1 AI-assisted changes shall be reviewed for insecure coding patterns, injection risks, hardcoded secrets, dependency vulnerabilities, and unsafe deserialization or command execution paths.

9.2 Dependency and license checks shall be performed for AI-suggested packages or third-party components.

9.3 Prompt content shall follow data minimization principles and approved data handling requirements.

9.4 AI outputs containing potential leakage of sensitive data shall be rejected and incident-managed.

IEC 62304 alignment: Clauses 4.2, 5.1, 7.1, 9.1.

## 10. Provenance and Recordkeeping

10.1 All AI-generated artifacts shall include required YAML provenance metadata in Markdown artifacts or approved equivalent for non-Markdown artifacts.

10.2 Required record elements shall include:

- Model provider and model version.
- Prompt identifier and prompt purpose.
- chat_id and ai_log path.
- Operator, reviewer, verifier, approver identifiers.
- Start/end timestamps and task durations.
- Approval and verification decision records.

  10.3 Records shall be retained with design history and software lifecycle records per applicable retention policy.

  10.4 Missing provenance records shall be treated as a process nonconformance.

## 11. Release Readiness and Approval Gates

11.1 Release gates for AI-assisted code shall include:

- Completed risk tier assignment.
- Completed required review and independent verification.
- Completed traceability updates.
- Completed required test evidence.
- Closed or accepted anomalies with documented rationale.

  11.2 Tier 4 changes shall require release authority and QA/RA concurrence.

  11.3 Emergency changes shall follow expedited change procedures but shall not bypass mandatory post-implementation verification and retrospective approval.

IEC 62304 alignment: Clauses 5.8, 6.3, 8.3, 9.8.

## 12. Post-Release Monitoring and CAPA Triggers

12.1 AI-origin defects shall be tagged in anomaly/problem systems for trend analysis.

12.2 Trigger criteria for CAPA consideration shall include repeated defect modes, severity escalation, recurrence in safety-related modules, or repeated control failures.

12.3 Post-release reviews shall include AI-origin defect metrics and corrective action effectiveness.

IEC 62304 alignment: Clauses 6.1, 9.1 through 9.8.

## 13. Training and Competency

13.1 Personnel acting as operators, reviewers, verifiers, or approvers for AI-assisted changes shall complete role-specific training before performing duties.

13.2 Training shall include AI risk awareness, secure usage practices, traceability requirements, and this addendum’s control model.

13.3 Competency shall be reassessed at least annually or when significant process changes occur.

## 14. Nonconformance and Escalation

14.1 Deviations from this addendum shall be documented as nonconformances and processed through the applicable nonconformance procedure.

14.2 Escalation shall be immediate for Tier 4 deviations, missing independent verification for required tiers, or any suspected patient safety impact.

14.3 Corrective actions shall include containment, root cause analysis, remediation, and effectiveness verification.

## 15. Metrics and Management Review

15.1 The following KPIs shall be monitored at minimum:

- Percentage of AI-assisted changes with complete provenance metadata.
- Review and verification completion rate by risk tier.
- AI-origin defect rate per release.
- Reopened defects linked to AI-assisted changes.
- Time to closure for AI-origin anomalies.
- Number of process deviations/nonconformances.

  15.2 Management review shall occur at least quarterly and shall evaluate trend data, CAPA status, control effectiveness, and resource/training adequacy.

  15.3 Management decisions and resulting actions shall be documented and tracked to completion.

IEC 62304 alignment: Clauses 4.1, 6.1, 9.1, and quality system monitoring expectations.

## Approvals

This addendum shall be approved by designated stakeholders per the governing document control and approval workflow before becoming effective.

## Revision History

- Rev 01 (Draft): Initial release of AI-generated code control addendum aligned to D0003329 Rev 03.
