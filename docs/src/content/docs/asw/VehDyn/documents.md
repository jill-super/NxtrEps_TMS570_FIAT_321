---
title: "Vehicle Dynamics documents"
description: "Word/PDF/text documents shipped with VehDyn (Vehicle Dynamics) and their conversion status."
---

# Vehicle Dynamics — documents

*Repository directory: `VehDyn`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## VehDyn_Integration_Manual.docx

- **Source:** `VehDyn/doc/VehDyn_Integration_Manual.docx`
- **Format:** `.docx` (~40 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (3633 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `VehDyn/doc/VehDyn_Integration_Manual.docx` for those.

```text
Integration Manual -- VehDyn
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
< Global function (except the ones that are defined in RTE modules) that is defined in this component but used by other function>
None
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Ap_VehDyn_Cfg.h (generated using Ap_VehDyn_Cfg.h.tt)
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
VehDynGeneral/VehDynCPEnable
Enable checkpoints if needed
VehDyn
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
VehicleSpeed_Kph_f32
HwTorque_HwNm_f32
TorqueCmdCRF_MtrNm_f32
VehicleSpeedValid_Cnt_lgc
MotorVelCRF_MtrRadpS_f32
RelHwPos_HwDeg_f32
CcwEOT_HwDeg_f32
CwEOT_HwDeg_f32
HwAuth_Uls_f32
HandwheelPosition_HwDeg_f32
MechMtrPos_Rev_f32
SrlHwAgVld_Cnt_lgc
SrlHwAg_HwDeg_f32
Required Global Data Outputs
SensorlessHwAuth_Uls_f32
SensorlessHwPos_HwDeg_f32
Specific Include Path present
< No >
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
VehDyn_Init1
Called from RTE before first call of periodic function
RTE at init
Runnable
Scheduling Requirements
Trigger
VehDyn_Per1
Should be called after the 2ms periodic that outputs RelHwPos and before the 2ms periodic that uses VDHwPos and VDAuthority
RTE 2 ms
Runnable
Scheduling Requirements
Trigger
VehDyn_Trns1
triggered on entering of Mode <OFF> of ModeDeclarationGroupPrototype <Mode> of PortPrototype <SystemState>
RTE
```
*…excerpt ends here (1133 further characters in the source).*

## VehDyn_MDD.docx

- **Source:** `VehDyn/doc/VehDyn_MDD.docx`
- **Format:** `.docx` (~336 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `VehDyn/doc/VehDyn_MDD.docx` for those.

```text
Module – VehDyn
High-Level Description
This module calculates HandWheel AutoCentering and determines the Vehicle Dynamics HandWheel Position and Vehicle Dynamics Authority.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
TorqueCmdCRF_MtrNm_f32
SensorlessHwAuth_Uls_f32
VehicleSpeed_Kph_f32
SensorlessHwPos_HwDeg_f32
HwTorque_HwNm_f32
VehicleSpeedValid_Cnt_lgc
MotorVelCRF_MtrRadpS_f32
RelHwPos_HwDeg_f32
CcwEOT_HwDeg_f32
CwEOT_HwDeg_f32
HwAuth_Uls_f32
HandwheelPosition_HwDeg_f32
MechMtrPos_Rev_f32
SrlHwAgVld_Cnt_lgc
SrlHwAg_HwDeg_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
VehDyn_PinTrqSV_M_Str. SV_Uls_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
VEHDYN_START_VAR_CLEARED_UNSPECIFIED
VehDyn_PinTrqSV_M_Str. K_Uls_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
VEHDYN_START_VAR_CLEARED_UNSPECIFIED
VehDyn_AutoCntrLoSpd_M_str. MtrVel_MtrRadpS_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
VEHDYN_START_VAR_CLEARED_UNSPECIFIED
VehDyn_AutoCntrLoSpd_M_str. VehSpd_kph_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
VEHDYN_START_VAR_CLEARED_UNSPECIFIED
VehDyn_AutoCntrLoSpd_M_str. FiltPinTrq_HwNm_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
VEHDYN_START_VAR_CLEARED_UNSPECIFIED
VehDyn_AutoCntrLoSpd_M_str. CntrWindow_HwDeg_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
VEHDYN_START_VAR_CLEARED_UNSPECIFIED
VehDyn_AutoCntrLoSpd_M_str. Timer1Thresh_mS_u16
1
See Data Dictionary
See Data Dictionary
VEHDYN_START_VAR_CLEARED_UNSPECIFIED
VehDyn_AutoCntrLoSpd_M_str. Timer2Thresh_mS_u16
1
See Data Dictionary
See Data Dictionary
VEHDYN_START_VAR_CLEARED_UNSPECIFIED
VehDyn_AutoCntrLoSpd_M_str. Timer1_mS_u32
1
See Data Dictionary
See Data Dictionary
VEHDYN_START_VAR_CLEARED_UNSPECIFIED
VehDyn_AutoCntrLoSpd_M_str. Timer2_mS_u32
1
See Data Dictionary
See Data Dictionary
VEHDYN_START_VAR_CLEARED_UNSPECIFIED
VehDyn_AutoCntrLoSpd_M_str. RelHwPosFilt1SV_HwDeg_str. SV_Uls_f32
Single Precision Float
See Data Dictio
```
*…excerpt ends here (3498 further characters in the source).*

## index_Skipped_WithoutPS.pdf

- **Source:** `VehDyn/utp/Tessy/report/index_Skipped_WithoutPS.pdf`
- **Format:** `.pdf` (~2762 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `VehDyn/utp/Tessy/report/index_Skipped_WithoutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-19, 20:22:09+0530
Project VehDyn
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 1
Successful: 1
Failed: 0
Not Executed: 0
Date: 2014-09-19
Time: 20:22:09+0530
Selected Project Items
Test Object "CBD_UnitTest/VehDyn/VehDyn_Per1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: No
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Statement Coverage, Branch Coverage, Modified Condition / Decision Coverage, 
Multiple Condition Coverage
Test Case Results for Each Test Object (without
```
*…excerpt ends here (5298 further characters in the source).*

## index_WithPS.pdf

- **Source:** `VehDyn/utp/Tessy/report/index_WithPS.pdf`
- **Format:** `.pdf` (~3746 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `VehDyn/utp/Tessy/report/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2015-09-15, 13:04:48+0530
Project VehDyn
© Report created by TESSY V3.1.12, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 6
Successful: 6
Failed: 0
Not Executed: 0
Date: 2015-09-15
Time: 13:04:48+0530
Selected Project Items
Test Object "CBD_UnitTest/VehDyn/Autocenter_f32"
Test Object "CBD_UnitTest/VehDyn/VehDyn_Init1"
Test Object "CBD_UnitTest/VehDyn/VehDyn_Per1"
Test Object "CBD_UnitTest/VehDyn/VehDyn_SCom_ForceCenter"
Test Object "CBD_UnitTest/VehDyn/VehDyn_SCom_ResetCenter"
Test Object "CBD_UnitTest/VehDyn/VehDyn_Trns1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
```
*…excerpt ends here (5299 further characters in the source).*

## index_WithoutPS.pdf

- **Source:** `VehDyn/utp/Tessy/report/index_WithoutPS.pdf`
- **Format:** `.pdf` (~3743 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `VehDyn/utp/Tessy/report/index_WithoutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2015-09-15, 13:26:42+0530
Project VehDyn
© Report created by TESSY V3.1.12, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 6
Successful: 6
Failed: 0
Not Executed: 0
Date: 2015-09-15
Time: 13:26:42+0530
Selected Project Items
Test Object "CBD_UnitTest/VehDyn/Autocenter_f32"
Test Object "CBD_UnitTest/VehDyn/VehDyn_Init1"
Test Object "CBD_UnitTest/VehDyn/VehDyn_Per1"
Test Object "CBD_UnitTest/VehDyn/VehDyn_SCom_ForceCenter"
Test Object "CBD_UnitTest/VehDyn/VehDyn_SCom_ResetCenter"
Test Object "CBD_UnitTest/VehDyn/VehDyn_Trns1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
```
*…excerpt ends here (5300 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `VehDyn/doc/QAC_Results/Ap_VehDyn.c.err` (~106 KiB)
- `VehDyn/doc/QAC_Results/Ap_VehDyn.c.met` (~712 KiB)

</details>
