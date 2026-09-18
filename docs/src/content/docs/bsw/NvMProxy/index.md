---
title: "NVRAM Proxy"
description: "NVRAM Proxy (NvMProxy) — Complex Driver NvMProxy which acts as a proxy between"
---

# NVRAM Proxy

*Repository directory: `NvMProxy`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

Complex Driver NvMProxy which acts as a proxy between

## AUTOSAR software component(s)

Modelled SW-C(s) found in `autosar/` (DaVinci/MICROSAR model, AUTOSAR 3.1.4):

- `NvMProxy`

## Key files

Implementation (`src/` or module root):

- `NvMProxy/src/Cd_NvMProxy.c`

Public headers (`include/` / `generate/`):

- `NvMProxy/include/Cd_NvMProxy.h`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 9 files)</summary>

- `NvMProxy/utp/contract/Ap_DiagMgr.h`
- `NvMProxy/utp/contract/Cd_NvMProxy_Cfg.h`
- `NvMProxy/utp/contract/Compiler_Cfg.h`
- `NvMProxy/utp/contract/Crc.h`
- `NvMProxy/utp/contract/MemMap.h`
- `NvMProxy/utp/contract/NvM.h`
- `NvMProxy/utp/contract/NvM_Types.h`
- `NvMProxy/utp/contract/Rte_Type.h`
- `NvMProxy/utp/contract/SchM_NvMProxy.h`

</details>

RTE/BSW generation templates (`generate/`, consumed by the Vector generators — the outputs land in the ECU project `GenData*` folders, not here):

- `NvMProxy/generate/Cd_NvMProxy_Cfg.h.tt`
- `NvMProxy/generate/Cd_NvMProxy_PBcfg.c.tt`
- `NvMProxy/generate/Cd_NvMProxy_swc.arxml.tt`

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `NvMProxy_Init` | `Cd_NvMProxy.c` |
| `NvMProxy_MainFunction` | `Cd_NvMProxy.c` |
| `NvMProxy_WriteBlock` | `Cd_NvMProxy.c` |
| `NvMProxy_WriteAll` | `Cd_NvMProxy.c` |
| `NvMProxy_GetErrorStatus` | `Cd_NvMProxy.c` |
| `NvMProxy_SetRamBlockStatus` | `Cd_NvMProxy.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
NvMProxy_Init();            /* once, during startup */
NvMProxy_MainFunction(/* ports */);  /* periodically, via RTE runnable */
```

## Dependencies

RTE (generated per ECU project, Vector MICROSAR/DaVinci — consumed, not owned):

- `Rte_Type.h`

Shared project services used:

- `Std_Types.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Ap_DiagMgr.h`
- `Cd_NvMProxy.h`
- `Cd_NvMProxy_Cfg.h`
- `Crc.h`
- `MemMap.h`
- `NvM.h`
- `NvM_Types.h`
- `SchM_NvMProxy.h`
- `Std_Types.h`

</details>

## Documents

The module ships 2 Word/PDF/text documentation file(s) plus 2 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `NvMProxy/doc/NvMProxy_Integration_Manual.docx`
- `NvMProxy/doc/NvMProxy_MDD.docx`
