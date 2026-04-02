# Prompts Analysis: IEC 62304 Assessment Templates

## IEC 62304 Compliance Assessment  

**Files Assessed**: All prompt files in `.github/prompts/` directory  
**Assessment Date**: December 19, 2025  
**Purpose**: Evaluate assessment prompt templates for IEC 62304 compliance coverage  
**Classification**: Assessment Templates (Supporting IEC 62304 compliance verification)

## Executive Summary

The prompts directory contains comprehensive assessment templates that systematically address all IEC 62304 clauses and requirements. These templates provide structured, systematic approaches to compliance assessment that align with regulatory audit requirements and industry best practices.

**Overall Assessment**: ✅ **COMPREHENSIVE IEC 62304 COVERAGE** with excellent systematic methodology

## Prompt Files Analysis

### Primary Assessment Prompt

#### assess-d0003329-iec62304-compliance.prompt.md

✅ **COMPREHENSIVE FRAMEWORK**:
- **Complete IEC 62304 Coverage**: Addresses all sections (4.4, 5.1-5.8, 6, 7, 8, 9)
- **Systematic Methodology**: Three-phase approach (Loading, Mapping, Assessment)  
- **Proper File Dependencies**: Requires primary document, standard reference, and context
- **Risk-Based Approach**: Integrates software safety classification throughout assessment

**Methodology Alignment with IEC 62304**:
```
Phase 1: Document Loading & Context → Supports §4.1 QMS documentation review
Phase 2: Compliance Mapping → Systematic requirement verification per each clause
Phase 3: Gap Analysis & Reporting → Evidence-based compliance assessment
```

✅ **Assessment Structure Strengths**:
- Section-by-section systematic review
- "Shall" requirement identification and mapping
- Gap analysis with severity classification  
- Actionable remediation recommendations
- Standard citation requirements for traceability

#### IEC 62304 Section Coverage Analysis

| Prompt File | IEC 62304 Section | Coverage Quality | Assessment |
|-------------|------------------|------------------|------------|
| assess-d0003329-clause4.4-legacy.prompt.md | §4.4 Legacy Software | ✅ Complete | Systematic legacy software risk assessment |
| assess-d0003329-clause5-development.prompt.md | §5.1-5.8 Development | ✅ Complete | Full lifecycle process coverage |
| assess-d0003329-clause6-maintenance.prompt.md | §6 Maintenance | ✅ Complete | Post-market software management |
| assess-d0003329-clause7-risk.prompt.md | §7 Risk Management | ✅ Complete | Software-specific risk processes |
| assess-d0003329-clause8-config.prompt.md | §8 Configuration Management | ✅ Complete | SOUP and version control |
| assess-d0003329-clause9-problems.prompt.md | §9 Problem Resolution | ✅ Complete | Systematic problem handling |

## Detailed Clause Analysis

### Clause 4.4: Legacy Software Assessment

✅ **STRENGTHS**:
- **Risk-Based Approach**: Aligns with IEC 62304:2006+A1:2015 risk-based legacy software assessment
- **Safety Classification Integration**: Links legacy software assessment to current safety class
- **Documentation Assessment**: Evaluates available documentation against current requirements
- **Hazard Analysis**: Systematic hazard identification for legacy software

✅ **IEC 62304 §4.4 COMPLIANCE**:
- Addresses software developed prior to IEC 62304 compliance
- Risk-based approach per Amendment 1 guidance
- Integration with current device risk management
- Systematic documentation gap assessment

**Assessment Methodology**:
```
1. Legacy software identification and categorization
2. Available documentation assessment  
3. Risk analysis for legacy software components
4. Gap analysis against current IEC 62304 requirements
5. Risk-benefit assessment for bringing into compliance vs. replacement
```

### Clause 5: Software Development Processes  

✅ **COMPREHENSIVE LIFECYCLE COVERAGE**:
- **Planning (§5.1)**: Software Development Plan assessment methodology
- **Requirements (§5.2)**: Requirements analysis and traceability verification
- **Architecture (§5.3)**: Architectural design assessment and SOUP integration  
- **Detailed Design (§5.4)**: Design documentation and verification planning
- **Implementation (§5.5)**: Unit implementation and verification assessment
- **Integration (§5.6)**: Integration testing and verification procedures
- **System Testing (§5.7)**: System-level testing and validation
- **Release (§5.8)**: Software release procedures and documentation

