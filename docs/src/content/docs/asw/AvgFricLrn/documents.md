---
title: "Average Friction Learning documents"
description: "Word/PDF/text documents shipped with AvgFricLrn (Average Friction Learning) and their conversion status."
---

# Average Friction Learning — documents

*Repository directory: `AvgFricLrn`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Average_Friction_Learning_MDD.docx

- **Source:** `AvgFricLrn/doc/Average_Friction_Learning_MDD.docx`
- **Format:** `.docx` (~1833 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5995 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `AvgFricLrn/doc/Average_Friction_Learning_MDD.docx` for those.

```text
Module – Average Friction Learning
High-Level Description
This module estimates the gear friction changes from the baseline friction and provides compensation. It is based on the column torque and handwheel angle. It is primarily active at higher speeds.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
HwAng_HwDeg_f32
EstFric_HwNm_f32
HwPosAuthority_Uls_f32
FricOffset_HwNm_f32
HwTrq_HwNm_f32
SatEstFric_HwNm_f32
HwVel_HwRadpS_f32
LatAcc_g_f32
CRFMtrTrq_MtrNm_f32
Temperature_DegC_f32
VehicleSpeedValid_Cnt_lgc
VehSpd_Kph_f32
DefeatFricLearning_Cnt_lgc
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
AvgFricLrn_FiltAvgFric_HwNm_M_f32[4]
See Data Dictionary
See Data Dictionary
See Data Dictionary
AVGFRICLRN_START_SEC_VAR_CLEARED_32
AvgFricLrn_SatAvgFric_HwNm_M_f32[4]
See Data Dictionary
See Data Dictionary
See Data Dictionary
AVGFRICLRN_START_SEC_VAR_CLEARED_32
AvgFricLrn_VehBaselineFric_HwNm_M_f32[4]
See Data Dictionary
See Data Dictionary
See Data Dictionary
AVGFRICLRN_START_SEC_VAR_CLEARED_32
AvgFricLrn_HwAngBuf_HwDeg_M_f32[12]
See Data Dictionary
See Data Dictionary
See Data Dictionary
AVGFRICLRN_START_SEC_VAR_CLEARED_32
AvgFricLrn_HwVelBuf_HwDegpS_M_f32[12]
See Data Dictionary
See Data Dictionary
See Data Dictionary
AVGFRICLRN_START_SEC_VAR_CLEARED_32
AvgFricLrn_ColTrqBuf_HwNm_M_f32[6]
See Data Dictionary
See Data Dictionary
See Data Dictionary
AVGFRICLRN_START_SEC_VAR_CLEARED_32
AvgFricLrn_LearnConstTimer_mS_M_u32
See Data Dictionary
See Data Dictionary
See Data Dictionary
AVGFRICLRN_START_SEC_VAR_CLEARED_32
AvgFricLrn_HwVelKSV_M_str
See Data Dictionary
See Data Dictionary
See Data Dictionary
AVGFRICLRN_START_SEC_VAR_CLEARED_UNSPECIFIED
AvgFricLrn_LatAccKSV_M_str
See Data Dictionary
See Data Dictionary
See Data Dictionary
AVGFRICLRN_START_SEC_VAR_CLEARED_UNSPECIFIED
AvgFricLrn_HwPosAuthorityKSV_M_str
See Data Dictionary
See Data Dictionary
See Data Dictionary
AVGFRICLRN_START_SEC_VAR_CLEARED_UNSPECIFIED
AvgFricLrn_VehSpdKSV_M_str
See Data Dictionary
See Data Dictionary
See Data Dictionary
AVGFRICLRN_START
```
*…excerpt ends here (3495 further characters in the source).*

## AvgFricLrn_Integration_Manual.docx

- **Source:** `AvgFricLrn/doc/AvgFricLrn_Integration_Manual.docx`
- **Format:** `.docx` (~40 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (4095 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `AvgFricLrn/doc/AvgFricLrn_Integration_Manual.docx` for those.

```text
Integration Manual –AvgFricLrn
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
<Name of SWC>
<Addition of global data, function*.
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
< None>
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Ap_AvgFricLrn_Cfg.h for checkpoint enable
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
<None>
DaVinci Interrupt Configuration Changes
ISR Name
VIM #
Priority Dependency
Notes
<None>
Manual Configuration Changes
Constant
Notes
SWC
<None>
Integration
Required Global Data Inputs
CRFMtrTrq_MtrNm_f32
DefeatFricLearning_Cnt_lgc
HwAng_HwDeg_f32
HwPosAuthority_Uls_f32
HwTrq_HwNm_f32
HwVel_HwRadpS_f32
LatAcc_g_f32
Temperature_DegC_f32
VehSpd_Kph_f32
VehicleSpeedValid_Cnt_lgc
Required Global Data Outputs
EstFric_HwNm_f32
FricOffset_HwNm_f32
SatEstFric_HwNm_f32
Specific Include Path present
No
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
AvgFricLrn_Init1()
None
Init
Runnable
Scheduling Requirements
Trigger
AvgFricLrn_Per1
triggered on TimingEvent
10ms
AvgFricLrn_SCom_GetEOLFric
triggered by server invocation for OperationPrototype <GetEOLFric> of PortPrototype <AvgFricLrn_SCom>
AvgFricLrn_SCom_GetOffsetOutputDefeat
triggered by server invocation for OperationPrototype <GetOffsetOutputDefeat> of PortPrototype <AvgFricLrn_SCom>
AvgFricLrn_SCom_GetSelect
triggered by server invocation for OperationPrototype <GetSelect> of PortPrototype <AvgFricLrn_SCom>
AvgFricLrn_SCom_InitLearnedTables
triggered by server invocation for OperationPrototype <InitLearnedTables> of PortProt
```
*…excerpt ends here (1595 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `AvgFricLrn/doc/QAC_Results/Ap_AvgFricLrn.c.err` (~105 KiB)
- `AvgFricLrn/doc/QAC_Results/Ap_AvgFricLrn.c.met` (~990 KiB)

</details>
