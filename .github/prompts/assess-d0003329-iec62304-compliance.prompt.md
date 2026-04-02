---
ai_generated: true
model: "anthropic/claude-3.5-sonnet@2024-10-22"
operator: "johnmillerATcodemag-com"
chat_id: "assess-d0003329-compliance-prompt-20251216"
prompt: |
  Create a prompt file for assessing D0003329_Rev_03_Final.md for IEC 62304 compliance issues
started: "2025-12-16T00:00:00Z"
ended: "2025-12-16T00:00:00Z"
task_durations:
  - task: "prompt file creation"
    duration: "00:02:00"
total_duration: "00:02:00"
ai_log: "ai-logs/2025/12/16/assess-d0003329-compliance-prompt-20251216/conversation.md"
source: "johnmillerATcodemag-com"
applyTo: "**/*.prompt.md"
---

# Prompt: IEC 62304 Compliance Assessment for D0003329 Rev 03

## Core Task

Assess D0003329_Rev_03_Final.md (Acme Global Work Instruction for Software Development) for complete IEC 62304 compliance across all software safety classes (A, B, C).

## Required Input Files

**CRITICAL**: Load these files before starting analysis:

1. **#file:D0003329_Rev_03_Final.md** - Work instruction being assessed (PRIMARY)
2. **#file:BSEN-62304.md** - IEC 62304 standard reference (REQUIRED)
3. **#file:D0003098_Rev_05_Final.md** - Related procedures (CONTEXTUAL)

## Analysis Workflow

Execute in sequence:

### Phase 1: Document Loading & Context Establishment

1. Read D0003329_Rev_03_Final.md completely
2. Load BSEN-62304.md for reference
3. Identify D0003329 document structure and section organization
4. Extract all IEC 62304 "shall" requirements from BSEN-62304.md

### Phase 2: Section-by-Section Compliance Mapping

For each IEC 62304 section (4.4, 5.1-5.8, 6, 7, 8, 9), execute:

### Phase 2: Section-by-Section Compliance Mapping

For each IEC 62304 section (4.4, 5.1-5.8, 6, 7, 8, 9), execute:

**Step 1**: Extract all "shall" requirements from IEC 62304 section
**Step 2**: Search D0003329 for corresponding requirement coverage
**Step 3**: Classify coverage status:

- ✅ COMPLIANT: Requirement fully addressed with adequate detail
- ⚠️ PARTIAL: Requirement mentioned but lacks specificity/clarity
- ❌ MISSING: Requirement not addressed or inadequate

**Step 4**: Document finding with:

- IEC 62304 section reference (§X.Y.Z format)
- D0003329 section reference (if applicable)
- Gap description (50-100 words)
- Regulatory risk level (Critical/Significant/Minor)
- Safety class impact (A, B, C, or All)

### Phase 3: Cross-Cutting Analysis

Assess these themes across all lifecycle phases:

1. **Traceability Mechanisms**
   - Requirements ↔ Design linkage
   - Design ↔ Test coverage
   - Risk Controls ↔ Verification
   - SOUP ↔ Risk assessment

2. **Documentation Deliverables**
   - Required content specified? (Yes/No/Partial)
   - Acceptance criteria defined? (Yes/No/Partial)
   - Review/approval process clear? (Yes/No/Partial)

3. **Safety Classification Differentiation**
   - Class A, B, C requirements distinguished?
   - Appropriate rigor levels specified?

4. **Risk Management Integration**
   - ISO 14971 integration at each lifecycle phase?
   - Risk control measure verification specified?

### Phase 4: Gap Prioritization & Remediation Planning

Organize findings into three tiers:

**CRITICAL GAPS** (Regulatory Blockers)

- Missing mandatory "shall" requirements
- Safety-critical process omissions
- Traceability failures

**SIGNIFICANT GAPS** (Partial Compliance)

- Unclear implementation guidance
- Insufficient detail for safety classes
- Missing acceptance criteria

**MINOR GAPS** (Best Practice)

- Clarification opportunities
- Process optimization suggestions

## Output Structure

Generate report using this exact format:

### 📋 Executive Summary (200-300 words)

- Overall compliance status: [Compliant/Substantially Compliant/Non-Compliant]
- Total gaps by severity: Critical (X), Significant (Y), Minor (Z)
- Top 3 critical issues requiring immediate attention
- Regulatory risk assessment
- High-level remediation roadmap

### ✅ IEC 62304 Section-by-Section Findings

**For EACH IEC 62304 section (4.4, 5.1-5.8, 6, 7, 8, 9):**

#### Section [X.Y]: [Section Title]

**Compliance Status**: [Compliant/Partial/Non-Compliant]

**Compliant Elements** ✅

