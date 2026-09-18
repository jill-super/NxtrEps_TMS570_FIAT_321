---
title: "Gliwa T1 Timing Measurement documents"
description: "Word/PDF/text documents shipped with GliwaT1 (Gliwa T1 Timing Measurement) and their conversion status."
---

# Gliwa T1 Timing Measurement — documents

*Repository directory: `GliwaT1`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## GliwaT1_IntegrationManual.doc

- **Source:** `GliwaT1/doc/GliwaT1_IntegrationManual.doc`
- **Format:** `.doc` (~500 KiB)
- **Kind:** Integration manual
- **Status:** summary record — legacy binary source retained at `GliwaT1/doc/GliwaT1_IntegrationManual.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **GliwaT1_IntegrationManual.doc** integration manual describes how to integrate `GliwaT1` into the ECU project: configuration of the DaVinci/MICROSAR RTE, calibration constants, NVRAM blocks, scheduling of runnables and dependency on BSW services. Follow it when regenerating the ECU project configuration.
