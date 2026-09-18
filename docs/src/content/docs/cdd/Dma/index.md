---
title: "Direct Memory Access Driver"
description: "Direct Memory Access Driver (Dma) — DMA is a driver level module that performs flash, RAM, and peripheral reads and writes in the background, free"
---

# Direct Memory Access Driver

*Repository directory: `Dma`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

DMA is a driver level module that performs flash, RAM, and peripheral reads and writes in the background, freeing up the CPU to do other work in parallel.

## Key files

Implementation (`src/` or module root):

- `Dma/src/Dma.c`

Public headers (`include/` / `generate/`):

- `Dma/include/Dma.h`
- `Dma/tools/Dma_Cfg_Template.h`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 8 files)</summary>

- `Dma/utp/contract/Adc.h`
- `Dma/utp/contract/Adc2.h`
- `Dma/utp/contract/Compiler_Cfg.h`
- `Dma/utp/contract/Dma_Cfg.h`
- `Dma/utp/contract/MemMap.h`
- `Dma/utp/contract/Nhet_SENT_Prog.h`
- `Dma/utp/contract/SpiNxt.h`
- `Dma/utp/contract/appinit_cfg.h`

</details>

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `Dma_Init` | `Dma.c` |
| `Dma_SlowADCGroupValidity` | `Dma.c` |
| `Dma_InvalidateSlowADCGroup` | `Dma.c` |
| `Dma_SetupMtrCtrlGroups` | `Dma.c` |
| `Dma_DisableFlsTstBlock` | `Dma.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
Dma_Init();            /* once, during startup */
```

## Dependencies

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Adc.h`
- `Adc2.h`
- `Ap_DiagMgr.h`
- `Dma.h`
- `Dma_Cfg.h`
- `MemMap.h`
- `Nhet_SENT_Prog.h`
- `SpiNxt.h`
- `appinit_cfg.h`
- `crc_regs.h`
- `dma_regs.h`
- `epwm_regs.h`
- `mibspi_regs.h`

</details>

## Documents

The module ships 2 Word/PDF/text documentation file(s) plus 2 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `Dma/doc/Dma Integration Manual.docx`
- `Dma/doc/Dma_MDD.docx`
