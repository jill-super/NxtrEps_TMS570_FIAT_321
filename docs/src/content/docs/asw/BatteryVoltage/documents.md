---
title: "Battery Voltage documents"
description: "Word/PDF/text documents shipped with BatteryVoltage (Battery Voltage) and their conversion status."
---

# Battery Voltage — documents

*Repository directory: `BatteryVoltage`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## BatteryVoltage_Integration_Manual.docx

- **Source:** `BatteryVoltage/doc/BatteryVoltage_Integration_Manual.docx`
- **Format:** `.docx` (~33 KiB)
- **Kind:** Integration manual
- **Status:** converted — text extracted from the binary (3926 characters in total; showing first 2500). Layout, tables, figures and images are omitted; consult `BatteryVoltage/doc/BatteryVoltage_Integration_Manual.docx` for those.

```text
Integration Manual – Battery Voltage
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
7Revision Control Log7
Dependencies
SWCs
Module
Required Feature
ADC
D_ADC1CURRENTMODE_ULS_LGC configuration constant
Basic System Services
EnableOvervoltThreshInterrupt()*
Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.
* Note: EnableOvervoltThreshInterrupt() must be called from ECUStartup.c as soon as possible, but AFTER Adc_Init(), so as to allow configuration of the ADC registers (and subsequently magnitude threshold).
Global Functions(Non RTE) to be provided to Integration Project
ISR(Isr_OvervoltThresh)
Since the ISR that contains the overvoltage threshold diagnostic is enabled in ECUStartup.c, the NTC could be set before the RTE starts. In this case the non-Rte “report NTC staus” API should be used. Also, the application that contains the Battery Voltage ISR and NTC is configured at the integration level. A component specific API, BATTERYVOLTAGE_REPORTERRORSTATUS, is used in the ISR source code and a header file, Template_BatteryVoltage_Cfg.h, needs to be configured to link the BATTERYVOLTAGE_REPORTERRORSTATUS() to the appropriate NxtrDiagMgr???_ReportNTCStatus() function. Remove the “Template_” from the file name and replace the ??? in the API with the appropriate application and place the file in the Header folder of the integration project.
Configuration
Build Time Config
Modules
Notes
None
Configuration Files to be provided by Integration Project
<Configuration file that will generated from this components that will require Da Vinci Config generation or manual generation. Describe each parameter >
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
Isr_OvervoltThresh
```
*…excerpt ends here (1426 further characters in the source).*

## Battery_Voltage_MDD.doc

- **Source:** `BatteryVoltage/doc/Battery_Voltage_MDD.doc`
- **Format:** `.doc` (~884 KiB)
- **Kind:** Module design document (MDD)
- **Status:** summary record — legacy binary source retained at `BatteryVoltage/doc/Battery_Voltage_MDD.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **Battery_Voltage_MDD.doc** module design document specifies the `BatteryVoltage` software component: requirements, interfaces/ports, internal behaviour, calibration and diagnostics. It is the normative reference for the implementation in `BatteryVoltage/src/`; the module page lists the files it governs.

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `BatteryVoltage/doc/QAC_Results/Ap_BatteryVoltage.c.err` (~101 KiB)
- `BatteryVoltage/doc/QAC_Results/Ap_BatteryVoltage.c.met` (~923 KiB)

</details>
