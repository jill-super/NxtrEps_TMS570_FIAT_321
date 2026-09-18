---
title: "Flash EEPROM Emulation Driver (Texas Instruments) documents"
description: "Word/PDF/text documents shipped with Fee (Flash EEPROM Emulation Driver (Texas Instruments)) and their conversion status."
---

# Flash EEPROM Emulation Driver (Texas Instruments) — documents

*Repository directory: `Fee`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## AutoSAR FEE Parameter Configuration.pdf

- **Source:** `Fee/doc/AutoSAR FEE Parameter Configuration.pdf`
- **Format:** `.pdf` (~300 KiB)
- **Kind:** Parameter configuration guide
- **Status:** converted — text extracted from the binary (5363 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fee/doc/AutoSAR FEE Parameter Configuration.pdf` for those.

```text
AutoSAR FEE Parameter Configuration (Rev 1.8) 
 
 
 
 
Texas Instruments Incorporated 
 
 
 
 
 
 
 
AutoSAR FEE Parameter 
Configuration Document 
 
 
 
 

 
 AutoSAR FEE Parameter Configuration (Rev 1.8) 
 
 
 
 
Texas Instruments Incorporated 2 
 
ABSTRACT 
 
AutoSAR Flash EEPROM Emulation (AutoSAR FEE) driver utilizes Code Generation 
Tool to generate the configuration parameters required for EEPROM emulation. Code 
Generation Tool is used to configure parameters like which Flash Sectors to use, the 
number of Block s, Block Size etc. for EE PROM emulation . Code Generation Tool 
generates two files (Fee_cfg.h & Fee_cfg.c) depending on the configuration. 
 
This document describes the parameters used by Code Generation Tool to generate the 
AutoSAR FEE Configuration parameters. 
 
 AutoSAR FEE Parameter Configuration (Rev 1.8) 
 
 
 
 
Texas Instruments Incorporated 3 
 
Revision History 
 
Version Release 
Date 
Author Comment 
1.0 09/16/2012 Vishwanath 
Reddy 
Initial version 
1.1 10/10/2012 Vishwanath 
Reddy 
Add configuration parameter 
FEE_NUMBER_OF_VIRTUAL_SECTORS_EEP1 
1.2 11/20/2012 Vishwanath 
Reddy 
Remove FeeSetModeSupported 
1.3 06/11/2013 Vishwanath 
Reddy 
Add con
```
*…excerpt ends here (4163 further characters in the source).*

## AutoSAR FEE User Guide.pdf

- **Source:** `Fee/doc/AutoSAR FEE User Guide.pdf`
- **Format:** `.pdf` (~317 KiB)
- **Kind:** User guide
- **Status:** converted — text extracted from the binary (5961 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fee/doc/AutoSAR FEE User Guide.pdf` for those.

```text
AutoSAR FEE Driver 
 
 
 
 
 
 
 
 
 
 
 
 
Version 1.13 
 
Mar15, 2016 
 
Copyright  Texas Instruments Incorporated 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
User's Guide
 User Manual 
Read This First 
 
 
 2 
IMPORTANT NOTICE 
 
Texas Instruments and its subsidiaries (TI) reserve the right to make changes to their products or to 
discontinue any product or service without notice, and advise customers to obtain the latest version of 
relevant information to verify, before placing orders, that information being relied on is current and 
complete. All products are sold subject to the terms and conditions of sale supplied at the time of order 
acknowledgment, including those pertaining to warranty, patent infringement, and limitation of liability. 
TI warrants performance of its products to the specifications appl icable at the time of sale in 
accordance with TI’s standard warranty. Testing and other quality control techniques are utilized to the 
extent TI deems necessary to support this warranty. Specific testing of all parameters of each device is 
not necessarily performed, except those mandated by government requirements. 
Customers are responsible for their applications using TI
```
*…excerpt ends here (4761 further characters in the source).*

## Static-analysis outputs (32 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `Fee/doc/QAC_Results/Device_TMS570LS07.c.err` (~23 KiB)
- `Fee/doc/QAC_Results/Device_TMS570LS07.c.met` (~147 KiB)
- `Fee/doc/QAC_Results/Device_TMS570LS12.c.err` (~23 KiB)
- `Fee/doc/QAC_Results/Device_TMS570LS12.c.met` (~147 KiB)
- `Fee/doc/QAC_Results/fee.c.err` (~35 KiB)
- `Fee/doc/QAC_Results/fee.c.met` (~221 KiB)
- `Fee/doc/QAC_Results/ti_fee_Info.c.err` (~30 KiB)
- `Fee/doc/QAC_Results/ti_fee_Info.c.met` (~192 KiB)
- `Fee/doc/QAC_Results/ti_fee_cancel.c.err` (~30 KiB)
- `Fee/doc/QAC_Results/ti_fee_cancel.c.met` (~192 KiB)
- `Fee/doc/QAC_Results/ti_fee_eraseimmediateblock.c.err` (~30 KiB)
- `Fee/doc/QAC_Results/ti_fee_eraseimmediateblock.c.met` (~198 KiB)
- `Fee/doc/QAC_Results/ti_fee_format.c.err` (~30 KiB)
- `Fee/doc/QAC_Results/ti_fee_format.c.met` (~189 KiB)
- `Fee/doc/QAC_Results/ti_fee_ini.c.err` (~32 KiB)
- `Fee/doc/QAC_Results/ti_fee_ini.c.met` (~225 KiB)
- `Fee/doc/QAC_Results/ti_fee_invalidateblock.c.err` (~30 KiB)
- `Fee/doc/QAC_Results/ti_fee_invalidateblock.c.met` (~197 KiB)
- `Fee/doc/QAC_Results/ti_fee_main.c.err` (~33 KiB)
- `Fee/doc/QAC_Results/ti_fee_main.c.met` (~209 KiB)
- `Fee/doc/QAC_Results/ti_fee_read.c.err` (~31 KiB)
- `Fee/doc/QAC_Results/ti_fee_read.c.met` (~200 KiB)
- `Fee/doc/QAC_Results/ti_fee_readSync.c.err` (~30 KiB)
- `Fee/doc/QAC_Results/ti_fee_readSync.c.met` (~189 KiB)
- `Fee/doc/QAC_Results/ti_fee_shutdown.c.err` (~30 KiB)
- `Fee/doc/QAC_Results/ti_fee_shutdown.c.met` (~189 KiB)
- `Fee/doc/QAC_Results/ti_fee_util.c.err` (~41 KiB)
- `Fee/doc/QAC_Results/ti_fee_util.c.met` (~384 KiB)
- `Fee/doc/QAC_Results/ti_fee_writeAsync.c.err` (~30 KiB)
- `Fee/doc/QAC_Results/ti_fee_writeAsync.c.met` (~204 KiB)
- `Fee/doc/QAC_Results/ti_fee_writeSync.c.err` (~30 KiB)
- `Fee/doc/QAC_Results/ti_fee_writeSync.c.met` (~189 KiB)

</details>
