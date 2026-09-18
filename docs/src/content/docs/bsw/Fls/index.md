---
title: "Flash Memory Driver (TI F021 Flash API)"
description: "Flash Memory Driver (TI F021 Flash API) (Fls) — ARM compiler specific info used by the F021 API."
---

# Flash Memory Driver (TI F021 Flash API)

*Repository directory: `Fls`*

:::caution[Origin: Third-party — Texas Instruments]
Hercules F021 Flash API (binary library plus headers). Proprietary TI delivery; see `Fls/doc/`.
:::

## Purpose and responsibility

ARM compiler specific info used by the F021 API.

## Key files

Public headers (`include/` / `generate/`):

- `Fls/include/CGT.ARM.h`
- `Fls/include/CGT.CCS.h`
- `Fls/include/CGT.GHS.h`
- `Fls/include/CGT.IAR.h`
- `Fls/include/CGT.gcc.h`
- `Fls/include/Compatibility.h`
- `Fls/include/Constants.h`
- `Fls/include/F021.h`
- `Fls/include/FapiFunctions.h`
- `Fls/include/Helpers.h`
- `Fls/include/Registers.h`
- `Fls/include/Registers_FMC_BE.h`
- `Fls/include/Registers_FMC_LE.h`
- `Fls/include/Types.h`

Prebuilt libraries linked from this module:

- `Fls/src/F021_API_CortexR4_BE_V3D16.lib`

## Public API

No C function definitions were detected in this module (it may ship headers, libraries, configuration or tooling only).

## Dependencies

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `CGT.ARM.h`
- `CGT.CCS.h`
- `CGT.GHS.h`
- `CGT.IAR.h`
- `CGT.gcc.h`
- `Compatibility.h`
- `Constants.h`
- `FapiFunctions.h`
- `Helpers.h`
- `Registers.h`
- `Registers_FMC_BE.h`
- `Registers_FMC_LE.h`
- `Types.h`

</details>

## Documents

The module ships 7 Word/PDF/text documentation file(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `Fls/doc/F021_Flash_API_License_Agreement.pdf`
- `Fls/doc/Release_Notes.pdf`
- `Fls/doc/SPNA148.pdf`
- `Fls/doc/SPNU501F.pdf`
- `Fls/doc/SPNZ210.pdf`
- `Fls/doc/build_information.txt`
- `Fls/doc/readme.txt`
