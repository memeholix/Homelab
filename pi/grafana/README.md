# Grafana

Metrics visualization and dashboards running on Raspberry Pi 5.
Connects to Prometheus as a data source and displays system metrics as interactive dashboards.

## Configuration

| Setting | Value |
|---|---|
| Web UI | http://192.168.0.23:3000 |
| Data source | Prometheus (http://192.168.0.23:9090) |
| Dashboard | Node Exporter Full (ID: 1860) |
| Restart policy | Unless stopped |

## Dashboards

| Dashboard | ID | Purpose |
|---|---|---|
| Node Exporter Full | 1860 | CPU, RAM, disk, network metrics for the Pi |

## Notes

- Data source configured via Grafana UI pointing to Prometheus
- Dashboard 1860 imported via Grafana dashboard import feature
- Login credentials set on first launch
