---
title: "AUTOSAR overview"
description: "How this repository maps to AUTOSAR layers and how modules were classified."
---


# AUTOSAR overview

The software follows the AUTOSAR 3.1.4 model (DaVinci/MICROSAR tooling, `autosar/*.arxml` + `*.dcf` per software component). Mapping used in this documentation:

| Documentation layer | AUTOSAR counterpart | Membership rule used here | Count |
| --- | --- | --- | --- |
| [Application Software](./../asw/) | Application SW-Cs | implementation files named `Ap_*` | 43 |
| [Complex Device Drivers](./../cdd/) | CDD / Sensor-Actuator SW-Cs / ECU-near HW drivers | `Sa_*` / `Cd_*` implementations, or direct-register drivers (`Adc`, `Dma`, `ePWM`, `SpiNxt`, `I2cNxtr`, …) | 18 |
| [BSW Services](./../bsw/) | Memory Services and related | `Fee`, `Fls`, `NvMMgr`, `NvMProxy` | 4 |
| [Libraries & Common](./../libs/) | Libraries / platform types | shared code, no RTE component | 3 |
| [Project & Integration](./../integration/) | ECU project, toolchain, QA | Vector BSW configuration, RTE/BSW generation, linker setup | 3 |

Known mixed cases (also noted on the affected module pages):

- Sine-Voltage Drive Diagnostics (`SVDiag`) mixes `Ap_*` and `Sa_*` sources → grouped under ASW by primary role.
- Enhanced PWM and NHET Driver (`ePWM`) mixes `Ap_*` and `Cd_*` sources → grouped under CDD (hardware-near).
- Diagnostics Manager (`DiagMgr`) is named `Ap_*` but behaves like a services layer (DEM/DTC abstraction); it stays in ASW by naming rule and is discussed in [Build system](./build-system/).
- NVRAM Manager (`NvMMgr`) / NVRAM Proxy (`NvMProxy`) are named `Cd_*` but implement memory services → grouped under BSW Services.

## Typical module anatomy

```text
<Module>/
  autosar/    DaVinci model: *.dcf, *.arxml (ComponentTypes, DataTypes, PortInterfaces)
  src/        implementation (*.c; Ap_*/Sa_*/Cd_* or driver sources)
  include/    public headers (when split from src)
  generate/   *.tt RTE/BSW templates consumed by the Vector generators
  tools/      Integrate.bat / RteGen.bat, QA-C projects
  doc/        MDD + integration manual (Word), QAC_Results/
  utp/        Tessy unit tests + contract/ RTE stubs (Vector-generated)
```

The RTE stubs under `utp/contract/` (`Rte*.h`) are Vector-generated test doubles of the ECU-project RTE; they are consumed for unit testing, not shipped on the ECU.
