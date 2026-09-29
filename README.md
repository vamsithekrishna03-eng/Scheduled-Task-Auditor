# Scheduled Task Auditor (PowerShell)

## Overview
This script is a Blue Team reconnaissance and endpoint security tool built for the Graysentinel Global Cybersecurity Sprint. It automates the enumeration of Windows scheduled tasks to detect potential persistence mechanisms used by attackers (such as executing scripts from temporary directories or utilizing encoded PowerShell commands).

## Features
- Enumerates all non-default Windows scheduled tasks.
- Inspects underlying execution paths and arguments.
- Flags indicators of compromise like execution from `\Temp\`, `\AppData\`, or usage of base64 encoding (`-enc`).
- Generates a structured audit report (`Scheduled_Task_Audit_Report.txt`).

## Usage
1. Open PowerShell as **Administrator**.
2. Run the script:
   ```powershell
   .\src\scheduled_task_auditor.ps1
