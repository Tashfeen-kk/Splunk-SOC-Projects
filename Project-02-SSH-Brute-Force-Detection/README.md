# 🔐 Project 02 – SSH Log Analysis & Brute-Force Detection using Splunk

## 📌 Project Overview

This project focuses on analyzing SSH authentication logs using Splunk Enterprise to identify authentication activity, failed login attempts, suspicious source IP addresses, and potential brute-force behavior.

The SSH log dataset was ingested into Splunk and analyzed using SPL queries. A dedicated dashboard was created to provide a visual overview of SSH activity and support SOC investigation.

---

## 🎯 Objectives

- Analyze SSH authentication logs using Splunk
- Identify successful SSH logins
- Identify failed SSH login attempts
- Analyze login attempts by username
- Identify IP addresses generating repeated failed logins
- Investigate possible brute-force activity
- Visualize SSH activity through a Splunk dashboard
- Develop practical SOC investigation skills

---

## 🛠️ Tools & Technologies

- Splunk Enterprise
- SPL (Search Processing Language)
- SSH Logs
- SIEM
- Log Analysis
- Network Security
- SOC Monitoring
- Threat Detection

---

## 📊 Dashboard Overview

The Splunk dashboard provides visibility into SSH authentication activity.

### Dashboard Metrics

| Metric | Observed Events |
|---|---:|
| Total SSH Events | 1,200 |
| Successful SSH Login | 306 |
| Failed SSH Login | 305 |
| Connection Without Authentication | 286 |

> These values represent the activity displayed in the project dashboard screenshot.

---

## 📈 Dashboard Components

### 1. Total SSH Events

Displays the total number of SSH-related events analyzed.

### 2. Successful SSH Login

Shows successful SSH authentication activity.

### 3. Failed SSH Login

Shows failed SSH authentication attempts that may require investigation when occurring repeatedly.

### 4. Connection Without Authentication

Shows SSH connections observed without a successful authentication event.

### 5. Failed Login by Username

Visualizes usernames associated with failed login attempts.

This can help identify commonly targeted accounts.

### 6. Possible Brute Force by IP Address

Lists source IP addresses associated with repeated authentication failures.

Repeated attempts from a source IP may indicate possible brute-force behavior and should be investigated further.

### 7. Brute Force Attack with Geo-location

Provides geographic visualization of potentially suspicious SSH activity.

---

## 🖼️ Dashboard Screenshot

![SSH Logs Dashboard](Screenshots/ssh-dashboard.png)

---

## 🔍 Investigation Workflow

```text
SSH Logs
   ↓
Log Ingestion into Splunk
   ↓
Field Analysis
   ↓
SPL Queries
   ↓
Authentication Analysis
   ↓
Failed Login Analysis
   ↓
Source IP Analysis
   ↓
Brute-Force Investigation
   ↓
Dashboard Visualization
   ↓
Incident Documentation
