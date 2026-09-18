---
title: "Motor Velocity Sensing (Digital) documents"
description: "Word/PDF/text documents shipped with MtrVel_Digi (Motor Velocity Sensing (Digital)) and their conversion status."
---

# Motor Velocity Sensing (Digital) — documents

*Repository directory: `MtrVel_Digi`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Motor Velocity_Integration_Manual.docx

- **Source:** `MtrVel_Digi/doc/Motor Velocity_Integration_Manual.docx`
- **Format:** `.docx` (~33 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (3723 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `MtrVel_Digi/doc/Motor Velocity_Integration_Manual.docx` for those.

```text
Integration Manual –Motor Velocity
Table of Contents
1Dependencies2
1.1SWCs2
1.2Functions to be provided to Integration Project2
2Configuration3
2.1Build Time Config3
2.2Configuration Files to be provided by Integration Project3
2.2.1Da Vinci Config Configuration Changes3
2.2.2Manual Configuration Changes3
3Integration4
3.1Required Global Data Inputs4
3.2Specific Include Path present4
4Runnable Scheduling5
5Memory Mapping5
5.1Mapping5
5.2Usage6
5.3RTE NvM Blocks6
5.4Non RTE NvM Blocks6
6Compiler Settings6
6.1Preprocessor MACRO6
6.2Optimization Settings6
7Revision Control Log7
Dependencies
SWCs
Module
Required Feature
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Functions to be provided to Integration Project
MtrVel3_Per1
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
MtrVel_Cfg.h (Refer MtrVel_Cfg_Template.h in tools folder)
Da Vinci Config Configuration Changes
Constant
Notes
SWC
None
Manual Configuration Changes
Constant
Notes
SWC
None
D_MTRVELOSBUFSZ_CNT_U08
D_MTRVELOSBUFSZ_CNT_U08” is defined as Cal “k_BuffSize_Cnt” in SF40AB
Confirm with the Program being integrated on for the value that needs to be configured for this constant
Integration
Required Global Data Inputs
Motor Position calculated in Motor Control ISR should be used. Motor Position Non RTE inputs should be processed at the same time rate of Motor Velocity Buffering Periodic
MtrVel_Read_MechMtrPos1TimeStamp_uS_u32 /* MtrPos Timestamp Calculated in 0.062 mSec should be used. Motor Pos should be processed at the same time rate of Motor Velocity 3 periodic 1*/
MtrVel_Read_MechMtrPos1_Rev_u0p16 /* MtrPos Calculated in 0.062 mSec should be used. Motor Pos should be processed at the same time rate of Motor Velocity 3 periodic 1 */
Specific Include Path present
Yes
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
MtrVel3_Init1
Once
RTE
MtrVel_Init
Once
RTE
MtrVel2_Init
Once
RTE
Runnable
Scheduling Requirements
Trigger
MtrVel3_Per1
After DigMSBCorrPer1 Motor ISR periodic (ES51 )
Motor Control ISR
MtrVel_Per1
After DigMSBCorr Per2 periodic (ES51 )
RTE(2mS)
MtrVel_Per2
RTE(2mS)
MtrVel2_Per1
RTE(2mS)
MtrVel2_Per2
RTE(2mS)
Note : The Scheduling of the periodic between MtrVel_Per1, MtrVel_Per2, MtrVel2_Per1 should take care of the followin
```
*…excerpt ends here (1223 further characters in the source).*

## MotorVelocity2_MDD.doc

- **Source:** `MtrVel_Digi/doc/MotorVelocity2_MDD.doc`
- **Format:** `.doc` (~752 KiB)
- **Kind:** Module design document (MDD)
- **Status:** summary record — legacy binary source retained at `MtrVel_Digi/doc/MotorVelocity2_MDD.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **MotorVelocity2_MDD.doc** module design document specifies the `MtrVel_Digi` software component: requirements, interfaces/ports, internal behaviour, calibration and diagnostics. It is the normative reference for the implementation in `MtrVel_Digi/src/`; the module page lists the files it governs.

## MotorVelocity3_MDD.doc

- **Source:** `MtrVel_Digi/doc/MotorVelocity3_MDD.doc`
- **Format:** `.doc` (~217 KiB)
- **Kind:** Module design document (MDD)
- **Status:** summary record — legacy binary source retained at `MtrVel_Digi/doc/MotorVelocity3_MDD.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **MotorVelocity3_MDD.doc** module design document specifies the `MtrVel_Digi` software component: requirements, interfaces/ports, internal behaviour, calibration and diagnostics. It is the normative reference for the implementation in `MtrVel_Digi/src/`; the module page lists the files it governs.

## MotorVelocity_MDD.doc

- **Source:** `MtrVel_Digi/doc/MotorVelocity_MDD.doc`
- **Format:** `.doc` (~1606 KiB)
- **Kind:** Module design document (MDD)
- **Status:** summary record — legacy binary source retained at `MtrVel_Digi/doc/MotorVelocity_MDD.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **MotorVelocity_MDD.doc** module design document specifies the `MtrVel_Digi` software component: requirements, interfaces/ports, internal behaviour, calibration and diagnostics. It is the normative reference for the implementation in `MtrVel_Digi/src/`; the module page lists the files it governs.

## index_WithOutPS.pdf

- **Source:** `MtrVel_Digi/utp/Tessy/report/MtrVel_Digi/index_WithOutPS.pdf`
- **Format:** `.pdf` (~1417 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `MtrVel_Digi/utp/Tessy/report/MtrVel_Digi/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-12-26, 17:52:10+0530
Project MtrVel_Digi
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 6
Successful: 6
Failed: 0
Not Executed: 0
Date: 2014-12-26
Time: 17:52:10+0530
Selected Project Items
Test Object "CBD_UnitTest/MtrVel_Digi/CalcCoarseVel"
Test Object "CBD_UnitTest/MtrVel_Digi/MtrVel_Init"
Test Object "CBD_UnitTest/MtrVel_Digi/MtrVel_Per1"
Test Object "CBD_UnitTest/MtrVel_Digi/MtrVel_Per2"
Test Object "CBD_UnitTest/MtrVel_Digi/MtrVelBlend"
Test Object "CBD_UnitTest/MtrVel_Digi/RegressionFit"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Inte
```
*…excerpt ends here (5300 further characters in the source).*

## index_WithPS.pdf

- **Source:** `MtrVel_Digi/utp/Tessy/report/MtrVel_Digi/index_WithPS.pdf`
- **Format:** `.pdf` (~1416 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `MtrVel_Digi/utp/Tessy/report/MtrVel_Digi/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-12-26, 16:53:07+0530
Project MtrVel_Digi
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 6
Successful: 6
Failed: 0
Not Executed: 0
Date: 2014-12-26
Time: 16:53:07+0530
Selected Project Items
Test Object "CBD_UnitTest/MtrVel_Digi/CalcCoarseVel"
Test Object "CBD_UnitTest/MtrVel_Digi/MtrVel_Init"
Test Object "CBD_UnitTest/MtrVel_Digi/MtrVel_Per1"
Test Object "CBD_UnitTest/MtrVel_Digi/MtrVel_Per2"
Test Object "CBD_UnitTest/MtrVel_Digi/MtrVelBlend"
Test Object "CBD_UnitTest/MtrVel_Digi/RegressionFit"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Inte
```
*…excerpt ends here (5300 further characters in the source).*

## index_WithOutPS.pdf

- **Source:** `MtrVel_Digi/utp/Tessy/report/MtrVel_Digi2/index_WithOutPS.pdf`
- **Format:** `.pdf` (~684 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `MtrVel_Digi/utp/Tessy/report/MtrVel_Digi2/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2015-01-08, 12:30:13+0530
Project MtrVel_Digi
© Report created by TESSY V3.1.9, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 3
Successful: 3
Failed: 0
Not Executed: 0
Date: 2015-01-08
Time: 12:30:13+0530
Selected Project Items
Test Object "CBD_UnitTest/MtrVel2/MtrVel2_Init"
Test Object "CBD_UnitTest/MtrVel2/MtrVel2_Per1"
Test Object "CBD_UnitTest/MtrVel2/MtrVel2_Per2"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: Yes
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Statement Coverage, Branch Coverage, Decision Cov
```
*…excerpt ends here (5298 further characters in the source).*

## index_WithPS.pdf

- **Source:** `MtrVel_Digi/utp/Tessy/report/MtrVel_Digi2/index_WithPS.pdf`
- **Format:** `.pdf` (~685 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `MtrVel_Digi/utp/Tessy/report/MtrVel_Digi2/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2015-01-08, 10:35:56+0530
Project MtrVel_Digi
© Report created by TESSY V3.1.9, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 3
Successful: 3
Failed: 0
Not Executed: 0
Date: 2015-01-08
Time: 10:35:56+0530
Selected Project Items
Test Object "CBD_UnitTest/MtrVel2/MtrVel2_Init"
Test Object "CBD_UnitTest/MtrVel2/MtrVel2_Per1"
Test Object "CBD_UnitTest/MtrVel2/MtrVel2_Per2"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: Yes
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Statement Coverage, Branch Coverage, Decision Cov
```
*…excerpt ends here (5298 further characters in the source).*

## Static-analysis outputs (6 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `MtrVel_Digi/doc/QAC_Results/Sa_MtrVel.c.err` (~110 KiB)
- `MtrVel_Digi/doc/QAC_Results/Sa_MtrVel.c.met` (~1049 KiB)
- `MtrVel_Digi/doc/QAC_Results/Sa_MtrVel2.c.err` (~111 KiB)
- `MtrVel_Digi/doc/QAC_Results/Sa_MtrVel2.c.met` (~1013 KiB)
- `MtrVel_Digi/doc/QAC_Results/Sa_MtrVel3.c.err` (~15 KiB)
- `MtrVel_Digi/doc/QAC_Results/Sa_MtrVel3.c.met` (~975 KiB)

</details>
