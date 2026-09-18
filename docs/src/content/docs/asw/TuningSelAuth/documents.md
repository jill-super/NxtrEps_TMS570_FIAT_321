---
title: "Tuning Select Authority documents"
description: "Word/PDF/text documents shipped with TuningSelAuth (Tuning Select Authority) and their conversion status."
---

# Tuning Select Authority — documents

*Repository directory: `TuningSelAuth`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Tuning_Select_Authority_MDD.docx

- **Source:** `TuningSelAuth/doc/Tuning_Select_Authority_MDD.docx`
- **Format:** `.docx` (~694 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5992 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TuningSelAuth/doc/Tuning_Select_Authority_MDD.docx` for those.

```text
Module – Tuning Select Authority
High-Level Description
This function broadcasts an authority to allow switching between calibration subsets while driving. It compares handwheel torque and vehicle speed to calibratable thresholds and outputs either a zero or a one.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
HwTorque_HwNm_f32
ActiveTunPers_Cnt_u16
VehicleSpeed_Kph_f32
ActiveTunSet_Cnt_u16
DesiredTunPers_Cnt_u16
TunPer_Ptr_Str *
DesiredTunSet_Cnt_u16
TunSet_Ptr_Str *
ActiveTunOvrPtrAddr_Cnt_u32
TuningSessionActPtr_Cnt_u8
* Note: For unit testing purposes these inputs are defined as pointers to uint16 (as opposed to pointers to tuning structures) for simplicity.
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
*HwTrqLPFiltSV_HwNm_M_str
Multiple
Multiple
Multiple
TUNINGSELAUTH_START_SEC_VAR_CLEARED_UNSPECIFIED
K_Uls_f32
Single Precision Float
0.0124877435
0.4665119090
SV_HwNm_f32
Single Precision Float
-10
10
PrevTunSet_Cnt_M_u16
1
0
100
TUNINGSELAUTH_START_SEC_VAR_CLEARED _16
PrevTunPers_Cnt_M_u16
1
0
100
TUNINGSELAUTH_START_SEC_VAR_CLEARED _16
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
None
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
k_TunSelHwTrqThresh_HwNm_f32
k_TunSelVehSpdThresh_Kph_f32
k_TunSelHwTrqLPFKn_Hz_f32
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
D_10MS_SEC_F32
Single Precision Float
Sec
0.010
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
D_TRUE_CNT_LGC
```
*…excerpt ends here (3492 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `TuningSelAuth/doc/QAC_Results/Ap_TuningSelAuth.c.err` (~168 KiB)
- `TuningSelAuth/doc/QAC_Results/Ap_TuningSelAuth.c.met` (~146 KiB)

</details>
