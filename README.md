# ARP‑Scan Troubleshooting & Analysis Training Guide

This repository contains a comprehensive, operator‑grade training guide focused on diagnosing and resolving ARP‑Scan vendor‑file issues in Linux environments. The project blends academic clarity with red‑team methodology, providing a structured, repeatable workflow for identifying malformed OUI data, hidden vendor files, and system‑level misconfigurations that impact ARP‑based network discovery.

The full PDF guide is included in this repository.

---

## Overview

ARP‑Scan is a powerful tool for network discovery, but its accuracy depends heavily on the integrity of its vendor (OUI) files. During this project, I reproduced real‑world failure modes, analyzed their root causes, and built a complete troubleshooting and remediation workflow. The result is a polished training guide suitable for cybersecurity students, SOC analysts, and red‑team operators.

---

## What This Guide Covers

### 1. ARP & OUI Fundamentals
- How ARP maps IP addresses to MAC addresses  
- How vendor files resolve MAC prefixes to manufacturers  
- Why vendor resolution matters for reconnaissance accuracy  

### 2. Vendor File Architecture
- The exact search order ARP‑Scan uses  
- Risk levels associated with each directory  
- How hidden or malformed files override system defaults  

### 3. Failure Mode Analysis
Documented and reproduced issues including:
- Malformed OUI entries  
- CRLF vs LF line‑ending conflicts  
- Duplicate or extended OUI prefixes  
- Hidden vendor files in user directories  
- Incorrect fallback behavior  

Each failure mode includes symptoms, root cause, and operational impact.

### 4. Diagnostic Workflow
A step‑by‑step troubleshooting process:
- Validate environment  
- Enumerate vendor file paths  
- Use `strace` to trace file access  
- Identify shadowed or malformed files  
- Validate formatting and encoding  
- Rebuild vendor directories from trusted sources  

### 5. Case Study: Hidden mac‑vendor.txt
A real troubleshooting scenario where ARP‑Scan produced “Could not parse OUI” warnings. Using `strace`, I discovered a malformed vendor file in the home directory. The guide documents the investigation, root cause, and resolution in full detail.

### 6. Remediation Procedures
- Remove corrupted vendor directories  
- Rebuild clean vendor file structures  
- Download official IEEE OUI data  
- Validate formatting (tabs, LF, no BOM)  
- Run clean scans to confirm resolution  

### 7. Expected Clean Output
Examples of correct ARP‑Scan output for comparison and validation.

### 8. Hands‑On Exercises
Academic‑style labs:
- Identify malformed OUI entries  
- Trace file access with `strace`  
- Rebuild vendor directories  
- Validate formatting  
- Perform clean scans and document results  

### 9. Red‑Team Application Scenarios
- Network footprinting  
- Identifying device types  
- Detecting rogue devices  
- Mapping IoT ecosystems  

---

## Skills Demonstrated

- Linux troubleshooting  
- Network discovery & enumeration  
- ARP protocol analysis  
- File system forensics  
- Diagnostic workflow design  
- Technical writing & documentation  
- Red‑team methodology  
- Academic training development  

---

## Included Files

- `arp_scan_training_guide_full.pdf` — Full training guide  
- `examples/` — Optional sample files for labs and demonstrations  

---

## Contact

Connect with me on LinkedIn:  
https://www.linkedin.com/in/easton-childress-99248127b
