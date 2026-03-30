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
