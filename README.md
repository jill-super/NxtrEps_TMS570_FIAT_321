# Electric Power Steering (EPS) System for Fiat 326/327

![License: MIT](https://img.shields.io/badge/license-MIT-green)
![Language: C](https://img.shields.io/badge/language-C-blue)
![Platform: TMS570](https://img.shields.io/badge/platform-TMS570_Hercules-orange)
![AUTOSAR: 3.1.4](https://img.shields.io/badge/AUTOSAR-3.1.4-lightgrey)
![Safety: ASIL D](https://img.shields.io/badge/safety-ASIL_D-red)
![Docs: Astro Starlight](https://img.shields.io/badge/docs-Astro_Starlight-purple)

Complete **Electric Power Steering (EPS)** system for the **Fiat 326/327** platform —
**TMS570** (Hercules) microcontroller, **AUTOSAR** software architecture,
**ISO 26262 ASIL D** processes, **CAN** communication and **UDS** diagnostics.

> **Documentation site:** the full layered reference (every module, origin badges,
> converted design documents) is generated from this repository with
> **Astro + Starlight**. Sources live in [`docs/`](docs/) — see
> [Documentation](#documentation) below.

## Table of contents

- [Features](#features)
- [Documentation](#documentation)
- [Repository structure](#repository-structure)
- [AUTOSAR layers and modules](#autosar-layers-and-modules)
- [Build instructions](#build-instructions)
- [Fiat 326/327 platform](#fiat-326327-platform)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Control:** precise power-assisted steering control, electric-motor power management.
- **Architecture:** AUTOSAR 3.1.4 software components (DaVinci/MICROSAR RTE), MCAL +
  Complex Device Drivers for the TMS570, Vector MICROSAR BSW stack.
- **Safety (ASIL D):** firewall monitors, reasonableness diagnostics, controlled shutdown,
  fault injection for validation.
- **Communication:** CAN stack (Vector), UDS diagnostics (Diagnostic Communication
  Manager / Diagnostic Event Manager via the Diagnostics Manager (`DiagMgr`)),
  XCP calibration/measurement, manufacturing services (`CMS_Common`).

## Documentation

The documentation site source is the **Astro 7 + Starlight** project in [`docs/`](docs/).
It organises all 71 modules by AUTOSAR layer, badges every module as
Vector-provided / in-house / third-party, and summarises the 260+ Word/PDF/text
documents shipped inside the module `doc/` folders.

| Page | What it covers |
| --- | --- |
| Home | Project overview, layer links, Vector-vs-custom summary |
| General → AUTOSAR overview | Layer model, membership rules, module anatomy |
| General → Vector vs. custom | Origin taxonomy, detection method, full module × origin table |
| General → Build system | CCS project, DaVinci/MICROSAR generation flow, rebuild sketch |
| General → Document inventory | Every prose artefact + conversion status |
| General → Platform & safety | TMS570 target, ASIL D context, CAN/UDS, XCP |
| ASW / CDD / BSW / Libraries / Integration | Layer indexes + one page per module (purpose, origin, API, dependencies, documents) |

<details>
<summary>Preview or build the docs site locally</summary>

```bash
cd docs
npm install
npm run dev      # local preview with live reload
npm run build    # static build into docs/dist/
```

The Pages URL (`site`/`base`) is derived automatically at build time from the
`GITHUB_REPOSITORY` environment variable or the git `origin` remote — no owner or
repository name is hardcoded, so forks work unchanged.

</details>

## Repository structure

```text
<Module>/                  # one folder per software component / driver / library
  autosar/                 # DaVinci model (*.dcf, *.arxml) — RTE software components
  src/ | include/          # implementation + public headers
  generate/                # *.tt RTE/BSW templates for the Vector generators
  tools/                   # Integrate.bat / RteGen.bat, QA-C projects
  doc/                     # MDD + integration manual (Word), QAC_Results/
  utp/                     # Tessy unit tests + contract/ RTE stubs (Vector-generated)
Fiasa_326_327_EPS_TMS570/  # ECU project: SwProject/ (CCS build, BSW, GenData*),
                           # HLDD/ (Vector Technical References), Tools/
docs/                      # Astro 7 + Starlight documentation site (this README's site)
LICENSE                    # MIT License
```

There are **no Makefiles/CMake files** — the build is the CCS ECU project plus
Vector generator batch files (details: *General → Build system* in the docs site).

## AUTOSAR layers and modules

Membership rule: `Ap_*` implementations → **ASW**; `Sa_*`/`Cd_*` and
direct-register drivers → **CDD**; memory stack → **BSW Services**; shared code →
**Libraries**; ECU project/tooling → **Integration**. Documented exceptions:
NVRAM Manager (`NvMMgr`) / NVRAM Proxy (`NvMProxy`) (`Cd_*` but memory services → BSW),
Enhanced PWM and NHET Driver (`ePWM`) / Sine-Voltage Drive Diagnostics (`SVDiag`) (mixed
prefixes, grouped by primary role). Names in parentheses are the repository directory
(short) names — used in paths, symbols and configuration files. Origin badges:
**Custom** = Nexteer in-house
(many files additionally carry a *Vector MICROSAR RTE Generator* banner — that is
only the generated RTE scaffold); **Vector** = MICROSAR BSW + DaVinci-generated
configuration; **TI/Gliwa** = silicon/tooling third parties.

<details>
<summary>Application Software (ASW) — 43 modules</summary>

| Module | Origin |
| --- | --- |
| Absolute Handwheel Position (Turns Counter, I²C, Sensorless Vehicle Dynamics) (`AbsHwPos_TcI2cVd`) | Custom (Vector scaffold) |
| Active Pull Compensation (`ActivePull`) | Custom (Vector scaffold) |
| Base Steering Assist (`Assist`) | Custom (Vector scaffold) |
| Assist Firewall (`AssistFirewall`) | Custom (Vector scaffold) |
| Assist Sum and Limit (Current Mode) (`AstLmt_CM`) | Custom (Vector scaffold) |
| Average Friction Learning (`AvgFricLrn`) | Custom (Vector scaffold) |
| Battery Voltage (`BatteryVoltage`) | Custom (Vector scaffold) |
| Battery Voltage Diagnostics (`BVDiag`) | Custom (Vector scaffold) |
| Compliance Error (`ComplErr`) | Custom (Vector scaffold) |
| Controlled Disable Shutdown (`CtrldDisShtdn`) | Custom (Vector scaffold) |
| Steering Damping (`Damping`) | Custom (Vector scaffold) |
| Damping Firewall (`DampingFirewall`) | Custom (Vector scaffold) |
| Diagnostics Manager (`DiagMgr`) | Custom |
| End-of-Travel Actuator Management (`EOTActuatorMng`) | Custom (Vector scaffold) |
| Electric Power Consumption Monitor (`ElePwr`) | Custom (Vector scaffold) |
| End-of-Travel Damping Firewall (`EtDmpFw`) | Custom (Vector scaffold) |
| Fault Injection (`FltInjection`) | Custom (Vector scaffold) |
| Frequency-Dependent Damping and Inertia Compensation (`FrqDepDmpnInrtCmp`) | Custom (Vector scaffold) |
| Global Signal Overwrite Detection (`Gsod`) | Custom (Vector scaffold) |
| High-Load Stall Thermal Management (`HiLoadStall`) | Custom (Vector scaffold) |
| High-Frequency Assist (`HighFreqAssist`) | Custom (Vector scaffold) |
| Hardware Power-Up Sequence (`HwPwUp`) | Custom (Vector scaffold) |
| Hysteresis Compensation (`HystComp`) | Custom (Vector scaffold) |
| Limiter Conditioning (`LmtCod`) | Custom (Vector scaffold) |
| End-of-Travel Position Learning (`LrnEOT`) | Custom (Vector scaffold) |
| Motor Control (Current Mode) (`MtrCtrl_CM`) | Custom (Vector scaffold) |
| Motor Temperature Estimation (`MtrTempEst`) | Custom (Vector scaffold) |
| Signal Polarity Assignment (`Polarity`) | Custom (Vector scaffold) |
| Power Limit Function (Current Mode) (`PwrLmtFuncCr`) | Custom (Vector scaffold) |
| Return Torque Control (`Return`) | Custom (Vector scaffold) |
| Return Firewall (`ReturnFirewall`) | Custom (Vector scaffold) |
| Signal Conditioning (`SgnlCond`) | Custom (Vector scaffold) |
| State Output Control (`StOpCtrl`) | Custom (Vector scaffold) |
| States and Modes (`StaMd`) | Custom |
| Stability Compensation (`StabilityComp`) | Custom (Vector scaffold) |
| Sine-Voltage Drive Diagnostics (`SVDiag`) | Custom (Vector scaffold) |
| Torque Sweep Generator (`Sweep`) | Custom (Vector scaffold) |
| Thermal Duty Cycle (`ThrmDutyCycle`) | Custom (Vector scaffold) |
| Torque Reasonableness Diagnostics (`TqRsDg`) | Custom (Vector scaffold) |
| Tuning Select Authority (`TuningSelAuth`) | Custom (Vector scaffold) |
| Vehicle Dynamics (`VehDyn`) | Custom (Vector scaffold) |
| Vehicle Speed Limiting (`VehSpdLmt`) | Custom (Vector scaffold) |
| XCP Measurement and Calibration Interface (`Xcp`) | Custom (Vector scaffold) |

</details>

<details>
<summary>Complex Device Drivers (CDD) — 18 modules</summary>

| Module | Origin |
| --- | --- |
| Analog-to-Digital Converter Driver (`Adc`) | Custom |
| Bulk Capacitor Precharge and Power Disconnect (`BkCpPc`) | Custom (Vector scaffold) |
| Common Motor Current Measurement (`CmMtrCurr`) | Custom (Vector scaffold) |
| Controller Temperature Monitor (`CtrlTemp`) | Custom (Vector scaffold) |
| Digital Column Position Sensor Interface (I²C) (`DigColPs`) | Custom (Vector scaffold) |
| Digital Handwheel Torque Sensing (SENT) (`DigHwTrqSENT`) | Custom (Vector scaffold) |
| Digital MSB Position Sensor Interface (`DigMSB`) | Custom (Vector scaffold) |
| Direct Memory Access Driver (`Dma`) | Custom |
| Enhanced PWM and NHET Driver (`ePWM`) | Custom (Vector scaffold) |
| I²C Driver (Nexteer) (`I2cNxtr`) | Custom |
| Motor Velocity Sensing (Digital) (`MtrVel_Digi`) | Custom (Vector scaffold) |
| Overvoltage Monitor (`OvrVoltMon`) | Custom (Vector scaffold) |
| Shutdown Mechanisms (`ShtdnMech`) | Custom (Vector scaffold) |
| SPI Driver (Nexteer) (`SpiNxt`) | Custom |
| Sine-Voltage Motor Driver (Current Mode) (`SVDrvr_CM`) | Custom |
| Temporal Monitor (`TmprlMon`) | Custom (Vector scaffold) |
| TMS570 Startup (System, Boot and Interrupt Vectors) (`TMS570_Startup`) | Custom |
| TMS570 Microcontroller Diagnostics (`TMS570_uDiag`) | Custom (Vector scaffold) |

</details>

<details>
<summary>BSW Services — 4 modules</summary>

| Module | Origin |
| --- | --- |
| Flash EEPROM Emulation Driver (Texas Instruments) (`Fee`) | Third-party TI (adapted) |
| Flash Memory Driver (TI F021 Flash API) (`Fls`) | Third-party TI (F021 Flash API) |
| NVRAM Manager (FEE Interface) (`NvMMgr`) | Custom |
| NVRAM Proxy (`NvMProxy`) | Custom |

The configured **Vector MICROSAR BSW stack** (CAN driver and interface, COM,
diagnostics, OS, … — `Can`, `Com`, `Dcm`, `Dem`, `Os`, …)
lives inside the ECU project — see the *Vector MICROSAR stack* reference (BSW section)
in the docs site.

</details>

<details>
<summary>Libraries & Common — 3 modules</summary>

| Module | Origin |
| --- | --- |
| Common Manufacturing Services (`CMS_Common`) | Custom |
| Nexteer Shared Library (Math, Filters, System Time) (`NxtrLib`) | Custom |
| Standard Platform Type Definitions (`StdDef`) | Custom (+ toolchain headers) |

</details>

<details>
<summary>Project & Integration — 3 modules</summary>

| Module | Origin |
| --- | --- |
| Fiat 326/327 EPS TMS570 ECU Project (`Fiasa_326_327_EPS_TMS570`) | Mixed (Vector MICROSAR + Nexteer integration) |
| Gliwa T1 Timing Measurement (`GliwaT1`) | Third-party Gliwa |
| QA-C Static Analysis Configuration (MISRA) (`QAC`) | Tooling configuration |

</details>

## Build instructions

This is an embedded CCS/Vector project (Windows toolchain), not a `make`/`cmake` build:

1. Clone this repository.
2. Install TI Code Composer Studio with Hercules (TMS570) support, plus licensed
   DaVinci Configurator + MICROSAR (Vector).
3. Regenerate RTE/BSW: run the module `RteGen`/`Integrate` steps so the ECU project
   `GenData*` folders are up to date (see *General → Build system* in the docs site).
4. Open the CCS project (`Fiasa_326_327_EPS_TMS570/SwProject/`, `Fiasa.ccxml`,
   `TMS570LS202x6SFlashLnk.cmd`) and build `SwProject` (`postbuild.bat` runs post-link steps).
5. Flash the image onto the TMS570 microcontroller.

## Fiat 326/327 platform

The **Fiat 326/327** platform is an electronic architecture for vehicles produced by
Fiat Chrysler Automobiles (now part of Stellantis). Examples of vehicles based on it:

1. **Fiat Tipo**: compact car with spacious interior and efficient engines.
2. **Fiat 500X**: compact crossover blending style and practicality.
3. **Jeep Renegade**: subcompact crossover SUV sharing the platform with the 500X.
4. **Fiat Doblo**: versatile MPV with ample cargo space.
5. **Fiat Fiorino**: compact urban-delivery van.

## Contributing

Contributions are welcome! Please submit a pull request. When touching ECU code,
keep the AUTOSAR layering (ASW/CDD/BSW) intact, update the module MDD/integration
manual where applicable, and reflect user-facing changes in [`docs/`](docs/).

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file.
Third-party deliveries retain their own terms: TI F021 Flash API / FEE driver
(`Fls/`, `Fee/` — see `Fls/doc/`), Vector MICROSAR/DaVinci (licensed, ECU-project
scoped), and Gliwa T1 (`GliwaT1/`).
