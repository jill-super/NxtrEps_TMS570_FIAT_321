---
title: "SPI Driver (Nexteer)"
description: "SPI Driver (Nexteer) (SpiNxt) — This module provides the following Autosar API: Spi_SetupEB() Spi_Init() Spi_AsyncTransmit() Spi_GetSequenceRe"
---

# SPI Driver (Nexteer)

*Repository directory: `SpiNxt`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

This module provides the following Autosar API: Spi_SetupEB() Spi_Init() Spi_AsyncTransmit() Spi_GetSequenceResult() This module provides the following TI Halcogen API: mibspiSetCtrlData() – Note: this is a modified form of the standard mibspiSetData() API mibspiTransfer() mibspiGetData() mibspiSetData() The Autosar API naming has been altered from the Autosar standard to allow co-existence of this module and a Third Party Spi driver implementation in the same project.

## AUTOSAR software component(s)

Modelled SW-C(s) found in `autosar/` (DaVinci/MICROSAR model, AUTOSAR 3.1.4):

- `SpiNxt`

## Key files

Implementation (`src/` or module root):

- `SpiNxt/src/SpiNxt.c`
- `SpiNxt/src/SpiNxt_Irq.c`

Public headers (`include/` / `generate/`):

- `SpiNxt/include/SpiNxt.h`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 10 files)</summary>

- `SpiNxt/utp/contract/Compiler_Cfg.h`
- `SpiNxt/utp/contract/Dio.h`
- `SpiNxt/utp/contract/Dio_Cfg.h`
- `SpiNxt/utp/contract/MemMap.h`
- `SpiNxt/utp/contract/Metrics.h`
- `SpiNxt/utp/contract/Os.h`
- `SpiNxt/utp/contract/SchM_SpiNxt.h`
- `SpiNxt/utp/contract/Spi.h`
- `SpiNxt/utp/contract/SpiNxt/SpiNxt_Cfg.h`
- `SpiNxt/utp/contract/sys_common.h`

</details>

RTE/BSW generation templates (`generate/`, consumed by the Vector generators — the outputs land in the ECU project `GenData*` folders, not here):

- `SpiNxt/generate/SpiNxt_Cfg.h.tt`

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `SpiNxt_GetSequenceResult` | `SpiNxt.c` |
| `SpiNxt_AsyncTransmit` | `SpiNxt.c` |
| `SpiNxt_Init` | `SpiNxt.c` |
| `mibspiSetData` | `SpiNxt.c` |
| `mibspiSetCtrlData` | `SpiNxt.c` |
| `mibspiGetData` | `SpiNxt.c` |
| `mibspiTransfer` | `SpiNxt.c` |
| `mibspiNotification` | `SpiNxt.c` |
| `mibspiGroupNotification` | `SpiNxt.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
SpiNxt_Init();            /* once, during startup */
```

## Dependencies

Shared project services used:

- `Std_Types.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Dio.h`
- `Dio_Cfg.h`
- `MemMap.h`
- `Metrics.h`
- `Os.h`
- `SchM_SpiNxt.h`
- `Spi.h`
- `SpiNxt.h`
- `SpiNxt_Cfg.h`
- `Std_Types.h`
- `mibspi_regs.h`
- `sys_common.h`

</details>

## Documents

The module ships 2 Word/PDF/text documentation file(s) plus 4 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `SpiNxt/doc/Spi_Nexteer_Integration_Manual.docx`
- `SpiNxt/doc/Spi_Nexteer_MDD.docx`
