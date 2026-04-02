---
ai_generated: true
model: "anthropic/claude-3.5-sonnet@2024-10-22"
operator: "github-copilot"
chat_id: "create-implementation-plan-prompt-20260401"
prompt: |
  Create a meta-prompt for generating implementation plans for various project activities
started: "2026-04-01T00:00:00Z"
ended: "2026-04-01T00:20:00Z"
task_durations:
  - task: "meta-prompt design"
    duration: "00:15:00"
  - task: "template creation"
    duration: "00:05:00"
total_duration: "00:20:00"
ai_log: "ai-logs/2026/04/01/create-implementation-plan-prompt-20260401/conversation.md"
source: "github-copilot-coding-agent"
applyTo: "**/*.prompt.md"
---

# Prompt: Create Implementation Plan

## Purpose

Generate comprehensive, actionable implementation plans for various activities including assessments, remediations, documentation projects, process improvements, and workflow executions in the AI-Assisted Software Development (AIASD) compliance repository.

## Core Task

Create a detailed implementation plan document that provides:

- Clear objectives and scope
- Structured task breakdown
- Parallel execution opportunities
- Success criteria and metrics
- Timeline estimates
- Risk mitigation strategies
- Complete deliverables specification

## Input Requirements

**User Must Provide**:

1. **Activity Type**: [Assessment | Remediation | Documentation | Process Improvement | Workflow Execution | Other]
2. **Activity Name**: Short descriptive name (e.g., "Assessment 4", "Rev 05 Remediation", "Traceability Framework Implementation")
3. **Primary Goal**: What this activity aims to accomplish (1-2 sentences)
4. **Key Inputs**: Documents, standards, or previous work to reference
5. **Expected Outputs**: Files or deliverables to be created
6. **Timeline Target**: Rough estimate or deadline (if applicable)

**Optional Context**:

- Previous similar activities (for comparison)
- Specific constraints or requirements
- Stakeholders or approval requirements
- Related repository policies or standards

## Assessment Activity Types (Critical Distinction)

When generating assessment plans, **clearly distinguish between two fundamentally different scenarios**:

### Type 1: Draft SOP Verification Assessment

**Purpose**: Verify that a **draft SOP is ready to be finalized** and published.

**Scenario**:

- Draft revision exists (e.g., `D0003329_Rev_04_Draft.md`)
- Previous assessment identified gaps in published version (e.g., Assessment 3 found 35 gaps in Rev 03)
- Draft was created to address those gaps
- Assessment verifies gap closure and readiness for publication

**Assessment Approach**:

- **Target**: Draft SOP document
- **Method**: Verify that previously identified gaps have been addressed in the draft
- **Outcome**:
  - ✅ **Pass**: All critical gaps closed, draft ready for finalization → Publish as final version
  - ❌ **Fail**: Gaps remain → Return to draft state for additional remediation
- **Deliverable Focus**: Gap closure tracking, verification evidence, go/no-go recommendation
- **Next Steps if Pass**: Finalize draft → Publish → Archive assessment
- **Next Steps if Fail**: Document remaining gaps → Continue remediation → Re-assess when ready

**Example**:

```
Assessment 4: Verify D0003329_Rev_04_Draft.md
- Assessment 3 found 35 gaps in Rev 03
- Rev 04 Draft created to address those gaps
- Assessment 4 verifies gaps are closed
- If successful: Rev 04 Draft → Rev 04 Final
- If unsuccessful: Rev 04 remains draft, needs more work
```

### Type 2: Published SOP Re-Assessment (Standard Update or Periodic Review)

**Purpose**: Re-assess a **published, in-use SOP** when regulatory standard updates or periodic review required.

**Scenario**:

- No draft exists; current published version is the latest (e.g., `D0003329_Rev_03_Final.md`)
- One of the following triggers:
  - **Standard Update**: New version of regulatory standard released (e.g., IEC 62304:2026)
  - **Periodic Review**: Quality system requires periodic compliance verification
  - **Regulatory Audit**: Preparing for submission or external audit
- Assessment identifies current gaps and proposes recommendations

**Assessment Approach**:

