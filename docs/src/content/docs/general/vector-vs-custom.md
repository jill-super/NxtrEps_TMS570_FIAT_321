---
title: "Vector vs. custom"
description: "Origin taxonomy: Vector-provided, in-house and third-party code, and how each module was classified."
---


# Vector vs. custom

## Taxonomy

| Badge | Meaning | Examples |
| --- | --- | --- |
| Custom — Nexteer in-house | Written for this project (Nexteer copyright headers) | most `Ap_*`/`Sa_*` modules, `Adc`, `SpiNxt`, `NxtrLib` |
| Custom — Nexteer logic on Vector-generated scaffold | Same as above, but the file header carries a `MICROSAR RTE Generator` banner and the module ships an `autosar/` model + `utp/contract` RTE stubs | most RTE software components |
| Vector-provided | Delivered/configured by Vector tooling; project only configures and generates | MICROSAR BSW in the ECU project, `GenData*` outputs, `Rte*.h` contract stubs |
| Mixed — Vector MICROSAR + Nexteer integration | ECU project combining both | `Fiasa_326_327_EPS_TMS570` |
| Third-party — Texas Instruments | Silicon-vendor delivery | `Fee` (FEE driver), `Fls` (F021 Flash API `.lib`) |
| Third-party — Gliwa | Measurement stack | `GliwaT1` (`libt1*.a`) |
| Tooling configuration | No ECU code | `QAC` |

## Detection method (reproducible)

For each module the generator sampled the headers of up to four `.c` files plus two public headers and searched for:

- `Nexteer` → in-house; `MICROSAR RTE Generator` / `Vector Informatik` / `DaVinci` → Vector-generated scaffold; `Texas Instruments` / `F021` / `Hercules` → TI; `Gliwa` → Gliwa.
- The verdict and its evidence class are recorded on every module page; ambiguous cases are labelled *assumed* and explained there.

## Full module × origin table

Names are the long display names; the repository directory short name follows in parentheses.

