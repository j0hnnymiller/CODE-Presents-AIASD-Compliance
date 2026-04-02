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

# Prompt: IEC 62304 Clause 5 (Software Development Process) Compliance Assessment

## Core Task

Assess D0003329_Rev_03_Final.md for compliance with IEC 62304 Clause 5 (Software Development Process) requirements.

## Required Input Files

**Load these files before analysis:**

1. **#file:D0003329_Rev_03_Final.md** - Work instruction sections covering software development
2. **#file:standards/BSEN-62304.md** - IEC 62304 standard §5 reference
3. **#file:D0003098_Rev_05_Final.md** - Related procedures (contextual)

## Analysis Scope

Assess IEC 62304 Section 5 requirements across all subsections:

### §5.1: Software Development Planning (9 requirements)

- Development plan preparation
- Software development plan update and review
- Risk management plan integration
- Configuration management integration
- Problem resolution plan integration
- Verification planning
- Integration and integration testing planning
- Safety classification documentation
- Software development standards and methods

### §5.2: Software Requirements Analysis (11 requirements)

- Requirements definition
- Requirements content (functional, performance, interfaces, data definition, safety)
- Evaluation criteria for functional requirements
- Requirements verification
- Risk control measures implementation in requirements
- Requirements communication
- User documentation content
- Requirements updates
- Hazardous situation verification
- Requirements traceability
- Re-evaluation of medical device risk analysis

### §5.3: Software Architectural Design (6 requirements)

- Architecture design documentation
- Software item segregation
- Interface specification (internal and external)
- Functional and performance requirements specification
- Verification of software architecture
- Architecture risk control measures implementation

### §5.4: Software Detailed Design (3 requirements)

- Detailed design for each software unit
- Detailed design interfaces
- Verification of detailed design

### §5.5: Software Unit Implementation and Verification (6 requirements)

- Software unit implementation
- Unit acceptance criteria
- Additional software unit acceptance criteria (Class C)
- Unit verification procedures
- Unit verification record
- Unit verification strategy evaluation

### §5.6: Software Integration and Integration Testing (6 requirements)

- Integration plan
- Verification of software integration
- Integration testing based on integration plan
- Anomaly recording
- Integration testing record
- Integration test strategy evaluation

### §5.7: Software System Testing (5 requirements)

- System test plan
- System test case documentation
- System test execution
- System test record
- Re-test requirements
- System test strategy evaluation

### §5.8: Software Release (3 requirements)

- Known residual anomalies evaluation
- Released versions documentation
- Release documentation archiving

## Assessment Methodology

For each requirement in §5:

1. **Extract** the exact "shall" requirement from BSEN-62304.md
2. **Search** D0003329 for corresponding coverage across relevant sections:
   - §6.2: Software Development Plan
   - §6.3: Software Requirements Analysis
   - §6.4: Software Architecture Design
   - §6.5: Software Detailed Design
   - §6.6: Software Unit Implementation and Verification
   - §6.7: Software Integration and Integration Testing
   - §6.8: Software System Testing
   - §6.9: Software Release
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

   - How development process provisions integrate with D0003098 design control phases
   - Whether development activities align with Phase 0-4 transition requirements
   - DHF documentation requirements for development lifecycle
   - Cross-references between D0003329 and D0003098 for development activities

6. **FDA Design Control Expectations**:

   - 21 CFR 820.30 design controls alignment
   - Design input/output requirements
   - Design verification/validation integration
   - Design transfer considerations
   - Design history file completeness

7. **Template References and Adequacy**:

   - D0004168: Software Development Plan template
   - D0004169: Software Requirements Specification template
   - D0004197: Software Architecture Design template
   - D0017986: Software Detailed Design template
   - Test documentation templates
   - Verification that templates support IEC 62304 requirements

8. **Practical Implementation Considerations**:

   - Guidance on executing development activities
   - Criteria for determining adequate depth/detail by safety class
   - Resource requirements and timeline guidance
   - Tools and automation recommendations

9. **Cross-Document Consistency**:
   - Terminology consistency between D0003329 and D0003098
   - Risk management process alignment throughout development
   - Configuration management integration
   - Problem resolution process integration
   - Traceability framework adequacy

## Output Structure

Generate assessment file: `assessments/assessment.2/D0003329_REV_03_Final.Analysis.Clause5.md`

### File Content Template

