## 📌 Overview
**OWarning** is a lightweight EDR-Lite tool designed to detect credential dumping attempts on Linux systems in real-time. It monitors file creation/modification in staging directories, correlates processes with suspicious files, detects ptrace/TracerPid activity on sensitive processes, and identifies direct /proc/<pid>/mem access.

---
## 🛡️ Detection Capabilities
- **File-based detection** — Suspicious dump files (core, .dmp, shadow-like names)
- **Process correlation** — Links newly created files to their creating processes
- **ptrace / TracerPid monitoring** — Detects debugging/tracing on sensitive processes (sshd, sudo, gnome-keyring, etc.)
- **ProcFS access monitoring** — /proc/<pid>/mem and /proc/<pid>/maps access
- **Command-line pattern matching** — gdb -p, gcore, dd if=/proc, etc.
- **Scoring engine** with severity levels (LOW → CRITICAL)

---
## 🖥️ Features
- Real-time inotify monitoring on `/tmp`, `/var/tmp`, `/dev/shm`
- Live process snapshot + open files correlation
- SQLite + JSONL + plain text logging
- Optional defensive mode (quarantine + process kill on CRITICAL)
- Clean colored terminal output + optional live summary dashboard
- Low resource footprint

---
## ⚙️ Requirements
- Linux (x86_64 / aarch64)
- Python 3.8+
- `psutil` package (`pip install psutil`)
- Root or sufficient privileges recommended for full ptrace and /proc access

---
## 🚀 Quick Start

### 1. Install dependencies
```bash
pip install psutil

Argument,Description
--summary,Show live summary dashboard every 5 seconds
--defensive,Enable defensive mode (kill/quarantine on CRITICAL)
--live,Disable dry-run (execute real actions)
--dry-run,Force dry-run mode (default)
--threshold LEVEL,Minimum severity: LOW | MEDIUM | HIGH | CRITICAL
--watch DIR,Add extra directory to watch
--no-sqlite,Disable SQLite logging
--interval N,File scan interval in seconds
--ptrace-interval N,ptrace scan interval in seconds


⚠️ Requirements

Linux (any modern distribution)
Root privileges (recommended for full visibility)
The tool is provided as a pre-built standalone executable

Note: No Python or additional packages needed on the target system.


📦 Part of OwlSec Toolkit
This tool is part of the OwlSec suite — a collection of 300+ security and privacy tools.
🔗 owlsec.org

©️ License
MIT License — © Khaled S. Haddad
Tools are distributed as pre-built executables. Source code is proprietary


