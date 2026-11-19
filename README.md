# Home SIEM & SOC Investigation: Incident #46
A hands-on home lab project simulating a Tier-1 SOC investigation. This project demonstrates end-to-end threat detection, log ingestion, and incident triage using Microsoft Sentinel, Azure Log Analytics, and Sysmon.

## Project Architecture
1. **Endpoint:** Windows host running Sysmon to capture process creation events (Event ID 1).
2. **Collection & Ingestion:** Azure Monitor Agent (AMA) sending event data to an Azure Log Analytics workspace (`law-sentinel-lab`).
3. **Detection & Triage:** Custom Microsoft Sentinel analytics rule detecting `whoami.exe` execution (MITRE ATT&CK: T1033 - Discovery) and generating an incident in the Microsoft Defender portal.

## Repository Contents
* **[Tier-1 SOC Investigation Report_ Incident #46.pdf](./Tier-1%20SOC%20Investigation%20Report_%20Incident%20%2346.pdf)** — Full investigation report, including screenshots
* **[artifacts/](./artifacts/)** — Portal exports and raw data (`Case_46.pdf` and `Raw_Data.pdf`).

## Key Findings
* **Event:** User discovery (`whoami`) command executed via PowerShell.
* **Verdict:** True Positive — Benign Testing (Authorized Lab Simulation).
* **Takeaway:** Successfully validated the end-to-end pipeline and identified future detection improvements.
