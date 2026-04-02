---
assessment_type: "IEC 62304 Clause 8 Gap Justifications"
target_document: "D0003329_Rev_03_Final.md"
reference_standard: "IEC 62304 (BS EN 62304:2006+A1:2015)"
assessment_date: "2025-12-16"
clause: "8"
ai_generated: true
model: "anthropic/claude-3.5-sonnet@2024-10-22"
operator: "GitHub Copilot (Medical-Device-Design-Controls-Expert mode)"
chat_id: "gap-justifications-20251216"
ai_log: "assessments/assessment.2/conversation.md"
source: "D0003329_REV_03_Final.Analysis.Clause8.md"
---

# IEC 62304 Clause 8 (Configuration Management) - Gap Justifications

## Document Purpose

This document provides justifications for critical compliance gaps identified in D0003329 Rev 03 §6.12 (Software Configuration Management) against IEC 62304 Clause 8 requirements.

---

## Critical Gap #1: Missing SOUP Identification Requirements (§8.1.2)

### IEC 62304 Requirement

§8.1.2 requires: "For each SOUP CONFIGURATION ITEM being used, including standard libraries, the MANUFACTURER shall document:
a) the title,
b) the MANUFACTURER, and
c) the unique SOUP designator"

### Gap Identified

D0003329 §6.12 does NOT require documentation of SOUP title, manufacturer, or unique designator (version). Only "description of SOUP items" is required in architecture (§6.4).

### Justification for Finding

**Root Cause**: SOUP configuration management requirements were not explicitly translated from IEC 62304 into D0003329. While §6.4 (Architecture) mentions SOUP description and §6.12 acknowledges SOUP as configuration items, the specific three-part identification requirement from §8.1.2 was not incorporated.

**Regulatory Impact**:

- **Severity**: CRITICAL
- **Audit Risk**: VERY HIGH - This is explicit, measurable requirement that auditors specifically check
- **Standard Violation**: IEC 62304 §8.1.2 applies to ALL classes (A, B, C)
- **FDA SBOM**: Software Bill of Materials (SBOM) requirements in FDA 2023 cybersecurity guidance require SOUP manufacturer and version
- **EU MDR**: Annex II requires identification of software including "software version"

**Safety/Quality Implications**:

1. **Cybersecurity Vulnerabilities**:
   - Cannot identify which devices are affected by CVE-published vulnerabilities
   - Cannot determine if security patches are needed
   - Cannot trace vulnerability to specific SOUP version deployed
2. **Maintenance Risks**:
   - Cannot identify which SOUP versions are in field
   - Cannot determine compatibility when updating SOUP
   - Cannot replicate exact configuration for bug reproduction
3. **Regulatory Non-Compliance**:
   - Cannot generate SOUP BOM for premarket submissions
   - Cannot respond to FDA/notified body questions about SOUP versions
   - Cannot demonstrate SOUP control per IEC 62304
4. **Recall Management**:
   - Cannot identify which devices affected by SOUP defect
   - Cannot determine scope of field action
   - Cannot notify customers of specific versions needing update

**Evidence from Assessment**:

- Assessment identifies: "MISSING MANDATORY ELEMENTS - D0003329 does **not** explicitly require documentation of: SOUP title, SOUP manufacturer, Unique SOUP designator" - Critical Gap #1 (Analysis.Clause8.md)
- Table shows:
  - SOUP title: ⚠️ PARTIAL (implicit in "description")
  - SOUP manufacturer: ❌ MISSING
  - Unique SOUP designator: ❌ MISSING
- IEC 62304 §8.1.2 is mandatory for ALL safety classes
- D0003329 §6.4 requires only "description of SOUP items" - far less specific than §8.1.2

**Why This Matters**:
SOUP identification is fundamental to software configuration management:

**Example - Medical Imaging Device**:

- Uses OpenSSL for secure communications
- **Without §8.1.2 documentation**:

  - Architecture doc states: "Uses OpenSSL for encryption"
  - No manufacturer documented (OpenSSL Software Foundation)
  - No version documented
  - CVE-2021-3711 published (critical vulnerability in OpenSSL 1.1.1k and earlier)
  - **Impact**: Cannot determine if device is affected → Cannot assess risk → Cannot plan updates

- **With §8.1.2 documentation**:
  - SOUP BOM entry:
    - Title: OpenSSL
    - Manufacturer: OpenSSL Software Foundation
    - Unique Designator: Version 1.1.1j, released 2021-02-16
  - CVE-2021-3711 affects versions ≤ 1.1.1k
  - **Impact**: Device affected → Risk assessment performed → Update planned → Customers notified

