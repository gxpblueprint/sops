---
title: Computerised System Validation SOP
version: 0.2-draft
effective-date: TBC
---

# Procedure for computerised system validation (CSV)

## Purpose
This SOP defines how to validate GMP computerised systems so they are fit for use and compliant with
GAMP 5, 21 CFR Part 11 and EU Annex 11. It covers new implementations and upgrades using a risk-based lifecycle
approach to achieve and maintain a validated state.

## Scope
This procedure applies to all GxP computerised systems used in development, manufacturing or quality
control at [Company]. It includes software, hardware, network infrastructure and interfaces. Cloud or SaaS systems
require additional qualification beyond this SOP.


## Definitions
* **Computerised system** – hardware, software and associated equipment processing GxP data.
* **CSV** – computerised system validation.
* **URS** – user requirements specification describing intended use and regulatory needs.
* **Functional/design specification** – details how the system meets the URS.
* **DQ** – design qualification confirming the design satisfies the URS.
* **FAT** – factory acceptance test at the supplier site.
* **SAT** – site acceptance test after delivery.
* **IQ** – installation qualification verifying correct installation.
* **OQ** – operational qualification verifying functionality under defined conditions.
* **PQ** – performance qualification demonstrating routine use meets requirements.
* **RTM** – requirements traceability matrix linking requirements to tests.
* **GxP** – good practice guidelines affecting product quality or patient safety.
* **Change control** – formal process to manage system changes.
## Roles and responsibilities

* **System owner** – defines user needs, ensures validation activities occur and maintains compliance once live.
* **Quality assurance** – provides independent oversight, reviewing and approving documentation and deviations.
* **IT/automation/engineering** – installs and supports the system, executes technical testing and manages upgrades.
* **Validation lead** – coordinates the validation project and keeps traceability.
* **Vendor/supplier** – provides a system meeting specifications with supporting documentation.
* **End users** – help define requirements and perform PQ. They follow SOPs and complete training before use.
## Procedure

### 1 Planning and initiation
Initiate projects or changes within the quality system. Define scope
and objectives, perform a risk assessment and create a validation plan listing deliverables, responsibilities and
acceptance criteria.

### 2 Requirements definition
Develop or update the URS from user needs and regulatory requirements. Maintain
bidirectional traceability from requirements through design and testing using an RTM.

### 3 Vendor selection and quality assessment
Evaluate suppliers to ensure they operate an acceptable quality
system and provide adequate documentation. Document any audits or assessments performed.

### 4 Design and configuration
Create functional and design specifications describing how the system will meet
the URS. For configurable systems, document the configuration. Perform a functional risk assessment to identify
and mitigate potential failures.

### 5 Factory acceptance test (FAT)
Where appropriate, verify major functions at the supplier site before
delivery. Document any issues for resolution prior to installation.

### 6 Site acceptance test (SAT)
After delivery, confirm correct installation and basic operation in the user
environment. Resolve issues before formal qualification begins.

### 7 Installation qualification (IQ)
Verify that hardware, software and infrastructure are installed correctly
and documented. Capture evidence such as version numbers, configuration settings and initial backups.

### 8 Operational qualification (OQ)
Execute detailed functional tests under defined conditions to demonstrate
the system operates as intended. Include security, error handling and audit trail checks. Record any deviations
and their resolution.

### 9 Performance qualification (PQ)
Demonstrate that the system and users can perform routine workflows reliably. Use
real or simulated production scenarios and confirm SOPs and training are in place.

### 10 Data migration qualification
If data is migrated from a legacy system, plan and verify the transfer. Ensure
records are complete and accurate in the new system and document any discrepancies.

### 11 Release decision and documentation
Complete the RTM and resolve all deviations. Prepare a validation summary
report describing activities, results and conclusions. QA approval authorises release for GMP use.

### 12 Post-implementation activities
Maintain the validated state through change control, periodic review,
incident management, backups and ongoing training. Store validation documentation in a controlled archive.

## Appendices
* [Appendix A — RTM template](app-a_rtm.md)
* [Appendix B — Validation plan checklist](app-b_vp.md)
![Placeholder diagram](./_images/placeholder.png)

Download the RTM workbook: [rtm-template.xlsx](./_files/rtm-template.xlsx)