```markdown
---
assessment_type: "IEC 62304 Clause 5 Compliance Assessment"
target_document: "D0003329_Rev_03_Final.md"
target_sections: "§6.2-6.9 (Software Development Process)"
reference_standard: "IEC 62304 (BS EN 62304:2006+A1:2015)"
assessment_date: "2025-12-16"
assessor: "Medical-Device-Design-Controls-Expert"
clause: "5"
total_requirements: 49
---

# IEC 62304 Clause 5 (Software Development Process) Compliance Assessment

## D0003329 Rev 03 - Software Development Process Requirements

**Assessment Date**: December 16, 2025
**Assessor**: Medical-Device-Design-Controls-Expert
**Standard**: BS EN 62304:2006+A1:2015 (IEC 62304)
**Scope**: Clause 5 - Software Development Process (49 requirements)

---

## 📋 Executive Summary

### Compliance Overview

| Status                     | Count  | Percentage |
| -------------------------- | ------ | ---------- |
| ✅ Compliant               | X      | X%         |
| ⚠️ Partial Compliance      | X      | X%         |
| ❌ Non-Compliant / Missing | X      | X%         |
| **Total Requirements**     | **49** | **100%**   |

### Critical Findings

[Brief summary of most critical gaps]

### Overall Assessment

[2-3 paragraph assessment of D0003329's coverage of Clause 5 development requirements]

---

## Section 5.1: Software Development Planning

**IEC 62304 Requirements**: 9 requirements
**D0003329 Coverage**: §6.2 Software Development Plan

### 5.1.1: Develop Software Development Plan

**IEC 62304 Requirement**:

> The MANUFACTURER shall develop a software development plan for conducting the activities of the software development process...

**D0003329 Coverage**: [Reference specific section(s)]

**Status**: ✅ COMPLIANT / ⚠️ PARTIAL / ❌ MISSING

**Analysis**:
[Detailed analysis of how D0003329 addresses this requirement]

**Gaps** (if applicable):

- [Specific gap 1]
- [Specific gap 2]

**Recommendations**:

- [Specific recommendation 1]
- [Specific recommendation 2]

**Safety Class Impact**: All / A / B / C
**Regulatory Risk**: Critical / Significant / Minor

---

### 5.1.2: Keep Software Development Plan Updated

[Continue same format for each requirement...]

---

## Section 5.2: Software Requirements Analysis

**IEC 62304 Requirements**: 11 requirements
**D0003329 Coverage**: §6.3 Software Requirements Analysis

### 5.2.1: Define and Document Software Requirements

[Analysis...]

### 5.2.2: Software Requirements Content

[Analysis...]

### 5.2.3: Include Risk Control Measures in Requirements

[Analysis...]

[Continue for all §5.2 requirements...]

---

## Section 5.3: Software Architectural Design

**IEC 62304 Requirements**: 6 requirements
**D0003329 Coverage**: §6.4 Software Architecture Design

[Continue similar format...]

---

## Section 5.4: Software Detailed Design

**IEC 62304 Requirements**: 3 requirements
**D0003329 Coverage**: §6.5 Software Detailed Design

[Continue similar format...]

---

## Section 5.5: Software Unit Implementation and Verification

**IEC 62304 Requirements**: 6 requirements
**D0003329 Coverage**: §6.6 Software Unit Implementation and Verification

[Continue similar format...]

---

## Section 5.6: Software Integration and Integration Testing

**IEC 62304 Requirements**: 6 requirements
**D0003329 Coverage**: §6.7 Software Integration and Integration Testing

[Continue similar format...]

---

## Section 5.7: Software System Testing

**IEC 62304 Requirements**: 5 requirements
**D0003329 Coverage**: §6.8 Software System Testing

[Continue similar format...]

---

## Section 5.8: Software Release

**IEC 62304 Requirements**: 3 requirements
**D0003329 Coverage**: §6.9 Software Release

[Continue similar format...]

---

## 🔍 Detailed Gap Analysis

### CRITICAL GAPS (Regulatory Blockers)

| #   | IEC §  | Requirement Summary      | D0003329 § | Gap Description     | Classes | Priority  |
| --- | ------ | ------------------------ | ---------- | ------------------- | ------- | --------- |
| 1   | §5.X.Y | [Brief requirement text] | Missing    | [What's absent]     | All     | Immediate |
| 2   | §5.X.Y | [Brief requirement text] | §6.X       | [What's inadequate] | B,C     | Immediate |
| ... | ...    | ...                      | ...        | ...                 | ...     | ...       |

**Total Critical Gaps**: X

---

### SIGNIFICANT GAPS (Partial Compliance)

| #   | IEC §  | Requirement Summary      | D0003329 § | Gap Description            | Classes | Priority |
| --- | ------ | ------------------------ | ---------- | -------------------------- | ------- | -------- |
| 1   | §5.X.Y | [Brief requirement text] | §6.X       | [What needs clarification] | All     | High     |
| ... | ...    | ...                      | ...        | ...                        | ...     | ...      |

**Total Significant Gaps**: X

---

### MINOR GAPS (Best Practice Improvements)

| #   | IEC §  | Area    | Improvement Opportunity   | Current State | Suggested Enhancement | Priority |
| --- | ------ | ------- | ------------------------- | ------------- | --------------------- | -------- |
| 1   | §5.X.Y | [Topic] | [Opportunity description] | [Current]     | [Recommendation]      | Low      |
| ... | ...    | ...     | ...                       | ...           | ...                   | ...      |

**Total Minor Gaps**: X

---

## 🎯 Cross-Cutting Themes

### Theme 1: Traceability Framework

**Affected Requirements**: [List IEC sections]

**Current State**: [What D0003329 provides]

**Gap**: [What's missing or unclear]

**Impact**: [How this affects compliance]

**Recommendation**: [Specific guidance]

---

### Theme 2: Safety Class Differentiation

[Continue for each cross-cutting theme...]

---

## 📊 Compliance by Safety Class

### Class A Requirements

| Subsection | Total | Compliant | Partial | Missing | Status     |
| ---------- | ----- | --------- | ------- | ------- | ---------- |
| §5.1       | X     | X         | X       | X       | [✅/⚠️/❌] |
| §5.2       | X     | X         | X       | X       | [✅/⚠️/❌] |
| §5.3       | X     | X         | X       | X       | [✅/⚠️/❌] |
| §5.4       | X     | X         | X       | X       | [✅/⚠️/❌] |
| §5.5       | X     | X         | X       | X       | [✅/⚠️/❌] |
| §5.6       | X     | X         | X       | X       | [✅/⚠️/❌] |
| §5.7       | X     | X         | X       | X       | [✅/⚠️/❌] |
| §5.8       | X     | X         | X       | X       | [✅/⚠️/❌] |
| **Total**  | **X** | **X**     | **X**   | **X**   | [✅/⚠️/❌] |

### Class B Requirements

[Similar table...]

### Class C Requirements

[Similar table...]

---

## 📚 Template and Tool Assessment

### Referenced Templates

| Template | Document | Purpose          | IEC Requirements Covered | Adequacy   | Gaps          |
| -------- | -------- | ---------------- | ------------------------ | ---------- | ------------- |
| D0004168 | SDP      | Development Plan | §5.1                     | [✅/⚠️/❌] | [List if any] |
| D0004169 | SRS      | Requirements     | §5.2                     | [✅/⚠️/❌] | [List if any] |
| D0004197 | SAD      | Architecture     | §5.3                     | [✅/⚠️/❌] | [List if any] |
| D0017986 | SDD      | Detailed Design  | §5.4                     | [✅/⚠️/❌] | [List if any] |
| ...      | ...      | ...              | ...                      | ...        | ...           |

**Note**: Template assessment based on work instruction references. Actual template content should be reviewed separately for complete validation.

---

## 🔗 Integration with Other Standards/Processes

### D0003098 Rev 05 Integration

**Design Control Phase Alignment**:

- Phase 0-1: [How §5.1-5.2 integrate]
- Phase 2: [How §5.3-5.4 integrate]
- Phase 3: [How §5.5-5.7 integrate]
- Phase 4: [How §5.8 integrates]

**Cross-Reference Assessment**: [✅/⚠️/❌]

**Gaps**:

- [List integration gaps]

---

### Risk Management (ISO 14971) Integration

**Requirements with Risk Management Integration**:

- §5.1.1: Risk management plan
- §5.2.3: Risk control measures in requirements
- §5.3.5: Risk control measures in architecture
- §5.8.1: Evaluation of known residual anomalies

**Integration Assessment**: [Analysis of how well integrated]

**Gaps**:

- [List gaps in risk management integration]

---

### Configuration Management Integration

**Requirements with CM Integration**:

- §5.1.1: Configuration management plan reference
- Throughout development: Version control expectations

**Integration Assessment**: [Analysis]

**Gaps**:

- [List gaps]

---

### Problem Resolution Integration

**Requirements with PR Integration**:

- §5.6.4: Anomaly recording during integration testing
- §5.7.4: Test result recording

**Integration Assessment**: [Analysis]

**Gaps**:

- [List gaps]

---

## 💡 Recommendations

### Immediate Actions (Critical - 0-30 Days)

1. **[Gap Topic]** (IEC §X.Y.Z)

   - **Action**: [Specific action to take]
   - **Rationale**: [Why this is critical]
   - **Success Criteria**: [How to verify completion]
   - **Effort**: [Estimated hours/days]

2. [Continue for each critical gap...]

---

### Short-Term Actions (High Priority - 30-90 Days)

1. **[Gap Topic]** (IEC §X.Y.Z)
   - **Action**: [Specific action]
   - **Rationale**: [Why needed]
   - **Success Criteria**: [How to verify]
   - **Effort**: [Estimate]

[Continue...]

---

### Long-Term Actions (Continuous Improvement - 90+ Days)

1. **[Enhancement Topic]**
   - **Action**: [Specific action]
   - **Benefit**: [Why worthwhile]
   - **Success Criteria**: [How to verify]
   - **Effort**: [Estimate]

[Continue...]

---

## ✅ Verification Checklist

Use this checklist to verify remediation:

- [ ] All critical gaps addressed with documented evidence
- [ ] All significant gaps resolved or have justified exceptions
- [ ] Templates updated to support IEC 62304 requirements
- [ ] Cross-references between D0003329 and templates verified
- [ ] Integration with D0003098, §7 (risk), §8 (CM), §9 (PR) validated
- [ ] Safety class-specific guidance clarified
- [ ] Traceability framework documented and implemented
- [ ] Training materials updated to reflect changes
- [ ] Quality management system documentation updated

---

_End of Clause 5 Assessment_

---

## Appendix A: Detailed Requirement Mapping

### Complete Traceability Matrix

| IEC § | IEC Requirement (Brief)         | D0003329 § | Coverage | Status | Class | Notes |
| ----- | ------------------------------- | ---------- | -------- | ------ | ----- | ----- |
| 5.1.1 | Develop SDP                     | §6.2.1     | Full     | ✅     | All   | ...   |
| 5.1.2 | Keep SDP updated                | §6.2.2     | Partial  | ⚠️     | All   | ...   |
| 5.1.3 | Document software dev standards | Missing    | None     | ❌     | All   | ...   |
| ...   | ...                             | ...        | ...      | ...    | ...   | ...   |

[Continue for all 49 requirements...]

---

## Appendix B: Reference Standards and Documents

### IEC 62304 Section 5 Requirements

**Source**: BS EN 62304:2006+A1:2015 Clause 5

[Optional: Include full text of relevant requirements if helpful]

### Related D0003329 Sections

- §6.2: Software Development Plan (pages X-Y)
- §6.3: Software Requirements Analysis (pages X-Y)
- §6.4: Software Architecture Design (pages X-Y)
- §6.5: Software Detailed Design (pages X-Y)
- §6.6: Software Unit Implementation and Verification (pages X-Y)
- §6.7: Software Integration and Integration Testing (pages X-Y)
- §6.8: Software System Testing (pages X-Y)
- §6.9: Software Release (pages X-Y)

### Related D0003098 Sections

[List relevant sections from D0003098 Rev 05]
```

