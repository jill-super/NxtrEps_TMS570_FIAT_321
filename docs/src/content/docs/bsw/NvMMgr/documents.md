---
title: "NVRAM Manager (FEE Interface) documents"
description: "Word/PDF/text documents shipped with NvMMgr (NVRAM Manager (FEE Interface)) and their conversion status."
---

# NVRAM Manager (FEE Interface) — documents

*Repository directory: `NvMMgr`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Fee_Interface_MDD.docx

- **Source:** `NvMMgr/doc/Fee_Interface_MDD.docx`
- **Format:** `.docx` (~609 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5994 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `NvMMgr/doc/Fee_Interface_MDD.docx` for those.

```text
Module -- Fee Interface
High-Level Description
This module contains the specific interfacing functions that are needed for TI’s Fee Driver. This includes an initialization routine and configurable trusted function interfaces that allow compatibility with the NvM/MemIf BSW.
Figures
Diagram – Function Data Sharing
N/A
Diagram – Function (Name)
N/A
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
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
<None>
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
<None>
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
<None>
Module specific Lookup Tables Constants
(This is for lookup tables (arrays) with fixed values, same name as other tables)
Constant Name
Resolution
Value
Software Segment
None
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
<None>
Data Hiding Functions
<None>
Global Functions/Macros Defined by this Module
Global Functions Defined if BC_FEEIF_ECUSTARTUPTRUSTED == STD_OFF
TWrapC_FeeIf_Init
This is the client (non-trusted) side of the FeeIf_Init Trusted Function
Function Name
TWrapC_FeeIf_Init
Type
Min
Max
UTP Tol.
Arguments Passed
None
Return Value
N/A
Description
TRUSTED_TWrapS_FeeIf_Init
This is the server (trusted) side of the FeeIf_Init Trusted F
```
*…excerpt ends here (3494 further characters in the source).*

## NvMMgr_Integration_Manual.docx

- **Source:** `NvMMgr/doc/NvMMgr_Integration_Manual.docx`
- **Format:** `.docx` (~64 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (5980 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `NvMMgr/doc/NvMMgr_Integration_Manual.docx` for those.

```text
Integration Manual –NvMMgr
Table of Contents
1Dependencies2
1.1SWCs2
1.2Functions to be provided to Integration Project2
2Configuration3
2.1Build Time Config3
2.2Configuration Files to be provided by Integration Project3
2.2.1Da Vinci Config generation3
2.2.2Manual Configuration Changes3
3Integration4
3.1Required Global Data Inputs4
3.2Optional Global Data Inputs4
3.3Specific Include Path present4
4Runnable Scheduling5
5Memory Mapping6
5.1Mapping6
5.2Usage6
5.3NvM Blocks6
6Compiler Settings6
6.1Preprocessor MACRO6
6.2Optimization Settings6
7Revision Control Log7
Dependencies
SWCs
Module
Required Feature
NvM
Entire BSW
MemIf
Entire BSW
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
FeeIf
There are differing functions provided by this module depending on how it is configured through configurator. These functions are listed below based on the generated configuration. The main idea is that if the configuration is going to require configuring trusted function calls through the O/S because of the requirement that the fee driver must execute in a privileged/trusted mode, the wrapper functions to implement the trusted functions will be provided by this module automatically. The notes indicate the intended caller of the function (be it the integrator, another BSW (O/S or MemIf), or if the function is strictly called internally by this module).
Functions provided if BC_FEEIF_ECUSTARTUPTRUSTED == STD_OFF
FeeIf_Init (for NvMMgr internal use only)
TWrapC_FeeIf_Init (for integrator scheduling)
TRUSTED_TWrapS_FeeIf_Init (for O/S)
TWrapC_Fee_MainFunction (for integrator scheduling)
TRUSTED_TWrapS_Fee_MainFunction (for O/S)
Functions provided if BC_FEEIF_ECUSTARTUPTRUSTED == STD_ON
FeeIf_Init (for integrator scheduling)
Functions provided if BC_FEEIF_NVMTRUSTED == STD_OFF
TWrapC_Fee_Read (for MemIf)
TRUSTED_TWrapS_Fee_Read (for O/S)
TWrapC_Fee_Write (for MemIf)
TRUSTED_TWrapS_Fee_Write (for O/S)
TWrapC_Fee_EraseImmediateBlock (for MemIf)
TRUSTED_TWrapS_Fee_EraseImmediateBlock (for O/S)
TWrapC_Fee_InvalidateBlock (for MemIf)
TRUSTED_TWrapS_Fee_InvalidateBlock (for O/S)
TWrapC_Fee_Cancel (for MemIf)
TRUSTED_TWrapS_Fee_Cancel (for O/S)
TWrapC_Fee_GetStatus (for MemIf)
TRUSTED_TWrapS_Fee_GetStatus( for O/S)
TWrapC_Fee_GetJobResult(for MemIf)
TRUSTED_TWrapS_Fee_GetJobResult (fo
```
*…excerpt ends here (3480 further characters in the source).*

## Static-analysis outputs (6 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `NvMMgr/doc/QAC_Results/Cd_FeeIf.c.err` (~4 KiB)
- `NvMMgr/doc/QAC_Results/Cd_FeeIf.c.met` (~63 KiB)
- `NvMMgr/doc/QAC_Results/Fapi_UserDefinedFunctions.c.err` (~0 KiB)
- `NvMMgr/doc/QAC_Results/Fapi_UserDefinedFunctions.c.met` (~5 KiB)
- `NvMMgr/doc/QAC_Results/QAC.err` (~1 KiB)
- `NvMMgr/doc/QAC_Results/QAC.met` (~3 KiB)

</details>
