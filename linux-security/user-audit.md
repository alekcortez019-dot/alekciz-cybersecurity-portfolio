# Linux User Audit

## Overview
This document provides an audit of all users, groups, and privilege levels on a Linux system to identify unauthorized accounts or privilege escalation risks.

##  Commands Used---

##  Findings

### 1. Accounts with UID 0 (Root-Level Access)
- **root** — expected  
- **admin_shadow** — unexpected (requires investigation)  

### 2. Suspicious Accounts
- **tempbackup** — no login history, unclear origin  
- **legacy_user01** — deprecated account still active  

### 3. Weak Password Configuration
- Several accounts lack password expiration policy  
- No MFA enforcement  

## Recommendations
- Disable or remove unauthorized root-level account  
- Force password reset for legacy accounts  
- Enforce password aging policies  
- Enable MFA (if supported)  
- Review /etc/sudoers for misuse