- **Target**: Published SOP (current production version)
- **Method**: Assess compliance against current (possibly updated) standard
- **Outcome**: Gap analysis report with prioritized remediation recommendations
- **Deliverable Focus**: Current state assessment, gap identification, remediation roadmap, projected improvement scenarios
- **Next Steps**:
  - Recommendations approved → Create new draft revision → Plan verification assessment
  - Recommendations deferred → Archive assessment, schedule next periodic review
  - Do nothing → Assessment becomes compliance baseline until next trigger

**Example**:

```
Assessment 4: Re-assess D0003329_Rev_03_Final.md
- IEC 62304:2006+A1:2015 is current standard (no update)
- Periodic review triggered per quality system
- Assessment 3 identified 35 gaps; no remediation performed yet
- Assessment 4 validates/refines those gaps
- Outcome: Recommendations for future Rev 04
- Next Steps: Stakeholders decide whether/when to implement
```

### Key Differences Summary

| Aspect              | Draft Verification                | Published Re-Assessment                          |
| ------------------- | --------------------------------- | ------------------------------------------------ |
| **Target Document** | Draft SOP (e.g., Rev_04_Draft.md) | Published SOP (e.g., Rev_03_Final.md)            |
| **Purpose**         | Verify readiness for publication  | Identify current gaps and recommend improvements |
| **Trigger**         | Draft exists after remediation    | Standard update OR periodic review               |
| **Outcome**         | Go/No-Go decision                 | Gap analysis + recommendations                   |
| **Success Metric**  | % of gaps closed                  | Quality of recommendations, ROI projection       |
| **Next Step**       | Publish OR continue remediation   | Approve recommendations → draft → verify         |
| **Output Focus**    | Verification evidence             | Remediation proposals and roadmap                |

### Plan Generation Guidance by Assessment Type

**For Draft Verification Assessments**:

- Focus objectives on gap closure verification
- Include "Gap Closure Tracking" deliverable showing before/after status
- Success criteria: X% of critical gaps closed, Y% overall gap closure
- Risk: Draft may not be ready (mitigation: document remaining work)
- Post-actions: If pass → finalize draft; if fail → continue remediation

**For Published Re-Assessments**:

- Focus objectives on gap identification and remediation planning
- Include "Gap Analysis and Remediation Recommendations" deliverable
- Include "Projected Compliance Improvement Analysis" showing scenarios
- Success criteria: Quality and actionability of recommendations
- Risk: Recommendations may not be implemented (mitigation: prioritize by ROI/risk)
- Post-actions: Stakeholder decision → implement OR defer OR archive

**Critical**: Always determine which type applies before generating the plan structure. Ask clarifying questions if ambiguous.

## Plan Generation Workflow

### Phase 1: Context Analysis (Required Inputs)

1. **Load Related Documents**
   - Review any referenced previous plans
   - Load applicable repository policies (`.github/instructions/`)
   - Review relevant standards or SOPs
   - Understand repository structure and conventions

2. **Identify Activity Pattern**
   - Determine if this follows an established pattern (e.g., assessment workflow)
   - Identify reusable components from previous similar activities
   - Extract lessons learned from prior executions

3. **Scope Definition**
   - Clarify what's in scope vs. out of scope
   - Identify all required inputs and their availability
   - Map dependencies on other activities or documents

### Phase 2: Plan Structure Generation

Create implementation plan with the following sections:

#### Section 1: Overview

```markdown
## Overview

**Activity Type**: [Type]
**Activity Name**: [Name]
**Planned Date**: [Date or timeframe]
**Status**: ⏳ PLANNED
**Purpose**: [1-2 sentence purpose statement]
```

#### Section 2: Objectives

List 3-7 specific, measurable objectives:

```markdown
## Objectives

[Activity Name] serves to:

1. **[Primary Objective]**: [Description]
2. **[Secondary Objective]**: [Description]
3. **[Tertiary Objective]**: [Description]
   ...
```

#### Section 3: Scope

Define scope including:

- Target documents or systems
- Standards or requirements to be met
- Baseline or previous versions (if applicable)
- Expected improvements or changes

```markdown
## Scope

### Target [Document/System/Process]

- **Item**: [Name/Version]
- **Location**: [Path or reference]
- **Previous Version**: [If applicable]

### [Baseline/Requirements/Standards]

- **[Key metric 1]**: [Value]
- **[Key metric 2]**: [Value]
  ...
```

