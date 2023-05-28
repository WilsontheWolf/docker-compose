# Grafana (and prometheus)

```sh
mkdir prometheus_data grafana_data
chown 472 grafana_data
chown 65534 prometheus_data
```

make a file `prometheus.yml`
```yml
global:
  scrape_interval: 1m

scrape_configs:
  - job_name: 'example'
    static_configs:
      - targets: ['example.shorty.systems']
```

