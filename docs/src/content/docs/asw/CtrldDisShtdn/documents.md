---
title: "Controlled Disable Shutdown documents"
description: "Word/PDF/text documents shipped with CtrldDisShtdn (Controlled Disable Shutdown) and their conversion status."
---

# Controlled Disable Shutdown — documents

*Repository directory: `CtrldDisShtdn`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Controller_Disable_MDD.docx

- **Source:** `CtrldDisShtdn/doc/Controller_Disable_MDD.docx`
- **Format:** `.docx` (~622 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5993 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `CtrldDisShtdn/doc/Controller_Disable_MDD.docx` for those.

```text
Module -- Controlled Disable Shutdown
High-Level Description
The Controlled Disable Damping Shutdown method is used for torque sensor failures. When the torque sensor fails, an output torque is computed based on motor velocity to reduce the amount of “handwheel kick” perceived by the driver.
Figures
Component Diagram
Module Inputs and Outputs
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs (Global Variable Name)
Module Outputs (Global Variable Name)
SumLimTrqCmd_MtrNm_f32
CntDisMtrTrqCmdCRF_MtrNm_f32
CRFMtrVel_MtrRadpS_f32
CtrldDmpCmp_Cnt_lgc
DiagStsF2Active_Cnt_lgc
CntDisMtrTrqCmdMRF_MtrNm_f32
AssistAssyPolarity_Cnt_s08
SysC_CRFMtrTrqCmd
SysC_MRFMtrTrqCmd
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
CntrlDampVelTrq_MtrNm_D_f32
Single Precision Float
-2200
2200
CTRLDDISSHTDN_START_SEC_VAR_CLEARED_32
CntrlDampElpsdTime_mS_D_u16
1
FULL
FULL
CTRLDDISSHTDN_START_SEC_VAR_CLEARED_16
LastF2Fault_mS_M_u32
1
0
1000
CTRLDDISSHTDN_START_SEC_VAR_CLEARED_32
CntrlDampTrq_MtrNm_D_f32
Single Precision Float
-5.75
5.75
CTRLDDISSHTDN_START_SEC_VAR_CLEARED_32
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Variable Name
Typedef Name
Storage Type
Safety Critical Classification
None
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
k_F2Damping_MtrNmpRadpS_f32
k_CtrlDpVelThr_MtrRadpS_f32
k_CntrlDmpRampEnd_Uls_u8p8
k_MaxCtrlDmpLimit_MtrNm_f32
k_CtrlDmpTmrBkptOne_mS_u16
k_CtrlDmpTmrBkptTwo_mS_u16
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Value
D_CNTRLDMPTMRSZ_CNT_U16
1
2
D_CTRLDMPRES_MTRNM_F32
Single Precision Floating Point
0.007813
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the
```
*…excerpt ends here (3493 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `CtrldDisShtdn/doc/QAC_Results/Ap_CtrldDisShtdn.c.err` (~174 KiB)
- `CtrldDisShtdn/doc/QAC_Results/Ap_CtrldDisShtdn.c.met` (~527 KiB)

</details>
