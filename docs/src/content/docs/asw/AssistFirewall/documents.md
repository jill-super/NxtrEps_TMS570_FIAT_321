---
title: "Assist Firewall documents"
description: "Word/PDF/text documents shipped with AssistFirewall (Assist Firewall) and their conversion status."
---

# Assist Firewall — documents

*Repository directory: `AssistFirewall`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## AssistFirewall_IntegrationManual.docx

- **Source:** `AssistFirewall/doc/AssistFirewall_IntegrationManual.docx`
- **Format:** `.docx` (~39 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2699 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `AssistFirewall/doc/AssistFirewall_IntegrationManual.docx` for those.

```text
Integration Manual –AssistFirewall
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
3Integration Dataflow Requirements4
3.1Required Global Data Inputs4
3.2Required Global Data Outputs4
3.3Specific Include Path present4
4Runnable Scheduling5
5Memory Mapping6
5.1Mapping6
5.2Usage6
5.3Non RTE NvM Blocks6
5.4RTE NvM Blocks6
6Compiler Settings7
6.1Preprocessor MACRO7
6.2Optimization Settings7
7Revision Control Log8
Dependencies
SWCs
Module
Required Feature
None
Note: Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.
Global Functions (Non RTE) to be provided to Integration Project
None
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Ap_AssistFirewall_Cfg.h for checkpoint enable
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
AssistFirewallGeneral/AssistFirewallCPEnable
To enable checkpoints
AssistFirewall
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
Integration Dataflow Requirements
Required Global Data Inputs
BaseAssistCmd_MtrNm_f32
Defeat_AsstTbl_Service_Cnt_lgc
HighFreqAssist_MtrNm_f32
HwTorque_HwNm_f32
HysteresisComp_MtrNm_f32
MEC_Counter_Cnt_enum
VehicleSpeed_Kph_f32
Required Global Data Outputs
AsstFirewallActive_Uls_f32
CombinedAssist_MtrNm_f32
Specific Include Path present
No
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
AssistFirewall_Init
On Rte_Init
Runnable
Scheduling Requirements
Trigger
AssistFirewall_Per1
triggered on TimingEvent
Disabled in WARMINIT and OFF
2ms
Memory Mapping
Mapping
Memory Section
Contents
Notes
ASSISTFIREWALL_START_SEC_VAR_CLEARED_32
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.
Usage
Feature
RAM
ROM
None
Table 1: ARM Cortex R4 Memory Usage
Non RTE NvM Blocks
Block Name
None
Note: Size of the NVM block if configured in developer
RTE NvM Blocks
Block Name
None
Note: Size of the NVM block if configured in deve
```
*…excerpt ends here (199 further characters in the source).*

## Assist_Firewall_MDD.docx

- **Source:** `AssistFirewall/doc/Assist_Firewall_MDD.docx`
- **Format:** `.docx` (~431 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5996 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `AssistFirewall/doc/Assist_Firewall_MDD.docx` for those.

```text
Module -- Assist Firewall
High-Level Description
This module limits the output from the Assist module according to safety requirements.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
BaseAssistCmd_MtrNm_f32
AsstFirewallActive_Uls_f32
HighFreqAssist_MtrNm_f32
CombinedAssist_MtrNm_f32
HwTorque_HwNm_f32
HysteresisComp_MtrNm_f32
VehicleSpeed_Kph_f32
Defeat_AsstTbl_Service_Cnt_lgc
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
AssistFirewall_UprBoundKSV_M_str
See Data Dictionary
See Data Dictionary
See Data Dictionary
ASSISTFIREWALL_START_SEC_VAR_CLEARED_UNSPECIFIED
AssistFirewall_LwrBoundKSV_M_str
See Data Dictionary
See Data Dictionary
See Data Dictionary
ASSISTFIREWALL_START_SEC_VAR_CLEARED_UNSPECIFIED
AssistFirewall_HiFreqKSV_M_str
See Data Dictionary
See Data Dictionary
See Data Dictionary
ASSISTFIREWALL_START_SEC_VAR_CLEARED_UNSPECIFIED
AssistFirewall_ActiveKSV_M_str
See Data Dictionary
See Data Dictionary
See Data Dictionary
ASSISTFIREWALL_START_SEC_VAR_CLEARED_UNSPECIFIED
AssistFirewall_ActiveRawAcc_Cnt_M_u16
See Data Dictionary
See Data Dictionary
See Data Dictionary
ASSISTFIREWALL_START_SEC_VAR_CLEARED_16
AssistFirewall_PNCountStatus_Cnt_M_lgc
See Data Dictionary
See Data Dictionary
See Data Dictionary
ASSISTFIREWALL_START_SEC_VAR_CLEARED_ BOOLEAN
AssistFirewall_AsstFWUprBound_MtrNm_D_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
ASSISTFIREWALL_START_SEC_VAR_CLEARED_32
AssistFirewall_AsstFWLwrBound_MtrNm_D_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
ASSISTFIREWALL_START_SEC_VAR_CLEARED_32
AssistFirewall_AsstFWSumInput_MtrNm_D_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
ASSISTFIREWALL_START_SEC_VAR_CLEARED_32
AssistFirewall_AsstFWLowFreqInput_MtrNm_D_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
ASSISTFIREWALL_START_SEC_VAR_CLEARED_32
AssistFirewall_AsstFWLowFreqLimited_MtrNm_D_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
ASSISTFIREWALL_START_SEC_VAR_CLEARED_32
AssistFirewall_AsstFWAc
```
*…excerpt ends here (3496 further characters in the source).*

## index_WithOutPS.pdf

- **Source:** `AssistFirewall/utp/Tessy/report/index_WithOutPS.pdf`
- **Format:** `.pdf` (~2006 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5997 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `AssistFirewall/utp/Tessy/report/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2015-03-23, 11:57:26+0530
Project AssistFirewall
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 2
Successful: 2
Failed: 0
Not Executed: 0
Date: 2015-03-23
Time: 11:57:26+0530
Selected Project Items
Test Object "CBD_UnitTest/AssistFireWall/AssistFirewall_Init1"
Test Object "CBD_UnitTest/AssistFireWall/AssistFirewall_Per1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test 
object on the y axis. Each bar is divided into passed
```
*…excerpt ends here (5297 further characters in the source).*

## index_WithPS.pdf

- **Source:** `AssistFirewall/utp/Tessy/report/index_WithPS.pdf`
- **Format:** `.pdf` (~2005 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5997 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `AssistFirewall/utp/Tessy/report/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2015-03-23, 11:41:07+0530
Project AssistFirewall
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 2
Successful: 2
Failed: 0
Not Executed: 0
Date: 2015-03-23
Time: 11:41:07+0530
Selected Project Items
Test Object "CBD_UnitTest/AssistFireWall/AssistFirewall_Init1"
Test Object "CBD_UnitTest/AssistFireWall/AssistFirewall_Per1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test 
object on the y axis. Each bar is divided into passed
```
*…excerpt ends here (5297 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `AssistFirewall/doc/QAC_Results/Ap_AssistFirewall.c.err` (~109 KiB)
- `AssistFirewall/doc/QAC_Results/Ap_AssistFirewall.c.met` (~964 KiB)

</details>
