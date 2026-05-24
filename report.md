# Impossible Travel Login Investigation

## Alert Description

A high-severity alert was triggered indicating an “impossible travel” scenario where a user account showed successful login attempts from two geographically distant locations within a very short time window.

This behavior is often associated with compromised credentials.

---

## Severity

High

---

## Detection Source

Microsoft Entra ID (Azure AD) / SIEM correlation

---

## Investigation Steps

1. Reviewed sign-in logs for the affected user account.
2. Identified login from Location A followed by Location B within minutes.
3. Checked IP addresses and geolocation data.
4. Verified whether MFA was triggered and successfully passed.
5. Analyzed device details and browser fingerprints.
6. Checked for suspicious mailbox or account activity.
7. Correlated login events in SIEM for additional anomalies.
8. Verified whether password reset occurred after detection.

---

## Logs Reviewed

- Azure AD Sign-in Logs
- Conditional Access Logs
- MFA Authentication Logs
- SIEM Correlation Events
- Endpoint Login Activity Logs

---

## Event Timeline

| Time | Location | Action |
|------|----------|--------|
| 10:15 IST | India | Successful login |
| 10:42 IST | Germany | Successful login |

---

## Indicators of Compromise (IOCs)

- User Account: johndoe@company.com  
- IP Address 1: 103.XX.XX.10 (India)  
- IP Address 2: 185.XX.XX.25 (Germany)  
- Device: Unknown browser session  

---

## MITRE ATT&CK Mapping

- T1078 – Valid Accounts  
- T1110 – Brute Force (possible credential compromise source)

---

## Root Cause

The user account credentials were likely compromised through an external phishing attack, allowing unauthorized access from two different geographic locations in a short time window.

---

## Containment Actions

- Forced password reset for affected user
- Revoked all active sessions
- Enabled MFA enforcement
- Blocked suspicious IP addresses
- Reviewed mailbox forwarding rules

---

## Final Conclusion

The incident was successfully contained before any evidence of data exfiltration or privilege escalation was observed.

However, the account was confirmed as compromised and secured through remediation actions.

---

## Recommendations

- Enforce MFA for all users
- Implement conditional access policies
- Block legacy authentication
- Improve phishing awareness training
- Monitor impossible travel alerts proactively
