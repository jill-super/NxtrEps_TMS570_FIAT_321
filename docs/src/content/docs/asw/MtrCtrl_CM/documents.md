---
title: "Motor Control (Current Mode) documents"
description: "Word/PDF/text documents shipped with MtrCtrl_CM (Motor Control (Current Mode)) and their conversion status."
---

# Motor Control (Current Mode) — documents

*Repository directory: `MtrCtrl_CM`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## CurrCmd_MDD.doc

- **Source:** `MtrCtrl_CM/doc/CurrCmd_MDD.doc`
- **Format:** `.doc` (~4894 KiB)
- **Kind:** Module design document (MDD)
- **Status:** summary record — legacy binary source retained at `MtrCtrl_CM/doc/CurrCmd_MDD.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **CurrCmd_MDD.doc** module design document specifies the `MtrCtrl_CM` software component: requirements, interfaces/ports, internal behaviour, calibration and diagnostics. It is the normative reference for the implementation in `MtrCtrl_CM/src/`; the module page lists the files it governs.

## CurrParamComp_MDD.docx

- **Source:** `MtrCtrl_CM/doc/CurrParamComp_MDD.docx`
- **Format:** `.docx` (~365 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5991 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `MtrCtrl_CM/doc/CurrParamComp_MDD.docx` for those.

```text
Module -- Parameter Compensation
High-Level Description
Figures
Diagram – Function Data Sharing
None
Diagram – Function (Name)
None
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
MtrCurrDaxRef _Amp_f32
EstKe_VpRadpS_f32
MtrCurrQaxRef_ Amp_f32
EstR_Ohm_f32
CuTempEst_DegC_f32
EstLq_Henry_f32
MagTempEst_DegC_f32
EstLd_Henry_f32
SiTempEst_DegC_f32
FastDataAccessBufIndex_Cnt_M_u16
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
EstKeFF_VpRadpS_M_f32
single precision float
0.025
0.075
CURRPARAMCOMP_START_SEC_VAR_CLEARED_32
EstRFF_Ohm_M_f32
single precision float
0.005
0.12565
CURRPARAMCOMP_START_SEC_VAR_CLEARED_32
KeSatSclFac_Uls_D_f32
single precision float
0
1
CURRPARAMCOMP_START_SEC_VAR_CLEARED_32
LqSatSclFac_Uls_D_f32
single precision float
0
2
CURRPARAMCOMP_START_SEC_VAR_CLEARED_32
LdSatSclFac_Uls_D_f32
single precision float
0
2
CURRPARAMCOMP_START_SEC_VAR_CLEARED_32
EstRfetFF_Ohm_D_f32
single precision float
0.005
0.12565
CURRPARAMCOMP_START_SEC_VAR_CLEARED_32
EstRmtrFF_Ohm_D_f32
single precision float
0.005
0.12565
CURRPARAMCOMP_START_SEC_VAR_CLEARED_32
PreLmtEstKe_VpRadpS_D_f32
single precision float
0.25
0.075
CURRPARAMCOMP_START_SEC_VAR_CLEARED_32
PreLmtEstLq_Henry_D_f32
single precision float
0.00003
0.00041
CURRPARAMCOMP_START_SEC_VAR_CLEARED_32
PreLmtEstLd_Henry_D_f32
single precision float
0.00003
0.00041
CURRPARAMCOMP_START_SEC_VAR_CLEARED_32
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
t_KeSatTblX_Amp_u9p7
t_KeSatTblY_Uls_u2p14
t_KeSatTblX_Amp_u12p4
t_CurrParamCompDaxRef_Amp_u9p7
t_CurrParamCompQaxRef_Amp_u9p7
t_CurrParamLqSatSclFac_Uls_u2p14
k_MinKeRngLmt_VpRadpS_f32
k_MaxKeRngLmt_VpRadpS_f32
k_MinRRngLmt_Ohm_f32
k_MaxRRngLmt_Ohm_f32
k_MinLqRngLmt_Henry_f32
k_MaxLqRngLmt_Henry_f32
k_MinLdRngLmt_Henry_f32
k_MaxLdRngLmt_Henry_f32
k_NomTemp_DegC_f32
k_M
```
*…excerpt ends here (3491 further characters in the source).*

## MtrCntrl_Integration_Manual.docx

- **Source:** `MtrCtrl_CM/doc/MtrCntrl_Integration_Manual.docx`
- **Format:** `.docx` (~41 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2815 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `MtrCtrl_CM/doc/MtrCntrl_Integration_Manual.docx` for those.

```text
Integration Manual -- MtrCntrl
Table of Contents
1Dependencies2
1.1SWCs2
1.2Configuration Files to be provided by Integration Project2
1.3Functions to be provided by Integration Project2
2Configuration3
2.1Build Time Config3
2.2Generator Config3
3Integration4
3.1Global Data4
3.2Component Conflicts4
3.3Include Path4
3.4ADC2 Changes4
3.5Configurator Changes4
3.5.1DIO4
3.5.2Port5
4Runnable Scheduling6
5Memory Mapping7
5.1Mapping7
5.2Usage7
6Revision Control Log8
Dependencies
SWCs
Module
Required Feature
Configuration Files to be provided by Integration Project
MtrCtrl_Cfg.h
Functions to be provided to Integration Project
PICurrCntrl_Per1()
TrqCogCancRefPer1()
Configuration
Build Time Config
Modules
Notes
PICurrentCntrl
TrqCanc
Optimization level greater than 3
Generator Config
Constant
Notes
SWC
None
Integration
Global Data
The global symbols mapping done in MtrCtrl_Cfg.h.
Component Conflicts
None
Include Path
The “include” directory of this SWC needs to be included in the integration project include search path.
.
Configurator Changes
None
Runnable Scheduling
This section specifies the required runnable scheduling.
Runnable
Scheduling Requirements
Trigger
TrqCogCancRefPer1()
Must be placed in the motor control ISR, after MtrPos
Cyclic (ISR)
PICurrCntrl_Per1()
Must be placed in the motor control ISR after TrqCogCancRefPer1()
Cyclic (ISR)
Runnable
Scheduling Requirements
Trigger
CurrParamComp_Init()
RTE (init)
PICurrCntrl_Init()
RTE (init)
TrqCanc_Init
Must be placed after CurrParamComp_Init
RTE (init)
QuadDet_Per1
Must run after TrqReasonable Diagnostics
RTE (2ms)
CurrCmd_Per1
Must run after QuadDet
RTE (2ms)
TrqCanc_Per1
Must run after CurrCmd_Per1
RTE (2ms)
PICurrCntrl_Per2()
Must be placed after TrqCanc_Per1
RTE (2ms)
CurrParamComp_Per1()
Must be placed after PICurrCntrl_Per2
RTE (2ms)
PeakCurrEst_Per1()
Must be placed after PICurrCntrl_Per2
RTE (2ms)
*Note: In motor control ISR include Ap_MtrCtrl.h instead of CDD_Func.h
Proper Initialization of input signals should occur before running each function for the first time. (CurrParamComp_Init).
Memory Mapping
Mapping
Memory Section
Contents
Notes
RTE Memory mapping
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.
Usage
Feature
RAM
ROM
Full driver
Table 1: ARM Cortex R4 Memory Usage
RTE NvM Blocks
Block Name Size
Rte_Pim_CogTrqCal 512
Rte_Pim_CogTrqRplComp 9
Note : Size of the NVM block is changed.
Revision Control Log
Rev #
Change Desc
```
*…excerpt ends here (315 further characters in the source).*

## PICurrentContrl.doc

- **Source:** `MtrCtrl_CM/doc/PICurrentContrl.doc`
- **Format:** `.doc` (~367 KiB)
- **Kind:** Supporting document
- **Status:** summary record — legacy binary source retained at `MtrCtrl_CM/doc/PICurrentContrl.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

