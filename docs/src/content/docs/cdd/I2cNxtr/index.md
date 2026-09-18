---
title: "I²C Driver (Nexteer)"
description: "I²C Driver (Nexteer) (I2cNxtr) — I2C Driver: Nexteer implementation."
---

# I²C Driver (Nexteer)

*Repository directory: `I2cNxtr`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

I2C Driver: Nexteer implementation.

## Key files

Implementation (`src/` or module root):

- `I2cNxtr/src/I2cNxtr.c`
- `I2cNxtr/src/I2cNxtr_Irq.c`

Public headers (`include/` / `generate/`):

- `I2cNxtr/include/I2cNxtr.h`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 6 files)</summary>

- `I2cNxtr/utp/contract/Compiler_Cfg.h`
- `I2cNxtr/utp/contract/I2cNxtr_Cfg.h`
- `I2cNxtr/utp/contract/MemMap.h`
- `I2cNxtr/utp/contract/Metrics.h`
- `I2cNxtr/utp/contract/Os.h`
- `I2cNxtr/utp/contract/interrupts.h`

</details>

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `I2c_Init` | `I2cNxtr.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
I2c_Init();            /* once, during startup */
```

## Dependencies

Shared project services used:

- `Std_Types.h` (calibration constants / system time / global macros)
- `SystemTime.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `I2cNxtr.h`
- `I2cNxtr_Cfg.h`
- `MemMap.h`
- `Metrics.h`
- `Os.h`
- `Std_Types.h`
- `SystemTime.h`
- `i2c_regs.h`
- `interrupts.h`

</details>

## Documents

The module ships 2 Word/PDF/text documentation file(s) plus 4 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `I2cNxtr/doc/I2cNxtr_Integration_Manual.docx`
- `I2cNxtr/doc/I2cNxtr_MDD.docx`
