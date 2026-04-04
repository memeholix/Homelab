# Pi Hardening

OS hardening steps applied to Raspberry Pi OS Lite (64-bit) on a Raspberry Pi 5.

## System Updates

- Updated package lists and upgraded all installed packages
- Enabled unattended-upgrades for automatic security updates

## Firewall — UFW

| Rule | Reason |
|---|---|
| Default deny incoming | Block all unsolicited inbound connections |
| Allow SSH | Remote access to the machine |
| Allow port 53 | DNS traffic for Pi-hole |

## Brute Force Protection — fail2ban

- Enabled on boot
- Monitors SSH login attempts
- Bans IPs after repeated failed failures

## System Auditing — auditd

- Logs system level activity
- Feeds into Wazuh SIEM for centralized analysis
- audispd-plugins installed for real time log forwarding

## SSH Hardening

| Setting | Value | Reason |
|---|---|---|
| PermitRootLogin | no | Prevent direct root login over SSH |
| PasswordAuthentication | no | Require key-based auth only |
| X11Forwarding | no | Disable graphical forwarding |
| MaxAuthTries | 3 | Limit login attempts per connection |

## SSH Key Authentication

Generated ed25519 key pair on ThinkPad and added public key during
Pi OS Lite installation via Raspberry Pi Imager. Password authentication
disabled — key only access.
