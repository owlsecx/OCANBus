# 🦉 OCANBus

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OCANBus** — part of the OwlSec Toolkit.

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OCANBus analyzes CAN bus captures from your own vehicle or test bench. It reads candump, SavvyCAN and ASCII logs (including 29-bit and CAN-FD frames), decodes signals using a DBC database and profiles every arbitration ID. Its anomaly engine flags flooding, injection and diagnostic activity. It reads capture files only and never writes to a bus.

---

## ✨ Features

- Reads candump, candump -L logs, ASCII ID#DATA, SavvyCAN CSV, 29-bit extended IDs and CAN-FD
- DBC parser with Intel/Motorola bit layouts, scale/offset, units and value tables
- Per-ID statistics: message counts, period, DLC and bus load
- Anomaly engine: ID flooding, unknown IDs, cadence breaks, counter stalls, payload entropy, DLC changes and security-access attempts
- UDS and OBD-II decoder (services, negative response codes, PIDs)
- Arbitration ID map, ASCII bus timeline and TXT/JSON/MD/CSV/SARIF reports

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OCANBus                                    # interactive menu
./OCANBus --file candump.log --stats
./OCANBus --file candump.log --anomalies
./OCANBus --file candump.log --decode --dbc vehicle.dbc
./OCANBus --file candump.log --uds
```

Run `./OCANBus --help` for the full list of options.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, the Go toolchain version it was built with, and every bundled
  component with its exact version and license. Feed it to Grype, Trivy or
  Dependency-Track to audit our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
