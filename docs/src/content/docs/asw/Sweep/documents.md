---
title: "Torque Sweep Generator documents"
description: "Word/PDF/text documents shipped with Sweep (Torque Sweep Generator) and their conversion status."
---

# Torque Sweep Generator — documents

*Repository directory: `Sweep`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Sweep1_MDD.docx

- **Source:** `Sweep/doc/Sweep1_MDD.docx`
- **Format:** `.docx` (~521 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Sweep/doc/Sweep1_MDD.docx` for those.

```text
Module – Sweep
High-Level Description
Figures
Component Diagram
Variable Data Dictionary
Module Inputs
Module Outputs
InputHwTrq_HwNm_f32
OutputHwTrq_HwNm_f32
VehSpdValid_Cnt_lgc
VehSpd_Kph_f32
Module Internal Variables
Variable Name
Datatype
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
{Data Type}
HwTrqQuantization_Uls_M_f32
Float32
SWEEP_START_SEC_VAR_CLEARED_32
CosSweepTorque_HwNm_M_f32
Float32
SWEEP_START_SEC_VAR_CLEARED_32
SweepVehSpdMax_Kph_M_f32
Float32
SWEEP_START_SEC_VAR_CLEARED_32
DwellStartTime_mS_M_u32p0
Uint32
SWEEP_START_SEC_VAR_CLEARED_32
LastStateSinArg_Uls_M_f32
Float32
SWEEP_START_SEC_VAR_CLEARED_32
TransStartTime_mS_M_u32p0
Uint32
SWEEP_START_SEC_VAR_CLEARED_32
MtrTrqQuantization_Uls_M_f32
Float32
SWEEP_START_SEC_VAR_CLEARED_32
SweepTorque_HwNm_M_f32
Float32
SWEEP_START_SEC_VAR_CLEARED_32
SweepAmplitude_HwNm_M_u5p11
Uint16
SWEEP_START_SEC_VAR_CLEARED_16
SweepOffset_HwNm_M_s4p11
Sint16
SWEEP_START_SEC_VAR_CLEARED_16
SweepState_Cnt_M_u16
Uint16
SWEEP_START_SEC_VAR_CLEARED_16
FreqIndex_Cnt_M_u16
Uint16
SWEEP_START_SEC_VAR_CLEARED_16
k_N_SweepConfig_Cnt_u16
Uint16
SWEEP_START_SEC_VAR_CLEARED_16
k_N_SweepGain_MtrNmpHwNm_u1p15
Uint16
SWEEP_START_SEC_VAR_CLEARED_16
L5_N_SweepOffset_HwNm_M_s4p11
Sint16
SWEEP_START_SEC_VAR_CLEARED_16
L5_N_SweepAmplitude_HwNm_M_u5p11
Uint16
SWEEP_START_SEC_VAR_CLEARED_16
L5_N_CosSweepTorque_HwNm_M_s10p5
Sint16
SWEEP_START_SEC_VAR_CLEARED_16
L5_N_RespTorque_HwNm_G_s10p5
Sint16
SWEEP_START_SEC_VAR_CLEARED_16
L5_N_SweepState_Cnt_M_u16
Uint16
SWEEP_START_SEC_VAR_CLEARED_16
L5_N_SweepTorque_HwNm_G_s10p5
Sint16
SWEEP_START_SEC_VAR_CLEARED_16
L5_N_InstFrequency_Hz_G_u7p9
Uint16
SWEEP_START_SEC_VAR_CLEARED_16
SweepConfig_Cnt_M_u16
Uint16
SWEEP_START_SEC_VAR_CLEARED_16
SweepGain_MtrNmpHwNm_M_u1p15
Uint16
SWEEP_START_SEC_VAR_CLEARED_16
L5_N_GenHwTrq_Cnt_M_lgc
boolean
N/A
FALSE
TRUE
SWEEP_START_SEC_VAR_CLEARED_BOOLEAN
k_N_EnVehSpdCheck_Cnt_lgc
boolean
N/A
FALSE
TRUE
SWEEP_START_SEC_VAR_CLEARED_BOOLEAN
k_N_SweepModeEn_Cnt_lgc
boolean
N/A
FALSE
TRUE
SWEEP_START_SEC_VAR_CLEARED_BOOLEAN
EnVehSpdCheck_Cnt_M_lgc
boolean
N/A
FALSE
TRUE
SWEEP_START_SEC_VAR_CLEARED_BOOLEAN
GenHwTrq_Cnt_M_lgc
boolean
N/A
FALSE
TRUE
SWEEP_START_SEC_VAR_CLEARED_BOOLEAN
SweepModeEn_Cnt_M_lgc
boolean
N/A
FALSE
TRUE
User defined typedef definition/declaration
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
Constant Data Dictionary
Calibration Constants
Constant Name
Program(fixed) Constants
Embedded Consta
```
*…excerpt ends here (3500 further characters in the source).*

## Sweep2_MDD.docx

- **Source:** `Sweep/doc/Sweep2_MDD.docx`
- **Format:** `.docx` (~105 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (2528 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Sweep/doc/Sweep2_MDD.docx` for those.

```text
Module – Sweep2
High-Level Description
Figures
Component Diagram
Variable Data Dictionary
Module Inputs
Module Outputs
InputMtrTrq_MtrNm_f32
OutputMtrTrq_MtrNm_f32
Module Internal Variables
Variable Name
Datatype
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
{Data Type}
SweepModeEn_Cnt_M_lgc
Boolean
N/A
FALSE
TRUE
SweepConfig_Cnt_M_u16
Uint16
1
0
FULL
User defined typedef definition/declaration
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
Constant Data Dictionary
Calibration Constants
Constant Name
Program(fixed) Constants
Embedded Constants
Local
Constant Name
Resolution
Units
Value
D_SWEEPMTRTRQ_CNT_U16
1
Uint16
1
Global
Constant Name
D_FALSE_CNT_LGC
D_ZERO_ULS_F32
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
Data Hiding Functions
<None>
Global Functions/Macros Defined by this Module
none
Local Functions/Macros Used by this MDD only
none
Software Module Implementation
Runtime Environment (RTE) Initial Values
Data
Value
InputMtrTrq_MtrNm_f32
0
Initialization Functions
None
Periodic Functions
Design Rationale
None
Store Module Inputs to Local copies Fault Recovery Functions
See below
Description
Store Local copy of outputs into Module Outputs
See above
Shutdown Functions
None
Interrupt Functions
None
Fault Recovery Functions
None
Shutdown Functions
None
Interrupt Functions
None
Serial Communication Functions
None
Execution Requirements
Execution Sequence of the Module
Execution Rates for sub-modules called by the Scheduler
This table serves as reference for the Scheduler design
Function Name
Calling Frequency
System State(s) in which the function is called
Sweep2_Per1
2ms
RTE_AP_SWEEP2_APPL_CODE
Execution Requirements for Serial Communication Functions
Function Name
Sub-Module called by (Serial Comm Function Name)
Memory Map Definition Requirements
Sub Modules (Functions)
This table identifies the software segments for functions identified in this module.
Name of Sub Module
Software Segment
Global and Local Functions
This table identifies the software segments for local functions identified in this module.
Name of Sub Module
Software Segment
Sweep2_Per1
RTE_AP_SWEEP2_APPL_CODE
Known Issues / Limitations With Design
(Item #1)
Revision Control Log
Rev #
Change Description
Date
Author Initials
1
Init
```
*…excerpt ends here (28 further characters in the source).*

## Static-analysis outputs (4 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `Sweep/doc/QAC_Results/Ap_Sweep.c.err` (~84 KiB)
- `Sweep/doc/QAC_Results/Ap_Sweep.c.met` (~789 KiB)
- `Sweep/doc/QAC_Results/Ap_Sweep2.c.err` (~82 KiB)
- `Sweep/doc/QAC_Results/Ap_Sweep2.c.met` (~784 KiB)

</details>
