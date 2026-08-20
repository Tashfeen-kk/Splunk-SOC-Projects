---

# 3. `Incident-Report.md`

```markdown
# 🚨 SSH Authentication Investigation Report

## 1. Incident Type

SSH Authentication Monitoring / Possible Brute-Force Activity

---

## 2. Detection Platform

Splunk Enterprise

---

## 3. Severity

**Medium – Investigation Required**

---

## 4. Executive Summary

SSH authentication logs were analyzed using Splunk Enterprise to identify potentially suspicious authentication patterns.

The dashboard contained:

- 1,200 total SSH events
- 306 successful SSH logins
- 305 failed SSH logins
- 286 connections without authentication

The investigation also identified usernames associated with failed login activity and source IP addresses associated with possible brute-force behavior.

---

## 5. Findings

### Finding 1 – Failed Authentication

A large number of failed SSH authentication events were observed.

Further investigation is required to determine whether the activity represents normal behavior, configuration issues, or password-guessing activity.

---

### Finding 2 – Targeted Accounts

Multiple usernames appeared in failed authentication activity.

Examples include:

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

### Finding 3 – Source IP Activity

Multiple source IP addresses were associated with possible brute-force activity.

Repeated authentication attempts from the same source should be investigated further.

---

### Finding 4 – Geographic Context

A geographic visualization was used to provide additional context for the observed source IP activity.

Geolocation is supporting evidence and does not independently confirm malicious activity.

---

## 6. Possible Attack Scenario

```text
Source IP
   ↓
Multiple SSH Login Attempts
   ↓
Multiple Usernames Targeted
   ↓
Authentication Failures
   ↓
Possible Password Guessing
   ↓
Potential Successful Login
   ↓
Further Investigation
