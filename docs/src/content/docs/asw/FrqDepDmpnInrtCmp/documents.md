---
title: "Frequency-Dependent Damping and Inertia Compensation documents"
description: "Word/PDF/text documents shipped with FrqDepDmpnInrtCmp (Frequency-Dependent Damping and Inertia Compensation) and their conversion status."
---

# Frequency-Dependent Damping and Inertia Compensation — documents

*Repository directory: `FrqDepDmpnInrtCmp`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Frequency_Dependant_Damping_And_Inertia_Compenstation_MDD.docx

- **Source:** `FrqDepDmpnInrtCmp/doc/Frequency_Dependant_Damping_And_Inertia_Compenstation_MDD.docx`
- **Format:** `.docx` (~812 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5996 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `FrqDepDmpnInrtCmp/doc/Frequency_Dependant_Damping_And_Inertia_Compenstation_MDD.docx` for those.

```text
Module -- Frequency Dependant Damping and Inertia Compensation
High-Level Description
This MDD describes the methods to provide compensation that is dependent on filter of motor velocity which will compensate for motor inertia at low frequencies and provide damping acting at higher frequencies.
Figures
Diagram – Component
Diagram – Function Data Sharing
N/A
Diagram – FrqDepDmpnInrtCmp_Per1
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs
Module Outputs
HwTorque_HwNm_f32
FrqDepDmpnInrtCmp_MtrNm_f32
CRFMotorVel_MtrRadpS_f32
BaseAssistCmd_MtrNm_f32
VehicleSpeed_Kph_f32
WIRCmdAmpBlnd_MtrNm_f32
FreqDepDmpSrlComSvcDft_Cnt_lgc
VehicleLonAccel_KphpS_T_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
PrevTbarAng_HwDeg_M_f32
Single Precision Floating Point
-20
20
FRQDEPDMPNINRTCMP_START_SEC_VAR_CLEARED_32
Prev1SclDrvVel_RadpS_M_f32
Single Precision Floating Point
-12917.3
12917.3
FRQDEPDMPNINRTCMP_START_SEC_VAR_CLEARED_32
Prev2SclDrvVel_RadpS_M_f32
Single Precision Floating Point
-12917.3
12917.3
FRQDEPDMPNINRTCMP_START_SEC_VAR_CLEARED_32
Prev1PreAttnComp_MtrNm_M_f32
Single Precision Floating Point
-8.8
8.8
FRQDEPDMPNINRTCMP_START_SEC_VAR_CLEARED_32
Prev2PreAttnComp_MtrNm_M_f32
Single Precision Floating Point
-8.8
8.8
FRQDEPDMPNINRTCMP_START_SEC_VAR_CLEARED_32
TbarVelFiltSv_M_str
N/A
N/A
N/A
FRQDEPDMPNINRTCMP_START_SEC_VAR_CLEARED_UNSPECIFIED
TbarVelFiltSv_M_str.K_ULS_F32
Single Precision Floating Point
0.001255848
0.715390457
TbarVelFiltSv_M_str.SV_ULS_F32
Single Precision Floating Point
-6.6667
6.6667
FRQDEPDMPNINRTCMP_START_SEC_VAR_CLEARED_32
PreDecelGain_Uls_M_f32
Single Precision Floating Point
1
FULL
FRQDEPDMPNINRTCMP_START_SEC_VAR_CLEARED_32
Module Display Variables
This section identifies the name, range and resolutions for data test points defined by the FDD. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal R
```
*…excerpt ends here (3496 further characters in the source).*

## index_Skipped_WithOutPS.pdf

- **Source:** `FrqDepDmpnInrtCmp/utp/Tessy/report/index_Skipped_WithOutPS.pdf`
- **Format:** `.pdf` (~229 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5993 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `FrqDepDmpnInrtCmp/utp/Tessy/report/index_Skipped_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-19, 16:43:04+0530
Project FDD_Inertia
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 1
Successful: 1
Failed: 0
Not Executed: 0
Date: 2014-09-19
Time: 16:43:04+0530
Selected Project Items
Test Object "CBD_UnitTest/FDD_Inertia/FrqDepDmpnInrtCmp_Init"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: Yes
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Statement Coverage, Branch Coverage, Decision Coverage, Modified Condition / 
Decision Coverage, Multiple Condition Coverage
Test C
```
*…excerpt ends here (5293 further characters in the source).*

## index_WithOutPS.pdf

- **Source:** `FrqDepDmpnInrtCmp/utp/Tessy/report/index_WithOutPS.pdf`
- **Format:** `.pdf` (~1903 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `FrqDepDmpnInrtCmp/utp/Tessy/report/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-19, 16:38:41+0530
Project FDD_Inertia
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 7
Successful: 6
Failed: 0
Not Executed: 1
Date: 2014-09-19
Time: 16:38:41+0530
Selected Project Items
Test Object "CBD_UnitTest/FDD_Inertia/ADDCoefCalc"
Test Object "CBD_UnitTest/FDD_Inertia/DecelGain"
Test Object "CBD_UnitTest/FDD_Inertia/DriverVelCalc"
Test Object "CBD_UnitTest/FDD_Inertia/FilterCoefCalc"
Test Object "CBD_UnitTest/FDD_Inertia/FrqDepDmpnInrtCmp_Init"
Test Object "CBD_UnitTest/FDD_Inertia/FrqDepDmpnInrtCmp_Per1"
Test Object "CBD_UnitTest/FDD_Inertia/GenFddIcCmd"
Used Test Envir
```
*…excerpt ends here (5300 further characters in the source).*

## index_WithOutPS_FLTINJ.pdf

- **Source:** `FrqDepDmpnInrtCmp/utp/Tessy/report/index_WithOutPS_FLTINJ.pdf`
- **Format:** `.pdf` (~1961 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `FrqDepDmpnInrtCmp/utp/Tessy/report/index_WithOutPS_FLTINJ.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-19, 17:00:04+0530
Project FDD_Inertia
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 7
Successful: 7
Failed: 0
Not Executed: 0
Date: 2014-09-19
Time: 17:00:04+0530
Selected Project Items
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/ADDCoefCalc"
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/DecelGain"
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/DriverVelCalc"
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/FilterCoefCalc"
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/FrqDepDmpnInrtCmp_Init"
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/FrqDepDmpnInrtCmp_Per1"
Test Object "CBD_UnitTes
```
*…excerpt ends here (5300 further characters in the source).*

## index_WithPS.pdf

- **Source:** `FrqDepDmpnInrtCmp/utp/Tessy/report/index_WithPS.pdf`
- **Format:** `.pdf` (~1904 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `FrqDepDmpnInrtCmp/utp/Tessy/report/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-19, 13:54:55+0530
Project FDD_Inertia
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 7
Successful: 7
Failed: 0
Not Executed: 0
Date: 2014-09-19
Time: 13:54:55+0530
Selected Project Items
Test Object "CBD_UnitTest/FDD_Inertia/ADDCoefCalc"
Test Object "CBD_UnitTest/FDD_Inertia/DecelGain"
Test Object "CBD_UnitTest/FDD_Inertia/DriverVelCalc"
Test Object "CBD_UnitTest/FDD_Inertia/FilterCoefCalc"
Test Object "CBD_UnitTest/FDD_Inertia/FrqDepDmpnInrtCmp_Init"
Test Object "CBD_UnitTest/FDD_Inertia/FrqDepDmpnInrtCmp_Per1"
Test Object "CBD_UnitTest/FDD_Inertia/GenFddIcCmd"
Used Test Envir
```
*…excerpt ends here (5299 further characters in the source).*

## index_WithPS_FLTINJ.pdf

- **Source:** `FrqDepDmpnInrtCmp/utp/Tessy/report/index_WithPS_FLTINJ.pdf`
- **Format:** `.pdf` (~1959 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `FrqDepDmpnInrtCmp/utp/Tessy/report/index_WithPS_FLTINJ.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-19, 15:54:46+0530
Project FDD_Inertia
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 7
Successful: 7
Failed: 0
Not Executed: 0
Date: 2014-09-19
Time: 15:54:46+0530
Selected Project Items
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/ADDCoefCalc"
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/DecelGain"
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/DriverVelCalc"
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/FilterCoefCalc"
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/FrqDepDmpnInrtCmp_Init"
Test Object "CBD_UnitTest/FDD_Inertia_FLTINJ/FrqDepDmpnInrtCmp_Per1"
Test Object "CBD_UnitTes
```
*…excerpt ends here (5300 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `FrqDepDmpnInrtCmp/doc/QAC_Results/Ap_FrqDepDmpnInrtCmp.c.err` (~107 KiB)
- `FrqDepDmpnInrtCmp/doc/QAC_Results/Ap_FrqDepDmpnInrtCmp.c.met` (~771 KiB)

</details>