Supporting document for `MtrCtrl_CM` (supporting document). Consult the binary original for figures, tables and formatted text.

## PeakCurrEst_MDD.docx

- **Source:** `MtrCtrl_CM/doc/PeakCurrEst_MDD.docx`
- **Format:** `.docx` (~218 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5054 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `MtrCtrl_CM/doc/PeakCurrEst_MDD.docx` for those.

```text
Module – PeakCurrEst
High-Level Description
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
Refer the Data Dictionary for inputs /outputs
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
Refer the Data Dictionary for Module level variables
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
k_EstPkCurr2msLPFKn_Uls_u16
k_EstPkCurrSlowLoopLPFKn_Uls_u16
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
D_ESTPKCURRLOLMT_AMPSQ_F32
D_ESTPKCURRHILMT_AMPSQ_F32
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
None
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
LPF_SvUpdate_u16InFixKTrunc_m
LPF_OpUpdate_u16InFixKTrunc_m
LPF_SvUpdate_s16InFixKTrunc_m
LPF_OpUpdate_s16InFixKTrunc_m
FPM_FloatToFixed_m
FPM_FixedToFloat_m
Limit_m
Data Hiding Functions
None
Global Functions/Macros Defined by this Module
None
Local Functions/Macros Used by this MDD only
None
Software Module Implementation
Runtime Environment (RTE) Initial Values
None
Initialization Functions
None
Periodic Functions
Per: PeakCurrEst_Per1
Design Rationale
None
Program Flow Start
Rte_Call_PeakCurrEst_Per1_CP0_CheckpointReached
Store Module Inputs to Local copies
IvtrLoaMtgtnEn_Cnt_T_
```
*…excerpt ends here (2554 further characters in the source).*

## Quadrant_Detection_MDD.docx

- **Source:** `MtrCtrl_CM/doc/Quadrant_Detection_MDD.docx`
- **Format:** `.docx` (~230 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5003 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `MtrCtrl_CM/doc/Quadrant_Detection_MDD.docx` for those.

```text
Module -- Quadrant Detection
High-Level Description
This module takes the cumulative motor position and determines the motor direction (using a previously saved state variable and a calibration constant for hysteresis). It then computes the torque command sign from the scaled torque command and uses both of these values to determine the motor quadrant.
Figures
Component Diagram
Diagram – Function QuadDet_Per1
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
MRFMtrTrqCmdScl_MtrNm_f32
InstMtrDir_Cnt_s08
MRFCumMtrPos_Deg_f32
MtrQuad_Cnt_u08
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
MtrTrqCmdSign_Cnt_D_s08
1
-1, 1
AP_QUADRANTDETECT_VAR_NOINIT
PrevCumMtrPos_Deg_M_f32
Single Precision Float
-1
1
AP_QUADRANTDETECT_VAR_INIT
PrevInstMtrDir_Cnt_M_s08
1
-1
1
AP_QUADRANTDETECT_VAR_INIT
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
k_InstMtrDirHyst_Deg_f32
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
D_CUMMTRPOSLOLMT_DEG_F32
Single Precision Float
Degrees
min value of MRFCumMtrPos_Deg_f32
D_CUMMTRPOSHILMT_DEG_F32
Single Precision Float
Degrees
max value of MRFCumMtrPos_Deg_f32
D_MTRTRQCMDTOL_MTRNM_F32
Single Precision Float
MtrNm
0.00390625
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
D_QUADRANT1_CNT_U8
D_QUADRANT2_CNT_U8
D_QUADRANT3_CNT_U8
D_QUADRANT4_CNT_U8
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
None
Functi
```
*…excerpt ends here (2503 further characters in the source).*

## TorqueCmdScaling_MDD.doc

- **Source:** `MtrCtrl_CM/doc/TorqueCmdScaling_MDD.doc`
- **Format:** `.doc` (~241 KiB)
- **Kind:** Module design document (MDD)
- **Status:** summary record — legacy binary source retained at `MtrCtrl_CM/doc/TorqueCmdScaling_MDD.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **TorqueCmdScaling_MDD.doc** module design document specifies the `MtrCtrl_CM` software component: requirements, interfaces/ports, internal behaviour, calibration and diagnostics. It is the normative reference for the implementation in `MtrCtrl_CM/src/`; the module page lists the files it governs.

## TrqCanc_MDD.docx

- **Source:** `MtrCtrl_CM/doc/TrqCanc_MDD.docx`
- **Format:** `.docx` (~1139 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5982 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `MtrCtrl_CM/doc/TrqCanc_MDD.docx` for those.

```text
Module -- TrqCanc
High-Level Description
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
Refer the Data dictionary
Refer the Data dictionary
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
Refer the Data dictionary
Refer the Data dictionary
Refer the Data dictionary
Refer the Data dictionary
Refer the Data dictionary
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
CoggingM_Amp_Str
CoggingMX_MtrNm_s2p13
sint16
FULL
FULL
CoggingMY_MtrNm_s2p13
sint16
FULL
FULL
CogTrqCalPtr
Rte_Pim_CogTrqCal()[512]
Uint16
-1
1
CogTrqCalRplCompPtr
Rte_Pim_CogTrqRplComp()[9]
Uint16
-1
1
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
k_Harmonic6thElec_Uls_f32
k_Harmonic12thElec_Uls_f32
k_Harmonic18thElec_Uls_f32
t_MtrCurrQaxRpl_Amp_u9p7[]
t_MtrCurrDaxRpl_Amp_u9p7[]
t2_MtrTrqRpl6X_MtrNm_s2p13
t2_MtrTrqRpl6Y_MtrNm_s2p13
t2_MtrTrqRpl12X_MtrNm_s2p13
t2_MtrTrqRpl12Y_MtrNm_s2p13
t2_MtrTrqRpl18X_MtrNm_s2p13
t2_MtrTrqRpl18Y_MtrNm_s2p13
t_MtrVelX_MtrRadpS_T_u14p2[10]
t_MtrTrqCancPIMagRP_Uls_u6p10[10]
t_MtrTrqCancPIPhRP_Rev_u0p16[10]
t_MtrTrqCmdPIY_MtrNm_u5p11 []
t2_MtrTrqCancPIMagRP_Uls_u6p10[]
t2_MtrTrqCancPIPhRP_Rev_u0p16[]
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
D_SQRT3OVR2_ULS_F32
Single precision float
Unit less
0.866025403784
D_6HARMONICNO_F32
Single precision float
Unit less
6
D_12HARMONICNO_F32
Single precision float
Unit less
12
D_COGGINGTBLRES_F32
Single precision float
Counts
81.48733
D_MAXTBLVALUE_CNT_u16
1
Counts
511
D_SCALERADTOCNTS_ULS_F32
Single precision float
Unit less
10430.3783505
D_30DEGREES_CNT_U16
```
*…excerpt ends here (3482 further characters in the source).*

## Static-analysis outputs (14 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `MtrCtrl_CM/doc/QAC_Results/Ap_CurrCmd.c.err` (~114 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_CurrCmd.c.met` (~951 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_CurrParamComp.c.err` (~103 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_CurrParamComp.c.met` (~818 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_PICurrCntrl.c.err` (~107 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_PICurrCntrl.c.met` (~865 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_PeakCurrEst.c.err` (~107 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_PeakCurrEst.c.met` (~926 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_QuadDet.c.err` (~91 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_QuadDet.c.met` (~216 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_TrqCanc.c.err` (~114 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_TrqCanc.c.met` (~978 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_TrqCmdScl.c.err` (~91 KiB)
- `MtrCtrl_CM/doc/QAC_Results/Ap_TrqCmdScl.c.met` (~215 KiB)

</details>
