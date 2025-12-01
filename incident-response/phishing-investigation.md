# Phishing Investigation

## Overview
User reported a suspicious email claiming account deactivation. Email displayed several red flags.

## Red Flags Identified
- SPF: FAIL  
- DKIM: None  
- Display name mismatch  
- From domain: support-update@icloudverify.net  
- Link redirected to: hxxp://account-verify-portal.com/login  

## Technical Evidence
### Header Snippet### URL Behavior
Link leads to a credential harvesting page designed to mimic Apple login.

## Conclusion
Email classified as a malicious phishing attempt.

## Action Taken
- Blocked domain
- Notified user
- Submitted IOCs to threat feed
