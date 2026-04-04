# Homer

Static homelab dashboard running on Raspberry Pi 5.
Provides a single page with links to all self-hosted services.

## Configuration

| Setting | Value |
|---|---|
| Web UI | http://192.168.0.23:8082 |
| Config file | /home/pi/homer/config.yml |
| Restart policy | Unless stopped |

## Services Listed

| Service | URL |
|---|---|
| Jellyfin | http://192.168.0.23:8096 |
| Pi-hole | http://192.168.0.23/admin |
| Portainer | https://192.168.0.23:9443 |
| Uptime Kuma | http://192.168.0.23:3001 |
| Grafana | http://192.168.0.23:3000 |

## Notes

- Config is a YAML file mounted as a volume into the container
- Dashboard updates automatically on browser refresh when config is changed
- Uses Font Awesome icons for service icons
