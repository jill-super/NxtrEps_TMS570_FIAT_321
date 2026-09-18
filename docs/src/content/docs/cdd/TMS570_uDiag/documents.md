---
title: "TMS570 Microcontroller Diagnostics documents"
description: "Word/PDF/text documents shipped with TMS570_uDiag (TMS570 Microcontroller Diagnostics) and their conversion status."
---

# TMS570 Microcontroller Diagnostics — documents

*Repository directory: `TMS570_uDiag`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Cd_uDiagFPU_MDD.docx

- **Source:** `TMS570_uDiag/doc/Cd_uDiagFPU_MDD.docx`
- **Format:** `.docx` (~208 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5984 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TMS570_uDiag/doc/Cd_uDiagFPU_MDD.docx` for those.

```text
High-Level Description
Cd_uDiagFPU provides diagnostic data on floating point exceptions. Based on “Unreleased draft of EA3.x FDD 32.5 uC Diagnostics Execution (0x02A-0x031) v002.docx” as saved on May 7, 2013 and “Unreleased Draft of EA3.x FDD 32.Appendices v002.docx” as saved on May 6, 2013.
On initialization, it sets up the Secondary Auxiliary Control Register to generate a floating point interrupt (VIM47) on the occurrence of any of these floating point exception flags: IOC (invalid operation), OFC (overflow), or DZC (divide by zero), and enables the floating point interrupt. When the floating point interrupt occurs, the module’s ISR saves program address information (to indicate where the exception occurred) and a reset reason indicating the type of exception, and causes a reset.
Cd_uDiagFPU functionality is enabled/disabled by D_ENABLEFPUDIAG_CNT_LGC. See Integration Manual for the configuration parameter that controls this #define.
Figures
Diagram – Function Data Sharing
No Shared Data
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs
Module Outputs
ResetCause_Cnt_Enum
ResetCause_Cnt_Enum
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
FPUExceptionAddr_Cnt_D_u32
NA
FULL
FULL
See Integration Manual
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
<None>
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
D_FPSCRBITIOC_CNT_U32
N/A
N/A
0x00000001
D_FPSCRBITDZC_
```
*…excerpt ends here (3484 further characters in the source).*

## Cd_uDiagUtility_MDD.docx

- **Source:** `TMS570_uDiag/doc/Cd_uDiagUtility_MDD.docx`
- **Format:** `.docx` (~31 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (3983 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TMS570_uDiag/doc/Cd_uDiagUtility_MDD.docx` for those.

```text
High-Level Description
Cd_uDiagUtility provides utility assembly language functions needed by the Cd_uDiag component.
Figures
Diagram – Function Data Sharing
No Shared Data
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs
Module Outputs
<None>
<None>
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
<None>
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
<None>
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
<None>
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
<None>
Data Hiding Functions
<None>
Global Functions/Macros Defined by this Module
Global Function #1
Function Name
_uDiagGetLinkRegForFiqIsr_()
Type
Dir.
Min
Max
UTP Tol.
Arguments Passed
None
Return Value
Link Register as saved in top stack frame when executing an FIQ ISR
uint32
FULL
FULL
Description
The saved link register is at offset 0x5C from the top of the stack. Load saved link register value to register R0 and return.
ldrr0, [sp, #0x5C
```
*…excerpt ends here (1483 further characters in the source).*

## Cd_uDiag_Integration_Manual.docx

- **Source:** `TMS570_uDiag/doc/Cd_uDiag_Integration_Manual.docx`
- **Format:** `.docx` (~49 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (5985 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TMS570_uDiag/doc/Cd_uDiag_Integration_Manual.docx` for those.

```text
Integration Manual –Cd_uDiag
Table of Contents
1Dependencies2
1.1SWCs2
1.2Functions to be provided to Integration Project2
2Configuration3
2.1Build Time Config3
2.2Configuration Files to be provided by Integration Project3
2.2.1Da Vinci Parameter Configuration Changes4
2.2.2DaVinci Interrupt Configuration Changes5
2.2.3Manual Configuration Changes5
3Integration6
3.1Required Global Data Inputs6
3.2Optional Global Data Inputs6
3.3Specific Include Path present6
4Runnable Scheduling6
5Memory Mapping7
5.1Mapping7
5.2Usage7
5.3NvM Blocks7
6Compiler Settings7
6.1Preprocessor MACRO7
6.2Optimization Settings7
7Revision Control Log8
Dependencies
NOTE – the TMS570_uDiag component includes both uDiag and FlsTst functionality. For complete integration information on the TMS570_uDiag component, also see the FlsTst integration manual (in the TMS570_uDiag\doc folder).
SWCs
Module
Required Feature
TMS570_Startup
_coreGetFPSCR_()
_coreGetSecondaryAuxiliaryControlRegister_()
_coreSetSecondaryAuxiliaryControlRegister_()
Reset Causes
_fiqhandler**
Basic System Services
EnableVFPInterrupt()*
EnableESMLInterrupt()***
Dma
Dma_DmaRstFail_Cnt_G_lgc****
Nhet
Nhet_Htu1RstFail_Cnt_G_lgc****
Nhet_Htu2RstFail_Cnt_G_lgc****
NOTES:
*When uDiagEnableFPUDiag is set to STD_OFF, the floating point exception diagnostic is disabled and EnableVFPInterrupt() is optional.
**_fiqhandler needed only if configuring Mcu_FpuIrq as an interrupt (see section 2.2.2).
*** EnableESMLInterrupt() is now called from a function in the TMS570_uDiag component, as of component version FDD32B_TMS570_uDiag_000.23. When using component version FDD32B_TMS570_uDiag_000.23 or later, any other call(s) to the EnableESMLInterrupt() function, e.g. in EcuStartup, must be removed. This fixes anomaly 6133.
**** DmaRstFail needed only when DMA_MPU_ENABLE is set to STD_ON; Htu1RstFail needed only when N2HET1TU_MPU_ENABLE is set to STD_ON; Htu2RstFail needed only when N2HET2TU_MPU_ENABLE is set to STD_ON. See section 2.2.3.
Functions to be provided to Integration Project
< Global function (except the ones that are defined in RTE modules) that is defined in this component but used by other function>
FUNC(void, CD_UDIAG_APPL_CODE) uDiagFPU_Init1(void);
FUNC(void, CD_UDIAG_APPL_CODE) uDiagFPU_Init2(void);
UDIAG_COMPILER_ISR void Mcu_FpuIrq(void);
FUNC(void, CD_UDIAG_APPL_CODE) uDiagCCRM_Init(void);
FUNC(void, CD_UDIAG_APPL_CODE) uDiagClockMonitor_Init(void);
FUNC(void, CD_UDIAG_APPL_CODE) uDiagECC_Init(void);
FUNC(void, CD_UDIAG_APP
```
*…excerpt ends here (3485 further characters in the source).*

## FlsTst_Integration_Manual.docx

- **Source:** `TMS570_uDiag/doc/FlsTst_Integration_Manual.docx`
- **Format:** `.docx` (~39 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (5884 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TMS570_uDiag/doc/FlsTst_Integration_Manual.docx` for those.

```text
Integration Manual -- Flash Test
Contents
1Dependencies1
1.1SWCs2
1.2Functions to be provided to Integration Project2
2Configuration2
2.1Build Time Config2
2.2Configuration Files to be provided by Integration Project2
2.2.1Da Vinci Parameter Configuration Changes3
2.2.2DaVinci Interrupt Configuration Changes3
2.2.3Manual Configuration Changes3
3Integration4
3.1Required Global Data Inputs4
3.2Optional Global Data Inputs4
3.3Specific Include Path present4
4Runnable Scheduling4
5Memory Mapping4
5.1Mapping4
5.2Usage5
5.3NvM Blocks5
6Compiler Settings5
6.1Preprocessor MACRO5
6.2Optimization Settings5
7Revision Control Log5
Dependencies
NOTE – the TMS570_uDiag component includes both uDiag and FlsTst functionality. For complete integration information on the TMS570_uDiag component, also see the Cd_uDiag integration manual (in the TMS570_uDiag\doc folder).
SWCs
Module
Required Feature
NxtrLib
DtrmnElapsedTime_uS_u32()
GetSystemTime_uS_u32()
TMS570 CRC peripheral
Exclusive access to the CRC peripheral registers.
DiagMgr (Nexteer DEM)
NxtrDiagMgr_ReportNTCStatus() API
Basic System Services
EnableCRCInterrupt()
DMA
DMA register and control packet initialization
Dma_DisableFlsTstBlock()
Dma_SetupFlsTstBlock()
Dma_EnableFlsTstBlock()
Functions to be provided to Integration Project
< Global function (except the ones that are defined in RTE modules) that is defined in this component but used by other function>
void FlsTst_MainFunction( void );
void FlsTst_Init( const FlsTst_ConfigType* ConfigPtr );
void FlsTst_Suspend( void );
void FlsTst_Resume( void );
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
FlsTst_Cfg.c generated by FlsTst_Cfg.c.tt
FlsTst_Cfg.h generated by FlsTst_Cfg.h.tt
NOTES: The FlsTst module parameter description file and generator templates are located in the “generate” folder. The generation scheme at this time relies on the ARTT generation framework developed by BMW. Following are the recommended steps to integrate the provided generation templates and parameter description with Davinci Configurator:
Copy the “Artt/artt” framework folder into the “Generators” directory (if not already present)
Execute the “Integrate.bat” script from the Tools directory of this component to perform the necessary integration steps:
The script creates the required directories in the integration project, “Generators/Artt/FlsTst” and “Generators/Components/_Schemes/FlsTst/bswmd”
The script then copies the requir
```
*…excerpt ends here (3384 further characters in the source).*

## FlsTst_MDD.docx

- **Source:** `TMS570_uDiag/doc/FlsTst_MDD.docx`
- **Format:** `.docx` (~28 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5988 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TMS570_uDiag/doc/FlsTst_MDD.docx` for those.

```text
Module -- Flash Test
High-Level Description
This is module implements the FLASH Memory testing requirements specified in “EA3.x FDD 32 - uC Diagnostics 000D” according to the AUTOSAR “Specification of Flash Test v1.2.0 ” API definition. This SWC is TI TMS570 target specific.
This module extends the AUTOSAR API definition by including a hardware Self Test function and including support for hardware IRQ’s.
Figures
Diagram – Function Data Sharing
This diagram shows all data that is shared between functions within the module.
(Note – If no data is shared between functions, the Text “No Shared Data” can be used in place of a graphic. Also note that init functions need not be shown unless they compute non-zero data to be used by other functions in the module).
Diagram – Function (Name)
This diagram describes the functional characteristics and data flow of a given function.
(Note – This is not mandatory, only used where a graphical representation helps explain the function. It is left to the author’s discretion. New headers of this level (Level 3) should be created for each function.
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs
Module Outputs
<VarName_Units_Type>
<VarName_Units_Type>
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
<None>
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
(Name given for the user defined typdef of type struct/union)
(Variable name qualified similar to all other variables)
(Variable name qualified similar to all other variables)
as other variables
(Variable name qualified similar to all other variables)
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
<None>
Program(fixed) Constants
Embedded Constan
```
*…excerpt ends here (3488 further characters in the source).*

## OsErrCallouts_MDD.docx

- **Source:** `TMS570_uDiag/doc/OsErrCallouts_MDD.docx`
- **Format:** `.docx` (~136 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (4106 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TMS570_uDiag/doc/OsErrCallouts_MDD.docx` for those.

```text
High-Level Description
OsErrCallouts provides the error hook functions ErrorHook() and ProtectionHook() to provide diagnostic information for certain errors that result in calls to these hooks.
Figures
Diagram – Function Data Sharing
No Shared Data
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs
Module Outputs
None
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
<None>
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
None
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
UNUSEDINTERRUPT
STACKOVERWRITE
MPUVIOLATION
osdErrSOStackOverflow
osdErrYOStackOverflow
osdErrUEUnhandledException
Module specific Lookup Tables Constants
(This is for lookup tables (arrays) with fixed values, same name as other tables)
Constant Name
Resolution
Value
Software Segment
<None>
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
RednRpdShtdn()
Data Hiding Functions
OSErrorGetosCANError()
Global Functions/Macros Defined by this Module
Global Function #1
Function Name
ErrorHook
Type
Dir.
Min
Max
UTP Tol.
Arguments Passed
ErrorCode
StatusType
N/A
N/A
Return Value
N/A
Design Rationale
When the error was a
```
*…excerpt ends here (1606 further characters in the source).*

## Static-analysis outputs (30 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagCCRM.c.err` (~4 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagCCRM.c.met` (~232 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagClockMonitor.c.err` (~10 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagClockMonitor.c.met` (~276 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagECC.c.err` (~100 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagECC.c.met` (~381 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagESM.c.err` (~8 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagESM.c.met` (~255 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagFPU.c.err` (~10 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagFPU.c.met` (~314 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagIOMM.c.err` (~10 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagIOMM.c.met` (~250 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagLossOfExec.c.err` (~6 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagLossOfExec.c.met` (~232 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagParity.c.err` (~11 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagParity.c.met` (~312 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagPeriphMPU.c.err` (~5 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagPeriphMPU.c.met` (~252 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagResetHandler.c.err` (~3 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagResetHandler.c.met` (~240 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagStaticRegs.c.err` (~5 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagStaticRegs.c.met` (~228 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagVIM.c.err` (~9 KiB)
- `TMS570_uDiag/doc/QAC_Results/Cd_uDiagVIM.c.met` (~271 KiB)
- `TMS570_uDiag/doc/QAC_Results/FlsTst.c.err` (~8 KiB)
- `TMS570_uDiag/doc/QAC_Results/FlsTst.c.met` (~253 KiB)
- `TMS570_uDiag/doc/QAC_Results/OsErrCallouts.c.err` (~7 KiB)
- `TMS570_uDiag/doc/QAC_Results/OsErrCallouts.c.met` (~104 KiB)
- `TMS570_uDiag/doc/QAC_Results/RednRpdShtdn.c.err` (~5 KiB)
- `TMS570_uDiag/doc/QAC_Results/RednRpdShtdn.c.met` (~60 KiB)

</details>
