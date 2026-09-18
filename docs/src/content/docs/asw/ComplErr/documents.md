---
title: "Compliance Error documents"
description: "Word/PDF/text documents shipped with ComplErr (Compliance Error) and their conversion status."
---

# Compliance Error — documents

*Repository directory: `ComplErr`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## ComplErr_Integration_Manual.docx

- **Source:** `ComplErr/doc/ComplErr_Integration_Manual.docx`
- **Format:** `.docx` (~33 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2382 characters in total; showing first 2382). Layout, tables, figures and images are omitted; consult `ComplErr/doc/ComplErr_Integration_Manual.docx` for those.

```text
Integration Manual –ComplErr
Table of Contents
1Integration Manual –ComplErr1
1Dependencies2
1.1SWCs2
1.2Global Functions (Non RTE) to be provided to Integration Project2
1.2.1ComplErr_Per1()2
2Configuration2
2.1Build Time Config2
2.2Configuration Files to be provided by Integration Project2
2.2.1Da Vinci Parameter Configuration Changes2
2.2.2DaVinci Interrupt Configuration Changes2
2.2.3Manual Configuration Changes2
3Integration3
3.1Required Global Data Inputs3
3.2Required Global Data Outputs3
3.3Specific Include Path present3
4Runnable Scheduling4
5Memory Mapping5
5.1Mapping5
5.2Usage5
5.3Non RTE NvM Blocks5
5.4RTE NvM Blocks5
6Compiler Settings5
6.1Preprocessor MACRO5
6.2Optimization Settings5
7Revision Control Log6
Dependencies
SWCs
Module
Required Feature
None
Note: Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.
Global Functions (Non RTE) to be provided to Integration Project
ComplErr_Per1()
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
<Configuration file that will be generated from this components that will require Da Vinci Config generation or manual generation. Describe each parameter >
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
None
DaVinci Interrupt Configuration Changes
ISR Name
VIM #
Priority Dependency
Notes
None
Manual Configuration Changes
Constant
Notes
SWC
None
Integration
Required Global Data Inputs
None
Required Global Data Outputs
None
Specific Include Path present
None
Runnable Scheduling
This section specifies the required runnable scheduling.
Runnable
Scheduling Requirements
Trigger
ComplErr_Per1
None
RTE(2ms)
Memory Mapping
Mapping
Memory Section
Contents
Notes
RTE_START_SEC_AP_COMPLERR_APPL_CODE
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.
Usage
Feature
RAM
ROM
N/A
Table 1: ARM Cortex R4 Memory Usage
Non RTE NvM Blocks
Block Name
N/A
Note : Size of the NVM block if configured in developer
RTE NvM Blocks
Block Name
N/A
Note : Size of the NVM block if configured in developer
Compiler Settings
Preprocessor MACRO
None
Optimization Settings
None
Revision Control Log
Rev #
Change Description
Date
Author
1
Initial version
08/22/13
SP
```

## Compliance_Error_MDD.docx

- **Source:** `ComplErr/doc/Compliance_Error_MDD.docx`
- **Format:** `.docx` (~87 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (4158 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ComplErr/doc/Compliance_Error_MDD.docx` for those.

```text
Module – Compliance Error
High-Level Description
This function calculates the compliance error that can be used to compensate for stiffness in the torque path between the motor position sensor and column axis.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
TorqueCmdCRF_MtrNm_f32
ComplErr_HwDeg_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
-
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
-
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
t_CompErrMtrPosNonLinComplDepTbl_HwDegpMtrNm_u8p8[6]
t_ComplErrMtrPosNonLinComplIndTbl_MtrNm_u5p11[6]
Program (fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
-
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
D_ZERO_ULS_F32
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
None
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
IntplVarXY_u16_u16Xu16Y_Cnt
FPM_FloatToFixed_m
TableSize_m
Abs_s16_m
FPM_FixedToFloat_m
Data Hiding Functions
None
Global Functions/Macros Defined by this Module
None
Local Functions/Macros Used by this MDD only
None
Software Module Implementation
Runtime Environment (RTE) Initial Values
This section lists the initial values of data written by this module but controlled by the RTE. After RTE initialization, the data in this table will contain these values.
Data
Value
Initializ
```
*…excerpt ends here (1658 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `ComplErr/doc/QAC_Results/Ap_ComplErr.c.err` (~113 KiB)
- `ComplErr/doc/QAC_Results/Ap_ComplErr.c.met` (~543 KiB)

</details>
