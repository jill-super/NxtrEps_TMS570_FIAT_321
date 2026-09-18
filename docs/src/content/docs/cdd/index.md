---
title: "Complex Device Drivers (CDD)"
description: "Hardware-near drivers and sensor/actuator components (`Sa_*`, `Cd_*`, direct-register drivers)."
---


# Complex Device Drivers (CDD)

Hardware-near drivers and sensor/actuator components (`Sa_*`, `Cd_*`, direct-register drivers).

This layer contains **18** module(s).

| Module | Origin | Purpose |
| --- | --- | --- |
| [Analog-to-Digital Converter Driver](./Adc/) | Custom — Nexteer in-house | The Adc Common module provides “stateless” application context independent functions which provide functionali |
| [Bulk Capacitor Precharge and Power Disconnect](./BkCpPc/) | Custom — Nexteer logic on Vector-generated scaffold | This module handles precharging of the bulk capacitor during initialization. |
| [Common Motor Current Measurement](./CmMtrCurr/) | Custom — Nexteer logic on Vector-generated scaffold | The Current Measurement function is responsible for measuring the motor phase currents used as feedback by the |
| [Controller Temperature Monitor](./CtrlTemp/) | Custom — Nexteer logic on Vector-generated scaffold | This module monitors the controller’s temperature sensor output, filters that output, and checks whether the o |
| [Digital Column Position Sensor Interface (I²C)](./DigColPs/) | Custom — Nexteer logic on Vector-generated scaffold | The digital column position sensor component reads sensor data from the digital column position sensor interfa |
| [Digital Handwheel Torque Sensing (SENT)](./DigHwTrqSENT/) | Custom — Nexteer logic on Vector-generated scaffold | This module computes the digital handwheel torque signal from the SENT digital sensor inputs. |
| [Digital MSB Position Sensor Interface](./DigMSB/) | Custom — Nexteer logic on Vector-generated scaffold | The data synchronsiation between Motor Control ISR and 2 ms Task will be provided at the integration level. |
| [Direct Memory Access Driver](./Dma/) | Custom — Nexteer in-house | DMA is a driver level module that performs flash, RAM, and peripheral reads and writes in the background, free |
| [Enhanced PWM and NHET Driver](./ePWM/) | Custom — Nexteer logic on Vector-generated scaffold | This module implements NHET1 and HTU1 initialization per ES-34B NHET1 subfunctions, and NHET2 initialization,  |
| [I²C Driver (Nexteer)](./I2cNxtr/) | Custom — Nexteer in-house | I2C Driver: Nexteer implementation. |
| [Motor Velocity Sensing (Digital)](./MtrVel_Digi/) | Custom — Nexteer logic on Vector-generated scaffold | Configuration file of DiagMgr module |
| [Overvoltage Monitor](./OvrVoltMon/) | Custom — Nexteer logic on Vector-generated scaffold | Overvoltage Monitor — role as described by the module design documentation (see Documents). |
| [Shutdown Mechanisms](./ShtdnMech/) | Custom — Nexteer logic on Vector-generated scaffold | This module handles diagnostic data during an F1 fault. |
| [SPI Driver (Nexteer)](./SpiNxt/) | Custom — Nexteer in-house | This module provides the following Autosar API: Spi_SetupEB() Spi_Init() Spi_AsyncTransmit() Spi_GetSequenceRe |
| [Sine-Voltage Motor Driver (Current Mode)](./SVDrvr_CM/) | Custom — Nexteer in-house | Non-AUTOSAR PWM driver required to perform EPS motor control PWM profiles. |
| [Temporal Monitor](./TmprlMon/) | Custom — Nexteer logic on Vector-generated scaffold | This module helps ensure valid execution time for the forward path. |
| [TMS570 Startup (System, Boot and Interrupt Vectors)](./TMS570_Startup/) | Custom — Nexteer in-house | sys_core provides assembly language functions for processor register data access and system startup. |
| [TMS570 Microcontroller Diagnostics](./TMS570_uDiag/) | Custom — Nexteer logic on Vector-generated scaffold | OsErrCallouts provides the error hook functions ErrorHook() and ProtectionHook() to provide diagnostic informa |
