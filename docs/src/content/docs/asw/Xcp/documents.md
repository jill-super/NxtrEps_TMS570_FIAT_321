---
title: "XCP Measurement and Calibration Interface documents"
description: "Word/PDF/text documents shipped with Xcp (XCP Measurement and Calibration Interface) and their conversion status."
---

# XCP Measurement and Calibration Interface — documents

*Repository directory: `Xcp`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## ApXcp_Integration_Manual.docx

- **Source:** `Xcp/doc/ApXcp_Integration_Manual.docx`
- **Format:** `.docx` (~80 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (5993 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `Xcp/doc/ApXcp_Integration_Manual.docx` for those.

```text
Integration Manual – ApXcp
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
GetSetIndexes() and GetPersIndexes()
Overview
The integration specific functions below, GetSetIndexes and GetPersIndexes, are used to return an array of tuning identifiers to the tune-on-the-fly (or online calibration as defined in the XCP specs) function. They are used to copy the active sets or personalities into RAM. The functions should be implemented in an integration specific component that determines the desired personality and desired set identifiers sent to tuning select authority SWC.
If tune-on-the-fly functionality is disabled, the functions below do not need to be defined.
If tune-on-the-fly is enabled and the lookup functions are disabled, the functions below do not need to be defined. When a copy cal page XCP command is called, the personalities are copied from 0 to a max limit based on the active tuning set that is currently being used. In the case of the tuning sets being copied, only the active tuning set is copied in to the RAM.
Module
Required API
<Integration Specific Module>
Function outline defined below:
Function Prototypes
The actual implementation of the function will vary between programs. However, the function should be structured so the passed arguments are of the same time to provide a common interface to the XCP functions.
Function Name
GetSetIndexes or GetPersndexes
Type
Dir.
Min
Max
UTP Tol.
Arguments Passed
NumOfSets_Cnt_T_u8orNumOfPers_Cnt_T_u8
uint8
I
0
255
data
uint8*
I/O
0
255
Return Value
N/A
Example 1 -- BMW
The following example illustrates a similar situation found in the BMW program. Active personalities are determined by coding bits. Using the GetPersIndexes function, the function will loop through the personalities to find the index of the personality that contains the matching coding ID. The indexes are returned and the active personalities are copied into RAM.
ProcessXCPPID()
Overview
This function must be available to this module to call
```
*…excerpt ends here (3493 further characters in the source).*
