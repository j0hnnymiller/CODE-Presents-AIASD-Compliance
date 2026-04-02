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

# Prompt: IEC 62304 Clause 7 (Software Risk Management) Compliance Assessment

## Core Task

Assess D0003329_Rev_03_Final.md for compliance with IEC 62304 Clause 7 (Software Risk Management Process) requirements.

## Required Input Files

**Load these files before analysis:**

1. **#file:D0003329_Rev_03_Final.md** - Work instruction §6.11 (Risk Management)
2. **#file:BSEN-62304.md** - IEC 62304 standard Clause 7 reference
3. **#file:D0003098_Rev_05_Final.md** - Related procedures (contextual)

## Analysis Scope

Assess IEC 62304 Clause 7 requirements:

### Section 7.1: Analysis of Software Contributing to Hazardous Situations

- **§7.1.1**: Identify software items that could contribute to hazardous situations
- **§7.1.2**: Identify potential causes of contribution to hazardous situations
- **§7.1.3**: Evaluate published SOUP anomaly lists
- **§7.1.4**: Document potential causes
- **§7.1.5**: (Reserved - not used in standard)

### Section 7.2: Risk Control Measures

- **§7.2.1**: Define risk control measures
- **§7.2.2**: Risk control measures implemented in software

### Section 7.3: Verification of Risk Control Measures

### Integration and Systems-Level Assessment

Additionally evaluate:

- **D0003098 Integration**:

  - Alignment with D0003103 (Global Procedure, Risk Management)
  - Integration with overall device risk management per ISO 14971
  - Software risk management within D0003098 Phase activities
  - Traceability between system-level and software-level risk controls

- **FDA Design Control Expectations**:

  - ISO 14971 risk management integration
  - Risk management file documentation requirements
  - Traceability of risk controls through design, verification, and validation
  - Post-market risk management (complaint/MDR integration)

- **Practical Implementation**:

  - Cybersecurity risk management integration (D0029257 reference)
  - SOUP anomaly evaluation methodology
  - Risk control verification procedures
  - Software safety classification determination process

- **Cross-Document Consistency**:

  - D0003103 risk management process alignment
  - Software requirements integration (§6.3) for risk controls
  - Verification protocol integration (§6.8) for risk control verification
  - Risk control traceability matrix maintenance

- **§7.3.1**: Verify risk control measures
- **§7.3.2**: (Not used in standard)
- **§7.3.3**: Document traceability (Class B, C)

### Section 7.4: Risk Management of Software Changes

- **§7.4.1**: Analyze changes to medical device software with respect to safety
- **§7.4.2**: Analyze impact of software changes on existing risk control measures
- **§7.4.3**: Perform risk management activities based on analyses

## Assessment Methodology

For each requirement in Clause 7:

1. **Extract** the exact "shall" requirement from BSEN-62304.md
2. **Search** D0003329 §6.11 for corresponding coverage
3. **Evaluate** integration with D0003103 (Risk Management Procedure)
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

Generate assessment file: `assessments/D0003329_REV_03_Final.Analysis.Clause7.md`

### File Content Template

```markdown
---
assessment_type: "IEC 62304 Clause 7 Compliance Assessment"
target_document: "D0003329_Rev_03_Final.md"
target_section: "§6.11 Software Risk Management"
reference_standard: "IEC 62304 (BS EN 62304:2006+A1:2015)"
assessment_date: "2025-12-16"
assessor: "Medical-Device-Design-Controls-Expert"
clause: "7"
---

# IEC 62304 Clause 7 (Software Risk Management) Compliance Assessment

## D0003329 Rev 03 - Software Risk Management Process

**Assessment Date**: December 16, 2025
**Assessor**: Systematic Compliance Analysis
**Standard**: BS EN 62304:2006+A1:2015 (IEC 62304)
**Scope**: Clause 7 - Software Risk Management Process

---

## Section 7.1: Analysis of Software Contributing to Hazardous Situations

### 7.1.1: Identify Software Items Contributing to Hazards

**Compliant Elements** ✅
[List compliant items with D0003329 references]

**Partial Compliance** ⚠️
[List partial items with gap descriptions]

**Non-Compliant/Missing** ❌
[List missing items]

---

### 7.1.2: Identify Potential Causes

**Compliant Elements** ✅
[Analysis...]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

### 7.1.3: Evaluate Published SOUP Anomaly Lists

[Continue for each sub-requirement...]

---

### 7.1.4: Document Potential Causes

[Analysis...]

---

## Section 7.2: Risk Control Measures

### 7.2.1: Define Risk Control Measures

[Analysis...]

---

### 7.2.2: Risk Control Measures Implemented in Software

[Analysis...]

---

## Section 7.3: Verification of Risk Control Measures

### 7.3.1: Verify Risk Control Measures

[Analysis...]

---

### 7.3.3: Document Traceability (Class B, C)

[Analysis...]

---

## Section 7.4: Risk Management of Software Changes

### 7.4.1: Analyze Changes with Respect to Safety

[Analysis...]

---

### 7.4.2: Analyze Impact on Existing Risk Control Measures

[Analysis...]

---

### 7.4.3: Perform Risk Management Activities

[Analysis...]

---

## Cross-Reference Analysis

### Integration with ISO 14971

[Assess how D0003329 §6.11 integrates IEC 62304 Clause 7 with ISO 14971 risk management]

### Cybersecurity Integration

[Assess integration with D0029257 Cybersecurity Work Instruction]

### Traceability Framework

[Assess traceability from hazards → software items → causes → risk controls → verification]

---

## Clause 7 Compliance Summary

**Total Requirements Analyzed**: [X]
**Compliant**: [X] ([X]%)
**Partial Compliance**: [X] ([X]%)
**Non-Compliant/Missing**: [X] ([X]%)

### Key Findings

[Summarize major compliance themes, particularly integration with overall risk management]

### Critical Gaps (Must Fix)

| #   | IEC § | Requirement | D0003329 § | Gap Description | Risk Level |
| --- | ----- | ----------- | ---------- | --------------- | ---------- |
| ... | ...   | ...         | ...        | ...             | ...        |

### Significant Gaps (Partial Compliance)

| #   | IEC § | Requirement | D0003329 § | Gap Description | Risk Level |
| --- | ----- | ----------- | ---------- | --------------- | ---------- |
| ... | ...   | ...         | ...        | ...             | ...        |

---

_End of Clause 7 Assessment_
```

## Quality Requirements

- [ ] All §7.1-7.4 sub-requirements analyzed
- [ ] Every finding includes specific IEC citation
- [ ] D0003329 §6.11 coverage explicitly assessed
- [ ] ISO 14971 integration evaluated
- [ ] Cybersecurity integration assessed (D0029257)
- [ ] Traceability requirements verified
- [ ] Gaps are specific and actionable
- [ ] Risk levels assigned to all gaps
- [ ] Output saved to `assessments/` folder
- [ ] Front matter metadata complete

## Success Criteria

Assessment complete when:

1. All hazard analysis requirements (§7.1) analyzed
2. All risk control requirements (§7.2) analyzed
3. All verification requirements (§7.3) analyzed
4. All change management requirements (§7.4) analyzed
5. Integration with ISO 14971 assessed
6. Compliance status clear for each requirement
7. Gaps prioritized by regulatory risk
8. Remediation guidance actionable
9. File saved with proper naming convention

---

**Analysis Mode**: Medical-Device-Design-Controls-Expert
**Required Model**: Claude Sonnet 4.5
**Estimated Duration**: 15-20 minutes
**Output File**: `assessments/D0003329_REV_03_Final.Analysis.Clause7.md`