**Modern Regulatory Landscape**:
FDA 2023 Premarket Cybersecurity Guidance requires:

- Software Bill of Materials (SBOM)
- For each software component including SOUP:
  - Name (= title)
  - Vendor (= manufacturer)
  - Version (= unique designator)

IEC 62304 §8.1.2 (published 2006) was forward-thinking - it already required what modern cybersecurity regulations demand.

**SOUP Identification Components**:

1. **Title**: Product name

   - Examples: "OpenSSL", "Qt Framework", "Linux Kernel", "Microsoft .NET Runtime"

2. **Manufacturer**: Vendor/developer name

   - Examples: "OpenSSL Software Foundation", "The Qt Company", "Linux Foundation", "Microsoft Corporation"
   - Critical for: Determining authority for security bulletins, license compliance, support contacts

3. **Unique Designator** (IEC 62304 NOTE: "could be, for example, a VERSION, a release date, a patch number or an upgrade designation"):
   - Examples: "1.1.1j", "5.15.2", "v5.10.17", ".NET 6.0.3"
   - Version number most common
   - Release date acceptable if version not available
   - Patch level critical for security (e.g., OpenSSL 1.1.1k patch 1 vs patch 2)

**Standard Libraries Inclusion**:
IEC 62304 explicitly states "including standard libraries" - this means:

- C/C++ standard library (glibc, newlib, MSVCRT)
- Python standard library modules
- Java standard library (JRE version)
- .NET Framework/Core libraries
- JavaScript runtime libraries

Many manufacturers overlook standard libraries, but they are SOUP and must be identified per §8.1.2.

**Remediation Rationale**:
The recommended fix (add explicit §8.1.2 requirements to §6.12 with SOUP BOM mandate) is appropriate because:

1. **IEC 62304 Compliance**: Directly implements §8.1.2 mandatory requirement
2. **Cybersecurity**: Enables CVE tracking and vulnerability management (integrates with D0029257)
3. **Regulatory**: Supports FDA SBOM requirements and EU MDR technical documentation
4. **Practical**: SOUP BOM is simple table/spreadsheet:
   | SOUP Item | Title | Manufacturer | Version | Release Date | Purpose | Risk Class |
   |-----------|-------|--------------|---------|--------------|---------|------------|
5. **Maintenance**: Critical for SOUP update planning and compatibility assessment
6. **Traceability**: Links SOUP to architecture, risk assessment, and verification
7. **Audit Readiness**: Provides immediate evidence of SOUP control

---

## Critical Gap #2: Missing Change Traceability Requirements (§8.2.4)

### IEC 62304 Requirement

§8.2.4 requires: "The MANUFACTURER shall provide a means for the traceability of a CHANGE REQUEST to:
a) the originating PROBLEM REPORT;
b) the approval authorizing the change; and
c) the CHANGE CONTROL records."

### Gap Identified

D0003329 does NOT require traceability between change requests, problem reports, and approvals. Only requirements-to-tests traceability is addressed.

### Justification for Finding

**Root Cause**: D0003329 §6.8 addresses requirements traceability but not change management traceability. The work instruction does not establish the change request ↔ problem report ↔ approval linkage required by §8.2.4.

**Regulatory Impact**:

- **Severity**: CRITICAL
- **Audit Risk**: VERY HIGH - Auditors will ask "Show me the change request for this problem report" and "Show me approval for this change"
- **Standard Violation**: IEC 62304 §8.2.4 applies to ALL classes (A, B, C)
- **21 CFR 820.30(i)**: Design changes must be documented; traceability is implicit requirement
- **ISO 13485:2016 §7.3.9**: Design changes must be reviewed, verified, validated before implementation - requires traceability

**Safety/Quality Implications**:

1. **Unapproved Changes**:
   - Cannot verify that implemented change was actually approved
   - No audit trail from authorization to implementation
   - Risk of unauthorized modifications
2. **Orphaned Changes**:
   - Changes implemented without documented rationale
   - Cannot trace why change was made
   - Difficult to assess if change actually solved problem
3. **Incomplete Problem Resolution**:
   - Problem reported but corresponding change request not traceable
   - Cannot verify all problems have been addressed
   - Trend analysis impossible (cannot link multiple changes to root cause)
4. **Regulatory Inspection Failures**:
   - Cannot demonstrate that changes were controlled
   - Cannot show that approvals were obtained before implementation
   - Cannot link post-market problems to corrective actions

**Evidence from Assessment**:

