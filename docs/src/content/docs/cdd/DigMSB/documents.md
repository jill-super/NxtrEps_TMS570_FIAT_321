---
title: "Digital MSB Position Sensor Interface documents"
description: "Word/PDF/text documents shipped with DigMSB (Digital MSB Position Sensor Interface) and their conversion status."
---

# Digital MSB Position Sensor Interface — documents

*Repository directory: `DigMSB`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## DigMSB_Integration_Manual.docx

- **Source:** `DigMSB/doc/DigMSB_Integration_Manual.docx`
- **Format:** `.docx` (~80 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (4399 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DigMSB/doc/DigMSB_Integration_Manual.docx` for those.

```text
Integration Manual
For
DigMSB (ES-50A)
VERSION: 8.0
DATE: 02-06-2015
Prepared By:
Rijvi Ahmed
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
nzt9hv
1
31-May-13
2
Corrected the Digital MSB
Nzt9hv
2
02-Aug-13
3
Updated for v 2 ES 50A Draft
Nzt9hv
3
08-Aug-13
4
Note added to provide buffer output synchronisation
Nzt9hv
4
28-Aug-13
5
Added new Memmap statement for cleared DIGMSB_START_SEC_VAR_CLEARED_8
Nzt9hv
5
23-Sep-13
6
Updated for ES50A prerelease
Selva
6
3-Apr-14
7
Updated for ES50A v6
Selva
7
23-Apr-14
8
Updated for FDD rev.008 and updated to latest Integration Manual Template
Rijvi
8
06-Feb-15
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
FDD
Functional Design Document
References
This section lists the title & version of all the documents that are referred for development of this document
Sr. No.
Title
Version
1
ES50A_DigMSBAllegro1331
008
Dependencies
SWCs
Module
Required Feature
SPINxt
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.
Note: Integration of DigMSBSigCorr component is required if using DigMSB component of version 5 or less. DigMSBCorr Component is not needed after the integration DigMSB v6 or more.
Global Functions(Non RTE) to be provided to Integration Project
DigMSB_Per1
Configuration REQUIREMeNTS
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
DigMSB_Cfg.h ( Refer DigMSB_Cfg_Template.h in tools folder)
(Data synchron
```
*…excerpt ends here (1899 further characters in the source).*

## DigtalMSB_MDD.docx

- **Source:** `DigMSB/doc/DigtalMSB_MDD.docx`
- **Format:** `.docx` (~1996 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5995 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DigMSB/doc/DigtalMSB_MDD.docx` for those.

```text
Module – Digital MSB`
High-Level Description
The data synchronsiation between Motor Control ISR and 2 ms Task will be provided at the integration level. But the synchronization between 2 and 100ms is provided by the Module level variable by disabling and enabling interrupts.
Note: Some variables are used as both input and output. For the those outputs use the ranges from inputs.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
UncorrMechMtrPos1_Rev_u0p16
UncorrMechMtrPos1_Rev_u0p16
Die2RxError_Cnt_u16
Die2RxError_Cnt_u16
Die2RxRevCtr_Cnt_u16
Die2RxRevCtr_Cnt_u16
Die2RxMtrPos_Cnt_u16
Die2RxMtrPos_Cnt_u16
Die1RxError_Cnt_u16
Die1RxError_Cnt_u16
Die1RxRevCtr_Cnt_u16
Die1RxRevCtr_Cnt_u16
CumMechMtrPos_Rev_f32
AlignedCumMechMtrPosCRF_Deg_f32
RxMtrPosParityAccum_Cnt_u16
CumMechMtrPosCRF_Deg_f32
MtrPosPolarity_Cnt_s08
CumMechMtrPosMRF_Deg_f32
EnergyModeState_Cnt_enum
MechMtrPos2_Rev_u0p16
CorrectedElecMtrPos_Rev_u0p16
SysCCumMechMtrPosMRF_Deg_f32
UncorrMechMtrPos1_Rev_u0p16
AlignedCumMechMtrPosStatus_Cnt_u08
Die1RxError_Cnt_u16
MechMtrPos1_Rev_u0p16
Die1RxRevCtr_Cnt_u16
SysCMechMtrPos1_Rev_u0p16
Die2RxRevCtr_Cnt_u16
SysCorrectedElecMtrPos_Rev_u0p16
Die2RxMtrPos_Cnt_u16
MechMtrPos1TimeStamp_uSec_u32
Die1UnderVoltgFltAccum_Cnt_u16
MechMtrPos2TimeStamp_uSec_u32
CorrectedElecMtrPos_Rev_u0p16
UncorrMechMtrPos1_Rev_u0p16
CumMechMtrPos_Rev_s15p16
Die1RxError_Cnt_u16
Die1RxRevCtr_Cnt_u16
Die2RxRevCtr_Cnt_u16
Die1RxMtrPos_Cnt_u16
Die2RxMtrPos_Cnt_u16
RxMtrPos1ParityAccum_Cnt_u16
RxMtrPos1UnderVoltgFltAccum_Cnt_u16
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
DigMSB_PWMGrpData_Cnt_M_u16[3]
1
See Data Dictionary
See Data Dictionary
DIGMSB_START_SEC_VAR_CLEARED_16
DigMSB_AsyncConfigGrpDie1_Cnt_M_u16[3]
1
See Data Dictionary
See Data Dictionary
DIGMSB_START_SEC_VAR_CLEARED_16
DigMSB_AsyncConfigGrpDie2_Cnt_M_u16[3]
1
See Data Dictionary
See Data Dictionary
DIGMSB_START_SEC_VAR_CLEARED_16
DigMSB_MechMtrPos1UnCorrec_Rev_M_u0p16
1.52588E-05
See Data Dictionary
See Data Dictionary
DIGMSB_START_SEC_VAR_CLEARED_16
DigMSB_RxMtrPo
```
*…excerpt ends here (3495 further characters in the source).*

## index_WithOutPS.pdf

- **Source:** `DigMSB/utp/Tessy/report/index_WithOutPS.pdf`
- **Format:** `.pdf` (~16670 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DigMSB/utp/Tessy/report/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2015-01-30, 20:20:13+0530
Project DigMSB
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 7
Successful: 4
Failed: 3
Not Executed: 0
Date: 2015-01-30
Time: 20:20:13+0530
Selected Project Items
Test Object "CBD_UnitTest/DiagMSB/DigMSB_Init"
Test Object "CBD_UnitTest/DiagMSB/DigMSB_Per1"
Test Object "CBD_UnitTest/DiagMSB/DigMSB_Per2"
Test Object "CBD_UnitTest/DiagMSB/DigMSB_Per3"
Test Object "CBD_UnitTest/DiagMSB/ErrorRegisterProcessing"
Test Object "CBD_UnitTest/DiagMSB/MtrPosProcessing"
Test Object "CBD_UnitTest/DiagMSB/RevCntrProcessing"
Used Test Environments
TI TMS 570 PLS UDE (Default
```
*…excerpt ends here (5300 further characters in the source).*

## index_WithPS.pdf

- **Source:** `DigMSB/utp/Tessy/report/index_WithPS.pdf`
- **Format:** `.pdf` (~16683 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DigMSB/utp/Tessy/report/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2015-01-30, 19:53:02+0530
Project DigMSB
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 7
Successful: 4
Failed: 3
Not Executed: 0
Date: 2015-01-30
Time: 19:53:02+0530
Selected Project Items
Test Object "CBD_UnitTest/DiagMSB/DigMSB_Init"
Test Object "CBD_UnitTest/DiagMSB/DigMSB_Per1"
Test Object "CBD_UnitTest/DiagMSB/DigMSB_Per2"
Test Object "CBD_UnitTest/DiagMSB/DigMSB_Per3"
Test Object "CBD_UnitTest/DiagMSB/ErrorRegisterProcessing"
Test Object "CBD_UnitTest/DiagMSB/MtrPosProcessing"
Test Object "CBD_UnitTest/DiagMSB/RevCntrProcessing"
Used Test Environments
TI TMS 570 PLS UDE (Default
```
*…excerpt ends here (5300 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `DigMSB/doc/QAC_Results/Sa_DigMSB.c.err` (~110 KiB)
- `DigMSB/doc/QAC_Results/Sa_DigMSB.c.met` (~987 KiB)

</details>