| Module | Layer | Origin |
| --- | --- | --- |
| [Absolute Handwheel Position (Turns Counter, I²C, Sensorless Vehicle Dynamics) (`AbsHwPos_TcI2cVd`)](./../asw/AbsHwPos_TcI2cVd/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Active Pull Compensation (`ActivePull`)](./../asw/ActivePull/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Analog-to-Digital Converter Driver (`Adc`)](./../cdd/Adc/) | Complex Device Drivers (CDD) | Custom — Nexteer in-house |
| [Base Steering Assist (`Assist`)](./../asw/Assist/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Assist Firewall (`AssistFirewall`)](./../asw/AssistFirewall/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Assist Sum and Limit (Current Mode) (`AstLmt_CM`)](./../asw/AstLmt_CM/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Average Friction Learning (`AvgFricLrn`)](./../asw/AvgFricLrn/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Battery Voltage Diagnostics (`BVDiag`)](./../asw/BVDiag/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Battery Voltage (`BatteryVoltage`)](./../asw/BatteryVoltage/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Bulk Capacitor Precharge and Power Disconnect (`BkCpPc`)](./../cdd/BkCpPc/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
| [Common Manufacturing Services (`CMS_Common`)](./../libs/CMS_Common/) | Libraries & Common | Custom — Nexteer in-house |
| [Common Motor Current Measurement (`CmMtrCurr`)](./../cdd/CmMtrCurr/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
| [Compliance Error (`ComplErr`)](./../asw/ComplErr/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Controller Temperature Monitor (`CtrlTemp`)](./../cdd/CtrlTemp/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
| [Controlled Disable Shutdown (`CtrldDisShtdn`)](./../asw/CtrldDisShtdn/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Steering Damping (`Damping`)](./../asw/Damping/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Damping Firewall (`DampingFirewall`)](./../asw/DampingFirewall/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Diagnostics Manager (`DiagMgr`)](./../asw/DiagMgr/) | Application Software (ASW) | Custom — Nexteer in-house |
| [Digital Column Position Sensor Interface (I²C) (`DigColPs`)](./../cdd/DigColPs/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
| [Digital Handwheel Torque Sensing (SENT) (`DigHwTrqSENT`)](./../cdd/DigHwTrqSENT/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
| [Digital MSB Position Sensor Interface (`DigMSB`)](./../cdd/DigMSB/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
| [Direct Memory Access Driver (`Dma`)](./../cdd/Dma/) | Complex Device Drivers (CDD) | Custom — Nexteer in-house |
| [End-of-Travel Actuator Management (`EOTActuatorMng`)](./../asw/EOTActuatorMng/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Electric Power Consumption Monitor (`ElePwr`)](./../asw/ElePwr/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [End-of-Travel Damping Firewall (`EtDmpFw`)](./../asw/EtDmpFw/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Flash EEPROM Emulation Driver (Texas Instruments) (`Fee`)](./../bsw/Fee/) | Basic Software — Services | Third-party — Texas Instruments (adapted) |
| [Fiat 326/327 EPS TMS570 ECU Project (`Fiasa_326_327_EPS_TMS570`)](./../integration/Fiasa_326_327_EPS_TMS570/) | Project & Integration | Mixed — Vector MICROSAR + Nexteer integration |
| [Flash Memory Driver (TI F021 Flash API) (`Fls`)](./../bsw/Fls/) | Basic Software — Services | Third-party — Texas Instruments |
| [Fault Injection (`FltInjection`)](./../asw/FltInjection/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Frequency-Dependent Damping and Inertia Compensation (`FrqDepDmpnInrtCmp`)](./../asw/FrqDepDmpnInrtCmp/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Gliwa T1 Timing Measurement (`GliwaT1`)](./../integration/GliwaT1/) | Project & Integration | Third-party — Gliwa |
| [Global Signal Overwrite Detection (`Gsod`)](./../asw/Gsod/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [High-Load Stall Thermal Management (`HiLoadStall`)](./../asw/HiLoadStall/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [High-Frequency Assist (`HighFreqAssist`)](./../asw/HighFreqAssist/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Hardware Power-Up Sequence (`HwPwUp`)](./../asw/HwPwUp/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Hysteresis Compensation (`HystComp`)](./../asw/HystComp/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [I²C Driver (Nexteer) (`I2cNxtr`)](./../cdd/I2cNxtr/) | Complex Device Drivers (CDD) | Custom — Nexteer in-house |
| [Limiter Conditioning (`LmtCod`)](./../asw/LmtCod/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [End-of-Travel Position Learning (`LrnEOT`)](./../asw/LrnEOT/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Motor Control (Current Mode) (`MtrCtrl_CM`)](./../asw/MtrCtrl_CM/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Motor Temperature Estimation (`MtrTempEst`)](./../asw/MtrTempEst/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Motor Velocity Sensing (Digital) (`MtrVel_Digi`)](./../cdd/MtrVel_Digi/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
| [NVRAM Manager (FEE Interface) (`NvMMgr`)](./../bsw/NvMMgr/) | Basic Software — Services | Custom — Nexteer in-house |
| [NVRAM Proxy (`NvMProxy`)](./../bsw/NvMProxy/) | Basic Software — Services | Custom — Nexteer in-house |
| [Nexteer Shared Library (Math, Filters, System Time) (`NxtrLib`)](./../libs/NxtrLib/) | Libraries & Common | Custom — Nexteer in-house |
| [Overvoltage Monitor (`OvrVoltMon`)](./../cdd/OvrVoltMon/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
| [Signal Polarity Assignment (`Polarity`)](./../asw/Polarity/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Power Limit Function (Current Mode) (`PwrLmtFuncCr`)](./../asw/PwrLmtFuncCr/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [QA-C Static Analysis Configuration (MISRA) (`QAC`)](./../integration/QAC/) | Project & Integration | Tooling configuration |
| [Return Torque Control (`Return`)](./../asw/Return/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Return Firewall (`ReturnFirewall`)](./../asw/ReturnFirewall/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Sine-Voltage Drive Diagnostics (`SVDiag`)](./../asw/SVDiag/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Sine-Voltage Motor Driver (Current Mode) (`SVDrvr_CM`)](./../cdd/SVDrvr_CM/) | Complex Device Drivers (CDD) | Custom — Nexteer in-house |
| [Signal Conditioning (`SgnlCond`)](./../asw/SgnlCond/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Shutdown Mechanisms (`ShtdnMech`)](./../cdd/ShtdnMech/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
| [SPI Driver (Nexteer) (`SpiNxt`)](./../cdd/SpiNxt/) | Complex Device Drivers (CDD) | Custom — Nexteer in-house |
| [State Output Control (`StOpCtrl`)](./../asw/StOpCtrl/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [States and Modes (`StaMd`)](./../asw/StaMd/) | Application Software (ASW) | Custom — Nexteer in-house |
| [Stability Compensation (`StabilityComp`)](./../asw/StabilityComp/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Standard Platform Type Definitions (`StdDef`)](./../libs/StdDef/) | Libraries & Common | Custom — Nexteer (+ toolchain headers) |
| [Torque Sweep Generator (`Sweep`)](./../asw/Sweep/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [TMS570 Startup (System, Boot and Interrupt Vectors) (`TMS570_Startup`)](./../cdd/TMS570_Startup/) | Complex Device Drivers (CDD) | Custom — Nexteer in-house |
| [TMS570 Microcontroller Diagnostics (`TMS570_uDiag`)](./../cdd/TMS570_uDiag/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
| [Thermal Duty Cycle (`ThrmDutyCycle`)](./../asw/ThrmDutyCycle/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Temporal Monitor (`TmprlMon`)](./../cdd/TmprlMon/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
| [Torque Reasonableness Diagnostics (`TqRsDg`)](./../asw/TqRsDg/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Tuning Select Authority (`TuningSelAuth`)](./../asw/TuningSelAuth/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Vehicle Dynamics (`VehDyn`)](./../asw/VehDyn/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Vehicle Speed Limiting (`VehSpdLmt`)](./../asw/VehSpdLmt/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [XCP Measurement and Calibration Interface (`Xcp`)](./../asw/Xcp/) | Application Software (ASW) | Custom — Nexteer logic on Vector-generated scaffold |
| [Enhanced PWM and NHET Driver (`ePWM`)](./../cdd/ePWM/) | Complex Device Drivers (CDD) | Custom — Nexteer logic on Vector-generated scaffold |
