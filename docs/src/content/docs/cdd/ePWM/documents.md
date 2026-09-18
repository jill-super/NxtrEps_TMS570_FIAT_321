---
title: "Enhanced PWM and NHET Driver documents"
description: "Word/PDF/text documents shipped with ePWM (Enhanced PWM and NHET Driver) and their conversion status."
---

# Enhanced PWM and NHET Driver — documents

*Repository directory: `ePWM`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## CD_NHET_1_MDD.docx

- **Source:** `ePWM/doc/CD_NHET_1_MDD.docx`
- **Format:** `.docx` (~543 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5992 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ePWM/doc/CD_NHET_1_MDD.docx` for those.

```text
Module –Nhet
High-Level Description
This module implements functionality with respect to ES-34B ePWM. This module implements the subfunctions other than the Motor Control Configuration Override subfunction and register initialization.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
Nhet_HtuDataTrq_Cnt_G_str
DigHwTrqT1_HwNm_f32
PWMPeriod_Cnt_u16
DigHwTrqT2_HwNm_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
Nhet1_NTCParamT1_Cnt_M_u08
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_NTCParamT2_Cnt_M_u08
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_FltAccT1_Cnt_M_u16
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_FltAccT2_Cnt_M_u16
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_HwTrqT1_HwNm_M_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_HwTrqT2_HwNm_M_f32
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_TotalMsg_Cnt_M_u32
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_T1MissMsg_Cnt_M_u32
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_T2MissMsg_Cnt_M_u32
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_PrevPulseCountT1_Cnt_M_u32
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_PrevPulseCountT2_Cnt_M_u32
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_T1CalcCRC_Cnt_D_u08
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
Nhet1_T2CalcCRC_Cnt_D_u08
See Data Dictionary
See Data Dictionary
See Data Dictionary
See Data Dictionary
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
(Refer the included ref for more details of register)
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal R
```
*…excerpt ends here (3492 further characters in the source).*

## NHetRegisters.pdf

- **Source:** `ePWM/doc/NHetRegisters.pdf`
- **Format:** `.pdf` (~1885 KiB)
- **Kind:** Reference document (PDF)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `ePWM/doc/NHetRegisters.pdf` for those.

```text
/0 /1 /2 /3 /4/5 /6 /7 /8 /9 /6 /10 /11 /12 /13 /14 /15 /8 /12 /9 /15 /16 /16 /16 /17 /18 /19 /17 /20 /21 /22
/23 /24 /25 /26 /25 /27 /28 /29 /30 /31 /32 /29 /33 /30 /34 /35 /36 /37 /38 /39 /32 /40 /36 /30 /34/41 /42 /37 /36 /43 /40 /42 /39 /44 /45 /46 /47 /28 /33 /41 /48
/49 /50 /51 /52 /53 /54 /55 /21 /56 /56 /57 /58 /18 /59 /60 /60 /60 /61 /62 /63 /64 /64 /65 /66 /49 /50 /51 /52 /53 /50 /55 /21 /56 /56 /57 /58 /18 /59 /60 /60 /60 /61 /62 /67 /64 /64 /65
/68 /69 /70 /71 /72 /73 /50 /74 /75 /54 /76 /76 /77 /78 /79 /80 /81 /82 /79 /83 /80 /84 /85 /69 /70 /71 /72 /82 /86 /69 /80 /84/87 /73 /70 /69 /88 /86 /73 /72 /89 /51 /52 /53 /78 /83 /87 /90
/91 /92 /93 /94 /93 /95 /93 /91 /93 /93 /93 /92 /93 /64 /92 /67 /92 /63 /92 /61 /92 /96
/97 /58 /57 /58 /98 /99 /58 /100 /101 /102 /103/104 /105 /106/102 /106 /107 /97 /57 /99 /100 /17 /108 /104 /97 /58 /57 /58 /98 /99 /58 /100 /104 /104 /60 /105 /109 /110 /108 /109
/97 /111 /64 /97 /112 /113/111 /92 /97 /111 /64 /97 /112 /113/111 /64 /97 /111 /64 /97 /112 /113/111 /64 /97 /112 /113/111 /64 /97 /112 /113/111 /64
/92 /94 /92 /64
/97 /58 /57 /58 /98 /99 /58 /100 /103 /114
/97 /111 /64 /97 /112 /113/111 /64
/115 /102 /116 /102 /106 /117 /118 /97
```
*…excerpt ends here (4800 further characters in the source).*

## Nhet_1_MDD.docx

- **Source:** `ePWM/doc/Nhet_1_MDD.docx`
- **Format:** `.docx` (~1813 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5989 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ePWM/doc/Nhet_1_MDD.docx` for those.

```text
Module – NHET
High-Level Description
This module implements NHET1 and HTU1 initialization per ES-34B NHET1 subfunctions, and NHET2 initialization, currently not documented in an FDD.
Figures
None
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
HET_INIT1_PST
Nhet_Htu1RstFail_Cnt_G_lgc
HET_INIT0_PST
Nhet_HtuDataTrq_Cnt_G_str
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
Nhet_HtuDataTrq_Cnt_G_str
N/A
N/A
N/A
NHET_START_SEC_VAR_CLEARED_UNSPECIFIED
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
(Refer the included ref for more details of register)
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
HtuDataTrq_Str
HtuDataTrq1_Cnt_u32 [8]
Uint32
0
FULL
HtuDataTrq2_Cnt_u32 [8]
Uint32
0
FULL
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
k_SENTSyncDelay_Cnt_u32
k_SENTSyncTrgMin_Cnt_u32
k_SPI50UOff_Cnt_u16
k_SPI1mOff_Cnt_u16
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
D_INSTTODATARATIO_CNT_U16
1
Counts
4
D_DATAFLDOFFSET_CNT_U16
1
Counts
8
D_BASEADDNHETRAM_CNT_U32
1
Counts
0xFF460000UL
D_WCAPHTUADDR1_CNT_U32
1
Counts
D_BASEADDNHETRAM_CNT_U32 + (16U*pHET_T1MSGCNTST_0) + 8UL
D_WCAPHTUADDR2_CNT_U32
1
Counts
D_BASEADDNHETRAM_CNT_U32 + (16U*pHET_T2MSGCNTST_0) + 8UL
D_CELEMENT_CNT_U16
1
Counts
8
D_CBUFLEN_CNT_U16
1
Counts
8
D_CONFIGHETREGDMA_CNT_U32
1
Counts
Configurable. 0UL if no DMA needs to be enabled and 1UL if using DMA
D_CFRAME_CNT_U16
1
Counts
(D_CBUFLEN_CNT_U16/D_CELEMENT_CNT_U16)
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
None
Mod
```
*…excerpt ends here (3489 further characters in the source).*

## RegisterReference_EPWM.pdf

- **Source:** `ePWM/doc/RegisterReference_EPWM.pdf`
- **Format:** `.pdf` (~2040 KiB)
- **Kind:** Reference document (PDF)
- **Status:** summary record — legacy binary source retained at `ePWM/doc/RegisterReference_EPWM.pdf`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

Supporting document for `ePWM` (reference document (pdf)). Consult the binary original for figures, tables and formatted text.

## ePWM_1_MDD.docx

- **Source:** `ePWM/doc/ePWM_1_MDD.docx`
- **Format:** `.docx` (~2216 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5986 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ePWM/doc/ePWM_1_MDD.docx` for those.

```text
Module – EPWM 1
High-Level Description
This module implements functionality with respect to ES-34B ePWM. This module implements the ePWM-related register initialization and the motor control and ADC SOCA configuration update subfunctions.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
PWMPeriod_Cnt_u16
ePWM1CMPA_Cnt_u16
DCPhsAComp_Cnt_u16
ePWM1CMPB_Cnt_u16
DCPhsBComp_Cnt_u16
ePWM2CMPA_Cnt_u16
DCPhsCComp_Cnt_u16
ePWM2CMPB_Cnt_u16
ePWM4CMPB_Cnt_u16
ePWM3CMPA_Cnt_u16
ePWM3CMPB_Cnt_u16
ePWM4CMPA_Cnt_u16
ePWM4CMPB_Cnt_u16
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
None
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
k_ADCTrig1Offset_Cnt_s16
k_PwmDeadBand_Cnt_u16
k_PwmRelay_Cnt_u16
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Legal Range
(min)
Legal Range
(max)
Value
D_DUTYCYCLESHIFT_CNT_U16
1
535U
535U
535U
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
None
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
None
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
ePWM_Read_PWMPeriod_u16
ePWM_Read_DCPhsAComp_u16
ePWM_Read_DCPhsBComp_u16
ePWM_Read_DCPhsCComp_u16
ePWM_Write_ePWM1CMPA_Cnt_u16
ePWM_Write_ePWM1CMPB_Cnt_u16
ePWM_Write_ePWM2CMPA_Cnt_u16
ePWM_Write_ePWM2CMPB_Cnt_u16
ePWM_Write_ePWM3CM
```
*…excerpt ends here (3486 further characters in the source).*

## ePWM_2_MDD.docx

- **Source:** `ePWM/doc/ePWM_2_MDD.docx`
- **Format:** `.docx` (~137 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5754 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ePWM/doc/ePWM_2_MDD.docx` for those.

```text
Module – EPWM 2
High-Level Description
This module implements the ”Motor Control Configuration Override” subfunction of ES-34B. It controls enable and disable of the motor control ePWM outputs.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
DiagStsCtrldDisRmpPres_Cnt_lgc
None
DiagStsNonRecRmpToZeroFltPres_Cnt_lgc
RampDwnStatusComplete_Cnt_lgc
CtrldDmpStsCmp_Cnt_lgc
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
(Refer the included ref for more details of register)
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
None
Program(fixed) Constants
Embedded Constants
All fixed point embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Units
Value
D_ZEROTHRESHOLD_MTRNM_F32
MtrNm
0.05
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
None
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
None
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
Abs_f32_m
ePWM_EnableOutputs
ePWM_DisableOutputs
Data Hiding Functions
None
Global Functions/Macros Defined by this Module
Local Macro
None
Local Functions/Macros Used by this MDD only
None
Software Module Implementation
Runtime Environment (RTE) Initial Values
This section lists the initial values of data written by this module but controlled by the RTE. After RTE initialization, the data in this table will contain these values.
```
*…excerpt ends here (3254 further characters in the source).*

## ePWM_Integration_Manual.docx

- **Source:** `ePWM/doc/ePWM_Integration_Manual.docx`
- **Format:** `.docx` (~50 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (5991 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `ePWM/doc/ePWM_Integration_Manual.docx` for those.

```text
Integration Manual ePWM
Table of Contents
1Dependencies2
1.1SWCs2
1.2Global Functions(Non RTE) to be provided to Integration Project2
2Configuration3
2.1Build Time Config3
2.2Configuration Files to be provided by Integration Project3
ePWM_Cfg.h is manually created and used.3
2.2.1Da Vinci Parameter Configuration Changes3
2.2.2DaVinci Interrupt Configuration Changes5
2.2.3Manual Configuration Changes5
3Integration6
3.1Required Global Data Inputs6
3.2Required Global Data Outputs6
3.3Specific Include Path present6
4Runnable Scheduling7
5Memory Mapping8
5.1Mapping8
5.2Usage8
5.3Non RTE NvM Blocks9
5.4RTE NvM Blocks9
6Other Configuration Changes9
6.1.1DIO and IOHwAb9
6.1.2Port10
7Compiler Settings11
7.1Preprocessor MACRO11
7.2Optimization Settings11
8Revision Control Log12
Dependencies
SWCs
Module
Required Feature
uDiag
HTU MPU ESM (uDiag Component version FDD32B_TMS570_uDiag_000.24 or later)
(Configuration of ESM Registers)
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
Nhet1_Per3
Nhet_Init1
ePWM_Per1
ePWM_Init1
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
ePWM_Cfg.h is manually created and used.
Refer the ePWM_Cfg_Template.h provided in the tools path of the component for more details
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
uDiag/RuntimeRegCheck/HTU__MP0S_HTU1
Address Linked during runtime
uDiagRegAddress
4294419572 (0xFFF7A474)
uDiagRegValueLnk
Nhet_HtuDataTrq_Cnt_G_str
uDiagRegValueLnkOffset
0
uDiag/RuntimeRegCheck /HTU__MP0E_HTU1
Address Linked during runtime
uDiagRegAddress
4294419576(0xFFF7A478)
uDiagRegValueLnk
Nhet_HtuDataTrq_Cnt_G_str
uDiagRegValueLnkOffset*
Sizeof(Nhet_HtuDataTrq_Cnt_G_str)-4
uDiag/RuntimeRegCheck HTUDCP1_IFADDRA_HTU1
Address Linked during runtime
uDiagRegAddress
(0xFF4E0010
uDiagRegValueLnk
Nhet_HtuDataTrq_Cnt_G_str.HtuDataTrq1_Cnt_u32[0]
uDiagRegValueLnkOffset
0
uDiag/RuntimeRegCheck/HTU__MP1S_HTU1
uDiagRegAddress
4294419532(0xFFF7A44C)
uDiagRegValue
0
uDiag/RuntimeRegCheck /HTU__MP1E_HTU1
uDiagRegAddress
4294419536(0xFFF7A450)
uDiagRegValue
0
uDiag/RuntimeRegCheck HTUDCP2_IFADDRA_HTU1
Address Linked during runtime
uDiagRegAddress
0xFF4E0020
uDiagRegValueLnk
(Nhet_HtuDataTrq_Cnt_G_str.HtuDataTrq2_Cnt_u32[0])
uDiagRegValueLnkOffset
0
uDiag/RuntimeR
```
*…excerpt ends here (3491 further characters in the source).*

## Static-analysis outputs (12 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `ePWM/doc/QAC_Results/Ap_ePWM2.c.err` (~91 KiB)
- `ePWM/doc/QAC_Results/Ap_ePWM2.c.met` (~339 KiB)
- `ePWM/doc/QAC_Results/Cd_Nhet1.c.err` (~104 KiB)
- `ePWM/doc/QAC_Results/Cd_Nhet1.c.met` (~521 KiB)
- `ePWM/doc/QAC_Results/Nhet.c.err` (~23 KiB)
- `ePWM/doc/QAC_Results/Nhet.c.met` (~228 KiB)
- `ePWM/doc/QAC_Results/Nhet2_ePWM_Prog.c.err` (~7 KiB)
- `ePWM/doc/QAC_Results/Nhet2_ePWM_Prog.c.met` (~109 KiB)
- `ePWM/doc/QAC_Results/Nhet_SENT_Prog.c.err` (~22 KiB)
- `ePWM/doc/QAC_Results/Nhet_SENT_Prog.c.met` (~148 KiB)
- `ePWM/doc/QAC_Results/ePWM.c.err` (~8 KiB)
- `ePWM/doc/QAC_Results/ePWM.c.met` (~61 KiB)

</details>
