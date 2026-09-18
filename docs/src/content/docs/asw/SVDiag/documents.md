---
title: "Sine-Voltage Drive Diagnostics documents"
description: "Word/PDF/text documents shipped with SVDiag (Sine-Voltage Drive Diagnostics) and their conversion status."
---

# Sine-Voltage Drive Diagnostics — documents

*Repository directory: `SVDiag`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## DigPhsReasDiag_MDD.docx

- **Source:** `SVDiag/doc/DigPhsReasDiag_MDD.docx`
- **Format:** `.docx` (~1264 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5996 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `SVDiag/doc/DigPhsReasDiag_MDD.docx` for those.

```text
Module -- Digital Phase Reasonableness Diagnostic
High-Level Description
This module compares the commanded duty cycle to each phase with the feedback from the NHET module. The values are compared, compensated with a previously defined fixed value, filtered, and compared against a valid threshold.
Figures
Component Diagram
Diagram – Function Data Sharing
No Shared Data.
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
ExpectedOnTimeA_Cnt_u32
ExpectedOnTimeB_Cnt_u32
ExpectedOnTimeC_Cnt_u32
MeasuredOnTimeA_Cnt_u32
MeasuredOnTimeB_Cnt_u32
MeasuredOnTimeC_Cnt_u32
LRPRCorrectedMtrPosCaptured_rev_u0p16
LRPRPhaseadvanceCaptured_Cnt_s16
LRPRModulationIndexCaptured_Uls_f32
MotorVelMRFUnfiltered_MtrRadpS_f32
ElecMechPolarity_Cnt_s08
PDActivateTest_Cnt_lgc
GateDriveResetActive_Cnt_lgc
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
SVDiag_FilterSV_Cnt_M_s18p13[3]
2-13
-210000
210000
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_32
SVDiag_PrevLRPRHighSector_Cnt_M_lgc
N/A
FALSE
TRUE
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_BOOLEAN
SVDiag_LRPRHighSector_Cnt_M_lgc
N/A
FALSE
TRUE
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_BOOLEAN
SVDiag_PrevLRPRLowSector_Cnt_M_lgc
N/A
FALSE
TRUE
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_BOOLEAN
SVDiag_LRPRLowSector_Cnt_M_lgc
N/A
FALSE
TRUE
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_BOOLEAN
SVDiag_LRPRAdjModldAComp_Cnt_M_f32
Single precision float
0
1
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_FLOAT32
SVDiag_PrevLRPRAdjModldComp_Cnt_M_f32
Single precision float
0
1
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_32
SVDiag_PrevLRPRPhsAdvComp_Cnt_M_u16
1
0
6144
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_16
SVDiag_LRPRPhsAdvComp_Cnt_M_u16
1
0
6144
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_16
SVDiag_PhaseOffset_Rev_M_u0p16
2-16
0
1
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_16
SVDiag_LowPhReasErrorAcc_Cnt_M_u16
1
0
1000
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_16
SVDiag_HighResPhsReasDisable_M_u8
1
0
100
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_8
SVDiag_LowResPhsReasDisable_M_u8
1
0
100
DIGPHSREASDIAG_START_SEC_VAR_CLEARED_8
SVDiag_MaxNrCommOffVltg_Cnt_M_f32
Single precision float
0
86400
```
*…excerpt ends here (3496 further characters in the source).*

## Motor_Driver_Diagnostics_MDD.docx

- **Source:** `SVDiag/doc/Motor_Driver_Diagnostics_MDD.docx`
- **Format:** `.docx` (~987 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5987 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `SVDiag/doc/Motor_Driver_Diagnostics_MDD.docx` for those.

```text
Module -- Motor Driver Diagnostics
High-Level Description
This function operates as a reporting mechanism for all Gate Drive faults.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
FETFaultPhase_Cnt_enum
MtrDrvrInitStart_Cnt_lgc
FETFaultType_Cnt_enum
MtrDrvrInitComplete_Cnt_lgc
GateDriveResetActive_Cnt_lgc
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
SVDiag_MtrDrvInitStartTime_mS_M_u32p0
uint32
FULL
FULL
MTRDRVDIAG_START_SEC_VAR_CLEARED_32
SVDiag_ResetWaitLoop_Cnt_M_lgc
boolean
FALSE
TRUE
MTRDRVDIAG_START_SEC_VAR_CLEARED_BOOLEAN
SVDiag_GateDrvFltSts_Cnt_D_b16
uint16
FULL
FULL
MTRDRVDIAG_START_SEC_VAR_CLEARED_16
SVDiag_MtrDrvInitActive_Cnt_M_lgc
boolean
FALSE
TRUE
MTRDRVDIAG_START_SEC_VAR_CLEARED_BOOLEAN
SVDiag_FETFaultType_Cnt_M_enum
FETFAULTTYPE_ENUM
NOFAULT , LOWER , UPPER
MTRDRVDIAG_START_SEC_VAR_CLEARED_UNSPECIFIED
SVDiag_FETFaultPhase_Cnt_M_enum
FETPHASETYPE_ENUM
NOPHASE, PHASEA , PHASEB , PHASEC
MTRDRVDIAG_START_SEC_VAR_CLEARED_UNSPECIFIED
SVDiag_GateDriveFltAcc_Cnt_M_u16
uint16
FULL
FULL
MTRDRVDIAG_START_SEC_VAR_CLEARED_16
SVDiag_GenGateDriveFltAcc_Cnt_M_u16
uint16
0
200
MTRDRVDIAG_START_SEC_VAR_CLEARED_16
SVDiag_MtrDrvInitComp_Cnt_M_lgc
boolean
FALSE
TRUE
MTRDRVDIAG_START_SEC_VAR_CLEARED_BOOLEAN
SVDiag_OnStateFltAcc_Cnt_M_u16
uint16
FULL
FULL
MTRDRVDIAG_START_SEC_VAR_CLEARED_16
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
<None>
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
k_GateDriveDiag_Cnt_str
k_OnStateDiag_Cnt_str
Program(fixed) Constants
Embedded Constants
Local
Constant Name
Resolution
Units
Value
D_PHASEALOWER_CNT_U16
uint16
Counts
0U
D_PHASEBLOWER_CNT_U16
uint16
Counts
1U
D_PHASECLOWER_CNT_U16
uint16
Counts
2U
D_PHASEAUPPER_CNT_U16
uint16
Counts
3U
D_PHASEBUPPER_CNT_U16
uint16
Counts
```
*…excerpt ends here (3487 further characters in the source).*

## SVDiag_Integration_Manual.docx

- **Source:** `SVDiag/doc/SVDiag_Integration_Manual.docx`
- **Format:** `.docx` (~78 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (4543 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `SVDiag/doc/SVDiag_Integration_Manual.docx` for those.

```text
Integration Manual
For
Sine Voltage Generation Diagnostics (ES-49)
VERSION: 2
DATE: 02-12-2014
Prepared By:
Rijvi Ahmed,
Nexteer Automotive,
Saginaw, MI, USA
Location: The official version of this document is stored in the Nexteer Configuration Management System.
Revision History
Sl. No.
Description
Author
Version
Date
1
Initial version
VT
1
03-Oct-2013
2
Updated for FDD rev.008 and updated the template.
Rijvi
2
01-Dec-2014
Table of Contents
1Abbrevations And Acronyms4
2References5
3Dependencies6
3.1SWCs6
3.2Global Functions(Non RTE) to be provided to Integration Project6
4Configuration REQUIREMeNTS7
4.1Build Time Config7
4.2Configuration Files to be provided by Integration Project7
4.3Da Vinci Parameter Configuration Changes7
4.4DaVinci Interrupt Configuration Changes7
4.5Manual Configuration Changes7
5Integration DATAFLOW REQUIREMENTS8
5.1Required Global Data Inputs8
5.2Required Global Data Outputs8
5.3Specific Include Path present8
6Runnable Scheduling9
7Memory Map REQUIREMENTS10
7.1Mapping10
7.2Usage10
7.3Non RTE NvM Blocks10
7.4RTE NvM Blocks10
8Compiler Settings11
8.1Preprocessor MACRO11
8.2Optimization Settings11
9Appendix12
Abbrevations And Acronyms
Abbreviation
Description
DFD
Design functional diagram
MDD
Module design Document
References
This section lists the title & version of all the documents that are referred for development of this document
Sr. No.
Title
Version
1
FDD ES-49. Sine Voltage Generation Diagnostics - EA3.x
008
Dependencies
SWCs
Module
Required Feature
None
None
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
Global function (except the ones that are defined in RTE modules) that is defined in this component but used by other function
Configuration REQUIREMeNTS
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
None
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
None
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
Integration DATAFLOW REQUIREMENTS
Required Global Data Inputs
ExpectedOnTimeA_Cnt_u32
ExpectedOnTimeB_Cnt_u32
ExpectedOnTimeC_Cnt_u32
LRPRCorrectedMtrPosCaptured_Rev_f32
LRPRModulationIndexCaptured_Uls_f32
LRPRPhaseadvanceCaptured_Cnt_s16
MeasuredOnTimeA_Cnt_u32
MeasuredOnT
```
*…excerpt ends here (2043 further characters in the source).*

## Static-analysis outputs (4 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `SVDiag/doc/QAC_Results/Ap_DigPhsReasDiag.c.err` (~108 KiB)
- `SVDiag/doc/QAC_Results/Ap_DigPhsReasDiag.c.met` (~926 KiB)
- `SVDiag/doc/QAC_Results/Sa_MtrDrvDiag.c.err` (~103 KiB)
- `SVDiag/doc/QAC_Results/Sa_MtrDrvDiag.c.met` (~906 KiB)

</details>