**Traceability Assessment Framework**:
```
Requirements → Design → Implementation → Testing → Release
     ↓              ↓           ↓            ↓          ↓
Risk Analysis → Architecture → Unit Tests → Integration → System Testing
```

### Clause 6: Software Maintenance Processes

✅ **POST-MARKET SOFTWARE MANAGEMENT**:
- **Maintenance Planning**: Systematic approach to software maintenance planning
- **Change Analysis**: Impact assessment for software modifications  
- **Regression Testing**: Requirements for testing after software changes
- **Version Control**: Maintenance of software versions and baselines

✅ **IEC 62304 §6 COMPLIANCE**:
- Maintenance plan development and implementation
- Change request analysis and approval processes
- Risk assessment for software modifications
- Verification of software changes

### Clause 7: Software Risk Management Process

✅ **COMPREHENSIVE RISK MANAGEMENT**:
- **Hazard Analysis**: Software-specific hazard identification
- **Risk Analysis**: Software contribution to hazardous situations
- **Risk Control**: Implementation of software-based risk control measures
- **Risk Evaluation**: Post-mitigation risk assessment

✅ **ISO 14971 INTEGRATION**:
- Software hazard analysis integration with device risk management
- Software fault tree analysis methodologies
- Risk control measure verification and validation
- Post-market risk management integration

### Clause 8: Configuration Management Process

✅ **COMPREHENSIVE CM COVERAGE**:  
- **Configuration Identification**: Software item identification and versioning
- **Change Control**: Systematic change control procedures
- **Status Accounting**: Configuration status tracking and reporting
- **SOUP Management**: Software of Unknown Provenance evaluation and control

✅ **SOUP ASSESSMENT FRAMEWORK**:
```
SOUP Identification → Risk Assessment → Integration Planning → Verification
        ↓                    ↓               ↓              ↓
Documentation Review → Hazard Analysis → Testing Strategy → Release Control
```

### Clause 9: Problem Resolution Process

✅ **SYSTEMATIC PROBLEM HANDLING**:
- **Problem Identification**: Software problem detection and reporting
- **Investigation**: Root cause analysis methodologies  
- **Resolution**: Systematic problem resolution procedures
- **Verification**: Resolution verification and effectiveness assessment

## Assessment Template Quality Analysis

### Methodology Consistency

✅ **STANDARDIZED APPROACH**:
- All prompts follow consistent assessment structure
- Systematic section-by-section analysis methodology
- Standardized gap analysis and reporting formats
- Consistent citation and evidence requirements

✅ **REGULATORY ALIGNMENT**:
- Assessment approaches align with regulatory audit methodologies
- Evidence-based compliance verification
- Systematic documentation of findings and recommendations
- Clear traceability to IEC 62304 requirements

### Assessment Depth and Coverage

| Assessment Aspect | Coverage Quality | Notes |
|------------------|------------------|-------|
| Requirement Identification | ✅ Complete | All "shall" requirements identified |
| Gap Analysis | ✅ Systematic | Structured gap identification and classification |
| Risk Assessment | ✅ Integrated | Risk-based approach throughout |
| Remediation Planning | ✅ Actionable | Specific, implementable recommendations |
| Evidence Documentation | ✅ Comprehensive | Clear evidence requirements and citations |

## Recommendations for Enhancement

### Priority 1: Immediate Improvements

1. **Add Cybersecurity Assessment**
   ```markdown
   # New Prompt: assess-d0003329-cybersecurity.prompt.md
   ## IEC 62304:2006+A1:2015 Cybersecurity Requirements
   - Security risk assessment per Amendment 1
   - Cybersecurity controls verification  
   - Security lifecycle integration
   ```

2. **Enhance Integration Testing Assessment**
   ```markdown
   # Enhancement to clause5 prompt:
   ## Software Integration Testing (§5.6) Detailed Assessment
   - Interface testing verification
   - Integration strategy assessment
   - Test coverage analysis for integrated systems
   ```

