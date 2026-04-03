# ThinkPad Hardening

OS hardening steps applied to Ubuntu Desktop 24.04 on a Lenovo ThinkPad.
The goal is to reduce the attack surface before installing any security tools.

## System Updates

Kept the system fully patched to eliminate known vulnerabilities.

- Updated package lists and upgraded all installed packages
- Removed unused dependency packages with autoremove

## Firewall — UFW

Configured UFW (Uncomplicated Firewall) to deny all incoming traffic by default,
only allowing what is explicitly needed.

| Rule | Reason |
|---|---|
| Default deny incoming | Block all unsolicited inbound connections |
| Allow SSH | Remote access to the machine |

## Brute Force Protection — fail2ban

Installed fail2ban to automatically ban IPs that repeatedly fail authentication.
Protects against brute force attacks on SSH and other services.

- Enabled on boot
- Default configuration monitors SSH login attempts
- Bans IPs after repeated failed attempts

## System Auditing — auditd

Installed auditd to log system-level activity including file access,
user logins, permission changes, and process execution.

- Feeds into Wazuh SIEM for centralized analysis
- Provides forensic trail of system activity
- Installed audispd-plugins for real-time log forwarding

## SSH Hardening

Modified /etc/ssh/sshd_config to lock down remote access.

| Setting | Value | Reason |
|---|---|---|
| PermitRootLogin | no | Prevent direct root login over SSH |
| PasswordAuthentication | no | Require key-based auth only |
| X11Forwarding | no | Disable graphical forwarding, known attack surface |
| MaxAuthTries | 3 | Limit login attempts per connection |

## Tools Used

- UFW — firewall management
- fail2ban — brute force protection
- auditd — system call auditing
- audispd-plugins — audit log forwarding
