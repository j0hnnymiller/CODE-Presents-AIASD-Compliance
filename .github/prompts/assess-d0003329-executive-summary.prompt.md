---
ai_generated: true
model: "anthropic/claude-3.5-sonnet@2024-10-22"
operator: "johnmillerATcodemag-com"
chat_id: "assess-d0003329-modular-prompts-20251216"
prompt: |
  Create modular assessment prompts for D0003329 IEC 62304 compliance by clause
started: "2025-12-16T00:00:00Z"
ended: "2025-12-16T00:00:00Z"
task_durations:
  - task: "modular prompt creation"
    duration: "00:10:00"
total_duration: "00:10:00"
ai_log: "ai-logs/2025/12/16/assess-d0003329-modular-prompts-20251216/conversation.md"
source: "johnmillerATcodemag-com"
applyTo: "**/*.prompt.md"
---

# Prompt: IEC 62304 Compliance Executive Summary and Gap Analysis

## Core Task

Create a consolidated executive summary and comprehensive gap analysis for D0003329_Rev_03_Final.md based on all individual clause assessments.

## Required Input Files

**Load these assessment files from assessments/assessment.2:**

1. **#file:assessments/assessment.2/D0003329_REV_03_Final.Analysis.Clause4.4.md** - Legacy Software assessment
2. **#file:assessments/assessment.2/D0003329_REV_03_Final.Analysis.Clause6.md** - Software Maintenance assessment
3. **#file:assessments/assessment.2/D0003329_REV_03_Final.Analysis.Clause7.md** - Risk Management assessment
4. **#file:assessments/assessment.2/D0003329_REV_03_Final.Analysis.Clause8.md** - Configuration Management assessment
5. **#file:assessments/assessment.2/D0003329_REV_03_Final.Analysis.Clause9.md** - Problem Resolution assessment

**Note**: Clause 5 (Software Development) assessment is located in assessment.1 folder if needed for reference.

## Analysis Scope

Synthesize findings across all IEC 62304 clauses:

- Clause 4.4: Legacy Software (5 requirements)
- Clause 5: Software Development Process (44 requirements)
- Clause 6: Software Maintenance Process (~12 requirements)
- Clause 7: Software Risk Management Process (~13 requirements)
- Clause 8: Configuration Management Process (~8 requirements)
- Clause 9: Problem Resolution Process (~8 requirements)

## Synthesis Methodology

1. **Extract** compliance metrics from each clause assessment
2. **Aggregate** findings into overall compliance status
3. **Prioritize** gaps by criticality and regulatory risk
4. **Identify** cross-cutting themes and systemic issues
5. **Develop** high-level remediation roadmap

## Output Structure

Generate summary file: `assessments/assessment.2/D0003329_REV_03_Final.IEC62304_Executive_Summary.md`

### File Content Template

