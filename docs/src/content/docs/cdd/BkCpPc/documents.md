---
title: "Bulk Capacitor Precharge and Power Disconnect documents"
description: "Word/PDF/text documents shipped with BkCpPc (Bulk Capacitor Precharge and Power Disconnect) and their conversion status."
---

# Bulk Capacitor Precharge and Power Disconnect — documents

*Repository directory: `BkCpPc`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Bulk_Cap_Precharge_MDD.docx

- **Source:** `BkCpPc/doc/Bulk_Cap_Precharge_MDD.docx`
- **Format:** `.docx` (~1083 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5995 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `BkCpPc/doc/Bulk_Cap_Precharge_MDD.docx` for those.

```text
Module – Bulk Capacitor Precharge and Power Disconnect
High-Level Description
This module handles precharging of the bulk capacitor during initialization. It is part of a larger initialization sequence, along with motor driver diagnostics and temporal monitor.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
OVERRIDESIGDIAGADC_Volt_f32
PwrDiscClosed_Cnt_lgc
PMOSDIAGADC_Volt_f32
PwrDiscATestComplete_Cnt_lgc
MotorVelocityMRFUnfiltered_MtrRadpS_f32
PwrDiscBTestComplete_Cnt_lgc
Batt_Volt_f32
BattSwitched_Volt_f32
PwrDiscATestStart_Cnt_lgc
PwrDiscBTestStart_Cnt_lgc
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
FirstRunComplete_Cnt_M_lgc
n/a
FALSE
TRUE
BKCPPC_START_SEC_VAR_CLEARED_UNSPECIFIED
PowerRelayInitFltFailed_Cnt_M_lgc
n/a
FALSE
TRUE
BKCPPC_START_SEC_VAR_CLEARED_UNSPECIFIED
PwrDiscATestComplete_Cnt_M_lgc
n/a
FALSE
TRUE
BKCPPC_START_SEC_VAR_CLEARED_UNSPECIFIED
PwrDiscBTestComplete_Cnt_M_lgc
n/a
FALSE
TRUE
BKCPPC_START_SEC_VAR_CLEARED_UNSPECIFIED
PwrDiscClosed_Cnt_M_lgc
n/a
FALSE
TRUE
BKCPPC_START_SEC_VAR_CLEARED_UNSPECIFIED
BulkCapPrechargeState_Cnt_M_enum
1
0
7
BKCPPC_START_SEC_VAR_CLEARED_UNSPECIFIED
RunTimeFaultAcc_Cnt_M_u16
1
FULL
FULL
BKCPPC_START_SEC_VAR_CLEARED_16
VerifyDiscOpenDiagTimer_mS_M_u32
1
FULL
FULL
BKCPPC_START_SEC_VAR_CLEARED_32
WaitForSqrWaveDiagTimer_mS_M_u32
1
FULL
FULL
BKCPPC_START_SEC_VAR_CLEARED_32
PrechargeDiagTimer_mS_M_u32
1
FULL
FULL
BKCPPC_START_SEC_VAR_CLEARED_32
PostCloseDiagTimer_mS_M_u32
1
FULL
FULL
BKCPPC_START_SEC_VAR_CLEARED_32
VerifyCloseDiagTimer_mS_M_u32
1
FULL
FULL
BKCPPC_START_SEC_VAR_CLEARED_32
VdischMax_Volts_M_f32
Single Precision Float
0
21
BKCPPC_START_SEC_VAR_CLEARED_32
VdischMin_Volts_M_f32
Single Precision Float
0
19
BKCPPC_START_SEC_VAR_CLEARED_32
VbattStart_Volts_M_f32
Single Precision Float
0
30
BKCPPC_START_SEC_VAR_CLEARED_32
VswitchStart_Volts_M_f32
Single Precision Float
0
20
BKCPPC_START_SEC_VAR_CLEARED_32
MotionDetected_Cnt_D_lgc
n/a
FALSE
TRUE
BKCPPC_START_SEC_VAR_CLEARED_UNSPECIFIED
DeltaV_Volts_D_f32
Single Precision Float
-20
30
BKCPPC_START_S
```
*…excerpt ends here (3495 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `BkCpPc/doc/QAC_Results/Sa_BkCpPc.c.err` (~93 KiB)
- `BkCpPc/doc/QAC_Results/Sa_BkCpPc.c.met` (~329 KiB)

</details>
