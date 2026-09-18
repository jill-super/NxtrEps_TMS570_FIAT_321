---
title: "Global Signal Overwrite Detection documents"
description: "Word/PDF/text documents shipped with Gsod (Global Signal Overwrite Detection) and their conversion status."
---

# Global Signal Overwrite Detection — documents

*Repository directory: `Gsod`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Gsod_MDD.docx

- **Source:** `Gsod/doc/Gsod_MDD.docx`
- **Format:** `.docx` (~309 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5988 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Gsod/doc/Gsod_MDD.docx` for those.

```text
Module -- Global Signal Overwrite Detection
High-Level Description
Key system inputs including handwheel torque, motor position, motor and handwheel velocity are widely distributed and used by command path and other safety critical system functions. The safety strategy for these “global” input signals is a dual channel diverse calculation with cross check to detect a systematic design fault that would propagate to the receiving functions. However, since the dual channel diversity does not continue along the command path out to the motor command output, this strategy cannot fully cover a potential systematic overwrite of the global signals after the cross checks are performed and downstream functions are then executed and use the primary path global signals. Therefore, an additional safety function has been defined to check for software over-write by co-existing software within the software memory partition where the primary global signals are calculated.
Each of the functions that generate a global input signal has been defined to store a copy of the output. The purpose of this function is to perform a comparison check of the primary signal (that was subsequently used by various system functions) and it’s redundantly stored copy. Any detected miscompare will generate an overwrite fault flag from this function to be evaluated by the diagnostics manager and result in performing an F1 shutdown response.
Design rationale note:
This module uses direct input reads instead of buffered reads to disable interrupts around data collection of the inputs to ensure that the data set is consistent. The limitation of this method is that it is only possible if inputs are being written from a task at the same or higher priority with the same or faster loop execution time; which is the case at the time of this implementation.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
Corrected_MtrPos_Rev_f32
Ana_Hw_Torque_HwNm_f32
Vecu_Volt_f32
Torque_Cmd_CRF_MtrNm_f32
Torque_Cmd_MRF_MtrNm_f32
Cum_Mtr_Pos_CRF_Deg_f32
MtrElecMech_Polarity_Cnt_s08
SysC_Corrected_MtrPos_Rev_f32
SysC_Ana_Hw_Torque_HwNm_f32
SysC_Vecu_Volt_f32
SysC_Torque_Cmd_CRF_MtrNm_f32
SysC_Torque_Cmd_MRF_MtrNm_f32
SysC_Cum_Mtr_Pos_CRF_Deg_f32
SysC_MtrElecMech_Polarity_Cnt_s32
Module Internal Variables
This section identifies the name
```
*…excerpt ends here (3488 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `Gsod/doc/QAC_Results/Ap_Gsod.c.err` (~7 KiB)
- `Gsod/doc/QAC_Results/Ap_Gsod.c.met` (~229 KiB)

</details>
