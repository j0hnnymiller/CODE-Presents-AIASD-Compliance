---
ai_generated: true
model: "openai/gpt-5.3-codex@2026-04-03"
operator: "github-copilot"
chat_id: "create-ai-code-controls-addendum-sop-prompt-20260403"
prompt: |
  Follow instructions in .github/prompts/create-prompt-for-ai-code-addendum-sop.prompt.md
  and generate the complete .github/prompts/create-ai-code-controls-addendum-sop.prompt.md file.
started: "2026-04-03T00:19:00Z"
ended: "2026-04-03T00:33:00Z"
task_durations:
  - task: "prompt requirements interpretation"
    duration: "00:04:00"
  - task: "prompt authoring"
    duration: "00:08:00"
  - task: "provenance and traceability updates"
    duration: "00:02:00"
total_duration: "00:14:00"
ai_log: "ai-logs/2026/04/03/create-ai-code-controls-addendum-sop-prompt-20260403/conversation.md"
source: ".github/prompts/create-prompt-for-ai-code-addendum-sop.prompt.md"
applyTo: "**/*.prompt.md"
---

# Prompt: Create SOP Addendum for AI-Generated Code Controls

## Mission

Create a formal SOP addendum document that defines additional, auditable controls for AI-generated code in regulated software development. The addendum must be compatible with IEC 62304 lifecycle expectations and be suitable for quality-system review.

## Primary Output Targets

Generate both of the following files:

1. `sop/D0003329_Rev_03_Addendum_AI_Generated_Code_Controls.md`
2. `output/AI_Generated_Code_Controls_Addendum_Implementation_Checklist.md`

## Required Input Files

Load and use these files before writing:

1. `sop/D0003329_Rev_03_Final.md`
2. `sop/D0003098_Rev_05_Final.md`
3. `standards/BSEN-62304.md`
4. `.github/instructions/ai-assisted-output.instructions.md`

## Context

The repository uses standardized SOPs and IEC 62304-oriented compliance artifacts. This addendum extends existing procedures to address AI-assisted code generation risks and governance obligations while preserving traceability, verification rigor, and release controls.

**CRITICAL**: All AI-generated artifacts in this repository MUST comply with `.github/instructions/ai-assisted-output.instructions.md`.

## Authoring Requirements for SOP Addendum

The SOP addendum shall include these numbered sections, in order.

### 1. Purpose and Scope

Define the purpose of AI-generated code controls and scope boundaries, including applicable software classes, lifecycle phases, and affected teams.

### 2. Definitions

Define at minimum:

- AI-assisted code
- AI-generated artifact
- Operator
- Independent verifier
- High-risk change
- Provenance record
- AI-origin defect

### 3. Roles and Responsibilities

Define accountable roles and decision rights for:

- Code author/operator
- Technical reviewer
- Independent verifier
- Approver/release authority
- QA/RA oversight

### 4. AI Usage Boundaries and Prohibited Practices

Specify allowed and prohibited AI usage, including:

- Ban on unreviewed direct promotion to production
- Restrictions on safety-critical logic generation without enhanced scrutiny
- Prohibition on exposing sensitive data to external model endpoints unless approved

### 5. Risk-Tiered Control Model

Define risk tiers (for example: low, moderate, high, safety-impacting) and required control intensity per tier.

### 6. Human Review and Independent Verification Controls

Require mandatory human review and independent verification criteria by risk tier, including segregation-of-duties expectations.

### 7. Design Control and Traceability Requirements

Define traceability requirements from requirement to code to verification evidence for AI-generated changes.

### 8. Verification and Validation Expectations

Define minimum testing requirements by risk tier:

- Unit tests
- Integration tests
- Regression tests
- Safety-impact verification
- Failure-mode focused testing where applicable

### 9. Security and Privacy Controls

Define controls for:

- Secret handling
- Dependency and license scrutiny
- Prompt injection and insecure output patterns
- Data leakage and data minimization

### 10. Provenance and Recordkeeping

Require capturing and retaining:

- Model provider and version
- Prompt identifiers and purpose
- `chat_id`
- `ai_log` path
- Operator, reviewer, verifier, approver identifiers
- Decision and evidence records

