---
title: "Vector MICROSAR stack"
description: "Vector-provided BSW modules in the ECU project and their Technical References."
---


# Vector MICROSAR stack

:::note[Origin: Vector-provided]
The modules below are the Vector MICROSAR basic-software delivery, configured with DaVinci for this ECU project. Sources live under `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/`; generated configuration under `Source/GenData*/`. Project code only *configures and calls* these modules.
:::

## Configured BSW modules

| Module | Role (per AUTOSAR / Vector delivery) | Technical Reference (in `HLDD/BSW/`) |
| --- | --- | --- |
| `BswM` | BSW Mode Manager — arbitrates mode requests and triggers mode-switch actions. | `TechnicalReference_Asr_BswM.pdf` |
| `Can` | CAN driver (TMS470 DCAN) — hardware access for the on-chip CAN controller. | `TechnicalReference_Asr_CanIf.pdf` |
| `CanIf` | CAN Interface — abstracts CAN controllers and routes PDUs to upper layers. | `TechnicalReference_Asr_CanIf.pdf` |
| `CanNm` | CAN Network Management — coordinated bus sleep/wakeup handling. | `TechnicalReference_Asr_CanNm.pdf` |
| `CanSM` | CAN State Manager — CAN network state machine, talks to ComM/BswM. | `TechnicalReference_Asr_CanSM.pdf` |
| `CanTp` | CAN Transport Protocol — segmented (ISO-TP) transfer for diagnostics/flashing. | `TechnicalReference_Asr_CanTp.pdf` |
| `CanXcp` | XCP on CAN — transport hook coupling the XCP stack to the CAN driver. | `TechnicalReference_Asr_CanXcp.pdf` |
| `Com` | AUTOSAR COM — signal/PDU packing, transmission modes, reception filtering. | `TechnicalReference_Asr_Com.pdf` |
| `ComM` | Communication Manager — bus communication state coordination. | `TechnicalReference_Asr_ComM.pdf` |
| `Crc` | CRC library — checksum routines used by E2E/safety mechanisms. | `TechnicalReference_Asr_Crc.pdf` |
| `Dcm` | Diagnostic Communication Manager — UDS protocol handling. | `TechnicalReference_Asr_Dcm.pdf` |
| `Dem` | Diagnostic Event Manager — DTC storage, debouncing, status handling. | `TechnicalReference_Asr_Dem.pdf` |
| `Det` | Default Error Tracer — development-error reporting hook. | `TechnicalReference_Asr_Det.pdf` |
| `Dio` | Digital I/O driver — discrete input/output channels. | `TechnicalReference_Asr_CanTrcv_30_GenericDio.pdf` |
| `EcuM` | ECU State Manager — startup/shutdown, sleep/wake sequencing. | `TechnicalReference_Asr_EcuM.pdf` |
| `Gpt` | General Purpose Timer driver — timer channels for schedule tables/timeouts. | — |
| `IoHwAb` | I/O Hardware Abstraction — project signal-level abstraction above MCAL. | `TechnicalReference_Asr_IoHwAb.pdf` |
| `Mcu` | MCU driver — clock, PLL and reset configuration. | — |
| `MemIf` | Memory Abstraction Interface — routes NvM requests to FEE/Flash devices. | `TechnicalReference_Asr_MemIf.pdf` |
| `Nm` | Generic Network Management interface. | `TechnicalReference_Asr_CanNm.pdf` |
| `NvM` | NVRAM Manager — block-based non-volatile data management. | `TechnicalReference_Asr_NvM.pdf` |
| `Os` | AUTOSAR OS (OSEK-compatible) — tasks, alarms, schedule tables, protection. | `TechnicalReference_WakeUp_and_Sleep_with_AUTOSAR.pdf` |
| `PduR` | PDU Router — routes I-PDUs between COM/DCM and interface/transport layers. | `TechnicalReference_Asr_PduR.pdf` |
| `Port` | Port driver — pin multiplexing and direction configuration. | — |
| `VStdLib` | Vector standard library — shared MISRA-safe helper routines. | `TechnicalReference_VStdLib.pdf` |
| `Wdg` | Watchdog driver — hardware watchdog servicing. | — |
| `WdgIf` | Watchdog Interface — abstracts multiple watchdog instances. | — |
| `WdgM` | Watchdog Manager — supervised alive/deadline monitoring of software. | — |
| `Xcp` | Universal Measurement and Calibration Protocol stack. | `TechnicalReference_Asr_CanXcp.pdf` |
| `_Common` | Shared BSW glue (version checks, common callbacks) for the configured stack. | — |

## Generator and tooling references

The `HLDD/BSW/` folder additionally ships Vector tooling references (DaVinci generators, DBC rules, wake-up/sleep application notes). Full per-file records are on the [ECU project documents page](./../integration/Fiasa_326_327_EPS_TMS570/documents/).

## Configuration outputs

The DaVinci/MICROSAR generators emit the ECU configuration into `Source/GenData*/` (~200 files in `GenData/` alone: `*_Cfg.h/.c`, `*_Lcfg.c`, `*_PBcfg.c`, `CalConstants*`). These files are Vector-*generated* for this project and are rebuilt whenever the DaVinci model changes — edit the model, not the output.
