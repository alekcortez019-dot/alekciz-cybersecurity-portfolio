# 🌐 Network Traffic Analysis

This section contains packet captures, traffic analysis exercises, and investigations using Wireshark to identify anomalies, suspicious behavior, and potential indicators of compromise within network traffic.

---

## 📌 Objectives
- Analyze packet captures using Wireshark  
- Identify malicious or abnormal traffic  
- Understand common protocols (TCP, UDP, DNS, HTTP, ARP)  
- Detect scanning behavior, beaconing, and suspicious patterns  
- Document findings and produce analyst summaries  

---

## 📂 Contents
- **pcap-analysis.md** – written breakdown of packet captures  
- **protocol-breakdowns.md** – explanations of key protocols and how they behave  
- **malicious-traffic.md** – detection of suspicious traffic patterns  
- **screenshots/** – Wireshark screenshots supporting analysis  

---

## 🧪 Example Traffic Analysis

### **Suspicious Beaconing Behavior**
**Indicators:**
- Repeated outbound connections to the same IP every 60 seconds  
- Small packet size (often 80–150 bytes)  
- Consistent timing patterns  

**Possible Explanation:**  
This behavior resembles command and control (C2) beaconing.

---

### **HTTP Traffic Review**
**Findings:**
- Unencrypted login form submissions  
- Internal IP addresses exposed in headers  
- Possible data exfiltration via POST requests  

**Recommendation:**  
Implement HTTPS enforcement and review server-side logs.

---

### **DNS Analysis**
**Suspicious Indicators:**
- Long or randomly generated domain names  
- Multiple failed DNS lookups  
- Frequent DNS queries to foreign TLDs  

Example:---

## 🛠 Tools Used
- Wireshark  
- TCPDump  
- Packet Capture Files (PCAP)  

---

## 📝 Sample Analyst Summary

**Event:** Suspicious outbound traffic  
**Severity:** Medium  
**Summary:**  
Continuous outbound connections detected from host 192.168.1.45 to an IP registered in a high risk region. Timing behavior indicates potential automated beaconing.

**Action Taken:**  
- Captured packets for further review  
- Flagged host in SIEM  
- Recommended isolation for deeper forensics  

---

## ✅ Skills Demonstrated
- Packet Analysis  
- Wireshark Investigation  
- Protocol Understanding  
- Traffic Pattern Recognition  
- SOC Documentation  
- Threat Hunting Fundamentals  
