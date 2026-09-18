---
title: "Signal Conditioning documents"
description: "Word/PDF/text documents shipped with SgnlCond (Signal Conditioning) and their conversion status."
---

# Signal Conditioning — documents

*Repository directory: `SgnlCond`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## SignalConditioning_MDD.docx

- **Source:** `SgnlCond/doc/SignalConditioning_MDD.docx`
- **Format:** `.docx` (~120 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5289 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `SgnlCond/doc/SignalConditioning_MDD.docx` for those.

```text
Module – Signal Conditioning
High-Level Description
This function conditions a signal received from SER prior to its distribution to other functions. Typical conditioning methods may include filters, slew rates, gain values or limits.
Figures
Diagram – Function Data Sharing
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs (Global Variable Name)
Module Outputs (Global Variable Name)
SrlComVehSpd_Kph_f32
VehicleSpeed_Kph_f32
SrlCom_VehicleLonAccel_KphpS_f32
Vehicle_LonAccel_KphpS_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
SignlCondn_CurrSrlComVehSpd_Kph_M_f32
Single precision floating point
See DataDictionary
See DataDictionary
SIGNLCONDN_START_SEC_VAR_NOINIT_32
SignlCondn_CurrSrlComVehLonAccel_KphpS_M_f32
Single precision floating point
See DataDictionary
See DataDictionary
SIGNLCONDN_START_SEC_VAR_NOINIT_32
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
k_VehSpdSlewRate_KphpSec_f32
k_VehAccelSlewRate_KphpSecSq_f32
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Value
D_VEHLONACCELGAIN_KPHPS_F32
N/A
3.6
D_VEHSPDLOLMT_KPH_F32
Single precision Float
0.0
D_VEHSPDHILMT_KPH_F32
Single precision Float
511.0
D_VEHLONACCELLOLMT_KPHPS_F32
Single precision Float
(-50.0)
D_VEHLONACCELHILMT_KPHPS_F32
Single precision Float
50.0
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Cons
```
*…excerpt ends here (2789 further characters in the source).*

## SignlCondn_Integration_Manual.docx

- **Source:** `SgnlCond/doc/SignlCondn_Integration_Manual.docx`
- **Format:** `.docx` (~38 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2619 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `SgnlCond/doc/SignlCondn_Integration_Manual.docx` for those.

```text
Integration Manual –SignlCondn
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
Ap_SignlCondn_Cfg.h for checkpoint enable
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
SrlComVehSpeed_Kph_f32
SrlCom_VehicleLonAccel_KphpS_f32
Required Global Data Outputs
VehicleSpeed_Kph_f32
Vehicle_LonAccel_KphpS_f32
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
SignlCondn_Per1
triggered on TimingEvent
2ms
Memory Mapping
Mapping
Memory Section
Contents
Notes
SIGNLCONDN_START_SEC_VAR_NOINIT_32
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
<Define Optimization levels that are neede
```
*…excerpt ends here (119 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `SgnlCond/doc/QAC_Results/Ap_SignlCondn.c.err` (~91 KiB)
- `SgnlCond/doc/QAC_Results/Ap_SignlCondn.c.met` (~152 KiB)

</details>
