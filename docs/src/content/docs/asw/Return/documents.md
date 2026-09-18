---
title: "Return Torque Control documents"
description: "Word/PDF/text documents shipped with Return (Return Torque Control) and their conversion status."
---

# Return Torque Control — documents

*Repository directory: `Return`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Return_MDD.docx

- **Source:** `Return/doc/Return_MDD.docx`
- **Format:** `.docx` (~549 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5994 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Return/doc/Return_MDD.docx` for those.

```text
Module -- Return
High-Level Description
This function uses the Absolute Hand Wheel position, Hand Wheel Torque, Hand Wheel Velocity and Vehicle Speed to derive the desired Return Torque command.
Figures
Component Diagram
None
Diagram – Return_L5_Per
This diagram describes the functional characteristics and data flow of a given function.
Module Inputs and Outputs
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs (Global Variable Name)
Module Outputs (Global Variable Name)
HandwheelVel_HwRadpS_f32
ReturnCmd_MtrNm_f32
HandwheelAuthority_Uls_f32
HandwheelPosition_HwDeg_f32
HwTorque_HwNm_f32
VehicleSpeed_Kph_f32
SrlComSvcDft_Cnt_b32
ReturnDDFactor_Uls_f32
PAReturnSclFct_Uls_f32
Return Offset_HwDeg_f32
AssistMechTempEst_DegC_f32
DefeatReturnSvc_Cnt_lgc
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
(Note: If no module specific variables are used by the design, place the text “None” in the first Variable Name cell in the table)
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
CurrentOffset_HwDeg_M_f32
Single Precision Float
0
20
RETURN_START_SEC_VAR_CLEARED_32
CrntHandWheelAthScl_Uls_M_f32
Single Precision Float
0
1
RETURN_START_SEC_VAR_CLEARED_32
HwPosReturnCmd _MtrNm_D_f32
Single Precision Float
0
0.5
RETURN_START_SEC_VAR_CLEARED_32
HwTrqReturnScl_Uls _D_f32
Single Precision Float
0
1
RETURN_START_SEC_VAR_CLEARED_32
HwVelReturnScl_Uls _D_f32
Single Precision Float
0
50
RETURN_START_SEC_VAR_CLEARED_32
TempReturnScl_Uls_D_f32
Single Precision Float
0
10
RETURN_START_SEC_VAR_CLEARED_32
AbsHwPosReturn_HwDeg_D_u12p4
0.0625
0
1640
RETURN_START_SEC_VAR_CLEARED_16
SgnHwPosReturn_HwDeg_D_f32
Single Precision Float
-1
1
RETURN_START_SEC_VAR_CLEARED_32
RtrnBasicReturn_MtrNm_D_f32
SinglePrecisionFloating point
-10
10
RETURN_START_SEC_VAR_CLEARED_32
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Variable Name
Typedef Name
Storage Type
Safety Critical Classification
None
Constant Data Dictionary
Calibration Constants
This section lists the calibr
```
*…excerpt ends here (3494 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `Return/doc/QAC_Results/Ap_Return.c.err` (~103 KiB)
- `Return/doc/QAC_Results/Ap_Return.c.met` (~557 KiB)

</details>
