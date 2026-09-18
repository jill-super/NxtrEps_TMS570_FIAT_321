---
title: "End-of-Travel Damping Firewall documents"
description: "Word/PDF/text documents shipped with EtDmpFw (End-of-Travel Damping Firewall) and their conversion status."
---

# End-of-Travel Damping Firewall — documents

*Repository directory: `EtDmpFw`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## EOTDampingFirewall_MDD.doc

- **Source:** `EtDmpFw/doc/EOTDampingFirewall_MDD.doc`
- **Format:** `.doc` (~632 KiB)
- **Kind:** Module design document (MDD)
- **Status:** summary record — legacy binary source retained at `EtDmpFw/doc/EOTDampingFirewall_MDD.doc`; convert with Word/Acrobat (or `pandoc`/`libreoffice`) for the full text.

The **EOTDampingFirewall_MDD.doc** module design document specifies the `EtDmpFw` software component: requirements, interfaces/ports, internal behaviour, calibration and diagnostics. It is the normative reference for the implementation in `EtDmpFw/src/`; the module page lists the files it governs.

## index_WithOutPS.pdf

- **Source:** `EtDmpFw/utp/Tessy/report/index_WithOutPS.pdf`
- **Format:** `.pdf` (~479 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5997 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `EtDmpFw/utp/Tessy/report/index_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-04, 17:31:38+0530
Project EtDmpFw
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 1
Successful: 1
Failed: 0
Not Executed: 0
Date: 2014-09-04
Time: 17:31:38+0530
Selected Project Items
Test Object "CBD_UnitTest/EtDmpFw/EtDmpFw_Per1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: Yes
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Statement Coverage, Branch Coverage, Decision Coverage, Modified Condition / 
Decision Coverage, Multiple Condition Coverage
Test Case Results for Ea
```
*…excerpt ends here (5297 further characters in the source).*

## index_WithOutPS_FLTINJ.pdf

- **Source:** `EtDmpFw/utp/Tessy/report/index_WithOutPS_FLTINJ.pdf`
- **Format:** `.pdf` (~512 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5997 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `EtDmpFw/utp/Tessy/report/index_WithOutPS_FLTINJ.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-04, 17:48:14+0530
Project EtDmpFw
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 1
Successful: 1
Failed: 0
Not Executed: 0
Date: 2014-09-04
Time: 17:48:14+0530
Selected Project Items
Test Object "CBD_UnitTest/EtDmpFw_FLTINJ/EtDmpFw_Per1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: Yes
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Statement Coverage, Branch Coverage, Decision Coverage, Modified Condition / 
Decision Coverage, Multiple Condition Coverage
Test Case Results
```
*…excerpt ends here (5297 further characters in the source).*

## index_WithPS.pdf

- **Source:** `EtDmpFw/utp/Tessy/report/index_WithPS.pdf`
- **Format:** `.pdf` (~479 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5997 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `EtDmpFw/utp/Tessy/report/index_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-04, 17:13:13+0530
Project EtDmpFw
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 1
Successful: 1
Failed: 0
Not Executed: 0
Date: 2014-09-04
Time: 17:13:13+0530
Selected Project Items
Test Object "CBD_UnitTest/EtDmpFw/EtDmpFw_Per1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: Yes
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Statement Coverage, Branch Coverage, Decision Coverage, Modified Condition / 
Decision Coverage, Multiple Condition Coverage
Test Case Results for Ea
```
*…excerpt ends here (5297 further characters in the source).*

## index_WithPS_FLTINJ.pdf

- **Source:** `EtDmpFw/utp/Tessy/report/index_WithPS_FLTINJ.pdf`
- **Format:** `.pdf` (~512 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5997 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `EtDmpFw/utp/Tessy/report/index_WithPS_FLTINJ.pdf` for those.

```text
TEST OVERVIEW REPORT 2014-09-04, 17:20:24+0530
Project EtDmpFw
© Report created by TESSY V3.1.7, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 1
Successful: 1
Failed: 0
Not Executed: 0
Date: 2014-09-04
Time: 17:20:24+0530
Selected Project Items
Test Object "CBD_UnitTest/EtDmpFw_FLTINJ/EtDmpFw_Per1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Batch Operation Settings
Check Interface: No
Generate Driver: Yes
Execute Test: Yes
Create New Test Run: No
Instrumentation: Test Object Only
Coverage: Statement Coverage, Branch Coverage, Decision Coverage, Modified Condition / 
Decision Coverage, Multiple Condition Coverage
Test Case Results
```
*…excerpt ends here (5297 further characters in the source).*

## Static-analysis outputs (2 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `EtDmpFw/doc/QAC_Results/Ap_EtDmpFw.c.err` (~102 KiB)
- `EtDmpFw/doc/QAC_Results/Ap_EtDmpFw.c.met` (~564 KiB)

</details>
