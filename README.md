# 🦉 OWarning

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OWarning** — Credential Dumping Early Warning ║

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OWarning is a security alerting and notification tool that evaluates findings against configurable thresholds and dispatches warnings to a chosen destination. It normalizes events from other tools, applies severity rules and deduplication, and relays concise alerts. It is intended for authorized defensive monitoring pipelines.

---

## ✨ Features


- Threshold-based evaluation of security findings and events
- Severity rules with deduplication to reduce alert noise
- Relay of alerts to a configured notification endpoint
- Normalization of events from multiple tool sources
- Structured log/export of dispatched warnings
- Offline --self-test for safe verification

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OWarning
./OWarning --self-test
./OWarning --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
