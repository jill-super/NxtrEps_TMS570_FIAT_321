---
title: "Electric Power Consumption Monitor documents"
description: "Word/PDF/text documents shipped with ElePwr (Electric Power Consumption Monitor) and their conversion status."
---

# Electric Power Consumption Monitor — documents

*Repository directory: `ElePwr`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## ElePwr_Integration_Manual.docx

- **Source:** `ElePwr/doc/ElePwr_Integration_Manual.docx`
- **Format:** `.docx` (~38 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2637 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ElePwr/doc/ElePwr_Integration_Manual.docx` for those.

```text
Integration Manual –ElePwr
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
<Name of SWC>
<Addition of global data, function*.
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
< None>
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Ap_ElePwr_Cfg.h for checkpoint enable
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
<None>
DaVinci Interrupt Configuration Changes
ISR Name
VIM #
Priority Dependency
Notes
<None>
Manual Configuration Changes
Constant
Notes
SWC
<None>
Integration
Required Global Data Inputs
MtrCurrDax_Amp_f32
MtrCurrQax_Amp_f32
MtrVoltDax_Volt_f32
MtrVoltQax_Volt_f32
Vecu_Volt_f32
Required Global Data Outputs
ElectricPower_Watt_f32
SupplyCurrent_Amp_f32
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
ElePwr_Per1
triggered on TimingEvent
10ms
Memory Mapping
Mapping
Memory Section
Contents
Notes
ELEPWR_START_SEC_VAR_CLEARED_32
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
Optimization Settings
<Define Optimization le
```
*…excerpt ends here (137 further characters in the source).*

## Electric_Power_Consumption_MDD.docx

- **Source:** `ElePwr/doc/Electric_Power_Consumption_MDD.docx`
- **Format:** `.docx` (~108 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (3968 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ElePwr/doc/Electric_Power_Consumption_MDD.docx` for those.

```text
Module -- Electric Power Consumption
High-Level Description
This module estimates the instantaneous electric power at the input of the control module and the supply current.
Figures
Diagram – Component Diagram
Variable Data Dictionary
Module Inputs
Module Outputs
Vecu_Volt_f32
ElectricPower_Watt_f32
MtrVoltDax_Volt_f32
SupplyCurrent_Amp_f32
MtrVoltQax_Volt_f32
MtrCurrDax_Amp_f32
MtrCurrQax_Amp_f32
Module Internal Variables
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
ModInPower_Watt_D_f32
Single Precision Floating Point
-2000
2000
ELEPWR_START_SEC_VAR_CLEARED _32
DropInPower_Watt_D_f32
Single Precision Floating Point
-200
200
ELEPWR_START_SEC_VAR_CLEARED _32
User defined typedef definition/declaration
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
Constant Name
k_CntlrInResist_Ohm_f32
k_PstcPowerLoss_Watt_f32
Program(fixed) Constants
Embedded Constants
Local
Constant Name
Resolution
Units
Value
D_SQRT3OVR2_ULS_F32
Single precision Float
Float32
0.866025403784
D_ELECPOWERLOLMT_WATT_F32
Single precision Float
Watt
(-2000.0)
D_ELECPOWERHILMT_WATT_F32
Single precision Float
Watt
2000.0
D_SUPPLYCURRENTLOLMT_AMP_F32
Single precision Float
Amp
(-200.0)
D_SUPPLYCURRENTHILMT_AMP_F32
Single precision Float
Amp
(200.0)
Global
Constant Name
D_ZERO_ULS_F32
D_VECUMIN_VOLTS_F32
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
None
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library functions / Macros that are called by the various sub modules are identified below,
Data Hiding Functions
None
Local Functions/Macros Used by this MDD only
None
Software Module Implementation
Initial Data Values
Data
Value
Rte_InitValue_Vecu_Volt_f32
5.0
Rte_InitValue_MtrVoltDax_Volt_f32
0.0
Rte_InitValue_MtrVoltQax_Volt_f32
0.0
Rte_InitValue_MtrCurrDax_Amp_f32
0.0
Rte_InitValue_MtrCurrQax_Amp_f32
0.0
Rte_InitValue_ElectricPower_Watt_f32
0.0
Periodic Functions
Per: ElePwr_Per1
Design Rationale
None
Program Flow Start
Rte_Call_ElePwr_Per1_CP0_CheckpointReached()
Store Module Inputs to Local copies
Local Copy
Module Input
Vecu_Volt_f32
Rte_IRead_ElePwr_Per1_Vecu_Volt_f32()
MtrVoltDax_Volt_f32
Rte_IRead_ElePwr_Per1_ MtrVoltDax_Volt_f32 ()
MtrVoltQax_Volt_f32
Rte_IRead_ElePwr_Per1_ MtrVoltQax_Volt_f32 ()
MtrCurrDax_Amp_f32
Rte_IRead_ElePwr_Per1_ MtrCurrDax_Amp_f32
MtrCurrQax_Amp_f32
Rte_IRead_ElePwr_Per1_ MtrCurrQax
```
*…excerpt ends here (1468 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `ElePwr/doc/QAC_Results/Ap_ElePwr.c.err` (~91 KiB)
- `ElePwr/doc/QAC_Results/Ap_ElePwr.c.met` (~146 KiB)

</details>
