---
assessment_type: "IEC 62304 Clause 7 Gap Justifications"
target_document: "D0003329_Rev_03_Final.md"
reference_standard: "IEC 62304 (BS EN 62304:2006+A1:2015)"
assessment_date: "2025-12-16"
clause: "7"
ai_generated: true
model: "anthropic/claude-3.5-sonnet@2024-10-22"
operator: "GitHub Copilot (Medical-Device-Design-Controls-Expert mode)"
chat_id: "gap-justifications-20251216"
ai_log: "assessments/assessment.2/conversation.md"
source: "D0003329_REV_03_Final.Analysis.Clause7.md"
---

# IEC 62304 Clause 7 (Software Risk Management) - Gap Justifications

## Document Purpose

This document provides justifications for critical compliance gaps identified in D0003329 Rev 03 §6.11 (Software-Specific Elements of the Risk Management Process) against IEC 62304 Clause 7 requirements.

---

## Critical Gap #1: Missing SOUP Anomaly Evaluation Process (§7.1.3)

### IEC 62304 Requirement

§7.1.3 requires: "If failure or unexpected results from SOUP is a potential cause of the SOFTWARE ITEM contributing to a hazardous situation, the MANUFACTURER shall EVALUATE as a minimum any ANOMALY list published by the supplier of the SOUP item relevant to the VERSION of the SOUP item used in the MEDICAL DEVICE..."

### Gap Identified

D0003329 §6.11 does NOT address SOUP anomaly evaluation despite SOUP being mentioned as part of hazard identification.

### Justification for Finding

**Root Cause**: While §6.11 mentions "including SOUP" in software items contributing to hazards, the specific requirement to evaluate published SOUP anomaly lists was not translated into procedural guidance. This represents an oversight in translating all §7.1 sub-requirements.

**Regulatory Impact**:

- **Severity**: CRITICAL
- **Audit Risk**: VERY HIGH - Specific, measurable, auditable requirement
- **Standard Violation**: IEC 62304 §7.1.3 explicit requirement for Class B/C
- **Cybersecurity**: FDA premarket cybersecurity guidance requires SOUP vulnerability assessment
- **EU MDR**: SOUP management is key element of technical documentation

**Safety/Quality Implications**:

1. **Known Vulnerabilities Deployed**:
   - CVE-listed vulnerabilities in SOUP may exist in deployed devices
   - Security patches available but not evaluated/applied
   - Exploitable weaknesses create patient safety risks
2. **Functional Defects Unrecognized**:
   - SOUP vendors publish known defects in release notes
   - Medical device manufacturer may use SOUP version with known bugs
   - Bugs that could contribute to hazards not assessed
3. **Version-Specific Issues**:
   - Different SOUP versions have different anomaly profiles
   - Using outdated version with critical defects
   - Upgrade path not informed by anomaly evaluation

**Evidence from Assessment**:

- Assessment states: "No procedure for evaluating published SOUP anomaly lists (CVE databases, vendor security bulletins)" - Critical Gap #1 (Analysis.Clause7.md)
- IEC 62304 §7.1.3 applies when SOUP is potential cause contributing to hazardous situation
- D0003329 §6.11 mentions SOUP in hazard identification but not anomaly evaluation
- D0029257 (Cybersecurity) exists but integration with §7.1.3 not explicit

**Why This Matters**:
Modern medical devices rely heavily on SOUP:

- Operating systems (Linux, Windows Embedded, RTOS)
- Libraries (OpenSSL, Boost, Qt, etc.)
- Frameworks (.NET, Java runtime, Python interpreter)
- Databases (SQLite, PostgreSQL)
- Communication stacks (TCP/IP, Bluetooth, WiFi)

Each SOUP item has:

- **CVE Database**: Common Vulnerabilities and Exposures (cve.mitre.org, nvd.nist.gov)
- **Vendor Security Bulletins**: Microsoft Security Response Center, Ubuntu Security Notices, etc.
- **Release Notes**: Known issues, bug fixes, deprecated features
- **Issue Trackers**: GitHub Issues, JIRA, Bugzilla for open-source SOUP

**Real-World Scenario**:

- **Device**: Patient monitoring system using OpenSSL 1.0.2g for secure data transmission
- **Without §7.1.3 evaluation**:
  - Development team selects OpenSSL 1.0.2g (latest at time)
  - Device released, deployed to hospitals
  - **6 months later**: CVE-2016-6309 published (high severity, buffer overflow in OpenSSL 1.0.2g allowing remote code execution)
  - Medical device manufacturer **unaware** (no monitoring process)
  - Devices remain vulnerable for months/years
