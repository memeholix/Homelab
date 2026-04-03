# VirtualBox Lab

Isolated virtual machine lab for offensive and defensive security practice.
All lab traffic is contained within a host-only network — no exposure to the home network.

## Network Configuration

| Setting | Value |
|---|---|
| Interface | vboxnet0 |
| Host IP | 192.168.56.1 |
| DHCP Range | 192.168.56.101 — 192.168.56.200 |
| Type | Host-only (isolated) |

No lab VM can reach the internet or home network unless explicitly given a NAT adapter.

## Virtual Machines

| VM | OS | Role | Network |
|---|---|---|---|
| Metasploitable 2 | Linux | Vulnerable target | Host-only |
| Kali Linux | Kali | Attacker machine | NAT + Host-only |
| REMnux | Linux | Malware analysis | Host-only |
| Windows 11 Enterprise LTSC | Windows | Windows target | Host-only |

## VM Specs

| VM | RAM | CPU |
|---|---|---|
| Metasploitable 2 | 512MB | 1 core |
| Kali Linux | 2048MB | 2 cores |
| REMnux | 2048MB | 2 cores |
| Windows 11 | 4096MB | 2 cores |

## Snapshots

Clean baseline snapshots taken for each VM before any lab work.
Allows instant revert if a VM becomes too compromised or broken.

## Lab Scenarios

- Red team practice — Kali attacking Metasploitable 2
- Malware analysis — generate samples with Metasploit, analyze in REMnux
- Windows exploitation — Kali attacking Windows 11 target
- Full kill chain — attack, compromise, analyze, detect in Wazuh SIEM
