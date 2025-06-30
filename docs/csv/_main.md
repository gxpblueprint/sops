---
title: Computerised System Validation SOP
version: 0.1-draft
effective-date: TBC
---

# 1 Purpose
This SOP defines the process for validating GMP computerised systems (new implementations and upgrades) to ensure they are fit for intended use and comply with regulatory expectations. It aligns with ISPE GAMP 5 guidance and requirements in 21 CFR Part 11 and EU GMP Annex 11. The procedure follows a risk-based lifecycle approach from planning through qualification and release to maintain a validated state.

# 2 Scope
This procedure applies to all GxP computerised systems used in development, manufacturing or quality control at [Company]. It covers new implementations and significant upgrades to existing systems, including software, hardware, network infrastructure and interfaces. The SOP focuses on on-premise deployments; cloud or SaaS systems require additional vendor qualification beyond this scope.

# 3 Responsibilities
| Role | Responsibility |
|------|---------------|
| System Owner | Define user needs, ensure validation activities occur and provide resources. Maintain compliance once live. |
| QA | Oversee the validation process, review and approve plans, protocols and results. Ensure change control preserves the validated state. |
| IT/Automation/Engineering | Install and support the system, execute technical testing and manage configuration or upgrades under change control. |
| Validation Lead | Plan and coordinate validation, maintain documentation and traceability. |
| Vendor/Supplier | Provide a system meeting specifications with supporting documentation and assistance. |
| End Users | Participate in defining requirements and executing PQ/UAT. Follow SOPs and complete training before use. |

# 4 Definitions
* **Computerised System** – hardware, software and associated equipment processing GxP data.
* **CSV** – Computerised System Validation.
* **URS** – User Requirements Specification.
* **Functional/Design Specification (FS/DS)** – documents describing how the system meets the URS.
* **DQ** – Design Qualification confirming the design satisfies requirements.
* **FAT** – Factory Acceptance Test at the supplier site.
* **SAT** – Site Acceptance Test after delivery.
* **IQ** – Installation Qualification verifying correct installation.
* **OQ** – Operational Qualification verifying functionality under defined conditions.
* **PQ** – Performance Qualification demonstrating routine use meets requirements.
* **RTM** – Traceability Matrix linking requirements to tests.
* **GxP** – Good Practice guidelines affecting product quality or patient safety.
* **Change Control** – formal process to manage system changes.

# 5 Procedure
![Validation life-cycle placeholder](./_images/v-model.png)

1. **Planning and Initiation** – start the project, define scope and create a validation plan based on risk assessment.
2. **Requirements Definition** – develop or update the URS and maintain traceability.
3. **Vendor Selection and Quality Assessment** – assess suppliers and review their documentation.
4. **Design and Configuration** – document functional and design specifications and perform risk assessment.
5. **Factory Acceptance Test (FAT)** – verify major functions at the supplier site when applicable.
6. **Site Acceptance Test (SAT)** – confirm correct installation and basic operation at the user site.
7. **Installation Qualification (IQ)** – verify installation and environment meet specifications.
8. **Operational Qualification (OQ)** – execute detailed functional tests under defined conditions.
9. **Performance Qualification (PQ) / User Acceptance** – demonstrate the system supports intended workflows with trained users.
10. **Data Migration Qualification** – verify accuracy and completeness of any migrated data.
11. **Release Decision and Documentation** – complete the RTM, resolve deviations and prepare a validation summary report for QA approval.
12. **Post-Implementation Activities** – manage changes under change control, conduct periodic reviews, handle incidents and maintain backups and documentation.

# 6 Appendices
* [Appendix A — RTM Template](app-a_rtm.md)
* [Appendix B — Validation Plan Checklist](app-b_vp.md)

![Placeholder diagram](./_images/placeholder.png)

Download the RTM workbook: [rtm-template.xlsx](./_files/rtm-template.xlsx)
