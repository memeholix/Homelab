# Red Team Toolkit

Security tools installed on Ubuntu Desktop 24.04 for offensive security research
and penetration testing practice.

## Network Tools

| Tool | Purpose |
|---|---|
| nmap | Network scanner, maps open ports and services on targets |
| netcat | Raw TCP/UDP connections, port scanning, creating listeners |
| tcpdump | Command line packet capture |
| wireshark | Graphical network traffic analyzer |
| tshark | Command line version of Wireshark |
| net-tools | Classic tools including ifconfig and netstat |

## Exploitation

| Tool | Purpose |
|---|---|
| Metasploit | Full exploitation framework with database backend |
| sqlmap | Automated SQL injection testing |
| hydra | Online brute force tool for SSH, FTP, web forms |

## Web Reconnaissance

| Tool | Purpose |
|---|---|
| nikto | Web server vulnerability scanner |
| gobuster | Directory and DNS enumeration |
| dirb | Hidden directory and file scanner |
| whatweb | Website fingerprinting and tech identification |
| dnsrecon | DNS enumeration and zone transfer testing |

## Password Cracking

| Tool | Purpose |
|---|---|
| john | John the Ripper — offline password hash cracker |
| hashcat | GPU accelerated password cracker for large wordlists |

## Forensics

| Tool | Purpose |
|---|---|
| binwalk | Binary analysis and file extraction |
| foremost | File carving and recovery from disk images |
| steghide | Steganography — hide and extract data in images |

## Installation Notes

- Metasploit installed via Rapid7 official apt repository
- Added self to wireshark group for non-root packet capture
- Python3, pip, and venv installed as base for Python security tools

## Usage

Tools are used exclusively against owned systems and isolated lab VMs.
All offensive testing conducted within the VirtualBox host-only network.
