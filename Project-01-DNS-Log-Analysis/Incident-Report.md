# 🚨 DNS Investigation Report

## 1. Investigation Type

DNS Traffic Analysis

## 2. Investigation Platform

Splunk Enterprise

## 3. Objective

Analyze DNS activity and identify notable patterns in DNS queries, source IP addresses, destination IP addresses, and event frequency.

---

## 4. Data Reviewed

The investigation analyzed DNS log data containing:

- DNS Query
- Source IP
- Destination IP
- Event Count

---

## 5. Investigation Process

### Step 1 – Log Ingestion

The DNS log dataset was imported into Splunk Enterprise.

### Step 2 – DNS Query Analysis

DNS queries were analyzed to identify frequently occurring requests.

### Step 3 – Source IP Analysis

Source IP addresses were analyzed to identify hosts generating DNS requests.

### Step 4 – Destination IP Analysis

Destination IP addresses were analyzed to understand DNS traffic destinations.

### Step 5 – Correlation

DNS queries were correlated with source IPs, destination IPs, and event counts.

### Step 6 – Visualization

The results were presented through a Splunk dashboard.

---

## 6. Findings

The analysis provided visibility into:

- Frequently occurring DNS queries
- Source IP activity
- Destination IP activity
- DNS event frequency

---

## 7. Security Assessment

DNS activity can be useful during SOC investigations because abnormal DNS behavior may require additional investigation.

However, the analyzed dataset alone does not establish confirmed malicious activity.

---

## 8. Recommended SOC Actions

If suspicious DNS activity is identified:

1. Investigate the source host.
2. Review the queried domain.
3. Check domain reputation.
4. Correlate DNS activity with endpoint logs.
5. Review firewall/network logs.
6. Investigate related processes and connections.
7. Escalate the event if malicious indicators are confirmed.

---

## 9. Conclusion

The investigation demonstrated how Splunk can be used to analyze DNS logs, correlate network information, and provide visibility useful for SOC monitoring and investigation.
