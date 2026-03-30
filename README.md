📌 Overview

OWarning is an advanced EDR-lite security tool designed to detect early signs of credential dumping attacks on Linux systems. It monitors file activity, process behavior, and ptrace interactions to identify suspicious operations in real-time.

| Element                    | Description                                           |
| -------------------------- | ----------------------------------------------------- |
| **Real-Time Alerts**       | Displays detected threats with severity levels        |
| **Live Summary Dashboard** | Shows total alerts, severity distribution, and uptime |
| **Rule Hits Section**      | Detailed breakdown of triggered detection rules       |
| **ptrace Findings**        | Identifies processes attempting memory tracing        |
| **Log Output**             | Continuous monitoring logs and activity stream        |

⚙️ Requirements
Linux (any distro)
Root privileges (recommended for full monitoring)
Optional: psutil for enhanced process tracking
Pre-built executable (no Python installation required)

| Element                    | Description                                           |
| -------------------------- | ----------------------------------------------------- |
| **Real-Time Alerts**       | Displays detected threats with severity levels        |
| **Live Summary Dashboard** | Shows total alerts, severity distribution, and uptime |
| **Rule Hits Section**      | Detailed breakdown of triggered detection rules       |
| **ptrace Findings**        | Identifies processes attempting memory tracing        |
| **Log Output**             | Continuous monitoring logs and activity stream        |


🚀 Usage

Run the tool directly:

./OWarning



Basic Options
--summary → Enable live dashboard
--defensive → Enable active response (kill/quarantine)
--dry-run → Simulation mode (default)
--live → Execute real defensive actions
--watch DIR → Add custom directory to monitor


🧠 Detection Capabilities

OWarning uses multiple detection layers:

File Monitoring
Detects dump files (core, mem, shadow, etc.)
Monitors suspicious directories (/tmp, /dev/shm)
Process Analysis
Identifies tools like gdb, strace, dd
Detects suspicious command patterns
ptrace Detection
Flags processes tracing sensitive targets
/proc Abuse Detection
Monitors access to /proc/<pid>/mem and sensitive files
Correlation Engine
Links suspicious files to originating processes
🚨 Severity Levels
Level	Description
CRITICAL	Immediate threat detected
HIGH	Strong indicators of compromise
MEDIUM	Suspicious activity
LOW	Informational
🛡️ Defensive Actions

When enabled:

Kill Process → Terminates malicious processes
Quarantine File → Moves suspicious files to safe location
Dry-Run Mode → Logs actions without executing (default)
📦 Part of OwlSec Toolkit

This tool is part of the OwlSec ecosystem — a collection of 300+ cybersecurity tools.

🔗 owlsec.org

©️ License

MIT License — © Khaled S. Haddad
Distributed as a pre-built executable. Source code is proprietary.
