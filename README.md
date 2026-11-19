# Home SIEM & SOC Investigation: Incident #46
A hands-on home lab project simulating a Tier-1 SOC investigation. This project demonstrates end-to-end threat detection, log ingestion, and incident triage using Microsoft Sentinel, Azure Log Analytics, and Sysmon.

## Project Architecture
1. **Endpoint:** Windows host running Sysmon to capture process creation events (Event ID 1).
2. **Collection & Ingestion:** Azure Monitor Agent (AMA) sending event data to an Azure Log Analytics workspace (`law-sentinel-lab`).
3. **Detection & Triage:** Custom Microsoft Sentinel analytics rule detecting `whoami.exe` execution (MITRE ATT&CK: T1033 - Discovery) and generating an incident in the Microsoft Defender portal.

## Repository Contents

## Key Findings
* **Event:** User discovery (`whoami`) command executed via PowerShell.
* **Verdict:** True Positive — Benign Testing (Authorized Lab Simulation).
**Takeaway:** Successfully validated the end-to-end pipeline and identified future detection improvements.
