---
title: "TMS570 Startup (System, Boot and Interrupt Vectors)"
description: "TMS570 Startup (System, Boot and Interrupt Vectors) (TMS570_Startup) — sys_core provides assembly language functions for processor register data access and system startup."
---

# TMS570 Startup (System, Boot and Interrupt Vectors)

*Repository directory: `TMS570_Startup`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

sys_core provides assembly language functions for processor register data access and system startup.

## Key files

Implementation (`src/` or module root):

- `TMS570_Startup/src/AppStartup.c`
- `TMS570_Startup/src/BootStartup.c`
- `TMS570_Startup/src/ResetCause.c`
- `TMS570_Startup/src/prooftestv02.c`
- `TMS570_Startup/src/sys_startup.c`

Public headers (`include/` / `generate/`):

- `TMS570_Startup/include/ResetCause.h`
- `TMS570_Startup/include/prooftestv02.h`
- `TMS570_Startup/include/sys_core.h`
- `TMS570_Startup/include/sys_memory.h`
- `TMS570_Startup/include/sys_pmu.h`
- `TMS570_Startup/src/prooftestv02.het`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 6 files)</summary>

- `TMS570_Startup/utp/contract/Compiler_Cfg.h`
- `TMS570_Startup/utp/contract/MemMap.h`
- `TMS570_Startup/utp/contract/appinit_cfg.h`
- `TMS570_Startup/utp/contract/startup_cfg.h`
- `TMS570_Startup/utp/contract/std_nhet.h`
- `TMS570_Startup/utp/contract/uDiag.h`

</details>

Assembly sources:

- `TMS570_Startup/src/fiqintvect.asm`
- `TMS570_Startup/src/sys_core.asm`
- `TMS570_Startup/src/sys_memory.asm`
- `TMS570_Startup/src/sys_pmu.asm`

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `_c_int00` | `AppStartup.c` |
| `BootStartup` | `BootStartup.c` |

## Dependencies

Shared project services used:

- `Std_Types.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Compiler.h`
- `MemMap.h`
- `Platform_Types.h`
- `ResetCause.h`
- `Std_Types.h`
- `adc_regs.h`
- `appinit_cfg.h`
- `ccm_regs.h`
- `dcan_regs.h`
- `dma_regs.h`
- `efc_regs.h`
- `esm_regs.h`
- `flash_regs.h`
- `gio_regs.h`
- `htu_regs.h`
- `mibspi_regs.h`
- `n2het_regs.h`
- `pbist_regs.h`
- `pcr_regs.h`
- `prooftestv02.h`
- `startup_cfg.h`
- `stc_regs.h`
- `std_nhet.h`
- `sys_core.h`
- `sys_memory.h`
- `sys_pmu.h`
- `system_regs.h`
- `tcram_regs.h`
- `uDiag.h`
- `vim_regs.h`

</details>

## Documents

The module ships 6 Word/PDF/text documentation file(s) plus 4 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `TMS570_Startup/doc/TMS570_Startup_BootStartup_MDD.docx`
- `TMS570_Startup/doc/TMS570_Startup_FiqIntVect_MDD.docx`
- `TMS570_Startup/doc/TMS570_Startup_Integration_Manual.docx`
- `TMS570_Startup/doc/TMS570_Startup_SysCore_MDD.docx`
- `TMS570_Startup/doc/TMS570_Startup_SysStartup_MDD.docx`
- `TMS570_Startup/doc/spna106a.pdf`