3. **Add SOUP-Specific Assessment Template**
   ```markdown
   # New Prompt: assess-soup-evaluation.prompt.md  
   ## SOUP Assessment per IEC 62304 §8.1.2
   - SOUP identification and classification
   - Risk assessment specific to SOUP
   - Integration and verification requirements
   ```

### Priority 2: Process Integration Enhancements

4. **Cross-Document Validation Template**
   ```markdown
   # New Prompt: cross-validate-d0003329-d0003098.prompt.md
   ## D0003329/D0003098 Consistency Assessment
   - Requirement consistency verification
   - Process integration assessment  
   - Gap identification between documents
   ```

5. **Traceability Verification Template**  
   ```markdown
   # New Prompt: verify-iec62304-traceability.prompt.md
   ## End-to-End Traceability Verification
   - Requirements to design traceability
   - Design to implementation traceability
   - Test to requirements traceability
   ```

### Priority 3: Regulatory Support Enhancement

6. **Audit Preparation Template**
   ```markdown
   # New Prompt: prepare-iec62304-audit.prompt.md
   ## IEC 62304 Audit Readiness Assessment
   - Evidence completeness verification
   - Documentation organization for audit
   - Compliance demonstration preparation
   ```

7. **Technical File Generation Template**
   ```markdown
   # New Prompt: generate-technical-file-content.prompt.md  
   ## Technical File Software Documentation
   - IEC 62304 compliance summary generation
   - Software safety classification documentation
   - Risk management file software sections
   ```

## Implementation Recommendations

### New Prompt File Structure

```markdown
.github/prompts/
├── assess-d0003329-iec62304-compliance.prompt.md (existing - master template)
├── assess-d0003329-clause4.4-legacy.prompt.md (existing)
├── assess-d0003329-clause5-development.prompt.md (existing) 
├── assess-d0003329-clause6-maintenance.prompt.md (existing)
├── assess-d0003329-clause7-risk.prompt.md (existing)
├── assess-d0003329-clause8-config.prompt.md (existing)
├── assess-d0003329-clause9-problems.prompt.md (existing)
├── assess-d0003329-cybersecurity.prompt.md (new - Amendment 1)
├── assess-soup-evaluation.prompt.md (new - SOUP specific)
├── cross-validate-d0003329-d0003098.prompt.md (new - integration)
├── verify-iec62304-traceability.prompt.md (new - traceability)
├── prepare-iec62304-audit.prompt.md (new - audit prep)
└── generate-technical-file-content.prompt.md (new - regulatory)
```

### Quality Assurance Enhancements

1. **Prompt Validation Checklist**:
   - All IEC 62304 "shall" requirements addressed
   - Risk-based approach implemented consistently  
   - Evidence requirements clearly specified
   - Standard citations accurate and complete

2. **Assessment Methodology Verification**:
   - Systematic approach verification
   - Gap analysis completeness check
   - Remediation recommendation quality assessment
   - Regulatory alignment verification

## Conclusion

The current prompt templates provide excellent comprehensive coverage of IEC 62304 requirements with systematic, evidence-based assessment methodologies that align with regulatory audit standards.

**Key Strengths**:
✅ **Complete IEC 62304 Coverage**: All clauses systematically addressed  
✅ **Systematic Methodology**: Consistent, auditable assessment approach  
✅ **Risk-Based Assessment**: Integrated risk management throughout  
✅ **Actionable Outputs**: Clear, implementable recommendations  
✅ **Regulatory Alignment**: Assessment approaches suitable for audit evidence

**Enhancement Opportunities**:
⚠️ **Cybersecurity Integration**: Add Amendment 1 cybersecurity assessment capabilities  
⚠️ **SOUP-Specific Assessment**: Dedicated SOUP evaluation template  
⚠️ **Cross-Document Validation**: Integration assessment between related documents  
⚠️ **Audit Preparation**: Regulatory submission and audit preparation templates

**Overall Rating**: ✅ **EXCELLENT ASSESSMENT FRAMEWORK** - Comprehensive current coverage with clear enhancement path for complete regulatory support

The prompt templates establish a professional-grade framework for IEC 62304 compliance assessment that supports both internal quality assurance and external regulatory audit requirements. The recommended enhancements would provide complete coverage of all IEC 62304:2006+A1:2015 requirements including cybersecurity considerations.