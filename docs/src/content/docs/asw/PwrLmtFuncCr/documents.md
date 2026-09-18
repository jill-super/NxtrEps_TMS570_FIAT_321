---
title: "Power Limit Function (Current Mode) documents"
description: "Word/PDF/text documents shipped with PwrLmtFuncCr (Power Limit Function (Current Mode)) and their conversion status."
---

# Power Limit Function (Current Mode) — documents

*Repository directory: `PwrLmtFuncCr`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Power_Limit_Function_CM_Integration_Manual.docx

- **Source:** `PwrLmtFuncCr/doc/Power_Limit_Function_CM_Integration_Manual.docx`
- **Format:** `.docx` (~39 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (3247 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `PwrLmtFuncCr/doc/Power_Limit_Function_CM_Integration_Manual.docx` for those.

```text
Integration Manual - PwrLmtFuncCr
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
< Global function (except the ones that are defined in RTE modules) that is defined in this component but used by other function>
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Ap_PwrLmtFuncCr_Cfg.h
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
PwrLmtFuncCrGeneral/PwrLmtFuncCrCPEnable
Enable checkpoints if needed
PwrLmtFuncCr
DaVinci Interrupt Configuration Changes
ISR Name
VIM #
Priority Dependency
Notes
<Configurator Changes for Interrupts>
Manual Configuration Changes
Constant
Notes
SWC
<Additional configuration changes>
Integration
Required Global Data Inputs
EstKe_VpRadpS_f32
MotorVelMRF_MtrRadpS_f32
PosServEnable_Cnt_lgc
Vecu_Volt_f32
CntDisMtrTrqCmdMRF_MtrNm_f32
AltFaultActive_Cnt_lgc
Required Global Data Outputs
MRFMtrTrqCmd_MtrNm_f32
FltTrqLmt_Uls_f32
ThresholdExceeded_Cnt_lgc
Specific Include Path present
< No >
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
PwrLmtFuncCr_Init1
Called from RTE before first call of periodic function
RTE at init
Runnable
Scheduling Requirements
Trigger
PwrLmtFuncCr_Per1
Not in WARMINIT, OFF, DISABLE
RTE 2ms
PwrLmtFuncCr_Per2
Not in WARMINIT, OFF, DISABLE
RTE 10ms
.
Memory Mapping
Mapping
Memory Section
Contents
Notes
PWRLMTFUNCCR_START_SEC_VAR_CLEARED_32
PWRLMTFUNCCR_START_SEC_VAR_CLEARED_BOOLEAN
PWRLMTFUNCCR_START_SEC_VAR_CLEARED_UNSPECIFIED
RTE_START_SEC_AP_PWRLMTFUNCC
```
*…excerpt ends here (747 further characters in the source).*

## Power_Limit_Function_CM_MDD.docx

- **Source:** `PwrLmtFuncCr/doc/Power_Limit_Function_CM_MDD.docx`
- **Format:** `.docx` (~575 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5993 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `PwrLmtFuncCr/doc/Power_Limit_Function_CM_MDD.docx` for those.

```text
Module – Power Limit Function (Current Mode)
High-Level Description
This module determines an appropriate limit for the system motor torque command based on reasonable output power and system temperature. It also determines to what degree the system command is being limited.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
EstKe_VpRadpS_f32
MRFMtrTrqCmd_MtrNm_f32
MotorVelMRF_MtrRadpS_f32
FltTrqLmt_Uls_f32
PosServEnable_Cnt_lgc
ThresholdExceeded_Cnt_lgc
Vecu_Volt_f32
CntDisMtrTrqCmdMRF_MtrNm_f32
AltFaultActive_Cnt_lgc
NOTE that the PosServEnable_Cnt_lgc input is included because it is listed in the FDD as an input to the component. However, per an FDD note, it is intended for use with functionality that is to be added in some later revision. The input is currently not used.
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
PwrLmtFuncCr_ SpdAdj_MtrRadpS_M_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
PWRLMTFUNCCR_START_SEC_VAR_CLEARED_32
PwrLmtFuncCr_ VoltageRecoveryTimer_mS_M_u32
1
See Data Dictionary
See Data Dictionary
PWRLMTFUNCCR_START_SEC_VAR_CLEARED_32
PwrLmtFuncCr_ ThresholdExceeded_Cnt_M_lgc
N/A
See Data Dictionary
See Data Dictionary
PWRLMTFUNCCR_START_SEC_VAR_CLEARED_BOOLEAN
PwrLmtFuncCr_ TrqLmtKSV_M_str
LPF32KSV_Str
See Data Dictionary
See Data Dictionary
PWRLMTFUNCCR_START_SEC_VAR_CLEARED_UNSPECIFIED
PwrLmtFuncCr_ TrqLmtKSV_M_str.SV_Uls_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
PwrLmtFuncCr_ TrqLmtKSV_M_str.K_Uls_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
PwrLmtFuncCr_ MtrVelKSV_M_str
LPF32KSV_Str
See Data Dictionary
See Data Dictionary
PWRLMTFUNCCR_START_SEC_VAR_CLEARED_UNSPECIFIED
PwrLmtFuncCr_ MtrVelKSV_M_str.SV_Uls_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
PwrLmtFuncCr_ MtrVelKSV_M_str.K_Uls_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
PwrLmtFuncCr_ MtrEnvSpd_MtrRadpS_M_f32
Single Precision Float
See Data Dictionary
See Data Dictionary
PWRLMTFUNCCR_START_SEC_VAR_CLEARED_32
PwrL
```
*…excerpt ends here (3493 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `PwrLmtFuncCr/doc/QAC_Results/Ap_PwrLmtFuncCr.c.err` (~106 KiB)
- `PwrLmtFuncCr/doc/QAC_Results/Ap_PwrLmtFuncCr.c.met` (~768 KiB)

</details>
