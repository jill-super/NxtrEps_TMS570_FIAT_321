---
title: "Battery Voltage Diagnostics documents"
description: "Word/PDF/text documents shipped with BVDiag (Battery Voltage Diagnostics) and their conversion status."
---

# Battery Voltage Diagnostics — documents

*Repository directory: `BVDiag`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## BVDiag_Integration_Manual.docx

- **Source:** `BVDiag/doc/BVDiag_Integration_Manual.docx`
- **Format:** `.docx` (~39 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (2892 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `BVDiag/doc/BVDiag_Integration_Manual.docx` for those.

```text
Integration Manual - BVDIAG
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
<None>
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be refered. Developer should track the references.
Global Functions(Non RTE) to be provided to Integration Project
< None>
Configuration
Build Time Config
Modules
Notes
<None>
Configuration Files to be provided by Integration Project
Ap_BVDiag_Cfg.h for checkpoint enables
Da Vinci Parameter Configuration Changes
Parameter
Notes
SWC
B1_BATTVOLTDIAG
This parameter will be turned ON only if customer requires $B1 NTC
STD_ON : Enables NTC $B1 logic
STD_Off : Disables NTC $B1 logic
B1_BATTVOLTDIAG_ELPW
This parameter will be turned ON if the customer requires $B1 NTC be enabled via input from SrlComInput via receiver port
STD_ON: Enables conditional setting of B1 via input
STD_OFF: Disables conditional setting of B1 via input
DaVinci Interrupt Configuration Changes
ISR Name
VIM #
Priority Dependency
Notes
<None>
Manual Configuration Changes
Constant
Notes
SWC
<None>
Integration
Required Global Data Inputs
Batt_Volt_f32 from SER
CCLMSAActive_Cnt_lgc (Note : Only required for BMW as per its SER)
Required Global Data Outputs
Sets BatteryVoltage Diagnostics
Specific Include Path present
No
Runnable Scheduling
This section specifies the required runnable scheduling.
Init
Scheduling Requirements
Trigger
None
None
Init
Runnable
Scheduling Requirements
Trigger
BVDiag_Per1
10ms
.
Memory Mapping
Mapping
Memory Section
Contents
Notes
BVDIAG_START_SEC_VAR_CLEARED_32
* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.
Usage
Feature
RAM
ROM
<Memmap usuage info>
Table 1: ARM Cortex R4 Memory Usage
Non RTE NvM Blocks
Block Name
<None >
Note : Size of the NVM block if configured in developer
RTE NvM Blocks
Block Name
None
Note : Size of the NVM block if configured in
```
*…excerpt ends here (392 further characters in the source).*

## Battery_Voltage_Diagnostics.doc

- **Source:** `BVDiag/doc/Battery_Voltage_Diagnostics.doc`
- **Format:** `.doc` (~916 KiB)
- **Kind:** Supporting document
- **Status:** summary record — legacy binary source retained at `BVDiag/doc/Battery_Voltage_Diagnostics.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

Supporting document for `BVDiag` (supporting document). Consult the binary original for figures, tables and formatted text.

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `BVDiag/doc/QAC_Results/Ap_BVDiag.c.err` (~50 KiB)
- `BVDiag/doc/QAC_Results/Ap_BVDiag.c.met` (~838 KiB)

</details>
