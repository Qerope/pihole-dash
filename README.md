# pihole-dash

Grafana dashboard for a Pi-hole using
pihole-exporter (ekofr/pihole-exporter) metrics.

    cp .env.example .env     # set the Pi-hole API token (Settings > API)
    docker-compose up -d

Edit the Pi-hole address in `docker-compose.yml`. Grafana is on :3000
(admin/admin on first login), Prometheus on :9090. Metrics are kept for 90
days. `PiholeDown` fires if the exporter has been down for 5 minutes; there is
no Alertmanager, check the Alerts page in Prometheus.