### 11. Release Readiness and Approval Gates

Define required gates and sign-offs before release of AI-assisted code changes.

### 12. Post-Release Monitoring and CAPA Triggers

Define defect monitoring, AI-origin trend analysis, and CAPA escalation criteria.

### 13. Training and Competency

Define baseline and recurring training requirements for personnel using or reviewing AI-assisted code.

### 14. Nonconformance and Escalation

Define deviation handling, corrective actions, and escalation routes for control failures.

### 15. Metrics and Management Review

Define measurable KPIs and periodic management review cadence (for example: review cycle, defect rates, verification completion rates, policy exceptions).

## Quality Constraints

The generated SOP addendum must be:

- Written in formal SOP language using enforceable terms such as shall and must
- Organized with clear numbered sections and objective controls
- Mapped to relevant IEC 62304 lifecycle expectations where appropriate
- Free of placeholders and suitable for direct quality-system review

## CRITICAL: Markdown Formatting Rules

Adhere to these rules when authoring sections and subsections:

### Rule 1: No Indentation on Subsections

All numbered subsections (3.2, 3.3, 5.2, 8.3, etc.) MUST start at column 0 — no leading spaces, even when appearing after bullet-point lists.

**CORRECT**:

```
3.1 Code author/operator shall:

- Use approved AI tools
- Maintain prompt records

3.2 Technical reviewer shall:

- Review all generated code
```

**INCORRECT** (do not generate this way):

```
  3.2 Technical reviewer shall:  ← 2 spaces before 3.2 is WRONG
```

### Rule 2: Bullet List Formatting

- Use standard markdown bullet format with leading dash and space: `- Item text`
- Bullet points should have no extra indentation relative to their parent section
- Separate bullets with blank line only if they are multi-line items

### Rule 3: Section/Subsection Hierarchy

Structure sections consistently:

- **Top-level sections**: `# Section Title` (markdown header level 2 in context of document)
- **Numbered sections**: `1. Purpose and Scope`, `2. Definitions`, etc.
- **Subsections**: `X.Y Role Description` (X = section number, Y = subsection number)
- **Subsection content**: Bulleted requirements or narrative text
- **No extra indentation between main sections and subsections**

Apply these rules throughout all 15 SOP sections.

## Checklist Output Requirements

The implementation checklist must include:

1. Control implementation tasks mapped to each SOP section
2. Role owner for each task
3. Objective evidence expected for completion
4. Verification method for completion status
5. Status field (Not Started, In Progress, Complete, Verified)
6. Priority and target completion date fields

## Required AI Provenance Metadata (YAML Front Matter)

Both generated Markdown artifacts must begin with YAML front matter including at least:

```yaml
ai_generated: true
model: "<provider>/<model-name>@<version>"
operator: "<username-or-name>"
chat_id: "<chat-id>"
prompt: |
  <exact-prompt-text-used>
started: "<ISO8601>"
ended: "<ISO8601>"
task_durations:
  - task: "<task-name>"
    duration: "<hh:mm:ss>"
total_duration: "<hh:mm:ss>"
ai_log: "ai-logs/<yyyy>/<mm>/<dd>/<chat-id>/conversation.md"
source: ".github/prompts/create-ai-code-controls-addendum-sop.prompt.md"
```

## Validation Checklist

Before finalizing outputs, verify:

- [ ] Both target files were created at the exact required paths
- [ ] All 15 SOP sections are present and substantive
- [ ] Controls are auditable, testable, and assigned to accountable roles
- [ ] Risk-tiered controls are explicit and actionable
- [ ] Traceability and provenance controls include `chat_id` and `ai_log`
- [ ] Security, privacy, and post-release monitoring controls are complete
- [ ] Checklist rows map directly to SOP controls with objective evidence fields
- [ ] Both files contain complete AI provenance YAML front matter

## Deliverable

Generate both complete files now:

1. `sop/D0003329_Rev_03_Addendum_AI_Generated_Code_Controls.md`
2. `output/AI_Generated_Code_Controls_Addendum_Implementation_Checklist.md`
