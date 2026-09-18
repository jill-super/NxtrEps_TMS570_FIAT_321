---
title: "Controller Temperature Monitor documents"
description: "Word/PDF/text documents shipped with CtrlTemp (Controller Temperature Monitor) and their conversion status."
---

# Controller Temperature Monitor — documents

*Repository directory: `CtrlTemp`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Controller_Temperature_MDD.docx

- **Source:** `CtrlTemp/doc/Controller_Temperature_MDD.docx`
- **Format:** `.docx` (~198 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5996 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `CtrlTemp/doc/Controller_Temperature_MDD.docx` for those.

```text
Module -- Controller Temperature
High-Level Description
This module monitors the controller’s temperature sensor output, filters that output, and checks whether the output is within a lower and upper limit.
Figures
Diagram – Function Data Sharing
This diagram shows all data that is shared between functions within the module.
Module Inputs and Outputs
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs (Global Variable Name)
Module Outputs (Global Variable Name)
DiagStsTempRdPrf_Cnt_lgc
FiltMeasTemp_DegC_f32
TemperatureADC_Volt_f32
AmbTemp_DegC_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
(Note: If no module specific variables are used by the design, place the text “None” in the first Variable Name cell in the table)
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
CtrlTemp_CtrlTempSV_M_str
LPF32KSV_Str
see data dictionary
see data dictionary
CTRLTEMP_START_SEC_VAR_CLEARED_UNSPECIFIED
CtrlTemp_CtrlTempSV_M_str .K_Uls_f32
Single Precision Floating Point
see data dictionary
see data dictionary
CtrlTemp_CtrlTempSV_M_str .SV_Uls_f32
Single Precision Floating Point
see data dictionary
see data dictionary
CtrlTemp_CtrlTemp_DegC_M_f32
Single Precision Floating Point
see data dictionary
see data dictionary
CTRLTEMP_START_SEC_VAR_CLEARED_32
CtrlTemp_CtrlTempErrorAcc_Cnt_M_u16
1
see data dictionary
see data dictionary
CTRLTEMP_START_SEC_VAR_CLEARED_16
CtrlTemp_CtrlTempFiltOut_DegC_D_f32
Single Precision Floating Point
see data dictionary
see data dictionary
CTRLTEMP_START_SEC_VAR_CLEARED_32
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Variable Name
Typedef Name
Storage Type
Safety Critical Classification
None
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
(Note: If no calibrations are used by the design, place the text “None” in the first location in the table)
Constant Name
k_TempSnsrFiltDf
```
*…excerpt ends here (3496 further characters in the source).*

## CtrlTemp_Integration_Manual.docx

- **Source:** `CtrlTemp/doc/CtrlTemp_Integration_Manual.docx`
- **Format:** `.docx` (~38 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2745 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `CtrlTemp/doc/CtrlTemp_Integration_Manual.docx` for those.

```text
Integration Manual – Controller Temperature (CtrlTemp)
Table of Contents
1Dependencies2
1.1SWCs2
1.2Functions to be provided to Integration Project2
2Configuration3
2.1Build Time Config3
2.2Configuration Files to be provided by Integration Project3
2.2.1Da Vinci Config generation3
2.2.2Manual Configuration Changes3
3Integration4
3.1Required Global Data Inputs4
3.2Optional Global Data Inputs4
3.3Specific Include Path present4
4Runnable Scheduling5
5Memory Mapping6
5.1Mapping6
5.2Usage6
5.3NvM Blocks6
6Compiler Settings6
6.1Preprocessor MACRO6
6.2Optimization Settings6
7Revision Control Log7
Dependencies
SWCs
Module
Required Feature
None
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
None
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Sa_CtrlTemp_Cfg.h generated by Sa_CtrlTemp_Cfg.h.tt
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
CtrlTempGeneral/CtrlTempCPEnable
To enable checkpoints
CtrlTemp
DaVinci Interrupt Configuration Changes
ISR Name
VIM #
Priority Dependency
Notes
None
Manual Configuration Changes
Constant
Notes
SWC
None
Integration
Required Global Data Inputs
TemperatureADC_Volt_f32
DiagStsTempRdPrf_Cnt_lgc
AmbTemp_DegC_f32
Required Global Data Outputs
FiltMeasTemp_DegC_f32
Specific Include Path present
No
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
CtrlTemp_Init1
Called from RTE before any call to the periodic functions
RTE init
Runnable
Scheduling Requirements
Trigger
CtrlTemp_Per1
None
RTE 2ms
CtrlTemp_Per2
None
RTE 100ms
.
Memory Mapping
Mapping
Memory Section
Contents
Notes
CTRLTEMP_START_SEC_VAR_CLEARED_32
CTRLTEMP_START_SEC_VAR_CLEARED_16
CTRLTEMP_START_SEC_VAR_CLEARED_UNSPECIFIED
RTE_START_SEC_SA_CTRLTEMP_APPL_CODE
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.
Usage
Feature
RAM
ROM
<Memmap usuage info>
Table 1: ARM Cortex R4 Memory Usage
Non RTE NvM Blocks
Block Name
<NVM block used Non RTE functions >
Note : Size of the NVM block if configured in developer
RTE NvM Blocks
Block Name
<NVM block used in RTE functions >
Note : Size of the NVM block if configured in developer
Compiler Settings
Preprocessor MACRO
<Define all
```
*…excerpt ends here (245 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `CtrlTemp/doc/QAC_Results/Sa_CtrlTemp.c.err` (~105 KiB)
- `CtrlTemp/doc/QAC_Results/Sa_CtrlTemp.c.met` (~809 KiB)

</details>
