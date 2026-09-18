---
title: "Common Motor Current Measurement documents"
description: "Word/PDF/text documents shipped with CmMtrCurr (Common Motor Current Measurement) and their conversion status."
---

# Common Motor Current Measurement — documents

*Repository directory: `CmMtrCurr`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## CmMtrCurr_Integration_Manual.docx

- **Source:** `CmMtrCurr/doc/CmMtrCurr_Integration_Manual.docx`
- **Format:** `.docx` (~41 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (3597 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `CmMtrCurr/doc/CmMtrCurr_Integration_Manual.docx` for those.

```text
Integration Manual –CmMtrCurr
Table of Contents
1Dependencies2
1.1SWCs2
1.2Functions to be provided to Integration Project2
2Configuration3
2.1Build Time Config3
2.2Configuration Files to be provided by Integration Project3
2.2.1Da Vinci Config Configuration Changes3
2.2.2Manual Configuration Changes3
3Integration5
3.1Required Global Data Inputs5
3.2Required Global Output Inputs5
3.3Specific Include Path present5
4Runnable Scheduling6
5Memory Mapping7
5.1Mapping7
5.2Usage7
5.3RTE NvM Blocks7
5.4Non RTE NvM Blocks7
6Compiler Settings7
6.1Preprocessor MACRO7
6.2Optimization Settings7
7Revision Control Log8
Dependencies
SWCs
Module
Required Feature
For version ES01 -008 or more
ADC 33E v3 or more
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Functions to be provided to Integration Project
CurrDQPer1
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
CmMtrCurr_Cfg.h ( Refer CmMtrCurr_Cfg_Template.h in tools folder)
(Data synchronization must be provided at the integration level between 2 ms periodic and Motor Control ISR Periodic’s)
Outputs from the CmMtrCurr (Motor Control ISR) periodic must be synchronized with the outputs from Motor position.
Da Vinci Config Configuration Changes
Constant
Notes
SWC
MTRCURRPHASEBC
PhaseB and Phase C used in Curr Measurement
MTRCURRPHASECB
PhaseC and Phase B used in Curr Measurement
MTRCURRPHASEAC
PhaseA and Phase C used in Curr Measurement
MTRCURRPHASECA
PhaseC and Phase A used in Curr Measurement
MTRCURRPHASEAB
PhaseA and Phase B used in Curr Measurement
MTRCURRPHASEBA
PhaseB and Phase A used in Curr Measurement
Note: Only one of the configuration can be selected based on the requirements. Make sure order matches oreder in ADC data read ie MTRCURRPHASEBC - “BC” represents current_1 is phase B and current_2 is phase C .
Manual Configuration Changes
Constant
Notes
SWC
none
Integration
Required Global Data Inputs
ADC2OffsetComp_Cnt_u8p8 ( mapped from ADC Configuration 33E)
For other inputs. Refer the template in tools folder of this component
Required Global Output Inputs
For other inputs. Refer the template in tools folder of this component
Specific Include Path present
Yes
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
CmMtrCurr_Init
None
RTE
Runnable
Scheduling R
```
*…excerpt ends here (1097 further characters in the source).*

## CmMtrCurr_MDD.docx

- **Source:** `CmMtrCurr/doc/CmMtrCurr_MDD.docx`
- **Format:** `.docx` (~1609 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5996 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `CmMtrCurr/doc/CmMtrCurr_MDD.docx` for those.

```text
Module -- CmMtrCurr
High-Level Description
The Current Measurement function is responsible for measuring the motor phase currents used as feedback by the Motor Control FDD. Two motor phase currents are measured using a shunt resistor and a differential amplifier circuitry, and along with the motor position are transformed into direct (D) and quadrature (Q) axes currents using the combined Clarke/Park transform
UNIT Test Notes:
Unit test should be done with enabling one of the six predefned macro MTRCURRPHASEBC, MTRCURRPHASECB, MTRCRRPHASECA, MTRCURRPHASEAB, MTRCURRPHASEAC, MTRCURRPHASEBA. Hence it should have six UTP results (one for each Macro enabled).
Figures
Component diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
ADCMtrCurr1_Volt_f32
MtrCurrQax_Amps_f32
ADCMtrCurr2_Volt_f32
MtrCurrDax_Amps_f32
MtrVel_MtrRadpS_f32
CurrentGainSvc_Cnt_lgc
FiltCntrlTemp_DegC_f32
ComOffset_Cnt_u16
MtrCurrAngle_Rev_f32
ElecPosDelayComp_Rad_f32
VehSpd_Kph_f32
CorrMtrCurrPosition_Rev_f32
VhSpdValid_Cnt_lgc
MtrCurrK1_Amps_f32
Vecu_Volt_f32
MtrCurrK2_Amps_f32
MtrCurr1TempOffset_Volt_f32
MtrCurr1_Volts_f32
MtrCurr2TempOffset_Volt_f32
MtrCurr2_Volts_f32
Phs1Curr_Cnt_u16
MtrCurrQax_Amps_f32
Phs2Curr_Cnt_u16
MtrCurrDax_Amps_f32
MtrElecPol_Cnt_s08
CurrentGainSvc_Cnt_lgc
DCPhsBComp_Cnt_u16
DCPhsCComp_Cnt_u16
DCPhsCComp_Cnt_u16
DCPhsBComp_Cnt_u16
DCPhsAComp_Cnt_u16
DCPhsBComp_Cnt_u16
DCPhsBComp_Cnt_u16
DCPhsAComp_Cnt_u16
DCPhsAComp_Cnt_u16
DCPhsCComp_Cnt_u16
DCPhsCComp_Cnt_u16
DCPhsAComp_Cnt_u16
ADC2OffsetComp_Cnt_u8p8
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
CmMtrCurr_CorrMtrCurr1_Amp_D_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
CMMTRCURR_START_SEC_VAR_CLEARED_32
CmMtrCurr_CorrMtrCurr2_Amp_D_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
CMMTRCURR_START_SEC_VAR_CLEARED_32
CmMtrCurr_CurrVectPosition_Rev_D_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
CMMTRCURR_START_SEC_VAR_CLEARED_32
CmMtrCurr_VectPosCosTheta_Uls_D_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
CMMTRCUR
```
*…excerpt ends here (3496 further characters in the source).*

## CmMtrCurr_MTRCURRPHASEAB_ON_UnitTestReport_WithOutPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEAB_ON_UnitTestReport_WithOutPS_PIL.pdf`
- **Format:** `.pdf` (~3117 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEAB_ON_UnitTestReport_WithOutPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-24, 12:06:11+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-24
Time: 12:06:11+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAB_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAB_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAB_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAB_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAB_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## CmMtrCurr_MTRCURRPHASEAB_ON_UnitTestReport_WithPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEAB_ON_UnitTestReport_WithPS_PIL.pdf`
- **Format:** `.pdf` (~3117 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEAB_ON_UnitTestReport_WithPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-24, 12:30:13+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-24
Time: 12:30:13+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAB_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAB_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAB_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAB_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAB_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## CmMtrCurr_MTRCURRPHASEAC_ON_UnitTestReport_WithOutPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEAC_ON_UnitTestReport_WithOutPS_PIL.pdf`
- **Format:** `.pdf` (~3009 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEAC_ON_UnitTestReport_WithOutPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-23, 17:58:07+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-23
Time: 17:58:07+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAC_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAC_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAC_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAC_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAC_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## CmMtrCurr_MTRCURRPHASEAC_ON_UnitTestReport_WithPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEAC_ON_UnitTestReport_WithPS_PIL.pdf`
- **Format:** `.pdf` (~3009 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEAC_ON_UnitTestReport_WithPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-24, 12:54:17+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-24
Time: 12:54:17+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAC_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAC_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAC_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAC_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEAC_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## CmMtrCurr_MTRCURRPHASEBA_ON_UnitTestReport_WithOutPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEBA_ON_UnitTestReport_WithOutPS_PIL.pdf`
- **Format:** `.pdf` (~3011 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEBA_ON_UnitTestReport_WithOutPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-23, 18:33:18+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-23
Time: 18:33:18+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBA_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBA_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBA_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBA_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBA_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## CmMtrCurr_MTRCURRPHASEBA_ON_UnitTestReport_WithPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEBA_ON_UnitTestReport_WithPS_PIL.pdf`
- **Format:** `.pdf` (~3013 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEBA_ON_UnitTestReport_WithPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-24, 13:14:20+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-24
Time: 13:14:20+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBA_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBA_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBA_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBA_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBA_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## CmMtrCurr_MTRCURRPHASEBC_ON_UnitTestReport_WithOutPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEBC_ON_UnitTestReport_WithOutPS_PIL.pdf`
- **Format:** `.pdf` (~3015 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEBC_ON_UnitTestReport_WithOutPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-23, 19:08:39+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-23
Time: 19:08:39+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBC_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBC_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBC_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBC_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBC_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## CmMtrCurr_MTRCURRPHASEBC_ON_UnitTestReport_WithPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEBC_ON_UnitTestReport_WithPS_PIL.pdf`
- **Format:** `.pdf` (~3016 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASEBC_ON_UnitTestReport_WithPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-24, 13:55:12+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-24
Time: 13:55:12+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBC_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBC_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBC_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBC_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASEBC_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## CmMtrCurr_MTRCURRPHASECA_ON_UnitTestReport_WithOutPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASECA_ON_UnitTestReport_WithOutPS_PIL.pdf`
- **Format:** `.pdf` (~3009 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASECA_ON_UnitTestReport_WithOutPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-23, 19:42:29+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-23
Time: 19:42:29+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECA_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECA_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECA_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECA_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECA_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## CmMtrCurr_MTRCURRPHASECA_ON_UnitTestReport_WithtPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASECA_ON_UnitTestReport_WithtPS_PIL.pdf`
- **Format:** `.pdf` (~3011 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASECA_ON_UnitTestReport_WithtPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-24, 14:12:48+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-24
Time: 14:12:48+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECA_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECA_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECA_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECA_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECA_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## CmMtrCurr_MTRCURRPHASECB_ON_UnitTestReport_WithOutPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASECB_ON_UnitTestReport_WithOutPS_PIL.pdf`
- **Format:** `.pdf` (~3011 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASECB_ON_UnitTestReport_WithOutPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-24, 11:45:05+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-24
Time: 11:45:05+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECB_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECB_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECB_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECB_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECB_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## CmMtrCurr_MTRCURRPHASECB_ON_UnitTestReport_WithPS_PIL.pdf

- **Source:** `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASECB_ON_UnitTestReport_WithPS_PIL.pdf`
- **Format:** `.pdf` (~3010 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `CmMtrCurr/utp/Tessy/report/CmMtrCurr_MTRCURRPHASECB_ON_UnitTestReport_WithPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-24, 14:31:04+0530
Project CmMtrCurr1
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 12
Successful: 12
Failed: 0
Not Executed: 0
Date: 2016-07-24
Time: 14:31:04+0530
Selected Project Items
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECB_ON/CmMtrCurr_Init"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECB_ON/CmMtrCurr_Per1"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECB_ON/CmMtrCurr_Per2"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECB_ON/CmMtrCurr_Per3"
Test Object "CBD_UnitTest/CmMtrCurr_MTRCURRPHASECB_ON/CmMtrCurr_SCom_CalGain"
Test Object "CBD_UnitTest/CmMtrCurr_M
```
*…excerpt ends here (5299 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `CmMtrCurr/doc/QAC_Results/Sa_CmMtrCurr.c.err` (~112 KiB)
- `CmMtrCurr/doc/QAC_Results/Sa_CmMtrCurr.c.met` (~731 KiB)

</details>
