---
title: "Application Software (ASW)"
description: "RTE software components (`Ap_*`): steering functions, arbitration, diagnostics and mode logic."
---


# Application Software (ASW)

RTE software components (`Ap_*`): steering functions, arbitration, diagnostics and mode logic.

This layer contains **43** module(s).

| Module | Origin | Purpose |
| --- | --- | --- |
| [Absolute Handwheel Position (Turns Counter, I²C, Sensorless Vehicle Dynamics)](./AbsHwPos_TcI2cVd/) | Custom — Nexteer logic on Vector-generated scaffold | The Absolute Hand Wheel Position Function is responsible for determining the steering wheel hand wheel positio |
| [Active Pull Compensation](./ActivePull/) | Custom — Nexteer logic on Vector-generated scaffold | This module corrects for vehicle pull issues by compensation for both long and short term torque offsets. |
| [Base Steering Assist](./Assist/) | Custom — Nexteer logic on Vector-generated scaffold | The Assist Function applies an appropriate level of motor torque based on handwheel torque and vehicle speed. |
| [Assist Firewall](./AssistFirewall/) | Custom — Nexteer logic on Vector-generated scaffold | This module limits the output from the Assist module according to safety requirements. |
| [Assist Sum and Limit (Current Mode)](./AstLmt_CM/) | Custom — Nexteer logic on Vector-generated scaffold | This module combines and limits the various assist command signals from EPS modules. |
| [Average Friction Learning](./AvgFricLrn/) | Custom — Nexteer logic on Vector-generated scaffold | This module estimates the gear friction changes from the baseline friction and provides compensation. |
| [Battery Voltage](./BatteryVoltage/) | Custom — Nexteer logic on Vector-generated scaffold | Battery Voltage configuration |
| [Battery Voltage Diagnostics](./BVDiag/) | Custom — Nexteer logic on Vector-generated scaffold | Functionality of Battery Voltage Diagnostics (`BVDiag`); no module-description header or MDD title was found,  |
| [Compliance Error](./ComplErr/) | Custom — Nexteer logic on Vector-generated scaffold | This function calculates the compliance error that can be used to compensate for stiffness in the torque path  |
| [Controlled Disable Shutdown](./CtrldDisShtdn/) | Custom — Nexteer logic on Vector-generated scaffold | The Controlled Disable Damping Shutdown method is used for torque sensor failures. |
| [Steering Damping](./Damping/) | Custom — Nexteer logic on Vector-generated scaffold | Damping function computes the Total damping Torque. |
| [Damping Firewall](./DampingFirewall/) | Custom — Nexteer logic on Vector-generated scaffold | Implementation of SF35 |
| [Diagnostics Manager](./DiagMgr/) | Custom — Nexteer in-house | Core Diagnostic Manager Functionality |
| [Electric Power Consumption Monitor](./ElePwr/) | Custom — Nexteer logic on Vector-generated scaffold | This module estimates the instantaneous electric power at the input of the control module and the supply curre |
| [End-of-Travel Actuator Management](./EOTActuatorMng/) | Custom — Nexteer logic on Vector-generated scaffold | The end of travel actuator management limit reduces the level of assist from the motor as the steering system  |
| [End-of-Travel Damping Firewall](./EtDmpFw/) | Custom — Nexteer logic on Vector-generated scaffold | End-of-Travel Damping Firewall — role as described by the module design documentation (see Documents). |
| [Fault Injection](./FltInjection/) | Custom — Nexteer logic on Vector-generated scaffold | This module manages the fault injection system. |
| [Frequency-Dependent Damping and Inertia Compensation](./FrqDepDmpnInrtCmp/) | Custom — Nexteer logic on Vector-generated scaffold | This MDD describes the methods to provide compensation that is dependent on filter of motor velocity which wil |
| [Global Signal Overwrite Detection](./Gsod/) | Custom — Nexteer logic on Vector-generated scaffold | Key system inputs including handwheel torque, motor position, motor and handwheel velocity are widely distribu |
| [High-Frequency Assist](./HighFreqAssist/) | Custom — Nexteer logic on Vector-generated scaffold | This module compensates for system inertia and road feedback. |
| [High-Load Stall Thermal Management](./HiLoadStall/) | Custom — Nexteer logic on Vector-generated scaffold | The High Load Stall Thermal Management algorithm protects the system from prolonged intervals of high assist t |
| [Hardware Power-Up Sequence](./HwPwUp/) | Custom — Nexteer logic on Vector-generated scaffold | This module controls the startup initialization sequence for several modules that would otherwise conflict wit |
| [Hysteresis Compensation](./HystComp/) | Custom — Nexteer logic on Vector-generated scaffold | Hysteresis Compensation — role as described by the module design documentation (see Documents). |
| [Limiter Conditioning](./LmtCod/) | Custom — Nexteer logic on Vector-generated scaffold | Limiter Conditioning — role as described by the module design documentation (see Documents). |
| [End-of-Travel Position Learning](./LrnEOT/) | Custom — Nexteer logic on Vector-generated scaffold | Functionality of End-of-Travel Position Learning (`LrnEOT`); no module-description header or MDD title was fou |
| [Motor Control (Current Mode)](./MtrCtrl_CM/) | Custom — Nexteer logic on Vector-generated scaffold | This module takes the cumulative motor position and determines the motor direction (using a previously saved s |
| [Motor Temperature Estimation](./MtrTempEst/) | Custom — Nexteer logic on Vector-generated scaffold | This module details out the estimation functions (first order lead lag filters) used to estimate the controlle |
| [Signal Polarity Assignment](./Polarity/) | Custom — Nexteer logic on Vector-generated scaffold | This module implements the polarity assignments for the EPS systems to allow for various configurations of inp |
| [Power Limit Function (Current Mode)](./PwrLmtFuncCr/) | Custom — Nexteer logic on Vector-generated scaffold | This module determines an appropriate limit for the system motor torque command based on reasonable output pow |
| [Return Torque Control](./Return/) | Custom — Nexteer logic on Vector-generated scaffold | This function uses the Absolute Hand Wheel position, Hand Wheel Torque, Hand Wheel Velocity and Vehicle Speed  |
| [Return Firewall](./ReturnFirewall/) | Custom — Nexteer logic on Vector-generated scaffold | This module limits the return command according to safety requirements. |
| [Signal Conditioning](./SgnlCond/) | Custom — Nexteer logic on Vector-generated scaffold | This function conditions a signal received from SER prior to its distribution to other functions. |
| [Stability Compensation](./StabilityComp/) | Custom — Nexteer logic on Vector-generated scaffold | This function provides in-vehicle stability of EPS behavior. |
| [States and Modes](./StaMd/) | Custom — Nexteer in-house | This module handles the EPS system state transitions and is used to determine the operating system state based |
| [State Output Control](./StOpCtrl/) | Custom — Nexteer logic on Vector-generated scaffold | This function performs the ramp up and ramp down of the Torque Command. |
| [Sine-Voltage Drive Diagnostics](./SVDiag/) | Custom — Nexteer logic on Vector-generated scaffold | This module compares the commanded duty cycle to each phase with the feedback from the NHET module. |
| [Torque Sweep Generator](./Sweep/) | Custom — Nexteer logic on Vector-generated scaffold | Header file for data communicated between Nexteer |
| [Thermal Duty Cycle](./ThrmDutyCycle/) | Custom — Nexteer logic on Vector-generated scaffold | This module computes a duty cycle limit based on system temperatures. |
| [Torque Reasonableness Diagnostics](./TqRsDg/) | Custom — Nexteer logic on Vector-generated scaffold | Functionality of Torque Reasonableness Diagnostics (`TqRsDg`); no module-description header or MDD title was f |
| [Tuning Select Authority](./TuningSelAuth/) | Custom — Nexteer logic on Vector-generated scaffold | This function broadcasts an authority to allow switching between calibration subsets while driving. |
| [Vehicle Dynamics](./VehDyn/) | Custom — Nexteer logic on Vector-generated scaffold | This module calculates HandWheel AutoCentering and determines the Vehicle Dynamics HandWheel Position and Vehi |
| [Vehicle Speed Limiting](./VehSpdLmt/) | Custom — Nexteer logic on Vector-generated scaffold | The Vehicle Speed Limiting Function determines a limited assist torque command value as a function of vehicle  |
| [XCP Measurement and Calibration Interface](./Xcp/) | Custom — Nexteer logic on Vector-generated scaffold | ApXcp Header File |
