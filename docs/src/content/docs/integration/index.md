---
title: "Project & Integration"
description: "ECU project (Vector MICROSAR configuration, RTE/BSW generation, linker setup), measurement tooling and static-analysis configuration."
---


# Project & Integration

ECU project (Vector MICROSAR configuration, RTE/BSW generation, linker setup), measurement tooling and static-analysis configuration.

This layer contains **3** module(s).

| Module | Origin | Purpose |
| --- | --- | --- |
| [Fiat 326/327 EPS TMS570 ECU Project](./Fiasa_326_327_EPS_TMS570/) | Mixed — Vector MICROSAR + Nexteer integration | ECU project for the Fiat 326/327 EPS on the TMS570: CCS build project, configured Vector MICROSAR BSW, DaVinci |
| [Gliwa T1 Timing Measurement](./GliwaT1/) | Third-party — Gliwa | Gliwa T1 timing-measurement integration: application interface and configuration (`T1_AppInterface`) linking t |
| [QA-C Static Analysis Configuration (MISRA)](./QAC/) | Tooling configuration | Static-analysis configuration for QA-C (analyser presets, profiles, per-module projects) plus the project MISR |
