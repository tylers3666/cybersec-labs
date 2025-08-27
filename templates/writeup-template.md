# <Title / Machine / Room Name>
**Date:** YYYY-MM-DD  
**Platform:** TryHackMe / HTB / CTF  
**Difficulty:** easy/medium/hard  
**TL;DR:** One-paragraph summary of scope + outcome

---

## Summary & Impact
- Short description of what I accomplished and why it matters.
- CVSS (if appropriate): e.g., CVSSv3: 6.5 (Medium)

---

## Scope & Setup
- Target (sanitized): `target: [REDACTED]`
- Tools used (high-level): e.g., enumeration tools, browser, Burp suites, disassembler
- Environment: local VM/homelab notes

---

## Methodology (high-level)
### Recon
- Summarize the discovery: “Found a web application with an unauthenticated endpoint that accepted user input and returned server-side errors.”  

### Exploitation (sanitized)
- Explain the vulnerability class and why it was exploitable (e.g., improper input validation; missing bounds checks).
- Provide sanitized steps: “Sent crafted request to endpoint; server returned stack trace revealing path X.” Avoid detailed commands.

### Privilege Escalation (if applicable)
- Summarize how I moved from user → admin (high-level only).
- Describe the learning point (e.g., misconfigured service allowed local file inclusion).

---

## Remediation
- Short bullet list of fixes for a developer or admin (input validation, auth checks, patch versions).

---

## Lessons learned & next steps
- What you learned technically.
- Follow-up labs or topics to study.

---

## Appendices (optional & sanitized)
- Screenshots (redact sensitive info)
- Pseudocode snippets (do not publish exploit payloads)
