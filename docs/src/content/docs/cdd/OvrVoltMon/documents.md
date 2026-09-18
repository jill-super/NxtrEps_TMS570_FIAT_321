---
title: "Overvoltage Monitor documents"
description: "Word/PDF/text documents shipped with OvrVoltMon (Overvoltage Monitor) and their conversion status."
---

# Overvoltage Monitor — documents

*Repository directory: `OvrVoltMon`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## OverVoltageMonitor_MDD.docx

- **Source:** `OvrVoltMon/doc/OverVoltageMonitor_MDD.docx`
- **Format:** `.docx` (~288 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (4954 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `OvrVoltMon/doc/OverVoltageMonitor_MDD.docx` for those.

```text
Module -- OverVoltageMonitor
Overvoltage monitor function operates so that when an overvoltage condition occurs on any of the CPU supply voltages the motor inverter operation is shutdown before the CPU can respond.
High-Level Description
Figures
Diagram – Function Data Sharing
Diagram – Function (Name)
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs
Module Outputs
PwrDiscBTestStart_Cnt_lgc
phyOvrVoltFdbk_OP_GET
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
OvrVoltMon_OverVoltAcc_Cnt_M_u16
1
1
512
OVRVOLTMON_START_SEC_VAR_CLEARED_16
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
k_CPUSupplyOV_Cnt_Str
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
None
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
None
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
Data Hiding Functions
Rte_Call_NxtrDiagMgr_SetNTCStatus
Rte_Mode_SystemState_Mode()
Global Functions/Macros Defined by this Module
Global Function #1
Function Name
Rte_Mode_SystemState_Mode
Type
Min
Max
Argument
```
*…excerpt ends here (2454 further characters in the source).*

## OvrVoltMon_Integration_Manual.docx

- **Source:** `OvrVoltMon/doc/OvrVoltMon_Integration_Manual.docx`
- **Format:** `.docx` (~39 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2683 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `OvrVoltMon/doc/OvrVoltMon_Integration_Manual.docx` for those.

```text
Integration Manual –OvrVoltMon
Table of Contents
1Dependencies2
1.1SWCs2
1.2Global Functions(Non RTE) to be provided to Integration Project2
2Configuration3
2.1Build Time Config3
2.2Configuration Files to be provided by Integration Project3
2.2.1Da Vinci Parameter Configuration Changes3
2.2.2DaVinci Interrupt Configuration Changes3
2.2.3Manual Configuration Changes3
3Integration4
3.1Required Global Data Inputs4
3.2Required Global Data Outputs4
3.3Specific Include Path present4
4Runnable Scheduling5
5Memory Mapping6
5.1Mapping6
5.2Usage6
5.3Non RTE NvM Blocks6
5.4RTE NvM Blocks6
6Compiler Settings6
6.1Preprocessor MACRO6
6.2Optimization Settings6
7Revision Control Log7
Dependencies
SWCs
Module
Required Feature
None
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
None
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Sa_OvrVoltMon_Cfg.h generated by Sa_OvrVoltMon_Cfg.h.tt
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
OvrVoltMonGeneral/OvrVoltMonCPEnable
To enable checkpoints
OvrVoltMon
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
Rte_Mode_SystemState_Mode
PwrDiscBTestStart_Cnt_lgc
phyOvrVoltFdbk_OP_GET
Required Global Data Outputs
Specific Include Path present
No
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
Runnable
Scheduling Requirements
Trigger
OvrVoltMon_Per1
HwPwUp Sequence should run before this periodic
RTE 2ms
.
Memory Mapping
Mapping
Memory Section
Contents
Notes
OVRVOLTMON_START_SEC_VAR_CLEARED_16
RTE_START_SEC_AP_OVRVOLTMON_APPL_CODE
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.
Usage
Feature
RAM
ROM
<Memmap usuage info>
Table 1: ARM Cortex R4 Memory Usage
Non RTE NvM Blocks
Block Name
<NVM block used Non RTE functions >
Note : Size of the NVM block if configured in developer
RTE NvM Blocks
Block Name
<NVM block used in RTE functions >
Note : Size of the NVM block if configured in developer
Compiler Settings
Preprocessor MACRO
<Define all the preprocessor Macros needed and conditions when needed>.
Op
```
*…excerpt ends here (183 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `OvrVoltMon/doc/QAC_Results/Sa_OvrVoltMon.c.err` (~91 KiB)
- `OvrVoltMon/doc/QAC_Results/Sa_OvrVoltMon.c.met` (~407 KiB)

</details>