- **With §7.1.3 evaluation**:
  - Initial selection: Evaluate OpenSSL 1.0.2g anomaly list → No critical issues
  - **Periodic re-evaluation** (quarterly): CVE-2016-6309 discovered
  - Analysis: Remote code execution could allow attacker to manipulate patient data display → hazardous situation
  - Response: Emergency patch release, customer notification, possible MDR/FSCA

**Cybersecurity Integration**:
FDA premarket cybersecurity guidance (2023) explicitly requires:

- Software Bill of Materials (SBOM) including SOUP
- Vulnerability management process
- Regular monitoring of CVE databases

IEC 62304 §7.1.3 predates modern cybersecurity focus but the requirement is directly applicable:

- "Anomaly" includes security vulnerabilities
- Evaluation determines if anomaly "could result in hazardous situation"
- For networked devices, many CVEs can contribute to hazards

D0029257 (Cybersecurity Work Instruction) should be integrated with §7.1.3 requirement - cybersecurity vulnerability assessment IS a type of SOUP anomaly evaluation.

**Remediation Rationale**:
The recommended fix (add explicit SOUP anomaly evaluation requirement with CVE database references and coordination with D0029257) is appropriate because:

1. **IEC 62304 Compliance**: Directly implements §7.1.3 mandatory requirement
2. **Patient Safety**: Prevents deployment of devices with known SOUP vulnerabilities
3. **Cybersecurity**: Aligns with FDA/IMDRF cybersecurity guidance
4. **Practical**: Specifies WHERE to find anomaly lists (CVE, vendor bulletins, release notes)
5. **Continuous**: Requires periodic re-evaluation (not just one-time at selection)
6. **Integration**: Coordinates with existing D0029257 cybersecurity procedures
7. **Documentation**: Requires evaluation results in Risk Management File for audit trail

---

## Critical Gap #2: No Explicit Risk Control Verification Process (§7.3.1)

### IEC 62304 Requirement

§7.3.1 requires: "The MANUFACTURER shall verify that the RISK CONTROL measures are implemented and effective. Additionally, the MANUFACTURER shall review the RISK CONTROL measure for addition of new HAZARDS."

### Gap Identified

D0003329 §6.11 does NOT explicitly require verification of risk control measure implementation or review for new hazards introduced by risk controls.

### Justification for Finding

**Root Cause**: §6.11 paragraph 3 addresses risk control implementation in software requirements but does not address the subsequent verification step or "new hazard" review required by §7.3.1.

**Regulatory Impact**:

- **Severity**: CRITICAL
- **Audit Risk**: VERY HIGH - Verification of safety measures is fundamental requirement
- **Standard Violation**: IEC 62304 §7.3.1 two-part requirement (verification + new hazard review) not addressed
- **ISO 14971**: Risk control verification is required by ISO 14971:2019 §7.4
- **FDA**: Risk control verification essential for premarket submission acceptance

**Safety/Quality Implications**:

1. **Unverified Risk Controls**:
   - Risk control may be specified but not actually implemented
   - Implementation may be incorrect or incomplete
   - Risk control may not be effective in actual use conditions
2. **New Hazards from Risk Controls**:
   - Risk control introduces different hazard (risk-risk tradeoff not assessed)
   - Example: Alarm volume increased (risk control for missed alarms) → Creates hazard from startle response
   - Example: Input validation added → Rejects valid inputs, creating usability hazard
3. **Verification Gaps**:
   - Testing may not specifically target risk control measures
   - Design reviews may not verify risk control implementation
   - Inspection/static analysis may miss risk control logic

**Evidence from Assessment**:

- Assessment identifies: "No explicit requirement to verify each risk control implementation; missing 'new hazard' review requirement" - Critical Gap #2 (Analysis.Clause7.md)
- IEC 62304 §7.3.1 has two distinct requirements: (1) verify implementation and effectiveness, (2) review for new hazards
- D0003329 §6.11 paragraph 3 addresses risk control implementation in requirements but not verification
- §6.8 (Software System Testing) does not explicitly require risk control verification tests

**Why This Matters**:
Risk control verification closes the loop:

```
Hazard Identified → Risk Control Defined → Risk Control Implemented → **Risk Control Verified**
                                                                              ↓
                                                                    Actually Works as Intended
                                                                    + No New Hazards Created
```

Without verification:

