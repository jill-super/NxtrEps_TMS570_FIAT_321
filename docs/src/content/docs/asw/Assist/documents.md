---
title: "Base Steering Assist documents"
description: "Word/PDF/text documents shipped with Assist (Base Steering Assist) and their conversion status."
---

# Base Steering Assist — documents

*Repository directory: `Assist`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Assist_Integration_Manual.docx

- **Source:** `Assist/doc/Assist_Integration_Manual.docx`
- **Format:** `.docx` (~26 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2406 characters in total; showing first 2406). Layout, tables, figures and images are omitted; consult `Assist/doc/Assist_Integration_Manual.docx` for those.

```text
Integration Manual -- Assist
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
The Assist module parameter description file and generator templates are located in the “generate” folder. The generation scheme at this time relies on the ARTT generation framework developed by BMW. Following are the recommended steps to integrate the provided generation templates and parameter description with Davinci Configurator:
Copy the “Artt/artt” framework folder into the “Generators” directory (if not already present)
Execute the “Integrate.bat” script from the Tools directory of this component to perform the necessary integration steps:
The script creates the required directories in the integration project, “Generators/Artt/Assist” and “Generators/Components/_Schemes/Assist/bswmd”
The script then copies the required files from the CBD generate directory into the new directories.
If this is the first time integration, then perform the Davinci Configurator 3rd party component integration procedure.
Constant
Notes
SWC
AssistGeneral
General module configuration. See Assist technical reference for details.
Assist
Rte Config
The SWC description included with this component in the “autosar” folder describes only the static portion of the SWC. A partial SWC description describing the configurable part of the component interface is generated into the Ap_Assist _Cfg.arxml file. This description must be imported into the Rte configuration tool (Developer) using the “Merge Object” option to merge the static SWC description with the generated partial SWC description file.
Runnable Scheduling
This section specifies the required runnable scheduling.
Runnable
Scheduling Requirements
Privileged Mode
Trigger
Assist_Per1()
Scheduled per integration project requirements
Not Required
2ms
Memory Mapping
Mapping
Constant
Notes
ASSIST_START_SEC_VAR_CLEARED_16
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
Author Initials
1
1
Initial version
JJW
```

## Assist_MDD.docx

- **Source:** `Assist/doc/Assist_MDD.docx`
- **Format:** `.docx` (~229 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5993 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Assist/doc/Assist_MDD.docx` for those.

```text
Module -- Assist
High-Level Description
The Assist Function applies an appropriate level of motor torque based on handwheel torque and vehicle speed.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs (Global Variable Name)
Module Outputs (Global Variable Name)
HwTrq_HwNm_f32
BaseAssistCmd_MtrNm_f32
HwTrqHysAdd_HwNm_f32
VehSpd_Kph_f32
AssistDDFactor_Uls_f32
IpTrqOvr_HwNm_f32
WIRCmdAmpBlnd_MtrNm_f32
DftAsstTbl_Cnt_lgc
DwnldAsstGain_Uls_f32
DutyCycleLevel_Uls_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
WIRBlend_Uls_D_u2p14
2-14
0
1
ASSIST_START_SEC_VAR_CLEARED_16
ThermalAssistScl_Uls_D_u2p14
2-14
0
1
ASSIST_START_SEC_VAR_CLEARED_16
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
t2_AsstHwtX0_HwNm_u8p8[][]
t2_AsstHwtX1_HwNm_u8p8[][]
t2_AsstAsstY0_MtrNm_s4p11[][]
t2_AsstAsstY1_MtrNm_s4p11[][]
t_CmnVehSpd_Kph_u9p7[]
t2_AsstWIRBlndX_MtrNm_u5p11[][]
t2_AsstWIRBlendY_Uls_u2p14[][]
t_AsstThermSclX_Cnt_u16p0[]
t_AsstThermSclY_Uls_u2p14[]
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Value
D_WIRBLENDFRAC_ULS_U2P14
2-14
1
D_ASSTTRQLLMT_MTRNM_F32
Single precision floating point
-0.1
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
BC_ASSIST_FAULTINJECTIONPOINT
STD_ON
FLTINJ_ASSIST
D_MTRTRQCMDHILMT_MTRNM_F32
D_MTRTRQCMDLOLMT_MTRNM_F32
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
None
Functions/Macros used by the Sub-Modules
Libr
```
*…excerpt ends here (3493 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `Assist/doc/QAC_Results/Ap_Assist.c.err` (~105 KiB)
- `Assist/doc/QAC_Results/Ap_Assist.c.met` (~618 KiB)

</details>
