# Network-Scanner-Project
# Network Scanner Project

## Project Overview
This project demonstrates complete network scanning and reconnaissance using Nmap in a Kali Linux environment. The objective is to identify live hosts, open ports, running services, operating systems, and potential security risks within a network.

Network scanning is a critical phase in cybersecurity and penetration testing, helping security professionals understand the attack surface of a network.

---

## Objective

- Perform network discovery and reconnaissance
- Identify open TCP and UDP ports
- Detect service names and versions
- Identify operating systems
- Understand stealth and evasion techniques
- Analyze security risks from scan results

---

## Tools Used

- Kali Linux
- Nmap
- VMware Workstation
- Windows Host System

---

## Experimental Setup

- VMware installed on Windows host
- Kali Linux virtual machine configured
- Network mode set to NAT or Bridged
- Target IP identified using `ip a` or `ifconfig`
- Nmap pre-installed in Kali Linux

---

# Nmap Commands and Explanations

---

## 1. Nmap Version Check

**Command Used:**

```bash
nmap --version
Explanation:
Performs default TCP SYN scan on top 1,000 ports for initial reconnaissance.

3. Scan a Hostname

Command Used:

nmap example.com


Explanation:
Resolves hostname to IP address via DNS and executes a standard port scan.

4. Scan Entire Network

Command Used:

nmap 10.85.57.0/24


Explanation:
Scans all 254 hosts in the /24 subnet to map the entire network segment.

5. List Active Hosts (Ping Scan)

Command Used:

nmap -sn 10.85.57.0/24


Explanation:
Discovers live hosts without performing port scans to minimize network traffic.

6. Skip Host Discovery

Command Used:

nmap -Pn 10.198.101.71


Explanation:
Assumes the target is online and bypasses ICMP/TCP/UDP discovery.

7. Scan Specific Port

Command Used:

nmap -p 80 10.198.101.71


Explanation:
Scans only port 80 to verify HTTP service availability.

8. Scan Multiple Ports

Command Used:

nmap -p 22,80,443 10.198.101.71


Explanation:
Scans SSH, HTTP, and HTTPS ports simultaneously.

9. Scan Port Range

Command Used:

nmap -p 1-1000 10.198.101.71


Explanation:
Sequential scan of the first 1,000 TCP ports.

10. Scan All Ports

Command Used:

nmap -p- 10.198.101.71


Explanation:
Performs a full scan of all 65,535 TCP ports to detect non-standard services.

11. Detect Service Version

Command Used:

nmap -sV 10.198.101.71


Explanation:
Identifies running services and exact versions for vulnerability analysis.

12. Light Version Detection

Command Used:

nmap -sV --version-light 10.198.101.71


Explanation:
Faster service detection using reduced probe set.

13. OS Detection

Command Used:

nmap -O 10.198.101.71


Explanation:
Detects operating system using TCP/IP stack fingerprinting.

14. Aggressive OS Detection

Command Used:

nmap -O --osscan-guess 10.198.101.71


Explanation:
Provides best-guess OS detection when results are uncertain.

15. Stealth SYN Scan

Command Used:

nmap -sS 10.198.101.71


Explanation:
Half-open SYN scan that reduces logging (requires root privileges).

16. TCP Connect Scan

Command Used:

nmap -sT 10.198.101.71


Explanation:
Performs full TCP handshake; visible in server logs.

17. UDP Scan

Command Used:

nmap -sU 10.198.101.71


Explanation:
Discovers UDP services like DNS, SNMP, and TFTP.

18. FIN Scan

Command Used:

nmap -sF 10.198.101.71


Explanation:
Firewall evasion scan using FIN packets.

19. NULL Scan

Command Used:

nmap -sN 10.198.101.71


Explanation:
Sends packets with no TCP flags to detect OS TCP behavior.

20. Xmas Scan

Command Used:

nmap -sX 10.198.101.71


Explanation:
Uses FIN, PSH, and URG flags for stealth detection.

21. Aggressive Scan

Command Used:

nmap -A 10.198.101.71


Explanation:
Combines OS detection, version detection, default scripts, and traceroute.

22. Traceroute

Command Used:

nmap --traceroute 10.198.101.71


Explanation:
Maps the network path between scanner and target.

23. Fragment Packet Scan

Command Used:

nmap -f 10.198.101.71


Explanation:
Splits packets into small fragments to evade simple filters.

24. Decoy Scan

Command Used:

nmap -D RND:5 10.198.101.71


Explanation:
Uses random decoy IP addresses to obscure the real scanner source.

25. Spoof MAC Address

Command Used:

nmap --spoof-mac random 10.198.101.71


Explanation:
Randomizes MAC address for local network evasion.

26. Default Script Scan

Command Used:

nmap -sC 10.198.101.71


Explanation:
Runs Nmap’s default safe scripts for common security checks.

27. Vulnerability Scan

Command Used:

nmap --script vuln 10.198.101.71


Explanation:
Runs vulnerability detection scripts based on known CVEs.

28. Specific Script Scan

Command Used:

nmap --script http-title 10.198.101.71


Explanation:
Extracts HTTP page titles for web enumeration.

29. Faster Timing Scan

Command Used:

nmap -T4 10.198.101.71


Explanation:
Uses aggressive timing template to speed up scanning while maintaining reliability.

Analysis

Open ports increase attack surface.

Unnecessary services may expose vulnerabilities.

Outdated versions can be exploited.

Firewall misconfiguration may allow unauthorized access.

Conclusion

This project provided hands-on experience with Nmap for network scanning and reconnaissance. It improved understanding of host discovery, port scanning, service detection, OS fingerprinting, and security risk analysis. These techniques form the foundation of penetration testing and defensive cybersecurity.

Author

Bharath kishore
Cybersecurity Student
