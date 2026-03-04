# Graylog SOC Lab Setup

## Overview
This lab simulates a basic Security Operations Center (SOC) monitoring environment using Graylog. System authentication logs are collected, analyzed for suspicious behavior, and alerts are generated for security events.

## Environment

| Component | Version |
|----------|--------|
| Ubuntu | 22.04 LTS |
| Graylog | 4.3.15 |
| OpenSearch | 1.3.x |
| MongoDB | 7.0.x |
| Log Forwarding | rsyslog |

## Architecture

System Logs → rsyslog → Graylog Syslog TCP Input → Streams → Detection Rules → Alerts → Dashboard

Graylog processes incoming logs and stores them in OpenSearch for indexing and searching. MongoDB stores Graylog configuration data.

## Graylog Configuration

Main configuration file: /etc/graylog/server/server.conf

Important parameters configured:
password_secret
root_password_sha2
elasticsearch_hosts = http://127.0.0.1:9200
Graylog web interface: http://localhost:9000

## Log Ingestion
A **Syslog TCP input** was created in Graylog.
Port used: 5140
rsyslog was configured to forward logs to Graylog by adding the following line:
. @@127.0.0.1:5140
rsyslog service was then restarted.

## Email Alerts

Email notifications were configured using Gmail SMTP in the Graylog configuration file.

Alerts are triggered when detection rules identify suspicious activity.

## Dashboard

A monitoring dashboard was created to visualize:

- Failed SSH login attempts
- Successful logins
- Sudo activity
- Log source counts

