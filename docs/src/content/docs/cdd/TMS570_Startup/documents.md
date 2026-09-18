---
title: "TMS570 Startup (System, Boot and Interrupt Vectors) documents"
description: "Word/PDF/text documents shipped with TMS570_Startup (TMS570 Startup (System, Boot and Interrupt Vectors)) and their conversion status."
---

# TMS570 Startup (System, Boot and Interrupt Vectors) — documents

*Repository directory: `TMS570_Startup`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## TMS570_Startup_BootStartup_MDD.docx

- **Source:** `TMS570_Startup/doc/TMS570_Startup_BootStartup_MDD.docx`
- **Format:** `.docx` (~117 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (4548 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TMS570_Startup/doc/TMS570_Startup_BootStartup_MDD.docx` for those.

```text
Module -- TMS570 Startup - Boot Startup
High-Level Description
This module outlines the functionality of the system startup functions of the TMS570. This code is intended to be run starting after the sys startup routine in the boot project.
Figures
Diagram – Function Data Sharing
This diagram shows all data that is shared between functions within the module.
No Shared Data
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
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
Value
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
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
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
<None>
Data Hiding Functions
<None>
Global Functions/Macros Defined by this Module
Global Function #1
Function Name
(Exact name used)
Type
Min
Max
UTP Tol.
Arguments Passed
(if none, write None)
(Insert more rows for additional passed arguments)
Return Value
(if no value returned, write N/A)
Description
(Place flowchart/design for local function)
Local Functions/Macros Used by this MDD only
Local Function #1
Function Name
(Exact name used)
Type
Min
Max
UT
```
*…excerpt ends here (2048 further characters in the source).*

## TMS570_Startup_FiqIntVect_MDD.docx

- **Source:** `TMS570_Startup/doc/TMS570_Startup_FiqIntVect_MDD.docx`
- **Format:** `.docx` (~35 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (4873 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TMS570_Startup/doc/TMS570_Startup_FiqIntVect_MDD.docx` for those.

```text
High-Level Description
fiqintvect provides the assembly language fiq handling function. The function loads the program counter with the value of the FIQ Interrupt Vector Register, which contains the address of the ISR with the highest priority pending FIQ request.
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
NOTE that all global functions in this module must be assembled in ARM mode. Therefore the .asm source file includes the .arm directive at the beginning of the file, applying the directive to all functions in the file.
```
*…excerpt ends here (2373 further characters in the source).*

## TMS570_Startup_Integration_Manual.docx

- **Source:** `TMS570_Startup/doc/TMS570_Startup_Integration_Manual.docx`
- **Format:** `.docx` (~44 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (5981 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TMS570_Startup/doc/TMS570_Startup_Integration_Manual.docx` for those.

```text
Integration Manual -- TMS570 Startup
Table of Contents
1Dependencies2
1.1SWCs2
1.2Functions to be provided to Integration Project2
1.3Functions to be provided by Integration Project2
2Configuration2
2.1Build Time Config2
2.2Configuration Files to be provided by Integration Project2
2.2.1startup_cfg.h3
2.2.2appinit_cfg.h3
2.3DaVinci Config Configuration Changes3
2.4Manual Configuration Changes3
3Integration3
3.1Required Global Data Inputs3
3.2Optional Global Data Inputs3
3.3Specific Include Path present3
3.4Build Exclusions3
3.5Definition of Stacks4
3.6Reset Causes4
3.7Impact on Integration Project6
3.7.1JTAG Debugger Considerations6
3.7.2RAM Memory State7
3.7.3ECC and Parity7
4Runnable Scheduling7
5Memory Mapping7
5.1.resetcause Section7
5.2Mapping7
5.3Usage7
5.4NvM Blocks8
6Compiler Settings8
6.1Preprocessor MACRO8
6.2Optimization Settings8
6.3Other Settings8
7Revision Control Log8
Dependencies
SWCs
Module
Required Feature
StdDef
TMS570 Register Definitions
Functions to be provided to Integration Project
void _fiqhandler(void);
uint32 _coreGetDebugStatusAndControlRegister_(void);
uint32 _coreGetSecondaryAuxiliaryControlRegister_(void);
void _coreSetSecondaryAuxiliaryControlRegister_(uint32 SecAuxCtrlRegVal_Cnt_T_u32);
uint32 _coreGetFPSCR_(void);
Functions to be provided by Integration Project
All common functionality required for a boot project startup is contained in “BootStartup.c”, and all common functionality for application project startup is contained in “AppStartup.c”. There may be instances, however, where a boot or application project will need to do special steps that are specific to a particular program, prior to the “main()” function call. To accommodate this, several functions are called, one at the start and one at the end of both BootStartup.c and AppStartup.c. These functions are
void BootStartupCallout1(void)
void BootStartupCallout2(void)
void AppStartupCallout1(void)
void AppStartupCallout2(void)
The integration projects are required to provide these functions, regardless of if there is content in them.
Configuration
Build Time Config
Modules
Notes
SWC
None
Configuration Files to be provided by Integration Project
Configuration files are needed to configure the startup sequence based on the needs of the program being implemented in. These configuration files are simply header files that define a set of build constants. Templates of these files are provided (located in the tools folder of this SWC) that can be adapted to the needs of th
```
*…excerpt ends here (3481 further characters in the source).*

## TMS570_Startup_SysCore_MDD.docx

- **Source:** `TMS570_Startup/doc/TMS570_Startup_SysCore_MDD.docx`
- **Format:** `.docx` (~45 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5624 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TMS570_Startup/doc/TMS570_Startup_SysCore_MDD.docx` for those.

```text
High-Level Description
sys_core provides assembly language functions for processor register data access and system startup.
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
NOTE that all global functions in this module must be assembled in ARM mode. Therefore the .asm source file includes the .arm directive at the beginning of the file, applying the directive to all functions in the file.
Global Function #1
Function Name
_coreEnableVfp_
Type
Dir.
Min
Max
UTP Tol.
Arguments Passed
None
Return Value
None
Description
Enables VFP
```
*…excerpt ends here (3124 further characters in the source).*

## TMS570_Startup_SysStartup_MDD.docx

- **Source:** `TMS570_Startup/doc/TMS570_Startup_SysStartup_MDD.docx`
- **Format:** `.docx` (~2003 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5992 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `TMS570_Startup/doc/TMS570_Startup_SysStartup_MDD.docx` for those.

```text
Module -- TMS570 Startup - SysStartup
High-Level Description
This module outlines the functionality of the system startup functions of the TMS570. This code is intended to be run starting at the reset vector.
Figures
Diagram – Function Data Sharing
This diagram shows all data that is shared between functions within the module.
No Shared Data
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
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
<None>
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
Value
enum systemClockSource
SYS_OSC
0
SYS_PLL1
1
SYS_EXTERNAL1
3
SYS_LPO_LOW
4
SYS_LPO_HIGH
5
SYS_PLL2
6
SYS_EXTERNAL2
7
SYS_VCLK
9
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
D_OTP1BITERRADDR_CNT_U32
1
Counts
0xF00803F4
D_OTP2BITERRADDR_CNT_U32
1
Counts
0xF00803FC
D_DPRAMSELECT_CNT_U32
1
Counts
0x4
D_SPRAMSELECT_CNT_U32
1
Counts
0x8
D_EFCAUTOLOADERROREN_CNT_U32
1
Counts
0x00040000
D_EFCINSTRUCTIONERROREN_CNT_U32
1
Counts
0x00080000
D_EFCINSTRUCTIONINFOEN_CNT_U32
1
Counts
0x00100000
D_EFCSELFTESTERROREN_CNT_U32
1
Counts
0x00200000
D_EFCSELFTESTDONE_CNT_U32
1
Counts
0x00008000
D_EFCSELFTESTERROR_CNT_U32
1
Counts
0x00004000
D_OUTPUTENABLE_CNT_U32
1
Counts
0x0003C000
D_SELFTESTERROR_CNT_U32
1
Counts
0x18
D_LPOTRIMVALUE_CNT_U32
1
Counts
((*(uint32*)0xF00801B4) & 0xFFFF0000)>>16
D_PLLSLIPMASK_CNT_U32
1
Counts
0x00000300
D_LOWBYTEMASK_CNT_U32
1
Counts
0x0000000FFUL
D_CURRENTLPOTRIMMASK_CNT_U32
1
Counts
0x00000FFFFUL
D_LPOMONLFTRIMMASK_CNT_U32
1
Counts
0xFFFFFF00UL
D_LPOMONHFTRIMMASK_CNT_U32
1
Count
```
*…excerpt ends here (3492 further characters in the source).*

## spna106a.pdf

- **Source:** `TMS570_Startup/doc/spna106a.pdf`
- **Format:** `.pdf` (~125 KiB)
- **Kind:** Reference document (PDF)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `TMS570_Startup/doc/spna106a.pdf` for those.

```text
Application Report
SPNA106A –January 2012
Initialization of Hercules™ ARM® Cortex™-R4F
Microcontrollers
Sunil Oak........................................................................................................................................
ABSTRACT
This application report provides a brief overview and initialization procedure of the TMS570LS31x series
and the RM4x series of microcontrollers in the Hercules family. "Hercules MCU" will be used henceforth in
this document to refer to any part in these series of microcontrollers.
The document also shows code fragments from source files that are generated using the HALCoGen tool.
All code constructs used in this document are defined in header files also generated by the same utility.
Project collateral and source code discussed in this application report can be downloaded from the
following URL: http://www.ti.com/lit/zip/spna106.
Contents
1 Block Diagram ............................................................................................................... 2
2 Standard Initialization Sequence for Hercules Microcontrollers ...................................................... 3
3 References ............................
```
*…excerpt ends here (4800 further characters in the source).*

## Static-analysis outputs (4 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `TMS570_Startup/doc/QAC_Results/AppStartup.c.err` (~75 KiB)
- `TMS570_Startup/doc/QAC_Results/AppStartup.c.met` (~476 KiB)
- `TMS570_Startup/doc/QAC_Results/sys_startup.c.err` (~48 KiB)
- `TMS570_Startup/doc/QAC_Results/sys_startup.c.met` (~374 KiB)

</details>