#### Section 4: Tasks Breakdown

Define all tasks with:

- Task number and name
- Scope and focus areas
- Dependencies
- **Parallel execution opportunities** (critical for optimization)
- Expected outputs

```markdown
## Tasks

### Task 1: [Task Name]

**Dependencies**: [None | Task X, Y]
**Can Run in Parallel With**: [Task numbers or "N/A"]
**Scope**: [Description]
**Focus Areas**:

- [Focus 1]
- [Focus 2]
  **Output**: [Deliverable file/artifact]
  **Estimated Duration**: [Time]

[Repeat for all tasks]
```

**CRITICAL**: Explicitly identify which tasks can run in parallel to optimize execution time.

#### Section 5: Execution Approach

Define phases with clear parallelization strategy:

```markdown
## Execution Approach

### Phase 1: [Phase Name] ([Duration])

**Execution Type**: [Sequential | Parallel]

[If Parallel]:
**Parallel Batch**:

- Task X: [Description]
- Task Y: [Description]
- Task Z: [Description]

**Optimization**: [Expected time savings]

### Phase 2: [Phase Name] ([Duration])

**Dependencies**: [Phase 1 completion | Specific tasks]
**Execution Type**: [Sequential | Parallel]

[Continue for all phases]
```

Include:

- Logical phase grouping
- Dependencies between phases
- Parallelization opportunities within each phase
- Time estimates and optimizations

#### Section 6: Expected Deliverables

Complete specification of all outputs:

```markdown
## Expected Deliverables

### [Category 1] (X files)

1. `[filename.ext]` (~X,XXX words/lines) - [Description]
2. `[filename.ext]` (~X,XXX words/lines) - [Description]

**Total [Category 1] Content**: ~XX,XXX words/lines

### [Category 2] (Y files)

[Repeat structure]

**Grand Total**: X deliverable files, ~XXX,XXX words/lines
```

#### Section 7: Success Criteria

Define measurable success criteria:

```markdown
## Success Criteria

### Completion Criteria

- ✅ [Criterion 1]
- ✅ [Criterion 2]
- ✅ [Criterion 3]

### Quality Criteria

- ✅ [Quality metric 1]
- ✅ [Quality metric 2]

### Performance/Improvement Targets (if applicable)

- **Target 1**: [Metric and threshold]
- **Target 2**: [Metric and threshold]
```

#### Section 8: Timeline Estimate

Provide detailed time breakdown:

```markdown
## Timeline Estimate

**Total Estimated Duration**: X-Y hours

### Detailed Breakdown

- **Phase 1**: X minutes
  - [Subtask]: X minutes
  - [Subtask]: X minutes

- **Phase 2**: X hours
  - [Subtask]: X minutes
  - [Subtask]: X minutes

**Optimization Opportunities**: [Note any parallelization possibilities and time savings]
```

#### Section 9: Risk Factors and Mitigations

Identify potential risks:

```markdown
## Risk Factors and Mitigations

### Risk 1: [Risk Name]

**Risk**: [Description of what could go wrong]
**Mitigation**: [How to prevent or address]

### Risk 2: [Risk Name]

**Risk**: [Description]
**Mitigation**: [Prevention/resolution strategy]

[3-5 key risks]
```

#### Section 10: Dependencies

List all required resources:

```markdown
## Dependencies

### Required Documents

- ✅ **[Document 1]**: `[path]` (available/status)
- ⚠️ **[Document 2]**: `[path]` (to be created/status)

### Required Tools

- [Tool 1]
- [Tool 2]

### Prerequisites

- [Prerequisite 1]
- [Prerequisite 2]
```

#### Section 11: Output Location

Specify where deliverables will be created:

```markdown
## Output Location

All deliverables will be created in:
```

[folder-structure]
├── [file1]
├── [file2]
└── [fileN]

```

[Include AI logs structure if applicable]
```

#### Section 12: Post-Activity Actions

Define what happens after completion:

```markdown
## Post-Activity Actions

Upon completion:

1. **[Action 1]**: [Description]
2. **[Action 2]**: [Description]
3. **[Action 3]**: [Description]
```

