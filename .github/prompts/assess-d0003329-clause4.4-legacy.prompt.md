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

# Prompt: IEC 62304 Clause 4.4 (Legacy Software) Compliance Assessment

## Core Task

Assess D0003329_Rev_03_Final.md for compliance with IEC 62304 Clause 4.4 (Legacy Software) requirements.

## Required Input Files

**Load these files before analysis:**

1. **#file:D0003329_Rev_03_Final.md** - Work instruction §6.1 (Legacy Software)
2. **#file:BSEN-62304.md** - IEC 62304 standard §4.4 reference
3. **#file:D0003098_Rev_05_Final.md** - Related procedures (contextual)

## Analysis Scope

Assess IEC 62304 Section 4.4 requirements:

- **§4.4.1**: Determine software safety classification
- **§4.4.2**: Perform risk management activities for continued legacy software use
- **§4.4.3**: Gap analysis of available deliverables
- **§4.4.4**: Gap closure activities and plan execution
- **§4.4.5**: Document rationale for continued legacy software use

## Assessment Methodology

For each requirement in §4.4:

1. **Extract** the exact "shall" requirement from BSEN-62304.md
2. **Search** D0003329 §6.1 for corresponding coverage
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

### Integration and Systems-Level Assessment

In addition to IEC 62304 compliance, evaluate:

5. **D0003098 Integration**:

   - How §6.1 legacy software provisions integrate with D0003098 design control phases
   - Whether legacy software handling aligns with Phase transition requirements
   - DHF documentation requirements for legacy software
   - Cross-references between D0003329 and D0003098 for legacy software

6. **FDA Design Control Expectations**:

   - 21 CFR 820.30 applicability to legacy software
   - Design history file completeness for legacy components
   - Verification/validation requirements for continued use
   - Post-market surveillance integration for legacy software

7. **Practical Implementation Considerations**:

   - Guidance on executing gap analysis (tools, templates, checklists)
   - Criteria for determining when to use §4.4 vs. full §5-9 compliance
   - Resource requirements for gap closure activities
   - Timeline and prioritization guidance

8. **Cross-Document Consistency**:
   - Terminology consistency between D0003329 and D0003098
   - Risk management process alignment (D0003329 §6.11 vs. D0003098 risk references)
   - Problem resolution process integration (§6.13)
   - Configuration management alignment (§6.12)

## Output Structure

Generate assessment file: `assessments/D0003329_REV_03_Final.Analysis.Clause4.4.md`

### File Content Template

```markdown
---
assessment_type: "IEC 62304 Clause 4.4 Compliance Assessment"
target_document: "D0003329_Rev_03_Final.md"
target_section: "§6.1 Legacy Software"
reference_standard: "IEC 62304 (BS EN 62304:2006+A1:2015)"
assessment_date: "2025-12-16"
assessor: "Medical-Device-Design-Controls-Expert"
clause: "4.4"
---

# IEC 62304 Clause 4.4 (Legacy Software) Compliance Assessment

## D0003329 Rev 03 - Legacy Software Requirements

**Assessment Date**: December 16, 2025
**Assessor**: Systematic Compliance Analysis
**Standard**: BS EN 62304:2006+A1:2015 (IEC 62304)
**Scope**: Clause 4.4 - Legacy Software

---

## Section 4.4: Legacy Software

### 4.4.1: Determine Software Safety Classification

**Compliant Elements** ✅
[List compliant items with D0003329 references]

**Partial Compliance** ⚠️
[List partial items with gap descriptions]

**Non-Compliant/Missing** ❌
[List missing items]

---

### 4.4.2: Risk Management Activities for Continued Use

**Compliant Elements** ✅
[Analysis...]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

### 4.4.3: Gap Analysis

[Continue for each sub-requirement...]

---

### 4.4.4: Gap Closure Activities

[Analysis...]

---

### 4.4.5: Rationale for Use of Legacy Software

[Analysis...]

---

## Clause 4.4 Compliance Summary

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

_End of Clause 4.4 Assessment_
```

## Quality Requirements

- [ ] All §4.4 sub-requirements analyzed
- [ ] Every finding includes specific IEC citation
- [ ] D0003329 §6.1 coverage explicitly assessed
- [ ] Gaps are specific and actionable
- [ ] Risk levels assigned to all gaps
- [ ] Output saved to `assessments/` folder
- [ ] Front matter metadata complete

## Success Criteria

Assessment complete when:

1. All 5 sub-sections of §4.4 analyzed
2. Compliance status clear for each requirement
3. Gaps prioritized by regulatory risk
4. Remediation guidance actionable
5. File saved with proper naming convention

---

**Analysis Mode**: Medical-Device-Design-Controls-Expert
**Required Model**: Claude Sonnet 4.5
**Estimated Duration**: 10-15 minutes
**Output File**: `assessments/D0003329_REV_03_Final.Analysis.Clause4.4.md`
