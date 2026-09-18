---
title: "Common Manufacturing Services"
description: "Common Manufacturing Services (CMS_Common) — Common Manufacturing Services: shared diagnostic-service helpers for XCP and ISO (`EPS_DiagSrvcs_*`), used by"
---

# Common Manufacturing Services

*Repository directory: `CMS_Common`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

Common Manufacturing Services: shared diagnostic-service helpers for XCP and ISO (`EPS_DiagSrvcs_*`), used by the ECU project manufacturing/diagnostic layers.

## Key files

Implementation (`src/` or module root):

- `CMS_Common/src/EPS_DiagSrvcs_ISO.c`
- `CMS_Common/src/EPS_DiagSrvcs_XCP.Vector.c`
- `CMS_Common/src/EPS_DiagSrvcs_XCP.c`

Public headers (`include/` / `generate/`):

- `CMS_Common/include/EPS_DiagSrvcs_CommonData.h`
- `CMS_Common/include/EPS_DiagSrvcs_ISO.h`
- `CMS_Common/include/EPS_DiagSrvcs_SrvcLUTbl.h`
- `CMS_Common/include/EPS_DiagSrvcs_XCP.h`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 28 files)</summary>

- `CMS_Common/utp/contract/Ap_DfltConfigData.h`
- `CMS_Common/utp/contract/Ap_DiagMgr.h`
- `CMS_Common/utp/contract/CDD_Const.h`
- `CMS_Common/utp/contract/CDD_Data.h`
- `CMS_Common/utp/contract/CalConstants.h`
- `CMS_Common/utp/contract/Cd_TcFlshPrg.h`
- `CMS_Common/utp/contract/Compiler_Cfg.h`
- `CMS_Common/utp/contract/DataLogistic.h`
- `CMS_Common/utp/contract/Dem_Cfg.h`
- `CMS_Common/utp/contract/Dem_Types.h`
- `CMS_Common/utp/contract/EPS_DiagSrvcs_ISO.Customer.h`
- `CMS_Common/utp/contract/EPS_DiagSrvcs_ISO.Interface.h`
- `CMS_Common/utp/contract/EPS_DiagSrvcs_XCP.Interface.h`
- `CMS_Common/utp/contract/Lnk_Symbols.h`
- `CMS_Common/utp/contract/MemMap.h`
- `CMS_Common/utp/contract/NvM.h`
- `CMS_Common/utp/contract/NvM_Cfg.h`
- `CMS_Common/utp/contract/NvM_Types.h`
- `CMS_Common/utp/contract/Omc.h`
- `CMS_Common/utp/contract/Rte.h`
- …and 8 more.

</details>

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `EPSDiagSrvcs_Task` | `EPS_DiagSrvcs_ISO.c` |
| `EPS_DiagSrvcs_Init` | `EPS_DiagSrvcs_ISO.c` |
| `NxtrMEC_Init` | `EPS_DiagSrvcs_ISO.c` |
| `DiagSrvcs_PIDIdxSearch` | `EPS_DiagSrvcs_ISO.c` |
| `DiagSrvcs_ConfiguredNrcCheck` | `EPS_DiagSrvcs_ISO.c` |
| `DiagSrvcs_NRCTranslate` | `EPS_DiagSrvcs_ISO.c` |
| `DiagSrvNullFunc` | `EPS_DiagSrvcs_ISO.c` |
| `ProcessF0FF` | `EPS_DiagSrvcs_ISO.c` |
| `XcpUserFreeDaq` | `EPS_DiagSrvcs_XCP.Vector.c` |
| `XcpUserMemSet` | `EPS_DiagSrvcs_XCP.Vector.c` |
| `XcpUserAllocDaq` | `EPS_DiagSrvcs_XCP.Vector.c` |
| `XcpUserAllocOdt` | `EPS_DiagSrvcs_XCP.Vector.c` |
| `XcpUserAllocOdtEntry` | `EPS_DiagSrvcs_XCP.Vector.c` |
| `XcpUserAllocMemory` | `EPS_DiagSrvcs_XCP.Vector.c` |
| `XcpUserSetDaqListMode` | `EPS_DiagSrvcs_XCP.Vector.c` |
| `XcpUserSetDaqPtr` | `EPS_DiagSrvcs_XCP.Vector.c` |
| `XcpUserWriteDaq` | `EPS_DiagSrvcs_XCP.Vector.c` |
| `ProcessXCPPID` | `EPS_DiagSrvcs_XCP.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
EPS_DiagSrvcs_Init();            /* once, during startup */
NxtrMEC_Init();            /* once, during startup */
ProcessF0FF(/* ports */);  /* periodically, via RTE runnable */
ProcessXCPPID(/* ports */);  /* periodically, via RTE runnable */
```

## Dependencies

RTE (generated per ECU project, Vector MICROSAR/DaVinci — consumed, not owned):

- `Rte_type.h`

Shared project services used:

- `CalConstants.h` (calibration constants / system time / global macros)
- `GlobalMacro.h` (calibration constants / system time / global macros)
- `Std_Types.h` (calibration constants / system time / global macros)
- `SystemTime.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Ap_DfltConfigData.h`
- `Ap_DiagMgr.h`
- `CDD_Const.h`
- `CDD_Data.h`
- `CalConstants.h`
- `Cd_TcFlshPrg.h`
- `Compiler.h`
- `DataLogistic.h`
- `Dem_Cfg.h`
- `Dem_Types.h`
- `EPS_DiagSrvcs_CommonData.h`
- `EPS_DiagSrvcs_ISO.Customer.h`
- `EPS_DiagSrvcs_ISO.Interface.h`
- `EPS_DiagSrvcs_ISO.h`
- `EPS_DiagSrvcs_SrvcLUTbl.h`
- `EPS_DiagSrvcs_XCP.Interface.h`
- `EPS_DiagSrvcs_XCP.h`
- `GlobalMacro.h`
- `Lnk_Symbols.h`
- `MemMap.h`
- `NvM.h`
- `NvM_Cfg.h`
- `NvM_Types.h`
- `Std_Types.h`
- `SystemTime.h`
- `XcpProf.h`
- `desc.h`
- `fixmath.h`
- `fpmtype.h`
- `omc.h`
- `osek.h`
- `tiotp_regs.h`
- `v_def.h`
- `xcp_cfg.h`

</details>

## Documents

The module ships 0 Word/PDF/text documentation file(s) plus 6 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