---

## Quality Requirements

- [ ] All 49 Clause 5 requirements assessed individually
- [ ] Each requirement has clear compliance status (✅/⚠️/❌)
- [ ] Gaps are specific, actionable, and prioritized
- [ ] Safety class implications documented for each requirement
- [ ] Cross-references to D0003329 sections verified
- [ ] Integration with D0003098, risk management, CM, and PR evaluated
- [ ] Template adequacy assessed
- [ ] Recommendations are prioritized by criticality
- [ ] Output saved to `assessments/assessment.2/` folder
- [ ] Front matter metadata complete

## Success Criteria

Assessment complete when:

1. All 49 requirements in Clause 5 individually assessed
2. Compliance percentages calculated accurately
3. Critical gaps clearly identified with specific remediation guidance
4. Cross-cutting themes documented
5. Safety class-specific analysis provided
6. Template and tool assessment completed
7. Integration with other processes/standards evaluated
8. File saved with proper naming convention
9. Ready for integration into executive summary

---

**Analysis Mode**: Medical-Device-Design-Controls-Expert
**Required Model**: Claude Sonnet 4.5
**Estimated Duration**: 45-60 minutes (due to 49 requirements)
**Output File**: `assessments/assessment.2/D0003329_REV_03_Final.Analysis.Clause5.md`
**Dependencies**: D0003329_Rev_03_Final.md, BSEN-62304.md, D0003098_Rev_05_Final.md
