---
title: "Direct Memory Access Driver documents"
description: "Word/PDF/text documents shipped with Dma (Direct Memory Access Driver) and their conversion status."
---

# Direct Memory Access Driver — documents

*Repository directory: `Dma`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Dma Integration Manual.docx

- **Source:** `Dma/doc/Dma Integration Manual.docx`
- **Format:** `.docx` (~286 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (5983 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Dma/doc/Dma Integration Manual.docx` for those.

```text
Integration Manual – Dma
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
7Architectural Concerns7
7.1Overall DMA Architecture8
7.2Affected Modules9
7.2.1IoHwAbstractionUsr9
7.2.2Adc9
7.2.3MtrCtrl_Irq9
7.2.4uDiag10
8Revision Control Log12
Dependencies
SWCs
Module
Required Feature
Adc
Using ADC triggers for DMA transfers as well as ADC conversion group sizes to calculate buffer sizes. Only required if ADC DMA channels are enabled. Requires version FDD33C_008_and_FDD33E_002.3 or later.
SpiNxt
Using SPI Rx buffer full triggers for DMA transfers as well as SPI transfer group sizes to calculate DMA buffer sizes. Only required if SPI DMA channels are used. Requires version ASR038_2.3.0_8 or later.
uDiag
If the FlsTst channels are enabled, uDiag is responsible for initializing and enabling these blocks. Requires version FDD32B_TMS570_uDiag_000.24 or later.
ePWM
Using NHET triggers for DMA transfers as well as NHET program addresses for destination addresses. Only required if NHET DMA channels are enabled. Requires version FDD34B_EPWM_NHETSENT_005.0 or later.
TMS570_Startup
Note that the DMA parity functionality requires version FDD32B_TMS570_Startup_000.19 or later in the bootloader. Note that DMA MPU startup test functionality requires FDD32B_TMS570_startup_000.21 or later in the application.
DiagMgr
Error reporting mechanism required if either of the slow SPI or ADC channels are enabled.
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
Dma_Init
Dma_SlowADCGroupValidity
Dma_InvalidateSlowADCGroup
Dma_SetupMtrCtrlGroups
Dma_SetupFlsTstBlock
Dma_EnableFlsTstBlock
Dma_DisableFlsTstBlock
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
Dma_Cfg.h
```
*…excerpt ends here (3483 further characters in the source).*

## Dma_MDD.docx

- **Source:** `Dma/doc/Dma_MDD.docx`
- **Format:** `.docx` (~379 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5995 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Dma/doc/Dma_MDD.docx` for those.

```text
Module Design Document
For
DMA
Document Identifier: <Project_id>_<Config Id>
VERSION: 4
DATE: 31-Jan-2015
Location: The official version of this document is stored in the Nexteer Configuration Management System and is uniquely identified by: <Project_ID>_<Config Id>
Revision History
Sl. No.
Description
Author
Version
Date
1
Initial version
Owen Tosh
1
04-Apr-2014
2
Updated to FDD52 v001
Owen Tosh
2
29-Apr-2014
3
Updated to FDD52 v002
Owen Tosh
3
02-May-2014
4
Updated to ES-52 v004
Kathleen Creager
4
31-Jan-2015
Table of Contents
1Abbrevations And Acronyms5
2References6
3DMA & High-Level Description7
4Design details of software module8
4.1Graphical representation of DMA8
5Variable Data Dictionary9
5.1User defined typedef definition/declaration9
5.2Variable definition for enumerated types9
6Constant Data Dictionary10
6.1Program(fixed) Constants10
6.1.1Embedded Constants10
6.1.1.1Local10
6.1.1.2Global10
6.1.2Module specific Lookup Tables Constants10
6.1.3Library Functions / Macros10
6.1.4Data Hiding Functions11
7Software Module Implementation12
7.1Initialization Functions12
7.1.1Init: Dma _Init12
7.1.1.1Design Rationale12
7.1.1.1.1MPU Settings12
7.1.1.1.2Priority Assignments12
7.1.1.1.3FlsTst Group (Channels 0 and 1)12
7.1.1.2Initialize DMA Registers12
7.1.1.3Module Outputs12
7.1.1.4Module Internal13
7.2PERIODIC FUNCTIONS13
7.2.1Per: Dma _Per113
7.2.1.1Design Rationale13
7.2.1.2Store Module Inputs to Local copies13
7.2.1.3Clear DMA RAM Buffers13
7.2.1.4Store Local copy of outputs into Module Outputs13
7.3Interrupt Functions13
7.4TRANSIENT FUNCTIONS13
7.5Serial Communication Functions13
7.6Local Function/Macro Definitions13
7.7GLObAL Function/Macro Definitions13
7.7.1Setup MtrCtrl Groups13
7.7.1.1Description13
7.7.2Setup FlsTst Blocks14
7.7.2.1Description14
7.7.3Enable FlsTst Block14
7.7.3.1Description14
7.7.4Disable FlsTst Block14
7.7.4.1Description14
7.7.5Report DMA MPU Error14
7.7.5.1Description14
8Known Limitations With Design15
9UNIT TEST CONSIDERATION16
10Appendix A – Configuration Schemes17
Abbrevations And Acronyms
Abbreviation
Description
MDD
Module design Document
MtrCtrl ISR
Motor Control Interrupt Service Routine. This is the “fast” code loop that controls the main PWM signals.
References
This section Lists the title & version of all the documents that are referred for development of this document
Sr. No.
Title
Version
1
MDD Guidelines
1
2
Software Naming Conventions
1
3
Coding Standands
1
4
ES 52 – DMA
004
DMA & High-Level Description
DMA is a dri
```
*…excerpt ends here (3495 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `Dma/doc/QAC_Results/Dma.c.err` (~15 KiB)
- `Dma/doc/QAC_Results/Dma.c.met` (~119 KiB)

</details>
