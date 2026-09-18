---
title: "Standard Platform Type Definitions"
description: "Standard Platform Type Definitions (StdDef) — This file provides the AUTOSAR compiler abstraction for the TI TMS470 Code generation Tools (Compiler)"
---

# Standard Platform Type Definitions

*Repository directory: `StdDef`*

:::tip[Origin: Custom — Nexteer (+ toolchain headers)]
Platform abstraction headers (`Std_Types.h`, `Compiler.h`, `Platform_Types.h`) plus compiler/derivative headers.
:::

## Purpose and responsibility

This file provides the AUTOSAR compiler abstraction for the TI TMS470 Code generation Tools (Compiler)

## AUTOSAR software component(s)

Modelled SW-C(s) found in `autosar/` (DaVinci/MICROSAR model, AUTOSAR 3.1.4):

- `Std_WorkSpace`

## Key files

Public headers (`include/` / `generate/`):

- `StdDef/include/Compiler.h`
- `StdDef/include/Platform_Types.h`
- `StdDef/include/Std_Types.h`
- `StdDef/include/TMS570_4_9_1/include/_fmt_specifier.h`
- `StdDef/include/TMS570_4_9_1/include/_isfuncdcl.h`
- `StdDef/include/TMS570_4_9_1/include/_isfuncdef.h`
- `StdDef/include/TMS570_4_9_1/include/_lock.h`
- `StdDef/include/TMS570_4_9_1/include/access.h`
- `StdDef/include/TMS570_4_9_1/include/assert.h`
- `StdDef/include/TMS570_4_9_1/include/cpy_tbl.h`
- `StdDef/include/TMS570_4_9_1/include/crc_tbl.h`
- `StdDef/include/TMS570_4_9_1/include/ctype.h`
- `StdDef/include/TMS570_4_9_1/include/elf_linkage.h`
- `StdDef/include/TMS570_4_9_1/include/errno.h`
- `StdDef/include/TMS570_4_9_1/include/etsi.h`
- `StdDef/include/TMS570_4_9_1/include/fenv.h`
- `StdDef/include/TMS570_4_9_1/include/file.h`
- `StdDef/include/TMS570_4_9_1/include/float.h`
- `StdDef/include/TMS570_4_9_1/include/fstream.h`
- `StdDef/include/TMS570_4_9_1/include/inttypes.h`
- `StdDef/include/TMS570_4_9_1/include/iomanip.h`
- `StdDef/include/TMS570_4_9_1/include/iostream.h`
- `StdDef/include/TMS570_4_9_1/include/iso646.h`
- `StdDef/include/TMS570_4_9_1/include/limits.h`
- `StdDef/include/TMS570_4_9_1/include/linkage.h`
- …and 95 more header(s).

## Public API

No C function definitions were detected in this module (it may ship headers, libraries, configuration or tooling only).

## Dependencies

Shared project services used:

- `Std_Types.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Compiler_Cfg.h`
- `Std_Types.h`
- `_fmt_specifier.h`
- `_isfuncdcl.h`
- `_isfuncdef.h`

</details>

## Documents

No Word/PDF/text documentation files were found in this module.
