---
title: "Return Firewall documents"
description: "Word/PDF/text documents shipped with ReturnFirewall (Return Firewall) and their conversion status."
---

# Return Firewall — documents

*Repository directory: `ReturnFirewall`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## ReturnFirewall_IntegrationManual.docx

- **Source:** `ReturnFirewall/doc/ReturnFirewall_IntegrationManual.docx`
- **Format:** `.docx` (~78 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (3139 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ReturnFirewall/doc/ReturnFirewall_IntegrationManual.docx` for those.

```text
Integration Manual
For
Return Firewall
VERSION: 1.0
DATE: 15-JAN-2015
Prepared By:
Spandana Balani
Revision History
Rev #
Change Description
Date
Author
1
Initial version
15-Jan-15
SB
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
<ADD more to the table if applicable>
References
This section lists the title & version of all the documents that are referred for development of this document
Sr. No.
Title
Version
1
SF36 Return Firewall
005
Dependencies
SWCs
Module
Required Feature
None
<Addition of global data, function>*.
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
None
Configuration REQUIREMeNTS
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Ap_ReturnFirewall_Cfg.h for checkpoint enable
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
ReturnFirewallGeneral/ReturnFirewallCPEnable
To enable checkpoints
ReturnFirewall
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
HandwheelPosition_HwDeg_f32
ReturnCmd_MtrNm_f32
VehicleSpeed_Kph_f32
Defeat_Return_Svc_Cnt_lgc
MEC_Counter_Cnt_enum
Required Global Data Outputs
LimitedReturn_MtrNm_f32
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
ReturnFirewall_Per1
triggered on TimingEvent
Disabled in WARM
```
*…excerpt ends here (639 further characters in the source).*

## Return_Firewall_MDD.docx

- **Source:** `ReturnFirewall/doc/Return_Firewall_MDD.docx`
- **Format:** `.docx` (~218 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5995 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ReturnFirewall/doc/Return_Firewall_MDD.docx` for those.

```text
Module – Return Firewall
High-Level Description
This module limits the return command according to safety requirements.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
HandwheelPosition_HwDeg_f32
LimitedReturn_MtrNm_f32
ReturnCmd_MtrNm_f32
VehicleSpeed_Kph_f32
Defeat_Return_Svc_Cnt_lgc
MEC_Counter_Cnt_enum
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
UprBound_MtrNm_D_f32
Single Precision Float
-8.8
8.8
RETURNFIREWALL_START_SEC_VAR_CLEARED_32
LwrBound_MtrNm_D_f32
Single Precision Float
-8.8
8.8
RETURNFIREWALL_START_SEC_VAR_CLEARED_32
OverBound_Cnt_D_lgc
N/A
FALSE
TRUE
RETURNFIREWALL_START_SEC_VAR_CLEARED_BOOLEAN
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
t_RtrnFWVehSpd_Kph_u9p7[]
t_RtrnFWUprBoundX_HwDeg_s11p4[]
t2_RtrnFWUprBoundY_MtrNm_s4p11[][]
Program (fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
None
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
D_ONE_ULS_F32
D_ZERO_ULS_F32
D_NEGONE_CNT_S16
D_FALSE_CNT_LGC
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
None
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
FPM_FloatToFixed_m
FPM_FixedToFloat_m
BilinearXMYM_s16_s16XMs16YM_Cnt
TableSize_m
Limit_m
Data Hiding Functions
Rte_Call_NxtrDiagMgr_SetNTCStatus
Global Functions/Ma
```
*…excerpt ends here (3495 further characters in the source).*

## index_WithOutPS.pdf

- **Source:** `ReturnFirewall/utp/Tessy/report/index_WithOutPS.pdf`
- **Format:** `.pdf` (~483 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5996 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `ReturnFirewall/utp/Tessy/report/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2015-03-23, 19:33:39+0530
Project Return
© Report created by TESSY V3.1.12, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 1
Successful: 1
Failed: 0
Not Executed: 0
Date: 2015-03-23
Time: 19:33:39+0530
Selected Project Items
Test Object "CBD_UnitTest/ReturnFireWall/ReturnFirewall_Per1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test 
object on the y axis. Each bar is divided into passed, not executed and failed test cases. The test case results 
do not ta
```
*…excerpt ends here (5296 further characters in the source).*

## index_WithPS.pdf

- **Source:** `ReturnFirewall/utp/Tessy/report/index_WithPS.pdf`
- **Format:** `.pdf` (~483 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5996 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `ReturnFirewall/utp/Tessy/report/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2015-03-23, 19:28:50+0530
Project Return
© Report created by TESSY V3.1.12, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 1
Successful: 1
Failed: 0
Not Executed: 0
Date: 2015-03-23
Time: 19:28:50+0530
Selected Project Items
Test Object "CBD_UnitTest/ReturnFireWall/ReturnFirewall_Per1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test 
object on the y axis. Each bar is divided into passed, not executed and failed test cases. The test case results 
do not ta
```
*…excerpt ends here (5296 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `ReturnFirewall/doc/QAC_Results/Ap_ReturnFirewall.c.err` (~104 KiB)
- `ReturnFirewall/doc/QAC_Results/Ap_ReturnFirewall.c.met` (~927 KiB)

</details>
