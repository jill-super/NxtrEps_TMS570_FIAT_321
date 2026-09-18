---
title: "Active Pull Compensation documents"
description: "Word/PDF/text documents shipped with ActivePull (Active Pull Compensation) and their conversion status."
---

# Active Pull Compensation — documents

*Repository directory: `ActivePull`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Active_Pull_Comp_MDD.docx

- **Source:** `ActivePull/doc/Active_Pull_Comp_MDD.docx`
- **Format:** `.docx` (~3381 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5995 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ActivePull/doc/Active_Pull_Comp_MDD.docx` for those.

```text
Module -- Active Pull Compensation
High-Level Description
This module corrects for vehicle pull issues by compensation for both long and short term torque offsets.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
HwTorque_HwNm_f32
PullCompCmd_MtrNm_f32
HandwheelPosition_HwDeg_f32
HandwheelAuthority_Uls_f32
VehicleSpeed_Kph_f32
VehicleSpeedValid_Cnt_lgc
HandwheelVelocity_HwRadpS_f32
SrlComYawRate_DegpS_f32
DisableLearning_Cnt_lgc
DisableOutput_Cnt_lgc
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
DecGain_Uls_M_f32
Single Precision Float
0.0000135
0.00054
ACTIVEPULL_START_SEC_VAR_CLEARED_32
IncGain_Uls_M_f32
Single Precision Float
0.0000135
0.00054
ACTIVEPULL_START_SEC_VAR_CLEARED_32
LTIntGain_Uls_M_f32
Single Precision Float
0.00001875
0.00045
ACTIVEPULL_START_SEC_VAR_CLEARED_32
LTWindUpLimit_HwNm_M_f32
Single Precision Float
0
4
ACTIVEPULL_START_SEC_VAR_CLEARED_32
STStepSize_HwNm_M_f32
Single Precision Float
0
20000
ACTIVEPULL_START_SEC_VAR_CLEARED_32
PullCompStepSize_HwNm_M_f32
Single Precision Float
0
0.2
ACTIVEPULL_START_SEC_VAR_CLEARED_32
ResetPer1_Cnt_M_lgc
n/a
FALSE
TRUE
ACTIVEPULL_START_SEC_VAR_CLEARED_BOOLEAN
ResetPer2_Cnt_M_lgc
n/a
FALSE
TRUE
ACTIVEPULL_START_SEC_VAR_CLEARED_BOOLEAN
ResetPer3_Cnt_M_lgc
n/a
FALSE
TRUE
ACTIVEPULL_START_SEC_VAR_CLEARED_BOOLEAN
HwTorqueSV_HwNm_M_Str
LPF32KSV_Str
N/A
N/A
ACTIVEPULL_START_SEC_VAR_CLEARED_UNSPECIFIED
HwTorqueSV_HwNm_M_Str.K_Uls_f32
Float32
0.001255848
0.715390457
HwTorqueSV_HwNm_M_Str.SV_Uls_f32
Float32
-10
10
SrlComYawRateSV_DegpS_M_Str
LPF32KSV_Str
N/A
N/A
ACTIVEPULL_START_SEC_VAR_CLEARED_UNSPECIFIED
SrlComYawRateSV_DegpS_M_Str.K_Uls_f32
Float32
0.001255848
0.715390457
SrlComYawRateSV_DegpS_M_Str.SV_Uls_f32
Float32
-128
127.9375
EnableTime_mS_M_u32
1
0
4294967295
ACTIVEPULL_START_SEC_VAR_CLEARED_32
EnableLearn_Cnt_M_lgc
n/a
FALSE
TRUE
ACTIVEPULL_START_SEC_VAR_CLEARED_BOOLEAN
HwTorqueSTSV_HwNm_M_Str
LPF32KSV_Str
N/A
N/A
ACTIVEPULL_START_SEC_VAR_CLEARED_UNSPECIFIED
HwTorqueSTSV_HwNm_M_Str.K_Uls_f32
Float32
0.001255848
0.715390457
HwTorqueSTSV_HwNm_M_S
```
*…excerpt ends here (3495 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `ActivePull/doc/QAC_Results/Ap_ActivePull.c.err` (~106 KiB)
- `ActivePull/doc/QAC_Results/Ap_ActivePull.c.met` (~632 KiB)

</details>
