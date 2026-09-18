---
title: "Shutdown Mechanisms documents"
description: "Word/PDF/text documents shipped with ShtdnMech (Shutdown Mechanisms) and their conversion status."
---

# Shutdown Mechanisms — documents

*Repository directory: `ShtdnMech`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Shutdown_Mechanisms_MDD.docx

- **Source:** `ShtdnMech/doc/Shutdown_Mechanisms_MDD.docx`
- **Format:** `.docx` (~145 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (4782 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ShtdnMech/doc/Shutdown_Mechanisms_MDD.docx` for those.

```text
Module – Shutdown Mechanisms
High-Level Description
This module handles diagnostic data during an F1 fault. The actual signal control is performed in other modules which “own” the signal.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
None
None
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
ESMErrOutStat_Cnt_D_u08
1
0
1
SHTDNMECH_START_SEC_VAR_CLEARED_8
SysFault2Stat_Cnt_D_u08
8
0
8
SHTDNMECH_START_SEC_VAR_CLEARED_8
GateDrvResetStat_Cnt_D_u32
524288
0
524288
SHTDNMECH_START_SEC_VAR_CLEARED_32
NHETPwmStat_Cnt_D_u32
22282308
0
22282308
SHTDNMECH_START_SEC_VAR_CLEARED_32
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
None
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
D_ESMERROUTSTAT_CNT_U08
1
Counts
0x01
D_SYSFAULT2STAT_CNT_U08
1
Counts
0x08
D_GATEDRVRESETSTAT_CNT_U32
1
Counts
0x00080000
D_NHETPWMSTAT_CNT_U32
1
Counts
0x01540044
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
D_ZERO_CNT_U8
D_ZERO_CNT_U32
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
None
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
None
Data Hiding Functions
None
Global Functions/Macros Defined by this Module
None
Local Functions/Macros Used by this MDD only
None
Software Module Implementation
Runtime
```
*…excerpt ends here (2282 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `ShtdnMech/doc/QAC_Results/Sa_ShtdnMech.c.err` (~33 KiB)
- `ShtdnMech/doc/QAC_Results/Sa_ShtdnMech.c.met` (~44 KiB)

</details>
