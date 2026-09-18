---
title: "SPI Driver (Nexteer) documents"
description: "Word/PDF/text documents shipped with SpiNxt (SPI Driver (Nexteer)) and their conversion status."
---

# SPI Driver (Nexteer) — documents

*Repository directory: `SpiNxt`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Spi_Nexteer_Integration_Manual.docx

- **Source:** `SpiNxt/doc/Spi_Nexteer_Integration_Manual.docx`
- **Format:** `.docx` (~40 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (5982 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `SpiNxt/doc/Spi_Nexteer_Integration_Manual.docx` for those.

```text
Integration Manual -- Spi Nexteer
Contents
1Dependencies1
1.1SWCs1
1.2Global Functions(Non RTE) to be provided to Integration Project2
2Configuration2
2.1Build Time Config2
2.2Configuration Files to be provided by Integration Project2
2.2.1Da Vinci Parameter Configuration Changes2
2.2.2Da Vinci Interrupt Configuration Changes3
2.2.3Manual Configuration Changes3
3Integration4
3.1Required Global Data Inputs4
3.2Required Global Data Outputs4
3.3Specific Include Path present4
4Runnable Scheduling5
5Memory Mapping5
5.1Mapping5
5.2Usage5
5.3Non RTE NvM Blocks5
5.4RTE NvM Blocks5
6Compiler Settings5
6.1Preprocessor MACRO5
6.2Optimization Settings6
Dependencies
SWCs
Module
Required Feature
Dio
Dio_WriteChannel() when SpiNxt used with Turns Counter
TMS570 MIBSPI3 and MIBSPI5 peripheral
Exclusive access to the MIBSPI3 and MIBSPI5 peripheral registers.
MIBSPI3 CS3 provided as a No Connect pin on CCA design when SpiNxt used with Turns Counter
Os
Category 2 ISR mapping for MIBSPI3 IRQ sources when SpiNxt used with Turns Counter
TurnsCounter
TurnsCounter_TxConfirmation() when SpiNxt used with Turns Counter
ePWM
Must provide SPI transmit trigger on N2HET1[14] for mibspi3, and N2HET1[18] for mibspi5, when SpiNxt used with Digital MSB.
Global Functions(Non RTE) to be provided to Integration Project
void SpiNxt_Init(void);
Std_ReturnType SpiNxt_AsyncTransmit( Spi_SequenceType Sequence );NOTE that this function is hardcoded for use with the Turns Counter component and returns E_NOT_OK when SpiNxt not configured for use with Turns Counter (see section 2.2.1).
Spi_SeqResultType SpiNxt_GetSequenceResult( Spi_SequenceType Sequence );
Std_ReturnType SpiNxt_SetupEB( Spi_ChannelType Channel, P2CONST(Spi_DataType, AUTOMATIC, SPI_APPL_DATA) SrcDataBufferPtr, P2VAR(Spi_DataType, AUTOMATIC, SPI_APPL_DATA) DesDataBufferPtr, Spi_NumberOfDataType Length);NOTE that this function is hardcoded for use with the Turns Counter component and returns E_NOT_OK when SpiNxt not configured for use with Turns Counter (see section 2.2.1).
void mibspiSetData(const mibspiBASE_t *mibspi, uint32 group, const uint16 data[]);
void mibspiSetCtrlData(const mibspiBASE_t *mibspi, uint32 group, const uint32 data[]);
uint32 mibspiGetData(const mibspiBASE_t *mibspi, uint32 group, uint16 data[]);NOTE this function is optimized for use by the Digital MSB component when SpiNxt is configured for use with Digital MSB (see section 2.2.1). In that configuration, the mibspi argument must be equal to the base register addre
```
*…excerpt ends here (3482 further characters in the source).*

## Spi_Nexteer_MDD.docx

- **Source:** `SpiNxt/doc/Spi_Nexteer_MDD.docx`
- **Format:** `.docx` (~1410 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5990 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `SpiNxt/doc/Spi_Nexteer_MDD.docx` for those.

```text
Module -- Spi Driver
High-Level Description
This module provides the following Autosar API:
Spi_SetupEB()
Spi_Init()
Spi_AsyncTransmit()
Spi_GetSequenceResult()
This module provides the following TI Halcogen API:
mibspiSetCtrlData() – Note: this is a modified form of the standard mibspiSetData() API
mibspiTransfer()
mibspiGetData()
mibspiSetData()
The Autosar API naming has been altered from the Autosar standard to allow co-existence of this module and a Third Party Spi driver implementation in the same project. SWC’s operating within the Rte can be mapped to either the Spi service ports offered by this BSW or the Third Parties Spi driver service ports by only changing the Rte service port mapping.
This driver exists to provide configurations/use cases that cannot provided by the third party Spi driver due to limitations in the design of the module.
The subset of the Texas Instruments Halcogen mibspi API is provided specifically to support the Turns Counter Flash Programming SWC and the Digital MSB SWC. If the Turns Counter Flash Programming SWC design and the Digital MSB design changed to use the standard Autosar API, then the provided mibspi API could be changed to module internal functions or removed. However, the requirements of the Digital MSB component are such that its SPI usage does not fit easily into the Autosar API definition (more detail provided in section 9).
References
PIC16(L)F1847 Data Sheet – DS41453B (41453B.pdf)
Turns Counter Column Position Sensor FDD 20C (FDD 20C Turns Counter Column Position Sensor (BMW EA3) Rev 03.doc)
TMS570LS31x/21x 16/32-Bit RISC Flash Microcontroller Technical Reference Manual – September 2011 (spnu499.pdf)
Specification of the SPI Handler/Driver v3.0.0 (AUTOSAR_SWS_SPIHandlerDriver.pdf)
Turns Counter Flash Programming FDD 98 Rev 002
Digital MSB FDD ES50ARev005 7-Feb-14
Allegro A1331 Data Sheet Addendum – Programming Reference A1331-ADD1
Figures
Diagram – Function Data Sharing
This diagram shows all data that is shared between functions within the module.
Diagram – Function (Name)
This diagram describes the functional characteristics and data flow of a given function.
(Note – This is not mandatory, only used where a graphical representation helps explain the function. It is left to the author’s discretion. New headers of this level (Level 3) should be created for each function.
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output
```
*…excerpt ends here (3490 further characters in the source).*

## Static-analysis outputs (4 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `SpiNxt/doc/QAC_Results/SpiNxt.c.err` (~6 KiB)
- `SpiNxt/doc/QAC_Results/SpiNxt.c.met` (~105 KiB)
- `SpiNxt/doc/QAC_Results/SpiNxt_Irq.c.err` (~5 KiB)
- `SpiNxt/doc/QAC_Results/SpiNxt_Irq.c.met` (~91 KiB)

</details>
