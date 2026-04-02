# Execute Assessment 3 - D0003329 IEC 62304 Compliance Analysis

## Overview

Execute all assessment prompt files for D0003329 Rev 03 work instruction and generate comprehensive IEC 62304 compliance analysis outputs in `assessments/assessment.3/`.

## Assessment Prompts to Execute (In Order)

Execute the following 8 prompts sequentially from `.github/prompts/`:

1. **assess-d0003329-iec62304-compliance.prompt.md**

   - Output: `assessments/assessment.3/D0003329_Rev_03_IEC62304_Compliance_Assessment_2025-12-17.md`
   - Comprehensive compliance overview across all IEC 62304 sections

2. **assess-d0003329-clause4.4-legacy.prompt.md**

   - Output: `assessments/assessment.3/D0003329_REV_03_Final.Analysis.Clause4.4.md`
   - Quality system requirements and legacy software analysis

3. **assess-d0003329-clause5-development.prompt.md**

   - Output: `assessments/assessment.3/D0003329_REV_03_Final.Analysis.Clause5.md`
   - Software development process compliance (5.1-5.8)

4. **assess-d0003329-clause6-maintenance.prompt.md**

   - Output: `assessments/assessment.3/D0003329_REV_03_Final.Analysis.Clause6.md`
   - Software maintenance process requirements

5. **assess-d0003329-clause7-risk.prompt.md**

   - Output: `assessments/assessment.3/D0003329_REV_03_Final.Analysis.Clause7.md`
   - Risk management integration analysis

6. **assess-d0003329-clause8-config.prompt.md**

   - Output: `assessments/assessment.3/D0003329_REV_03_Final.Analysis.Clause8.md`
   - Configuration management requirements

7. **assess-d0003329-clause9-problems.prompt.md**

   - Output: `assessments/assessment.3/D0003329_REV_03_Final.Analysis.Clause9.md`
   - Problem resolution process compliance

8. **assess-d0003329-executive-summary.prompt.md**
   - Output: `assessments/assessment.3/D0003329_REV_03_Final.IEC62304_Executive_Summary.md`
   - High-level summary and key findings synthesis

## Required Input Files

Each prompt should load these files using `#file:` references:

- **D0003329_Rev_03_Final.md** - Primary work instruction being assessed
- **standards/BSEN-62304.md** - IEC 62304 standard reference
- **D0003098_Rev_05_Final.md** - Related procedures (contextual)

## Output Requirements

### File Naming Convention

Follow the pattern: `D0003329_REV_03_Final.Analysis.<Topic>.md`

Example outputs:

- `D0003329_REV_03_Final.Analysis.Clause4.4.md`
- `D0003329_REV_03_Final.Analysis.Clause5.md`
- `D0003329_REV_03_Final.IEC62304_Executive_Summary.md`

### AI Provenance Metadata

Each generated file must include front matter per `.github/instructions/ai-assisted-output.instructions.md`:

```yaml
---
ai_generated: true
model: "<provider>/<model>@<version>"
operator: "github-copilot-coding-agent"
chat_id: "<github-issue-number>-assessment-3-execution"
prompt: |
  <reference to source prompt file>
started: "<ISO8601-timestamp>"
ended: "<ISO8601-timestamp>"
task_durations:
  - task: "assessment execution"
    duration: "<hh:mm:ss>"
total_duration: "<hh:mm:ss>"
ai_log: "ai-logs/<yyyy>/<mm>/<dd>/<chat-id>/conversation.md"
source: ".github/prompts/<prompt-filename>.prompt.md"
---
```

### Analysis Quality Standards

Each assessment must include:

1. **📋 Executive Summary** - Brief compliance status overview
2. **✅ Compliance Findings** - Organized by IEC 62304 section
   - ✅ Fully compliant elements
   - ⚠️ Partial compliance / needs clarification
   - ❌ Non-compliant or missing elements
3. **🔍 Gap Analysis** - Specific requirements not addressed
4. **💡 Recommendations** - Prioritized with standard citations
5. **📝 Implementation Notes** - Practical remediation guidance

## Acceptance Criteria

- [ ] All 8 prompt files executed successfully
- [ ] All output files generated in `assessments/assessment.3/`
- [ ] Each file includes complete AI provenance metadata
- [ ] Each analysis follows the required format structure
- [ ] IEC 62304 section citations are accurate and specific
- [ ] Gap analysis identifies critical vs. minor issues
- [ ] Recommendations are actionable with clear implementation steps
- [ ] Executive summary synthesizes findings across all clauses
- [ ] AI conversation logs created per `.github/instructions/ai-assisted-output.instructions.md`

## Additional Context

### Assessment Comparison

This is the third assessment iteration:

- **Assessment 1**: Preliminary analysis without embedded standard text
- **Assessment 2**: Detailed analysis with embedded standard text and justifications
- **Assessment 3**: Current execution - should leverage lessons from previous assessments

### Key Focus Areas

- Software safety classification requirements (Class A, B, C)
- Traceability matrix completeness
- Risk management integration throughout lifecycle
- Documentation adequacy for regulatory submission
- Verification and validation strategy alignment

## Deliverables

Upon completion, the `assessments/assessment.3/` folder should contain:

```
assessment.3/
├── D0003329_Rev_03_IEC62304_Compliance_Assessment_2025-12-17.md
├── D0003329_REV_03_Final.Analysis.Clause4.4.md
├── D0003329_REV_03_Final.Analysis.Clause5.md
├── D0003329_REV_03_Final.Analysis.Clause6.md
├── D0003329_REV_03_Final.Analysis.Clause7.md
├── D0003329_REV_03_Final.Analysis.Clause8.md
├── D0003329_REV_03_Final.Analysis.Clause9.md
└── D0003329_REV_03_Final.IEC62304_Executive_Summary.md
```

## Notes for Coding Agent

- Execute prompts sequentially to maintain logical flow
- Ensure consistent terminology and compliance ratings across all analyses
- Cross-reference findings between clauses where applicable
- Flag any ambiguities or conflicting interpretations
- Generate comprehensive AI conversation logs for audit trail

---

**Priority**: High
**Complexity**: Complex - Multi-stage analysis requiring regulatory domain expertise
**Estimated Duration**: 4-6 hours for comprehensive execution

#github-pull-request_copilot-coding-agent
