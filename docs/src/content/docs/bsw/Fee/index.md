---
title: "Flash EEPROM Emulation Driver (Texas Instruments)"
description: "Flash EEPROM Emulation Driver (Texas Instruments) (Fee) — This file implements the Autosar FEE 3.1 Api's."
---

# Flash EEPROM Emulation Driver (Texas Instruments)

*Repository directory: `Fee`*

:::caution[Origin: Third-party — Texas Instruments (adapted)]
TI FEE driver sources delivered for TMS570, integrated behind the Nexteer `Cd_FeeIf` wrapper in `NvMMgr`.
:::

## Purpose and responsibility

This file implements the Autosar FEE 3.1 Api's.

## Key files

Implementation (`src/` or module root):

- `Fee/generate/Fee/T_Fee_Cfg.c`
- `Fee/src/Device_TMS570LS07.c`
- `Fee/src/Device_TMS570LS12.c`
- `Fee/src/fee.c`
- `Fee/src/ti_fee_Info.c`
- `Fee/src/ti_fee_cancel.c`
- `Fee/src/ti_fee_eraseimmediateblock.c`
- `Fee/src/ti_fee_format.c`
- `Fee/src/ti_fee_ini.c`
- `Fee/src/ti_fee_invalidateblock.c`
- `Fee/src/ti_fee_main.c`
- `Fee/src/ti_fee_read.c`
- `Fee/src/ti_fee_readSync.c`
- `Fee/src/ti_fee_shutdown.c`
- `Fee/src/ti_fee_util.c`
- `Fee/src/ti_fee_writeAsync.c`
- `Fee/src/ti_fee_writeSync.c`

Public headers (`include/` / `generate/`):

- `Fee/generate/Fee/T_Fee_Cfg.h`
- `Fee/include/Device_Header.h`
- `Fee/include/Device_TMS570LS07.h`
- `Fee/include/Device_TMS570LS12.h`
- `Fee/include/Device_types.h`
- `Fee/include/Fee_Cbk.h`
- `Fee/include/fee.h`
- `Fee/include/fee_interface.h`
- `Fee/include/fee_memmap.h`
- `Fee/include/ti_fee.h`
- `Fee/include/ti_fee_cfg.h`
- `Fee/include/ti_fee_types.h`

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 15 files)</summary>

- `Fee/utp/contract/Fee/Compiler_Cfg.h`
- `Fee/utp/contract/Fee/Constants.h`
- `Fee/utp/contract/Fee/Det.h`
- `Fee/utp/contract/Fee/F021.h`
- `Fee/utp/contract/Fee/Helpers.h`
- `Fee/utp/contract/Fee/MemIf_Types.h`
- `Fee/utp/contract/Fee/MemMap.h`
- `Fee/utp/contract/Fee/NvM_Cfg.h`
- `Fee/utp/contract/Fee/Registers.h`
- `Fee/utp/contract/Fee/Registers_FMC_BE.h`
- `Fee/utp/contract/Fee/SchM_Fee.h`
- `Fee/utp/contract/Fee/Types.h`
- `Fee/utp/contract/Fee/fee_cfg.h`
- `Fee/utp/contract/Fee/nvm.h`
- `Fee/utp/contract/Fee/stdint.h`

</details>

RTE/BSW generation templates (`generate/`, consumed by the Vector generators — the outputs land in the ECU project `GenData*` folders, not here):

- `Fee/generate/ (see folder)`

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `Fee_Write` | `fee.c` |
| `Fee_Read` | `fee.c` |
| `Fee_GetVersionInfo` | `fee.c` |
| `Fee_InternalUpdateGlobalStructure` | `fee.c` |
| `TI_Fee_GetVersionInfo` | `ti_fee_Info.c` |
| `TI_Fee_Cancel` | `ti_fee_cancel.c` |
| `TI_Fee_EraseImmediateBlock` | `ti_fee_eraseimmediateblock.c` |
| `TI_Fee_Format` | `ti_fee_format.c` |
| `TI_Fee_Init` | `ti_fee_ini.c` |
| `TI_Fee_InvalidateBlock` | `ti_fee_invalidateblock.c` |
| `TI_Fee_Read` | `ti_fee_read.c` |
| `TI_Fee_ReadSync` | `ti_fee_readSync.c` |
| `TI_Fee_Shutdown` | `ti_fee_shutdown.c` |
| `TI_FeeInternal_WriteDataF021` | `ti_fee_util.c` |
| `TI_FeeInternal_WriteInitialize` | `ti_fee_util.c` |
| `TI_FeeInternal_GetBlockSize` | `ti_fee_util.c` |
| `TI_FeeInternal_GetBlockIndex` | `ti_fee_util.c` |
| `TI_FeeInternal_GetArrayIndex` | `ti_fee_util.c` |
| `TI_FeeInternal_UpdateBlockOffsetArray` | `ti_fee_util.c` |
| `TI_FeeInternal_CheckModuleState` | `ti_fee_util.c` |
| `TI_FeeInternal_SanityCheck` | `ti_fee_util.c` |
| `TI_FeeInternal_WriteBlockHeader` | `ti_fee_util.c` |
| `TI_FeeInternal_WritePreviousBlockHeader` | `ti_fee_util.c` |
| `TI_FeeInternal_InvalidateErase` | `ti_fee_util.c` |
| `TI_FeeInternal_StartProgramBlock` | `ti_fee_util.c` |
| `TI_FeeInternal_CheckForError` | `ti_fee_util.c` |
| `TI_FeeInternal_Fletcher16` | `ti_fee_util.c` |
| `TI_Fee_ErrorRecovery` | `ti_fee_util.c` |
| `TI_Fee_ErrorHookSingleBitError` | `ti_fee_util.c` |
| `TI_Fee_ErrorHookDoubleBitError` | `ti_fee_util.c` |

*Table truncated — 34 functions detected in total.*

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
TI_Fee_Init();            /* once, during startup */
TI_FeeInternal_WriteInitialize();            /* once, during startup */
```

## Dependencies

Shared project services used:

- `Std_Types.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Constants.h`
- `Det.h`
- `Device_TMS570LS07.h`
- `Device_TMS570LS12.h`
- `Device_header.h`
- `Device_types.h`
- `F021.h`
- `Fee.h`
- `Fee_Cbk.h`
- `Fee_Cfg.h`
- `Helpers.h`
- `MemIf_Types.h`
- `MemMap.h`
- `NvM_Cfg.h`
- `Registers.h`
- `Registers_FMC_BE.h`
- `Registers_FMC_LE.h`
- `SchM_Fee.h`
- `Std_Types.h`
- `Types.h`
- `fee_cfg.h`
- `fee_interface.h`
- `nvm.h`
- `stdint.h`
- `ti_fee.h`
- `ti_fee_cfg.h`
- `ti_fee_types.h`

</details>

## Documents

The module ships 2 Word/PDF/text documentation file(s) plus 32 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `Fee/doc/AutoSAR FEE Parameter Configuration.pdf`
- `Fee/doc/AutoSAR FEE User Guide.pdf`
