---
title: "Gliwa T1 Timing Measurement"
description: "Gliwa T1 Timing Measurement (GliwaT1) — Gliwa T1 timing-measurement integration: application interface and configuration (`T1_AppInterface`) linking t"
---

# Gliwa T1 Timing Measurement

*Repository directory: `GliwaT1`*

:::caution[Origin: Third-party — Gliwa]
Gliwa T1 timing-measurement stack (prebuilt `libt1*.a` libraries) plus project glue (`T1_AppInterface`).
:::

## Purpose and responsibility

Gliwa T1 timing-measurement integration: application interface and configuration (`T1_AppInterface`) linking the prebuilt third-party T1 measurement libraries for execution-time analysis.

## Key files

Implementation (`src/` or module root):

- `GliwaT1/src/T1_AppInterface.c`
- `GliwaT1/src/T1_config.c`
- `GliwaT1/utp/Example_Integration_Specific/T1_AppInterface_Cfg.c`
- `GliwaT1/utp/Example_Tools_GliwaT1/Overlay/GM_C1XX_EPS_TMS570/SwProject/Source/BSW/Can/can_drv.c`
- `GliwaT1/utp/Example_Tools_GliwaT1/Overlay/GM_C1XX_EPS_TMS570/SwProject/Source/BSW/Gpt/Gpt_Irq.c`
- `GliwaT1/utp/Example_Tools_GliwaT1/Overlay/GM_C1XX_EPS_TMS570/SwProject/Source/BSW/Os/osektask.c`

Public headers (`include/` / `generate/`):

- `GliwaT1/include/Metrics.h`
- `GliwaT1/include/T1_AppInterface.h`
- `GliwaT1/include/T1_MemMap.h`
- `GliwaT1/include/T1_baseConfig.h`
- `GliwaT1/include/T1_baseInterface.h`
- `GliwaT1/include/T1_bid.h`
- `GliwaT1/include/T1_config.h`
- `GliwaT1/include/T1_contConfig.h`
- `GliwaT1/include/T1_contInterface.h`
- `GliwaT1/include/T1_delayConfig.h`
- `GliwaT1/include/T1_delayInterface.h`
- `GliwaT1/include/T1_flexConfig.h`
- `GliwaT1/include/T1_flexInterface.h`
- `GliwaT1/include/T1_modInterface.h`
- `GliwaT1/include/T1_runnables.h`
- `GliwaT1/include/T1_scopeConfig.h`
- `GliwaT1/include/T1_scopeInterface.h`
- `GliwaT1/include/T1_targetSpecifics.h`
- `GliwaT1/include/sys_pmu.h`
- `GliwaT1/utp/Example_Integration_Specific/T1_AppInterface_Cfg.h`
- `GliwaT1/utp/Example_Tools_GliwaT1/Overlay/GliwaT1/include/T1_AppInterface.h`

Assembly sources:

- `GliwaT1/src/sys_pmu.asm`
- `GliwaT1/utp/Example_Tools_GliwaT1/Overlay/GM_C1XX_EPS_TMS570/SwProject/Source/BSW/Os/osekasm.asm`

Prebuilt libraries linked from this module:

- `GliwaT1/src/libt1base.a`
- `GliwaT1/src/libt1com8.a`
- `GliwaT1/src/libt1cont.a`
- `GliwaT1/src/libt1delay.a`
- `GliwaT1/src/libt1flex.a`
- `GliwaT1/src/libt1mod.a`
- `GliwaT1/src/libt1scope.a`

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `T1_AppInit` | `T1_AppInterface.c` |
| `T1_AppHandler` | `T1_AppInterface.c` |
| `T1_AppBgHandler` | `T1_AppInterface.c` |
| `T1_TraceEvent_` | `T1_AppInterface.c` |
| `T1_TraceEventFast_` | `T1_AppInterface.c` |
| `T1_TraceEventNoSusp_` | `T1_AppInterface.c` |
| `T1_InitEventChainsCore0` | `T1_config.c` |
| `T1_ContErrCallback` | `T1_config.c` |
| `T1_ContCsrnCallback` | `T1_config.c` |
| `T1_CPULoadCallback` | `T1_config.c` |
| `T1_AppPrefetchAbortHandler` | `T1_config.c` |
| `T1_AppDataAbortHandler` | `T1_config.c` |
| `T1_DataAbortHandler` | `T1_config.c` |
| `T1_PrefetchAbortHandler` | `T1_config.c` |
| `GliwaT1_MsgProcess_RxT1HostToTarget` | `T1_AppInterface_Cfg.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
T1_AppInit();            /* once, during startup */
T1_InitEventChainsCore0();            /* once, during startup */
GliwaT1_MsgProcess_RxT1HostToTarget(/* ports */);  /* periodically, via RTE runnable */
```

## Dependencies

Shared project services used:

- `Std_Types.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Gpt.h`
- `Gpt_Irq.h`
- `MemMap.h`
- `Metrics.h`
- `Std_Types.h`
- `T1_AppInterface.h`
- `T1_AppInterface_Cfg.h`
- `T1_MemMap.h`
- `T1_baseConfig.h`
- `T1_baseInterface.h`
- `T1_bid.h`
- `T1_config.h`
- `T1_contConfig.h`
- `T1_contInterface.h`
- `T1_delayConfig.h`
- `T1_delayInterface.h`
- `T1_flexConfig.h`
- `T1_flexInterface.h`
- `T1_modInterface.h`
- `T1_scopeConfig.h`
- `T1_scopeInterface.h`
- `T1_targetSpecifics.h`
- `can_cfg.h`
- `can_inc.h`
- `can_par.h`
- `il_inc.h`
- `osek.h`
- `osekext.h`
- `sys_common.h`
- `sys_pmu.h`
- `vrm.h`

</details>

## Documents

The module ships 1 Word/PDF/text documentation file(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `GliwaT1/doc/GliwaT1_IntegrationManual.doc`
