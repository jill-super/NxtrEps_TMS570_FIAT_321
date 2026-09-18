---
title: "Signal Polarity Assignment documents"
description: "Word/PDF/text documents shipped with Polarity (Signal Polarity Assignment) and their conversion status."
---

# Signal Polarity Assignment — documents

*Repository directory: `Polarity`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Polarity_MDD.docx

- **Source:** `Polarity/doc/Polarity_MDD.docx`
- **Format:** `.docx` (~1027 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5994 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Polarity/doc/Polarity_MDD.docx` for those.

```text
Module -- Polarity
High-Level Description
This module implements the polarity assignments for the EPS systems to allow for various configurations of input and output signals for proper alignment.
Figures
Diagram – Component Diagram
Diagram – Function Data Sharing
No shared data.
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
DiagHwTrqPolarity_Cnt_s08
HwTrqPolarity_Cnt_s08
DiagHwPosPolarity_Cnt_s08
HwPosPolarity_Cnt_s08
DiagMtrPosPolarity_Cnt_s08
MtrPosPolarity_Cnt_s08
DiagMtrVelPolarity_Cnt_s08
MtrVelPolarity_Cnt_s08
DiagMtrElecMechPolarity_Cnt_s08
MtrElecMechPolarity_Cnt_s08
DiagAssistAssyPolarity_Cnt_s08
AssistAssyPolarity_Cnt_s08
SysC_ MtrElecMechPolarity_Cnt_s32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Data Type
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
Polarity_Cnt_Str
Polarity_DataType
N/A
See DataType
See DataType
**NvM/Per-Instance Memory**
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
Polarity_DataType
Polarity_Cnt_b08
uint8
Full
Full
R_Polarity_Cnt_b08
uint8
Full
Full
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
Units
Value
D_HWTRQPOL_CNT_B08
1
Counts
0x01
D_HWPOSPOL_CNT_B08
1
Counts
0x02
D_MTRPOSPOL_CNT_B08
1
Counts
0x04
D_MTRVELPOL_CNT_B08
1
Counts
0x08
D_ASSTASSEMPOL_CNT_B08
1
Counts
0x10
D_MTRELECMECHPOL_CNT_B08
1
Counts
0x20
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
D_NEGONE_CNT_S8
D_ONE_CNT_S8
Module specific Lookup Tables Constants
(This is for lookup tables (arrays) with fixed v
```
*…excerpt ends here (3494 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `Polarity/doc/QAC_Results/Ap_Polarity.c.err` (~4 KiB)
- `Polarity/doc/QAC_Results/Ap_Polarity.c.met` (~202 KiB)

</details>
