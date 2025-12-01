# Packet Capture (PCAP) Analysis

##  Overview
This analysis focuses on suspicious network traffic captured in a PCAP file. The goal was to identify abnormal behavior, potential command and control traffic, or malicious communication patterns.

##  Key Observations

### 1. Repeated Outbound Connections
- Destination IP: 103.229.33.12  
- Frequency: Every 60 seconds  
- Size: ~120 bytes per packet  
- Protocol: HTTP  

**Interpretation:**  
This pattern strongly resembles beaconing behavior used by malware communicating with a C2 server.


### 2. Suspicious DNS Queries
- Randomized domain: `kjds92js9dk2.xyz`  
- TLD associated with malware campaigns  
- Multiple NXDOMAIN responses  

### 3. HTTP POST Activity
- Clear text credentials transmitted  
- Base64 encoded data observed in payload  
- Signs of possible data exfiltration  

##  Potential Indicators of Compromise (IOCs)
- **103.229.33.12** — suspicious foreign IP  
- **Encoded payloads** sent via POST  
- **Repetitive periodic traffic**  

##  Analyst Conclusion
Traffic likely associated with either:
- Malware beaconing  
- Unauthorized remote control activity  

System should be isolated and escalated for deeper forensic review.
