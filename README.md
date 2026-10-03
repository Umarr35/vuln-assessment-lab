[README.md](https://github.com/user-attachments/files/33001149/README.md)
# Vulnerability Assessment Lab — Metasploitable 2

A hands-on vulnerability assessment conducted against Metasploitable 2 in an isolated home lab environment, combining automated scanning (Nessus) with manual exploitation to validate findings — simulating the workflow of a junior penetration tester / vulnerability analyst.

## Lab Setup

- **Attacker machine:** Kali Linux (VirtualBox)
- **Target:** Metasploitable 2 (VirtualBox)
- **Network:** Isolated VirtualBox host-only network — no internet or external network exposure, by design

## Tools Used

- **Nmap** — reconnaissance and port/service enumeration
- **Nessus Essentials** — automated vulnerability scanning
- **Metasploit Framework** — exploitation
- **netcat, smbclient, TigerVNC Viewer** — manual verification

## Process

1. Built and isolated the lab network (VirtualBox host-only adapter)
2. Ran Nmap reconnaissance (basic, service/version, and full port scans)
3. Ran a Nessus vulnerability scan to identify CVEs and CVSS severity scores
4. Manually verified 6 of the highest-severity findings through direct exploitation — not just relying on scanner output
5. Documented everything in a formal report with evidence, impact analysis, and remediation guidance

## Key Findings

10 vulnerabilities were identified, 6 confirmed through manual exploitation — including **three that granted full unauthenticated root access** to the system (vsftpd 2.3.4 backdoor, an open bind shell, and a weak VNC password). Full details, evidence, and remediation steps are in the report below.

## Repo Contents

- [`report/`](report/) — full vulnerability assessment report (PDF)
- [`scans/`](scans/) — raw Nmap scan output
- [`evidence/`](evidence/) — screenshots from manual verification
- [`diagram/`](diagram/) — network diagram

## Report

📄 [Full Vulnerability Assessment Report](report/vulnerability_assessment_report.pdf)

---

*This assessment was conducted entirely within an isolated, non-production lab environment built for educational purposes.*
