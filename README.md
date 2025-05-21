# SOC Analyst Home Lab: Kali, Ubuntu & Splunk

This project simulates a functional SOC analyst workflow using Kali Linux, Ubuntu, and Splunk Enterprise. It demonstrates how attacks are generated, detected, and analyzed using open-source and enterprise-grade tools.

## Objectives

- Simulate basic cyberattacks using Kali Linux
- Collect system and security logs from Ubuntu
- Analyze logs and detect threats using local Splunk
- Practice building detection rules and triage reports
- Understand foundational SOC workflows and tooling

## Lab Setup

- **Virtualization Platform**: VirtualBox
- **Network Type**: Internal-only
- **Machines**:
  - Kali Linux: Attack simulation
  - Ubuntu Desktop: Target endpoint
  - Splunk Enterprise: Installed on Ubuntu or another Linux VM

## Tools Used

- **Kali Linux**: Nmap, Hydra, Nikto
- **Ubuntu**: SSH, UFW, Fail2ban, Syslog
- **Splunk Enterprise**: Installed locally, used as SIEM
- **Splunk Universal Forwarder**: Installed on Ubuntu, sends logs to Splunk

## Workflow Overview

1. Install and configure Splunk Enterprise on a VM
2. Install Splunk Universal Forwarder on Ubuntu and forward logs
3. Launch attacks from Kali (e.g., Nmap scan, SSH brute force via Hydra)
4. Analyze incoming logs in Splunk (search queries, dashboards)
5. Build detection use cases (SSH brute force, port scans, failed logins)

## Detection Use Cases

- Multiple failed SSH login attempts from the same IP (Brute force)
- Port scan detection from Nmap probes
- Unauthorized root/sudo usage
- Failed login trends over time
