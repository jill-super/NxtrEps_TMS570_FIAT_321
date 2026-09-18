---
title: "Sine-Voltage Motor Driver (Current Mode) documents"
description: "Word/PDF/text documents shipped with SVDrvr_CM (Sine-Voltage Motor Driver (Current Mode)) and their conversion status."
---

# Sine-Voltage Motor Driver (Current Mode) — documents

*Repository directory: `SVDrvr_CM`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## PWMCdd_Integration_Manual.docx

- **Source:** `SVDrvr_CM/doc/PWMCdd_Integration_Manual.docx`
- **Format:** `.docx` (~38 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (3550 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `SVDrvr_CM/doc/PWMCdd_Integration_Manual.docx` for those.

```text
Integration Manual – PWMCdd
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
CDD_Data
Global variables for DC Phs Comp (for using in Nhet/)
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
CDDPorts_ClearPhsReasSum(uint16 DataAccessBfr_Cnt_T_u16)
CDD_ApplyPWMMtrElecMechPol(sint8 MtrElecMechPol_Cnt_s8)
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
<Configuration file that will generated from this components that will require Da Vinci Config generation or manual generation. Describe each parameter >
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
d_PwmFreq_Hz_Cnt_u16
d_PWMFreqDither_Hz_u16
Integration
Required Global Data Inputs
The following global symbols must be defined in CDD_Data.c and .h (populated by PwmCdd):
uint16: CDD_DCPhsComp_Cnt_G_u16[3]
uint16: CDD_PWMPeriod_Cnt_G_u16
NHET/EPWM version corresponding PWMCdd component spilt and using global variables CDD_DCPhsComp_Cnt_G_u16 and CDD_PWMPeriod_Cnt_G_u16 should be used.
CDD_Read_PhaseAdvanceFinal_Rev_u0p16
CDD_Read_CorrectedMtrPos_Rev_u0p16
CDD_Read_CommOffset_Cnt_u16
PwmCdd_Read_ModIdxFinal_Uls_u16p16
Required Global Data Outputs
CDD_Write_DCPhsBComp_Cnt_u16p0
CDD_Write_DCPhsCComp_Cnt_u16p0
Specific Include Path present
Yes - The “include” directory of this SWC needs to be included in the integration project include search path.
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
PwmCdd_Init
Place in E
```
*…excerpt ends here (1050 further characters in the source).*

## PWM_CDD_MDD.docx

- **Source:** `SVDrvr_CM/doc/PWM_CDD_MDD.docx`
- **Format:** `.docx` (~500 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5995 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `SVDrvr_CM/doc/PWM_CDD_MDD.docx` for those.

```text
Module – Module Title
High-Level Description
Non-AUTOSAR PWM driver required to perform EPS motor control PWM profiles.
Figures
Component Diagram
This diagram shows all data that is shared between functions within the module.
No data sharing
Diagram – Function (Per1)
None (For more refer section 6)
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs (Global Variable Name)
Module Outputs (Global Variable Name)
CDD_PhaseAdvFinal_Cnt_G_u16[2]
CDD_CommOffset_Cnt_G_u16[2]
CDD_PWMDutyCycleASum_Cnt_G_u32[2]
CDD_MtrPosElec_Rev_G_u0p16[2]
CDD_PWMDutyCycleBSum_Cnt_G_u32[2]
CDD_PwmDisable_Cnt_G_lgc[2]
CDD_PWMDutyCycleCSum_Cnt_G_u32[2]
CDD_PWMPeriodSum_Cnt_G_u32[2]
CDD_PhsReasA_Cnt_G_u16[2]
CDD_ModIdxFinal_Uls_G_u16p16
CDD_PhsReasB_Cnt_G_u16[2]
CDD_CDDDataAccessBfr_Cnt_G_u16
CDD_PhsReasC_Cnt_G_u16[2]
CDD_AppDataFwdPthAccessBfr_Cnt_G_u16
CDD_DCPhsComp_Cnt_G_u16[3]
CDD_AppDataFbkPthAccessBfr_Cnt_G_u16
CDD_PWMPeriod_Cnt_G_u16
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
CDD_SeedPWMDither_Cnt_M_u16
1
0
65535
PWMCDD_START_SEC_VAR_CLEARED_16
CDD_DitherFlt1SV_Cnt_M_u16
1
0
65535
PWMCDD_START_SEC_VAR_CLEARED_16
CDD_DitherFlt2SV_Cnt_M_u16
1
0
65535
PWMCDD_START_SEC_VAR_CLEARED_16
CDD_PhaseOffset_Rev_M_u0p16[3]
2^-16
0
0.99998
PWMCDD_START_SEC_VAR_CLEARED_16
PrevDCPhsAComp_Cnt_M_u16p0
1
0
7150
PWMCDD_START_SEC_VAR_CLEARED_16
PrevDCPhsBComp_Cnt_M_u16p0
1
0
7150
PWMCDD_START_SEC_VAR_CLEARED_16
PrevDCPhsCComp_Cnt_M_u16p0
1
0
7150
PWMCDD_START_SEC_VAR_CLEARED_16
DCPhsAComp_Cnt_M_u16p0
1
0
7150
PWMCDD_START_SEC_VAR_CLEARED_16
DCPhsBComp_Cnt_M_u16p0
1
0
7150
PWMCDD_START_SEC_VAR_CLEARED_16
DCPhsCComp_Cnt_M_u16p0
1
0
7150
PWMCDD_START_SEC_VAR_CLEARED_16
PrevPWMPeriod_Cnt_M_u16
1
2950
7150
PWMCDD_START_SEC_VAR_CLEARED_16
PWMPeriod_Cnt_M_u16
1
2950
7150
PWMCDD_START_SEC_VAR_CLEARED_16
PwmCdd_PWMPrdMax_Cnt_M_u16
1
4000
6667
PWMCDD_START_SEC_VAR_CLEARED_16
PwmCdd_PWMPrdMin_Cnt_M_u16
1
3334
5000
PWMCDD_START_SEC_VAR_CLEARED_16
PwmCdd_PWMPrdRange_Cnt_M_u16
1
666
1667
PWMCDD_START_SEC_VAR_CLEARED_16
User defined typedef definition/declaration
This section documents any user types
```
*…excerpt ends here (3495 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `SVDrvr_CM/doc/QAC_Results/PwmCdd.c.err` (~103 KiB)
- `SVDrvr_CM/doc/QAC_Results/PwmCdd.c.met` (~969 KiB)

</details>