#### Section 13: Governance

Include ownership and contacts:

```markdown
## Contact and Governance

**Activity Owner**: [Role/Person]
**Stakeholders**: [List]
**Approval Authority**: [Role/Person]

For questions or clarifications, refer to:

- [Reference 1]: `[path]`
- [Reference 2]: `[path]`
```

### Phase 3: Optimization Analysis

After generating the plan structure:

1. **Identify Parallel Execution Opportunities**
   - Scan all tasks for dependencies
   - Group independent tasks that can run concurrently
   - Calculate time savings from parallelization
   - Update execution approach with parallel batches

2. **Validate Completeness**
   - All inputs identified and available (or marked as TBD)
   - All outputs specified with acceptance criteria
   - All dependencies mapped
   - All risks identified with mitigations

3. **Add Repository Policy Compliance**
   - Include AI provenance metadata requirements
   - Reference applicable instruction files
   - Include conversation logging requirements
   - Specify README update requirements (if creating new artifacts)

### Phase 4: Meta-Information

Add plan metadata at the end:

```markdown
---

**Plan Version**: 1.0
**Created**: [Date]
**Status**: ⏳ READY FOR EXECUTION
```

## Plan File Placement

Save the generated plan to appropriate location:

**For Assessments**: `assessments/assessment.X/ASSESSMENT_PLAN.md` or `assessments/assessment.X/[ACTIVITY]_PLAN.md`
**For Remediations**: `sop/remediation-plans/[ACTIVITY]_PLAN.md` or in relevant project folder
**For Documentation Projects**: `docs/plans/[ACTIVITY]_PLAN.md`
**For General Activities**: `[relevant-folder]/[ACTIVITY]_PLAN.md`

## AI Provenance for Generated Plan

The plan document itself should include AI provenance metadata:

```markdown
---
ai_generated: true
model: "[model-used]"
operator: "[operator-id]"
chat_id: "[unique-chat-id]"
prompt: |
  Create implementation plan for [activity] using .github/prompts/create-implementation-plan.prompt.md
started: "[ISO8601-timestamp]"
ended: "[ISO8601-timestamp]"
task_durations:
  - task: "plan generation"
    duration: "HH:MM:SS"
total_duration: "HH:MM:SS"
ai_log: "ai-logs/YYYY/MM/DD/[chat-id]/conversation.md"
source: ".github/prompts/create-implementation-plan.prompt.md"
---
```

## Quality Checklist

Before finalizing the plan, verify:

- [ ] **Assessment Type Correctly Identified** (if applicable): Draft Verification vs. Published Re-Assessment clearly determined
- [ ] All required sections present
- [ ] Objectives are specific and measurable
- [ ] All tasks have clear outputs
- [ ] Dependencies are accurately mapped
- [ ] Parallel execution opportunities identified
- [ ] Timeline estimates are realistic
- [ ] Success criteria are testable
- [ ] Risks have mitigation strategies
- [ ] All required inputs are identified
- [ ] Output location is specified
- [ ] **Post-activity actions match assessment type** (publish vs. recommend for assessments)
- [ ] Repository policies are followed
- [ ] AI provenance metadata is complete

## Example Usage Scenarios

### Scenario 1a: Draft SOP Verification Assessment

**Input**:

```
Activity Type: Assessment
Activity Name: Assessment 5 - Rev 04 Draft Verification
Assessment Type: Draft Verification
Primary Goal: Verify D0003329_Rev_04_Draft.md has addressed all 35 gaps from Assessment 3 and is ready for publication
Key Inputs: D0003329_Rev_04_Draft.md, Assessment 3 gap list (35 gaps), IEC 62304:2006+A1:2015 standard
Expected Outputs: 8 clause assessments, gap closure tracking report, verification summary, go/no-go recommendation
Timeline Target: 2 hours with parallelization
Context: Assessment 3 identified 35 gaps in Rev 03. Rev 04 Draft created to address them. This assessment verifies closure.
```

**Output**: Complete assessment plan targeting the draft document, focusing on verification that gaps are closed, with clear go/no-go decision criteria and publish/continue-remediation next steps.

### Scenario 1b: Published SOP Re-Assessment (Standard Update)

