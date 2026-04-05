---
ai_generated: true
model: "openai/gpt-5.3-codex@2026-04-03"
operator: "github-copilot"
chat_id: "create-prompt-for-ai-code-addendum-sop-20260403"
prompt: |
  Create a prompt file that creates a prompt file that creates an addendum SOP
  describing the additional controls needed for AI-generated code.
started: "2026-04-03T00:00:00Z"
ended: "2026-04-03T00:18:00Z"
task_durations:
  - task: "requirements review"
    duration: "00:06:00"
  - task: "meta-prompt authoring"
    duration: "00:09:00"
  - task: "repository updates"
    duration: "00:03:00"
total_duration: "00:18:00"
ai_log: "ai-logs/2026/04/03/create-prompt-for-ai-code-addendum-sop-20260403/conversation.md"
source: "github-copilot-coding-agent"
applyTo: "**/*.prompt.md"
---

# Prompt: Create Prompt for AI-Generated Code Controls Addendum SOP

## Purpose

Generate a second prompt file that, when executed, creates an SOP addendum document describing mandatory additional controls for AI-generated code in regulated software development.

## Primary Task

Create the complete prompt file:

`.github/prompts/create-ai-code-controls-addendum-sop.prompt.md`

The generated prompt must produce:

`sop/D0003329_Rev_03_Addendum_AI_Generated_Code_Controls.md`

## Context

This repository contains SOPs and compliance artifacts for IEC 62304-aligned software lifecycle controls. The addendum must extend existing SOP controls specifically for AI-assisted code generation, review, validation, release, and traceability.

**CRITICAL**: All AI-generated artifacts in this repository MUST comply with `.github/instructions/ai-assisted-output.instructions.md`.

## Requirements for the Prompt You Generate

The generated prompt file must include the following sections and content requirements.

### 1. Mission

Clearly state that the prompt must create an SOP addendum defining additional AI-generated code controls that are auditable, actionable, and compatible with IEC 62304 processes.

### 2. Required Input Files

Require loading these files before authoring the addendum:

1. `sop/D0003329_Rev_03_Final.md`
2. `sop/D0003098_Rev_05_Final.md`
3. `standards/BSEN-62304.md`
4. `.github/instructions/ai-assisted-output.instructions.md`

### 3. Addendum Content Requirements

Require the SOP addendum output to include at least these sections:

1. Purpose and Scope of AI-generated code usage
2. Definitions (AI-assisted code, operator, verifier, provenance, high-risk change)
3. Roles and responsibilities (author, reviewer, approver, QA/RA)
4. AI usage boundaries and prohibited use cases
5. Risk-tiered control model for AI-generated code changes
6. Mandatory human review and independent verification rules
7. Design control and traceability requirements for AI-generated code
8. Verification and validation expectations (unit, integration, regression, safety-impact)
9. Security and privacy controls (secrets, dependencies, injection, data leakage)
10. Provenance and recordkeeping requirements (`chat_id`, `ai_log`, model/version, prompt capture)
11. Release readiness and approval gates
12. Post-release monitoring and CAPA triggers for AI-origin defects
13. Training and competency requirements
14. Nonconformance handling and escalation path
15. Metrics and periodic management review requirements

### 4. Deliverable Quality Constraints

Require the generated SOP addendum to be:

- Written in formal SOP language using mandatory terms (`shall`, `must`)
- Structured with numbered sections and enforceable controls
- Explicitly mapped to relevant IEC 62304 lifecycle expectations where appropriate
- Ready for quality-system review without placeholder text

### 4.1 Markdown Formatting Requirements (CRITICAL)

Require strict adherence to these formatting rules:

**Subsection Numbering After Bullet Lists**:

- Subsections (e.g., "3.2", "5.3", "10.4") following bullet-point lists MUST NOT be indented
- Example CORRECT format:

  ```
  3.1 Code author/operator shall:

  - Use only approved AI tools
  - Document all prompts used

  3.2 Technical reviewer shall:

  - Perform line-by-line code review
  ```

- Example INCORRECT format (do not use):
  ```
    3.2 Technical reviewer shall:   ← DO NOT INDENT SUBSECTIONS
  ```
- All numbered subsections must start at column 0 (no leading spaces)

### 5. Deliverables Produced by the Generated Prompt

Require the generated prompt to produce both files:

1. `sop/D0003329_Rev_03_Addendum_AI_Generated_Code_Controls.md` (primary SOP addendum)
2. `output/AI_Generated_Code_Controls_Addendum_Implementation_Checklist.md` (operational checklist)

### 6. Metadata Requirements

Require the generated prompt to enforce complete AI provenance YAML front matter in each produced Markdown artifact, following `.github/instructions/ai-assisted-output.instructions.md`.

## Output Format for the Prompt You Generate

The second prompt file must be complete and executable, and include:

1. YAML front matter with AI provenance metadata
2. Mission and context
3. Input requirements
4. Detailed section-by-section authoring instructions
5. Quality validation checklist
6. Explicit output file paths

## Deliverable

Generate the complete `.github/prompts/create-ai-code-controls-addendum-sop.prompt.md` file now.
