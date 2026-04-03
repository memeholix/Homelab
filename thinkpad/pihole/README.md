# Pi-hole — ThinkPad (Temporary)

Temporary Pi-hole instance running on the ThinkPad in Docker.
Deployed to maintain network-wide DNS filtering during Raspberry Pi OS migration.
Will be decommissioned once the Pi is fully set up.

## Deployment

Running as a Docker container with persistent volumes so configuration
survives container restarts and updates.

## Configuration

| Setting | Value |
|---|---|
| Host IP | 192.168.0.231 |
| Web UI | http://192.168.0.231:8080/admin |
| DNS Port | 53 |
| Timezone | America/Los_Angeles |

## Network Integration

Router primary DNS set to 192.168.0.231 so all devices on the network
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

Total domains blocked: 831,706+

## Lid Behavior

Modified /etc/systemd/logind.conf to set HandleLidSwitch=ignore
so Pi-hole keeps running when the laptop lid is closed.

## Notes

- systemd-resolved disabled to free up port 53
- avahi-daemon disabled — not needed
- Docker restart policy set to unless-stopped for automatic recovery on reboot
