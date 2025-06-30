---
title: Computerised System Validation SOP
version: 0.3-draft
effective-date: TBC
status: Draft
---

# Procedure for Computerised System Validation (CSV) –  
GAMP 5 / 21 CFR Part 11 / EU Annex 11 Compliance

---

## 1  Purpose  
This SOP defines the process for validating GMP-relevant computerised systems—both **new implementations** and **upgrades**—so they are fit for intended use and compliant with:

* ISPE **GAMP 5** guidelines  
* **21 CFR Part 11** (FDA)  
* **EU GMP Annex 11**

It provides a **risk-based life-cycle framework**—from planning and requirements through IQ / OQ / PQ and release—to achieve and maintain a validated state.

---

## 2  Scope  
Applies to all **GxP computerised systems** used in development, manufacturing, or quality control at [Company] (e.g. LIMS, MES, SCADA/DCS, laboratory data-acquisition systems).  
Includes software, hardware, network infrastructure, and interfaces.  
*On-premises systems only; Cloud/SaaS require additional qualification.*

Both vendor-supplied and internally developed/configured systems are covered.

---

## 3  References  

| # | Reference |
|---|-----------|
| 1 | ISPE **GAMP 5** Guide |
| 2 | EU **EudraLex Vol 4 Annex 11: Computerised Systems** |
| 3 | **21 CFR Part 11**: Electronic Records / Electronic Signatures |
| 4 | WHO TRS 1019 Annex 3 – Qualification & Validation |
| 5 | [Company] Quality Policy & Validation Master Plan |

*(Inline numbers in text map to these references.)*

---

## 4  Definitions  

* **Computerised System** – hardware, software, and associated equipment that process GxP data.  
* **CSV** – Computerised System Validation.  
* **URS** – User Requirements Specification.  
* **FS/DS** – Functional / Design Specification.  
* **DQ / FAT / SAT / IQ / OQ / PQ** – Design Qualification & test stages.  
* **RTM** – Requirements Traceability Matrix.  
* **GxP** – Good Practice (GMP, GLP, GCP, …).  
* **Change Control** – formal change-management process.

*(Extended definitions appear inline throughout Procedure.)*

---

## 5  Roles & Responsibilities  

| Role | Responsibilities (summary) |
|------|----------------------------|
| **System Owner / Process Owner** | Define user needs; ensure URS & resources; maintain compliance (14, 15, 16) |
| **Quality Assurance (QA)** | Independent oversight; approve plans, protocols, deviations; release authorization (17, 18) |
| **IT / Automation / Engineering** | Install/support system; execute technical testing; manage security & upgrades (19–21) |
| **Validation Lead / CSV Coordinator** | Author Validation Plan; coordinate lifecycle; ensure traceability |
| **Vendor / Supplier** | Provide system & docs; maintain own quality system; assist FAT/SAT (22) |
| **End Users / SMEs** | Contribute URS; execute PQ/UAT; follow SOP & training |

---

## 6  Procedure  

### 6.1 Planning & Initiation  
1. **Project / Change initiation** (new vs. upgrade)  
2. Create **Validation Plan** with scope, deliverables, risk-based strategy (27–29)  
3. Document **Regulatory Impact** (Part 11 / Annex 11 controls in scope) (30)  
4. Perform initial **Risk Assessment** (GAMP 5 category; critical quality attributes) (26)

### 6.2 Requirements Definition  
* Draft / update **URS** – include regulatory, data-integrity, security, performance needs (31–34)  
* For upgrades: impact-analyse existing URS; add, modify, or retire requirements.  
* Begin **RTM**; maintain bidirectional traceability (11, 12).  

### 6.3 Vendor Selection & Quality Assessment  
* Audit or qualify supplier per Annex 11 §4.5 (22).  
* Review vendor docs, release notes, validation kits (if provided).  
* **Infrastructure Qualification** – ensure servers, OS, DB are qualified (36).  

### 6.4 Design & Configuration  
* Produce / review **FS / DS**; perform **Design Qualification (DQ)** (37–39).  
* Document configuration, interfaces, and integrations.  
* Conduct **Functional Risk Assessment (FRA)** to drive test depth (26, 39).  

### 6.5 Factory Acceptance Test (FAT) (if applicable)  
* Execute FAT at supplier site; log deviations; decide ship/hold (7, 8).  

### 6.6 Site Acceptance Test (SAT) (if applicable)  
* Verify installation environment; run critical function checks; gate to IQ.  

### 6.7 Installation Qualification (IQ)  
* Verify hardware, software, infrastructure; capture evidence (40–43).  
* For upgrades: confirm carry-over of configs & legacy data accessibility.  

### 6.8 Operational Qualification (OQ)  
* Risk-based functional testing: security, audit trail, error handling, interfaces (44–49).  
* Record deviations; retest or justify (50).  
* For upgrades: focus on delta + core regression.  

### 6.9 Performance Qualification (PQ) / User Acceptance  
* End-to-end, real-world scenarios (sample lifecycle, batch, doc workflow) (10).  
* Verify controls (e-signatures, backups), SOP availability, and training (51–54).  
* Include **Data Migration Verification** if applicable (55, 56).  

### 6.10 Data Migration Qualification (MQ) (if applicable)  
* Backup, migrate, verify counts & critical fields, reconcile discrepancies (55–57).  

### 6.11 Release Decision & Documentation  
* Finalise **RTM**; close deviations (57, 58).  
* Prepare **Validation Summary Report (VSR)** with conclusion & QA sign-off (58, 59).  
* Issue formal **Release for Use** communication.  

### 6.12 Post-Implementation Activities  
* **Change Control** for all modifications (13).  
* **Periodic Review** (Annex 11 §11) (60).  
* **Incident Management**; CAPA triggers (61).  
* **Backup / Archiving** incl. test restores (62, 63).  
* **Ongoing Training** and documentation upkeep (64).  

---

## 7  Appendices  

* [Appendix A — RTM template](app-a_rtm.md)  
* [Appendix B — Validation Plan checklist](app-b_vp.md)

![Validation V-model lifecycle](./_images/v-model.png){#fig:vmodel}

Download the RTM workbook: [rtm-template.xlsx](./_files/rtm-template.xlsx)

---

*This SOP assures [Company] introduces or upgrades any computerised system in a controlled, compliant way, satisfying Part 11 and Annex 11 through a documented, risk-based validation lifecycle.*  
