---

# 2. `Documentation/SSH-Log-Analysis.md`

```markdown
# 📚 SSH Log Analysis Documentation

## 1. Objective

The objective of this project was to analyze SSH authentication logs using Splunk Enterprise and create a dashboard for SOC monitoring.

The investigation focused on authentication activity, failed logins, usernames, source IP addresses, and possible brute-force behavior.

---

## 2. Environment

### SIEM
Splunk Enterprise

### Log Source
SSH Authentication Logs

### Analysis
SPL-based log analysis and dashboard visualization.

---

## 3. Dashboard Metrics

The Splunk dashboard displayed:

- Total SSH Events: 1,200
- Successful SSH Login: 306
- Failed SSH Login: 305
- Connection Without Authentication: 286

---

## 4. Username Analysis

Failed SSH login attempts were analyzed by username.

This helps identify accounts that are repeatedly targeted during authentication attempts.

Observed usernames included:

- root
- backup
- alice
- admin
- test
- john.doe
- svc_user
- service
- dbadmin
- webmaster

---

## 5. Source IP Analysis

Source IP addresses were analyzed to identify systems generating repeated authentication attempts.

A high number of failed authentication attempts from one source may indicate possible password-guessing or brute-force behavior.

---

## 6. Brute-Force Detection Concept

The investigation considered the following indicators:

- Repeated failed SSH logins
- Multiple usernames targeted
- Repeated attempts from the same source IP
- High authentication frequency
- Failed attempts followed by a successful login

These indicators should be correlated with additional logs before confirming an attack.

---

## 7. Geographic Analysis

The dashboard included a geographic visualization of possible brute-force activity.

This provides additional context about the origin of source IP addresses.

Geolocation alone is not sufficient evidence of malicious behavior.

---

## 8. SOC Investigation Workflow

```text
Collect SSH Logs
      ↓
Ingest into Splunk
      ↓
Identify Relevant Fields
      ↓
Analyze Authentication
      ↓
Analyze Failed Logins
      ↓
Analyze Usernames
      ↓
Analyze Source IPs
      ↓
Review Geo-location
      ↓
Correlate Events
      ↓
Document Findings
