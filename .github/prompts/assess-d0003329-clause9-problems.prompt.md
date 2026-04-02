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

# Prompt: IEC 62304 Clause 9 (Problem Resolution) Compliance Assessment

## Core Task

Assess D0003329_Rev_03_Final.md for compliance with IEC 62304 Clause 9 (Software Problem Resolution Process) requirements.

## Required Input Files

**Load these files before analysis:**

1. **#file:D0003329_Rev_03_Final.md** - Work instruction §6.13 (Problem Resolution)
2. **#file:BSEN-62304.md** - IEC 62304 standard Clause 9 reference
3. **#file:D0003098_Rev_05_Final.md** - Related procedures (contextual)

## Analysis Scope

Assess IEC 62304 Clause 9 requirements:

- **§9.1**: Prepare problem reports
- **§9.2**: Investigate the problem
- **§9.3**: Advise relevant parties
- **§9.4**: Use change control process
- **§9.5**: Maintain records
- **§9.6**: Analyze problems for trends
- **§9.7**: Verify problem resolution (including regression testing)
- **§9.8**: Test documentation contents

### Integration and Systems-Level Assessment

Additionally evaluate:

- **D0003098 Integration**:

  - Integration with D0003325 (Complaint Handling) for post-market problems
  - Integration with D0003293 (Post-Market Surveillance) for problem trending
  - CAPA system integration for problem resolution
  - Problem resolution within design change process (D0003336)

- **FDA Design Control Expectations**:

  - 21 CFR 820.100 CAPA integration
  - Problem report documentation in DHF/DMR as appropriate
  - Post-market problem resolution and regulatory reporting
  - Trend analysis requirements for identifying systemic issues

- **Practical Implementation**:

  - Problem report template/tool requirements (D0004198 reference)
  - Defect tracking system requirements (Jira, Azure DevOps)
  - Problem prioritization criteria (Critical/Major/Minor)
  - Root cause analysis methodology
  - Regression testing scope determination
  - Verification of fixes procedure

- **Cross-Document Consistency**:
  - Configuration management integration (§6.12) for change implementation
  - Risk management integration (§6.11) for safety assessment
  - Maintenance process integration (§6.10) for post-release problems
  - Software development planning (§6.2) for problem resolution process definition

## Assessment Methodology

For each requirement in Clause 9:

1. **Extract** the exact "shall" requirement from BSEN-62304.md
2. **Search** D0003329 §6.13 for corresponding coverage
3. **Evaluate** integration with:
   - §6.2 (Software Development Planning)
   - §6.10 (Software Maintenance)
   - D0003325 (Nonconformance Procedure)
4. **Classify** compliance status:
   - ✅ **COMPLIANT**: Fully addressed with adequate detail
   - ⚠️ **PARTIAL**: Mentioned but lacks specificity/clarity
   - ❌ **MISSING**: Not addressed or inadequate
5. **Document** findings with:
   - IEC 62304 section reference (§X.Y.Z)
   - D0003329 section reference or "Missing"
   - Gap description (specific, actionable)
   - Regulatory risk level (Critical/Significant/Minor)
   - Safety class impact (A, B, C, or All)

## Output Structure

Generate assessment file: `assessments/D0003329_REV_03_Final.Analysis.Clause9.md`

### File Content Template

