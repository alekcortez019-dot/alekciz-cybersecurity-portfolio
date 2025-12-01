# Alert Triage Process

This document outlines the workflow used to validate alerts, collect evidence, and determine whether escalation is needed within a SOC environment.

---

## Triage Steps

### 1. Validate the Alert
- Confirm event is real, not a false positive  
- Check event source: SIEM, EDR, firewall, or authentication logs  
- Verify the timestamp and affected user or system  

### 2. Gather Evidence
- Review related log entries  
- Check endpoint behavior  
- Look for unusual network traffic  
- Collect screenshots or extracted data  

### 3. Identify IOCs
Indicators may include:
- Suspicious IP addresses  
- Malicious file hashes  
- Anomalous login locations  
- Unusual PowerShell or CMD execution  

### 4. Determine Severity
Severity depends on:
- Privilege level of user account  
- Type of activity detected  
- Whether data was accessed or modified  

### 5. Escalate if Needed
Escalate to Tier 2 if:
- Malicious scripts are executed  
- There is confirmed compromise  
- Privileged accounts are involved  
- Data exfiltration is suspected  

### 6. Document Everything
- What triggered the alert  
- What log sources were reviewed  
- What conclusions were reached  
- Recommended action  

---

##  Example Alert

**Alert:** Suspicious login from unusual location  
**User:** jperez  
**IP:** 201.11.223.19  
**Behavior:** Login attempt followed by quick logout  

### Analyst Notes
- No prior logins from this region  
- User confirmed no travel  
- Behavior flagged as suspicious  

### Status:  
**Escalated to Tier 2**  
