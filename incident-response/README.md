#  Incident Response Investigations

This section includes documented incident response exercises, phishing investigations, alert triage workflows, and escalation reports modeled after real SOC Tier 1 analyst responsibilities.

---

## Objectives
- Identify indicators of compromise (IOCs)  
- Analyze suspicious email headers and attachments  
- Validate alerts using log sources and evidence  
- Escalate incidents using proper SOC workflow  
- Produce clear, structured IR documentation  

---

##  Contents
- **phishing-investigation.md** – analysis of suspicious emails, headers, links, and IOCs  
- **alert-triage.md** – sample workflow for validating alerts  
- **escalation-report.md** – sample escalation to Tier 2  
- **ioc-list.md** – list of known malicious hashes, IPs, and domains  
- **screenshots/** – investigation screenshots to support findings  

---

##  Phishing Email Investigation Example

**Suspicious Indicators Found:**
- Display name mismatch  
- External sender warning triggered  
- SPF authentication failure  
- IP address flagged on VirusTotal  
- Embedded link redirecting to credential harvesting page  

**Header Analysis Snippet:****Decision:**  
Alert classified as *Malicious Phishing Attempt*

**Action Taken:**  
- Blocked sender domain  
- Quarantined email  
- Notified end user  
- Documented IOCs  

---

##  Basic Alert Triage Workflow

1. **Validate the alert**  
   - Review event logs  
   - Confirm legitimacy  

2. **Collect evidence**  
   - Host logs  
   - Network logs  
   - Endpoint status  

3. **Analyze impact**  
   - Does the event match malicious behavior patterns?  

4. **Escalate if needed**  
   - Provide summary  
   - Attach evidence  
   - Recommend containment steps  

5. **Document everything**  
   - SOC documentation  
   - IR summary report  

---

##  Sample Escalation Summary

**Alert:** Possible credential compromise  
**Source:** SIEM authentication logs  
**IOC:** Repeated login failures from single foreign IP  
**Severity:** High  

**Summary:**  
Multiple failed login attempts for a privileged account detected over 2 minutes from an IP located in a high-risk region. Behavior consistent with brute force activity.

**Recommended Action:**  
- Reset affected account credentials  
- Block source IP  
- Enable MFA if not already enforced  

---

##  Skills Demonstrated
- Incident Triage  
- Phishing Analysis  
- IOC Identification  
- Documentation  
- Escalation Procedures  
- SOC Analyst Methodology  
