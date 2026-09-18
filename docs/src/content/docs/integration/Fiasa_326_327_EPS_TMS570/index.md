---
title: "Fiat 326/327 EPS TMS570 ECU Project"
description: "Fiat 326/327 EPS TMS570 ECU Project (Fiasa_326_327_EPS_TMS570) — ECU project for the Fiat 326/327 EPS on the TMS570: CCS build project, configured Vector MICROSAR BSW, DaVinci"
---

# Fiat 326/327 EPS TMS570 ECU Project

*Repository directory: `Fiasa_326_327_EPS_TMS570`*

:::note[Origin: Mixed — Vector MICROSAR + Nexteer integration]
ECU project: Vector MICROSAR BSW sources/configuration and DaVinci-generated RTE/BSW files alongside Nexteer integration code (`Source/`, `SwProject/`).
:::

## Purpose and responsibility

ECU project for the Fiat 326/327 EPS on the TMS570: CCS build project, configured Vector MICROSAR BSW, DaVinci-generated RTE/BSW configuration (`GenData*`), linker/target setup and project-specific integration software components.

> **Note:** this directory mixes AUTOSAR naming prefixes (`Ap_`, `Cd_`, `Sa_`); it is grouped under Project & Integration by its primary role, with cross-references where relevant.

## Key files

Implementation (`src/` or module root):

- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/src/Sa_CDDInterface.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/CMS_Fiasa/src/EPS_DiagSrvcs_ISO.Customer.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/CMS_Fiasa/src/EPS_DiagSrvcs_SrvcLUTbl.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/ChkPt/src/Ap_ChkPtAp10.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/ChkPt/src/Ap_ChkPtAp8.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/ChkPt/src/Ap_ChkPtAp9.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/DemIf/src/Ap_DemIf.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/DfltConfigData/src/Ap_DfltConfigData.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/DiagSvc/src/Ap_DiagSvc.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/IoHwAbstractionUsr/src/IoHwAbstractionUsr.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/AppStartupCallout.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/ApplCallbacks.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/BswM/BswM.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/Can/Can.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/Can/Can_Irq.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/CanIf/CanIf.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/CanNm/CanNm.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/CanSM/CanSM.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/CanTp/CanTp.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/CanXcp/CanXcp.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/Com/Com.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/ComM/ComM.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/Crc/Crc.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/Dcm/Dcm.c`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/Dem/Dem.c`
- …and 127 more `.c` file(s).

Public headers (`include/` / `generate/`):

- `Fiasa_326_327_EPS_TMS570/SwProject/CMS_Fiasa/include/EPS_DiagSrvcs_ISO.Customer.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CMS_Fiasa/include/EPS_DiagSrvcs_ISO.Interface.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CMS_Fiasa/include/EPS_DiagSrvcs_XCP.Interface.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/DfltConfigData/include/Ap_DfltConfigData.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/DiagSvc/include/Ap_DiagSvc.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/Adc2_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/Adc_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/ApplCallbacks.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/BatteryVoltage_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/CmMtrCurr_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/Det_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/DigMSB_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/Dma_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/EcuCommonData.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/I2cNxtr_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/Lnk_Symbols.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/MemMap.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/MtrCtrl_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/MtrVel_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/Nhet_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/NtWrap.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/NtWrap_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/PwmCdd_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/SchM.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/Header/SchM_BswM.h`
- …and 402 more header(s).

<details>
<summary>Unit-test RTE stubs (`utp/contract/`, Vector-generated, 168 files)</summary>

- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/CDD_Const.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/CDD_Data.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/CalConstants.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/Compiler_Cfg.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/EPS_DiagSrvcs_SrvcLUTbl.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/Interrupts.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/MemMap.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/Nhet.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/Nhet2_ePWM_Prog.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/Nhet_SENT_Prog.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/Rte.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/Rte_Sa_CDDInterface.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/Rte_Type.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/contract/std_nhet.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CMS_Fiasa/utp/contract/Ap_DfltConfigData.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CMS_Fiasa/utp/contract/Ap_DiagMgr.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CMS_Fiasa/utp/contract/Ap_DiagMgr_Types.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CMS_Fiasa/utp/contract/CDD_Const.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CMS_Fiasa/utp/contract/CDD_Data.h`
- `Fiasa_326_327_EPS_TMS570/SwProject/CMS_Fiasa/utp/contract/CalConstants.h`
- …and 148 more.

</details>

Assembly sources:

- `Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/Os/osekasm.asm`
- `Fiasa_326_327_EPS_TMS570/SwProject/Source/GenDataOS/intvect.asm`
- `Fiasa_326_327_EPS_TMS570/Tools/GliwaT1/Overlay/Fiasa_326_327_EPS_TMS570/SwProject/Source/BSW/Os/osekasm.asm`
- `Fiasa_326_327_EPS_TMS570/Tools/GliwaT1/Overlay/Haitec_LC_EPS_TMS570/SwProject/Source/BSW/Os/osekasm.asm`

Prebuilt libraries linked from this module:

- `Fiasa_326_327_EPS_TMS570/Tools/AsrProject/Generators/SafeWdg/WdgM_Verifier/libwdgm_verifierdll.a`

## Public API (extracted from sources)

Non-static function definitions found in the module `.c` files (file shown for reference; signatures live in the headers above):

| Function | Defined in |
| --- | --- |
| `CDDInterface_Init1` | `Sa_CDDInterface.c` |
| `CDDInterface_Init2` | `Sa_CDDInterface.c` |
| `CDDInterface_Per1` | `Sa_CDDInterface.c` |
| `CDDInterface_Per2` | `Sa_CDDInterface.c` |
| `CDDInterface_Per4` | `Sa_CDDInterface.c` |
| `CDDPorts_ApplyMtrElecMechPol` | `Sa_CDDInterface.c` |
| `CDDInterface_Per5` | `Sa_CDDInterface.c` |
| `ChkPtAp10_100msEnd_Per` | `Ap_ChkPtAp10.c` |
| `ChkPtAp10_100msStart_Per` | `Ap_ChkPtAp10.c` |
| `ChkPtAp10_10msEnd_Per` | `Ap_ChkPtAp10.c` |
| `ChkPtAp10_10msStart_Per` | `Ap_ChkPtAp10.c` |
| `ChkPtAp10_2msEnd_Per` | `Ap_ChkPtAp10.c` |
| `ChkPtAp10_2msStart_Per` | `Ap_ChkPtAp10.c` |
| `ChkPtAp10_4msEnd_Per` | `Ap_ChkPtAp10.c` |
| `ChkPtAp10_4msStart_Per` | `Ap_ChkPtAp10.c` |
| `ChkPtAp8_100msEnd_Per` | `Ap_ChkPtAp8.c` |
| `ChkPtAp8_100msStart_Per` | `Ap_ChkPtAp8.c` |
| `ChkPtAp8_2msEnd_Per` | `Ap_ChkPtAp8.c` |
| `ChkPtAp8_2msStart_Per` | `Ap_ChkPtAp8.c` |
| `ChkPtAp9_100msEnd_Per` | `Ap_ChkPtAp9.c` |
| `ChkPtAp9_100msStart_Per` | `Ap_ChkPtAp9.c` |
| `ChkPtAp9_10msEnd_Per` | `Ap_ChkPtAp9.c` |
| `ChkPtAp9_10msStart_Per` | `Ap_ChkPtAp9.c` |
| `ChkPtAp9_2msEnd_Per` | `Ap_ChkPtAp9.c` |
| `ChkPtAp9_2msStart_Per` | `Ap_ChkPtAp9.c` |
| `ChkPtAp9_4msEnd_Per` | `Ap_ChkPtAp9.c` |
| `ChkPtAp9_4msStart_Per` | `Ap_ChkPtAp9.c` |
| `DemIf_DemShutdown` | `Ap_DemIf.c` |
| `DemIf_RestartDem` | `Ap_DemIf.c` |
| `DemIf_SetEventStatus` | `Ap_DemIf.c` |

*Table truncated — 898 functions detected in total.*

## Typical usage

Call pattern derived from the detected entry points (exact runnable mapping is defined by the RTE configuration in the ECU project):

```c
CDDInterface_Init1();            /* once, during startup */
CDDInterface_Init2();            /* once, during startup */
CDDInterface_Per1(/* ports */);  /* periodically, via RTE runnable */
CDDInterface_Per2(/* ports */);  /* periodically, via RTE runnable */
CDDInterface_Per4(/* ports */);  /* periodically, via RTE runnable */
CDDInterface_Per5(/* ports */);  /* periodically, via RTE runnable */
```

## Dependencies

RTE (generated per ECU project, Vector MICROSAR/DaVinci — consumed, not owned):

- `Rte_Ap_AbsHwPos.h`
- `Rte_Ap_ActivePull.h`
- `Rte_Ap_ApXcp.h`
- `Rte_Ap_Assist.h`
- `Rte_Ap_AssistFirewall.h`
- `Rte_Ap_AstLmt.h`
- `Rte_Ap_AvgFricLrn.h`
- `Rte_Ap_BVDiag.h`
- `Rte_Ap_BatteryVoltage.h`
- `Rte_Ap_ChkPtAp10.h`
- `Rte_Ap_ChkPtAp8.h`
- `Rte_Ap_ChkPtAp9.h`

Shared project services used:

- `CalConstants.h` (calibration constants / system time / global macros)
- `GlobalMacro.h` (calibration constants / system time / global macros)
- `Std_Types.h` (calibration constants / system time / global macros)
- `SystemTime.h` (calibration constants / system time / global macros)

<details>
<summary>All quoted project includes (raw, for traceability)</summary>

- `Adc.h`
- `Adc2.h`
- `Adc2_Cfg.h`
- `Adc_Cfg.h`
- `Adc_Common.h`
- `AmdRtm.h`
- `Ap_ApXcp.h`
- `Ap_DfltConfigData.h`
- `Ap_DiagMgr.h`
- `Ap_DiagMgr_Types.h`
- `Ap_DiagSvc.h`
- `Ap_MtrCtrl.h`
- `Ap_StaMd.h`
- `Ap_StaMd_Cfg.h`
- `Ap_VehPwrMd_Cfg.h`
- `ApplCallbacks.h`
- `Appl_Cbk.h`
- `Appl_Dem.h`
- `Appl_Det.h`
- `Appl_Mcu.h`
- `BswM.h`
- `BswM_CanSM.h`
- `BswM_ComM.h`
- `BswM_Dcm.h`
- `CDD_Const.h`
- `CDD_Data.h`
- `CDD_Func.h`
- `CalConstants.h`
- `Can.h`
- `CanIf.h`
- `CanIf_Cbk.h`
- `CanIf_Cfg.h`
- `CanIf_Types.h`
- `CanNm.h`
- `CanNm_Cbk.h`
- `CanNm_Cfg.h`
- `CanNm_cfg.h`
- `CanSM.h`
- `CanSM_BswM.h`
- `CanSM_Cbk.h`
- `CanSM_ComM.h`
- `CanSM_EcuM.h`
- `CanSM_SchM.h`
- `CanTp.h`
- `CanTp_Cbk.h`
- `CanTp_Cfg.h`
- `CanTp_Lcfg.h`
- `CanTp_PBcfg.h`
- `CanTp_Priv.h`
- `CanTp_Types.h`
- `CanXcp.h`
- `CanXcp_Cfg.h`
- `CanXcp_Types.h`
- `Can_Cfg.h`
- `Cd_FeeIf.h`
- `Cd_NvMProxy.h`
- `Cd_NvMProxy_Cfg.h`
- `Com.h`
- `ComM.h`
- `ComM_BusSM.h`
- …and 213 more.

</details>

## Documents

The module ships 48 Word/PDF/text documentation file(s) plus 272 QA-C analyser output(s). Summaries and conversion notes live on the documents page:

- [Design and reference documents](./documents/)

Source files:

- `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_ASR_IpduM.pdf`
- `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_BswM.pdf`
- `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanIf.pdf`
- `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanNm.pdf`
- `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanSM.pdf`
- `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanTp.pdf`
- `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanTrcv_30_GenericDio.pdf`
- `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanXcp.pdf`
- …and 40 more (see documents page).

## ECU project structure

`SwProject/` sub-projects (each typically with its own `src/`, `doc/`, `tools/`, `utp/`):
- Complex Device Driver Interface (`CDDInterface/`)
- Common Manufacturing Services (Fiasa variant) (`CMS_Fiasa/`)
- Checkpoint (program-flow monitoring) (`ChkPt/`)
- Diagnostic Event Manager Interface (`DemIf/`)
- Default Configuration Data (`DfltConfigData/`)
- Diagnostic Services (`DiagSvc/`)
- `Header/`
- I/O Hardware Abstraction (project user code) (`IoHwAbstractionUsr/`)
- `Source/`
- Serial Communication Input (`SrlComInput/`)
- Serial Communication Output (`SrlComOutput/`)
- Vehicle Power Mode (`VehPwrMd/`)

Build artefacts at `SwProject/` root: `Fiasa.ccxml` (CCS target configuration), `TMS570LS202x6SFlashLnk.cmd` (linker command file), `T1_Fast.inc`, `postbuild.bat`.

Notable `Source/` contents: `BSW/` (configured Vector MICROSAR stack — [reference](./../../bsw/vector-microsar-stack/)), `CDD/`, `GenData*/` (~200 DaVinci/MICROSAR-generated RTE/BSW configuration files), `IoHwAb.c`, `NtWrap.c`, `SchM.c`.

`Tools/` hosted utilities and generator plug-ins:
- `AsrProject/`
- `CCT/`
- `GliwaT1/`
- `GnuWin32/`
- `Metrics/`
- `OilTool/`
- `Patch/`
- `Polyspace/`
- `QAC/`

`HLDD/` holds the Vector Technical References for the configured BSW (summarised on the [documents page](./documents/)).
