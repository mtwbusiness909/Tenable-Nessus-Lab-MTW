# Tenable-Nessus-Lab-MTW

A hands-on cybersecurity lab demonstrating how to use **Tenable Nessus Essentials** to discover network assets, perform authenticated vulnerability scans, and analyze security findings on a Windows Server.

---

# Overview

Vulnerability management is one of the most important responsibilities of a cybersecurity team. Organizations continuously scan their systems to identify missing patches, insecure configurations, outdated software, and other weaknesses before attackers can exploit them.

In this lab, I installed and configured **Tenable Nessus Essentials** to perform two different types of vulnerability assessments against a Windows Server:

- **Network Discovery Scan**
- **Credentialed Vulnerability Scan**

The first scan identified hosts and exposed network services, while the second authenticated directly to the Windows Server using administrator credentials to perform a much deeper inspection of the operating system.

This project demonstrates the same vulnerability assessment workflow commonly performed by Security Analysts, Vulnerability Analysts, and Security Engineers in enterprise environments.

---

# Business Problem

Organizations often manage hundreds or even thousands of computers across their networks. Without an automated vulnerability management solution, security teams would have no efficient way to identify:

- Missing Windows updates
- Weak security configurations
- Disabled security controls
- Outdated software
- Known vulnerabilities

Attackers actively search for these weaknesses. Tools like **Tenable Nessus** allow defenders to identify and prioritize security risks before they become security incidents.

This lab demonstrates how vulnerability scanners help organizations proactively reduce their attack surface.

---

# Lab Environment

| Component | Description |
|-----------|-------------|
| Vulnerability Scanner | Tenable Nessus Essentials |
| Target Machine | Windows Server |
| Scan Types | Network Discovery & Credentialed Scan |
| Authentication | Windows Administrator Credentials |

---

# Project Walkthrough

## Step 1 — Identify the Target

The Windows Server was configured and its IP address identified before scanning.

> 📷 **Insert Screenshot 1**

This establishes the target system that Nessus will assess.

---

## Step 2 — Create a New Scan

A new scan policy was created inside Nessus.

> 📷 **Insert Screenshot 2**

This defines how Nessus will perform the assessment.

---

## Step 3 — Select the Basic Network Scan Template

The Basic Network Scan template was selected.

> 📷 **Insert Screenshot 3**

This template performs host discovery and identifies exposed services running on the target machine.

---

## Step 4 — Configure the Scan

The Windows Server IP address was entered into the scan configuration.

> 📷 **Insert Screenshot 4**

At this stage, Nessus knows which system it should assess.

---

## Step 5 — Save and Launch the Scan

The scan configuration was saved and executed.

> 📷 **Insert Screenshot 5**

> 📷 **Insert Screenshot 6**

Nessus began probing the target system for open ports, services, and operating system information.

---

## Step 6 — Review Discovery Results

Once the scan completed, Nessus generated its first report.

> 📷 **Insert Screenshot 7**

### What this scan tells us

The discovery scan identifies:

- Reachable hosts
- Open ports
- Running services
- Basic operating system information

Because no credentials were supplied, Nessus could only analyze information that was publicly accessible across the network.

This type of scan is commonly used for:

- Asset discovery
- External attack surface assessments
- Initial penetration testing
- Network inventory

---

# Credentialed Vulnerability Scan

Unlike a discovery scan, a credentialed scan authenticates directly into Windows.

This allows Nessus to inspect:

- Installed software
- Windows Updates
- Registry settings
- Password policies
- Local security policies
- Security configuration
- Windows Defender
- Firewall configuration

Credentialed scans provide significantly more visibility than unauthenticated scans and are considered the industry standard for internal vulnerability management.

---

## Configuring the Credentialed Scan

The administrator credentials for the Windows Server were added to Nessus.

> 📷 **Insert Screenshots 8–13**

This allows Nessus to inspect the operating system rather than only scanning exposed network services.

---

# Introducing Security Misconfigurations

To demonstrate how Nessus detects security weaknesses, several intentionally insecure configurations were introduced.

### Windows Firewall Disabled

> 📷 **Insert Screenshot 14**

Disabling the Windows Firewall exposes the server to unnecessary network risks and is commonly identified during vulnerability assessments.

---

### Weak Password Policy

> 📷 **Insert Screenshot 15**

Weak password requirements increase the likelihood of password attacks such as brute force or credential stuffing.

---

### Microsoft Defender Disabled

> 📷 **Insert Screenshot 16**

Without endpoint protection, malware and malicious software become significantly easier to execute on the system.

---

### Missing Windows Updates

> 📷 **Insert Screenshot 17**

Missing security updates leave known vulnerabilities unpatched and increase the likelihood of successful exploitation.

---

# Scan Reports

## Network Discovery Report

📄 **Lab Network Discovery Scan.pdf**

This report summarizes the results of the unauthenticated scan.

It includes:

- Discovered hosts
- Open ports
- Network services
- Operating system detection
- Basic vulnerability information

This report demonstrates what an attacker could learn without authenticating to the target system.

---

## Credentialed Vulnerability Report

📄 **Lab Windows Server - Credential Scan.pdf**

This report provides a much deeper assessment of the Windows Server.

Because Nessus authenticated using administrator credentials, it was able to identify:

- Missing Windows security updates
- Security configuration issues
- Disabled security controls
- Weak password policies
- Potential vulnerabilities requiring remediation
- Risk severity ratings
- CVSS scores
- Recommended remediation steps

This type of report is commonly used by IT and Security teams to prioritize patching efforts and improve an organization's overall security posture.

---

# What I Learned

This lab gave me practical experience using an enterprise vulnerability management platform to identify and analyze security risks.

Throughout the project I learned how to:

- Install and configure Tenable Nessus Essentials
- Perform network discovery scans
- Configure credentialed Windows scans
- Authenticate vulnerability scans using administrator credentials
- Analyze vulnerability severity ratings
- Interpret CVSS scores
- Understand the difference between authenticated and unauthenticated scanning
- Identify insecure Windows configurations
- Read professional vulnerability assessment reports
- Understand how vulnerability scanners support enterprise security operations

---

# Skills Demonstrated

- Vulnerability Management
- Vulnerability Assessment
- Tenable Nessus Essentials
- Windows Server Administration
- Windows Security
- Credentialed Vulnerability Scanning
- Network Discovery
- Security Hardening
- CVSS Risk Analysis
- Vulnerability Prioritization
- Windows Firewall Configuration
- Microsoft Defender
- Patch Management
- Security Reporting
- Risk Assessment

---

# Key Takeaways

- Credentialed scans provide significantly more visibility than unauthenticated scans.
- Vulnerability management is an ongoing process rather than a one-time activity.
- Security misconfigurations can be just as dangerous as missing patches.
- CVSS scores help organizations prioritize remediation efforts based on risk.
- Vulnerability scanners enable organizations to proactively identify weaknesses before attackers can exploit them.

---

# Portfolio Summary

This project demonstrates practical experience performing enterprise-style vulnerability assessments using **Tenable Nessus Essentials**.

By completing both unauthenticated and credentialed scans, I gained hands-on experience identifying security weaknesses, analyzing professional vulnerability reports, and understanding how organizations prioritize and remediate risk.

This lab strengthened my understanding of vulnerability management, Windows security, and defensive cybersecurity practices while reinforcing skills commonly used by Security Analysts, Vulnerability Analysts, and Security Engineers.
