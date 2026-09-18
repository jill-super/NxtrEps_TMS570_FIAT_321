---
title: "Fiat 326/327 EPS TMS570 ECU Project documents"
description: "Word/PDF/text documents shipped with Fiasa_326_327_EPS_TMS570 (Fiat 326/327 EPS TMS570 ECU Project) and their conversion status."
---

# Fiat 326/327 EPS TMS570 ECU Project — documents

*Repository directory: `Fiasa_326_327_EPS_TMS570`*

> **Conversion note:** Word (`.docx`) and PDF sources below were converted to text (layout, tables, figures and images are omitted; the binary originals remain in the repository). Legacy `.doc` binaries cannot be converted with the available tooling and are recorded as structured summaries. Plain-text (`.txt`) sources are embedded in full; QA-C analyser outputs are tabulated, not embedded.

## TechnicalReference_ASR_IpduM.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_ASR_IpduM.pdf`
- **Format:** `.pdf` (~531 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5965 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_ASR_IpduM.pdf` for those.

```text
MICROSAR I-PDU Multiplexer 
Technical Reference 
 
 
Version 1.2.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Safiulla Shakir 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR I-PDU Multiplexer 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Safiulla Shakir 26.03.2009 1.0 Initial version 
Safiulla Shakir 28.06.2010 1.1.0 Updated to support IPDUM 
system description 3.1.4 
format 
Safiulla Shakir 02.02.2011 1.2.0 ESCAN00046128 
Table 1-1 History of the document 
1.2 Reference Documents 
No. Title Version 
[1] AUTOSAR_SWS_IPDUM.pdf 1.2.1 
[2] AUTOSAR_SWS_IPDUM.doc 1.3.0 
[3] AUTOSAR_BasicSoftwareModules.pdf 1.0.0 
[4] AUTOSAR_SWS_IPDUM ASR3.2.pdf 1.3.0 
Table 1-2 Reference documents 
 
 
 
Please note 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector’s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire. 
 
 
Info 
[2] is a draft version of AUTOSAR release 4.0. 
 
©2011, Vector Informatik GmbH Version: 1.2.0 
based on template version 3.
```
*…excerpt ends here (4765 further characters in the source).*

## TechnicalReference_Asr_BswM.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_BswM.pdf`
- **Format:** `.pdf` (~1708 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5956 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_BswM.pdf` for those.

```text
MICROSAR BswM 
Technical Reference 
 
 
Version 1.6.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Daniel Hof, Thomas Kuhl, Leticia Garcia Herrera 
Status Released 
 
 
 
 
 
 
 
Technical Reference MICROSAR BswM 
2014, Vector Informatik GmbH Version: 1.6.0 
based on template version 4.8.0 
2 / 124 
Document Information 
History 
Author Date Version Remarks 
Daniel Hof 2011-01-14 1.0 Creation 
Daniel Hof 2011-05-27 1.1 ESCAN00051215: Added description for 
Nm_Fiat and some minor modifications 
Daniel Hof 2011-08-03 1.2 > Added description of further Det 
checks 
> Added descriptions for automatic 
configuration of recommended Use 
Cases 
> Added description of multiple 
identities configuration 
> Added Passive Mode description 
> Added Partial Networks description 
Thomas Kuhl 2011-11-03 1.2.1 > ESCAN00054154 
Thomas Kuhl 2011-12-06 1.2.2 > ESCAN00055325 
Thomas Kuhl 2012-01-10 1.3.0 > Add function description 
BswM_Dcm_ApplicationUpdated 
> Update Module Configuration 
description for Dcm service 
“Application Updated” 
Thomas Kuhl 2012-05-07 1.4.0 > Update Template 
> Add chapter 5.6.1.2 Require Ports 
> Add chapter 6.2.4 Timer 
Configuration 
> Extend chapter 6.2.5.2.2 Adding 
Actions to an
```
*…excerpt ends here (4756 further characters in the source).*

## TechnicalReference_Asr_CanIf.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanIf.pdf`
- **Format:** `.pdf` (~523 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5956 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanIf.pdf` for those.

```text
CAN Interface 
Technical Reference 
 
 
Version 2.10.01 
 
 
 
 
 
 
 
 
 
 
Authors Thomas Arnold, Rüdiger Naas, Eugen Stripling 
Versions: 2.10.01 
Status: Released 
 
 
 
 
 
Technical Reference CAN Interface 
©2011, Vector Informatik GmbH Version: 2.10.01 
based on template version 2.10.0 
2/ 6 2
1 Document Information 
1.1 History 
Author Date Version Remarks 
Thomas Arnold 2006-06-22 1.0 Initial version 
Thomas Arnold 2006-07-05 1.1 Minor corrections (Review) 
Add additional DET error codes 
Thomas Arnold 2006-07-05 1.2 Add justification for possible 
compiler warning 
Thomas Arnold 2006-10-30 1.3 Add additional features (TxFullCAN, 
TxPolling, …), 
Add GENy configuration chapter. 
Hartmut Hörner 2007-01-04 1.4 Added information about supported 
AUTOSAR version 
Thomas Arnold 2007-01-19 1.5 Add additional features (BusOff 
polling, Post build configuration). 
Changes in GENy configuration 
chapter. 
Thomas Arnold 2007-06-04 1.6 Adapt to AUTOSAR 2.1 
Thomas Arnold 2007-07-20 1.7 Switch to new template / 
modifications for Autosar 2.1 
Thomas Arnold 2008-03-03 1.8 Add Extended ID support 
Thomas Arnold 2008-03-10 2.0 Adapt to AUTOSAR 3 
Thomas Arnold 2008-05-16 2.1 Changes due
```
*…excerpt ends here (4756 further characters in the source).*

## TechnicalReference_Asr_CanNm.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanNm.pdf`
- **Format:** `.pdf` (~1112 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5967 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanNm.pdf` for those.

```text
MICROSAR CAN Network Management 
Technical Reference 
 
CAN NM 
 
 
 
 
 
 
 
 
 
 
 
 
Authors Markus Drescher 
Version 4.18.00 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR CAN Network Management 
2013, Vector Informatik GmbH Version: 4.18.00 
based on template version 3.4 
2 / 99 
Document Information 
History 
Author Date Version Remarks 
Oliver Hornung 2007-12-10 4.0.0 ESCAN00023633: Update Documentation 
for AUTOSAR Release 3 
Oliver Hornung 2008-02-01 4.1.0 Added Coordination Extension; Updated 
configuration. 
Oliver Hornung 2008-03-11 4.2.0 ESCAN00025282: Configuration changes 
Oliver Hornung 2008-04-02 4.2.1 Corrected Coordination Extension 
Oliver Hornung 2008-04-21 4.3.0 ESCAN00025499: Renamed Technical 
Reference 
Oliver Hornung 2008-05-02 4.3.1 Corrected Memory Mapping 
Oliver Hornung 2008-11-28 4.4.0 ESCAN00031692: Adapted Configuration 
and API 
Oliver Hornung 2009-03-31 4.5.0 ESCAN00034277: Re-structured document; 
added chapter with service functions that 
are used by CAN NM. 
Oliver Hornung 2009-07-31 4.06.00 ESCAN00036641: Documented changed 
behavior when requesting and releasing bus 
communication in state Bus Sleep. 
ESCAN00036642: Documented Multi
```
*…excerpt ends here (4767 further characters in the source).*

## TechnicalReference_Asr_CanSM.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanSM.pdf`
- **Format:** `.pdf` (~1038 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5958 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanSM.pdf` for those.

```text
MICROSAR CAN State Manager 
Technical Reference 
 
 
Version 1.16 
 
 
 
 
 
 
 
 
 
 
 
 
 
Authors Mark A. Fingerle 
Status Released 
 
Technical Reference MICROSAR CAN State Manager 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Mark A. Fingerle 2008-02-04 1.0 ASR 3.0 beta release 
Mark A. Fingerle 2008-02-27 1.1 Switch to new template 
Mark A. Fingerle 2008-03-31 1.2 ESCAN00025504 Rename Technical Reference to 
MSR Short Name 
ESCAN00025710 Adapt initialization. 
ESCAN00025711 Adapt Chapter Configuration 
GENy to ASR names 
Mark A. Fingerle 2008-05-06 1.3 ESCAN00025892 Simplify the set controller mode 
algorithm of the CanSM 
ESCAN00026001 Extend error handling to the case 
a transition fails and the mode request changes 
before recovering of the transition. 
Mark A. Fingerle 2008-07-18 1.4 Allowed timer values 
IPDU via drop down list 
critical section kinds 
Mark A. Fingerle 2008-10-08 1.5 New feature/API ECU passive mode 
CAN bus specific bus-off configuration parameter 
Mark A. Fingerle 2008-10-28 1.6 State machine start/entry point 
Additional explanation of passive mode 
Additional explanation of error counter 
Figure 4-1 updated 
GENy screen shots upd
```
*…excerpt ends here (4758 further characters in the source).*

## TechnicalReference_Asr_CanTp.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanTp.pdf`
- **Format:** `.pdf` (~592 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5945 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanTp.pdf` for those.

```text
MICROSAR CAN Transport Layer 
Technical Reference 
 
 
 
Version 1.18.01 
 
 
 
 
 
 
 
 
 
 
 
Authors Peter Herrmann 
Status Released 
 
 
 
 
Technical Reference MICROSAR CAN Transport Layer 
©2011, Vector Informatik GmbH Version: 1.18.01 
based on template version 3.9 
2/ 7 3
Document Information 
History 
Author Date Version Remarks 
Peter Herrmann 2006-12-07 1.0 Initial version 
Peter Herrmann 2007-06-19 1.3 Update to AUTOSAR Release 2.1.0 
Peter Herrmann 2008-01-18 1.4 Added database attributes 
Peter Herrmann 2008-01-22 1.5 Added pre-compile macros for Tx 
Confirmation and Rx Indication callbacks 
Peter Herrmann 2008-04-07 1.6 Adaptation to MICROSAR document 
template. 
Peter Herrmann 2008-07-31 1.7 Added description for optimizations: 
- dynamic channel assignment 
(DYN_CHANNEL_ASSIGNMENT), 
- single connection 
(SINGLE_CONN_OPTIMIZED) 
- single connection pre-compile 
(SINGLE_CONN_NOPB_OPTIMIZED) 
- addressing types 
(STANDARD_ADDRESSING, 
EXTENDED_ADDRESSING) 
- partial buffer provision 
(RX/TX_FULL_BUFFER_PROVISION) 
Peter Herrmann 2008-09-16 1.8 Burst transmission 
Peter Herrmann 2008-10-30 1.9 Version number updated 
Peter Herrmann 2008-11-26 1.10 Single connection op
```
*…excerpt ends here (4745 further characters in the source).*

## TechnicalReference_Asr_CanTrcv_30_GenericDio.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanTrcv_30_GenericDio.pdf`
- **Format:** `.pdf` (~684 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5922 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanTrcv_30_GenericDio.pdf` for those.

```text
MICROSAR CAN Transceiver Driver 
Technical Reference 
 
Generic 
Version 3.02.00 
 
 
 
 
 
 
 
 
 
Authors Matthias Fleischmann, Senol Cendere, Mihai Olariu, 
Timo Vanoni 
Status Released 
 
Technical Reference MICROSAR CAN Transceiver Driver 
2013, Vector Informatik GmbH Version: 3.02.00 
based on template version 3.1 
2 / 51 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Matthias Fleischmann 2008-04-21 1.00 Creation 
Senol Cendere 2008-06-10 1.01 Rework file names 
Rework tool description 
Mihai Olariu 2008-07-10 1.02 Rename the placeholders 
Mihai Olariu 2008-10-13 1.03 Minor changes in the GENy 
GUI 
Mihai Olariu 2008-12-15 1.04 Add support for the platforms 
which cannot wakeup by CAN 
bus activity 
Matthias Fleischmann 2009-07-01 1.05 Updated description for ICU 
notification function and 
GENy configuration. 
Added description for 
BSWMD file configuration. 
Timo Vanoni 2009-11-12 1.06 Added API 
CanTrcv_30_<Your_Trcv>_W
ait() 
Filenames were renamed to 
match BSW00347. 
Change of initialization flow. 
Timo Vanoni 2010-05-06 1.06.1 Fixed example in chapter 4.5 
Timo Vanoni 2011-01-26 1.07.00 Added support for Identity 
Manager Configurations 
Timo Vanon
```
*…excerpt ends here (4722 further characters in the source).*

## TechnicalReference_Asr_CanXcp.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanXcp.pdf`
- **Format:** `.pdf` (~237 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5969 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CanXcp.pdf` for those.

```text
XCP on CAN 
Technical Reference 
 
XCP on CAN Transport Layer for MICROSAR CanIf 
 
 
Version 1.06.00 
 
 
 
 
 
 
 
 
 
 
Authors: Frank Triem, Sven Hesselmann, Andreas 
Herkommer 
Version: 1.06.00 
Status: released (in preparation/completed/inspected/released) 
 
 
 
 
Technical Reference XCP on CAN Transport Layer for MICROSAR CanIf 
 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Frank Triem 2007-01-26 1.00.00 ESCAN00017890: Creation of Cp_XcpOnCanAsr 
based on Cp_XcpOnCan 
Sven 
Hesselmann 
2008-08-05 1.01.00 Adaptations to AUTOSAR R3 
Mario Kunz 2009-12-17 1.02.00 Support of a2l export. 
Andreas 
Herkommer 
2010-01-14 1.03.00 ESCAN00040120: Support MultiChannel 
Removed Section 3.3 
Andreas 
Herkommer 
2010-03-30 1.04.00 ESCAN00041935: Add feature to disable 
XcpOnCanAsr in serial production ECUs 
ESCAN00043225: Missing limitation for Multiple 
Identity with several CAN channels 
Andreas 
Herkommer 
2011-01-04 1.05.00 ESCAN00046305: AR3-297 AR3-894: Support 
PduInfoType instead of the DataPtr 
Andreas 
Herkommer 
2011-03-22 1.06.00 ESCAN00049434: Support Monitoring Hooks for 
AUTOSAR 4 
 
1.2 Reference Documents 
Index Document 
[1] XCP -Part 1 – Overview,
```
*…excerpt ends here (4769 further characters in the source).*

## TechnicalReference_Asr_CddFiat.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CddFiat.pdf`
- **Format:** `.pdf` (~869 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5955 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_CddFiat.pdf` for those.

```text
CddFiat 
Technical Reference 
 
Complex Device Driver 
Version 1.06.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Jochen Vorreiter 
Status Released 
 
 
 
 
 
Technical Reference CddFiat 
2013, Vector Informatik GmbH Version: 1.06.00 
based on template version 4.6 
2 / 38 
Document Information 
History 
Author Date Version Remarks 
virlg 2010-10-06 1.00.00 First Version 
virlg 2010-12-23 1.01.00 Adding content for Class B ECU features 
virlg 2011-03-07 1.02.00 Changing the interface for the used IPDU 
callouts 
virlg 2011-05-18 1.02.01 Chapter 6.3 added to describe additional 
unhandled signals 
virlg 2011-08-30 1.03.00 Class C supports EOL. Integration chapter 
updated 
visvjn 2012-11-15 1.04.00 Adding APIs for support of Class C with 
Wakeup 
visvjn 2013-03-12 1.05.00 Adding support for Multichannel ECUs 
visvjn 2013-10-15 1.06.00 ESCAN00070746: Adding API 
CddFiat_StatusC_MessageIndication 
ESCAN00069050: Adding support for 
OSEK_NM 
ESCAN00069060: Adding description 
about configuration of Multiple Ecu 
Reference Documents 
No. Source Title Version 
[1] AUTOSAR AUTOSAR_SWS_DET.pdf V2.2.1 
[2] AUTOSAR AUTOSAR_BasicSoftwareModules.pdf V1.3.0 
[3] Vector AN-ISC-8-1124 FGA Class C Nm in MICRO
```
*…excerpt ends here (4755 further characters in the source).*

## TechnicalReference_Asr_Com.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Com.pdf`
- **Format:** `.pdf` (~3140 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5959 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Com.pdf` for those.

```text
MICROSAR COM 
Technical Reference 
 
 
Version 2.11.01 
 
 
 
 
 
 
 
 
 
 
 
Authors Gunnar Meiss, Hartmut Hörner, Klaus Emmert, Hannes 
Haas, Michael Bissinger, Dominik Biber 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR COM 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Gunnar Meiss 2006-07-31 0.1 Creation 
Hartmut Hörner 2006-09-13 0.2 Update to new template version 
Klaus Emmert 2006-09-25 0.3 New Illustrations 
Hartmut Hörner 2006-10-13 0.4 Post build process figure updated, several minor 
changes based on review comments 
Hartmut Hörner 2006-10-24 0.5 Added configuration chapter and list of DET error 
codes. 
Hartmut Hörner 2006-11-06 1.0 Minor changes based on review comments. 
Gunnar Meiss 2007-01-08 1.1 ESCAN00018727, 
ESCAN00018724, 
ESCAN00018738, 
ESCAN00018721, 
ESCAN00018723 
Gunnar Meiss 2007-03-13 1.2 ESCAN00019913 
Hannes Haas 2007-04-26 1.2 ESCAN00019913: Added Signal Gateway 
Update to new template 
General rework 
Gunnar Meiss 2007-08-01 1.2 ESCAN00021344: Update EcuC Description 
Removed error message list 
Removed COM_IPDU_DIRECTION , 
COM_NETWORK_SIGNAL_DIRECTION 
Updated EcuC attribute names 
Updated EcuC Import/Export 
Update
```
*…excerpt ends here (4759 further characters in the source).*

## TechnicalReference_Asr_ComM.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_ComM.pdf`
- **Format:** `.pdf` (~486 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5941 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_ComM.pdf` for those.

```text
MICROSAR Communication Manager 
Technical Reference 
 
 
Version 3.14 
 
 
 
 
 
 
 
 
 
 
 
Authors Thomas Petrus 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR Communication Manager 
©2011, Vector Informatik GmbH Version: 3.14 
based on template version 3.1 
2/ 6 5
1 Document Information 
1.1 History 
Author Date Version Remarks 
Thomas Petrus 2008-02-01 3.0 Complete rework and 
adaptation to new template 
Thomas Petrus 2008-02-20 3.1  correct 
ComM_MainFunction() 
description 
 correct and advance ComM 
service port description 
 advance configuration setting 
description 
Thomas Petrus 2008-03-20 3.2  Update Compiler Abstraction 
and Memory Mapping 
Thomas Petrus 2008-03-30 3.3  add description for DEM 
support 
 update file structure 
 remove callback decriptions 
for 
ComM_LinSm_ModeIndicatio
n, 
ComM_CanSm_ModeIndicati
on and 
ComM_FrSm_ModeIndicatio
n 
 add callback description for 
ComM_BusSM_ModeIndicati
on 
 update configuration chapter 
Thomas Petrus 2008-05-08 3.4  update include structure 
 update chapter 5.1.2 
Dynamic Files 
 Add chapter 4.4.2, 4.4.3, 5.4 
and 5.5 
 update configuration 
description 
Thomas Kuhl 2008-08-22 3.5  Update functio
```
*…excerpt ends here (4741 further characters in the source).*

## TechnicalReference_Asr_Crc.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Crc.pdf`
- **Format:** `.pdf` (~298 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5962 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Crc.pdf` for those.

```text
MICROSAR CRC 
Technical Reference 
 
 
Version 4.00.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Claudia Mausz 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR CRC 
©2008, Vector Informatik GmbH Version: 4.00.00 
based on template version 3.2 
2/ 2 4
1 Document Information 
1.1 History 
Author Date Version Remarks 
Tobias Schmid 13-12-2006 1.0 Initial Version 
Tobias Schmid 21-01-2008 3.00.00 Update to ASR 2.1 
Changed versioning to new 
notation 
Claudia Mausz 19-05-2008 4.00.00 Update to ASR3.0.0 
Add Crc8 calculation 
Table 1-1 History of the document 
1.2 Reference Documents 
No. Title Version 
[1] AUTOSAR_SWS_CRC_Routines.pdf V3.0 Rev 
0002 
[2] AUTOSAR_BasicSoftwareModules.pdf V1.2.0 
Table 1-2 Reference documents 
 
1.1 Scope of the Document 
This technical reference describes the general use of the CRC driver basis software. There 
are no aspects which are controller specific. 
 
 
Please note 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector’s release of the programs delivered to your 
company is expressly restricted to the co
```
*…excerpt ends here (4762 further characters in the source).*

## TechnicalReference_Asr_Dcm.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Dcm.pdf`
- **Format:** `.pdf` (~3108 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5940 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Dcm.pdf` for those.

```text
MICROSAR DCM 
Technical Reference 
 
Vector 
Version 3.26.02 
 
 
 
 
 
 
 
 
 
 
 
Authors Mishel Shishmanyan, Jochen Breunich, Katrin Thurow 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR DCM 
2012, Vector Informatik GmbH Version: 3.26.02 
based on template version 3.1 
2 / 163 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Mishel Shishmanyan 2008-04-20 1.0 Reworks based on the new document 
template. 
Mishel Shishmanyan 2008-06-13 1.1 Extensions to DCM 3.03.00 
Removed unused chapters and sections. 
Modified: 
5.10.3 Configuration Aspects 
Mishel Shishmanyan 2008-07-18 1.2 Minor editorial changes. 
Added: 
6 Additional features beyond AUTOSAR 
DCM 3.0 
Mishel Shishmanyan 2008-08-20 3.4 Modified: 
Version jump to unify the different DCM 
generation documentations. 
8.5.1.2.11, 8.5.1.2.12, 8.5.1.2.13, 8.5.1.2.14 
– port interface change for service $2F. 
9.2.2 General DCM options 
 
 
Mishel Shishmanyan 2008-09-01 3.5 Modified: 
5.18.1 Functionality 
Table 8-23 Require Ports on BSW module 
side 
 
Added: 
5.18.1.1 Difference between single and 
multiple UUDT message transmission 
Mishel Shishmanyan 2008-10-08 3.6 Modified: 
5.16.2 Implementation Limit
```
*…excerpt ends here (4740 further characters in the source).*

## TechnicalReference_Asr_Dem.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Dem.pdf`
- **Format:** `.pdf` (~1437 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5965 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Dem.pdf` for those.

```text
MICROSAR Diagnostic Event Manager 
(DEM) 
Technical Reference 
 
Vector 
Version 2.2.0 
 
 
 
 
 
 
 
 
 
 
 
Authors P. Speidel, A. Ditte, S. Hübner 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR Diagnostic Event Manager (DEM) 
1 Document Information 
1.1 History 
Author Date Version Remarks 
P. Stöhr 2008-04-08 1.0 Created for OEM “Vector” base of 
TechnicalReference_DEM_<OEM>.doc 
P . Stöhr 2008-06-18 1.0.1 Updated to AUTOSAR Release 3 
P . Stöhr 2008-06-19 1.0.2 Added reference [8] 
P . Stöhr 2008-06-27 1.0.3 Modified description of configuration 
P . Stöhr 2009-01-08 2.0.10 Modified include structure, added chapter NvRAM 
Demand, added FreezeFrame descriptions, updated 
description of configuration, added description of 
scheduling DEM and DCM 
P . Stöhr 2009-02-16 2.0.13 Added internal OccurrenceCounter implementation 
A. Ditte 2009-04-14 2.0.14 Added description for event de-bouncing 
Added DEM_E_INV_TIMER_SLOT_VAL in chapter 4.6.1 
S. Hübner 2009-08-21 2.1.2 Update R7, DEM 2.08.00 
Added Variant Handling (Single Identity/VSG mode) 
B. Freiberger 2009-11-11 2.1.3 Add detailed description of AUTOSAR APIs 
P . Speidel 2010-03-03 2.1.4 Add information to “post-build s
```
*…excerpt ends here (4765 further characters in the source).*

## TechnicalReference_Asr_Det.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Det.pdf`
- **Format:** `.pdf` (~461 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5970 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Det.pdf` for those.

```text
MICROSAR DET 
Technical Reference 
 
 
 
 
Version 1.3 
 
 
 
 
 
 
 
 
Authors Hartmut Hörner 
Version: 1.3 
Status: Released 
 
 
 
Technical Reference MICROSAR DET 
©2008, Vector Informatik GmbH Version: 1.3 
based on template version 2.0 
2/ 2 5
1 Document Information 
1.1 History 
Author Date Version Remarks 
Hartmut Hörner 2007-11-29 1.0 Initial version 
Hartmut Hörner 2008-01-03 1.1 Update to AUTOSAR 3.0 
Hartmut Hörner 2008-04-14 1.2 Naming changed to 
AUTOSAR short name, 
screen shots updated. 
(ESCAN00025687) 
Hartmut Hörner 2008-09-16 1.3 Added DET extension 
mechanism based on callout 
(4.7, 6.3.1). 
Added chapter 5.3. 
Table 1-1 History of the Document 
1.2 Reference Documents 
Index Document 
[1] AUTOSAR_SWS_DET.pdf, Version 2.2.0 
 
Table 1-2 Referenced documents 
 
 
 
 
Please note 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire. 
Technical Reference MICROSAR DET 
©2008, Vector
```
*…excerpt ends here (4770 further characters in the source).*

## TechnicalReference_Asr_EcuM.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_EcuM.pdf`
- **Format:** `.pdf` (~870 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5950 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_EcuM.pdf` for those.

```text
MICROSAR ECUM 
Technical Reference 
 
 
Version 2.07.02 
 
 
 
 
 
 
 
 
 
 
 
Authors Christian Marchl, Bethina Mausz 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR ECUM 
©2011, Vector Informatik GmbH Version: 2.07.02 
based on template version 3.1 
2/ 1 1 7
1 Document Information 
1.1 History 
Author Date Version Remarks 
Christian Marchl 2006-10-12 0.9 Initial setup 
Christian Marchl 2006-12-12 1.0 Rework of review findings, 
first release 
Christian Marchl 2007-07-30 1.1 Update chapter for AUTOSAR 
2.1 release 
Christian Marchl 2007-09-26 1.2 Description of EcuM_Init() 
function corrected 
Christian Marchl 2008-04-03 1.03.00 Added AUTOSAR 3 changes. 
Christian Marchl 2008-05-07 1.04.00 File renamed according to 
new standard name. 
Christian Marchl, Heike Bischof 2008-05-07 2.00.00 Conversion to MICROSAR 
Technical Reference. 
Christian Marchl 2008-07-23 2.00.01 ESCAN00028261: Added TTII 
in abbreviation table. 
Christian Marchl 2008-10-22 2.00.02 Added description for 
PreCompile implementation 
variant. 
Christian Marchl 2008-12-08 2.01.00 Added description for 
currentMode port, 
Solved ESCAN00031271, 
Added description new callout 
function for selection the boot
```
*…excerpt ends here (4750 further characters in the source).*

## TechnicalReference_Asr_FiM.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_FiM.pdf`
- **Format:** `.pdf` (~416 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5958 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_FiM.pdf` for those.

```text
MICROSAR FiM 
Technical Reference 
 
Version 2.1.4 
 
 
 
 
 
 
 
 
 
 
 
Authors Joachim Kalmbach, Katrin Thurow 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR FiM 
©2011, Vector Informatik GmbH Version: 2.1.4 
based on template version 3.2 
2/ 2 9
1 Document Information 
1.1 History 
Author Date Version Remarks 
Joachim Kalmbach 2007-01-03 1.00.00 Initial version 
Joachim Kalmbach 2007-08-21 1.01.00 Updated for AUTOSAR 2.1 
Katrin Thurow 2007-10-10 1.02.00 Updated supported features 
and known issues 
Katrin Thurow 2008-06-05 2.00.00 Updated for AUTOSAR 3 
Katrin Thurow 2008-07-02 2.01.00 Change of error table 
Katrin Thurow 2009-07-22 2.01.01 Modified not supported 
feature table 
Katrin Thurow 2010-01-17 2.01.02 Small corrections 
Modified not supported 
feature table 
Katrin Thurow 2010-11-30 2.01.03 Added chapter 4.4 Critical 
Sections 
Katrin Thurow 2011-12-08 2.01.04 Changed chapter 4.4 Critical 
Sections 
Table 1-1 History of the document 
1.2 Reference Documents 
No. Title Version 
[1] AUTOSAR_SWS_FIM.pdf V1.2.0 
[2] AUTOSAR_BasicSoftwareModules.pdf V1.0.0 
Table 1-2 Reference documents 
 
 
 
 
 
 
 
 
 
Technical Reference MICROSAR FiM 
©2011, Vector Informati
```
*…excerpt ends here (4758 further characters in the source).*

## TechnicalReference_Asr_GenTool_CsAsrDbUpdateConsole.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_GenTool_CsAsrDbUpdateConsole.pdf`
- **Format:** `.pdf` (~336 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5955 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_GenTool_CsAsrDbUpdateConsole.pdf` for those.

```text
MICROSAR DB Update 
Technical Reference 
 
Description 
Version 1.9 
 
 
 
 
 
 
 
 
 
Authors Benjamin Gottschalk, Mario Kunz, Matthias Bannholzer 
Status Released 
 
 
 
Technical Reference MICROSAR DB Update 
2013, Vector Informatik GmbH Version: 1.9 
based on template version 4.5 
2 / 22 
Document Information 
History 
Author Date Version Remarks 
Benjamin Gottschalk 2009-12-10 1.0 Creation 
Benjamin Gottschalk 2009-12-17 1.1 Adapted Reference 
Documents 
Benjamin Gottschalk 2010-01-13 1.2 Added examples for 
validation and fix mode 
Benjamin Gottschalk 2010-03-31 1.3 Added chapter “Basic 
Concepts” 
Manuela Scheufele 2010-06-24 1.4 Add Appendix Supported Use 
Cases 
Benjamin Gottschalk 2010-09-27 1.5 ESCAN00045603 
Benjamin Gottschalk 2011-01-14 1.6 Added chapter 5 
Mario Kunz 2011-10-31 1.7 ESCAN00054591, 
ESCAN00054592 
Matthias Banholzer 2012-09-14 1.8 ESCAN00050371 
Mario Kunz 2013-03-27 1.9 ESCAN00065153 
Reference Documents 
No. Source Title Version 
[1] VECTOR TechnicalReference_Asr_GenTool_CsAsrInitialEcuC.pdf 1.0 
[2] VECTOR DbUpdateConsoleApplication.exe.config 
 
 
 
 
 
 
Please note 
We have configured the programs in accordance with your specifications in the 
q
```
*…excerpt ends here (4755 further characters in the source).*

## TechnicalReference_Asr_GenTool_CsAsrInitialEcuC.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_GenTool_CsAsrInitialEcuC.pdf`
- **Format:** `.pdf` (~752 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5949 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_GenTool_CsAsrInitialEcuC.pdf` for those.

```text
MICROSAR Initial ECUC Generator 
Technical Reference 
 
Description 
Version 1.9 
 
 
 
 
 
 
 
 
 
 
 
Authors Benjamin Gottschalk, Mario Kunz, Matthias Banholzer 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR Initial ECUC Generator 
2013, Vector Informatik GmbH Version: 1.9 
based on template version 4.5 
2 / 25 
Document Information 
History 
Author Date Version Remarks 
Benjamin Gottschalk 2009-12-10 1.0 Creation 
Benjamin Gottschalk 2010-06-18 1.1 Added list of supported intput 
and output AUTOSAR 
versions 
Benjamin Gottschalk 2010-08-10 1.2 Adapted lists of supported 
input and output AUTOSAR 
versions 
Benjamin Gottschalk 2010-11-09 1.3 Added constraint for 
overlaying pdus, which are 
part of a multiplexed pdu. 
Benjamin Gottschalk 2010-11-29 1.4 Added UseCase 
IdentityManager.Config 
Mario Kunz 2011-11-02 1.5 Adapted lists of supported 
input and output AUTOSAR 
versions 
Adapted chapter 2.4.5. 
Added restriction of identities. 
Matthias Banholzer 2012-02-29 1.6 Different behavior between 
DaVinci Developer and 
MICROSAR Initial ECUC 
Generator in Identity Manager 
with buffer overlaying 
Matthias Banholzer 2012-09-13 1.8 Added Appendix 
Mario Kunz 2013-02-13 1
```
*…excerpt ends here (4749 further characters in the source).*

## TechnicalReference_Asr_IoHwAb.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_IoHwAb.pdf`
- **Format:** `.pdf` (~603 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5959 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_IoHwAb.pdf` for those.

```text
MICROSAR IOHWAB 
Technical Reference 
 
 
Version 2.02.02 
 
 
 
 
 
 
 
 
 
 
 
Authors Christoph Ederer 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR IOHWAB 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Christian Marchl 2007-02-09 1.00.00 Initial version 
Christian Marchl 2007-08-09 1.01.00 Typos corrected; Added 
description for component 
name field 
Christian Marchl 2007-12-13 1.01.01 Version adapted according to 
new version scheme 
Christoph Ederer 2008-05-21 2.00.00 Transfer of the document to 
new Technical Reference 
template; Adapted 
descriptions and screenshots 
to new software version 
Christoph Ederer 2008-07-11 2.00.01 Update of document due to 
changes in DCM interface 
and RTE usage 
Christoph Ederer 2009-01-14 2.01.00 Update of the naming of 
graphical elements in the 
configuration, Screenshots 
reworked, DCM subfunctions 
reworked, Added description 
of default value in 
configuration 
Christoph Ederer 2009-03-23 2.01.01 Updated development error 
detection in GUI description, 
toolchain naming updated, 
hints added to chapter 4.1.2 
Christoph Ederer 2009-07-21 2.02.00 Updated description of the 
generation process (user 
blocks,
```
*…excerpt ends here (4759 further characters in the source).*

## TechnicalReference_Asr_MemIf.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_MemIf.pdf`
- **Format:** `.pdf` (~519 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5961 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_MemIf.pdf` for those.

```text
MICROSAR MemIf 
Technical Reference 
 
 
Version 1.0 
 
 
 
 
 
 
 
 
 
 
 
Authors Tobias Schmid 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR MemIf 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Tobias Schmid 2008-04-14 1.0 Creation of document 
Table 1-1 History of the document 
1.2 Reference Documents 
No. Title Version 
[1] AUTOSAR_SWS_Mem_AbstractionInterface.pdf V1.2.0 
[2] AUTOSAR_SWS_DET.pdf V2.2.0 
[3] AUTOSAR_BasicSoftwareModules.pdf V1.0.0 
[4] AUTOSAR_SWS_EEPROM_Abstraction.pdf V1.2.0 
[5] AUTOSAR_SWS_Flash_EEPROM_Emulation.pdf V1.2.0 
Table 1-2 Reference documents 
 
1.1 Scope of the Document 
This technical reference describes the gener al use of module MemIf (AUTOSAR Memory 
Abstraction Interface). 
 
 
Please note 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire. 
©2008, Vector Informatik GmbH Version: 1.0 
based on template version 3.1 
2/ 3 2
Tec
```
*…excerpt ends here (4761 further characters in the source).*

## TechnicalReference_Asr_Nm.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Nm.pdf`
- **Format:** `.pdf` (~1376 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5975 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Nm.pdf` for those.

```text
MICROSAR Network Management 
Interface 
Technical Reference 
 
NM Interface 
Version 2.22.00 
 
 
 
 
 
 
 
 
 
 
Authors Markus Drescher 
Status: Released 
 
 
 
 
 
Technical Reference MICROSAR Network Management Interface 
2013, Vector Informatik GmbH Version: 2.22.00 
based on template version 4.8.0 
2 / 104 
Document Information 
History 
Author Date Version Remarks 
Oliver Hornung 2006-10-24 1.00.00 ESCAN00018802: Creation of document for 
AUTOSAR Release 2.1. 
Oliver Hornung 2006-12-21 1.01.00 Reworked after User Review. 
Oliver Hornung 2007-01-07 1.02.00 ESCAN00019105: Update to actual 
implementation. 
Figures updated. 
Oliver Hornung 2007-03-09 1.03.00 ESCAN00019899: Database attribute 
description added. 
Oliver Hornung 2007-04-11 1.04.00 ESCAN00020054: Limp Home Indication 
feature added. 
Oliver Hornung 2007-09-24 2.00.00 ESCAN00022463: Update to current Software 
Specification for AUTOSAR Release 3 
Oliver Hornung 2008-02-01 2.01.00 Added coordination extension 
Oliver Hornung 2008-03-12 2.02.00 ESCAN00025306: Channel link-time support. 
Oliver Hornung 2008-04-02 2.02.01 Adapted coordination extension 
Oliver Hornung 2008-04-21 2.03.00 ESCAN00025501: Renaming of Tech
```
*…excerpt ends here (4775 further characters in the source).*

## TechnicalReference_Asr_NvM.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_NvM.pdf`
- **Format:** `.pdf` (~947 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5957 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_NvM.pdf` for those.

```text
MICROSAR NVM 
Technical Reference 
 
 
Version 3.07.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Manfred Duschinger 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR NVM 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Christian Kaiser 2007-08-20 1.4 AUTOSAR 2.1, 
updated for EAD3.1 usage, 
conversion to new template 
Christian Kaiser 2007-12-06 3.01.00 Change of the document's versioning 
scheme to correspond to the module's 
major and minor, 
update of parameter description in 
chapter 'Graphical Configuration of NvM' 
and service port generation description, 
remove of DATASET ROM, feature not 
supported anymore, 
remove of introduction paragraphs from 
'Description of Memory Mapping and 
Compiler Abstraction', not subject of this 
document, 
simplified 'Block Management Types' 
naming, 
formal changes 
Christian Kaiser 2008-01-11 3.01.01 New chapter to clarify the dependency on 
the CRC library, 
stated explicitly that DET is optional, 
corrected default values 
Manfred Duschinger, 
Heike Bischof 
2008-05-23 3.02.00 AUTOSAR 3, 
conversion to Technical Reference 
Manfred Duschinger 2008-12-08 3.03.00 ESCAN00027300: Description of 
NvM_ServiceIdType in 
SingleBlockC
```
*…excerpt ends here (4757 further characters in the source).*

## TechnicalReference_Asr_PduR.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_PduR.pdf`
- **Format:** `.pdf` (~2126 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5954 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_PduR.pdf` for those.

```text
MICROSAR PDU Router 
Technical Reference 
 
 
Version 3.10.02 
 
 
 
 
 
 
 
 
 
 
 
Authors Hartmut Hörner, Hannes Haas, Erich Schondelmaier, 
Gunnar Meiss 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR PDU Router 
2012, Vector Informatik GmbH Version: 3.10.02 
based on template version 4.6 
2 / 106 
Document Information 
History 
Author Date Version Remarks 
Hartmut Hörner 2006-02-01 0.1 Initial version 
Hartmut Hörner 2006-03-13 0.2 Pre-compile variants added in chapter 3.6 
Configuration Phases 
Hartmut Hörner 2006-03-17 0.3 Added chapter with required API functions 
Hannes Haas 2006-06-14 2.0 Adapted to AUTOSAR version 2.0 
Hannes Haas 2006-07-30 2.1 Added LIN IF support 
Hannes Haas 2006-11-22 2.2 Added CAN TP support 
Added Post-Build support 
Hannes Haas 2007-04-26 2.3 New Template 
Simplified post-build configuration procedure 
Revision of all chapters 
Hannes Haas 2007-11-20 2.4 Removed non-selectable post-build configuration 
Added Interface Gateway with Callouts 
Hannes Haas 2008-01-08 2.5 Added TP Gateway and memory allocation 
Added Glossary 
Adapted to AUTOSAR 3 
Added include structure 
Added J1939TP support 
Hannes Haas 2008-03-26 3.0 Corrected return val
```
*…excerpt ends here (4754 further characters in the source).*

## TechnicalReference_Asr_Xcp.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Xcp.pdf`
- **Format:** `.pdf` (~1197 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5973 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Asr_Xcp.pdf` for those.

```text
XCP Protocol Layer 
Technical Reference 
 
 
 
 
Version 2.03.00 
 
 
 
 
 
 
 
 
 
 
 
Version: 2.03.00 
Status: Released 
 
 
 
 
Technical Reference XCP Protocol Layer 
2013, Vector Informatik GmbH Version: 2.03.00 
 
2 / 109 
1 History 
Date Version Remarks 
2005-01-17 1.00.00 ESCAN00009143: Initial draft 
Warning Text added 
2005-06-22 1.01.00 FAQ extended: ESCAN00012356, ESCAN00012314 
ESCAN00012617: Add service to retrieve XCP state 
2005-12-20 1.02.00 ESCAN00013883: Revise Resume Mode 
2006-03-09 1.03.00 ESCAN00015608: Support command TRANSPORT_LAYER_CMD 
ESCAN00015609: Support XCP on FlexRay Transport Layer 
2006-04-24 1.04.00 ESCAN00015913: Correct filenames 
Data page banking support of application callback template added 
2006-05-08 1.05.00 ESCAN00016263: Describe support of reflected CRC16 CCITT 
ESCAN00016159: Add demo disclaimer to XCP Basic 
2006-05-29 1.06.00 ESCAN00016226: Support XCP on LIN Transport Layer 
2006-07-20 1.07.00 ESCAN00012636: Add configuration with GENy 
ESCAN00016956: Support AUTOSAR CRC module 
2006-10-26 1.08.00 ESCAN00018115: DPRAM Support only available in XCP Basic 
ESCAN00017948: Add paging support 
ESCAN00017221: Documentation of reentrant
```
*…excerpt ends here (4773 further characters in the source).*

## TechnicalReference_DbcRules_Fiat_FAS.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_DbcRules_Fiat_FAS.pdf`
- **Format:** `.pdf` (~382 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5960 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_DbcRules_Fiat_FAS.pdf` for those.

```text
DBC and LDF Configuration 
Technical Reference 
 
for FGA 
Version 1.7.2 
 
 
 
 
 
 
 
 
 
 
 
Authors Hannes Haas, Milena Shakir 
Status Released 
 
 
 
 
 
Technical Reference DBC and LDF Configuration 
2013, Vector Informatik GmbH Version: 1.7.2 
based on template version 4.7.2 
2 / 28 
Document Information 
History 
Author Date Version Remarks 
Hannes Haas, Klaus Emmert 2010-09-27 1.0.0 Created 
Hannes Haas 2010-09-28 1.0.1 Added update bit for signal groups 
Hannes Haas 2010-10-13 1.0.2 GenMsgNrOfRepetition description 
changed 
Removed restrictions of Tx Mode 
combination 
Added description to message routing 
Hannes Haas 2010-10-15 1.0.3 Changed spec. for GenSigTimeoutTime 
Hannes Haas 2010-11-08 1.0.4 GenMsgCycleTimeFast for Tx modes 
with repetitions 
Hannes Haas 2010-12-17 1.1.0 Added LDF 2.1 rules 
Renamed NmNodeType to 
NwmNodeType 
Hannes Haas 2011-01-03 1.1.1. Improved Tx mode mappings by adding 
GenMsgCycleTimeFast to the examples 
Fixed issues in Send Type examples 
Hannes Haas 2011-03-07 1.1.2 CONTROL Tx mode only supported for 
carry-back ECUs 
Hannes Haas 2011-04-07 1.1.3 Release 
Hannes Haas 2011-05-03 1.1.4 Changed definition of 
GenMsgNrOfRepetition to make
```
*…excerpt ends here (4760 further characters in the source).*

## TechnicalReference_DrvCanAsr_Tms470_Dcan.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_DrvCanAsr_Tms470_Dcan.pdf`
- **Format:** `.pdf` (~2698 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5964 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_DrvCanAsr_Tms470_Dcan.pdf` for those.

```text
MICROSAR CAN Driver 
Technical Reference 
 
Texas Instruments 
Tms470 / Tms570 
Dcan 
 
Version 1.10.00 
 
 
 
 
 
 
 
 
 
 
Authors Georg Pflügel, Sebastian Gärtner, 
Mihai Olariu, Robert Schelkle 
Status Released 
 
 
 
 
 
Technical Reference MICROSAR CAN Driver 
2013, Vector Informatik GmbH Version: 1.10.00 Page 2 
1. Document Information 
1.1 History 
Platforms 
Author Date Version Remarks 
Georg Pflügel 2007-01-12 1.00 Initial version. 
Georg Pflügel 2007-11-15 1.01 CAN-Driver Update to ASR2.1. 
Georg Pflügel 2008-08-05 1.02 CAN-Driver Update to ASR3 
Sebastian 
Gärtner 
2009-09-11 1.03 CAN-Driver Update to R7. 
Sebastian 
Gärtner 
2009-12-14 1.04 Local power-down mode added. 
Mihai Olariu 2010-07-28 1.05 CAN-Driver Update to R9. 
Description for DCAN Issue#22. 
Georg Pflügel 2011-03-08 1.06 Description of mailbox objects updated 
Georg Pflügel 2011-07-06 1.07 Description for the TMS570LS30316U added 
Georg Pflügel 2011-08-24 1.08 Description for GeneratorGeny added 
Georg Pflügel 2012-07-19 1.09 Update to R14 
Robert Schelkle 2013-01-16 1.10 Update to template 2.05.01 
Adapt Overrun/Overwrite description 
Table 1-1 History of the Document 
 
1.2 Reference Documents 
No. Titl
```
*…excerpt ends here (4764 further characters in the source).*

## TechnicalReference_ExternalDependenciesOfGenerators.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_ExternalDependenciesOfGenerators.pdf`
- **Format:** `.pdf` (~158 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (2578 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_ExternalDependenciesOfGenerators.pdf` for those.

```text
External Tool Dependencies 
Technical Reference 
 
Standalone Generators 
Version 1.3 
 
 
 
 
 
 
 
 
 
 
 
Authors Manuela Scheufele 
Status Released 
 
 
 
 
 
Technical Reference External Tool Dependencies 
2013, Vector Informatik GmbH Version: 1.3 
based on template version 4.7.2 
2 / 4 
History 
Author Date Version Remarks 
Manuela Scheufele 
Günther Piehler 
2010-08-26 1.0 Create and release document 
Manuela Scheufele 2010-08-26 1.1 Minor changes 
Manuela Scheufele 2010-09-03 1.2 Delete Vector GenTool_ 
CsDataServer 
Klaus Emmert 2013-06-07 1.3 Microsoft links deleted in 
chapter 1.2 
 
Technical Reference External Tool Dependencies 
2013, Vector Informatik GmbH Version: 1.3 
based on template version 4.7.2 
3 / 4 
1 External Tool Dependencies 
The MICROSAR Generators included in your SIP can be used without installing the 
configuration tools such as GENy and DaVinci Configurator. 
If the configuration tools have not been installed, dependencies to external software such 
as the Microsoft .NET Framework* might be unresolved. This will cause the generators to 
now work. 
Before using the standalone generators the software listed in this document has to be 
installed on th
```
*…excerpt ends here (1378 further characters in the source).*

## TechnicalReference_GenTool_CsAsrLegacyDb2SystemDescr_Vector.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_GenTool_CsAsrLegacyDb2SystemDescr_Vector.pdf`
- **Format:** `.pdf` (~632 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5920 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_GenTool_CsAsrLegacyDb2SystemDescr_Vector.pdf` for those.

```text
Vector Legacy Converter 
Technical Reference 
 
Technical Documentation 
Version 1.3 
 
 
 
 
 
 
 
 
 
 
 
Authors Thorsten Fröhlinghaus 
Status Released 
 
 
 
 
 
Technical Reference Vector Legacy Converter 
2012, Vector Informatik GmbH Version: 1.3 
based on template version 4.11.1 
2 / 29 
Document Information 
History 
Author Date Version Remarks 
Thorsten Fröhlinghaus 2011-04-07 1.0 Created 
Thorsten Fröhlinghaus 2011-04-07 1.0 Released 
Thorsten Fröhlinghaus 2011-12-20 1.1 Legacy Converter V1.3.0 
Thorsten Fröhlinghaus 2012-01-20 1.1 Released 
Thorsten Fröhlinghaus 2012-03-22 1.2 Released 
Thorsten Fröhlinghaus 2012-11-21 1.3 Released 
Reference Documents 
No. Source Title Version 
[1] Autosar Specification of the System Template, R3.1 Rev 4 V3.2.0 
[2] Autosar Specification of the System Template, R3.2 Rev 1 V3.4.0 
[3] Autosar System Template, R4.0 Rev 3 V4.2.0 
 
 
 
 
 
Caution 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector´s release of the programs delivered to your 
company is expressly restricted to the configurati
```
*…excerpt ends here (4720 further characters in the source).*

## TechnicalReference_VStdLib.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_VStdLib.pdf`
- **Format:** `.pdf` (~191 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5959 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_VStdLib.pdf` for those.

```text
VStdLib 
Technical Reference 
 
Vector Standard Library 
Version 1.6 
 
 
 
 
 
 
 
 
 
 
 
Authors Patrick Markl 
Status Released 
 
 
 
 
 
Technical Reference VStdLib 
©2009, Vector Informatik GmbH Version: 1.6 
based on template version 3.7 
2/ 2 0
1 Document Information 
1.1 History 
Author Date Version Remarks 
Patrick Markl 2008-02-06 1.0 Creation, merge from Application Note 
Patrick Markl 2008-10-31 1.3 Fixed document version 
Patrick Markl 2008-11-07 1.4 Added information about mixed VStdLib versions
Patrick Markl 2009-07-02 1.5 Updated assertion codes 
Added chapter about QNX OS 
Patrick Markl 2009-10-16 1.6 Described inclusion of OSEK OS header file 
Table 1-1 History of the Document 
 
 
 
 
 
 
Please note 
We have configured the programs in accordance with your specifications in the 
questionnaire. Whereas the programs do support other configurations than the one 
specified in your questionnaire, Vector’s release of the programs delivered to your 
company is expressly restricted to the configuration you have specified in the 
questionnaire. 
Technical Reference VStdLib 
©2009, Vector Informatik GmbH Version: 1.6 
based on template version 3.7 
3/ 2 0
Contents 
1 Docu
```
*…excerpt ends here (4759 further characters in the source).*

## TechnicalReference_Vmm.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Vmm.pdf`
- **Format:** `.pdf` (~220 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5959 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_Vmm.pdf` for those.

```text
Vehicle Mode Management 
Technical Reference 
 
VMM 
Version 1.06.00 
 
 
 
 
 
 
 
 
 
 
 
Authors Thomas Kuhl, Markus Schwarz 
Status Released 
 
 
 
 
 
Technical Reference Vehicle Mode Management 
1 Document Information 
1.1 History 
Author Date Version Remarks 
Thomas Petrus 2008-06-02 1.0 Initial Version 
Thomas Kuhl 2008-10-17 1.1 Update configuration chapter 
Thomas Kuhl 2008-11-28 1.2 Update configuration chapter 
Updated Chapter 7.4 
Add function description: 
Vmm_BusSm_EnableRecepti
onDM 
Add function description: 
Vmm_BusSm_DisableRecept
ionDM 
Thomas Kuhl 2009-03-16 1.3 Add chapter 4.3 ECU Passive 
Handling 
Add API 
Vmm_Dcm_SetPassiveMode 
Update chapter “System 
configuration” 
Thomas Kuhl 2009-08-10 1.4 add chapter 5.4 Critical code 
sections 
Thomas Kuhl 2009-11-16 1.5 ESCAN00038948 
Thomas Kuhl 2010-04-29 1.05.01 ESCAN00040934 
Thomas Kuhl 2010-08-10 1.05.02 ESCAN00044654 
Thomas Kuhl 2011-02-10 1.06.00 Extend description of 
Vmm_Init 
Table 1-1 History of the Document 
1.2 Reference Documents 
No. Title Version 
[1] AUTOSAR_BasicSoftwareModules.pdf V1.0.0 
[2] AUTOSAR_SWS_DET.pdf V2.2.0 
[3] AN-ISC-8-1118 MICROSAR BSW Compatibility Check V1.0.0 
Table 1-2 Referen
```
*…excerpt ends here (4759 further characters in the source).*

## TechnicalReference_WakeUp_and_Sleep_with_AUTOSAR.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_WakeUp_and_Sleep_with_AUTOSAR.pdf`
- **Format:** `.pdf` (~1213 KiB)
- **Kind:** Vector Technical Reference (MICROSAR BSW)
- **Status:** converted — text extracted from the binary (5956 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/HLDD/BSW/TechnicalReference_WakeUp_and_Sleep_with_AUTOSAR.pdf` for those.

```text
Wake-up and Sleep with AUTOSAR 
Technical Reference 
 
Wakeup CAN, LIN, FlexRay via Communication Channel 
Version 1.00.05 
 
 
 
 
 
 
 
 
 
 
 
Authors Mark A. Fingerle, Thomas Kuhl 
Status Released 
 
 
 
 
 
Technical Reference Wake-up and Sleep with AUTOSAR 
2013, Vector Informatik GmbH Version: 1.00.05 
based on template version 4.2 
2 / 42 
Document Information 
History 
Author Date Version Remarks 
Mark A. Fingerle 2010-01-19 1.0 Initial version 
Thomas Kuhl 2011-02-22 1.00.01 Change CAN wake up source 
validation handling refer to 
2.3.5 
Mark A. Fingerle, Klaus Emmert 2011-07-19 1.00.02 Remove Chapter “1.2.4 
Wake-up by polling the wake-
up source(s)” feature not 
supported by EcuM 
> Synchronous and 
asynchronous wake-up 
handling added (chapter 
1.4.1). 
> New screen shots for 
ECUM and ICU 
Klaus Emmert 2013-01-21 1.00.03 Chapter 1.3 added 
Chapter 2.3.5 example code 
updated 
Thoms Kuhl 2013-05-22 1.00.04 correct typing errors inside 
source code samples 
(ESCAN00052636) 
Thomas Kuhl 2013-08-01 1.00.05 correct typing errors 
(ESCAN00068119) 
Reference Documents 
No. Source Title Version 
[1] ASR Specification of ECU State Manager 1.2.0 
[2] Vector AN-ISC-2-1098_Wakeu
```
*…excerpt ends here (4756 further characters in the source).*

## CDDInterface_UnitTestReports_WithOutPS.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/Tessy/report/CDDInterface_UnitTestReports_WithOutPS.pdf`
- **Format:** `.pdf` (~1934 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/Tessy/report/CDDInterface_UnitTestReports_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-06-03, 15:23:37+0530
Project CDDInterface_FIASA
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 7
Successful: 7
Failed: 0
Not Executed: 0
Date: 2016-06-03
Time: 15:23:37+0530
Selected Project Items
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Init1"
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Init2"
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Per1"
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Per2"
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Per4"
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Per5"
Test Object "CBD_UnitTest/CDDInterface/
```
*…excerpt ends here (5299 further characters in the source).*

## CDDInterface_UnitTestReports_WithPS.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/Tessy/report/CDDInterface_UnitTestReports_WithPS.pdf`
- **Format:** `.pdf` (~1933 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5999 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/CDDInterface/utp/Tessy/report/CDDInterface_UnitTestReports_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-06-03, 15:08:31+0530
Project CDDInterface_FIASA
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 7
Successful: 7
Failed: 0
Not Executed: 0
Date: 2016-06-03
Time: 15:08:31+0530
Selected Project Items
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Init1"
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Init2"
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Per1"
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Per2"
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Per4"
Test Object "CBD_UnitTest/CDDInterface/CDDInterface_Per5"
Test Object "CBD_UnitTest/CDDInterface/
```
*…excerpt ends here (5299 further characters in the source).*

## DemIf_UnitTestReport_WithOutPS_PIL.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/DemIf/utp/Tessy/report/DemIf_UnitTestReport_WithOutPS_PIL.pdf`
- **Format:** `.pdf` (~660 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5997 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/DemIf/utp/Tessy/report/DemIf_UnitTestReport_WithOutPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-05-18, 16:07:19+0530
Project DemIf
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 4
Successful: 4
Failed: 0
Not Executed: 0
Date: 2016-05-18
Time: 16:07:19+0530
Selected Project Items
Test Collection "UnitTest"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test 
object on the y axis. Each bar is divided into passed, not executed and failed test cases. The test case results 
do not take into account any coverage result
```
*…excerpt ends here (5297 further characters in the source).*

## DemIf_UnitTestReport_WithPS_PIL.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/DemIf/utp/Tessy/report/DemIf_UnitTestReport_WithPS_PIL.pdf`
- **Format:** `.pdf` (~661 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5997 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/DemIf/utp/Tessy/report/DemIf_UnitTestReport_WithPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-05-18, 15:58:44+0530
Project DemIf
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 4
Successful: 4
Failed: 0
Not Executed: 0
Date: 2016-05-18
Time: 15:58:44+0530
Selected Project Items
Test Collection "UnitTest"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test 
object on the y axis. Each bar is divided into passed, not executed and failed test cases. The test case results 
do not take into account any coverage result
```
*…excerpt ends here (5297 further characters in the source).*

## DfltConfigData_UnitTestReport_WithOutPS_PIL.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/DfltConfigData/utp/Tessy/report/DfltConfigData_UnitTestReport_WithOutPS_PIL.pdf`
- **Format:** `.pdf` (~269 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/DfltConfigData/utp/Tessy/report/DfltConfigData_UnitTestReport_WithOutPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-05-23, 16:02:21+0530
Project DfltConfigData
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 1
Successful: 1
Failed: 0
Not Executed: 0
Date: 2016-05-23
Time: 16:02:21+0530
Selected Project Items
Test Object "CBD_UnitTest/DfltConfigData/DfltConfigData_Init1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test 
object on the y axis. Each bar is divided into passed, not executed and failed test cases. The test case results
```
*…excerpt ends here (5298 further characters in the source).*

## DfltConfigData_UnitTestReport_WithPS_PIL.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/DfltConfigData/utp/Tessy/report/DfltConfigData_UnitTestReport_WithPS_PIL.pdf`
- **Format:** `.pdf` (~269 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/DfltConfigData/utp/Tessy/report/DfltConfigData_UnitTestReport_WithPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-05-23, 16:06:08+0530
Project DfltConfigData
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 1
Successful: 1
Failed: 0
Not Executed: 0
Date: 2016-05-23
Time: 16:06:08+0530
Selected Project Items
Test Object "CBD_UnitTest/DfltConfigData/DfltConfigData_Init1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test 
object on the y axis. Each bar is divided into passed, not executed and failed test cases. The test case results
```
*…excerpt ends here (5298 further characters in the source).*

## IoHwAbstractionUsr_UnitTestReports_WithOutPS.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/IoHwAbstractionUsr/utp/Tessy/report/IoHwAbstractionUsr_UnitTestReports_WithOutPS.pdf`
- **Format:** `.pdf` (~1050 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/IoHwAbstractionUsr/utp/Tessy/report/IoHwAbstractionUsr_UnitTestReports_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-06-02, 10:15:58+0530
Project IoHwAbstractionUsr_FIASA
© Report created by TESSY V3.1.11, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 5
Successful: 5
Failed: 0
Not Executed: 0
Date: 2016-06-02
Time: 10:15:58+0530
Selected Project Items
Test Object "UnitTest/IoHwAbstractionUsr/IoHwAb_CaptureADC"
Test Object "UnitTest/IoHwAbstractionUsr/IoHwAb_Init"
Test Object "UnitTest/IoHwAbstractionUsr/IoHwAb_ReadAdc"
Test Object "UnitTest/IoHwAbstractionUsr/IoHwAb_SlowADCGroupValidity"
Test Object "UnitTest/IoHwAbstractionUsr/IoHwAb_StartAdc"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test
```
*…excerpt ends here (5298 further characters in the source).*

## IoHwAbstractionUsr_UnitTestReports_WithPS.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/IoHwAbstractionUsr/utp/Tessy/report/IoHwAbstractionUsr_UnitTestReports_WithPS.pdf`
- **Format:** `.pdf` (~1050 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/IoHwAbstractionUsr/utp/Tessy/report/IoHwAbstractionUsr_UnitTestReports_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-06-02, 10:40:23+0530
Project IoHwAbstractionUsr_FIASA
© Report created by TESSY V3.1.11, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 5
Successful: 5
Failed: 0
Not Executed: 0
Date: 2016-06-02
Time: 10:40:23+0530
Selected Project Items
Test Object "UnitTest/IoHwAbstractionUsr/IoHwAb_CaptureADC"
Test Object "UnitTest/IoHwAbstractionUsr/IoHwAb_Init"
Test Object "UnitTest/IoHwAbstractionUsr/IoHwAb_ReadAdc"
Test Object "UnitTest/IoHwAbstractionUsr/IoHwAb_SlowADCGroupValidity"
Test Object "UnitTest/IoHwAbstractionUsr/IoHwAb_StartAdc"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test
```
*…excerpt ends here (5298 further characters in the source).*

## WdgM_Graph.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/Source/GenData/WdgM_Graph.pdf`
- **Format:** `.pdf` (~39 KiB)
- **Kind:** Reference document (PDF)
- **Status:** converted — text extracted from the binary (777 characters in total; showing first 777). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/Source/GenData/WdgM_Graph.pdf` for those.

```text
SE_100ms_9
SE_10ms_10
SE_10ms_9
SE_4ms_10SE_100ms_10
SE_100ms_8 SE_4ms_9
SE_2ms_10
SE_2ms_8
SE_2ms_9
ChkPtAp10_100msStart_CP(0)
ChkPtAp10_100msEnd_CP(1)
LT_100ms_10
ChkPtAp8_100msStart_CP(0)
GT_100ms_10_8
ChkPtAp8_100msEnd_CP(1)
LT_100ms_8
ChkPtAp9_100msStart_CP(0)
GT_100ms_8_9
ChkPtAp9_100msEnd_CP(1)
LT_100ms_9
ChkPtAp10_10msStart_CP(0)
ChkPtAp10_10msEnd_CP(1)
LT_10ms_10
ChkPtAp9_10msStart_CP(0)
GT_10ms_10_9
ChkPtAp9_10msEnd_CP(1)
LT_10ms_9
ChkPtAp10_4msStart_CP(0)
ChkPtAp10_4msEnd_CP(1)
LT_4ms_10
ChkPtAp9_4msStart_CP(0)
GT_4ms_10_9
ChkPtAp9_4msEnd_CP(1)
LT_4ms_9
ChkPtAp10_2msStart_CP(0)
ChkPtAp10_2msEnd_CP(1)
LT_2ms_10
ChkPtAp8_2msStart_CP(0)
GT_2ms_10_8
GlbFinal_CP0(2)
ChkPtAp8_2msEnd_CP(1)
LT_2ms_8
ChkPtAp9_2msStart_CP(0)
GT_2ms_8_9
ChkPtAp9_2msEnd_CP(1)
LT_2ms_9
```

## SrlComInput_UnitTestReport_WithOutPS_PIL.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/SrlComInput/utp/Tessy/report/SrlComInput_UnitTestReport_WithOutPS_PIL.pdf`
- **Format:** `.pdf` (~7945 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/SrlComInput/utp/Tessy/report/SrlComInput_UnitTestReport_WithOutPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-06-07, 18:38:50+0530
Project Fiasa_SrlComInput
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 26
Successful: 25
Failed: 1
Not Executed: 0
Date: 2016-06-07
Time: 18:38:50+0530
Selected Project Items
Test Object "CBD_UnitTest/SrlComInput/Appl_CanSM_BusOffBegin"
Test Object "CBD_UnitTest/SrlComInput/Appl_CanSM_BusOffEnd"
Test Object "CBD_UnitTest/SrlComInput/Appl_COMCbk_Com_CmdIgn_FailSts__STATUS_C_BCM2__CCAN"
Test Object "CBD_UnitTest/SrlComInput/Appl_COMCbk_Com_CmdIgnSts__STATUS_C_BCM2__CCAN"
Test Object "CBD_UnitTest/SrlComInput/
Appl_COMCbk_Com_Digit_01__CFG_DATA_CODE_REQUEST__C
```
*…excerpt ends here (5300 further characters in the source).*

## SrlComInput_UnitTestReport_WithPS_PIL.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/SrlComInput/utp/Tessy/report/SrlComInput_UnitTestReport_WithPS_PIL.pdf`
- **Format:** `.pdf` (~8048 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (6000 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/SrlComInput/utp/Tessy/report/SrlComInput_UnitTestReport_WithPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-06-07, 18:52:52+0530
Project Fiasa_SrlComInput
© Report created by TESSY V3.1.11, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 26
Successful: 25
Failed: 1
Not Executed: 0
Date: 2016-06-07
Time: 18:52:52+0530
Selected Project Items
Test Object "CBD_UnitTest/SrlComInput/Appl_CanSM_BusOffBegin"
Test Object "CBD_UnitTest/SrlComInput/Appl_CanSM_BusOffEnd"
Test Object "CBD_UnitTest/SrlComInput/Appl_COMCbk_Com_CmdIgn_FailSts__STATUS_C_BCM2__CCAN"
Test Object "CBD_UnitTest/SrlComInput/Appl_COMCbk_Com_CmdIgnSts__STATUS_C_BCM2__CCAN"
Test Object "CBD_UnitTest/SrlComInput/
Appl_COMCbk_Com_Digit_01__CFG_DATA_CODE_REQUEST__C
```
*…excerpt ends here (5300 further characters in the source).*

## SrlComOutput_UnitTestReports_WithOutPS.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/SrlComOutput/utp/Tessy/report/SrlComOutput_UnitTestReports_WithOutPS.pdf`
- **Format:** `.pdf` (~740 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/SrlComOutput/utp/Tessy/report/SrlComOutput_UnitTestReports_WithOutPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-06-03, 16:30:29+0530
Project SrlcomOutput_FIASA
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 3
Successful: 2
Failed: 1
Not Executed: 0
Date: 2016-06-03
Time: 16:30:29+0530
Selected Project Items
Test Object "CBD_UnitTest/SrlComOutput/CfgCodeResponse"
Test Object "CBD_UnitTest/SrlComOutput/SetBusOffRecovered"
Test Object "CBD_UnitTest/SrlComOutput/SrlComOutput_Per1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test
```
*…excerpt ends here (5298 further characters in the source).*

## SrlComOutput_UnitTestReports_WithPS.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/SrlComOutput/utp/Tessy/report/SrlComOutput_UnitTestReports_WithPS.pdf`
- **Format:** `.pdf` (~740 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/SrlComOutput/utp/Tessy/report/SrlComOutput_UnitTestReports_WithPS.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-06-03, 16:36:16+0530
Project SrlcomOutput_FIASA
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 3
Successful: 2
Failed: 1
Not Executed: 0
Date: 2016-06-03
Time: 16:36:16+0530
Selected Project Items
Test Object "CBD_UnitTest/SrlComOutput/CfgCodeResponse"
Test Object "CBD_UnitTest/SrlComOutput/SetBusOffRecovered"
Test Object "CBD_UnitTest/SrlComOutput/SrlComOutput_Per1"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test
```
*…excerpt ends here (5298 further characters in the source).*

## VehPwrMd_UnitTestReport_WithOutPS_PIL.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/VehPwrMd/utp/Tessy/report/VehPwrMd_UnitTestReport_WithOutPS_PIL.pdf`
- **Format:** `.pdf` (~691 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/VehPwrMd/utp/Tessy/report/VehPwrMd_UnitTestReport_WithOutPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-06-03, 15:20:54+0530
Project VehPwrMd
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 2
Successful: 2
Failed: 0
Not Executed: 0
Date: 2016-06-03
Time: 15:20:54+0530
Selected Project Items
Test Collection "UnitTest"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test 
object on the y axis. Each bar is divided into passed, not executed and failed test cases. The test case results 
do not take into account any coverage resu
```
*…excerpt ends here (5298 further characters in the source).*

## VehPwrMd_UnitTestReport_WithPS_PIL.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/SwProject/VehPwrMd/utp/Tessy/report/VehPwrMd_UnitTestReport_WithPS_PIL.pdf`
- **Format:** `.pdf` (~691 KiB)
- **Kind:** Unit-test report (Tessy)
- **Status:** converted — text extracted from the binary (5998 characters in total; showing first 700). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/SwProject/VehPwrMd/utp/Tessy/report/VehPwrMd_UnitTestReport_WithPS_PIL.pdf` for those.

```text
TEST OVERVIEW REPORT 2016-06-03, 15:31:08+0530
Project VehPwrMd
© Report created by TESSY V3.1.13, report template V2.0 1
Summary Overall Test Object Results (including Coverage)
Total Test Objects: 2
Successful: 2
Failed: 0
Not Executed: 0
Date: 2016-06-03
Time: 15:31:08+0530
Selected Project Items
Test Collection "UnitTest"
Used Test Environments
TI TMS 570 PLS UDE (Default)
Test Case Results for Each Test Object (without Coverage)
The table above shows each test object on the x axis and the number of test cases of the respective test 
object on the y axis. Each bar is divided into passed, not executed and failed test cases. The test case results 
do not take into account any coverage resu
```
*…excerpt ends here (5298 further characters in the source).*

## ReleaseNotes_Artt_Generator.pdf

- **Source:** `Fiasa_326_327_EPS_TMS570/Tools/AsrProject/Generators/Artt/artt/ReleaseNotes_Artt_Generator.pdf`
- **Format:** `.pdf` (~44 KiB)
- **Kind:** Reference document (PDF)
- **Status:** converted — text extracted from the binary (5390 characters in total; showing first 1200). Layout, tables, figures and images are omitted; consult `Fiasa_326_327_EPS_TMS570/Tools/AsrProject/Generators/Artt/artt/ReleaseNotes_Artt_Generator.pdf` for those.

```text
Page 1 of 14
Copyright (c) 2010 by BMW Group. All rights reserved.
BMW Package Release Notes
Artt_Generator-2.0.2
Package Status:
Released
Author:
BMW Group
Version:
2.0.2
Release Date:
23-Nov-2011

Page 2 of 14
Copyright (c) 2010 by BMW Group. All rights reserved.
1 Revision History
 1.0.1
 03-Oct-2008
Initial revision. CR70051, CR70068.
 1.0.2
 29-Jun-2009
Support of more BAC2.1 templates. CR70168, 
CR70166, CR70167, CR70195, CR70237, 
CR70267.
 1.0.3
 27-Oct-2009
Performance optimization CR70341.
 1.1.0
 11-Nov-2009
User friendliness and portability CR70397, 
CR70343.
 1.1.1
 27-May-2010
CR70519.
 1.2.0
 30-Jun-2010
New validation feature CR70359, CR .
 1.3.0
 11-Oct-2010
AUTOSAR 4.0 schema CR .
 2.0.0
 15-Mar-2011
Behaviour of ValueOf() changed CR71004, 
CR71005.
 2.0.1
 14-Apr-2011
Method ModuleConfAtDefRefTo() added CR71008.
 2.0.2
 23-Nov-2011
CR71146, CR71147.
 Revision
 Date
 Remarks

Page 3 of 14
Copyright (c) 2010 by BMW Group. All rights reserved.
2 Package Enumeration Scheme
3 Package Description
artt is a command line application allowing to generate text files, including source code, from 
AUTOSAR descriptions. As input data artt uses a template file describing stati
```
*…excerpt ends here (4190 further characters in the source).*

## Static-analysis outputs (272 files)

QA-C analyser transcripts (`.err`/`.met`) for this module — reproduce with the QA-C project in `tools/` (or the shared `QAC/` configuration). Tabulated, not embedded:

<details>
<summary>Full list of analyser outputs</summary>

- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/AbortHandler.c.err` (~3 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/AbortHandler.c.met` (~136 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Adc.c.err` (~756 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Adc.c.met` (~1838 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Adc2.c.err` (~767 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Adc2.c.met` (~1866 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Adc_Common.c.err` (~698 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Adc_Common.c.met` (~1820 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_AbsHwPos.c.err` (~1089 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_AbsHwPos.c.met` (~1917 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ActivePull.c.err` (~1011 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ActivePull.c.met` (~1899 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ApXcp.c.err` (~5048 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ApXcp.c.met` (~3774 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Assist.c.err` (~640 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Assist.c.met` (~1797 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_AssistFirewall.c.err` (~891 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_AssistFirewall.c.met` (~1855 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_AstLmt.c.err` (~831 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_AstLmt.c.met` (~1850 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_AvgFricLrn.c.err` (~1162 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_AvgFricLrn.c.met` (~1955 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_BVDiag.c.err` (~772 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_BVDiag.c.met` (~1814 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_BatteryVoltage.c.err` (~1448 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_BatteryVoltage.c.met` (~2582 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ChkPtAp10.c.err` (~413 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ChkPtAp10.c.met` (~905 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ChkPtAp8.c.err` (~413 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ChkPtAp8.c.met` (~896 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ChkPtAp9.c.err` (~495 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ChkPtAp9.c.met` (~1451 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ComplErr.c.err` (~467 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ComplErr.c.met` (~1755 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_CtrldDisShtdn.c.err` (~828 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_CtrldDisShtdn.c.met` (~1831 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_CurrCmd.c.err` (~646 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_CurrCmd.c.met` (~1933 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_CurrParamComp.c.err` (~707 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_CurrParamComp.c.met` (~1838 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Damping.c.err` (~753 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Damping.c.met` (~1835 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DampingFirewall.c.err` (~964 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DampingFirewall.c.met` (~1927 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DemIf.c.err` (~565 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DemIf.c.met` (~1053 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DfltConfigData.c.err` (~2150 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DfltConfigData.c.met` (~3258 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DiagMgr_Core.c.err` (~1421 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DiagMgr_Core.c.met` (~2606 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DiagMgr_DemIf.c.err` (~1508 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DiagMgr_DemIf.c.met` (~2661 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DiagMgr_FailAction.c.err` (~776 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DiagMgr_FailAction.c.met` (~1858 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DiagSvc.c.err` (~5127 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DiagSvc.c.met` (~4560 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DigPhsReasDiag.c.err` (~890 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_DigPhsReasDiag.c.met` (~1854 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_EOTActuatorMng.c.err` (~624 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_EOTActuatorMng.c.met` (~1857 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ElePwr.c.err` (~510 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ElePwr.c.met` (~1760 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_EtDmpFw.c.err` (~767 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_EtDmpFw.c.met` (~1818 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_FltInjection.c.err` (~545 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_FltInjection.c.met` (~913 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_FrqDepDmpnInrtCmp.c.err` (~763 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_FrqDepDmpnInrtCmp.c.met` (~1851 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Gsod.c.err` (~796 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Gsod.c.met` (~1591 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_HiLoadStall.c.err` (~564 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_HiLoadStall.c.met` (~1781 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_HighFreqAssist.c.err` (~579 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_HighFreqAssist.c.met` (~1785 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_HwPwUp.c.err` (~842 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_HwPwUp.c.met` (~1818 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_HystComp.c.err` (~753 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_HystComp.c.met` (~1849 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_LmtCod.c.err` (~655 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_LmtCod.c.met` (~1800 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_LrnEOT.c.err` (~1039 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_LrnEOT.c.met` (~1857 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_MtrTempEst.c.err` (~621 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_MtrTempEst.c.met` (~1816 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_PICurrCntrl.c.err` (~718 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_PICurrCntrl.c.met` (~1885 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_PeakCurrEst.c.err` (~643 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_PeakCurrEst.c.met` (~1798 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Polarity.c.err` (~870 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Polarity.c.met` (~1609 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_PwrLmtFuncCr.c.err` (~1186 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_PwrLmtFuncCr.c.met` (~1946 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_QuadDet.c.err` (~578 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_QuadDet.c.met` (~1768 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Return.c.err` (~698 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Return.c.met` (~1814 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ReturnFirewall.c.err` (~773 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ReturnFirewall.c.met` (~1826 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_SignlCondn.c.err` (~653 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_SignlCondn.c.met` (~1779 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_SrlComInput.c.err` (~6245 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_SrlComInput.c.met` (~3851 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_SrlComOutput.c.err` (~7983 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_SrlComOutput.c.met` (~4515 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_StOpCtrl.c.err` (~804 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_StOpCtrl.c.met` (~1062 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_StaMd.c.err` (~1468 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_StaMd.c.met` (~3623 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_StabilityComp.c.err` (~877 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_StabilityComp.c.met` (~1853 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_StabilityComp2.c.err` (~567 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_StabilityComp2.c.met` (~1797 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Sweep.c.err` (~644 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Sweep.c.met` (~1469 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Sweep2.c.err` (~447 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_Sweep2.c.met` (~1436 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ThrmlDutyCycle.c.err` (~1195 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ThrmlDutyCycle.c.met` (~1937 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_TqRsDg.c.err` (~822 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_TqRsDg.c.met` (~1830 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_TrqCanc.c.err` (~843 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_TrqCanc.c.met` (~1985 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_TrqCmdScl.c.err` (~663 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_TrqCmdScl.c.met` (~1779 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_TuningSelAuth.c.err` (~1637 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_TuningSelAuth.c.met` (~2848 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_VehDyn.c.err` (~1287 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_VehDyn.c.met` (~1946 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_VehPwrMd.c.err` (~1096 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_VehPwrMd.c.met` (~1874 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_VehSpdLmt.c.err` (~509 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_VehSpdLmt.c.met` (~1774 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ePWM2.c.err` (~570 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Ap_ePWM2.c.met` (~1012 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/AppStartup.c.err` (~1863 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/AppStartup.c.met` (~1998 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/AppStartupCallout.c.err` (~4 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/AppStartupCallout.c.met` (~120 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/ApplCallbacks.c.err` (~2157 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/ApplCallbacks.c.met` (~2860 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/CDD_Data.c.err` (~551 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/CDD_Data.c.met` (~972 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_FeeIf.c.err` (~2505 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_FeeIf.c.met` (~1888 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_Nhet1.c.err` (~1225 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_Nhet1.c.met` (~2239 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_NvMProxy.c.err` (~1159 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_NvMProxy.c.met` (~1759 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagCCRM.c.err` (~577 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagCCRM.c.met` (~1561 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagClockMonitor.c.err` (~581 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagClockMonitor.c.met` (~1618 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagECC.c.err` (~805 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagECC.c.met` (~2530 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagESM.c.err` (~600 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagESM.c.met` (~1594 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagFPU.c.err` (~1920 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagFPU.c.met` (~1619 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagIOMM.c.err` (~583 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagIOMM.c.met` (~1588 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagLossOfExec.c.err` (~864 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagLossOfExec.c.met` (~2453 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagParity.c.err` (~583 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagParity.c.met` (~1658 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagResetHandler.c.err` (~434 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagResetHandler.c.met` (~937 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagStaticRegs.c.err` (~690 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagStaticRegs.c.met` (~1580 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagVIM.c.err` (~940 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Cd_uDiagVIM.c.met` (~2511 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/CheckSums.c.err` (~179 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/CheckSums.c.met` (~1332 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Dma.c.err` (~687 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Dma.c.met` (~1319 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EPS_DiagSrvcs_ISO.Customer.c.err` (~2116 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EPS_DiagSrvcs_ISO.Customer.c.met` (~3116 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EPS_DiagSrvcs_ISO.c.err` (~3455 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EPS_DiagSrvcs_ISO.c.met` (~3988 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EPS_DiagSrvcs_SrvcLUTbl.c.err` (~3143 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EPS_DiagSrvcs_SrvcLUTbl.c.met` (~3835 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EPS_DiagSrvcs_XCP.Vector.c.err` (~3229 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EPS_DiagSrvcs_XCP.Vector.c.met` (~3690 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EPS_DiagSrvcs_XCP.c.err` (~3299 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EPS_DiagSrvcs_XCP.c.met` (~3765 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EcuM_Callout_Stubs.c.err` (~1989 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EcuM_Callout_Stubs.c.met` (~1811 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EcuStartup.c.err` (~11089 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/EcuStartup.c.met` (~5412 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Fapi_UserDefinedFunctions.c.err` (~21 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Fapi_UserDefinedFunctions.c.met` (~181 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Fiasa_326_327_EPS_TMS570.err` (~182 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Fiasa_326_327_EPS_TMS570.met` (~308 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/FlsTst.c.err` (~905 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/FlsTst.c.met` (~1337 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/FlsTst_Irq.c.err` (~644 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/FlsTst_Irq.c.met` (~1601 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Interrupts.c.err` (~374 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Interrupts.c.met` (~1534 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/IoHwAb.c.err` (~1345 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/IoHwAb.c.met` (~1716 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/IoHwAbstractionUsr.c.err` (~1450 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/IoHwAbstractionUsr.c.met` (~2956 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/MtrCtrl_Irq.c.err` (~439 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/MtrCtrl_Irq.c.met` (~1741 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Nhet.c.err` (~810 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Nhet.c.met` (~2181 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Nhet2_ePWM_Prog.c.err` (~9 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Nhet2_ePWM_Prog.c.met` (~209 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Nhet_SENT_Prog.c.err` (~24 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Nhet_SENT_Prog.c.met` (~249 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/NtWrap.c.err` (~6422 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/NtWrap.c.met` (~4456 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/OsErrCallouts.c.err` (~371 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/OsErrCallouts.c.met` (~1517 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/PwmCdd.c.err` (~355 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/PwmCdd.c.met` (~1977 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/RednRpdShtdn.c.err` (~7 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/RednRpdShtdn.c.met` (~168 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/ResetCause.c.err` (~60 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/ResetCause.c.met` (~136 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/RteErrata10.c.err` (~413 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/RteErrata10.c.met` (~889 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/RteErrata8.c.err` (~413 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/RteErrata8.c.met` (~889 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/RteErrata9.c.err` (~413 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/RteErrata9.c.met` (~889 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_BkCpPc.c.err` (~1021 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_BkCpPc.c.met` (~1873 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_CDDInterface.c.err` (~2660 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_CDDInterface.c.met` (~3477 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_CmMtrCurr.c.err` (~1559 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_CmMtrCurr.c.met` (~2348 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_CtrlTemp.c.err` (~751 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_CtrlTemp.c.met` (~1805 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_DigHwTrqSENT.c.err` (~1316 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_DigHwTrqSENT.c.met` (~1962 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_DigMSB.c.err` (~1475 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_DigMSB.c.met` (~2344 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_MtrDrvDiag.c.err` (~1724 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_MtrDrvDiag.c.met` (~2610 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_MtrVel.c.err` (~822 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_MtrVel.c.met` (~1884 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_MtrVel2.c.err` (~767 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_MtrVel2.c.met` (~1844 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_MtrVel3.c.err` (~460 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_MtrVel3.c.met` (~1382 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_OvrVoltMon.c.err` (~773 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_OvrVoltMon.c.met` (~1798 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_ShtdnMech.c.err` (~657 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_ShtdnMech.c.met` (~943 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_TmprlMon.c.err` (~1657 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_TmprlMon.c.met` (~1969 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_TmprlMon2.c.err` (~413 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/Sa_TmprlMon2.c.met` (~890 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/SchM.c.err` (~8434 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/SchM.c.met` (~6335 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/SpiNxt.c.err` (~265 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/SpiNxt.c.met` (~272 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/SpiNxt_Irq.c.err` (~574 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/SpiNxt_Irq.c.met` (~1627 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/SystemTime.c.err` (~1442 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/SystemTime.c.met` (~1891 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/WdgResetHandler.c.err` (~1754 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/WdgResetHandler.c.met` (~1611 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/atan2_octants.c.err` (~60 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/atan2_octants.c.met` (~125 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/ePWM.c.err` (~769 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/ePWM.c.met` (~2132 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/filters.c.err` (~97 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/filters.c.met` (~231 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/interpolation.c.err` (~56 KiB)
- `Fiasa_326_327_EPS_TMS570/Tools/QAC/QAC Output/interpolation.c.met` (~616 KiB)

</details>
