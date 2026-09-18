---
title: "Hardware Power-Up Sequence documents"
description: "Word/PDF/text documents shipped with HwPwUp (Hardware Power-Up Sequence) and their conversion status."
---

# Hardware Power-Up Sequence — documents

*Repository directory: `HwPwUp`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Hardware_Power_Up_MDD.docx

- **Source:** `HwPwUp/doc/Hardware_Power_Up_MDD.docx`
- **Format:** `.docx` (~212 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5995 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `HwPwUp/doc/Hardware_Power_Up_MDD.docx` for those.

```text
Module – Hardware Power Up Sequence
High-Level Description
This module controls the startup initialization sequence for several modules that would otherwise conflict with one another. It uses a series of boolean inputs and outputs to control these modules.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
PwrDiscATestComplete_Cnt_lgc
PwrDiscATestStart_Cnt_lgc
TMFTestComplete_Cnt_lgc
TMFTestStart_Cnt_lgc
PwrDiscBTestComplete_Cnt_lgc
PwrDiscBTestStart_Cnt_lgc
MtrDrvrInitComplete_Cnt_lgc
MtrDrvrInitStart_Cnt_lgc
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
HwPwUp_PowerUpState_Cnt_M_enum
1
0
6
HWPWUP_START_SEC_VAR_CLEARED_UNSPECIFIED
HwPwUp_PwrDiscATestStart_Cnt_M_lgc
boolean
FALSE
TRUE
HWPWUP_START_SEC_VAR_CLEARED_UNSPECIFIED
HwPwUp_TMFTestStart_Cnt_M_lgc
boolean
FALSE
TRUE
HWPWUP_START_SEC_VAR_CLEARED_UNSPECIFIED
HwPwUp_PwrDiscBTestStart_Cnt_M_lgc
boolean
FALSE
TRUE
HWPWUP_START_SEC_VAR_CLEARED_UNSPECIFIED
HwPwUp_MtrDrvrInitStart_Cnt_M_lgc
boolean
FALSE
TRUE
HWPWUP_START_SEC_VAR_CLEARED_UNSPECIFIED
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
PowerUpSequenceType
PWRUP_PWRDISCSTEPA = 0
PWRUP_TMFINIT = 1
PWRUP_PWRDISCSTEPB = 2
PWRUP_MTRDRIVERINIT = 3
PWRUP_WARMINITCOMPLETE = 4
PWRUP_RUN = 5
PWRUP_DISABLE = 6
uint8
0
6
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
none
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
D_PWRDISCSTEPAMASK_CNT_U16
1
Counts
0x0001
D_PWRDISCSTEPBMASK_CNT_U16
1
Counts
0x0004
D_PGMSPECMASK_CNT_U16
1
Counts
configurable
Global
This section lists the global constants used b
```
*…excerpt ends here (3495 further characters in the source).*

## HwPwUp_Integration_Manual.docx

- **Source:** `HwPwUp/doc/HwPwUp_Integration_Manual.docx`
- **Format:** `.docx` (~38 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2448 characters in total; showing first 2448). Layout, tables, figures and images are omitted; consult `HwPwUp/doc/HwPwUp_Integration_Manual.docx` for those.

```text
Integration Manual HwPwUp
Table of Contents
1Dependencies2
1.1SWCs2
1.2Global Functions(Non RTE) to be provided to Integration Project2
2Configuration3
2.1Build Time Config3
2.2Configuration Files to be provided by Integration Project3
2.2.1Da Vinci Parameter Configuration Changes3
2.2.2DaVinci Interrupt Configuration Changes3
2.2.3Manual Configuration Changes3
3Integration4
3.1Required Global Data Inputs4
3.2Required Global Data Outputs4
3.3Specific Include Path present4
4Runnable Scheduling5
5Memory Mapping6
5.1Mapping6
5.2Usage6
5.3Non RTE NvM Blocks6
5.4RTE NvM Blocks6
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
Ap_ HwPwUp _Cfg.h generated by Ap_HwPwUp_Cfg.h.tt
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
HwPwUpGeneral/HwPwUpCPEnable
To enable checkpoints
HwPwUp
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
None
Required Global Data Outputs
None
Specific Include Path present
No
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
None
Runnable
Scheduling Requirements
Trigger
HwPwUp_Per1
It should run before torque oscillation calculation
RTE 2ms
.
Memory Mapping
Mapping
Memory Section
Contents
Notes
HWPWUP_START_SEC_VAR_CLEARED_BOOLEAN
HWPWUP_START_SEC_VAR_CLEARED_UNSPECIFIED
RTE_START_SEC_AP_ HWPWUP _APPL_CODE
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.
Usage
Feature
RAM
ROM
<Memmap usuage info>
Table 1: ARM Cortex R4 Memory Usage
Non RTE NvM Blocks
Block Name
None
Note : Size of the NVM block if configured in developer
RTE NvM Blocks
Block Name
None
Note : Size of the NVM block if configured in developer
Compiler Settings
Preprocessor MACRO
None
Optimization Settings
None
Revision Control Log
Rev #
Change Description
Date
Author
1
Initial version
17-June-14
nzt9hv
```

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `HwPwUp/doc/QAC_Results/Ap_HwPwUp.c.err` (~6 KiB)
- `HwPwUp/doc/QAC_Results/Ap_HwPwUp.c.met` (~70 KiB)

</details>
