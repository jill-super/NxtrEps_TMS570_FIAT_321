---
title: "Stability Compensation documents"
description: "Word/PDF/text documents shipped with StabilityComp (Stability Compensation) and their conversion status."
---

# Stability Compensation — documents

*Repository directory: `StabilityComp`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## StabilityCompensation2_MDD.docx

- **Source:** `StabilityComp/doc/StabilityCompensation2_MDD.docx`
- **Format:** `.docx` (~362 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5992 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `StabilityComp/doc/StabilityCompensation2_MDD.docx` for those.

```text
Module -- Stability Compensation
High-Level Description
This function provides in-vehicle stability of EPS behavior. To maximize steering feel, the function blends between two different tunings based on vehicle speed and low frequency handwheel torque. Because system gains may get multiplied by various scale factors, either from serial communications or from other software functions, this function provides a second blending feature.
Some vehicle programs require a secondary, or "systematic", calculation of stability compensation followed by a correlation check. The systematic calculations usually must reside in a separate Memory Partition Unit (MPU), and switching between MPUs negatively impacts system throughput. This model is designed using the best-known implementation at this time.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
AssistDDFactor_Uls_f32
SysAssistCmd_MtrNm_f32
HwTorque_HwNm_f32
VehicleSpeed_Kph_f32
CombinedAssist_MtrNm_f32
AsstFWActive_Uls_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
StCmp1Out2_MtrNm_D_f32
Single Precision Float
-2312
2312
STABILITYCOMP2_START_SEC_VAR_CLEARED_32
StCmp2Out2_MtrNm_D_f32
Single Precision Float
-2312
2312
STABILITYCOMP2_START_SEC_VAR_CLEARED_32
StCmp3Out2_MtrNm_D_f32
Single Precision Float
-2312
2312
STABILITYCOMP2_START_SEC_VAR_CLEARED_32
StCmp4Out2_MtrNm_D_f32
Single Precision Float
-2312
2312
STABILITYCOMP2_START_SEC_VAR_CLEARED_32
HwTorqueSV_HwNm_M_f32
Single Precision Float
-10
10
STABILITYCOMP2_START_SEC_VAR_CLEARED_32
VehicleSpeedSV_Kph_M_f32
Single Precision Float
0
511.9921875
STABILITYCOMP2_START_SEC_VAR_CLEARED_32
AssistDDFactorSV_Uls_M_f32
Single Precision Float
1
2
STABILITYCOMP2_START_SEC_VAR_CLEARED_32
CombAstNFSV2_Cnt_M_Str*
N/A
N/A
N/A
STABILITYCOMP2_START_SEC_VAR_CLEARED_UNSPECIFIED
CombAstNFSV2_Cnt_M_Str[].SV1_Uls_f32
Single Precision Floating Point
-2077
2077
CombAstNFSV2_Cnt_M_Str[].SV2_Uls_f32
Single Precision Floating Point
-1981
1981
CombAstNFSV2_Cnt_M_Str[].Out_Uls_f32
Single Precision Floating Point
-2312
2312
CombAstNFSV2_C
```
*…excerpt ends here (3492 further characters in the source).*

## StabilityCompensation_MDD.docx

- **Source:** `StabilityComp/doc/StabilityCompensation_MDD.docx`
- **Format:** `.docx` (~498 KiB)
- **Kind:** Module design document (MDD)
- **Status:** converted — text extracted from the binary (5993 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `StabilityComp/doc/StabilityCompensation_MDD.docx` for those.

```text
Module -- Stability Compensation
High-Level Description
This function provides in-vehicle stability of EPS behavior. To maximize steering feel, the function blends between two different tunings based on vehicle speed and low frequency handwheel torque. Because system gains may get multiplied by various scale factors, either from serial communications or from other software functions, this function provides a second blending feature.
Some vehicle programs require a secondary, or "systematic", calculation of stability compensation followed by a correlation check. The systematic calculations usually must reside in a separate Memory Partition Unit (MPU), and switching between MPUs negatively impacts system throughput. This model is designed using the best-known implementation at this time.
Figures
Component Diagram
Variable Data Dictionary
For details on module input / output variable, refer to the Data Dictionary for the application. Input / output variable names are listed here for reference.
Module Inputs
Module Outputs
AssistDDFactor_Uls_f32
AssistCmd_MtrNm_f32
SysAssistCmd_MtrNm_f32
HwTorque_HwNm_f32
VehicleSpeed_Kph_f32
CombinedAssist_MtrNm_f32
AsstFWActive_Uls_f32
Module Internal Variables
This section identifies the name, range and resolutions for module specific data created by this module. If there are no range restrictions on the variable, the term “FULL” is placed into the table for legal range.
Variable Name
Resolution
Legal Range
(min)
Legal Range
(max)
Software Segment
StCmpAsstFctrCmpBlnd_Uls_D_f32
Single Precision Float
0
1
STABILITYCOMP_START_SEC_VAR_CLEARED_32
StCmp12Blend_Uls_D_f32
Single Precision Float
0
1
STABILITYCOMP_START_SEC_VAR_CLEARED_32
StCmp34Blend_Uls_D_f32
Single Precision Float
0
1
STABILITYCOMP_START_SEC_VAR_CLEARED_32
StCmp02Blend_Uls_D_f32
Single Precision Float
0
1
STABILITYCOMP_START_SEC_VAR_CLEARED_32
StCmp04Blend_Uls_D_f32
Single Precision Float
0
1
STABILITYCOMP_START_SEC_VAR_CLEARED_32
StCmp1Out_MtrNm_D_f32
Single Precision Float
-2312
2312
STABILITYCOMP_START_SEC_VAR_CLEARED_32
StCmp2Out_MtrNm_D_f32
Single Precision Float
-2312
2312
STABILITYCOMP_START_SEC_VAR_CLEARED_32
StCmp3Out_MtrNm_D_f32
Single Precision Float
-2312
2312
STABILITYCOMP_START_SEC_VAR_CLEARED_32
StCmp4Out_MtrNm_D_f32
Single Precision Float
-2312
2312
STABILITYCOMP_START_SEC_VAR_CLEARED_32
AssistCmdSV_MtrNm_M_f32
Single Precision Float
-8.8
8.8
STABILITYCOMP_START_SEC_VAR_CLEARED_32
HwTrqSV_HwNm_M_Str
N/A
N/A
N/A
STABILITYCOMP_START_SEC_VAR_CLEARED_
```
*…excerpt ends here (3493 further characters in the source).*

## logfile.txt

- **Source:** `StabilityComp/tools/logfile.txt`
- **Format:** `.txt` (~11 KiB)
- **Kind:** Tool log file (generator transcript)
- **Status:** converted in full (plain text embedded below).

Generator transcript (first lines; full log retained in the repository):

```text

MICROSAR RTE Generator Version 2.17.2
Copyright c 2001-2010 Vector Informatik GmbH
License CBD1010122 valid for CBD1010122 Nexteer  GM MSR_SLP3_BSW_RTE_wGMLAN TexasInstruments TMS570 Texas Instruments
Loading profile settings from file 'C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\ProfileSettings.xml'.
Failed to load profile settings from file 'C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\ProfileSettings.xml'. Applying default settings.

Importing AUTOSAR XML-exchange file <C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\ComponentTypes\Ap_StabilityComp.arxml>...
Using DaVinci AUTOSAR V3.1.4 (XSD rev. 0004), SHORT-NAMEs with up to 128 characters
file is valid

Importing AUTOSAR XML-exchange file <C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\ComponentTypes\Ap_StabilityComp2.arxml>...
Using DaVinci AUTOSAR V3.1.4 (XSD rev. 0004), SHORT-NAMEs with up to 128 characters
file is valid

Importing AUTOSAR XML-exchange file <C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\Constants.arxml>...
Using DaVinci AUTOSAR V3.1.4 (XSD rev. 0004), SHORT-NAMEs with up to 128 characters
file is valid

Importing AUTOSAR XML-exchange file <C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\DataTypes.arxml>...
Using DaVinci AUTOSAR V3.1.4 (XSD rev. 0004), SHORT-NAMEs with up to 128 characters
file is valid

Importing AUTOSAR XML-exchange file <C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\PortInterfaces.arxml>...
Using DaVinci AUTOSAR V3.1.4 (XSD rev. 0004), SHORT-NAMEs with up to 128 characters
file is valid

Importing generic attributes XML file <C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\ComponentTypes\Ap_StabilityComp_gen_attr.xml>...
file is valid

Importing generic attributes XML file <C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\ComponentTypes\Ap_StabilityComp2_gen_attr.xml>...
file is valid

Importing generic attributes XML file <C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\Constants_gen_attr.xml>...
file is valid

Importing generic attributes XML file <C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\DataTypes_gen_attr.xml>...
file is valid

Importing generic attributes XML file <C:\Synergy_projects\StabilityComp-lz4p8n\StabilityComp\autosar\PortInterfaces_gen_attr.xml>...
```
*…truncated here; the complete log (156 lines) remains at `StabilityComp/tools/logfile.txt`.*

## Static-analysis outputs (4 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `StabilityComp/doc/QAC_Results/Ap_StabilityComp.c.err` (~106 KiB)
- `StabilityComp/doc/QAC_Results/Ap_StabilityComp.c.met` (~920 KiB)
- `StabilityComp/doc/QAC_Results/Ap_StabilityComp2.c.err` (~106 KiB)
- `StabilityComp/doc/QAC_Results/Ap_StabilityComp2.c.met` (~914 KiB)

</details>
