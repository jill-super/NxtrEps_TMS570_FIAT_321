---
title: "States and Modes"
description: "States and Modes (StaMd) — This module handles the EPS system state transitions and is used to determine the operating system state based"
---

# States and Modes

*Repository directory: `StaMd`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

This module handles the EPS system state transitions and is used to determine the operating system state based on knowledge of customer and internal inputs.

## Key files

Implementation (`src/` or module root):

- `StaMd/src/Ap_StaMd.c`

Public headers (`include/` / `generate/`):

- `StaMd/include/Ap_StaMd.h`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 12 files)</summary>

- `StaMd/utp/contract/Ap_StaMd/Ap_StaMd_Cfg.h`
- `StaMd/utp/contract/Ap_StaMd/CalConstants.h`
- `StaMd/utp/contract/Ap_StaMd/Compiler_Cfg.h`
- `StaMd/utp/contract/Ap_StaMd/MemMap.h`
- `StaMd/utp/contract/Ap_StaMd/Os.h`
- `StaMd/utp/contract/Ap_StaMd/Rte.h`
- `StaMd/utp/contract/Ap_StaMd/Rte_Ap_StaMd.h`
- `StaMd/utp/contract/Ap_StaMd/Rte_Compiler_Cfg.h`
- `StaMd/utp/contract/Ap_StaMd/Rte_Hook.h`
- `StaMd/utp/contract/Ap_StaMd/Rte_MemMap.h`
- `StaMd/utp/contract/Ap_StaMd/Rte_Type.h`
- `StaMd/utp/contract/Ap_StaMd/math.h`

</details>

RTE/BSW generation templates (`generate/`, consumed by the Vector generators — the outputs land in the ECU project `GenData*` folders, not here):

- `StaMd/generate/Ap_StaMd_Cfg.c.tt`
- `StaMd/generate/Ap_StaMd_Cfg.h.tt`
- `StaMd/generate/Ap_StaMd_Proxy.c.tt`
- `StaMd/generate/Ap_StaMd_swc.arxml.tt`

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `StaMd_Init0` | `Ap_StaMd.c` |
| `StaMd_Init1` | `Ap_StaMd.c` |
| `StaMd_Per1` | `Ap_StaMd.c` |
| `StaMd_Trns1` | `Ap_StaMd.c` |
| `MilestoneRqst_WarmInitMilestoneComplete` | `Ap_StaMd.c` |
| `MilestoneRqst_WarmInitMilestoneNotComplete` | `Ap_StaMd.c` |
| `StaMd_SCom_EcuReset` | `Ap_StaMd.c` |
| `StaMd_SCom_FBLTransitionReq` | `Ap_StaMd.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
StaMd_Init0();            /* once, during startup */
StaMd_Init1();            /* once, during startup */
MilestoneRqst_WarmInitMilestoneComplete();            /* once, during startup */
MilestoneRqst_WarmInitMilestoneNotComplete();            /* once, during startup */
StaMd_Per1(/* ports */);  /* periodically, via RTE runnable */
```

## Dependencies

RTE (generated per ECU project, Vector MICROSAR/DaVinci — consumed, not owned):

- `Rte_Ap_StaMd.h`
- `Rte_Type.h`

Shared project services used:

- `CalConstants.h` (calibration constants / system time / global macros)
- `GlobalMacro.h` (calibration constants / system time / global macros)
- `Std_Types.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Ap_StaMd_Cfg.h`
- `CalConstants.h`
- `GlobalMacro.h`
- `MemMap.h`
- `Os.h`
- `Std_Types.h`

</details>

## Documents

The module ships 6 Word/PDF/text documentation file(s) plus 2 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `StaMd/doc/StaMd_Integration_Manual.docx`
- `StaMd/doc/States_And_Modes_GeneratedConfiguration_MDD.docx`
- `StaMd/doc/States_And_Modes_MDD.docx`
- `StaMd/utp/StaMd UnitTest Notes for Developer.docx`
- `StaMd/utp/Tessy/report/index_WithPS.pdf`
- `StaMd/utp/Tessy/report/index_WithoutPS.pdf`
