# Jellyfin

Open source media server running on Raspberry Pi 5.
Chosen over Plex for being fully free, no account required,
and no paywall for hardware transcoding.

## Configuration

| Setting | Value |
|---|---|
| Host IP | 192.168.0.23 |
| Web UI | http://192.168.0.23:8096 |
| Restart policy | Unless stopped |

## Media Libraries

| Library | Path |
|---|---|
| Movies | /media/movies |
| TV Shows | /media/shows |
| Music | /media/music |
| Books | /media/books |

## Storage

Media files stored on Pi 5 NVMe SSD.
Planned expansion to RAID 1 (2x2TB NVMe) for redundancy.

## Access

Available on any device on the local network via browser or Jellyfin app.
Remote access available via Tailscale VPN.

## Notes

- Config and cache stored in ~/jellyfin/ on the Pi
- Media folder mapped directly into the container
- No Plex Pass or subscription required
