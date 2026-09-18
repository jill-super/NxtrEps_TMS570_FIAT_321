---
title: "Diagnostics Manager"
description: "Diagnostics Manager (DiagMgr) — Core Diagnostic Manager Functionality"
---

# Diagnostics Manager

*Repository directory: `DiagMgr`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

Core Diagnostic Manager Functionality

## Key files

Implementation (`src/` or module root):

- `DiagMgr/src/Ap_DiagMgr_Core.c`
- `DiagMgr/src/Ap_DiagMgr_DemIf.c`
- `DiagMgr/src/Ap_DiagMgr_FailAction.c`

Public headers (`include/` / `generate/`):

- `DiagMgr/include/Ap_DiagMgr.h`
- `DiagMgr/include/Ap_DiagMgr_Types.h`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 12 files)</summary>

- `DiagMgr/utp/contract/CalConstants.h`
- `DiagMgr/utp/contract/Compiler_Cfg.h`
- `DiagMgr/utp/contract/Det.h`
- `DiagMgr/utp/contract/DiagMgr_Cfg.h`
- `DiagMgr/utp/contract/MemMap.h`
- `DiagMgr/utp/contract/NvM.h`
- `DiagMgr/utp/contract/Os.h`
- `DiagMgr/utp/contract/Rte.h`
- `DiagMgr/utp/contract/Rte_Ap_DiagMgr.h`
- `DiagMgr/utp/contract/Rte_Compiler_Cfg.h`
- `DiagMgr/utp/contract/Rte_MemMap.h`
- `DiagMgr/utp/contract/Rte_Type.h`

</details>

RTE/BSW generation templates (`generate/`, consumed by the Vector generators — the outputs land in the ECU project `GenData*` folders, not here):

- `DiagMgr/generate/DiagMgr_Cfg.c.tt`
- `DiagMgr/generate/DiagMgr_Cfg.h.tt`
- `DiagMgr/generate/DiagMgr_Proxy.c.tt`
- `DiagMgr/generate/DiagMgr_swc.arxml.tt`

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `NxtrDiagMgr_GetNTCActive_Core` | `Ap_DiagMgr_Core.c` |
| `DiagMgr_Init1` | `Ap_DiagMgr_DemIf.c` |
| `DiagMgr_Trns1` | `Ap_DiagMgr_DemIf.c` |
| `DiagMgr_StaCtrl_Shutdown` | `Ap_DiagMgr_DemIf.c` |
| `DiagMgr_Per2` | `Ap_DiagMgr_DemIf.c` |
| `DiagMgr_SCom_ResetNTCStatus` | `Ap_DiagMgr_DemIf.c` |
| `DiagMgr_SCom_ReadStrgArray` | `Ap_DiagMgr_DemIf.c` |
| `DiagMgr_SCom_ClearBlackBox` | `Ap_DiagMgr_DemIf.c` |
| `DiagMgr_SCom_ClearLatchCounters` | `Ap_DiagMgr_DemIf.c` |
| `DiagMgr_Per1` | `Ap_DiagMgr_FailAction.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
DiagMgr_Init1();            /* once, during startup */
DiagMgr_Per2(/* ports */);  /* periodically, via RTE runnable */
DiagMgr_Per1(/* ports */);  /* periodically, via RTE runnable */
```

## Dependencies

RTE (generated per ECU project, Vector MICROSAR/DaVinci — consumed, not owned):

- `Rte_Ap_DiagMgr.h`
- `Rte_Type.h`

Shared project services used:

- `CalConstants.h` (calibration constants / system time / global macros)
- `GlobalMacro.h` (calibration constants / system time / global macros)
- `Std_Types.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Ap_DiagMgr.h`
- `Ap_DiagMgr_Types.h`
- `CalConstants.h`
- `Det.h`
- `DiagMgr_Cfg.h`
- `GlobalMacro.h`
- `MemMap.h`
- `NvM.h`
- `Os.h`
- `Std_Types.h`
- `fixmath.h`

</details>

## Documents

The module ships 4 Word/PDF/text documentation file(s) plus 6 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `DiagMgr/doc/Diagnostics_Manager_Core_MDD.docx`
- `DiagMgr/doc/Diagnostics_Manager_DemIf_MDD.docx`
- `DiagMgr/doc/Diagnostics_Manager_FailAction_MDD.docx`
- `DiagMgr/doc/Diagnostics_Manager_GeneratedCfg_MDD.docx`
