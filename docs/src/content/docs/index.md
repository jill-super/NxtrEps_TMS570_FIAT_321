---
title: "EPS AUTOSAR documentation"
description: "AUTOSAR-based Electric Power Steering (TMS570, Fiat 326/327): layered module docs, origins, build and documents."
---


# Electric Power Steering — AUTOSAR documentation

Complete reference for the **Electric Power Steering (EPS)** system for the **Fiat 326/327** platform: TMS570 (Hercules) microcontroller, AUTOSAR software architecture, ISO 26262 ASIL D processes, CAN communication and UDS diagnostics.

## Layers

| Layer | Contents |
| --- | --- |
| [Application Software (ASW)](./asw/) | RTE software components (`Ap_*`): steering functions, arbitration, diagnostics and mode logic. |
| [Complex Device Drivers (CDD)](./cdd/) | Hardware-near drivers and sensor/actuator components (`Sa_*`, `Cd_*`, direct-register drivers). |
| [Basic Software — Services](./bsw/) | Memory, NVRAM and platform services: TI FEE/Flash, Nexteer NvM wrappers. |
| [Libraries & Common](./libs/) | Shared libraries, platform types and diagnostic-service helpers used across modules. |
| [Project & Integration](./integration/) | ECU project (Vector MICROSAR configuration, RTE/BSW generation, linker setup), measurement tooling and static-analysis configuration. |

## Vector-provided vs. in-house code

Every module page carries an **origin badge** (Custom, Vector-provided, third-party, …). The short version:

- **Custom (Nexteer in-house)** — steering functions, drivers and glue written for this project. Many `Ap_*`/`Sa_*` files additionally carry a *Vector MICROSAR RTE Generator* banner: that is only the generated RTE scaffold; the control logic is in-house.
- **Vector-provided** — the MICROSAR basic-software stack and DaVinci-generated RTE/BSW configuration inside the ECU project (see [Project & Integration](./integration/) and [Vector vs. custom](./general/vector-vs-custom/)).
- **Third-party silicon/tooling** — TI F021 Flash API + FEE driver, Gliwa T1 measurement stack.

Read [Vector vs. custom](./general/vector-vs-custom/) for the full taxonomy and detection method, and [Build system](./general/build-system/) for how the pieces are generated and linked.

## Source documents

The repository ships **263** prose documentation artefacts (142 Word, 117 PDF, 4 text) plus **514** QA-C analyser outputs. Each module page links to its documents page; [Document inventory](./general/doc-inventory/) lists every file and its conversion status.
