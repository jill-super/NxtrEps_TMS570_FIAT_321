---
title: "Fault Injection documents"
description: "Word/PDF/text documents shipped with FltInjection (Fault Injection) and their conversion status."
---

# Fault Injection — documents

*Repository directory: `FltInjection`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Fault_Injection_MDD.docx

- **Source:** `FltInjection/doc/Fault_Injection_MDD.docx`
- **Format:** `.docx` (~241 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5994 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `FltInjection/doc/Fault_Injection_MDD.docx` for those.

```text
Module – Fault Injection
High-Level Description
This module manages the fault injection system. It receives parameters through CANape-generated XCP signals (which write directly into memory), and creates a fault injection signal at a specified location based on these parameters.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
MotorVelCRF_MtrRadpS_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
CanapeParameters_M_Str
CanapeParametersType
FLTINJECTION_START_SEC_VAR_CLEARED_UNSPECIFIED
FaultTrigger_Cnt_M_lgc
n/a
FALSE
TRUE
FLTINJECTION_START_SEC_VAR_CLEARED_UNSPECIFIED
ManualTriggerHangover_Cnt_M_lgc
n/a
FALSE
TRUE
FLTINJECTION_START_SEC_VAR_CLEARED_UNSPECIFIED
FaultInjectionLocation_Cnt_M_enum
1
0
255
FLTINJECTION_START_SEC_VAR_CLEARED_UNSPECIFIED
PathGain_Uls_M_f32
Single Precision Float
0
5
FLTINJECTION_START_SEC_VAR_CLEARED_32
FaultOffset_Uls_M_f32
Single Precision Float
-15
15
FLTINJECTION_START_SEC_VAR_CLEARED_32
SinewaveAmplitude_Uls_M_f32
Single Precision Float
0
15
FLTINJECTION_START_SEC_VAR_CLEARED_32
FaultDuration_mS_M_u32
1
0
10000
FLTINJECTION_START_SEC_VAR_CLEARED_32
FaultStartTime_mS_M_u32
1
FULL
FULL
FLTINJECTION_START_SEC_VAR_CLEARED_32
SineFactor_kHz_M_f32
Single Precision Float
0
0.125663706
FLTINJECTION_START_SEC_VAR_CLEARED_32
PathOffset_Uls_M_f32
Single Precision Float
-30
30
FLTINJECTION_START_SEC_VAR_CLEARED_32
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
CanapeParametersType
FaultInjectionLocation_Cnt_enum
FltInjectionLocType
0
255
PathGain_Uls_f32
float32
0
5
FaultOffset_Uls_f32
float32
-15
15
SinewaveFrequency_Hz_f32
float32
0
20
SinewaveAmplitude_Uls_f32
float32
0
15
VelocityTriggerSetpoint_MtrRadpS_f32
float32
0
800
EnableManualTrigger_Cnt_lgc
boolean
FALSE
TRUE
FaultDuration_mS_u32
uint32
0
10000
AssistDDFactor_Uls_f32
float32
1
2
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the modul
```
*…excerpt ends here (3494 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `FltInjection/doc/QAC_Results/Ap_FltInjection.c.err` (~213 KiB)
- `FltInjection/doc/QAC_Results/Ap_FltInjection.c.met` (~184 KiB)

</details>
