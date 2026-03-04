# soc-graylog-soc-lab
SOC monitoring lab built using Graylog, OpenSearch, and Ubuntu. Includes log ingestion, detection engineering, alerting, and dashboards.

## Project Overview

This project demonstrates a small Security Operations Center (SOC) monitoring environment built using **Graylog**. The lab collects system authentication logs, detects suspicious activities, generates alerts, and visualizes security events on a dashboard.

The objective of this project is to simulate real-world **security monitoring and detection engineering** tasks performed by SOC analysts.

---

## Technologies Used

- Graylog 4.3.15
- OpenSearch 1.3.x
- MongoDB 7.0
- Ubuntu 22.04
- rsyslog
- Gmail SMTP (Email Alerts)

---

## Key Features

- Centralized log collection
- SSH authentication monitoring
- Brute force attack detection
- Privilege escalation monitoring
- Email alert notifications
- Security dashboard visualization

---

## Detection Rules Implemented

1. SSH Brute Force Detection  
2. Successful SSH Login Monitoring  
3. Sudo Privilege Escalation Monitoring  

---

## Example Alerts

The system generates alerts when suspicious activity is detected such as:

- Multiple failed login attempts
- Multiple failed login attempts then a successful attempt from same IP address
- Successful login after brute-force attempts
- Unauthorized sudo activity

---

## Dashboard

The dashboard provides visualization of security activity including:

- Failed SSH login attempts
- Successful logins
- Sudo command activity
- Log source distribution

---

## Repository Structure


Graylog-SOC-Lab
│
├── README.md
├── documentation
│ ├── setup-process.md
│ ├── detection-rules.md
│ └── testing-scenarios.md
│
└── screenshots

---

## Skills Demonstrated

- Security monitoring
- Log analysis
- SIEM configuration
- Detection rule creation
- Alerting and incident detection
- SOC dashboard creation

---

## Future Improvements

- Add Windows event log monitoring
- Integrate threat intelligence feeds
- Implement log pipelines
- Add correlation rules

---

## Author

Faith Okonoboh
