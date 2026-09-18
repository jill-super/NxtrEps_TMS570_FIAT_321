---
title: "Nexteer Shared Library (Math, Filters, System Time)"
description: "Nexteer Shared Library (Math, Filters, System Time) (NxtrLib) — Shared project library: digital filters, fixed-point math, interpolation, checksums, atan2 and system-time ser"
---

# Nexteer Shared Library (Math, Filters, System Time)

*Repository directory: `NxtrLib`*

:::tip[Origin: Custom — Nexteer in-house]
Nexteer Automotive in-house development (copyright headers in the module sources).
:::

## Purpose and responsibility

Shared project library: digital filters, fixed-point math, interpolation, checksums, atan2 and system-time services consumed by the application components (see `NxtrLib/include/`).

## Key files

Implementation (`src/` or module root):

- `NxtrLib/src/CheckSums.c`
- `NxtrLib/src/SystemTime.c`
- `NxtrLib/src/atan2_octants.c`
- `NxtrLib/src/filters.c`
- `NxtrLib/src/interpolation.c`

Public headers (`include/` / `generate/`):

- `NxtrLib/include/CheckSums.h`
- `NxtrLib/include/Filter_Types.h`
- `NxtrLib/include/GlobalMacro.h`
- `NxtrLib/include/SystemTime.h`
- `NxtrLib/include/atan2.h`
- `NxtrLib/include/filters.h`
- `NxtrLib/include/fixmath.h`
- `NxtrLib/include/fpmtype.h`
- `NxtrLib/include/interpolation.h`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 2 files)</summary>

- `NxtrLib/utp/contract/Platform_Types.h`
- `NxtrLib/utp/contract/float.h`

</details>

Assembly sources:

- `NxtrLib/src/atan2.asm`

RTE/BSW generation templates (`generate/`, consumed by the Vector generators — the outputs land in the ECU project `GenData*` folders, not here):

- `NxtrLib/generate/SystemTime_Cfg.h.tt`

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `DtrmnElapsedTime_uS_u16` | `SystemTime.c` |
| `DtrmnElapsedTime_uS_u32` | `SystemTime.c` |
| `DtrmnElapsedTime_mS_u16` | `SystemTime.c` |
| `DtrmnElapsedTime_mS_u32` | `SystemTime.c` |
| `GetSystemTime_uS_u32` | `SystemTime.c` |
| `GetSystemTime_mS_u32` | `SystemTime.c` |
| `SystemTime_Init` | `SystemTime.c` |
| `SystemTime_Per1` | `SystemTime.c` |
| `BilinearXYM_s16_u16Xs16YM_Cnt` | `interpolation.c` |
| `BilinearXYM_u16_u16Xu16YM_Cnt` | `interpolation.c` |
| `BilinearXYM_s16_s16Xs16YM_Cnt` | `interpolation.c` |
| `BilinearXYM_u16_s16Xu16YM_Cnt` | `interpolation.c` |
| `BilinearXMYM_u16_u16XMu16YM_Cnt` | `interpolation.c` |
| `BilinearXMYM_s16_u16XMs16YM_Cnt` | `interpolation.c` |
| `BilinearXMYM_s16_s16XMs16YM_Cnt` | `interpolation.c` |
| `BilinearXMYM_u16_s16XMu16YM_Cnt` | `interpolation.c` |
| `IntplVarXY_u16_u16Xu16Y_Cnt` | `interpolation.c` |
| `IntplVarXY_u16_s16Xu16Y_Cnt` | `interpolation.c` |
| `IntplVarXY_s16_s16Xs16Y_Cnt` | `interpolation.c` |
| `IntplVarXY_s16_u16Xs16Y_Cnt` | `interpolation.c` |
| `IntplFxdX_u16_u16Xu16Y_Cnt` | `interpolation.c` |
| `IntplFxdX_u16_s16Xu16Y_Cnt` | `interpolation.c` |
| `IntplFxdX_s16_s16Xs16Y_Cnt` | `interpolation.c` |
| `IntplFxdX_s16_u16Xs16Y_Cnt` | `interpolation.c` |

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
SystemTime_Init();            /* once, during startup */
SystemTime_Per1(/* ports */);  /* periodically, via RTE runnable */
```

## Dependencies

RTE (generated per ECU project, Vector MICROSAR/DaVinci — consumed, not owned):

- `Rte_NexteerLibs.h`
- `Rte_Type.h`

Shared project services used:

- `GlobalMacro.h` (calibration constants / system time / global macros)
- `Std_Types.h` (calibration constants / system time / global macros)
- `SystemTime.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `CheckSums.h`
- `Filter_Types.h`
- `GlobalMacro.h`
- `Gpt.h`
- `Gpt_Cfg.h`
- `MemMap.h`
- `Platform_Types.h`
- `Std_Types.h`
- `SystemTime.h`
- `SystemTime_Cfg.h`
- `filters.h`
- `fixmath.h`
- `fpmtype.h`

</details>

## Documents

The module ships 3 Word/PDF/text documentation file(s) plus 2 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `NxtrLib/doc/Filter_Library_Design_Document.doc`
- `NxtrLib/doc/Interpolation_Design_MDD.doc`
- `NxtrLib/doc/NxtrLib_Systemtime Integration_Manual.docx`
