# SIEM Dashboard Project

A Security Information and Event Management (SIEM) project built using the Elastic Stack to collect, process, visualize, and monitor security-related login events.

## Project Overview

This project demonstrates a basic SIEM pipeline for detecting and monitoring failed authentication attempts.

Security events are collected from a log file, processed using Logstash, stored in Elasticsearch, and visualized through Kibana dashboards.

## Architecture

```text
Security Log
     |
     v
  Logstash
     |
     v
Elasticsearch
     |
     v
   Kibana
     |
     v
Dashboard & Security Monitoring
## Technologies Used

- Elasticsearch
- Logstash
- Kibana
- Ubuntu Linux
- VMware
- Git & GitHub

## Features

- Failed login monitoring
- Username monitoring
- Source IP monitoring
- Security log ingestion
- Log parsing with Logstash
- Elasticsearch data storage
- Kibana dashboard visualization
- Security alert rule

## Log Source

The project uses:

`security.log`

Example security events:

```text
Failed password for root from 192.168.1.10
Failed password for admin from 192.168.1.20
Failed password for attacker from 192.168.1.99
## Detection Example

The SIEM dashboard can be used to identify:

- Repeated failed login attempts
- Suspicious source IP addresses
- Targeted usernames
- Authentication failures

Example:

```text
User: root
Source IP: 192.168.1.10
Event: Failed password
## Screenshots

Project screenshots are available in the `screenshots/` directory.

They demonstrate the SIEM dashboard, security events, and monitoring configuration.
## How It Works

1. Security events are written to `security.log`.
2. Logstash reads and processes the events.
3. Logstash extracts important fields such as username and source IP.
4. Processed events are sent to Elasticsearch.
5. Elasticsearch stores the security events.
6. Kibana retrieves and visualizes the data.
7. Dashboard and alert rules help monitor suspicious authentication activity.
## Project Files

```text
SIEM-project/
├── README.md
├── siem.conf
├── security.log
└── screenshots/
