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

# Prompt: IEC 62304 Clause 6 (Software Maintenance) Compliance Assessment

## Core Task

Assess D0003329_Rev_03_Final.md for compliance with IEC 62304 Clause 6 (Software Maintenance Process) requirements.

## Required Input Files

**Load these files before analysis:**

1. **#file:D0003329_Rev_03_Final.md** - Work instruction §6.10 (Software Maintenance)
2. **#file:BSEN-62304.md** - IEC 62304 standard Clause 6 reference
3. **#file:D0003098_Rev_05_Final.md** - Related procedures (contextual)

## Analysis Scope

Assess IEC 62304 Clause 6 requirements:

- **§6.1**: Establish software maintenance plan

  - §6.1.a: Procedures for receiving/documenting/evaluating feedback
  - §6.1.b: Criteria for determining if feedback is a problem
  - §6.1.c: Use of software risk management process
  - §6.1.d: Use of software problem resolution process
  - §6.1.e: Use of software configuration management process
  - §6.1.f: Procedures for SOUP upgrades/obsolescence
  - §6.1.g: User/regulator notification procedures

- **§6.2**: Maintenance problem analysis
  - §6.2.1: Document and evaluate feedback
  - §6.2.2: Use software problem resolution process
  - §6.2.3: Analyze problems for trends

### Integration and Systems-Level Assessment

Additionally evaluate:

- **D0003098 Integration**:

  - Integration with D0003293 (Post-Market Surveillance)
  - Integration with D0003325 (Complaint Handling)
  - Integration with D0003336 (Design Changes)
  - Software maintenance activities within D0003098 lifecycle phases

- **FDA Design Control Expectations**:

  - 21 CFR 820.30(j) design change verification/validation
  - Post-market surveillance data integration (MDR, complaints)
  - Software update validation requirements
  - Version management for fielded software

- **Practical Implementation**:

  - Rollback procedures for failed updates
  - User notification processes
  - Update deployment validation
  - Fielded version tracking mechanisms

- **Cross-Document Consistency**:
  - Risk management process references (D0003329 §6.11)
  - Problem resolution integration (D0003329 §6.13)
  - Configuration management alignment (D0003329 §6.12)
  - §6.2.4: Verify implemented changes
  - §6.2.5: Test for unintended effects

## Assessment Methodology

For each requirement in Clause 6:

1. **Extract** the exact "shall" requirement from BSEN-62304.md
2. **Search** D0003329 §6.10 for corresponding coverage
3. **Classify** compliance status:
   - ✅ **COMPLIANT**: Fully addressed with adequate detail
   - ⚠️ **PARTIAL**: Mentioned but lacks specificity/clarity
   - ❌ **MISSING**: Not addressed or inadequate
4. **Document** findings with:
   - IEC 62304 section reference (§X.Y.Z)
   - D0003329 section reference or "Missing"
   - Gap description (specific, actionable)
   - Regulatory risk level (Critical/Significant/Minor)
   - Safety class impact (A, B, C, or All)

## Output Structure

Generate assessment file: `assessments/D0003329_REV_03_Final.Analysis.Clause6.md`

### File Content Template

```markdown
---
assessment_type: "IEC 62304 Clause 6 Compliance Assessment"
target_document: "D0003329_Rev_03_Final.md"
target_section: "§6.10 Software Maintenance"
reference_standard: "IEC 62304 (BS EN 62304:2006+A1:2015)"
assessment_date: "2025-12-16"
assessor: "Medical-Device-Design-Controls-Expert"
clause: "6"
---

# IEC 62304 Clause 6 (Software Maintenance) Compliance Assessment

## D0003329 Rev 03 - Software Maintenance Process

**Assessment Date**: December 16, 2025
**Assessor**: Systematic Compliance Analysis
**Standard**: BS EN 62304:2006+A1:2015 (IEC 62304)
**Scope**: Clause 6 - Software Maintenance Process

---

## Section 6.1: Establish Software Maintenance Plan

### 6.1: Software Maintenance Plan Requirements

**Compliant Elements** ✅
[List compliant items with D0003329 references]

**Partial Compliance** ⚠️
[List partial items with gap descriptions]

**Non-Compliant/Missing** ❌
[List missing items]

---

### 6.1.a: Procedures for Feedback Management

**Compliant Elements** ✅
[Analysis...]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

### 6.1.b: Problem Determination Criteria

[Continue for each sub-requirement...]

---

### 6.1.c: Risk Management Process Integration

[Analysis...]

---

### 6.1.d: Problem Resolution Process

[Analysis...]

---

### 6.1.e: Configuration Management Process

[Analysis...]

---

### 6.1.f: SOUP Upgrades and Obsolescence

[Analysis...]

---

### 6.1.g: User and Regulator Notification

[Analysis...]

---

## Section 6.2: Maintenance Problem Analysis

### 6.2.1: Document and Evaluate Feedback

[Analysis...]

---

### 6.2.2: Use Problem Resolution Process

[Analysis...]

---

### 6.2.3: Analyze for Trends

[Analysis...]

---

### 6.2.4: Verify Implemented Changes

[Analysis...]

---

### 6.2.5: Test for Unintended Effects

[Analysis...]

---

## Clause 6 Compliance Summary

**Total Requirements Analyzed**: [X]
**Compliant**: [X] ([X]%)
**Partial Compliance**: [X] ([X]%)
**Non-Compliant/Missing**: [X] ([X]%)

### Key Findings

[Summarize major compliance themes]

### Critical Gaps (Must Fix)

| #   | IEC § | Requirement | D0003329 § | Gap Description | Risk Level |
| --- | ----- | ----------- | ---------- | --------------- | ---------- |
| ... | ...   | ...         | ...        | ...             | ...        |

### Significant Gaps (Partial Compliance)

| #   | IEC § | Requirement | D0003329 § | Gap Description | Risk Level |
| --- | ----- | ----------- | ---------- | --------------- | ---------- |
| ... | ...   | ...         | ...        | ...             | ...        |

---

_End of Clause 6 Assessment_
```

## Quality Requirements

- [ ] All §6.1 and §6.2 sub-requirements analyzed
- [ ] Every finding includes specific IEC citation
- [ ] D0003329 §6.10 coverage explicitly assessed
- [ ] Integration with D0003325 (Nonconformance) evaluated
- [ ] Gaps are specific and actionable
- [ ] Risk levels assigned to all gaps
- [ ] Output saved to `assessments/` folder
- [ ] Front matter metadata complete

## Success Criteria

Assessment complete when:

1. All maintenance plan requirements (§6.1.a-g) analyzed
2. All maintenance problem analysis requirements (§6.2.1-5) analyzed
3. Compliance status clear for each requirement
4. Gaps prioritized by regulatory risk
5. Remediation guidance actionable
6. File saved with proper naming convention

---

**Analysis Mode**: Medical-Device-Design-Controls-Expert
**Required Model**: Claude Sonnet 4.5
**Estimated Duration**: 10-15 minutes
**Output File**: `assessments/D0003329_REV_03_Final.Analysis.Clause6.md`
