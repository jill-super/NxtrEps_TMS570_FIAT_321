---
title: "Damping Firewall documents"
description: "Word/PDF/text documents shipped with DampingFirewall (Damping Firewall) and their conversion status."
---

# Damping Firewall — documents

*Repository directory: `DampingFirewall`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## DampingFirewall_IntegrationManual.docx

- **Source:** `DampingFirewall/doc/DampingFirewall_IntegrationManual.docx`
- **Format:** `.docx` (~78 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (3438 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DampingFirewall/doc/DampingFirewall_IntegrationManual.docx` for those.

```text
Integration Manual
For
Damping Firewall
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
SF35 Damping Firewall
011
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
Ap_DampingFirewall_Cfg.h for checkpoint enable
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
DampingFirewallGeneral/DampingFirewallCPEnable
To enable checkpoints
DampingFirewall
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
AsstFirewallActive_Uls_f32
DampingCmd_MtrNm_f32
HwTorque_HwNm_f32
InertiaComp_MtrNm_f32
MtrVelCRF_MtrRadpS_f32
VehicleSpeed_Kph_f32
VehicleLonAccel_KphpS_f32
BaseAssistCmd_MtrNm_f32
WIRCmdAmpBlnd_MtrNm_f32
FreqDepDmpSrlComSvcDft_Cnt_lgc
Defeat_Damping_Svc_Cnt_lgc
MEC_Counter_Cnt_enum
Required Global Data Outputs
CombinedDamping_MtrNm_f32
Specific Include Path present
No
Runnable Scheduling
This section specifies t
```
*…excerpt ends here (938 further characters in the source).*

## Damping_Firewall_MDD.doc

- **Source:** `DampingFirewall/doc/Damping_Firewall_MDD.doc`
- **Format:** `.doc` (~5409 KiB)
- **Kind:** Module design document (MDD)
- **Status:** summary record — legacy binary source retained at `DampingFirewall/doc/Damping_Firewall_MDD.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **Damping_Firewall_MDD.doc** module design document specifies the `DampingFirewall` software component: requirements, interfaces/ports, internal behaviour, calibration and diagnostics. It is the normative reference for the implementation in `DampingFirewall/src/`; the module page lists the files it governs.

## index_WithOutPS.pdf

- **Source:** `DampingFirewall/utp/Tessy/report/index_WithOutPS.pdf`
- **Format:** `.pdf` (~4566 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DampingFirewall/utp/Tessy/report/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-06, 17:13:08+0530
Project DampingFirewall_SF35_014.0_NoUTP
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 6
Successful: 1
Failed: 5
Not Executed: 0
Date: 2016-07-06
Time: 17:13:08+0530
Selected Project Items
Test Object "CBD_UnitTest/DampingFirewall/ADDCoefCalc"
Test Object "CBD_UnitTest/DampingFirewall/DampingFirewall_Init1"
Test Object "CBD_UnitTest/DampingFirewall/DampingFirewall_Per1"
Test Object "CBD_UnitTest/DampingFirewall/DriverVelCalc"
Test Object "CBD_UnitTest/DampingFirewall/FilterCoefCalc"
Test Object "CBD_UnitTest/DampingFirewall/GenFddIcCmd"
Used Test Environment
```
*…excerpt ends here (5300 further characters in the source).*

## index_WithPS.pdf

- **Source:** `DampingFirewall/utp/Tessy/report/index_WithPS.pdf`
- **Format:** `.pdf` (~4562 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `DampingFirewall/utp/Tessy/report/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-07-06, 15:29:56+0530
Project DampingFirewall_SF35_014.0_NoUTP
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 6
Successful: 1
Failed: 5
Not Executed: 0
Date: 2016-07-06
Time: 15:29:56+0530
Selected Project Items
Test Object "CBD_UnitTest/DampingFirewall/ADDCoefCalc"
Test Object "CBD_UnitTest/DampingFirewall/DampingFirewall_Init1"
Test Object "CBD_UnitTest/DampingFirewall/DampingFirewall_Per1"
Test Object "CBD_UnitTest/DampingFirewall/DriverVelCalc"
Test Object "CBD_UnitTest/DampingFirewall/FilterCoefCalc"
Test Object "CBD_UnitTest/DampingFirewall/GenFddIcCmd"
Used Test Environment
```
*…excerpt ends here (5300 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `DampingFirewall/doc/QAC_Results/Ap_DampingFirewall.c.err` (~180 KiB)
- `DampingFirewall/doc/QAC_Results/Ap_DampingFirewall.c.met` (~800 KiB)

</details>