- [IEC §X.Y.Z] - [Brief description] → D0003329 §[reference]
- [IEC §X.Y.Z] - [Brief description] → D0003329 §[reference]

**Partial Compliance** ⚠️

- [IEC §X.Y.Z] - [Requirement] → D0003329 §[reference]
  - **Gap**: [What's missing or unclear]
  - **Risk**: [Critical/Significant/Minor]
  - **Classes Affected**: [A/B/C/All]

**Non-Compliant/Missing** ❌

- [IEC §X.Y.Z] - [Requirement] → **Not addressed in D0003329**
  - **Gap**: [What's completely missing]
  - **Risk**: [Critical/Significant/Minor]
  - **Classes Affected**: [A/B/C/All]

### 🔍 Gap Analysis by Priority

#### CRITICAL GAPS (Must Fix for Compliance)

#### CRITICAL GAPS (Must Fix for Compliance)

| #   | IEC § | Requirement              | D0003329 § | Gap Description     | Classes | Remediation Priority |
| --- | ----- | ------------------------ | ---------- | ------------------- | ------- | -------------------- |
| 1   | X.Y.Z | [Brief requirement text] | Missing    | [What's absent]     | All     | Immediate            |
| 2   | X.Y.Z | [Brief requirement text] | §N.N       | [What's inadequate] | B,C     | Immediate            |

#### SIGNIFICANT GAPS (Partial Compliance)

| #   | IEC § | Requirement              | D0003329 § | Gap Description            | Classes | Remediation Priority |
| --- | ----- | ------------------------ | ---------- | -------------------------- | ------- | -------------------- |
| 3   | X.Y.Z | [Brief requirement text] | §N.N       | [What needs clarification] | All     | High                 |

#### MINOR GAPS (Best Practice Improvements)

| #   | Area    | Improvement Opportunity   | Current State | Suggested Enhancement | Priority |
| --- | ------- | ------------------------- | ------------- | --------------------- | -------- |
| X   | [Topic] | [Opportunity description] | [Current]     | [Recommendation]      | Low      |

### 💡 Remediation Recommendations

**For each gap identified above, provide:**

#### Gap [Number]: [Short Title]

**IEC 62304 Requirement**: §X.Y.Z - [Full requirement text]

**Current State in D0003329**: [What document currently says or lacks]

**Compliance Risk**: [Critical/Significant/Minor] - [Why this matters]

**Recommended Action**:

```
[Specific text to add to D0003329, or]
[Structural change to implement, or]
[Process clarification needed]
```

**Affected Safety Classes**: [A/B/C/All]

**Implementation Steps**:

1. [Concrete action step 1]
2. [Concrete action step 2]
3. [Verification method]

**Success Criteria**: [How to verify compliance achieved]

### 📝 Cross-Cutting Assessments

#### Traceability Framework

| Traceability Link            | Required by IEC | Specified in D0003329? | Adequacy Rating | Gap Description |
| ---------------------------- | --------------- | ---------------------- | --------------- | --------------- |
| Requirements → Design        | §5.3.6          | Yes/No/Partial         | 1-5             | [Details]       |
| Design → Implementation      | §5.5.1          | Yes/No/Partial         | 1-5             | [Details]       |
| Requirements → Tests         | §5.7.1          | Yes/No/Partial         | 1-5             | [Details]       |
| Risk Controls → Verification | §7.3.3          | Yes/No/Partial         | 1-5             | [Details]       |
| SOUP → Risk Assessment       | §8.1.2          | Yes/No/Partial         | 1-5             | [Details]       |

#### Documentation Deliverables Matrix

| Deliverable                    | IEC Requirement | D0003329 Coverage | Content Adequacy | Acceptance Criteria | Review Process |
| ------------------------------ | --------------- | ----------------- | ---------------- | ------------------- | -------------- |
| Software Development Plan      | §5.1.1          | §[X]              | ✅/⚠️/❌         | ✅/⚠️/❌            | ✅/⚠️/❌       |
| Requirements Specification     | §5.2.1          | §[X]              | ✅/⚠️/❌         | ✅/⚠️/❌            | ✅/⚠️/❌       |
| Architecture Design            | §5.3.1          | §[X]              | ✅/⚠️/❌         | ✅/⚠️/❌            | ✅/⚠️/❌       |
| Detailed Design (Class B/C)    | §5.4.1          | §[X]              | ✅/⚠️/❌         | ✅/⚠️/❌            | ✅/⚠️/❌       |
| Unit Test Documentation        | §5.5.5          | §[X]              | ✅/⚠️/❌         | ✅/⚠️/❌            | ✅/⚠️/❌       |
| Integration Test Documentation | §5.6.6          | §[X]              | ✅/⚠️/❌         | ✅/⚠️/❌            | ✅/⚠️/❌       |
| System Test Documentation      | §5.7.5          | §[X]              | ✅/⚠️/❌         | ✅/⚠️/❌            | ✅/⚠️/❌       |
| Risk Management File           | §7.1.1          | §[X]              | ✅/⚠️/❌         | ✅/⚠️/❌            | ✅/⚠️/❌       |

#### Safety Classification Differentiation

| Lifecycle Phase       | Class A Requirements Clear? | Class B Requirements Clear? | Class C Requirements Clear? | Gap Description |
| --------------------- | --------------------------- | --------------------------- | --------------------------- | --------------- |
| Requirements Analysis | ✅/⚠️/❌                    | ✅/⚠️/❌                    | ✅/⚠️/❌                    | [Details]       |
| Architectural Design  | ✅/⚠️/❌                    | ✅/⚠️/❌                    | ✅/⚠️/❌                    | [Details]       |
| Detailed Design       | N/A                         | ✅/⚠️/❌                    | ✅/⚠️/❌                    | [Details]       |
| Unit Testing          | ✅/⚠️/❌                    | ✅/⚠️/❌                    | ✅/⚠️/❌                    | [Details]       |
| Integration Testing   | ✅/⚠️/❌                    | ✅/⚠️/❌                    | ✅/⚠️/❌                    | [Details]       |

## Quality Control Checklist

Before finalizing report, verify:

- [ ] All 10 IEC 62304 sections analyzed (4.4, 5.1-5.8, 6, 7, 8, 9)
- [ ] Every finding includes specific IEC §X.Y.Z citation
- [ ] Every gap includes D0003329 section reference or "Missing"
- [ ] Regulatory risk level assigned to each gap
- [ ] Safety class impact identified for each finding
- [ ] Remediation recommendations are actionable and specific
- [ ] Traceability assessment completed across all required links
- [ ] Documentation deliverables matrix fully populated
- [ ] Safety classification differentiation assessed
- [ ] Executive summary accurately reflects detailed findings
- [ ] All tables are complete with no [TBD] placeholders
- [ ] Exact regulatory terminology used throughout

## Output File Requirements

**CRITICAL**: Save the complete assessment report to file:

**File Path**: `assessments/D0003329_Rev_03_IEC62304_Compliance_Assessment_YYYY-MM-DD.md`

**File Naming Convention**:

- Replace `YYYY-MM-DD` with actual assessment date (e.g., `2025-12-16`)
- Example: `assessments/D0003329_Rev_03_IEC62304_Compliance_Assessment_2025-12-16.md`

**File Creation**:

- Create the `assessments/` folder if it does not exist
- Save the complete structured markdown report to this file
- Include all sections: Executive Summary, Section-by-Section Findings, Gap Analysis, Remediation Recommendations, Cross-Cutting Assessments
- Preserve all formatting, tables, and structure
- Add file metadata in front matter including assessment date, assessor, and document version

**File Front Matter Template**:

```yaml
---
assessment_type: "IEC 62304 Compliance Assessment"
target_document: "D0003329_Rev_03_Final.md"
reference_standard: "IEC 62304 (BS EN 62304:2006+A1:2015)"
assessment_date: "YYYY-MM-DD"
assessor: "Medical-Device-Design-Controls-Expert"
compliance_status: "[Compliant/Substantially Compliant/Non-Compliant]"
total_gaps: "[Number]"
critical_gaps: "[Number]"
significant_gaps: "[Number]"
minor_gaps: "[Number]"
---
```

## Success Metrics

Assessment is complete when:

1. ✅ All IEC 62304 lifecycle sections covered systematically
2. ✅ Every "shall" requirement from standard addressed
3. ✅ Specific section citations provided for all findings
4. ✅ Clear compliance status assigned (Compliant/Partial/Missing)
5. ✅ Actionable remediation guidance for every gap
6. ✅ Priority/risk levels support implementation planning
7. ✅ Traceability framework completely assessed
8. ✅ Documentation deliverables adequacy evaluated
9. ✅ Output ready for regulatory review or audit defense
10. ✅ Report length: 3000-5000 words (excluding tables)
11. ✅ **Complete assessment report saved to `assessments/` folder with proper filename and front matter**

---

**Analysis Mode**: Medical-Device-Design-Controls-Expert
**Required Model**: Claude Sonnet 4.5
**Estimated Duration**: 45-60 minutes
**Output Format**: Structured Markdown Report

---

**Prompt Version**: 2.0.0 (Optimized for AI Agent Execution)
**Created**: 2025-12-16
**Optimization Focus**: Structured workflow, clear outputs, actionable steps
**Target Document**: D0003329_Rev_03_Final.md
**Reference Standard**: IEC 62304 (BS EN 62304)
**Analysis Mode**: Medical-Device-Design-Controls-Expert
**Required Model**: Claude Sonnet 4.5
