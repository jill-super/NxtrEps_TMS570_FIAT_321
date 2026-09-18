---
title: "Limiter Conditioning documents"
description: "Word/PDF/text documents shipped with LmtCod (Limiter Conditioning) and their conversion status."
---

# Limiter Conditioning — documents

*Repository directory: `LmtCod`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## Limiter_Conditioning_MDD.doc

- **Source:** `LmtCod/doc/Limiter_Conditioning_MDD.doc`
- **Format:** `.doc` (~608 KiB)
- **Kind:** Module design document (MDD)
- **Status:** summary record — legacy binary source retained at `LmtCod/doc/Limiter_Conditioning_MDD.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **Limiter_Conditioning_MDD.doc** module design document specifies the `LmtCod` software component: requirements, interfaces/ports, internal behaviour, calibration and diagnostics. It is the normative reference for the implementation in `LmtCod/src/`; the module page lists the files it governs.

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `LmtCod/doc/QAC_Results/Ap_LmtCod.c.err` (~104 KiB)
- `LmtCod/doc/QAC_Results/Ap_LmtCod.c.met` (~845 KiB)

</details>
