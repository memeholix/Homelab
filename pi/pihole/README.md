# Pi-hole

Network-wide DNS filtering and ad blocking running on the Raspberry Pi 5.
Permanent installation replacing the temporary ThinkPad instance.

## Configuration

| Setting | Value |
|---|---|
| Host IP | 192.168.0.23 |
| Web UI | http://192.168.0.23/admin |
| DNS Port | 53 |
| Timezone | America/Los_Angeles |
| Listening Mode | All interfaces |

## Network Integration

Router primary DNS set to 192.168.0.23 so all devices on the network
route DNS through Pi-hole automatically.

Fallback DNS set to OpenDNS (208.67.222.222) in case Pi-hole goes down.

## Blocklists

| List | Purpose |
|---|---|
| Steven Black Unified Hosts | Ads and malware |
| OISD Full | Comprehensive ad and tracker blocking |
| Hagezi Pro | Malware, phishing and tracking |
| URLhaus | Active malware distribution domains |
| WindowsSpyBlocker | Microsoft telemetry blocking |

Total domains blocked: 831,745+

## Notes

- FTLCONF_dns_listeningMode=all set to accept queries from all interfaces
- avahi-daemon disabled to free up port 53
- Persistent volumes used for configuration and blocklists
- Replaces temporary Docker instance that ran on ThinkPad during migration
