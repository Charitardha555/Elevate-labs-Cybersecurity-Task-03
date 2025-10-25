# Task 3: Basic Vulnerability Scan on Local PC

A repository for the task 03 from the Elevate labs, Cybersecurity

## Project Overview

This project documents a vulnerability assessment on a local Windows machine using Nessus Essentials, as part of the Elevate Labs Cybersecurity Internship (MSME, Govt. of India) [file:2].

---

## Objective

- Identify common vulnerabilities on a personal computer using free tools.
- Analyze and prioritize discovered issues based on industry standards.

---

## Tools Used

- **Scanner:** Nessus Essentials (Tenable)
- **Target:** Localhost (192.168.1.7)
- **Scan Duration:** Approximately 30-60 minutes
- **Method:** CVSS-based risk prioritization [web:8]

---

## Scan Results Summary

| Vulnerability Name                                      | Family                | Count | Severity |
| ------------------------------------------------------- | --------------------- | ----- | -------- |
| SMB (Multiple Issues)                                   | Windows               | 6     | Info     |
| Netstat Portscanner (SSH)                               | Port scanners         | 58    | Info     |
| DCE Services Enumeration                                | Windows               | 8     | Info     |
| Service Detection                                       | Service detection     | 2     | Info     |
| Host Fully Qualified Domain Name (FQDN) Resolution      | General               | 1     | Info     |
| mDNS Detection (Local Network)                          | Service detection     | 1     | Info     |
| Microsoft Windows NTLMSSP Authentication Request        | Windows               | 1     | Info     |
| Netstat Connection Information                          | General               | 1     | Info     |

---

## Scan Results Screenshot

![Nessus Scan Results](screenshots/nessus-scan-results.png)

## CVSS Scoring and Risk Analysis

---

The Common Vulnerability Scoring System (**CVSS**) rates findings 0.0 (Info) to 10.0 (Critical). All current findings are **Informational** (not exploitable), but still reveal available services and network exposure [web:11][web:8].

---

## Key Findings

- **Windows service enumeration:** SMB and DCE services are detectable.
- **Port scanning:** SSH and general network services visible.
- **Authentication protocols:** NTLMSSP visible on network.
- **DNS/mDNS discovery:** Hostname and multicast DNS detectable.

---

## Security Recommendations

- Restrict network service exposure.
- Disable unused Windows services.
- Apply proper authentication controls.
- Perform monthly scans and maintain patch discipline [web:10].

---

## Tools Comparison: Nessus Vs OpenVAS

| Feature               | Nessus Essentials     | OpenVAS             |
|---------------------- | -------------------- | ------------------- |
| Cost                  | Free (limited)       | Free                |
| Vulnerabilities DB    | 50k+                 | 26k+                |
| Plugins/Test Count    | 130k+ plugins        | 50k+ tests          |
| UI                    | Modern web dashboard | Technical/CLI       |
| OS Support            | Windows/Linux/Mac    | Linux/Unix focus    |
| Updates               | Automatic            | Manual              |
| Ease of Use           | Beginner-friendly    | Technical users     |

[web:12][web:15]

---

## Interview Preparation

1. **What is vulnerability scanning?**  
   Automated identification of security weaknesses on systems [file:2].

2. **Difference from penetration testing?**  
   Scanning finds potential flaws; pen testing exploits them.

3. **Common PC vulnerabilities?**  
   Unpatched software, weak passwords, open services.

4. **Detection methods?**  
   Probing, enumeration, version checks, configuration analysis.

5. **What is CVSS?**  
   The global standard for vulnerability severity scoring [web:14].

6. **Recommended scan frequency?**  
   Monthly for workstations, weekly for critical systems [web:10].

7. **False positives?**  
   Findings that don't represent real vulnerabilities.

8. **Prioritization?**  
   Based on CVSS, exploit potential, business impact.

---

## Project Structure

vulnerability-scan-project/
├── README.md
├── screenshots/
│ └── nessus-scan-results.png
├── reports/
│ └── nessus-scan-report.html
└── documentation/
└── scan-configuration.txt


---

## Learning Outcomes

- Experienced hands-on vulnerability assessment using standard tools.
- Learned to interpret CVSS scores and prioritize risks.
- Gained documentation and reporting skills for cybersecurity [file:2][web:14].
