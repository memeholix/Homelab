# Prometheus

Metrics collection and storage running on Raspberry Pi 5.
Scrapes system metrics from Node Exporter and stores them for Grafana to visualize.

## Configuration

| Setting | Value |
|---|---|
| Web UI | http://192.168.0.23:9090 |
| Config file | /home/pi/prometheus/prometheus.yml |
| Scrape interval | 15 seconds |
| Scrape target | 192.168.0.23:9100 (Node Exporter) |
| Restart policy | Unless stopped |

## Node Exporter

Runs alongside Prometheus to expose system metrics from the Pi.

| Setting | Value |
|---|---|
| Port | 9100 |
| Metrics endpoint | http://192.168.0.23:9100/metrics |
| Restart policy | Unless stopped |

Mounts /proc, /sys, and / from the host as read-only volumes so it can
read system metrics without modifying anything.

## Notes

- Prometheus config mounted as read-only volume into container
- Node Exporter target uses Pi IP (192.168.0.23) not localhost — containers have their own loopback
- Config file located at /home/pi/prometheus/prometheus.yml on the Pi
