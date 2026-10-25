# 🦉 OCANBus

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
