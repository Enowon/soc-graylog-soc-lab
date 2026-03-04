# Detection Rules

Detection rules were created using Graylog Event Definitions to identify suspicious authentication activity.

## SSH Brute Force Detection

Query:
message:"Failed password"

Configuration:

- Search window: 5 minutes
- Trigger condition: count() > 10
- Group by: source

Purpose:
Detect repeated failed login attempts from the same IP address.

---

## Successful Login Monitoring

Query:
message:"Accepted password"

Purpose:
Monitor successful SSH logins, especially following multiple failed attempts.

---

## Sudo Activity Monitoring

Query:
message:"sudo"


Purpose:
Track privilege escalation activity on the system.

---

## Alert Notifications

When a rule is triggered, Graylog sends an email notification containing event details and timestamps. For each alert, a an email notification was created.
