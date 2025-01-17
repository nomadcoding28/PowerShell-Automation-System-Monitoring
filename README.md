# PowerShell Automation for System Monitoring

This repository contains a set of PowerShell scripts for automating system monitoring tasks on macOS. The scripts monitor system resources like CPU usage, memory usage, and disk space, and they can be automated to run at regular intervals.

## Features

- **CPU Monitoring**: Checks the current CPU usage and provides a warning if the usage exceeds a specified threshold.
- **Memory Monitoring**: Monitors system memory usage and warns if memory usage is too high.
- **Disk Space Monitoring**: Tracks available disk space and sends a warning if space is low.
- **Automated Monitoring**: A central script to automate the running of CPU, memory, and disk space monitoring tasks at regular intervals.

## Prerequisites

- PowerShell Core installed on your macOS system.
  - PowerShell can be installed via Homebrew (`brew install --cask powershell`).

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/PowerShell-Automation-System-Monitoring.git
   cd PowerShell-Automation-System-Monitoring
   ```
2. Ensure PowerShell is installed on your system. You can test it by running:
  ```bash
  pwsh
  ```
3.Make sure the scripts are executable. You can do this by setting the execute permission:
```
chmod +x *.ps1
```
## Setting Up a Cron Job for Automation
1. Open your crontab file for editing:
2. Add a cron job to run the automation script every hour:
```bash
crontab -e
0 * * * * pwsh /path/to/your/scripts/automated_monitoring.ps1 >> /path/to/log/monitoring.log 2>&1
```





