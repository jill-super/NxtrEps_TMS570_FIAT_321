---
title: "Digital Column Position Sensor Interface (I²C) documents"
description: "Word/PDF/text documents shipped with DigColPs (Digital Column Position Sensor Interface (I²C)) and their conversion status."
---

# Digital Column Position Sensor Interface (I²C) — documents

*Repository directory: `DigColPs`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## DigColPsInt_MDD.docx

- **Source:** `DigColPs/doc/DigColPsInt_MDD.docx`
- **Format:** `.docx` (~1273 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5994 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DigColPs/doc/DigColPsInt_MDD.docx` for those.

```text
Module -- Digital Column Position Sensor (I2C) Interface
High-Level Description
This module is responsible for the transport of sensor data between the I2C peripheral and the DigColPs Component. This module accomplishes this task by providing a number of interface functions. The functions handle the complexities of making request and handling the underlying interrupts to present the periodic task in the DigColPs module with the requested data on the next iteration.
Figures
Diagram – Function Data Sharing
See DigColPs_MDD for sequence diagram and interaction between this module, the DigColPs module and the physical sensor.
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
Type_Cnt_u08
CommFaults_Cnt_b08
DataType_Cnt_u08
ColSnsrData_Cnt_u16
SpurSnsrData_Cnt_u16
DigColPsInt_I2CHwCustData_Uls_M_u16
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
DigColPsInt_CurrentStepNo_Cnt_M_enum
1
0
36
DIGCOLPSINT_START_SEC_VAR_CLEARED_UNSPECIFIED
DigColPsInt_InitialTime_mS_M_u32
1
0
FULL
DIGCOLPSINT_START_SEC_VAR_CLEARED_32
DigColPsInt_ColSnsrData_Cnt_M_u16
1
0
65535
DIGCOLPSINT_START_SEC_VAR_CLEARED_16
DigColPsInt_SpurSnsrData_Cnt_M_u16
1
0
65535
DIGCOLPSINT_START_SEC_VAR_CLEARED_16
DigColPsInt_ColSnsrErrData_Cnt_D_u16
1
0
FULL
DIGCOLPSINT_START_SEC_VAR_CLEARED_16
DigColPsInt_ColSnsrExtErrData_Cnt_D_u16
1
0
FULL
DIGCOLPSINT_START_SEC_VAR_CLEARED_16
DigColPsInt_ColSnsrCheckStatData_Cnt_D_u16
1
0
FULL
DIGCOLPSINT_START_SEC_VAR_CLEARED_16
DigColPsInt_SpurSnsrErrData_Cnt_D_u16
1
0
FULL
DIGCOLPSINT_START_SEC_VAR_CLEARED_16
DigColPsInt_SpurSnsrExtErrData_Cnt_D_u16
1
0
FULL
DIGCOLPSINT_START_SEC_VAR_CLEARED_16
DigColPsInt_SpurSnsrCheckStatData_Cnt_D_u16
1
0
FULL
DIGCOLPSINT_START_SEC_VAR_CLEARED_16
DigColPsInt_CurrentSlave_Cnt_M_u08
1
0
127
DIGCOLPSINT_START_SEC_VAR_CLEARED_8
DigColPsInt_RecvdDataType_Cnt_M_u08
1
0
5
DIGCOLPSINT_START_SEC_VAR_CLEARED_8
DigColPsInt_Buffer_Cnt_M_u08[]
1
0
255
DIGCOLPSINT_START_SEC_VAR_CLEARED_8
DigColPsInt_PrevReqDataType_Cnt_M_u08
1
0
5
DIGCOLPSINT_START_SEC_VAR_CLEARED_8
DigColPsInt_TransactionCnt_Cnt_M_u08
1
0
255
DIGCO
```
*…excerpt ends here (3494 further characters in the source).*

## DigColPs_Integration_Manual.docx

- **Source:** `DigColPs/doc/DigColPs_Integration_Manual.docx`
- **Format:** `.docx` (~31 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2931 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DigColPs/doc/DigColPs_Integration_Manual.docx` for those.

```text
Integration Manual – Digital Column Position Sensor
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
I2cNxtr
All functions
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
None
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
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
The following settings need to be configured in I2cNxtr_Cfg.h – a template of which can be found in the include directory of the I2cNxtr component.
Constant
Notes
SWC
D_COMMBUFFERSIZE_CNT_U08
3
I2cNxtr
I2c_Notification
DigColPsInt_InterruptNotification
I2cNxtr
D_I2CREG_STRCPTR
i2cREG1
I2cNxtr
D_VCLK_HZ_F32
Set to corresponding VCLK frequency, commonly 8000000.0 for a 160.0 MHz part.
I2cNxtr
Integration
Required Global Data Inputs
None
Required Global Data Outputs
None
Specific Include Path present
Yes
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
DigColPs_Init1
None
RTE(Init)
Runnable
Scheduling Requirements
Trigger
DigColPs_Per1
Early in 2 ms task to minimize jitter
RTE (2 ms)
DigColPs_Per2
None
RTE (4 ms)
.
Memory Mapping
Mapping
Memory Section
Contents
Notes
DIGCOLPS_START_SEC_VAR_CLEARED_32
float32
DIGCOLPS_START_SEC_VAR_CLEARED_16
uint16
DIGCOLPS_START_SEC_VAR_CLEARED_8
uint8, sint8
DIGCOLPS_START_SEC_VAR_CLEARED_BOOLEAN
Boolean
DIGCOLPS_START_SEC_VAR_CLEARED_UNSPECIFIED
LPF32KSV_Str
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requiremen
```
*…excerpt ends here (431 further characters in the source).*

## DigColPs_MDD.docx

- **Source:** `DigColPs/doc/DigColPs_MDD.docx`
- **Format:** `.docx` (~2111 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5997 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DigColPs/doc/DigColPs_MDD.docx` for those.

```text
Module -- Digital Column Position Sensor (I2C)
High-Level Description
The digital column position sensor component reads sensor data from the digital column position sensor interface and processes the raw angle data into handwheel position in degrees and determines the validity of that angle.
Figures
Data Flow Sequence
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs
Module Outputs
MecState_Cnt_enum
I2CHwAbsPos_HwDeg_f32
I2CHwAbsPosValid_Cnt_lgc
TrimComp_Cnt_lgc
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
DigColPs_I2CHwColAngle_Deg_M_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
DIGCOLPS_START_SEC_VAR_CLEARED_32
DigColPs_I2CHwSpurAngle_Deg_M_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
DIGCOLPS_START_SEC_VAR_CLEARED_32
DigColPs_PrevI2CHwColAngle_Deg_M_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
DIGCOLPS_START_SEC_VAR_CLEARED_32
DigColPs_PrevI2CHwSpurAngle_Deg_M_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
DIGCOLPS_START_SEC_VAR_CLEARED_32
DigColPs_PrevColPos_Deg_M_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
DIGCOLPS_START_SEC_VAR_CLEARED_32
DigColPs_ColTrimStatic_Deg_M_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
DIGCOLPS_START_SEC_VAR_CLEARED_32
DigColPs_SpurTrimStatic_Deg_M_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
DIGCOLPS_START_SEC_VAR_CLEARED_32
DigColPs_VernDiagError_Deg_D_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
DIGCOLPS_START_SEC_VAR_CLEARED_32
DigColPs_ColAngle_Deg_D_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
DIGCOLPS_START_SEC_VAR_CLEARED_32
DigColPs_SpurAngle_Deg_D_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
DIGCOLPS_START_SEC_VAR_CLEARED_32
DigColPs_VernierLevel_Deg_D_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
DIGCOLPS_START_SEC_VAR_CLEARED_32
DigColPs_
```
*…excerpt ends here (3497 further characters in the source).*

## index_WithOutPS.pdf

- **Source:** `DigColPs/utp/Tessy/report/DigColPs/index_WithOutPS.pdf`
- **Format:** `.pdf` (~3761 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DigColPs/utp/Tessy/report/DigColPs/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-10-14, 18:25:00+0530
Project DigColPs
© Report created by TESSY V3.1.9, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2014-10-14
Time: 18:25:00+0530
Selected Project Items
Test Object "CBD_UnitTest/DigColPs/ComputeRoughTurns"
Test Object "CBD_UnitTest/DigColPs/ConstrainOneRev"
Test Object "CBD_UnitTest/DigColPs/DiagnosticThreshold"
Test Object "CBD_UnitTest/DigColPs/DigColPs_Init1"
Test Object "CBD_UnitTest/DigColPs/DigColPs_Per1"
Test Object "CBD_UnitTest/DigColPs/DigColPs_Per2"
Test Object "CBD_UnitTest/DigColPs/DigColPs_SCom_CustClrTrim"
Test Object "CBD_UnitTe
```
*…excerpt ends here (5300 further characters in the source).*

## index_WithPS.pdf

- **Source:** `DigColPs/utp/Tessy/report/DigColPs/index_WithPS.pdf`
- **Format:** `.pdf` (~3762 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DigColPs/utp/Tessy/report/DigColPs/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-10-14, 17:39:58+0530
Project DigColPs
© Report created by TESSY V3.1.9, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2014-10-14
Time: 17:39:58+0530
Selected Project Items
Test Object "CBD_UnitTest/DigColPs/ComputeRoughTurns"
Test Object "CBD_UnitTest/DigColPs/ConstrainOneRev"
Test Object "CBD_UnitTest/DigColPs/DiagnosticThreshold"
Test Object "CBD_UnitTest/DigColPs/DigColPs_Init1"
Test Object "CBD_UnitTest/DigColPs/DigColPs_Per1"
Test Object "CBD_UnitTest/DigColPs/DigColPs_Per2"
Test Object "CBD_UnitTest/DigColPs/DigColPs_SCom_CustClrTrim"
Test Object "CBD_UnitTe
```
*…excerpt ends here (5300 further characters in the source).*

## index_WithOutPs.pdf

- **Source:** `DigColPs/utp/Tessy/report/DigColPsInt/index_WithOutPs.pdf`
- **Format:** `.pdf` (~3831 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DigColPs/utp/Tessy/report/DigColPsInt/index_WithOutPs.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-10-14, 23:13:27+0530
Project DigColPsInt
© Report created by TESSY V3.1.9, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 8
Successful: 6
Failed: 2
Not Executed: 0
Date: 2014-10-14
Time: 23:13:27+0530
Selected Project Items
Test Collection "CBD_UnitTest"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: Yes
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Statement Coverage, Branch Coverage, Modified Condition / Decision Coverage, 
Multiple Condition Coverage
Test Case Results for Each Test Object (without Coverage
```
*…excerpt ends here (5298 further characters in the source).*

## index_WithPS.pdf

- **Source:** `DigColPs/utp/Tessy/report/DigColPsInt/index_WithPS.pdf`
- **Format:** `.pdf` (~3832 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DigColPs/utp/Tessy/report/DigColPsInt/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-10-14, 23:47:43+0530
Project DigColPsInt
© Report created by TESSY V3.1.9, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 8
Successful: 6
Failed: 2
Not Executed: 0
Date: 2014-10-14
Time: 23:47:43+0530
Selected Project Items
Test Collection "CBD_UnitTest"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: Yes
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Statement Coverage, Branch Coverage, Modified Condition / Decision Coverage, 
Multiple Condition Coverage
Test Case Results for Each Test Object (without Coverage
```
*…excerpt ends here (5298 further characters in the source).*

## Static-analysis outputs (4 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `DigColPs/doc/QAC_Results/Sa_DigColPs.c.err` (~106 KiB)
- `DigColPs/doc/QAC_Results/Sa_DigColPs.c.met` (~858 KiB)
- `DigColPs/doc/QAC_Results/Sa_DigColPsInt.c.err` (~9 KiB)
- `DigColPs/doc/QAC_Results/Sa_DigColPsInt.c.met` (~402 KiB)

</details>
