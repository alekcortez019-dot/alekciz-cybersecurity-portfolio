# Escalation Report

##  Incident Summary
**Alert:** Suspicious PowerShell Execution  
**Host:** WKS-22-IT  
**User:** staff_jflores  
**Severity:** High  

A PowerShell process was observed executing with hidden window parameters and an encoded command, behavior commonly associated with malware, loader scripts, or unauthorized administrative activity.

---

##  Technical Evidence

###  Process Details- `-nop` disables PowerShell profiles  
- `-w hidden` hides execution window  
- `-encodedcommand` indicates obfuscated script  

###  Log Source
- Windows Event Log: Security + PowerShell  
- Event ID: 4104 (Script Block Logging)  
- Event ID: 4688 (Process Creation)  

### 💡 Additional Findings
- No change management request for PowerShell activity  
- User normally does not run PowerShell  
- Timestamp occurred outside normal business hours  

---

##  Analyst Assessment
Behavior highly suspicious due to:
- Obfuscation  
- Hidden execution  
- No legitimate reason found  
- Potential for malware execution or lateral movement  

---

##  Recommended Actions
1. **Isolate the host** from the network  
2. **Reset the user credentials** immediately  
3. Pull full memory dump and run volatility analysis  
4. Collect:
   - Prefetch files  
   - Registry autoruns  
   - PowerShell histories  
5. Escalate to Tier 3 or IR team for forensic review  

##  Escalation Status
**Escalated to:** Tier 2 / Incident Response  
**Reason:** Confirmed suspicious execution with possible malicious intent  
**Time Escalated:** 11:32 AM  
**Escalated By:** Alekciz Cortez  
