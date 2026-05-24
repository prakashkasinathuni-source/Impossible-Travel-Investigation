# Impossible Travel Investigation

This folder contains a SOC investigation of an "impossible travel" login detection scenario in a cloud environment.

---

## Overview

A user account showed successful login attempts from two geographically distant locations within a short time frame, triggering a high-severity identity security alert.

---

## What was analyzed

- Azure AD sign-in logs
- MFA authentication logs
- IP geolocation data
- Device and browser information
- SIEM correlation alerts

---

## Key Findings

- Login from India followed by Germany within minutes
- Suspicious session activity detected
- Likely credential compromise
- Sessions revoked after investigation

---

## Skills Demonstrated

- Cloud security monitoring
- Identity and access investigation
- SIEM log analysis
- Threat detection in Azure AD
- Incident response workflow
- IOC analysis

---

## MITRE ATT&CK

- T1078 – Valid Accounts  
- T1110 – Credential Access (possible compromise vector)

---

## Outcome

The compromised account was identified and secured before any further malicious activity occurred.

---

## Disclaimer

All data used in this investigation is fictional and created for educational and portfolio purposes only.
