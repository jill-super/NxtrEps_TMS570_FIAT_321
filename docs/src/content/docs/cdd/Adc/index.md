---
title: "Analog-to-Digital Converter Driver"
description: "Analog-to-Digital Converter Driver (Adc) — The Adc Common module provides “stateless” application context independent functions which provide functionali"
---

# Analog-to-Digital Converter Driver

*Repository directory: `Adc`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

The Adc Common module provides “stateless” application context independent functions which provide functionality required by both the Adc and Adc2 modules.

## Key files

Implementation (`src/` or module root):

- `Adc/src/Adc.c`
- `Adc/src/Adc2.c`
- `Adc/src/Adc_Common.c`

Public headers (`include/` / `generate/`):

- `Adc/include/Adc.h`
- `Adc/include/Adc2.h`
- `Adc/include/Adc_Common.h`
- `Adc/tools/Template_Adc2_Cfg.h`
- `Adc/tools/Template_Adc_Cfg.h`
- `Adc/utp/Contract/Adc2_Cfg.h`
- `Adc/utp/Contract/Adc_Cfg.h`
- `Adc/utp/Contract/Ap_DiagMgr.h`
- `Adc/utp/Contract/CDD_Const.h`
- `Adc/utp/Contract/CDD_Data.h`
- `Adc/utp/Contract/CalConstants.h`
- `Adc/utp/Contract/Compiler_Cfg.h`
- `Adc/utp/Contract/MemMap.h`

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `Adc_Init_FixedCfg` | `Adc.c` |
| `Adc_StartGroupConversion` | `Adc.c` |
| `Adc_GetGroupStatus` | `Adc.c` |
| `Adc_ReadGroup` | `Adc.c` |
| `Adc2_Init1` | `Adc2.c` |
| `Adc2_StartGroupConversion` | `Adc2.c` |
| `Adc2_EnableGroupNotification` | `Adc2.c` |
| `ADCOffsetCalibration` | `Adc_Common.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
Adc_Init_FixedCfg();            /* once, during startup */
Adc2_Init1();            /* once, during startup */
```

## Dependencies

Shared project services used:

- `CalConstants.h` (calibration constants / system time / global macros)
- `GlobalMacro.h` (calibration constants / system time / global macros)
- `Std_Types.h` (calibration constants / system time / global macros)
- `SystemTime.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Adc.h`
- `Adc2.h`
- `Adc2_Cfg.h`
- `Adc_Cfg.h`
- `Adc_Common.h`
- `Ap_DiagMgr.h`
- `CDD_Const.h`
- `CDD_Data.h`
- `CalConstants.h`
- `Calconstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Std_Types.h`
- `SystemTime.h`
- `adc_regs.h`

</details>

## Documents

The module ships 4 Word/PDF/text documentation file(s) plus 6 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `Adc/doc/Adc2_MDD.docx`
- `Adc/doc/Adc_Common_MDD.docx`
- `Adc/doc/Adc_MDD.docx`
- `Adc/doc/Integration_Manual_ADC.docx`
