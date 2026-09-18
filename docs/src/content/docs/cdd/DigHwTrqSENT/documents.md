---
title: "Digital Handwheel Torque Sensing (SENT) documents"
description: "Word/PDF/text documents shipped with DigHwTrqSENT (Digital Handwheel Torque Sensing (SENT)) and their conversion status."
---

# Digital Handwheel Torque Sensing (SENT) — documents

*Repository directory: `DigHwTrqSENT`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## DigHwTrqSENT_Integration_Manual.docx

- **Source:** `DigHwTrqSENT/doc/DigHwTrqSENT_Integration_Manual.docx`
- **Format:** `.docx` (~41 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (3577 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DigHwTrqSENT/doc/DigHwTrqSENT_Integration_Manual.docx` for those.

```text
Integration Manual - DigHwTrqSENT
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
<None>
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
< None>
Configuration
Build Time Config
Modules
Notes
BC_DIGHWTRQSENT_FAULTINJECTIONPOINT
Fault injection points
Configuration Files to be provided by Integration Project
Sa_DigHwTrqSENT_Cfg.h for checkpoint enables
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
T1_HwNm_f32 from FDD ES-34B
T2_HwNm_f32 from FDD ES-34B
Required Global Data Outputs
HwTorque_HwNm_f32
SysCHwTorque_HwNm_f32
Specific Include Path present
No
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
DigHwTrqSENT_Init1()
None
Init
Runnable
Scheduling Requirements
Trigger
DigHwTrqSENT_Per1
After update of T1_HwNm_f32 and T2_HwNm_f32
2 ms
DigHwTrqSENT_Per2
None
4 ms
DigHwTrqSENT_Per3
None
100 ms
DigHwTrqSENT_SCom_ClrTrqTrim
triggered by server invocation for OperationPrototype <ClrTrqTrim> of PortPrototype <DigHwTrqSENT_SCom>
On event
DigHwTrqSENT_SCom_SetTrqTrim
triggered by server invocation for OperationPrototype <SetTrqTrim> of PortPrototype <DigHwTrqSENT_SCom>
On event
DigHwTrqSENT_SCom_TrimData
triggered by server invocation for OperationPrototype <TrimData> of PortPrototype <DigHwTrqSENT_SCom>
On event
DigHwTrqSENT_SCom_WriteData
triggered by server invocation for OperationPrototype <WriteData> of PortPrototype <DigHwTrqSENT_SCom>
On event
.
Memory Mapping
Mapping
Memory Section
Contents
Notes
DIGHWTRQSENT_START_SEC_VAR_CLEARED_32
DIGHWTRQSENT_START_SEC_VAR_CLEARE
```
*…excerpt ends here (1077 further characters in the source).*

## DigHwTrqSENT_MDD.docx

- **Source:** `DigHwTrqSENT/doc/DigHwTrqSENT_MDD.docx`
- **Format:** `.docx` (~622 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5992 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DigHwTrqSENT/doc/DigHwTrqSENT_MDD.docx` for those.

```text
Module -- Digital Handwheel Torque Function (SENT)
High-Level Description
This module computes the digital handwheel torque signal from the SENT digital sensor inputs. It takes the sensor inputs, calculates the hw torque, compensates for trim, applies filtering and limits, and outputs the handwheel torque in HwNm. It uses long term correlated compensation to provide a T1 vs T2 correlation fault diagnostic. It also contains the service calls for a trim to be set or cleared.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
T1_HwNm_f32
HwTorque_HwNm_f32
T2_HwNm_f32
SrlComHwTrq_HwNm_f32
MECCounter_Cnt_enum
SrlComHwTrqValid_Cnt_Lgc
SysCHwTorque_HwNm_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
DigHwTrqSENT_T1_HwNm_M_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
DIGHWTRQSENT_START_SEC_VAR_CLEARED_32
DigHwTrqSENT_T2_HwNm_M_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
DIGHWTRQSENT_START_SEC_VAR_CLEARED_32
DigHwTrqSENT_HwTrq_HwNm_M_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
DIGHWTRQSENT_START_SEC_VAR_CLEARED_32
DigHwTrqSENT_TDiagFiltOut_HwNm_M_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
DIGHWTRQSENT_START_SEC_VAR_CLEARED_32
DigHwTrqSENT_SSDiagFiltOut_HwNm_M_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
DIGHWTRQSENT_START_SEC_VAR_CLEARED_32
DigHwTrqSENT_CMCFiltOut_HwNm_M_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
DIGHWTRQSENT_START_SEC_VAR_CLEARED_32
DigHwTrqSENT_TrqSum_HwNm_M_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
DIGHWTRQSENT_START_SEC_VAR_CLEARED_32
DigHwTrqSENT_DigHwTrqKSV_M_str
See Data Dictionary
See Data Dictionary
See Data Dictionary
DIGHWTRQSENT_START_SEC_VAR_CLEARED_UNSPECIFIED
DigHwTrqSENT_TDiagFiltKSV_M_str
See Data Dictionary
See Data Dictionary
See Data Dictionary
DIGHWTRQSENT_START_SEC_VAR_CLEARED_UNSPECIFIED
DigHwTrqSENT_SSFiltKSV_M_str
See Data Dictionary
See Data Dictionary
See Data Dictionary
DIGHWTRQSENT_START_SEC_VAR_CLEARED_UNSPECIFIED
DigHwTrqSEN
```
*…excerpt ends here (3492 further characters in the source).*

## index_Skipped_WithPS_FLTINJ.pdf

- **Source:** `DigHwTrqSENT/utp/Tessy/report/index_Skipped_WithPS_FLTINJ.pdf`
- **Format:** `.pdf` (~240 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5995 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DigHwTrqSENT/utp/Tessy/report/index_Skipped_WithPS_FLTINJ.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-08-25, 17:23:56+0530
Project CBD_DigHwTrqSENT
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 1
Successful: 1
Failed: 0
Not Executed: 0
Date: 2014-08-25
Time: 17:23:56+0530
Selected Project Items
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqSENT_SCom_WriteData"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: Yes
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object and Called Functions
Coverage: Statement Coverage, Branch Coverage, Decision Coverage, Modified Condition / 
Decision Coverage,
```
*…excerpt ends here (5295 further characters in the source).*

## index_WithOutPS.pdf

- **Source:** `DigHwTrqSENT/utp/Tessy/report/index_WithOutPS.pdf`
- **Format:** `.pdf` (~1978 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DigHwTrqSENT/utp/Tessy/report/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-08-22, 18:11:05+0530
Project CBD_DigHwTrqSENT
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 9
Successful: 7
Failed: 2
Not Executed: 0
Date: 2014-08-22
Time: 18:11:05+0530
Selected Project Items
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_Init1"
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_Per1"
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_Per2"
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_Per3"
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_SCom_ClrTrqTrim"
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_SCom_SetTrqTrim"
Test Object "CBD_Unit
```
*…excerpt ends here (5299 further characters in the source).*

## index_WithOutPS_FLTINJ.pdf

- **Source:** `DigHwTrqSENT/utp/Tessy/report/index_WithOutPS_FLTINJ.pdf`
- **Format:** `.pdf` (~1995 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DigHwTrqSENT/utp/Tessy/report/index_WithOutPS_FLTINJ.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-08-25, 16:11:20+0530
Project CBD_DigHwTrqSENT
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 9
Successful: 7
Failed: 2
Not Executed: 0
Date: 2014-08-25
Time: 16:11:20+0530
Selected Project Items
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqSENT_Init1"
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqSENT_Per1"
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqSENT_Per2"
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqSENT_Per3"
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqSENT_SCom_ClrTrqTrim"
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqS
```
*…excerpt ends here (5300 further characters in the source).*

## index_WithPS.pdf

- **Source:** `DigHwTrqSENT/utp/Tessy/report/index_WithPS.pdf`
- **Format:** `.pdf` (~1979 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DigHwTrqSENT/utp/Tessy/report/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-08-22, 17:02:56+0530
Project CBD_DigHwTrqSENT
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 9
Successful: 7
Failed: 2
Not Executed: 0
Date: 2014-08-22
Time: 17:02:56+0530
Selected Project Items
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_Init1"
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_Per1"
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_Per2"
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_Per3"
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_SCom_ClrTrqTrim"
Test Object "CBD_UnitTest/DigHwTrqSENT/DigHwTrqSENT_SCom_SetTrqTrim"
Test Object "CBD_Unit
```
*…excerpt ends here (5299 further characters in the source).*

## index_WithPS_FLTINJ.pdf

- **Source:** `DigHwTrqSENT/utp/Tessy/report/index_WithPS_FLTINJ.pdf`
- **Format:** `.pdf` (~1994 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DigHwTrqSENT/utp/Tessy/report/index_WithPS_FLTINJ.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-08-25, 16:39:59+0530
Project CBD_DigHwTrqSENT
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 9
Successful: 6
Failed: 2
Not Executed: 1
Date: 2014-08-25
Time: 16:39:59+0530
Selected Project Items
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqSENT_Init1"
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqSENT_Per1"
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqSENT_Per2"
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqSENT_Per3"
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqSENT_SCom_ClrTrqTrim"
Test Object "CBD_UnitTest/DigHwTrqSENT_FLTINJ/DigHwTrqS
```
*…excerpt ends here (5300 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `DigHwTrqSENT/doc/QAC_Results/Sa_DigHwTrqSENT.c.err` (~106 KiB)
- `DigHwTrqSENT/doc/QAC_Results/Sa_DigHwTrqSENT.c.met` (~971 KiB)

</details>
