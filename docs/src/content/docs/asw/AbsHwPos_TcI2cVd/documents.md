---
title: "Absolute Handwheel Position (Turns Counter, I²C, Sensorless Vehicle Dynamics) documents"
description: "Word/PDF/text documents shipped with AbsHwPos_TcI2cVd (Absolute Handwheel Position (Turns Counter, I²C, Sensorless Vehicle Dynamics)) and their conversion status."
---

# Absolute Handwheel Position (Turns Counter, I²C, Sensorless Vehicle Dynamics) — documents

*Repository directory: `AbsHwPos_TcI2cVd`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## AbsHwPos_TcI2cVd_Integration_Manual.docx

- **Source:** `AbsHwPos_TcI2cVd/doc/AbsHwPos_TcI2cVd_Integration_Manual.docx`
- **Format:** `.docx` (~41 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (3812 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `AbsHwPos_TcI2cVd/doc/AbsHwPos_TcI2cVd_Integration_Manual.docx` for those.

```text
Integration Manual – Absolute Handwheel Position – Turns Counter, I2C, and SensorlessVehicle Dynamics
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
None
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Ap_AbsHwPos_Cfg.h (generated using Ap_AbsHwPos_Cfg.h.tt)
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
AbsHwPosGeneral\AbsHwPosCPEnable
Enable checkpoints if needed
AbsHwPos
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
CumMechMtrPosCRF_Deg_f32
AlignedCumMechMtrPosCRF_Deg_f32
TurnsCntrValidity_Cnt_u08
I2CHwAbsPos_HwDeg_f32
I2CHwAbsPosValid_Cnt_lgc
SensorlessHwPos_HwDeg_f32
SensorlessAuthority_Uls_f32
ComplError_HwDeg_f32
DiagStatusHwPosReducedPerf_Cnt_lgc
ManufMode_Cnt_enum
Required Global Data Outputs
HandwheelPosition_HwDeg_f32
HandwheelAuthority_Uls_f32
RelHwPos_HwDeg_f32
HwPosSource_Cnt_u16
SrlComHwPos_HwDeg_f32
SrlComHwPosStatus_Cnt_u16
Specific Include Path present
No
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
AbsHwPos_Init1
Called from RTE before first call of periodic function
RTE at init
Runnable
Scheduling Requirements
Trigger
AbsHwPos_Per1
Call before 2ms periodic that uses RelHwPos_HwDeg_f32
RTE 2 ms
AbsHwPos_Per2
Call after 2ms periodic that outputs VDHwPos_HwDeg_f32
RTE 2 ms
AbsHwPos_Per3
None
RTE 4 ms
AbsHwPos_Per4
None
RTE 10 ms
AbsHwPos_S
```
*…excerpt ends here (1312 further characters in the source).*

## Absolute_Handwheel_Position_TcI2cVd_MDD.docx

- **Source:** `AbsHwPos_TcI2cVd/doc/Absolute_Handwheel_Position_TcI2cVd_MDD.docx`
- **Format:** `.docx` (~1199 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5994 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `AbsHwPos_TcI2cVd/doc/Absolute_Handwheel_Position_TcI2cVd_MDD.docx` for those.

```text
Module -- Absolute Handwheel Position TcI2cVd
High-Level Description
The Absolute Hand Wheel Position Function is responsible for determining the steering wheel hand wheel position using either a Turns Counter estimate of motor position during key off and sensorless learnt internal hw position (for eg. Sensorless Vehicle Dynamics, Stored Last Position, Travel Exclusuin, etc) or I2C digital hw position sensor and sensorless learnt internal hw position.
Figures
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs
Module Outputs
CumMechMtrPosCRF_Deg_f32
HandwheelPosition_HwDeg_f32
AlignedCumMechMtrPosCRF_Deg_f32
HandwheelAuthority_Uls_f32
TurnsCntrValidity_Cnt_u08
RelHwPos_HwDeg_f32
I2CHwAbsPos_HwDeg_f32
HwPosSource_Cnt_u16
I2CHwAbsPosValid_Cnt_lgc
SrlComHwPos_HwDeg_f32
SensorlessHwPos_HwDeg_f32
SrlComHwPosStatus_Cnt_u16
SensorlessAuthority_Uls_f32
ComplError_HwDeg_f32
DiagStatusHwPosReducedPerf_Cnt_lgc
ManufMode_Cnt_enum
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
AbsHwPos_HwPosState_Cnt_M_enum
1
See Data Dictionary
See Data Dictionary
ABSHWPOS_START_SEC_VAR_CLEARED_UNSPECIFIED
AbsHwPos_HandwheelPositionLPF_M_str.SV_Uls_f32
Single precision Float
See Data Dictionary
See Data Dictionary
ABSHWPOS_START_SEC_VAR_CLEARED_UNSPECIFIED
AbsHwPos_HandwheelPositionLPF_M_str.K_Uls_f32
Single precision Float
See Data Dictionary
See Data Dictionary
ABSHWPOS_START_SEC_VAR_CLEARED_UNSPECIFIED
AbsHwPos_SrlComHwPosStatus_Cnt_M_u16
1
See Data Dictionary
See Data Dictionary
ABSHWPOS_START_SEC_VAR_CLEARED_16
AbsHwPos_VehCntrValid_Cnt_M_lgc
n/a
See Data Dictionary
See Data Dictionary
ABSHWPOS_START_SEC_VAR_CLEARED_BOOLEAN
AbsHwPos_VehCntrOfstLearn_Cnt_M_lgc
n/a
See Data Dictionary
See Data Dictionary
ABSHWPOS_START_SEC_VAR_CLEARED_BOOLEAN
AbsHwPos_HwAtoMtrAFltAcc_Cnt_M_u16
1
See Data Dictionary
See Data Dictionary
ABSHWPOS_START_SEC_VAR_CLEARED_16
AbsHwPos_HwPosSource_Cnt_M_u16
1
See Data Dictionary
See Data Dictionary
ABSHWPOS_START_SEC_VAR_
```
*…excerpt ends here (3494 further characters in the source).*

## index_WithOutPS.pdf

- **Source:** `AbsHwPos_TcI2cVd/utp/Tessy/report/index_WithOutPS.pdf`
- **Format:** `.pdf` (~2459 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `AbsHwPos_TcI2cVd/utp/Tessy/report/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-04, 16:46:29+0530
Project AbsHwPos_TcI2cVd
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 10
Successful: 10
Failed: 0
Not Executed: 0
Date: 2014-09-04
Time: 16:46:29+0530
Selected Project Items
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_Init1"
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_Per1"
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_Per2"
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_Per3"
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_Per4"
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_SCom_CustClrTrim"
Test Object "CBD_UnitTest/Abs
```
*…excerpt ends here (5300 further characters in the source).*

## index_WithPS.pdf

- **Source:** `AbsHwPos_TcI2cVd/utp/Tessy/report/index_WithPS.pdf`
- **Format:** `.pdf` (~2458 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `AbsHwPos_TcI2cVd/utp/Tessy/report/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-04, 15:57:41+0530
Project AbsHwPos_TcI2cVd
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 10
Successful: 10
Failed: 0
Not Executed: 0
Date: 2014-09-04
Time: 15:57:41+0530
Selected Project Items
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_Init1"
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_Per1"
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_Per2"
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_Per3"
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_Per4"
Test Object "CBD_UnitTest/AbsHwPos_TcI2lVd/AbsHwPos_SCom_CustClrTrim"
Test Object "CBD_UnitTest/Abs
```
*…excerpt ends here (5300 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `AbsHwPos_TcI2cVd/doc/QAC_Results/Ap_AbsHwPos.c.err` (~98 KiB)
- `AbsHwPos_TcI2cVd/doc/QAC_Results/Ap_AbsHwPos.c.met` (~487 KiB)

</details>
