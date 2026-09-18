---
title: "Assist Sum and Limit (Current Mode) documents"
description: "Word/PDF/text documents shipped with AstLmt_CM (Assist Sum and Limit (Current Mode)) and their conversion status."
---

# Assist Sum and Limit (Current Mode) — documents

*Repository directory: `AstLmt_CM`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Assist_Sum_Limit_CurrentMode_MDD.docx

- **Source:** `AstLmt_CM/doc/Assist_Sum_Limit_CurrentMode_MDD.docx`
- **Format:** `.docx` (~462 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5994 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `AstLmt_CM/doc/Assist_Sum_Limit_CurrentMode_MDD.docx` for those.

```text
Module – Assist Sum and Limit (Current Mode)
High-Level Description
This module combines and limits the various assist command signals from EPS modules. It puts out several torque commands from different points in the summation and limiting process.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
AssistCmd_MtrNm_f32
LimitPercentFiltered_Uls_f32
AssistEOTDamping_MtrNm_f32
AssistEOTGain_Uls_f32
AssistEOTLimit_MtrNm_f32
PreLimitForStall_MtrNm_f32
PreLimitTorque_MtrNm_f32
AssistStallLimit_MtrNm_f32
SumLimTrqCmd_MtrNm_T_f32
AssistVehSpdLimit_MtrNm_f32
TrqLimitMin_MtrNm_f32
CombinedDamping_MtrNm_f32
DefeatLimitService_Cnt_lgc
LimitedReturn_MtrNm_f32
LrnPnCtrCCDisable_Cnt_lgc
LrnPnCtrEnable_Cnt_lgc
LrnPnCtrTCmd_MtrNm_f32
OpTrqOvr_MtrNm_f32
OutputRampMult_Uls_f32
PosServCCDisable_Cnt_lgc
PowerLimitPerc_Uls_f32
PrkAssistCmd_MtrNm_f32
PullCompCmd_MtrNm_f32
ThermalLimitPerc_Uls_f32
ThermalLimit_MtrNm_f32
VehSpd_Kph_f32
WheelImbalanceCmd_MtrNm_f32
TSMitCommand_MtrNm_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
AstLmt_ManualTrqCmd_MtrNm_M_f32
Single Precision Float
-16
15.9995
ASTLMT_START_SEC_VAR_CLEARED_32
AstLmt_ManualTrqCmdEn_Cnt_M_lgc
n/a
FALSE
TRUE
ASTLMT_START_SEC_VAR_CLEARED_BOOLEAN
AstLmt_SteeringAsstDefeat_Cnt_M_lgc
n/a
FALSE
TRUE
ASTLMT_START_SEC_VAR_CLEARED_BOOLEAN
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
None
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
k_SumLimPlCmpLimit_MtrNm_f32
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
None
Global
This section lists the global constants
```
*…excerpt ends here (3494 further characters in the source).*

## AstLmt_CM_IntegrationManual.docx

- **Source:** `AstLmt_CM/doc/AstLmt_CM_IntegrationManual.docx`
- **Format:** `.docx` (~42 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (3341 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `AstLmt_CM/doc/AstLmt_CM_IntegrationManual.docx` for those.

```text
Integration Manual –AstLmt
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
Ap_AstLmt_Cfg.h generated by Ap_AstLmt_Cfg.h.tt
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
AstLmtGeneral/AstLmtCPEnable
To enable checkpoints
AstLmt
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
AssistCmd_MtrNm_f32
AssistEOTDamping_MtrNm_f32
AssistEOTGain_Uls_f32
AssistEOTLimit_MtrNm_f32
AssistStallLimit_MtrNm_f32
AssistVehSpdLimit_MtrNm_f32
CombinedDamping_MtrNm_f32
DefeatLimitService_Cnt_lgc
LimitedReturn_MtrNm_f32
LrnPnCtrCCDisable_Cnt_lgc
LrnPnCtrEnable_Cnt_lgc
LrnPnCtrTCmd_MtrNm_f32
OpTrqOvr_MtrNm_f32
OutputRampMult_Uls_f32
PosServCCDisable_Cnt_lgc
PowerLimitPerc_Uls_f32
PrkAssistCmd_MtrNm_f32
PullCompCmd_MtrNm_f32
TSMitCommand_MtrNm_f32
ThermalLimitPerc_Uls_f32
ThermalLimit_MtrNm_f32
VehSpd_Kph_f32
WheelImbalanceCmd_MtrNm_f32
Required Global Data Outputs
LimitPercentFiltered_Uls_f32
PreLimitForStall_MtrNm_f32
PreLimitTorque_MtrNm_f32
SumLimTrqCmd_MtrNm_f32
TrqLimitMin_MtrNm_f32
Used for TrqReasonable dianostics
Specific Include Path present
No
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
AstLmt_Init1
Called from RTE before any call to the periodic functions
RTE init
Runnable
Scheduling Requirements
Trigger
AstLmt_Per1
None
RTE 2ms
AstLmt_Scom_ManualTrqCmd
None
Server inv
```
*…excerpt ends here (841 further characters in the source).*

## index_WithOutPS.pdf

- **Source:** `AstLmt_CM/utp/Tessy/report/index_WithOutPS.pdf`
- **Format:** `.pdf` (~1196 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `AstLmt_CM/utp/Tessy/report/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-05, 17:35:09+0530
Project AstLmt_CM
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 5
Successful: 5
Failed: 0
Not Executed: 0
Date: 2014-09-05
Time: 17:35:09+0530
Selected Project Items
Test Object "CBD_UnitTest/AstLmt/AstLmt_Init"
Test Object "CBD_UnitTest/AstLmt/AstLmt_Per1"
Test Object "CBD_UnitTest/AstLmt/AstLmt_Scom_GetSteeringAssistDefeat"
Test Object "CBD_UnitTest/AstLmt/AstLmt_Scom_ManualTrqCmd"
Test Object "CBD_UnitTest/AstLmt/AstLmt_Scom_SetSteeringAssistDefeat"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Dr
```
*…excerpt ends here (5300 further characters in the source).*

## index_WithPS.pdf

- **Source:** `AstLmt_CM/utp/Tessy/report/index_WithPS.pdf`
- **Format:** `.pdf` (~1197 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `AstLmt_CM/utp/Tessy/report/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-05, 18:13:34+0530
Project AstLmt_CM
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 5
Successful: 5
Failed: 0
Not Executed: 0
Date: 2014-09-05
Time: 18:13:34+0530
Selected Project Items
Test Object "CBD_UnitTest/AstLmt/AstLmt_Init"
Test Object "CBD_UnitTest/AstLmt/AstLmt_Per1"
Test Object "CBD_UnitTest/AstLmt/AstLmt_Scom_GetSteeringAssistDefeat"
Test Object "CBD_UnitTest/AstLmt/AstLmt_Scom_ManualTrqCmd"
Test Object "CBD_UnitTest/AstLmt/AstLmt_Scom_SetSteeringAssistDefeat"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Dr
```
*…excerpt ends here (5300 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `AstLmt_CM/doc/QAC_Results/Ap_AstLmt.c.err` (~92 KiB)
- `AstLmt_CM/doc/QAC_Results/Ap_AstLmt.c.met` (~196 KiB)

</details>
