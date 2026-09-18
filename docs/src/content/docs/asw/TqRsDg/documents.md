---
title: "Torque Reasonableness Diagnostics documents"
description: "Word/PDF/text documents shipped with TqRsDg (Torque Reasonableness Diagnostics) and their conversion status."
---

# Torque Reasonableness Diagnostics — documents

*Repository directory: `TqRsDg`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## TorqueReasonableDiagnostics.docx

- **Source:** `TqRsDg/doc/TorqueReasonableDiagnostics.docx`
- **Format:** `.docx` (~247 KiB)
- **Kind:** Supporting document
- **Status:** converted — text extracted from the binary (5995 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TqRsDg/doc/TorqueReasonableDiagnostics.docx` for those.

```text
Module – Torque Reasonable Diagnostics
High-Level Description
The Torque Reasonableness Diagnostic compares the commanded electromagnetic motor torque (calculated from the commanded Iq and Id currents) to the measured electromagnetic torque (calculated from the measured Iq and Id currents) and sets a diagnostic flag when the error is outside of calibration boundaries for calibration time periods. This diagnostic is intended to trip due to a variety of possible errors within the closed loop control of the motor control, including but not exclusive to certain current measurement errors and output drive errors.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
DervLambdaAlphaDiag_Volt_f32
DervLambdaBetaDiag_Volt_f32
OutputRampMult_Uls_f32
TrqLimitMin_MtrNm_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
TqRsDg_AlpaCurrDiagPrimLPF_M_Str
LPF32KSV_Str
See data dictionary
See data dictionary
TQRSDG_START_SEC_VAR_NOINIT_UNSPECIFIED
TqRsDg_BetaCurrDiagPrimLPF_M_Str
LPF32KSV_Str
See data dictionary
See data dictionary
TQRSDG_START_SEC_VAR_NOINIT_UNSPECIFIED
TqRsDg_AlpaCurrDiagSecLPF_M_Str
LPF32KSV_Str
See data dictionary
See data dictionary
TQRSDG_START_SEC_VAR_NOINIT_UNSPECIFIED
TqRsDg_BetaCurrDiagSecLPF_M_Str
LPF32KSV_Str
See data dictionary
See data dictionary
TQRSDG_START_SEC_VAR_NOINIT_UNSPECIFIED
TqRsDg_CurrDiagPrimPNAccum_Cnt_M_u16
1
See data dictionary
See data dictionary
TQRSDG_START_SEC_VAR_CLEARED_16
TqRsDg_CurrDiagSecPNAccum_Cnt_M_u16
1
See data dictionary
See data dictionary
TQRSDG_START_SEC_VAR_CLEARED_16
TqRsDg_DervLambdaAlphaDiagPrimFilt_Volt_D_f32
Single precision float
See data dictionary
See data dictionary
TQRSDG_START_SEC_VAR_CLEARED_32
TqRsDg_DervLambdaBetaDiagPrimFilt_Volt_D_f32
Single precision float
See data dictionary
See data dictionary
TQRSDG_START_SEC_VAR_CLEARED_32
TqRsDg_DervLambdaAlphaDiagSecFilt_Volt_D_f32
Single precision float
See data dictionary
See data dictionary
TQRSDG_START_SEC_VAR_CLEARED_32
TqRsDg_DervLambdaBetaDiagSecFilt_Volt_D_f32
Single precision float
See data dicti
```
*…excerpt ends here (3495 further characters in the source).*

## TrqReasonableness_Integration_Manual.docx

- **Source:** `TqRsDg/doc/TrqReasonableness_Integration_Manual.docx`
- **Format:** `.docx` (~40 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2697 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TqRsDg/doc/TrqReasonableness_Integration_Manual.docx` for those.

```text
Integration Manual –TqRsDg
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
None
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
None
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Ap_TqRsDg_Cfg.h generated by Ap_TqRsDg_Cfg.h.tt
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
TqRsDgGeneral/TqRsDgCPEnable
To enable checkpoints
TqRsDg
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
Integration
Required Global Data Inputs
DervLambdaAlphaDiag_Volt_f32
DervLambdaBetaDiag_Volt_f32
OutputRampMult_Uls_f32
TrqLimitMin_MtrNm_f32
Required Global Data Outputs
Specific Include Path present
No
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
TqRsDg _Init1
Called from RTE before any call to the periodic functions
RTE init
Runnable
Scheduling Requirements
Trigger
TqRsDg_Per1
Must run after CmMtrCurr_Per2
and before CurrCmd_Per1
RTE (2ms)
.
Memory Mapping
Mapping
Memory Section
Contents
Notes
TQRSDG_START_SEC_VAR_CLEARED_32
TQRSDG_START_SEC_VAR_NOINIT_UNSPECIFIED
TQRSDG_START_SEC_VAR_CLEARED_16
RTE_START_SEC_AP_TQRSDG_APPL_CODE
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.
Usage
Feature
RAM
ROM
<Memmap usuage info>
Table 1: ARM Cortex R4 Memory Usage
Non RTE NvM Blocks
Block Name
None
Note : Size of the NVM block if configured in developer
RTE NvM Blocks
Block Name
Note : Size of the NVM block if configured in developer
Compiler Settings
Prepro
```
*…excerpt ends here (197 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `TqRsDg/doc/QAC_Results/Ap_TqRsDg.c.err` (~106 KiB)
- `TqRsDg/doc/QAC_Results/Ap_TqRsDg.c.met` (~823 KiB)

</details>
