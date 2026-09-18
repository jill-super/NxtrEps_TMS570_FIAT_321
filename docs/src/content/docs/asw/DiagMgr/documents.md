---
title: "Diagnostics Manager documents"
description: "Word/PDF/text documents shipped with DiagMgr (Diagnostics Manager) and their conversion status."
---

# Diagnostics Manager — documents

*Repository directory: `DiagMgr`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Diagnostics_Manager_Core_MDD.docx

- **Source:** `DiagMgr/doc/Diagnostics_Manager_Core_MDD.docx`
- **Format:** `.docx` (~1047 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DiagMgr/doc/Diagnostics_Manager_Core_MDD.docx` for those.

```text
Module -- Diagnostics Manager Core
High-Level Description
Figures
Component Diagram
Variable Data Dictionary
Module Inputs
Module Outputs
MEC_Cnt_enum
MfgDiagInhibit_Cnt_lgc
SystemState_Mode
Module Internal Variables
Variable Name
Datatype
Resolution
Legal Range
(min)
Legal Range
(max)
Multiplicity
Software Segment
{Data Type}
NTCStrgArray_Cnt_str
NTCStrgArray
N/A
N/A
N/A
1:1
DIAGMGR_START_SEC_VAR_SAVED_ZONEHGS_UNSPECIFIED
NTCBlackBoxData_Cnt_str
NTCBlkBoxData
N/A
N/A
N/A
1:1
DIAGMGR_START_SEC_VAR_SAVED_ZONEHGS_UNSPECIFIED
DEMEventActive_Cnt_M_lgc[D_NUMOFDEMEVENTS_CNT_U08+1]
Boolean
N/A
FALSE
TRUE
1:1
DIAGMGR_START_SEC_VAR_CLEARED_BOOLEAN
ResetNTCFlag_Cnt_M_u08
Refer *
Refer *
Refer *
Refer *
Refer *
Refer *
DiagMgr_NTCInfo#_Cnt_M_str
Refer *
Refer *
Refer *
Refer *
Refer *
Refer *
User defined typedef definition/declaration
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
NTCStrgArray
NTCStrg
NTCBlkBoxData
NTCBlkBoxType
typedef struct { } NTCBlkBoxType
NTC_Cnt_u08
Uint8
1
FULL
Param_Cnt_u08
Uint8
0
FULL
SystemState_Cnt_u08
Uint8
0
4
VehSpd_Kph_u8p0
Uint8
0
FULL
BlkBoxCfgData1
Uint32
0
FULL
BlkBoxCfgData2
Uint32
0
FULL
BlkBoxCfgData3
Uint32
0
FULL
HwTrq_HwNm_s4p11
Sint16
-10
10
MtrTrq_MtrNm_s4p11
Sint16
-8.8
8.8
IgnCtr_Cnt_u16
Uint16
0
FULL
typedef struct { } NTCStrg
NTC
NTCNumber
0
511
Status
uint8
0
FULL
AgingCounter
uint8
0
FULL
Status
uint8
0
FULL
AgingCounter
uint8
0
FULL
Constant Data Dictionary
Calibration Constants
Constant Name
k_FltRspTbl_Cnt_str[]
k_FltRmpRate_UlspmS_f32[]
Program(fixed) Constants
Embedded Constants
Local
Constant Name
Resolution
Units
Value
D_FLTRSPNTCACTIVEBIT_CNT_B32
N/A
Counts
0x00800000
D_FLTRSPRECOVERABLEBIT_CNT_B32
N/A
Counts
0x00400000
D_FLTRSPHWASBSYSTMFLTBIT_CNT_B32
N/A
Counts
0x00200000
D_FLTRSPDEFVEHSPDBIT_CNT_B32
N/A
Counts
0x00100000
D_FLTRSPDEFTEMPBIT_CNT_B32
N/A
Counts
0x00080000
D_FLTRSPSCOMHWANOTVALIDBIT_CNT_B32
N/A
Counts
0x00040000
D_FLTRSPWIRDISABLEBIT_CNT_B32
N/A
Counts
0x00008000
D_FLTRSPPWRCYCLTCHBIT_CNT_B32
N/A
Counts
0x00000010
D_FLTRSPNTCINHIBITNOTOPERATEBIT_CNT_B32
N/A
Counts
0x00000020
D_FLTRSPNTCINHIBITRUNBIT_CNT_B32
N/A
Counts
0x00000040
D_FLTRSPRAMPBITS_CNT_B32
N/A
Counts
0x0000000F
D_FLTRSPBLKBOXBITS_CNT_B32
N/A
Counts
0x00003800
D_BLKBOXBITOFFSET_CNT_U08
N/A
Counts
11
D_RAMPNONE_CNT_U8
1
Counts
0x0F
D_RAMPF2_CNT_U8
1
Counts
0x0E
D_RAMPF1_CNT_U8
1
Counts
0x0D
D_DIAGRMPRTLOLMT_ULSPMS_F32
Single precision float
Uls/mS
0.0001
D_DIAGRMPRTHILMT_ULSPMS_F32
Single precisio
```
*…excerpt ends here (3498 further characters in the source).*

## Diagnostics_Manager_DemIf_MDD.docx

- **Source:** `DiagMgr/doc/Diagnostics_Manager_DemIf_MDD.docx`
- **Format:** `.docx` (~662 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5996 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DiagMgr/doc/Diagnostics_Manager_DemIf_MDD.docx` for those.

```text
Module -- Diagnostics Manager DEM Interface
High-Level Description
Figures
Component Diagram
Variable Data Dictionary
Module Inputs
Module Outputs
IgnCnt_Cnt_u16
MtrTrq_MtrNm_f32
VehSpd_Kph_f32
HwTrq_HwNm_f32
SystemState_Mode
Module Internal Variables
Variable Name
Datatype
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
{Data Type}
DEMEventActive_Cnt_M_lgc[D_NUMOFDEMEVENTS_CNT_U08+1]
Refer to Diagnostics_Manager_Core_MDD.docx
ResetNTCFlag_Cnt_M_u08
Diagnostics_Manager_GeneratedCfg_MDD.docx
LatchCounter_Cnt_u16
uint16
1
0
65535
DIAGMGRDEMIF_START_SEC_VAR_16
NTCStrgArray_Cnt_str
Refer to Diagnostics_Manager_Core_MDD.docx
NTCBlackBoxData_Cnt_str
Refer to Diagnostics_Manager_Core_MDD.docx
User defined typedef definition/declaration
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
Typedef struct {} NTCLatch_Str
NTC
NTCNumber
0
511
DiagSettings_Str.Threshold
Uint16
0
65535
DiagSettings_Str.PStep
Uint16
0
65535
DiagSettings_Str.NStep
Uint16
0
65535
Constant Data Dictionary
Calibration Constants
Constant Name
t_SortedNTCs_Cnt_enum[]
k_FltRspTbl_Cnt_str[]
t_BlkBoxGrp_Ptr_u32[][]
t_LatchFaults_Cnt_str[]
Program(fixed) Constants
Embedded Constants
Local
Constant Name
Resolution
Units
Value
D_EVTNOTPASSBITS_CNT_B8
N/A
Counts
(D_TESTFAILEDBIT_CNT_B8 | D_TESTNOTCOMPLETETHISOPCYCLEBIT_CNT_B8)
D_AGINGCOUNTERTHRESH_CNT_U08
N/A
Counts
0x40
Global
Constant Name
D_NUMOFDEMEVENTS_CNT_U08
D_TESTFAILEDBIT_CNT_B8
D_TESTNOTCOMPLETETHISOPCYCLEBIT_CNT_B8
D_NTCACTIVEBITS_CNT_B8
D_MAXLATCHACTIVENTCS_CNT_U08
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
T_DiagMgrNtcAppInfoMap_Cnt_Str[SIZE]
Refer *
AP_DIAGMGR_CONST
T_DiagMgrNtcInfoPtr_Cnt_Str[SIZE]
Refer *
AP_DIAGMGR_CONST
Note: “ Refer *” - Refer to Diagnostics_Manager_GeneratedCfg_MDD
Note Size and elements of Table constants varies across projects. Check project configuration files Under UTP/ Contract folder for data.
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
TableSize_m()
Data Hiding Functions
<None>
Global Functions/Macros Defined by this Module
Diagnostic Manager Init 1
Function Name
DiagMgr_Init1
Type
Min
Max
Arguments Passed
none
Return Value
none
Description
Diagnostic Manager Transition 1
Function Name
DiagMgr_Trns1
Type
Min
Max
Arguments Passed
none
Return Value
none
Description
Rte_Call_DemIf_RestartDem()
Rte_Cal
```
*…excerpt ends here (3496 further characters in the source).*

## Diagnostics_Manager_FailAction_MDD.docx

- **Source:** `DiagMgr/doc/Diagnostics_Manager_FailAction_MDD.docx`
- **Format:** `.docx` (~147 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (3670 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DiagMgr/doc/Diagnostics_Manager_FailAction_MDD.docx` for those.

```text
Module -- Diagnostics Manager Fail Action
High-Level Description
Figures
Component Diagram
Variable Data Dictionary
Module Inputs
Module Outputs
DiagStsNonRecRmpToZeroFltPres_Cnt_lgc
DiagStsCtrldDisRmpPres_Cnt_lgc
DiagStsRecRmpToZeroFltPres_Cnt_lgc
DiagStsHWASbSystmFltPres_Cnt_lgc
DiagStsDefVehSpd_Cnt_lgc
DiagStsDefTemp_Cnt_lgc
DiagStsScomHWANotValid_Cnt_lgc
DiagStsWIRDisable_Cnt_lgc
DiagRampRate_XpmS_f32
DiagRampValue_Uls_f32
DiagRmpToZeroActive_Cnt_lgc
Module Internal Variables
Variable Name
Datatype
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
{Data Type}
DiagSts#_Cnt_M_b16[2]
Refer to Diagnostics_Manager_GeneratedCfg_MDD.docx
ActiveRmpRate#_UlspmS_M_f32[2]
Refer to Diagnostics_Manager_GeneratedCfg_MDD.docx
User defined typedef definition/declaration
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
Constant Data Dictionary
Calibration Constants
Constant Name
Program(fixed) Constants
Embedded Constants
Local
Constant Name
Resolution
Units
Value
Global
Constant Name
DIAGMGR_NUMAPPS
D_DIAGSTSNONRECRMPTOZEROBIT_CNT_B16
D_DIAGSTSRECRMPTOZEROBIT_CNT_B16
D_DIAGSTSCTRLDDISRMPBIT_CNT_B16
D_DIAGSTSHWASBSYSTMFLTBIT_CNT_B16
D_DIAGSTSDEFVEHSPDBIT_CNT_B16
D_DIAGSTSDEFTEMPBIT_CNT_B16
D_DIAGSTSSCOMHWANOTVALIDBIT_CNT_B16
D_DIAGSTSWIRDISABLEBIT_CNT_B16
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
T_DiagMgrDiagSts_Ptr_b16[SIZE]
N/A
Refer *
AP_DIAGMGR_CONST
T_DiagMgrRmpRate_Ptr_f32[SIZE]
N/A
Refer *
AP_DIAGMGR_CONST
Note: “ Refer *” - Refer to Diagnostics_Manager_GeneratedCfg_MDD
Note Size and elements of Table constants varies across projects. Check project configuration files Under UTP/ Contract folder for data.
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
TableSize_m()
Data Hiding Functions
<None>
Global Functions/Macros Defined by this Module
Diagnostic Manager Periodic 1
Function Name
DiagMgr_Per1
Type
Min
Max
Arguments Passed
none
Return Value
none
Description
Local Functions/Macros Used by this MDD only
Read Bits
Function Name
ReadBit_u16
Type
Min
Max
Arguments Passed
Data
Uint16
0
FULL
BitMask
Uint16
0
FULL
Return Value
Boolean
FALSE
TRUE
Description
IF (Data & BitMask) = 0
Return (FALSE)
ELSEReturn(TRUE)
END IF
Software Module Implementation
Runtime Environment (RTE) Initial Values
Data
Value
Initialization Functions
None
Periodic Functions
None
Fault
```
*…excerpt ends here (1170 further characters in the source).*

## Diagnostics_Manager_GeneratedCfg_MDD.docx

- **Source:** `DiagMgr/doc/Diagnostics_Manager_GeneratedCfg_MDD.docx`
- **Format:** `.docx` (~313 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `DiagMgr/doc/Diagnostics_Manager_GeneratedCfg_MDD.docx` for those.

```text
Module -- Diagnostics Manager Core
High-Level Description
Figures
Component Diagram
Variable Data Dictionary
Module Inputs
Module Outputs
Module Internal Variables
Variable Name
Datatype
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
{Data Type}
ResetNTCFlag_Cnt_M_u08
Uint8
1
0
FF
DIAGMGR#_START_SEC_VAR_CLEARED_8
NTCQueueIndex#_Cnt_M_u08
Uint8
1
Range depends on size of NTCInfoQueue#_Cnt_M_Str[SIZE]
Refer *
DIAGMGR#_START_SEC_VAR_CLEARED_UNSPECIFIED
DiagMgrInitComp#_Cnt_M_lgc
Boolean
NA
False
True
DIAGMGR#_START_SEC_VAR_CLEARED_Unspecified
DiagMgr_NTCInfo#_Cnt_M_str[SIZE]
NTCInfo_Str
NA
See section 3.1.1
See section 3.1.1
DIAGMGR#_START_SEC_VAR_CLEARED_Unspecified
NTCInfoQueue#_Cnt_M_str[SIZE]
NTCInfoQueue_Str
NA
See section 3.1.1
See section 3.1.1
DIAGMGR#_START_SEC_VAR_CLEARED_Unspecified
ActDiagSts#_Cnt_M_u08
Uint8
1
0
1
DIAGMGR#_START_SEC_VAR_CLEARED_8
ResetNTCFlag#_Cnt_M_u08
Uint8
1
0
FF
DIAGMGR#_START_SEC_VAR_CLEARED_8
DiagSts#_Cnt_M_b16[SIZE]
Uint16
1
0
FULL
DIAGMGR#_START_SEC_VAR_CLEARED_Unspecified
ActiveRmpRate#_UlspmS_M_f32[SIZE]
Float32
Single Precision float
0.0001
0.5
DIAGMGR#_START_SEC_VAR_CLEARED_32
Note: *Refer: Size varies across projects. Check Configuration files under UTP/Contract folder
User defined typedef definition/declaration
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
typedef struct { } NTCInfo_Str
Param
uint8
0
FULL
Status
uint8
0
FULL
AgingCounter
uint8
0
64
typedef struct { } NTCInfoQueue_Str
NTC
NTCNumber
0
511
Param
Uint8
0
FULL
Status
NxtrDiagMgrStatus
0
255
Constant Data Dictionary
Calibration Constants
Constant Name
k_FltRspTbl_Cnt_str[]
k_FltRmpRate_UlspmS_f32[]
Program(fixed) Constants
Embedded Constants
Local
Global
Constant Name
** DIAGMGR_NUMAPPS
** DIAGMGR_EVENTNUM_#
** DIAGMGR_APID_#
Note **: Global const values varies across projects. Check configuration files under UTP/Contract folder. “#” denotes application number.
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
T_NTCMapTbl#_Cnt_enum[SIZE]
N/A
{ ** }
AP_DIAGMGR_CONST
T_DiagMgrNtcInfoPtr_Cnt_Str[SIZE]
N/A
** {&DiagMgr_NTCInfo#_Cnt_M_str[0], #,
}
AP_DIAGMGR_CONST
T_DiagMgrNtcAppInfoMap_Cnt_Str[SIZE]
N/A
** {{ &DiagMgr_NTCInfo#_Cnt_M_str[0], #},
…
}
AP_DIAGMGR_CONST
**NOTE : Elements and Size of table are different across different projects and applications. Check Configuration files under UTP/Contract folder
Functions/Macros used by the Sub-Modules
Library Functions / Mac
```
*…excerpt ends here (3499 further characters in the source).*

## Static-analysis outputs (6 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `DiagMgr/doc/QAC_Results/Ap_DiagMgr_Core.c.err` (~92 KiB)
- `DiagMgr/doc/QAC_Results/Ap_DiagMgr_Core.c.met` (~402 KiB)
- `DiagMgr/doc/QAC_Results/Ap_DiagMgr_DemIf.c.err` (~102 KiB)
- `DiagMgr/doc/QAC_Results/Ap_DiagMgr_DemIf.c.met` (~839 KiB)
- `DiagMgr/doc/QAC_Results/Ap_DiagMgr_FailAction.c.err` (~36 KiB)
- `DiagMgr/doc/QAC_Results/Ap_DiagMgr_FailAction.c.met` (~226 KiB)

</details>
