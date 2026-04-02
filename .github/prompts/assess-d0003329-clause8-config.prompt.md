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

# Prompt: IEC 62304 Clause 8 (Configuration Management) Compliance Assessment

## Core Task

Assess D0003329_Rev_03_Final.md for compliance with IEC 62304 Clause 8 (Software Configuration Management Process) requirements.

## Required Input Files

**Load these files before analysis:**

1. **#file:D0003329_Rev_03_Final.md** - Work instruction §6.12 (Configuration Management)
2. **#file:BSEN-62304.md** - IEC 62304 standard Clause 8 reference
3. **#file:D0003098_Rev_05_Final.md** - Related procedures (contextual)

## Analysis Scope

Assess IEC 62304 Clause 8 requirements:

### Section 8.1: Configuration Identification

- **§8.1.1**: Establish means to identify configuration items
- **§8.1.2**: Identify SOUP (including version, manufacturer)
- **§8.1.3**: Identify system configuration documentation

### Section 8.2: Change Control

- **§8.2.1**: Approve change requests prior to implementation
- **§8.2.2**: Implement changes per software development plan/maintenance plan
- **§8.2.3**: Verify changes (including re-verification and regression per §5.7.3 and §9.7)
- **§8.2.4**: Provide means for traceability of change

### Section 8.3: Configuration Status Accounting

### Integration and Systems-Level Assessment

Additionally evaluate:

- **D0003098 Integration**:

  - Configuration management within D0003098 design control framework
  - Integration with D0003336 (Design Changes) for change control
  - DHF documentation and configuration item archival
  - Configuration management during Phase transitions

- **FDA Design Control Expectations**:

  - Design history file configuration item retention
  - Change control approval workflows (design changes)
  - Traceability of configuration items through lifecycle
  - Configuration baseline establishment at Phase gates

- **Practical Implementation**:

  - Repository requirements and tool validation (D0003078 reference)
  - Version control system requirements
  - Configuration item naming/numbering conventions
  - Configuration status accounting mechanisms
  - SOUP Bill of Materials maintenance

- **Cross-Document Consistency**:

  - Problem resolution process integration (§6.13)
  - Maintenance process integration (§6.10)
  - Software development planning integration (§6.2)
  - Version Description Document requirements (D0004199)

- **§8.3**: Record and report configuration items, status, change requests, implementation status

## Assessment Methodology

For each requirement in Clause 8:

1. **Extract** the exact "shall" requirement from BSEN-62304.md
2. **Search** D0003329 §6.12 for corresponding coverage
3. **Evaluate** integration with §6.2 (Software Development Planning)
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

Generate assessment file: `assessments/D0003329_REV_03_Final.Analysis.Clause8.md`

### File Content Template

```markdown
---
assessment_type: "IEC 62304 Clause 8 Compliance Assessment"
target_document: "D0003329_Rev_03_Final.md"
target_section: "§6.12 Software Configuration Management"
reference_standard: "IEC 62304 (BS EN 62304:2006+A1:2015)"
assessment_date: "2025-12-16"
assessor: "Medical-Device-Design-Controls-Expert"
clause: "8"
---

# IEC 62304 Clause 8 (Configuration Management) Compliance Assessment

## D0003329 Rev 03 - Software Configuration Management Process

**Assessment Date**: December 16, 2025
**Assessor**: Systematic Compliance Analysis
**Standard**: BS EN 62304:2006+A1:2015 (IEC 62304)
**Scope**: Clause 8 - Software Configuration Management Process

---

## Section 8.1: Configuration Identification

### 8.1.1: Establish Means to Identify Configuration Items

**Compliant Elements** ✅
[List compliant items with D0003329 references]

**Partial Compliance** ⚠️
[List partial items with gap descriptions]

**Non-Compliant/Missing** ❌
[List missing items]

---

### 8.1.2: Identify SOUP

**Compliant Elements** ✅
[Analysis - must include version identification and manufacturer]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

### 8.1.3: Identify System Configuration Documentation

[Continue for each sub-requirement...]

---

## Section 8.2: Change Control

### 8.2.1: Approve Change Requests

**Compliant Elements** ✅
[Analysis...]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

### 8.2.2: Implement Changes per Plan

[Analysis...]

---

### 8.2.3: Verify Changes

[Analysis - include assessment of re-verification, regression testing requirements]

---

### 8.2.4: Provide Traceability of Change

[Analysis...]

---

## Section 8.3: Configuration Status Accounting

### 8.3: Record and Report Status

**Compliant Elements** ✅
[Analysis - must cover configuration items, status, change requests, implementation status]

**Partial Compliance** ⚠️
[Analysis...]

**Non-Compliant/Missing** ❌
[Analysis...]

---

## Cross-Reference Analysis

### Integration with Software Development Planning (§5.1.9)

[Assess how §6.12 implements planning requirements from §6.2]

### Tool Validation Requirements

[Assess D0003078 (Non-Device Software Validation) integration for Class B/C]

### Repository and Archive Requirements

[Assess controlled repository requirements and archival per §5.8.7]

---

## Clause 8 Compliance Summary

**Total Requirements Analyzed**: [X]
**Compliant**: [X] ([X]%)
**Partial Compliance**: [X] ([X]%)
**Non-Compliant/Missing**: [X] ([X]%)

### Key Findings

[Summarize major compliance themes, particularly configuration item control and change management]

### Critical Gaps (Must Fix)

| #   | IEC § | Requirement | D0003329 § | Gap Description | Risk Level |
| --- | ----- | ----------- | ---------- | --------------- | ---------- |
| ... | ...   | ...         | ...        | ...             | ...        |

### Significant Gaps (Partial Compliance)

| #   | IEC § | Requirement | D0003329 § | Gap Description | Risk Level |
| --- | ----- | ----------- | ---------- | --------------- | ---------- |
| ... | ...   | ...         | ...        | ...             | ...        |

---

_End of Clause 8 Assessment_
```

## Quality Requirements

- [ ] All §8.1-8.3 sub-requirements analyzed
- [ ] Every finding includes specific IEC citation
- [ ] D0003329 §6.12 coverage explicitly assessed
- [ ] SOUP identification requirements verified
- [ ] Change control workflow assessed
- [ ] Configuration status accounting evaluated
- [ ] Tool validation requirements (D0003078) assessed
- [ ] Gaps are specific and actionable
- [ ] Risk levels assigned to all gaps
- [ ] Output saved to `assessments/` folder
- [ ] Front matter metadata complete

## Success Criteria

Assessment complete when:

1. All configuration identification requirements (§8.1) analyzed
2. All change control requirements (§8.2) analyzed
3. Configuration status accounting (§8.3) analyzed
4. Integration with planning requirements assessed
5. Repository and archival adequacy verified
6. Compliance status clear for each requirement
7. Gaps prioritized by regulatory risk
8. Remediation guidance actionable
9. File saved with proper naming convention

---

**Analysis Mode**: Medical-Device-Design-Controls-Expert
**Required Model**: Claude Sonnet 4.5
**Estimated Duration**: 10-15 minutes
**Output File**: `assessments/D0003329_REV_03_Final.Analysis.Clause8.md`
