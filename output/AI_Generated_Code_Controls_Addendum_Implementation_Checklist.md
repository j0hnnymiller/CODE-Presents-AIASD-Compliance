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
  - task: "checklist design"
    duration: "00:06:00"
  - task: "checklist authoring"
    duration: "00:07:00"
  - task: "metadata and validation"
    duration: "00:02:00"
total_duration: "00:15:00"
ai_log: "ai-logs/2026/04/03/create-ai-code-controls-addendum-artifacts-20260403/conversation.md"
source: ".github/prompts/create-ai-code-controls-addendum-sop.prompt.md"
---

# AI-Generated Code Controls Addendum Implementation Checklist

## Usage Instructions

- Use this checklist to implement and verify controls defined in D0003329 Rev 03 AI-generated code addendum.
- Update Status as work progresses: Not Started, In Progress, Complete, Verified.
- Attach objective evidence links/IDs in project records.

## Checklist Table

| SOP Section                  | Implementation Task                                                                                           | Role Owner                 | Objective Evidence                                      | Verification Method                             | Status      | Priority | Target Completion Date |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------- | -------------------------- | ------------------------------------------------------- | ----------------------------------------------- | ----------- | -------- | ---------------------- |
| 1 Purpose and Scope          | Publish controlled addendum and define applicability boundaries for all software classes and lifecycle phases | QA/RA                      | Approved controlled document ID and distribution record | Document control audit                          | Not Started | High     | TBD                    |
| 2 Definitions                | Add and approve glossary entries for AI-assisted code terms used in projects                                  | QA/RA + R&D                | Updated glossary revision and approval signatures       | Spot-check project usage against glossary       | Not Started | Medium   | TBD                    |
| 3 Roles and Responsibilities | Update RACI matrix to assign operator, reviewer, verifier, and approver accountabilities                      | Project Manager + QA/RA    | Approved RACI matrix and role assignment records        | Internal audit of sampled changes               | Not Started | High     | TBD                    |
| 4 Usage Boundaries           | Configure policy that blocks direct promotion of AI-generated code without review gates                       | DevOps + QA/RA             | Branch protection rules, workflow policy, approval logs | Pipeline control test and audit trail review    | Not Started | High     | TBD                    |
| 4 Usage Boundaries           | Implement prohibited-data handling guidance for AI prompts                                                    | Security + R&D             | Approved guidance and training completion record        | Prompt review sampling and security audit       | Not Started | High     | TBD                    |
| 5 Risk-Tiered Model          | Define tiering criteria and decision worksheet for each AI-assisted change                                    | R&D + Risk Management      | Risk-tier worksheet template and approved examples      | Review of completed worksheet in change records | Not Started | High     | TBD                    |
| 5 Risk-Tiered Model          | Embed required controls by tier into change workflow templates                                                | QA/RA + DevOps             | Updated workflow template and SOP references            | Mock change execution walkthrough               | Not Started | High     | TBD                    |
| 6 Human Review               | Require mandatory reviewer checklist for all AI-assisted code submissions                                     | R&D Leads                  | Reviewer checklist records in pull requests             | Sampled pull request audit                      | Not Started | High     | TBD                    |
| 6 Independent Verification   | Enforce independent verification assignment for Tier 2-4                                                      | QA/RA + R&D Leads          | Verification assignment records and sign-offs           | Segregation-of-duties audit                     | Not Started | High     | TBD                    |
| 7 Traceability               | Update traceability matrix template to flag AI-assisted artifacts and linked tests                            | Systems Engineering + R&D  | Updated traceability matrix and completed sample        | End-to-end traceability review                  | Not Started | High     | TBD                    |
| 8 V&V Expectations           | Define minimum test pack per risk tier including failure-mode tests for Tier 3-4                              | Verification Team          | Test strategy update and executed protocol/report IDs   | Test evidence completeness check                | Not Started | High     | TBD                    |
| 8 V&V Expectations           | Add regression evidence gate for Tier 3-4 release candidates                                                  | DevOps + Verification Team | CI gate configuration and regression report             | Controlled release dry run                      | Not Started | High     | TBD                    |
| 9 Security and Privacy       | Enable automated scans for secrets, vulnerable dependencies, and insecure patterns                            | Security Engineering       | Scan reports, policy configuration snapshots            | Security dashboard and exception review         | Not Started | High     | TBD                    |
| 9 Security and Privacy       | Add license and SOUP scrutiny step for AI-suggested packages                                                  | R&D + Legal/Compliance     | Dependency review records and approvals                 | Sample package approval audit                   | Not Started | Medium   | TBD                    |
| 10 Provenance                | Enforce YAML metadata checks for AI-generated markdown artifacts                                              | QA/RA + DevOps             | CI policy and passing check outputs                     | CI control verification                         | Not Started | High     | TBD                    |
| 10 Provenance                | Ensure chat_id and ai_log records are retained with DHF evidence                                              | Document Control + QA/RA   | DHF index entries and linked ai-logs references         | DHF records audit                               | Not Started | High     | TBD                    |
| 11 Release Gates             | Add AI-assisted release readiness checklist to release workflow                                               | Release Manager            | Signed release checklist and gate approvals             | Pre-release gate review                         | Not Started | High     | TBD                    |
| 11 Release Gates             | Require QA/RA concurrence for Tier 4 releases                                                                 | QA/RA                      | Release packet with QA/RA sign-off                      | Release governance audit                        | Not Started | High     | TBD                    |
| 12 Post-Release Monitoring   | Tag AI-origin defects in problem resolution system                                                            | Service + QA/RA            | Defect taxonomy update and tagged records               | Trend report verification                       | Not Started | Medium   | TBD                    |
| 12 CAPA Triggers             | Define CAPA trigger thresholds for AI-origin defects                                                          | QA/RA + Risk Management    | Approved trigger matrix and CAPA criteria               | CAPA board review                               | Not Started | High     | TBD                    |
| 13 Training and Competency   | Deliver role-based training for operator/reviewer/verifier/approver populations                               | Training + QA/RA           | Training rosters and competency assessments             | Training effectiveness review                   | Not Started | High     | TBD                    |
| 14 Nonconformance            | Update nonconformance workflow to include AI-control deviations                                               | QA/RA                      | Updated procedure and example records                   | Nonconformance process audit                    | Not Started | High     | TBD                    |
| 14 Escalation                | Define immediate escalation path for Tier 4 or safety-impact control failures                                 | QA/RA + Leadership         | Escalation matrix and communication logs                | Drill or tabletop exercise                      | Not Started | High     | TBD                    |
| 15 Metrics                   | Implement KPI dashboard for provenance completeness, defects, and verification rates                          | QA/RA + Analytics          | Dashboard export and metric definitions                 | Management review package                       | Not Started | Medium   | TBD                    |
| 15 Management Review         | Add quarterly management review agenda item for AI-control effectiveness                                      | Quality Management         | Meeting agenda/minutes and action tracker               | Review action closure verification              | Not Started | Medium   | TBD                    |

## Completion Criteria

- All High-priority tasks are at least Complete before broad deployment of AI-assisted coding workflows.
- Tasks tied to Tier 4 controls must reach Verified before any Tier 4 change release.
- Evidence references must be auditable and retained according to record retention policy.
