# SIEM Monitoring and Log Analysis

This section contains hands on SIEM investigations, log analysis exercises, and security detections created through my home SOC lab environment.

---

##  Objectives
- Identify suspicious authentication patterns  
- Analyze Windows event logs  
- Detect port scans and brute force attempts  
- Build simple Splunk queries  
- Document findings and create analyst reports  

---

## 📂 Contents
- **log-analysis-notes.md** – Written notes on log behavior, indicators of compromise, and alert observations  
- **splunk-searches.md** – Example SPL queries used for detection  
- **screenshots/** – Screenshots of dashboards, queries, and alerts  
- **incident-report.md** – Sample incident summary documenting a detected event  

---

##  Sample Splunk Queries

### **Failed login attempts by username**### **Possible brute force detection**### **Port scan detection**### ---

## Sample Incident Summary

**Incident Name:** Multiple Failed Login Attempts  
**Category:** Authentication Anomaly  
**Severity:** Medium  

**Summary:**  
A high number of failed authentication attempts were observed within a 3 minute period from a single IP address targeting multiple user accounts. Behavior is consistent with brute force activity.

**Indicators Observed:**  
- Repeated EventCode 4625 logs  
- Same source IP  
- Attempts across multiple user accounts  

**Action Taken:**  
- Source IP blocked  
- Account activity monitored  
- Logs escalated to Tier 2 for review  

---

## Skills Demonstrated
- SIEM Monitoring  
- SPL Query Creation  
- Threat Detection  
- Log Correlation  
- Incident Documentation  
- SOC Tier 1 Workflow  
