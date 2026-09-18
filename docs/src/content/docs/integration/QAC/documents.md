---
title: "QA-C Static Analysis Configuration (MISRA) documents"
description: "Word/PDF/text documents shipped with QAC (QA-C Static Analysis Configuration (MISRA)) and their conversion status."
---

# QA-C Static Analysis Configuration (MISRA) — documents

*Repository directory: `QAC`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## MISRA Compliance Guidelines.docx

- **Source:** `QAC/doc/MISRA Compliance Guidelines.docx`
- **Format:** `.docx` (~535 KiB)
- **Kind:** Coding-guideline document
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `QAC/doc/MISRA Compliance Guidelines.docx` for those.

```text
MISRA Compliance Guidelines
VERSION: 1.0
DATE: 29-Jul-2014
Prepared By:
Nexteer Automotive,
Saginaw, MI, USA
Revision History
Sl. No.
Description
Author
Version
Date
Approved By
1
Initial Version
Spandana Balani
1.0
28-Jul-2014
SPRB
Table of Contents
1.Abbreviations And Acronyms5
2.References6
3.Introduction7
3.1.Purpose7
3.2.Scope7
3.3.Document Conventions and Definitions7
4.MISRA Guidelines8
4.1.Software modules classification8
4.2.MISRA C Compliance and Deviations8
4.3.Suppression Technique8
4.4.Single Line Comment9
4.5.Block Level9
4.6.File Level Comment9
5.ISO 26262 Compliance10
5.1.Coverage of ISO26262 Part 6 Table 1 — Topics to be covered by modelling and coding guidelines10
5.2.Coverage of ISO26262 Part 6 Table 8 -- Design principles for software unit design and implementation10
6.Appendix11
6.1.QAC Project Creation and Analysis for component11
6.2.Guidelines to create component wise QAC project with standard folder structure11
6.3.Manual creation of QAC project11
6.4.QAC Project Creation and Analysis for Integration project17
6.5.Instructions to change QAC personality files18
Abbreviations And Acronyms
Abbreviation
Description
MISRA
Motor Industry Software Reliability Association
ISO
International Standards Organization
References
Sr. No.
Title
Version
1
MISRA-C:2004, Guidelines for the use of the C language in critical systems, ISBN 978-0-9524156-2-6, MIRA, October 2004
2004
2
Software Design and Coding Standards
2014
3
Software Naming Conventions
1.0
4
ISO/IEC 9899:1999(E) – International Standard /Programming languages – C
5
ISO 26262 -6 Road vehicles - Functional safety - Part 6: Product development at the software level
2011-11-15
6
QAC-8.1 Users Guide
2012
Introduction
Purpose
The purpose of this document is to identify Nexteer Automotive’s Electrical Steering Systems software compliance to the MISRA C 2004 standards.
Scope
All production intent software developed by Nexteer Automotive’s Electrical Steering Systems product engineering group [ESG] shall comply with the MISRA C coding Standards and any exceptions should be documented.
As required by MISRA C: 2004 (section 4.4), this document covers the following:
A compliance matrix that demonstrates how each rule is enforced
Analysis to ensure all C code in the product is compliant with the MISRA C rules or deviations documented
List all instances where rules are not being followed, including the deviation process
Configuration and use of QAC version 8.x as the Static Code Analysis tool
Docum
```
*…excerpt ends here (3499 further characters in the source).*
