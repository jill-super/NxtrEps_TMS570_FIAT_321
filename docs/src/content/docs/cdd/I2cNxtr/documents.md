---
title: "I²C Driver (Nexteer) documents"
description: "Word/PDF/text documents shipped with I2cNxtr (I²C Driver (Nexteer)) and their conversion status."
---

# I²C Driver (Nexteer) — documents

*Repository directory: `I2cNxtr`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## I2cNxtr_Integration_Manual.docx

- **Source:** `I2cNxtr/doc/I2cNxtr_Integration_Manual.docx`
- **Format:** `.docx` (~35 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (5416 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `I2cNxtr/doc/I2cNxtr_Integration_Manual.docx` for those.

```text
Integration Manual – I2cNxtr
Table of Contents
1Dependencies2
1.1SWCs2
1.2Global Functions(Non RTE) to be provided to Integration Project2
2Configuration3
2.1Build Time Config3
2.2Configuration Files to be provided by Integration Project3
2.2.1Da Vinci Parameter Configuration Changes3
2.2.2DaVinci Interrupt Configuration Changes3
2.2.3Interrupt Enable/Disable Functions3
2.2.4Manual Configuration Changes4
3Integration5
3.1Required Global Data Inputs5
3.2Required Global Data Outputs5
3.3Specific Include Path present5
4Runnable Scheduling6
5Memory Mapping7
5.1Mapping7
5.2Usage7
5.3Non RTE NvM Blocks7
5.4RTE NvM Blocks7
6Compiler Settings7
6.1Preprocessor MACRO7
6.2Optimization Settings7
7Revision Control Log8
Dependencies
SWCs
Module
Required Feature
None
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
I2c_Init
I2c_Enable
I2c_Reset
I2c_SetupMasterTransmit
I2c_SetupMasterReceive
I2c_SwitchMasterReceive
I2c_SetCount
I2c_SetOwnAdd
I2c_SetSlaveAdd
I2c_SetFunctional
I2c_SetBaudrate
I2c_IsTxReady
I2c_SendByte
I2c_Send
I2c_IsRxReady
I2c_RxError
I2c_ReceiveByte
I2c_SetRecv
I2c_SetDirection
I2c_SetBit
I2c_GetBit
I2c_EnableNotification
I2c_DisableNotification
I2c_GenStartCond
I2c_GenStopCond
I2c_GetIntVect
I2c_GetStatus
I2c_SetStatus
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
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
Isr_I2c
66
None
See comment below about enable/disable for very low priority interrupts.
Interrupt Enable/Disable Functions
Verify that interrupt 66 can be enabled and disabled in interrupts.c. It was found that only interrupts up to 63 could be enabled and disabled with current code. Below is a suggestion of how the enable function should look:
FUNC(void, INTERRUPT_CODE) EnableIrq(uint8 irqRequest){ if (irqRequest < 32) { osWritePeripheral32(OS_MEM_AREA_VIM, (osuint32)&(VIM->REQMASKSET0), (((osuint32)1) << (irqRequest))); } else if (irqRequest < 64) { irqRequest -= 32; osWritePeripheral32(OS_MEM_AREA_VIM, (osuint32)&(VIM->REQMASKSET1), (((osuint32)1) << (irqRequest))); } else { irqRequest -= 64; osWritePeripheral32(OS_MEM_AREA_VIM, (osuint32)&(VIM->REQMASKSET2), (((osuint32)1) << (irqReq
```
*…excerpt ends here (2916 further characters in the source).*

## I2cNxtr_MDD.docx

- **Source:** `I2cNxtr/doc/I2cNxtr_MDD.docx`
- **Format:** `.docx` (~1013 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5994 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `I2cNxtr/doc/I2cNxtr_MDD.docx` for those.

```text
Module -- I2C Nexteer
This document describes the software design and implementation of the Nexteer inter-integrated circuit (I2C) driver for EA3.x applications.
Equations for Register Settings
Depending on the type of device attached to the I2C bus different register settings may be required. The following equations were used to determine the module clock frequency and high and low times for the required device that are documented in this MDD.
Module Clock Frequency
The module clock frequency determines the frequency at which the I2C module operates. The value in the prescale register (I2CPSC) is programmable and divides the input clock to produce the module clock. The module clock frequency must be between 6.7 MHz and 13.3 MHz for proper operation of the I2C module. At the time this specification was created, the input clock frequency is 80MHz.
Master Clock Frequency
The master clock frequency is the frequency that will be used on the SCL pin of the TMS570 device when in master mode. Depending on the value of the I2CPSC and the desired clock low (I2CCKL) and high (I2CCKH) times, the mast clock frequency can be calculated by one of the two equations below:
Where d depends on:
I2CPSC
d
0
7
1
6
Greater than 1
5
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
I2cNxtr_I2cTransfer_Cnt_M_str. Mode_Cnt_b32
1
0
0x10
I2CNXTR_START_SEC_VAR_CLEARED_UNSPECIFIED
I2cNxtr_I2cTransfer_Cnt_M_str. Length_Cnt_u32
1
FULL
FULL
I2CNXTR_START_SEC_VAR_CLEARED_UNSPECIFIED
I2cNxtr_I2cTransfer_Cnt_M_str. DataPtr_Cnt_u08
1
FULL
FULL
I2CNXTR_START_SEC_VAR_CLEARED_UNSPECIFIED
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
i2cctrlregs_t
OAR
IMR
STR
CLKL
CLKH
CNT
DRR
SAR
DXR
MDR
IVR
EMDR
PSC
PID11
PID12
DMAC
FUN
DIR
DIN
DOUT
SET
CLR
ODR
PD
PSL
uint32
uint32
uint32
uint32
uint32
uint32
uint32
uint32
uint32
uint32
uint32
uint32
uint32
uint32
uint32
uint32
uint32
```
*…excerpt ends here (3494 further characters in the source).*

## Static-analysis outputs (4 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `I2cNxtr/doc/QAC_Results/I2cNxtr.c.err` (~4 KiB)
- `I2cNxtr/doc/QAC_Results/I2cNxtr.c.met` (~102 KiB)
- `I2cNxtr/doc/QAC_Results/I2cNxtr_Irq.c.err` (~3 KiB)
- `I2cNxtr/doc/QAC_Results/I2cNxtr_Irq.c.met` (~63 KiB)

</details>
