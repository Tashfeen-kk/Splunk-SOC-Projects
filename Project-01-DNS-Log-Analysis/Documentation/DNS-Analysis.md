# 📚 DNS Log Analysis – Technical Documentation

## 1. Project Objective

The objective of this project was to analyze DNS logs using Splunk Enterprise and transform raw log data into useful information for SOC monitoring and investigation.

---

## 2. Data Source

A DNS log dataset was imported into Splunk for analysis.

The following fields were analyzed:

- query
- src_ip
- dst_ip
- count

---

## 3. DNS Query Analysis

The DNS query field was analyzed to identify frequently occurring DNS requests.

This provides visibility into the domains being requested within the dataset.

---

## 4. Source IP Analysis

Source IP addresses were analyzed to determine which hosts were generating DNS requests.

This can help a SOC analyst identify hosts with unusually high DNS activity.

---

## 5. Destination IP Analysis

Destination IP addresses were analyzed to identify the endpoints associated with DNS traffic.

---

## 6. Query Correlation

A table was created to correlate:

| Field | Purpose |
|---|---|
| Query | Requested DNS domain |
| Source IP | Host generating the request |
| Destination IP | Destination associated with the DNS traffic |
| Count | Number of observed events |

---

## 7. Dashboard

A Splunk dashboard was created to provide a visual overview of the DNS activity.

The dashboard includes DNS query and IP-based analysis.

---

## 8. SOC Use Case

DNS monitoring can provide useful visibility during security investigations.

A SOC analyst can investigate:

- High-volume DNS activity
- Unusual DNS queries
- Unexpected source hosts
- Unexpected destinations
- Repeated DNS requests

Further investigation and correlation with other security sources would be required before classifying activity as malicious.

---

## 9. Investigation Workflow

DNS Logs
    ↓
Splunk Ingestion
    ↓
Field Analysis
    ↓
SPL Queries
    ↓
DNS Query Analysis
    ↓
Source/Destination IP Analysis
    ↓
Dashboard
    ↓
SOC Investigation

---

## 10. Conclusion

This project provided hands-on experience with Splunk Enterprise, SPL, DNS log analysis, IP analysis, visualization, and SOC-focused investigation.