```markdown
---
assessment_type: "IEC 62304 Compliance Executive Summary"
target_document: "D0003329_Rev_03_Final.md"
reference_standard: "IEC 62304 (BS EN 62304:2006+A1:2015)"
assessment_date: "2025-12-16"
assessor: "Medical-Device-Design-Controls-Expert"
overall_status: "[Compliant/Substantially Compliant/Non-Compliant]"
---

# IEC 62304 Compliance Executive Summary

## D0003329 Rev 03 - Software Development Work Instruction

**Assessment Date**: December 16, 2025
**Assessor**: Medical-Device-Design-Controls-Expert
**Standard**: BS EN 62304:2006+A1:2015 (IEC 62304)
**Overall Status**: [Compliant/Substantially Compliant/Non-Compliant]

---

## 📋 Executive Summary

### Overall Compliance Status

**Total IEC 62304 Requirements**: [X]
**Fully Compliant**: [X] ([X]%)
**Partial Compliance**: [X] ([X]%)
**Non-Compliant/Missing**: [X] ([X]%)

### Regulatory Assessment

[200-300 word assessment of overall regulatory posture]

### Top 5 Critical Issues

1. **[Issue Title]** (IEC §X.Y.Z)

   - **Risk**: [Critical/Significant]
   - **Impact**: [Description]
   - **Remediation**: [High-level action]

2. [Continue for top 5...]

### Compliance by Clause

| Clause    | Title                    | Total Reqs | Compliant | Partial | Missing | Status     |
| --------- | ------------------------ | ---------- | --------- | ------- | ------- | ---------- |
| 4.4       | Legacy Software          | X          | X         | X       | X       | [✅/⚠️/❌] |
| 5         | Software Development     | 44         | X         | 14      | 0       | ⚠️         |
| 6         | Software Maintenance     | X          | X         | X       | X       | [✅/⚠️/❌] |
| 7         | Risk Management          | X          | X         | X       | X       | [✅/⚠️/❌] |
| 8         | Configuration Management | X          | X         | X       | X       | [✅/⚠️/❌] |
| 9         | Problem Resolution       | X          | X         | X       | X       | [✅/⚠️/❌] |
| **Total** | **All Clauses**          | **X**      | **X**     | **X**   | **X**   | [✅/⚠️/❌] |

---

## 🔍 Detailed Gap Analysis by Priority

### CRITICAL GAPS (Regulatory Blockers)

Must be addressed for compliance. Organized by clause:

| #   | Clause | IEC §  | Requirement              | D0003329 § | Gap Description     | Classes | Priority  |
| --- | ------ | ------ | ------------------------ | ---------- | ------------------- | ------- | --------- |
| 1   | [X]    | [§X.Y] | [Brief requirement text] | Missing    | [What's absent]     | All     | Immediate |
| 2   | [X]    | [§X.Y] | [Brief requirement text] | §X.X       | [What's inadequate] | B,C     | Immediate |
| ... | ...    | ...    | ...                      | ...        | ...                 | ...     | ...       |

**Total Critical Gaps**: [X]

---

### SIGNIFICANT GAPS (Partial Compliance)

Require clarification or enhancement. Organized by clause:

| #   | Clause | IEC §  | Requirement              | D0003329 § | Gap Description            | Classes | Priority |
| --- | ------ | ------ | ------------------------ | ---------- | -------------------------- | ------- | -------- |
| 1   | [X]    | [§X.Y] | [Brief requirement text] | §X.X       | [What needs clarification] | All     | High     |
| ... | ...    | ...    | ...                      | ...        | ...                        | ...     | ...      |

**Total Significant Gaps**: [X]

---

### MINOR GAPS (Best Practice Improvements)

Opportunities for process optimization. Organized by clause:

| #   | Clause | Area    | Improvement Opportunity   | Current State | Suggested Enhancement | Priority |
| --- | ------ | ------- | ------------------------- | ------------- | --------------------- | -------- |
| 1   | [X]    | [Topic] | [Opportunity description] | [Current]     | [Recommendation]      | Low      |
| ... | ...    | ...     | ...                       | ...           | ...                   | ...      |

**Total Minor Gaps**: [X]

---

## 🎯 Cross-Cutting Themes

### Theme 1: [e.g., Traceability Framework Gaps]

**Affected Clauses**: [List clauses]

**Issue**: [Description of systemic issue]

**Impact**: [How this affects compliance]

**Recommendation**: [High-level remediation approach]

---

### Theme 2: [e.g., Documentation Completeness]

[Continue for each cross-cutting theme...]

---

## 💡 Remediation Roadmap

### Phase 1: Critical Gaps (Immediate - 0-30 days)

**Objective**: Address regulatory blockers

**Actions**:

1. [Specific action for critical gap 1]
2. [Specific action for critical gap 2]
3. [Continue...]

**Success Criteria**: [How to verify completion]

---

### Phase 2: Significant Gaps (High Priority - 30-90 days)

**Objective**: Resolve partial compliance issues

**Actions**:

1. [Specific action]
2. [Continue...]

**Success Criteria**: [How to verify completion]

---

### Phase 3: Minor Gaps (Continuous Improvement - 90+ days)

**Objective**: Optimize processes and documentation

**Actions**:

1. [Specific action]
2. [Continue...]

**Success Criteria**: [How to verify completion]

---

## 📊 Compliance Summary by Safety Class

### Class A Software Requirements

| Aspect      | Total Reqs | Compliant | Partial | Missing | Status     |
| ----------- | ---------- | --------- | ------- | ------- | ---------- |
| Development | X          | X         | X       | X       | [✅/⚠️/❌] |
| Maintenance | X          | X         | X       | X       | [✅/⚠️/❌] |
| Risk Mgmt   | X          | X         | X       | X       | [✅/⚠️/❌] |
| Config Mgmt | X          | X         | X       | X       | [✅/⚠️/❌] |
| Problem Res | X          | X         | X       | X       | [✅/⚠️/❌] |

### Class B Software Requirements

[Similar table...]

### Class C Software Requirements

[Similar table...]

---

## 📚 Supporting Documentation Assessment

### Template Adequacy

| Template | Document     | Purpose               | IEC Requirements Covered | Adequacy   | Gaps   |
| -------- | ------------ | --------------------- | ------------------------ | ---------- | ------ |
| D0004168 | SDP          | Software Dev Plan     | §5.1                     | [✅/⚠️/❌] | [List] |
| D0004169 | SRS          | Requirements Spec     | §5.2                     | [✅/⚠️/❌] | [List] |
| D0004197 | Architecture | Software Architecture | §5.3                     | [✅/⚠️/❌] | [List] |
| D0017986 | Detailed     | Detailed Design       | §5.4                     | [✅/⚠️/❌] | [List] |
| D0004170 | CM Plan      | Config Management     | §8                       | [✅/⚠️/❌] | [List] |
| D0004171 | Maint Plan   | Maintenance Plan      | §6                       | [✅/⚠️/❌] | [List] |
| D0004198 | Anomaly      | Anomaly Reports       | §9                       | [✅/⚠️/❌] | [List] |
| ...      | ...          | ...                   | ...                      | ...        | ...    |

**Note**: Template assessment based on work instruction references. Actual template content should be reviewed separately.

---

## 🔗 Reference Documents

### Individual Clause Assessments

- [Clause 4.4 Assessment](D0003329_REV_03_Final.Analysis.Clause4.4.md) - Legacy Software
- [Clause 6 Assessment](D0003329_REV_03_Final.Analysis.Clause6.md) - Software Maintenance
- [Clause 7 Assessment](D0003329_REV_03_Final.Analysis.Clause7.md) - Risk Management
- [Clause 8 Assessment](D0003329_REV_03_Final.Analysis.Clause8.md) - Configuration Management
- [Clause 9 Assessment](D0003329_REV_03_Final.Analysis.Clause9.md) - Problem Resolution

---

## 📝 Recommendations

### Immediate Actions (Next 30 Days)

1. **[Action 1]**: [Description and rationale]
2. **[Action 2]**: [Description and rationale]
3. [Continue...]

### Short-Term Actions (30-90 Days)

1. **[Action]**: [Description]
2. [Continue...]

### Long-Term Actions (90+ Days)

1. **[Action]**: [Description]
2. [Continue...]

---

## ✅ Audit Readiness Assessment

**Current State**: [Ready/Needs Work/Not Ready]

**Strengths**:

- [List compliance strengths]

**Weaknesses**:

- [List areas requiring attention before audit]

**Recommended Pre-Audit Actions**:

1. [Specific action]
2. [Continue...]

---

_End of Executive Summary_

---

## Appendix: Compliance Metrics

### Detailed Requirements Coverage

[Include detailed breakdown if helpful]

### Gap Distribution by Clause

[Visual representation or detailed table]

### Safety Class-Specific Findings

[Additional detail on Class A, B, C specific gaps]
```

## Quality Requirements

- [ ] All six clause assessments reviewed and synthesized
- [ ] Overall compliance percentage calculated accurately
- [ ] Critical gaps prioritized and actionable
- [ ] Cross-cutting themes identified
- [ ] Remediation roadmap provides clear phases
- [ ] Safety class-specific analysis included
- [ ] Template adequacy assessed
- [ ] Audit readiness evaluated
- [ ] Output saved to `assessments/` folder
- [ ] Front matter metadata complete

## Success Criteria

Executive summary complete when:

1. All clause findings synthesized
2. Overall compliance status determined
3. Top critical issues clearly identified
4. Actionable remediation roadmap provided
5. Audit readiness assessed
6. Cross-cutting themes documented
7. File saved with proper naming convention
8. Summary is executive-ready (suitable for management review)

---

**Analysis Mode**: Medical-Device-Design-Controls-Expert
**Analysis Mode**: Medical-Device-Design-Controls-Expert
**Required Model**: Claude Sonnet 4.5
**Estimated Duration**: 20-30 minutes
**Output File**: `assessments/assessment.2/D0003329_REV_03_Final.IEC62304_Executive_Summary.md`
**Dependencies**: All individual clause assessments in assessment.2 folder must be completed first