- **Scenario 1**: Radiation therapy device

  - Hazard: Excessive dose delivery
  - Risk Control: Software limits maximum dose to 5 Gy
  - Implementation: Dose limit coded as constant
  - **Missing Verification**: Limit never tested under extreme input conditions
  - **Field Failure**: Edge case allows 10 Gy delivery → Patient injury
  - **Root Cause**: Risk control implementation not verified

- **Scenario 2**: Infusion pump
  - Hazard: Over-infusion due to hardware failure
  - Risk Control: Software monitors pressure sensor, stops infusion if anomaly detected
  - Implementation: Monitoring code added
  - **Missing "New Hazard" Review**: Monitoring algorithm rejects valid sensor readings in certain patient positions
  - **Result**: False alarms cause clinician to disable monitoring → defeats risk control

Verification methods for risk controls:

1. **Code Inspection**: Verify risk control logic present and correct
2. **Design Review**: Verify architecture supports risk control
3. **Unit Testing**: Test risk control logic in isolation
4. **Integration Testing**: Test risk control in system context
5. **System Testing**: Test risk control under realistic use conditions
6. **Stress Testing**: Test risk control under boundary/extreme conditions

New hazard review:

1. Could risk control create usability problems?
2. Does risk control reject valid inputs/conditions?
3. Could risk control fail in a way that creates hazard?
4. Does risk control increase system complexity (introduce bugs)?
5. Does risk control have performance impact (timing hazards)?

**IEC 62304 §7.3.1 + ISO 14971 Alignment**:
ISO 14971:2019 §7.4: "For each risk control measure, the organization shall verify that:
a) the risk control measure is implemented
b) the risk control measure is effective"

IEC 62304 §7.3.1 adds software-specific requirement: review for NEW HAZARDS.

This is critical because software risk controls often introduce new software-specific hazards (complexity, timing, resource consumption, usability).

**Remediation Rationale**:
The recommended fix (add explicit verification requirement with integration to testing processes) is appropriate because:

1. **IEC 62304 Compliance**: Directly implements §7.3.1 two-part requirement
2. **ISO 14971 Alignment**: Implements ISO 14971:2019 §7.4 for software
3. **Safety Assurance**: Verifies risk controls actually work before release
4. **Proactive**: Identifies problems introduced by risk controls before field deployment
5. **Integration**: Links to existing verification processes:
   - D0017982 (Software Verification Protocol) for test requirements
   - §6.8 (Software System Testing) for execution
   - Risk Management File for documentation
6. **Traceability**: Ensures risk control verification traced per §7.3.3
7. **Complete Process**: Closes risk management loop (identify → control → verify)

---

## Critical Gap #3: Missing Change Risk Management Process (§7.4)

### IEC 62304 Requirement

§7.4.1: "The MANUFACTURER shall analyse changes to the MEDICAL DEVICE SOFTWARE (including SOUP) to determine whether: a) additional potential causes are introduced contributing to a hazardous situation; and b) additional software RISK CONTROL measures are required."

§7.4.2: "The MANUFACTURER shall analyse changes to the software, including changes to SOUP, to determine whether the software modification could interfere with existing RISK CONTROL measures."

§7.4.3: "The MANUFACTURER shall perform relevant RISK MANAGEMENT ACTIVITIES defined in 7.1, 7.2 and 7.3 based on these analyses."

### Gap Identified

D0003329 §6.11 does NOT address risk management of software changes (entire §7.4 section missing).

### Justification for Finding

**Root Cause**: §6.11 focuses on initial risk management (§7.1-7.3) but does not address ongoing risk management for changes. The critical requirement that ALL changes must be risk-analyzed was not incorporated into D0003329.

**Regulatory Impact**:

- **Severity**: CRITICAL
- **Audit Risk**: VERY HIGH - Software changes are primary source of new risks
- **Standard Violation**: IEC 62304 §7.4 entire section missing; applies to ALL classes (A, B, C)
- **FDA**: Software changes must be risk-assessed per 21 CFR 820.30(i)
- **ISO 14971**: §9 Production and post-production requires analysis of changes

**Safety/Quality Implications**:

1. **New Hazards from Changes**:
   - Software modifications introduce new failure modes
   - New features create new use scenarios with different risks
   - Bug fixes may have unintended consequences
2. **Risk Control Interference**:
   - Change may disable or bypass existing risk control
   - Performance of risk control may be degraded
   - Assumptions underlying risk control may be invalidated
3. **Unevaluated Risks**:
   - Changes released without risk assessment
   - No triggering of risk management activities (§7.1-7.3)
   - Risk Management File not updated

**Evidence from Assessment**:

