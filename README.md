# Scan-of-local-Network-for-open-Ports-Task1-
This is a scan for open ports in my local network using Nmap &amp; Wireshark.

# Project Overview 
This project demonstrate network reconnaissance skills by performing port scanning on a local network to identify open ports.

# Objectives 
- Perform network discovery using Nmap
- Identify open ports and services
- Analyze potential security risks
- Document findings and methodologies

# Tools Used 
- **Namp** - Network scanning and discovery
- **Kali Linux** - Security assessment platform

## Quick Start 

- Installation of Kali Linux from the below link

==> https://nmap.org/download#linux-rpm

# Go to Command Line

1. nmap --version --> To check the version of Namp / to check if Nmap has installed 
  (Nmap is genrally pre-installed in all the kali systems)

2. ifconfig --> Finding loocal range

3. nmcli device show --> Network Manager (eg : 192.168.1.x is inet address)

4. **To Perform TCP SYN Scan**
   sudo namp -sS 192.168.1.0/24

   OR

   **For Advance Scan**
   sudo nmap -sS -p 1-1000 192.168.1.0/24

   sudo nmap -sS -p 21,22,23,25,53,80,110,135,139,143,443,445,993,995,3389 192.168.1.0/24

5.**To save results in html format**

  sudo namp -sS -sV -O 192.168.1.0/24 -oH scan_results.html


