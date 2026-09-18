---
title: "Sine-Voltage Motor Driver (Current Mode)"
description: "Sine-Voltage Motor Driver (Current Mode) (SVDrvr_CM) — Non-AUTOSAR PWM driver required to perform EPS motor control PWM profiles."
---

# Sine-Voltage Motor Driver (Current Mode)

*Repository directory: `SVDrvr_CM`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

Non-AUTOSAR PWM driver required to perform EPS motor control PWM profiles.

## Key files

Implementation (`src/` or module root):

- `SVDrvr_CM/src/PwmCdd.c`

Public headers (`include/` / `generate/`):

- `SVDrvr_CM/include/PwmCdd.h`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 6 files)</summary>

- `SVDrvr_CM/utp/contract/CalConstants.h`
- `SVDrvr_CM/utp/contract/Compiler_Cfg.h`
- `SVDrvr_CM/utp/contract/MemMap.h`
- `SVDrvr_CM/utp/contract/PwmCdd/CDD_Data.h`
- `SVDrvr_CM/utp/contract/PwmCdd/CDD_Func.h`
- `SVDrvr_CM/utp/contract/PwmCdd/PwmCdd_Cfg.h`

</details>

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `PwmCdd_Init` | `PwmCdd.c` |
| `PwmCdd_Per1` | `PwmCdd.c` |
| `CDD_ApplyPWMMtrElecMechPol` | `PwmCdd.c` |
| `CDDPorts_ClearPhsReasSum` | `PwmCdd.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
PwmCdd_Init();            /* once, during startup */
PwmCdd_Per1(/* ports */);  /* periodically, via RTE runnable */
```

## Dependencies

Shared project services used:

- `CalConstants.h` (calibration constants / system time / global macros)
- `GlobalMacro.h` (calibration constants / system time / global macros)
- `Std_Types.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `CDD_Data.h`
- `CDD_Func.h`
- `CalConstants.h`
- `Filter_Types.h`
- `GlobalMacro.h`
- `MemMap.h`
- `PwmCdd.h`
- `PwmCdd_Cfg.h`
- `Std_Types.h`
- `fixmath.h`

</details>

## Documents

The module ships 2 Word/PDF/text documentation file(s) plus 2 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `SVDrvr_CM/doc/PWMCdd_Integration_Manual.docx`
- `SVDrvr_CM/doc/PWM_CDD_MDD.docx`
