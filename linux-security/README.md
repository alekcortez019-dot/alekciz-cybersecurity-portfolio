#  Linux Security & System Hardening

This section contains Linux security configurations, system auditing exercises, user account investigations, and hardening practices commonly used in SOC and system administration environments.

---

##  Objectives
- Perform user and permission audits  
- Analyze system logs for suspicious activity  
- Harden Linux configurations  
- Identify unauthorized access  
- Practice real-world system security techniques  

---

##  Contents
- **user-audit.md** – review of users, groups, privileges  
- **log-review.md** – security-relevant log analysis  
- **hardening-steps.md** – system hardening procedures  
- **file-permissions.md** – permission review and corrections  
- **screenshots/** – screenshots of commands and outputs  

---

##  Basic User Audit Example

Commands used:**Findings:**
- Root account correctly configured  
- No unexpected users with UID 0  
- Several unused accounts discovered  

**Recommendation:**  
Disable or remove unused legacy accounts.

---

##  Log Review Example

Checked the following log files:**Suspicious Indicators:**
- Multiple failed login attempts from IP 192.168.1.200  
- Unauthorized sudo attempts  
- Unexpected cron job entries  

**Action Taken:**
- Blocked offending IP  
- Forced password reset for affected account  
- Removed unauthorized cron job  

---

##  Hardening Steps Example

Common system hardening includes:

- Disable root SSH login  
- Enforce SSH key authentication  
- Configure UFW firewall  
- Remove unnecessary packages  
- Secure file permissions on sensitive directories  
- Enable automatic security updates  

Example commands:---

##  Sample Analyst Summary

**Event:** Unauthorized sudo usage  
**Severity:** High  

**Summary:**  
System logs revealed repeated sudo attempts from an unprivileged user account during non-work hours. Attempts originate from the local machine and do not match authorized activity.

**Action Taken:**  
- Disabled account  
- Notified system administrator  
- Conducted full review of system logs  

---

##  Skills Demonstrated
- Linux Administration  
- System Hardening  
- Log Analysis  
- User Auditing  
- Security Configuration  
- SOC Reporting  
