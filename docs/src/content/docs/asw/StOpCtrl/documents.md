---
title: "State Output Control documents"
description: "Word/PDF/text documents shipped with StOpCtrl (State Output Control) and their conversion status."
---

# State Output Control — documents

*Repository directory: `StOpCtrl`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## State_Output_Control_MDD.docx

- **Source:** `StOpCtrl/doc/State_Output_Control_MDD.docx`
- **Format:** `.docx` (~216 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5995 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `StOpCtrl/doc/State_Output_Control_MDD.docx` for those.

```text
Module – State Output Control
High-Level Description
This function performs the ramp up and ramp down of the Torque Command.
Figures
Diagram – Function Data Sharing
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs (Global Variable Name)
Module Outputs (Global Variable Name)
TrqCmd_MtrNm_f32
FinalTrqCmd_MtrNm_f32
SrlComSvcDft_Cnt_b32
OutputRampMult_Uls_f32
DiagRampRate_XpmS_32
RampDwnStatusComplete_Cnt_lgc
DiagRampValue_Uls_f32
OperRampRate_XpmS_f32
OperRampValue_Uls_f32
RampSrlComSvcDft_Cnt_lgc
DiagStsDiagRmpActive_Cnt_lgc
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
AttenFactor_Uls_M_f32
Single precision floating point
1.175494351e-038
3.402823466e+038
ActvRampUsr_Cnt_M_u16
1
0
16
PrevOutputRampMult_Uls_M_f32
Single precision floating point
0
1
STOPCTRL_START_SEC_VAR_NOINIT_32
PrevTargetRampMult_Uls_M_f32
Single precision floating point
0
1
STOPCTRL_START_SEC_VAR_NOINIT_32
PrevRate_XpmS_M_f32
Single precision floating point
0.0001
0.5
STOPCTRL_START_SEC_VAR_NOINIT_32
RampState_M_Str
RampState_T
See 3.1.1
See 3.1.1
STOPCTRL_START_SEC_VAR_NOINIT_UNSPECIFIED
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
RampState_T
StartTime_mS_u32
Duration_mS_u32
StartVal_Uls_f32
EndVal_Uls_f32
uint32
uint32
float32
float32
0
0
0
0
2^32-1
2^32-1
1
1
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Value
D_TWO_MS_U32
1
2
D_MAXRAMP_XPMS_F32
Single precision floating point
0.5
Global
This sect
```
*…excerpt ends here (3495 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `StOpCtrl/doc/QAC_Results/Ap_StOpCtrl.c.err` (~206 KiB)
- `StOpCtrl/doc/QAC_Results/Ap_StOpCtrl.c.met` (~168 KiB)

</details>