**Input**:

```
Activity Type: Assessment
Activity Name: Assessment 6 - Rev 04 Re-Assessment for IEC 62304:2026
Assessment Type: Published SOP Re-Assessment
Primary Goal: Re-assess D0003329_Rev_04_Final.md against new IEC 62304:2026 standard requirements
Key Inputs: D0003329_Rev_04_Final.md (current published version), IEC 62304:2026 (new standard), Assessment 5 results (baseline)
Expected Outputs: Compliance assessment vs. 2026 standard, gap analysis, remediation recommendations, projected improvement scenarios
Timeline Target: 3 hours (new standard requires detailed review)
Context: IEC 62304:2026 released with new AI/ML requirements. Need to assess current SOP against updated standard.
```

**Output**: Complete assessment plan targeting the published document, identifying new gaps introduced by standard update, proposing specific remediation recommendations, and modeling scenarios for achieving compliance with new requirements.

### Scenario 1c: Published SOP Re-Assessment (Periodic Review)

**Input**:

```
Activity Type: Assessment
Activity Name: Assessment 4 - Rev 03 Periodic Re-Assessment
Assessment Type: Published SOP Re-Assessment
Primary Goal: Validate and refine Assessment 3 findings for D0003329_Rev_03_Final.md, develop detailed remediation roadmap
Key Inputs: D0003329_Rev_03_Final.md (current published version), Assessment 3 findings (35 gaps, 61% compliance), IEC 62304:2006+A1:2015
Expected Outputs: Validated gap analysis, remediation recommendations, phased implementation roadmap, ROI projections
Timeline Target: 1.5 hours with parallelization
Context: Assessment 3 completed 6 months ago. No remediation performed yet. Quality system requires re-validation before planning Rev 04.
```

**Output**: Complete assessment plan re-assessing the published Rev 03, validating previous gaps remain relevant, proposing specific changes for future Rev 04, and providing decision-making framework for stakeholders.

### Scenario 2: Remediation Plan

**Input**:

```
Activity Type: Remediation
Activity Name: Rev 05 Gap Remediation
Primary Goal: Address remaining gaps from Assessment 4 to achieve 95% compliance
Key Inputs: Assessment 4 gap list, D0003329_Rev_04_Final.md, remediation templates
Expected Outputs: Updated D0003329_Rev_05_Draft.md with all gaps closed
Timeline Target: 40 hours development + 20 hours review
```

**Output**: Remediation plan with gap-by-gap remediation strategy, implementation steps, and verification approach.

### Scenario 3: Documentation Project Plan

**Input**:

```
Activity Type: Documentation
Activity Name: IEC 62304 Training Materials
Primary Goal: Create comprehensive training materials for IEC 62304 compliance
Key Inputs: D0003329_Rev_04_Final.md, IEC 62304 standard, existing training slides
Expected Outputs: Training presentation, hands-on exercises, assessment quiz, trainer guide
Timeline Target: 3 weeks
```

**Output**: Documentation project plan with content development tasks, review cycles, and deployment strategy.

## Customization Guidelines

When creating domain-specific implementation plans:

1. **Adapt Section Emphasis**: Some sections may be more detailed for certain activity types
2. **Add Domain-Specific Sections**: Include specialized sections as needed (e.g., "Regulatory Considerations" for compliance activities)
3. **Scale Appropriately**: Simple activities may have abbreviated plans; complex multi-phase projects need detailed breakdown
4. **Leverage Patterns**: Reuse structures from similar previous activities
5. **Maintain Consistency**: Follow repository conventions for file naming, folder structure, metadata

## Output Format

Generate the complete implementation plan as a well-formatted Markdown document with:

- Clear hierarchical structure (##, ###, ####)
- Consistent use of lists, tables, and code blocks
- Emoji indicators for status (✅, ⚠️, ❌, ⏳, 🔍)
- Professional tone suitable for technical documentation
- Cross-references to related documents
- Proper Markdown link syntax for all file references

---

**Prompt Version**: 1.0
**Created**: April 1, 2026
**Purpose**: Meta-prompt for generating implementation plans across various activity types
**Usage**: Provide activity details to generate comprehensive, actionable implementation plan
