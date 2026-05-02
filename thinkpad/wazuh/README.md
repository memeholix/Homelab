# Wazuh SIEM

Full Wazuh SIEM stack running on Lenovo ThinkPad (Ubuntu Desktop 24.04).
Chosen as the SIEM host to avoid ARM64 compatibility issues on Raspberry Pi.

## Components

| Component | Role |
|---|---|
| Wazuh Manager | Receives and analyzes events from agents, generates alerts |
| Wazuh Indexer | Stores and indexes all log data for fast querying (OpenSearch) |
| Wazuh Dashboard | Web UI for monitoring alerts and events |

## Configuration

| Setting | Value |
|---|---|
| Host IP | 192.168.0.45 |
| Dashboard URL | https://192.168.0.45 |
| Manager port | 1514 |
| Enrollment port | 1515 |
| Installation method | Official Wazuh install script (wazuh-install.sh -a) |

## Agents

| Device | OS | Role |
|---|---|---|
| Raspberry Pi 5 | Raspberry Pi OS Lite | Homelab server — coming soon |

## Notes

- Installed via official Wazuh automated install script
- Ubuntu 26.04 not officially supported — installed with compatibility warning, working correctly
- All three components (manager, indexer, dashboard) running as native systemd services
- UFW rules opened for ports 443, 1514, 1515