- Assessment states: "No requirement to maintain records linking change requests ↔ problem reports ↔ approvals. Only requirements-to-tests traceability exists." - Critical Gap #2 (Analysis.Clause8.md)
- IEC 62304 §8.2.4 requires THREE traceability links:
  - (a) Change Request → Problem Report
  - (b) Change Request → Approval
  - (c) Change Request → Change Control Records
- D0003329 §6.8 addresses only requirement → test traceability (different requirement)

**Why This Matters**:
Change traceability is essential for demonstrating controlled process:

**Traceability Flow**:

```
Problem Report #PR-123
    ↓ (link required by §8.2.4.a)
Change Request #CR-456
    ↓ (link required by §8.2.4.b)
Approval Record (who, when, signature/electronic approval)
    ↓ (link required by §8.2.4.c)
Change Control Records:
  - Configuration items modified
  - Verification results
  - Release record
```

**Without Traceability**:

- Auditor: "Show me the approval for this software change"
- Team: "We know it was approved but can't find the approval record for this specific change"
- Result: Observation/Finding - Uncontrolled change

**With Traceability**:

- Auditor: "Show me the approval for this software change"
- Team: Opens change request CR-456 → Links show:
  - Originated from Problem Report PR-123
  - Approved by [Name] on [Date] per approval record [ID]
  - Implemented in version 2.3.1 per release record
  - Verified per test report [ID]
- Result: Compliance demonstrated

**Real-World Scenario - Device Recall**:

- FDA requires: "Identify all software changes made in the 6 months before recall"
- **Without traceability**:

  - Search through hundreds of source code commits
  - Try to remember which changes were related to which problems
  - Cannot definitively link changes to approvals
  - **Result**: Cannot demonstrate that changes were properly controlled

- **With traceability**:
  - Query change management system for changes in timeframe
  - Each change shows:
    - Problem that triggered it
    - Who approved it
    - What was modified
    - How it was verified
  - **Result**: Complete audit trail provided to FDA

**Traceability Mechanisms**:
Modern implementation:

1. **Defect Tracking System** (e.g., Jira, Azure DevOps):

   - Problem Report = Issue/Bug
   - Change Request = Linked issue or custom "Change Request" type
   - Approval = Workflow state transition (requires approval to move to "Approved")
   - Change Control Records = Linked commits, pull requests, test results

2. **Traceability Matrix**:

   - Spreadsheet or database linking:
     - Problem Report ID → Change Request ID
     - Change Request ID → Approval Record ID
     - Change Request ID → Modified files/versions
     - Change Request ID → Verification record ID

3. **Version Control Integration**:
   - Git commits reference change request number in commit message
   - Pull requests linked to change requests
   - Branch names include change request ID

**Remediation Rationale**:
The recommended fix (add §8.2.4 traceability requirements to §6.12) is appropriate because:

1. **IEC 62304 Compliance**: Directly implements §8.2.4 mandatory requirement
2. **Quality Assurance**: Demonstrates controlled change process
3. **Audit Readiness**: Provides immediate evidence for any change
4. **Problem Resolution**: Ensures problems trigger changes and changes solve problems (closed loop)
5. **Regulatory**: Supports 21 CFR 820.30(i), ISO 13485 §7.3.9
6. **Integration**: Links §6.12 (Configuration Management) with:
   - §6.13 (Problem Resolution) via problem reports
   - Change approval processes
   - Verification (§6.8) via test records
7. **Practical**: Modern tools (Jira, Azure DevOps, GitHub) support this linkage natively

---

## Significant Gap #3: Missing Configuration Status Accounting (§8.3)

### IEC 62304 Requirement

§8.3 requires: "The MANUFACTURER shall provide a means for the recording and reporting of information related to the configuration status of the CONFIGURATION ITEMS, at least for CLASS B and CLASS C SOFTWARE."

### Gap Identified

D0003329 §6.12 requires "validated, controlled, and auditable repositories" but does NOT explicitly require recording WHO made changes, WHEN, WHY, or configuration status reporting.

### Justification for Finding

**Root Cause**: Repository requirement (Para 4) establishes infrastructure but does not mandate the specific status accounting activities required by §8.3 (recording history, reporting status).

**Regulatory Impact**:

- **Severity**: SIGNIFICANT
- **Audit Risk**: HIGH - Configuration status accounting is essential for demonstrating control
- **Standard Violation**: IEC 62304 §8.3 applies to Class B and C
- **21 CFR 820.186**: History records must include "dates and times"
- **Recall Management**: Cannot identify affected configurations without status accounting

**Safety/Quality Implications**:

1. **Cannot Recreate Historical Configurations**:
   - Unable to build exact version that was released
   - Cannot reproduce field-reported defects
   - Cannot verify which version was in affected device
