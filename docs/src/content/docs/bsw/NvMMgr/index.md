---
title: "NVRAM Manager (FEE Interface)"
description: "NVRAM Manager (FEE Interface) (NvMMgr) — This module contains the specific interfacing functions that are needed for TI’s Fee Driver."
---

# NVRAM Manager (FEE Interface)

*Repository directory: `NvMMgr`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

This module contains the specific interfacing functions that are needed for TI’s Fee Driver.

## Key files

Implementation (`src/` or module root):

- `NvMMgr/src/Cd_FeeIf.c`
- `NvMMgr/src/Fapi_UserDefinedFunctions.c`

Public headers (`include/` / `generate/`):

- `NvMMgr/include/Cd_FeeIf.h`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 8 files)</summary>

- `NvMMgr/utp/contract/Cd_NvMMgr_Cfg.h`
- `NvMMgr/utp/contract/Compiler_Cfg.h`
- `NvMMgr/utp/contract/F021.h`
- `NvMMgr/utp/contract/MemIf_Types.h`
- `NvMMgr/utp/contract/MemMap.h`
- `NvMMgr/utp/contract/Os.h`
- `NvMMgr/utp/contract/fee.h`
- `NvMMgr/utp/contract/trustfct.h`

</details>

RTE/BSW generation templates (`generate/`, consumed by the Vector generators — the outputs land in the ECU project `GenData*` folders, not here):

- `NvMMgr/generate/Cd_NvMMgr_Cfg.h.tt`

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `FeeIf_Init` | `Cd_FeeIf.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
FeeIf_Init();            /* once, during startup */
```

## Dependencies

Shared project services used:

- `Std_Types.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Cd_FeeIf.h`
- `Cd_NvMMgr_Cfg.h`
- `F021.h`
- `MemIf_Types.h`
- `Os.h`
- `Std_Types.h`
- `fee.h`
- `trustfct.h`

</details>

## Documents

The module ships 2 Word/PDF/text documentation file(s) plus 6 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `NvMMgr/doc/Fee_Interface_MDD.docx`
- `NvMMgr/doc/NvMMgr_Integration_Manual.docx`