```markdown
---
assessment_type: "IEC 62304 Clause 9 Compliance Assessment"
target_document: "D0003329_Rev_03_Final.md"
target_section: "§6.13 Software Problem Resolution Process"
reference_standard: "IEC 62304 (BS EN 62304:2006+A1:2015)"
assessment_date: "2025-12-16"
assessor: "Medical-Device-Design-Controls-Expert"
clause: "9"
---

# IEC 62304 Clause 9 (Problem Resolution) Compliance Assessment

## D0003329 Rev 03 - Software Problem Resolution Process

**Assessment Date**: December 16, 2025
**Assessor**: Systematic Compliance Analysis
**Standard**: BS EN 62304:2006+A1:2015 (IEC 62304)
**Scope**: Clause 9 - Software Problem Resolution Process

---

## Section 9.1: Prepare Problem Reports

**Compliant Elements** ✅
[List compliant items with D0003329 references]

**Partial Compliance** ⚠️
[List partial items with gap descriptions]

**Non-Compliant/Missing** ❌
[List missing items]

---

## Section 9.2: Investigate the Problem

**Compliant Elements** ✅
[Analysis - must include investigation and evaluation]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

## Section 9.3: Advise Relevant Parties

**Compliant Elements** ✅
[Analysis - internal and external notification]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

## Section 9.4: Use Change Control Process

**Compliant Elements** ✅
[Analysis - integration with Clause 8 change control]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

## Section 9.5: Maintain Records

**Compliant Elements** ✅
[Analysis - record retention requirements]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

## Section 9.6: Analyze Problems for Trends

**Compliant Elements** ✅
[Analysis - trend analysis procedures]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

## Section 9.7: Verify Problem Resolution

**Compliant Elements** ✅
[Analysis - must include regression testing requirements]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

## Section 9.8: Test Documentation Contents

**Compliant Elements** ✅
[Analysis - required content for problem resolution tests]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

## Cross-Reference Analysis

### Integration with Software Development Planning (§5.1.1.e)

[Assess how §6.13 implements problem resolution planning from §6.2]

### Integration with Maintenance Process (§6.1.d and §6.2.2)

[Assess how §6.13 supports maintenance problem resolution per §6.10]

### Integration with Nonconformance Procedure (D0003325)

[Assess integration with D0003325 for complaint management]

### Anomaly Tracking Throughout Lifecycle

[Assess requirements for anomaly tracking during development (§5.6.8, §5.7.2) and post-release]

---

## Clause 9 Compliance Summary

**Total Requirements Analyzed**: [X]
**Compliant**: [X] ([X]%)
**Partial Compliance**: [X] ([X]%)
**Non-Compliant/Missing**: [X] ([X]%)

### Key Findings

[Summarize major compliance themes, particularly problem investigation and resolution verification]

### Critical Gaps (Must Fix)

| #   | IEC § | Requirement | D0003329 § | Gap Description | Risk Level |
| --- | ----- | ----------- | ---------- | --------------- | ---------- |
| ... | ...   | ...         | ...        | ...             | ...        |

### Significant Gaps (Partial Compliance)

| #   | IEC § | Requirement | D0003329 § | Gap Description | Risk Level |
| --- | ----- | ----------- | ---------- | --------------- | ---------- |
| ... | ...   | ...         | ...        | ...             | ...        |

---

_End of Clause 9 Assessment_
```

## Quality Requirements

- [ ] All §9.1-9.8 requirements analyzed
- [ ] Every finding includes specific IEC citation
- [ ] D0003329 §6.13 coverage explicitly assessed
- [ ] Integration with development process verified (§5.6.8, §5.7.2)
- [ ] Integration with maintenance process verified (§6.2.2)
- [ ] D0003325 (Nonconformance) integration assessed
- [ ] Trend analysis requirements evaluated
- [ ] Verification and regression testing requirements assessed
- [ ] Gaps are specific and actionable
- [ ] Risk levels assigned to all gaps
- [ ] Output saved to `assessments/` folder
- [ ] Front matter metadata complete

## Success Criteria

Assessment complete when:

1. All problem resolution requirements (§9.1-9.8) analyzed
2. Integration with other processes verified
3. Complaint management linkage assessed
4. Compliance status clear for each requirement
5. Gaps prioritized by regulatory risk
6. Remediation guidance actionable
7. File saved with proper naming convention

---

**Analysis Mode**: Medical-Device-Design-Controls-Expert
**Required Model**: Claude Sonnet 4.5
**Estimated Duration**: 10-15 minutes
**Output File**: `assessments/D0003329_REV_03_Final.Analysis.Clause9.md`
