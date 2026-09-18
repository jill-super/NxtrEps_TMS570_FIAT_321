---
title: "Vehicle Speed Limiting documents"
description: "Word/PDF/text documents shipped with VehSpdLmt (Vehicle Speed Limiting) and their conversion status."
---

# Vehicle Speed Limiting — documents

*Repository directory: `VehSpdLmt`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## VehSpdLmt_MDD.docx

- **Source:** `VehSpdLmt/doc/VehSpdLmt_MDD.docx`
- **Format:** `.docx` (~408 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5549 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `VehSpdLmt/doc/VehSpdLmt_MDD.docx` for those.

```text
Module -- Vehicle Speed Limiting
High-Level Description
The Vehicle Speed Limiting Function determines a limited assist torque command value as a function of vehicle speed and handwheel position to manage mechanical fatigue near end-of-travel positions.
Figures
Diagram – Function Data Sharing
No Shared Data
Diagram – Function
None
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs
Module Outputs
VehSpd_Kph_f32
AstVehSpdLimit_MtrNm_f32
HwPos_HwDeg_f32
HwPosAuth_Uls_f32
CWPosition_HwDeg_f32
CCWPosition_HwDeg_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
ZeroVehSpd_MtrNm_D_u5p11
2^-11
0
8.8
VEHSPDLMT_START_SEC_VAR_CLEARED_16
LimitTerm_MtrNm_D_u5p11
2^-11
0
8.8
VEHSPDLMT_START_SEC_VAR_CLEARED_16
BkPtOne_HwDeg_D_u12p4
2^-4
0
900
VEHSPDLMT_START_SEC_VAR_CLEARED_16
BkPtTwo_HwDeg_D_u12p4
2^-4
0
900
VEHSPDLMT_START_SEC_VAR_CLEARED_16
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
k_PosMaxOfstOne_HwDeg_u12p4
k_PosMaxOfstTwo_HwDeg_u12p4
t_MaxAsstTblX_Kph_u9p7[]
t_MaxAsstTblY_MtrNm_u5p11[5]
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
D_MAXCONF_ULS_F32
single precision float
Unitless
1.0
D_ASTVEHSPDLMTLOLMT_MTRNM_F32
single precision float
MtrNm
0.0
D_ASTVEHSPDLMTHILMT_MTRNM_F32
single precision float
MtrNm
8.8
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant N
```
*…excerpt ends here (3049 further characters in the source).*
