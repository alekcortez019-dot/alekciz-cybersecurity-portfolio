# Malicious Traffic Indicators

##  DNS Indicators
- Queries for long, random domain names  
- Repeated requests to:
  - `jdk2983jds2.xyz`
  - `rerangehostmail.info`
- Multiple NXDOMAIN responses indicate domain generation algorithm (DGA) behavior.

---

##  HTTP Indicators
- POST requests containing encoded blobs  
- Credentials transmitted in clear text  
- User agent strings inconsistent with normal browser traffic  

Example:---

##  Network Behavior
- High volume of outbound traffic to foreign IPs  
- Regular periodic connections every 30 to 90 seconds  
- Possible C2 beaconing behavior  

---

##  Analyst Notes
The traffic patterns, combined with DGA-like DNS behavior, strongly suggest malware or botnet activity on the affected host.  
Immediate host isolation is recommended.
