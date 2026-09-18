---
title: "Nexteer Shared Library (Math, Filters, System Time) documents"
description: "Word/PDF/text documents shipped with NxtrLib (Nexteer Shared Library (Math, Filters, System Time)) and their conversion status."
---

# Nexteer Shared Library (Math, Filters, System Time) — documents

*Repository directory: `NxtrLib`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Filter_Library_Design_Document.doc

- **Source:** `NxtrLib/doc/Filter_Library_Design_Document.doc`
- **Format:** `.doc` (~362 KiB)
- **Kind:** Supporting document
- **Status:** summary record — legacy binary source retained at `NxtrLib/doc/Filter_Library_Design_Document.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

Supporting document for `NxtrLib` (supporting document). Consult the binary original for figures, tables and formatted text.

## Interpolation_Design_MDD.doc

- **Source:** `NxtrLib/doc/Interpolation_Design_MDD.doc`
- **Format:** `.doc` (~150 KiB)
- **Kind:** Module design document (MDD)
- **Status:** summary record — legacy binary source retained at `NxtrLib/doc/Interpolation_Design_MDD.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **Interpolation_Design_MDD.doc** module design document specifies the `NxtrLib` software component: requirements, interfaces/ports, internal behaviour, calibration and diagnostics. It is the normative reference for the implementation in `NxtrLib/src/`; the module page lists the files it governs.

## NxtrLib_Systemtime Integration_Manual.docx

- **Source:** `NxtrLib/doc/NxtrLib_Systemtime Integration_Manual.docx`
- **Format:** `.docx` (~25 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (1118 characters in total; showing first 1118). Layout, tables, figures and images are omitted; consult `NxtrLib/doc/NxtrLib_Systemtime Integration_Manual.docx` for those.

```text
Integration Manual – NxtrLib_SystemTime
Contents
1Dependencies1
2Configuration1
2.1Build Time Config1
2.2Generator Config1
2.2.1System1
2.2.2NvMProxyBlock2
3Integration2
4Runnable Scheduling2
5Memory Mapping3
5.1Mapping3
5.2Usage3
6Revision Control Log4
Dependencies
Module
Required Feature
Configuration
Build Time Config
Constant
Notes
SWC
Generator Config
System
Constant
Notes
SWC
Integration
The following import steps must be completed:
Place CBD project structure to appropriate integration folder
Copy SystemTime_Cfg.h.tt into the Header folder and remove the .tt extension.
Configure the constant D_TickRate_Cnt_u32 to the appropriate Os system tick time.
Runnable Scheduling
This section specifies the required runnable scheduling.
Runnable
Scheduling Requirements
Trigger
Memory Mapping
Mapping
Constant
Notes
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.
Usage
Feature
RAM
ROM
Full driver
Table 1: ARM Cortex R4 Memory Usage
Revision Control Log
Item #
Rev #
Change Description
Date
Author Initials
1
Initial version
26Jul13
SAH
```

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `NxtrLib/doc/QAC_Results/interpolation.c.err` (~33 KiB)
- `NxtrLib/doc/QAC_Results/interpolation.c.met` (~478 KiB)

</details>
