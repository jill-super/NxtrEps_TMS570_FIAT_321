---
title: "High-Frequency Assist documents"
description: "Word/PDF/text documents shipped with HighFreqAssist (High-Frequency Assist) and their conversion status."
---

# High-Frequency Assist — documents

*Repository directory: `HighFreqAssist`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## HighFreqAssist_Integration_Manual.docx

- **Source:** `HighFreqAssist/doc/HighFreqAssist_Integration_Manual.docx`
- **Format:** `.docx` (~27 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2538 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `HighFreqAssist/doc/HighFreqAssist_Integration_Manual.docx` for those.

```text
Integration Manual -- HighFreqAssist
Contents
1Dependencies1
2Configuration1
2.1Build Time Config1
2.2Generator Config1
3Runnable Scheduling5
4Memory Mapping6
4.1Mapping6
4.2Usage6
Dependencies
Module
Required Feature
Rte
Port and runnable mapping.
WdgM
CheckpointReached() API
Configuration
Build Time Config
Constant
Notes
SWC
None
Generator Config
The HighFreqAssist module parameter description file and generator templates are located in the “generate” folder. The generation scheme at this time relies on the ARTT generation framework developed by BMW. Following are the recommended steps to integrate the provided generation templates and parameter description with Davinci Configurator:
Copy the “Artt/artt” framework folder into the “Generators” directory (if not already present)
Execute the “Integrate.bat” script from the Tools directory of this component to perform the necessary integration steps:
The script creates the required directories in the integration project, “Generators/Artt/HighFreqAssist” and “Generators/Components/_Schemes/HighFreqAssist/bswmd”
The script then copies the required files from the CBD generate directory into the new directories.
If this is the first time integration, then perform the Davinci Configurator 3rd party component integration procedure.
Constant
Notes
SWC
HighFreqAssistGeneral
General module configuration. See HighFreqAssist technical reference for details.
HighFreqAssist
Rte Config
The SWC description included with this component in the “autosar” folder describes only the static portion of the SWC. A partial SWC description describing the configurable part of the component interface is generated into the Ap_HighFreqAssist_Cfg.arxml file. This description must be imported into the Rte configuration tool (Developer) using the “Merge Object” option to merge the static SWC description with the generated partial SWC description file.
Runnable Scheduling
This section specifies the required runnable scheduling.
Runnable
Scheduling Requirements
Privileged Mode
Trigger
HighFreqAssist_Per1()
Scheduled per integration project requirements
Not Required
2ms
Memory Mapping
Mapping
Constant
Notes
HYSTADD_START_SEC_VAR_CLEARED_UNSPECIFIED
HIGHFREQASSIST_START_SEC_VAR_CLEARED_32
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.
Usage
Feature
RAM
ROM
Full SWC
Table 1: ARM Cortex R4 Memory UsageRevision Control Log
Item #
Rev #
Change Description
Date
Author Initi
```
*…excerpt ends here (38 further characters in the source).*

## High_Frequency_Assist_MDD.docx

- **Source:** `HighFreqAssist/doc/High_Frequency_Assist_MDD.docx`
- **Format:** `.docx` (~954 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5771 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `HighFreqAssist/doc/High_Frequency_Assist_MDD.docx` for those.

```text
Module – High Frequency Assist
High-Level Description
This module compensates for system inertia and road feedback. It puts handwheel torque through a high-pass filter and multiplies it by a tunable gain parameter to compensate for these factors.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
VehicleSpeed_Kph_f32
HighFreqAssist_MtrNm_f32
HwTorque_HwNm_f32
WIRCmdAmpBlnd_MtrNm_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
HwTorqueHPFKSV_Cnt_M_str
Single Precision Float
-10
10
HYSTADD_START_SEC_VAR_CLEARED_UNSPECIFIED
GainBlend_Uls_D_f32
Single Precision Float
0
1
HIGHFREQASSIST_START_SEC_VAR_CLEARED_32
GainWIRZero_MtrNmpHwNm_D_f32
Single Precision Float
0
10
HIGHFREQASSIST_START_SEC_VAR_CLEARED_32
GainVal_MtrNmpHwNm_D_f32
Single Precision Float
0
10
HIGHFREQASSIST_START_SEC_VAR_CLEARED_32
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
t_LPFKnY_Hz_u7p9[12]
t_CmnVehSpd_Kph_u9p7[12]
t2_TorqX0_HwNm_u5p11[12][13]
t2_TorqX1_HwNm_u5p11[12][13]
t2_GainY0_MtrNmpHwNm_u3p13[12][13]
t2_GainY1_MtrNmpHwNm_u3p13[12][13]
t2_WIRBlendX_MtrNm_u4p12[12][5]
t2_WIRBlendY_Uls_u1p15[12][5]
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
D_ZERO_ULS_F32
D_2MS_SEC_F32
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
None
Functions/Macros used by the Sub-Module
```
*…excerpt ends here (3271 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `HighFreqAssist/doc/QAC_Results/Ap_HighFreqAssist.c.err` (~106 KiB)
- `HighFreqAssist/doc/QAC_Results/Ap_HighFreqAssist.c.met` (~660 KiB)

</details>
