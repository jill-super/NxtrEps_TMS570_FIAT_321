---
title: "Platform & safety"
description: "TMS570 target, ASIL D context, CAN/UDS and calibration interfaces."
---


# Platform & safety

- **Target:** TI TMS570 (Hercules, ARM Cortex-R4, lockstep) — startup, core/fault handling and microcontroller diagnostics live in TMS570 Startup (`TMS570_Startup`) and TMS570 Microcontroller Diagnostics (`TMS570_uDiag`) ([CDD](./../cdd/)).
- **Functional safety:** developed under ISO 26262 ASIL D processes — firewall monitors (Assist Firewall (`AssistFirewall`), Damping Firewall (`DampingFirewall`), Return Firewall (`ReturnFirewall`), End-of-Travel Damping Firewall (`EtDmpFw`)), reasonableness diagnostics (Torque Reasonableness Diagnostics (`TqRsDg`), Temporal Monitor (`TmprlMon`), Sine-Voltage Drive Diagnostics (`SVDiag`), Battery Voltage Diagnostics (`BVDiag`), Overvoltage Monitor (`OvrVoltMon`)), controlled shutdown (Controlled Disable Shutdown (`CtrldDisShtdn`), Shutdown Mechanisms (`ShtdnMech`)) and fault injection for validation (Fault Injection (`FltInjection`), in [ASW](./../asw/)).
- **Communication & diagnostics:** CAN stack from Vector MICROSAR (see the [MICROSAR stack reference](./../bsw/vector-microsar-stack/)), UDS via `Dcm`/`Dem` with the Diagnostics Manager (`DiagMgr`) abstraction and Common Manufacturing Services (`CMS_Common`).
- **Calibration & measurement:** XCP (XCP Measurement and Calibration Interface (`Xcp`) + Vector XCP BSW) and the Gliwa T1 timing setup (Gliwa T1 Timing Measurement (`GliwaT1`), in [Project & Integration](./../integration/)).
