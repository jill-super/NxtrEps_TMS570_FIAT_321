---
title: "End-of-Travel Position Learning documents"
description: "Word/PDF/text documents shipped with LrnEOT (End-of-Travel Position Learning) and their conversion status."
---

# End-of-Travel Position Learning — documents

*Repository directory: `LrnEOT`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## LearnEOT.docx

- **Source:** `LrnEOT/doc/LearnEOT.docx`
- **Format:** `.docx` (~426 KiB)
- **Kind:** Supporting document
- **Status:** converted — text extracted from the binary (5996 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `LrnEOT/doc/LearnEOT.docx` for those.

```text
Module -- LrnEOT
High-Level Description
LrnEOT uses vehicle operational information to learn the appropriate end of travel positions for a given system.
Figures
Component Diagram
Module Inputs and Outputs
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs (Global Variable Name)
Module Outputs (Global Variable Name)
MtrVelCRF_MtrRadpS_f32
CWPosition_HwDeg_f32
HandwheelPosition_HwDeg_f32
CCWPosition_HwDeg_f32
HandwheelAuthority_Uls_f32
CWFound_Cnt_lgc
HwTorque_HwNm_f32
CCWFound_Cnt_lgc
DiagStsHwPosDis_Cnt_lgc
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
LrnEOT_CcwEOTTimer_mS_M_u32
1
0
Full
LRNEOT_START_SEC_VAR_32
LrnEOT_CwEOTTimer_mS_M_u32
1
0
Full
LRNEOT_START_SEC_VAR_32
LrnEOT_ResetLimitReq_Cnt_M_lgc
N/A
N/A
N/A
LRNEOT_START_SEC_VAR_ BOOLEAN
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
Storage Type
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
k_MinRackTrvl_HwDeg_f32
k_MaxRackTrvl_HwDeg_f32
k_AuthorityStartLrn_Uls_f32
k_HwTrqEOTLrn_HwNm_f32
k_MtrVelEOTLrn_MtrRadpS_f32
k_EOTLrnTimer_mS_u16
k_MtrTrqEOTLrn_MtrNm_f32
k_MinResetAuthority_Uls_f32
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Value
D_CCWEOTPOSITIONLOLIM_HWDEG_F32
Single precision Float
(-1440.11)
D_CCWEOTPOSITIONHILIM_HWDEG_F32
Single precision Float
(-360.0)
D_CWEOTPOSITIONLOLIM_HWDEG_F32
Single precision Float
360.0
D_CWEOTPOSITIONHILIM_HWDEG_F32
Single precision Float
1440.11
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
D_ZERO_ULS_F32
D_FALSE_CNT_LGC
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
Non
```
*…excerpt ends here (3496 further characters in the source).*

## LrnEOT_Integration_Manual.docx

- **Source:** `LrnEOT/doc/LrnEOT_Integration_Manual.docx`
- **Format:** `.docx` (~38 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2888 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `LrnEOT/doc/LrnEOT_Integration_Manual.docx` for those.

```text
Integration Manual –LrnEOT
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
Ap_LrnEOT_Cfg.h for checkpoint enable
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
DiagStsHwPosDis_Cnt_lgc
HandwheelAuthority_Uls_f32
HandwheelPosition_HwDeg_f32
HwTorque_HwNm_f32
MtrVelCRF_MtrRadpS_f32
Required Global Data Outputs
CCWFound_Cnt_lgc
CCWPosition_HwDeg_f32
CWFound_Cnt_lgc
CWPosition_HwDeg_f32
Specific Include Path present
No
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
LrnEOT_Init1()
None
Init
Runnable
Scheduling Requirements
Trigger
LrnEOT_Per1
Triggered on Timing Event
10ms
LrnEOT_Scom_ResetEOT
triggered by server invocation for OperationPrototype <ResetEOT> of PortPrototype <LrnEOT_Scom>
On event
.
Memory Mapping
Mapping
Memory Section
Contents
Notes
LRNEOT_START_SEC_VAR_CLEARED_32
LRNEOT_START_SEC_VAR_CLEARED_BOOLEAN
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
Block
```
*…excerpt ends here (388 further characters in the source).*

## index_WithOutPS.pdf

- **Source:** `LrnEOT/utp/Tessy/report/index_WithOutPS.pdf`
- **Format:** `.pdf` (~971 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5997 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `LrnEOT/utp/Tessy/report/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-08-26, 16:22:29+0530
Project LrnEOT
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 4
Successful: 4
Failed: 0
Not Executed: 0
Date: 2014-08-26
Time: 16:22:29+0530
Selected Project Items
Test Object "CBD_UnitTest/LrnEOT/LrnEOT_Init1"
Test Object "CBD_UnitTest/LrnEOT/LrnEOT_Per1"
Test Object "CBD_UnitTest/LrnEOT/LrnEOT_Scom_ResetEOT"
Test Object "CBD_UnitTest/LrnEOT/ResetEOT"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: No
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Statemen
```
*…excerpt ends here (5297 further characters in the source).*

## index_WithPS.pdf

- **Source:** `LrnEOT/utp/Tessy/report/index_WithPS.pdf`
- **Format:** `.pdf` (~971 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `LrnEOT/utp/Tessy/report/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-08-26, 16:38:04+0530
Project LrnEOT
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 4
Successful: 4
Failed: 0
Not Executed: 0
Date: 2014-08-26
Time: 16:38:04+0530
Selected Project Items
Test Object "CBD_UnitTest/LrnEOT/LrnEOT_Init1"
Test Object "CBD_UnitTest/LrnEOT/LrnEOT_Per1"
Test Object "CBD_UnitTest/LrnEOT/LrnEOT_Scom_ResetEOT"
Test Object "CBD_UnitTest/LrnEOT/ResetEOT"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: Yes
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Stateme
```
*…excerpt ends here (5298 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `LrnEOT/doc/QAC_Results/Ap_LrnEOT.c.err` (~35 KiB)
- `LrnEOT/doc/QAC_Results/Ap_LrnEOT.c.met` (~257 KiB)

</details>
