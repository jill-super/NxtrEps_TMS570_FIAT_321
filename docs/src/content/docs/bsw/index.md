---
title: "Basic Software — Services"
description: "Memory, NVRAM and platform services: TI FEE/Flash, Nexteer NvM wrappers."
---


# Basic Software — Services

Memory, NVRAM and platform services: TI FEE/Flash, Nexteer NvM wrappers.

This layer contains **4** module(s).

| Module | Origin | Purpose |
| --- | --- | --- |
| [Flash EEPROM Emulation Driver (Texas Instruments)](./Fee/) | Third-party — Texas Instruments (adapted) | This file implements the Autosar FEE 3.1 Api's. |
| [Flash Memory Driver (TI F021 Flash API)](./Fls/) | Third-party — Texas Instruments | ARM compiler specific info used by the F021 API. |
| [NVRAM Manager (FEE Interface)](./NvMMgr/) | Custom — Nexteer in-house | This module contains the specific interfacing functions that are needed for TI’s Fee Driver. |
| [NVRAM Proxy](./NvMProxy/) | Custom — Nexteer in-house | Complex Driver NvMProxy which acts as a proxy between |
