# Python and Splunk Brute Force Lab 

SOC laboratory project using Python and Splunk Enterprise to detect brute force attacks through log analysis and automated alert generation.

## Overview

This project simulates authentication attacks and demonstrates a basic Security Operations Center (SOC) detection workflow.

The goal is to identify multiple failed login attempts from the same IP address, generate a security alert, and investigate the event using Splunk Enterprise.

## Technologies Used

- Python
- Splunk Enterprise
- Kali Linux
- SPL (Search Processing Language)

## Project Workflow

```
Authentication Logs
        |
        v
Python Detection Script
        |
        v
Brute Force Alert Generation
        |
        v
Splunk Enterprise Investigation
```

## Detection Scenario

The Python script analyzes authentication logs and identifies repeated failed login attempts.

Detection rule:

- Monitor failed login events.
- Count attempts by IP address.
- Generate an alert when the threshold is reached.

Example generated alert:

```
[ALERTA] brute force detectado - IP: 192.168.1.10 - Tentativas: 5
```

## Project Structure

```
python-and-splunk-bruteforce-lab/

├── detector.py
├── attacks2.log
├── alertas_soc.log
│
├── screenshots/
│   ├── terminal-detector.png
│   └── splunk-bruteforce-alert.png
│
└── splunk/
    └── queries.txt
```

## Splunk Investigation

The generated alerts were indexed in Splunk Enterprise for analysis.

Query used:

```
index="security_lab" source="/home/linace/alertas_soc.log" "brute force"
```

## Evidence

Screenshots demonstrating the detection workflow are available in the `screenshots` folder:

- Python script execution
- Generated SOC alert
- Splunk investigation result

## Skills Demonstrated

- Log analysis
- Python automation
- SIEM investigation
- Splunk queries
- Security monitoring
- Brute force detection
