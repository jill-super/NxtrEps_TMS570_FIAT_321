---
title: "Analog-to-Digital Converter Driver documents"
description: "Word/PDF/text documents shipped with Adc (Analog-to-Digital Converter Driver) and their conversion status."
---

# Analog-to-Digital Converter Driver — documents

*Repository directory: `Adc`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Adc2_MDD.docx

- **Source:** `Adc/doc/Adc2_MDD.docx`
- **Format:** `.docx` (~362 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5996 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Adc/doc/Adc2_MDD.docx` for those.

```text
Module – ADC2
High-Level Description
The ADC2 module shall control sampling and conversion of voltages from the hardware layer into digital signals.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
None
ADC2OffsetComp_Cnt_u8p8
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
See Adc_MDD.doc for Adc subsystem types
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
None
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
D_GROUPEV_CNT_U8
1
Counts
0
D_GROUP1_CNT_U8
1
Counts
1
D_GROUP2_CNT_U8
1
Counts
2
D_NTCPARMBIT1_CNT_U8
1
Counts
2
D_ADC2EVTBUFSZ_CNT_U08
1
Counts
Generated in Adc2_Cfg.h
D_ADC2G1BUFSZ_CNT_U08
1
Counts
Generated in Adc2_Cfg.h
D_ADC2G2BUFSZ_CNT_U08
1
Counts
Generated in Adc2_Cfg.h
D_ADC2EVSRC_CNT_U32
1
Counts
Generated in Adc2_Cfg.h
D_ADC2G1SRC_CNT_U32
1
Counts
Generated in Adc2_Cfg.h
D_ADC2G2SRC_CNT_U32
1
Counts
Generated in Adc2_Cfg.h
D_ADC2NUMEVTCH_CNT_U08
1
Counts
Generated in Adc2_Cfg.h
D_ADC2EVTCH_CNT_U32
1
Counts
Generated in Adc2_Cfg.h
D_ADC2NUMG1CH_CNT_U08
1
Counts
Generated in Adc2_Cfg.h
D_ADC2G1CH_CNT_U32
1
Counts
Generated in Adc2_Cfg.h
D_ADC2NUMG2CH_CNT_U08
1
Counts
Generated in Adc2_Cfg.h
D_ADC2G2CH_CNT_U32
1
Counts
Generated in Adc2_Cfg.h
D_ADC2RSLTBASEADR_CNT_U32
1
Counts
Generated in Adc2_Cfg.h
D_ADC2EVINTENA_CNT_U32
1
Counts
Generated in Adc2_Cfg.h
D_ADC2EVSAMPDISEN_CNT_U32
1
Counts
Generated in Adc2_Cfg.h
D_ADC2EVFIFORESETCR_CNT_U32
1
Counts
Generated in Adc2_Cfg.h
D_ADC2EVDMACR_CNT_U32
1
Counts
Generated in Adc2_Cfg.h
D_
```
*…excerpt ends here (3496 further characters in the source).*

## Adc_Common_MDD.docx

- **Source:** `Adc/doc/Adc_Common_MDD.docx`
- **Format:** `.docx` (~133 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (4248 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Adc/doc/Adc_Common_MDD.docx` for those.

```text
Module -- Adc Core
High-Level Description
The Adc Common module provides “stateless” application context independent functions which provide functionality required by both the Adc and Adc2 modules. In order to operate in any given application, the function design must not write to any fixed static variable location, unless it is in Globally shared memory. All static variable writes outside of Globally shared memory must be performed via pointer access where the caller provides the pointer reference to allowed writable memory in the application context from with the caller is executing.
The motivation for creating core functions is to reduce duplication and testing of common code design.
Figures
Component Diagram
None
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
None
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
None
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
None
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
D_NUMOFADCCALREADS_CNT_U8
1
Counts
128
Global
This section lists the global constants used by the module. For details on global constants, refer to the Data Dictionary for the application.
Constant Name
D_FALSE_CNT_LGC
D_TRUE_CNT_LGC
Module specific Lookup Tables Constants
Constant Name
Resolution
Value
Software Segment
None
Functions/Macros used by the Sub-Modules
Library Functions / Macros
The library and functions / Macros that are called by the various sub modules are identified below,
None
Data Hiding Functions
<None>
Global Functions/Macros Def
```
*…excerpt ends here (1748 further characters in the source).*

## Adc_MDD.docx

- **Source:** `Adc/doc/Adc_MDD.docx`
- **Format:** `.docx` (~327 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5992 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Adc/doc/Adc_MDD.docx` for those.

```text
Module -- ADC
High-Level Description
The ADC module shall control sampling and conversion of voltages from the hardware layer into digital signals. The ADC Register definition has been captured from the TMS570LS31x/21x 16/32-Bit RISC Flash Microcontroller Technical Reference Manual (SPNU499 – September 2011).
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
None
ADC1OffsetComp_Cnt_u8p8
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
Adc_GroupType
N/A
uint8
0
2
Adc_GroupConfigDataType
uint8 NumOfChannels,
uint32 ChannelSelect,
uint32* ResultBuf
struct
FULL
FULL
Adc_StatusType
ADC_IDLE,
ADC_BUSY,
ADC_COMPLETED,
ADC_STREAM_COMPLETED
enum
0
3
Adc_ValueGroupType
N/A
uint16
0
4095
Adc_ValueGroupType
N/A
uint16*
FULL
FULL
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
Constant Name
k_VbattOVTransIntConfig_Cnt_u32
Program(fixed) Constants
Embedded Constants
All embedded constants whose values are provided in Eng units will be evaluated to the equivalent counts by using the FPM_InitFixedPoint_m() macro within the #define statement.
Local
Constant Name
Resolution
Units
Value
D_NUMOFGROUPS_CNT_U8
1
Counts
3
D_GROUPEV_CNT_U8
1
Counts
0
D_GROUP1_CNT_U8
1
Counts
1
D_GROUP2_CNT_U8
1
Counts
2
D_NUMOFADCCALREADS_CNT_U8
1
Counts
8
D_NTCPARMBIT0_CNT_U8
1
Counts
1
D_NTCPARMBIT1_CNT_U8
1
Counts
2
D_NTCPARMBIT2_CNT_U8
1
Counts
4
D_ADC1RSLTBASEADR_CNT_U32
1
Counts
0xFF3E0000U
D_ADC1NUMRSLTBUF_CNT_U08
1
Counts
64
D_ADC1CURRENTMODE_ULS_LGC
1
BOOLEAN
Generated in Adc_Cfg.h.
D_ADC1MAGINTMASK1_CNT_U16
1
Counts
0/0*
D_ADC1MAGINTASET_CNT_U16
1
Counts
1/0*
D_ADC1MAGINTCR1_CNT_U32
1
Counts
k_VbattOVTransIntConfig_Cnt_u32/ 0*
D_ADC1THRINTENACLR_CNT_U16
1
Counts
6/7*
D_ADC1EVTBUFSZ_CNT_U08
1
Counts
Gener
```
*…excerpt ends here (3492 further characters in the source).*

## Integration_Manual_ADC.docx

- **Source:** `Adc/doc/Integration_Manual_ADC.docx`
- **Format:** `.docx` (~44 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (5982 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Adc/doc/Integration_Manual_ADC.docx` for those.

```text
Integration Manual –<Name of component>
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
3Integration6
3.1Required Global Data Inputs6
3.2Required Global Data Outputs6
3.3Specific Include Path present6
4Runnable Scheduling7
5Memory Mapping8
5.1Mapping8
5.2Usage8
5.3Non RTE NvM Blocks8
5.4RTE NvM Blocks8
6Compiler Settings8
6.1Preprocessor MACRO8
6.2Optimization Settings8
7Revision Control Log9
Dependencies
SWCs
Module
Required Feature
IoHwAbsUsr
Parts of the Adc FDDs (33C or 33E) are intended to be implemented at the integration level and are typically included in IoHwAbsUsr. Note that this includes implementation of NTC 0x32 and/or NTC 0x33 as needed for the specific application.
NOTE that as of FDD33C rev 008 and FDD33E rev 002, DMA-related updates are not included in the FDDs. The looping on group busy and associated timeouts and NTC setting should not be implemented when using with DMA; alternate means of getting the data when ready and associated fault setting are outlined in the DMA FDD ES-52.
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
Adc_Init() NOTE this is a macro mapped to Adc_Init_FixedCfg for Autosar interface compatibility. The Adc_Init macro takes a parameter which is not used by the function.
FUNC(void, ADC_CODE) Adc_StartGroupConversion(Adc_GroupType Group)
FUNC(Std_ReturnType, ADC_CODE) Adc_ReadGroup(Adc_GroupType Group, Adc_ValueGroupRefType DataBufferPtr)
FUNC(Adc_StatusType, ADC_CODE) Adc_GetGroupStatus(Adc_GroupType Group)
inline uint16 Adc2_ReadConversion(uint16 ConvId) NOTE this function directly accesses Adc RAM and should not be used when using DMA to transfer Adc data
void Adc2_Init1(void)
void Adc2_StartGroupConversion(uint8 group)
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Adc_Cfg.h and Adc2_Cfg.h. Configuration file templates are in the Tools folder.
NOTE:
For Projects using 33E, make sure “D_ADC1CURRENTMODE_ULS_LGC” is defined in Adc_Cfg.h file.
For Projects using 33C, make
```
*…excerpt ends here (3482 further characters in the source).*

## Static-analysis outputs (6 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `Adc/doc/QAC_Results/Adc.c.err` (~91 KiB)
- `Adc/doc/QAC_Results/Adc.c.met` (~127 KiB)
- `Adc/doc/QAC_Results/Adc2.c.err` (~93 KiB)
- `Adc/doc/QAC_Results/Adc2.c.met` (~135 KiB)
- `Adc/doc/QAC_Results/Adc_Common.c.err` (~2 KiB)
- `Adc/doc/QAC_Results/Adc_Common.c.met` (~42 KiB)

</details>
