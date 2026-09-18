---
title: "Hysteresis Compensation documents"
description: "Word/PDF/text documents shipped with HystComp (Hysteresis Compensation) and their conversion status."
---

# Hysteresis Compensation — documents

*Repository directory: `HystComp`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## HystComp_Integration_Manual.docx

- **Source:** `HystComp/doc/HystComp_Integration_Manual.docx`
- **Format:** `.docx` (~27 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2515 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `HystComp/doc/HystComp_Integration_Manual.docx` for those.

```text
Integration Manual -- HystComp
Contents
1Dependencies1
2Configuration1
2.1Build Time Config1
2.2Generator Config1
3Runnable Scheduling5
4Memory Mapping6
4.1Mapping6
4.2Usage6
Dependencies
Module
Required Feature
Rte
Port and runnable mapping.
WdgM
CheckpointReached() API
Configuration
Build Time Config
Constant
Notes
SWC
None
Generator Config
The HystComp module parameter description file and generator templates are located in the “generate” folder. The generation scheme at this time relies on the ARTT generation framework developed by BMW. Following are the recommended steps to integrate the provided generation templates and parameter description with Davinci Configurator:
Copy the “Artt/artt” framework folder into the “Generators” directory (if not already present)
Execute the “Integrate.bat” script from the Tools directory of this component to perform the necessary integration steps:
The script creates the required directories in the integration project, “Generators/Artt/HystComp” and “Generators/Components/_Schemes/HystComp/bswmd”
The script then copies the required files from the CBD generate directory into the new directories.
If this is the first time integration, then perform the Davinci Configurator 3rd party component integration procedure.
Constant
Notes
SWC
HystCompGeneral
General module configuration. See HystComp technical reference for details.
HystComp
Rte Config
The SWC description included with this component in the “autosar” folder describes only the static portion of the SWC. A partial SWC description describing the configurable part of the component interface is generated into the Ap_HystComp _Cfg.arxml file. This description must be imported into the Rte configuration tool (Developer) using the “Merge Object” option to merge the static SWC description with the generated partial SWC description file.
Runnable Scheduling
This section specifies the required runnable scheduling.
Runnable
Scheduling Requirements
Privileged Mode
Trigger
HystComp_Per1()
Scheduled per integration project requirements
Not Required
2ms
Memory Mapping
Mapping
Constant
Notes
HYSTCOMP_START_SEC_VAR_CLEARED_UNSPECIFIED
HYSTCOMP_START_SEC_VAR_CLEARED_32
HYSTCOMP_START_SEC_VAR_CLEARED_16
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.
Usage
Feature
RAM
ROM
Full SWC
Table 1: ARM Cortex R4 Memory UsageRevision Control Log
Item #
Rev #
Change Description
Date
Author Initials
1
1
Initial version
```
*…excerpt ends here (15 further characters in the source).*

## Hysteresis_Compensation_MDD.doc

- **Source:** `HystComp/doc/Hysteresis_Compensation_MDD.doc`
- **Format:** `.doc` (~2043 KiB)
- **Kind:** Module design document (MDD)
- **Status:** summary record — legacy binary source retained at `HystComp/doc/Hysteresis_Compensation_MDD.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **Hysteresis_Compensation_MDD.doc** module design document specifies the `HystComp` software component: requirements, interfaces/ports, internal behaviour, calibration and diagnostics. It is the normative reference for the implementation in `HystComp/src/`; the module page lists the files it governs.

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `HystComp/doc/QAC_Results/Ap_HystComp.c.err` (~107 KiB)
- `HystComp/doc/QAC_Results/Ap_HystComp.c.met` (~677 KiB)

</details>