2. **Change Accountability Missing**:
   - Cannot determine who made changes
   - Cannot determine when changes were made
   - Cannot determine why changes were made
3. **Configuration Status Unknown**:
   - Don't know which items are under development vs. released
   - Cannot report current configuration of deployed devices
   - Cannot track progression of changes through lifecycle
4. **Audit Trail Gaps**:
   - Cannot demonstrate change history
   - Cannot show configuration evolution
   - Cannot verify that only approved changes were made

**Evidence from Assessment**:

- Assessment identifies: "No explicit requirements for who/when/why recording, change request status tracking, or reporting capability" - Significant Gap #8 (Analysis.Clause8.md)
- IEC 62304 §8.3 requires "recording and reporting"
- D0003329 §6.12 Para 4 requires "auditable repositories" but doesn't define what must be recorded

**Why This Matters**:
Configuration status accounting = knowing the history and current state of all configuration items.

**Required Information (implicit in §8.3)**:
For each configuration item:

- **Who**: Author of change, approver
- **When**: Date/time of change, date of approval
- **Why**: Change rationale, linked change request
- **What**: Description of change, files modified
- **Status**: Development, under review, released, obsolete

**Configuration Status Reports**:

- **Item Status Report**: List all configuration items with current status
- **Change Status Report**: List all change requests with status (pending, approved, implemented)
- **Release Configuration Report**: Exact set of items/versions comprising a release
- **Configuration Audit Report**: Comparison of documented vs. actual configuration

**Real-World Scenario - Medical Device Investigation**:

- **Incident**: Patient alarm failed to sound
- **Investigation**: Which software version was in device?
- **Without Status Accounting**:

  - Device has version "2.1" sticker
  - Source code repository has multiple "2.1" versions (dev, test, release)
  - Cannot determine EXACTLY which configuration item versions were in device
  - **Impact**: Cannot reliably reproduce issue → Investigation stalled

- **With Status Accounting**:
  - Device serial number → Configuration management system
  - System shows: Version 2.1.0 build 1234, released 2023-03-15
  - Configuration report shows exact versions of all items in build 1234
  - **Impact**: Exact configuration recreated → Issue reproduced → Root cause found

**Version Control Systems**:
Modern VCS (Git, SVN, etc.) automatically record:

- Who (commit author)
- When (commit timestamp)
- What (file changes)

But require process to record:

- Why (commit message - must reference change request)
- Status (tags, branches, release labels)
- Approval (pull request approval, protected branches)

D0003329 should explicitly require these capabilities, not just "auditable repositories."

**Remediation Rationale**:
The recommended fix (add new §6.12.2 Configuration Status Accounting section) is appropriate because:

1. **IEC 62304 Compliance**: Implements §8.3 requirement for Class B/C
2. **Traceability**: Complements §8.2.4 change traceability
3. **Recall Management**: Enables identification of affected configurations
4. **Investigation Support**: Enables reproduction of historical configurations
5. **Audit Preparation**: Provides configuration status reports for auditors
6. **Process Control**: Demonstrates configuration under control throughout lifecycle
7. **Tool Agnostic**: Can be implemented with Git, SVN, Azure DevOps, or other VCS with proper processes

---

## Summary

These three gaps represent **critical absences** in D0003329 §6.12 configuration management:

1. **§8.1.2**: SOUP identification (title, manufacturer, version) not required - CRITICAL
2. **§8.2.4**: Change traceability (problem → change → approval) not required - CRITICAL
3. **§8.3**: Configuration status accounting (history, reporting) insufficiently detailed - SIGNIFICANT

**Current State**: §6.12 establishes configuration management planning and repository requirements but lacks:

- SOUP-specific identification mandates
- Change management traceability mechanisms
- Explicit status accounting requirements

**Impact on Compliance**: 25% compliant (0 of 8 sub-requirements fully compliant, 6 partial, 2 missing)

**Remediation Priority**:

1. **Immediate**: SOUP identification (§8.1.2) - Required for cybersecurity, regulatory submissions
2. **Immediate**: Change traceability (§8.2.4) - Fundamental to demonstrating controlled process
3. **Near-term**: Status accounting (§8.3) - Enhances existing repository requirements

All remediations leverage existing tools and processes; no new infrastructure required.

---

**Prepared**: December 16, 2025
**Related Documents**:

- D0003329_REV_03_Final.Analysis.Clause8.md (source assessment)
- D0003329 Rev 03 Final.md (target document)
- IEC 62304:2006+A1:2015 (reference standard)
