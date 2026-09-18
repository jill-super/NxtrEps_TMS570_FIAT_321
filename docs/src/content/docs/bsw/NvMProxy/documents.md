---
title: "NVRAM Proxy documents"
description: "Word/PDF/text documents shipped with NvMProxy (NVRAM Proxy) and their conversion status."
---

# NVRAM Proxy — documents

*Repository directory: `NvMProxy`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## NvMProxy_Integration_Manual.docx

- **Source:** `NvMProxy/doc/NvMProxy_Integration_Manual.docx`
- **Format:** `.docx` (~45 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (5973 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `NvMProxy/doc/NvMProxy_Integration_Manual.docx` for those.

```text
Integration Manual – NvM Proxy
Table of Contents
1Dependencies2
1.1SWCs2
1.2Functions to be provided to Integration Project2
2Configuration3
2.1Build Time Config3
2.2Configuration Files to be provided by Integration Project3
2.2.1Da Vinci Config generation3
2.2.2Manual Configuration Changes3
3Integration4
3.1Required Global Data Inputs4
3.2Optional Global Data Inputs4
3.3Specific Include Path present4
4Runnable Scheduling5
5Memory Mapping6
5.1Mapping6
5.2Usage6
5.3NvM Blocks6
6Compiler Settings6
6.1Preprocessor MACRO6
6.2Optimization Settings6
7Revision Control Log7
Dependencies
SWCs
Module
Required Feature
NvM
NvM_WriteBlock()
NvM_GetBlockStatus()
DiagMgr
NxtrDiagMgr#_ReportNTCStatus()
Crc
Crc_CalculateCRC16()
Global Functions(Non RTE) to be provided to Integration Project
NvMProxy_Init
NvMProxy_MainFunction
NvMProxy_WriteBlock
NvMProxy_WriteAll
NvMProxy_GetErrorStatus
NvMProxy_SetRamBlockStatus
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
NvMProxyConfigSet/NvMProxyBlock/NvmRamBlockDataAddressSecure
The symbol name of the secured buffer location for the block data
NOTE: For blocks defined by PIM memory in the Rte, this parameter is the symbol name that Developer inserts into the NvM Ram block configuration parameter for the associated NvM block)
NvMProxy
NvMProxyConfigSet/NvMProxyBlock/InitBlockHandling
This parameter chooses the type of protection handling done on the block at initialization:
None: No specific handling needed
CRC16: Run a 16 bit CRC on the NvM block and check it against the CRC stored in the NvM block (last two bytes). Failures will trigger the fail action specified in the “InitCheckFailResponse” configuration
Redundant: Run redundant storage check on the NvM block. The 1’s compliment of the block data is stored in the NvM block to protect against corruption. Failures will trigger the fail action specified in the “InitCheckFailResponse” configuration
ZeroData: Ignore what is stored in NvM and always over-ride the NvM RAM buffer with zeros. This is useful for blocks that may be un
NvMProxy
NvMProxyConfigSet/NvMProxyBlock/InitCheckFailResponse
Defines the type of response to occur if the NvM block fails either the CRC16 or Redundant check at initialization:
N/A: This should be chosen if the block doesn’t have CRC16 or Redundant InitBlockHandling turned on
SetNTC_0x0A: This should be chosen to set NTC 0x0A (should be
```
*…excerpt ends here (3473 further characters in the source).*

## NvMProxy_MDD.docx

- **Source:** `NvMProxy/doc/NvMProxy_MDD.docx`
- **Format:** `.docx` (~736 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5988 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `NvMProxy/doc/NvMProxy_MDD.docx` for those.

```text
Module -- NvM Proxy
High-Level Description
(Description must be within 8-10 lines.)
Figures
Diagram – Function Data Sharing
This diagram depicts the physical memory allocation for the various parts of the NvM Proxy system. 3 application RAM areas are shown for illustrative purposes, however, this module can handle any number of application RAM areas.
The memory stack components below the NvM are not shown in this diagram to promote clarity.
The NvMProxy_CmdQueue is required to be allocated to global shared memory to provide write access to the Proxy server function that is designed to be called from any application.
Diagram – NvM Data Initialization
Depiction of the Nv Data initialization sequence from the perspective of which application is active (i.e. MPU configuration at the time of operation execution)
Only pertinent initialization functions and steps are shown to promote clarity.
Diagram – NvM Runtime
Following is a depiction of the write Motor Position EOL calibrations via diagnostic service request. The MtrPos component is assumed to be running in the ASIL D application and its server runnable for processing an EOL motor cal write request is assumed to invoke the NvM_WriteBlock operation.
The lifelines in this diagram represent execution within the Os or an application. The details of the diagnostic service request are omitted from this diagram for clarity purposes.
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
Configured by NvMProxyCfg
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
NvMPWriteRqst_Cnt_M_Str[D_NUMPRXYBLOCKS_CNT_U16]
See NvMPWriteBuff_Type
See NvMPWriteBuff_Type
See NvMPWriteBuff_Type
NVMPROXY_START_SEC_VAR_CLEARED_UNSPECIFIED
NvMPSetRBSRqst_Cnt_M_Str[D_NUMPRXYBLOCKS_CNT_U16]
See NvMPSetRBSBuff_Type
See NvMPSetRBSBuff_Type
See NvMPSetRBSBuff_Type
NVMPROXY_START_SEC_VAR_CLEARED_UNSPECIFIED
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Typedef Name
Element Name
User Defined Type
Legal Range
(min)
Legal Range
(max)
NvMProxyCfg_Type
NvMBlo
```
*…excerpt ends here (3488 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `NvMProxy/doc/QAC_Results/Cd_NvMProxy.c.err` (~10 KiB)
- `NvMProxy/doc/QAC_Results/Cd_NvMProxy.c.met` (~59 KiB)

</details>
