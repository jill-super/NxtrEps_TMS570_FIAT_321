---
title: "High-Load Stall Thermal Management documents"
description: "Word/PDF/text documents shipped with HiLoadStall (High-Load Stall Thermal Management) and their conversion status."
---

# High-Load Stall Thermal Management — documents

*Repository directory: `HiLoadStall`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## HiLoadStall_MDD.docx

- **Source:** `HiLoadStall/doc/HiLoadStall_MDD.docx`
- **Format:** `.docx` (~1635 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5966 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `HiLoadStall/doc/HiLoadStall_MDD.docx` for those.

```text
Module -- HiLoadStall
High-Level Description
The High Load Stall Thermal Management algorithm protects the system from prolonged intervals of high assist torque at near-stall conditions.
Figures
Diagram – Function Data Sharing
This diagram shows all data that is shared between functions within the module.
None
Diagram – Ret HiLoadStall _Per1
This diagram describes the functional characteristics and data flow of a given function.
Module Inputs and Outputs
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
(Note: Full variable names required in table.)
(Note: All global variables including End Of Line data used should be shown here)
Module Inputs (Global Variable Name)
Module Outputs (Global Variable Name)
MtrVelCRF_MtrRadpS_f32
AssistStallLimit_MtrNm_f32
PreLimitForStall_MtrNm_f32
DftStallLimit_Cnt_lgc
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
(Note: If no module specific variables are used by the design, place the text “None” in the first Variable Name cell in the table)
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
PrevAssistStallLimit_MtrNm_M_f32
Single Precision Floating Point
0
8.8
HILOADSTALL_START_SEC_VAR_CLEARED_32
ModPreLimitFiltSV_MtrNm_M_u8p24
2^-24
0
8.8
HILOADSTALL_START_SEC_VAR_CLEARED_32
ModPreLimit_MtrNm_D_u8p8
0.00390625
0
8.8
HILOADSTALL_START_SEC_VAR_CLEARED_16
FiltModPreLimit_MtrNm_D_u8p8
0.00390625
0
8.8
HILOADSTALL_START_SEC_VAR_CLEARED_16
StallLimit_MtrNm_D_u8p8
0.00390625
0
8.8
HILOADSTALL_START_SEC_VAR_CLEARED_16
User defined typedef definition/declaration
This section documents any user types uniquely used for the module.
Variable Name
Typedef Name
Storage Type
Safety Critical Classification
None
Constant Data Dictionary
Calibration Constants
This section lists the calibrations used by the module. For details on calibration constants, refer to the Data Dictionary for the application.
(Note: If no calibrations are used by the design, place the text “None” in the first location in the table)
Constant Name
k_AbsMtrVelBkt_MtrRadps_f32
k_EOTThrmPrtLPFKn_Cnt_u16
t_EOTThrmIndptTbl_MtrNm_u8p8
t_EOTThrmDpntTbl_MtrNm_u8p8
k_EOTThrmSlwLmtStp_MtrNm_f32
Program(fixed) Constants
Embedded Constants
All embedded con
```
*…excerpt ends here (3466 further characters in the source).*

## logfile.txt

- **Source:** `HiLoadStall/tools/logfile.txt`
- **Format:** `.txt` (~2 KiB)
- **Kind:** Tool log file (generator transcript)
- **Status:** converted in full (plain text embedded below).

Generator transcript (first lines; full log retained in the repository):

```text

MICROSAR RTE Generator Version 2.17.2
Copyright c 2001-2010 Vector Informatik GmbH
License CBD1010122 valid for CBD1010122 Nexteer  GM MSR_SLP3_BSW_RTE_wGMLAN TexasInstruments TMS570 Texas Instruments
Loading profile settings from file 'C:\Documents and Settings\nzt9hv\My Documents\Synergy\ccm_wa\ESG_Dev_65\HiLoadStall-nzt9hv\HiLoadStall\autosar\ProfileSettings.xml'.
Failed to load profile settings from file 'C:\Documents and Settings\nzt9hv\My Documents\Synergy\ccm_wa\ESG_Dev_65\HiLoadStall-nzt9hv\HiLoadStall\autosar\ProfileSettings.xml'. Applying default settings.

Importing AUTOSAR XML-exchange file <C:\Documents and Settings\nzt9hv\My Documents\Synergy\ccm_wa\ESG_Dev_65\HiLoadStall-nzt9hv\HiLoadStall\autosar\ComponentTypes\Ap_HiLoadStall.arxml>...
Using DaVinci AUTOSAR V3.1.4 (XSD rev. 0004), SHORT-NAMEs with up to 128 characters
file is valid

Importing AUTOSAR XML-exchange file <C:\Documents and Settings\nzt9hv\My Documents\Synergy\ccm_wa\ESG_Dev_65\HiLoadStall-nzt9hv\HiLoadStall\autosar\Constants.arxml>...
Using DaVinci AUTOSAR V3.1.4 (XSD rev. 0004), SHORT-NAMEs with up to 128 characters
file is valid

Importing AUTOSAR XML-exchange file <C:\Documents and Settings\nzt9hv\My Documents\Synergy\ccm_wa\ESG_Dev_65\HiLoadStall-nzt9hv\HiLoadStall\autosar\DataTypes.arxml>...
Using DaVinci AUTOSAR V3.1.4 (XSD rev. 0004), SHORT-NAMEs with up to 128 characters
file is valid

Importing AUTOSAR XML-exchange file <C:\Documents and Settings\nzt9hv\My Documents\Synergy\ccm_wa\ESG_Dev_65\HiLoadStall-nzt9hv\HiLoadStall\autosar\PortInterfaces.arxml>...
Using DaVinci AUTOSAR V3.1.4 (XSD rev. 0004), SHORT-NAMEs with up to 128 characters
file is valid

Importing generic attributes XML file <C:\Documents and Settings\nzt9hv\My Documents\Synergy\ccm_wa\ESG_Dev_65\HiLoadStall-nzt9hv\HiLoadStall\autosar\ComponentTypes\Ap_HiLoadStall_gen_attr.xml>...
file is valid

Importing generic attributes XML file <C:\Documents and Settings\nzt9hv\My Documents\Synergy\ccm_wa\ESG_Dev_65\HiLoadStall-nzt9hv\HiLoadStall\autosar\Constants_gen_attr.xml>...
file is valid

Importing generic attributes XML file <C:\Documents and Settings\nzt9hv\My Documents\Synergy\ccm_wa\ESG_Dev_65\HiLoadStall-nzt9hv\HiLoadStall\autosar\DataTypes_gen_attr.xml>...
file is valid

Importing generic attributes XML file <C:\Documents and Settings\nzt9hv\My Documents\Synergy\ccm_wa\ESG_Dev_65\HiLoadStall-nzt9hv\HiLoadStall\autosar\PortInterfaces_gen_attr.xml>...
file is valid

Importing generic attributes XML file <C:\Documents and Settings\nzt9hv\My Documents\Synergy\ccm_wa\ESG_Dev_65\HiLoadStall-nzt9hv\HiLoadStall\autosar\Ap_HiLoadStall_attr_def.xml>...
file is valid
Import finished

Generation started at 10:25:49 2012-09-21
```
*…truncated here; the complete log (51 lines) remains at `HiLoadStall/tools/logfile.txt`.*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `HiLoadStall/doc/QAC_Results/Ap_HiLoadStall.c.err` (~20 KiB)
- `HiLoadStall/doc/QAC_Results/Ap_HiLoadStall.c.met` (~461 KiB)

</details>