- Assessment states: "No explicit requirement to analyze all changes for new hazards and risk control needs" and "Complete absence of §7.4" - Critical Gaps #3, #4, #5 (Analysis.Clause7.md)
- IEC 62304 §7.4 applies to ALL safety classes (A, B, C)
- §6.10 (Maintenance) mentions risk assessment but does not invoke §7.4
- §6.13 (Problem Resolution) mentions safety evaluation but not §7.4

**Why This Matters**:
Software changes are inherently risky:

- **Statistics**: 60-80% of software failures trace to changes
- **Complexity**: Ripple effects hard to predict
- **Assumptions**: Original design assumptions may not apply after change

**Without §7.4 Analysis:**

Change Requested → Developer Implements → Test → Release
(Missing: Risk Analysis)

**With §7.4 Analysis:**

```
Change Requested
    ↓
§7.4.1 Analysis: New hazards? New risk controls needed?
    ↓
§7.4.2 Analysis: Interferes with existing risk controls?
    ↓
§7.4.3: Perform §7.1-7.3 activities based on analysis
    ↓
Implement → Verify → Release
```

**Real-World Failure - Therac-25**:

- Software change to improve usability (reduce key presses)
- **Missing §7.4 analysis**: Change not assessed for safety impact
- Change introduced race condition in safety interlock
- Result: Massive radiation overdoses, patient deaths
- Root cause: Software change made without risk analysis

**Modern Example - Pacemaker**:

- Change: Update communication protocol for faster data transfer
- **§7.4.1 Analysis (new hazards)**:
  - New protocol more complex → potential for implementation bugs
  - Higher data rate → increased power consumption → battery life impact
  - **Decision**: New hazard identified → Perform §7.1 analysis
- **§7.4.2 Analysis (risk control interference)**:
  - Existing risk control: Checksum validation on communicated data
  - Analysis: New protocol uses different checksum → Must update validation
  - **Decision**: Risk control affected → Perform §7.3 re-verification
- **§7.4.3 Activities**:
  - §7.1: Identify new hazards from power consumption
  - §7.2: Define new risk controls (power management)
  - §7.3: Verify updated checksum validation
  - Result: Safe change deployment

**Applicability to ALL Changes**:
§7.4 applies to:

- Bug fixes
- Feature enhancements
- Performance improvements
- Security patches
- SOUP updates
- Configuration changes
- Maintenance modifications

Each requires risk analysis before implementation.

**Remediation Rationale**:
The recommended fix (add comprehensive §7.4 requirements to §6.11) is appropriate because:

1. **IEC 62304 Compliance**: Implements entire missing §7.4 section
2. **ALL Classes**: Applies to Class A, B, C (§7.4.1) and B, C (§7.4.2, §7.4.3)
3. **Proactive**: Identifies risks BEFORE changes implemented
4. **Integration**: Links to:
   - §6.10 (Maintenance) for maintenance changes
   - §6.13 (Problem Resolution) for problem-driven changes
   - §7.1-7.3 activities triggered by analysis
5. **Systematic**: Ensures consistent risk analysis of all changes
6. **Safety-Critical**: Prevents deployment of safety-degrading changes
7. **Regulatory**: Required by FDA, ISO 14971, IEC 62304

---

## Summary

These three critical gaps represent **fundamental absences** in D0003329 §6.11's risk management process:

1. **§7.1.3**: SOUP anomaly evaluation process missing
2. **§7.3.1**: Risk control verification and new hazard review not required
3. **§7.4**: Entire change risk management section missing

**Current State**: §6.11 addresses initial risk management (hazard identification, risk controls) but lacks:

- SOUP-specific evaluation procedures
- Verification closure of risk controls
- Ongoing risk management for changes

**Impact on Compliance**: 45% compliant (5 of 11 requirements adequately addressed)

**Remediation**: All gaps are remediable through additions to §6.11 establishing:

- SOUP anomaly evaluation procedures (integrate with D0029257 cybersecurity)
- Risk control verification requirements (integrate with §6.8 testing)
- Change risk management procedures (integrate with §6.10 maintenance and §6.13 problem resolution)

All remediations leverage existing D0003329 infrastructure and align with ISO 14971 risk management framework already referenced in §6.11.

---

**Prepared**: December 16, 2025
**Related Documents**:

- D0003329_REV_03_Final.Analysis.Clause7.md (source assessment)
- D0003329 Rev 03 Final.md (target document)
- IEC 62304:2006+A1:2015 (reference standard)
- ISO 14971:2019 (Risk management for medical devices)
