# Status for mixnode

## Pre-requistes
- Telegraf
- InfluxDB v2
- Grafana datasource must be `Flux`

To authenticate from Grafana to InfluxDB a token is mandatory. [https://docs.influxdata.com/influxdb/cloud/security/tokens/create-token/](https://docs.influxdata.com/influxdb/cloud/security/tokens/create-token/)

[Grafana dashboard](https://grafana.com/grafana/dashboards/16460-ntv-mixnode)

Demo: [No Trust Verify mixnode](https://status.notrustverify.ch/)


1. `docker-compose up -d`
2. Configure [influxdb](https://docs.influxdata.com/influxdb/v2.2/install/#set-up-influxdb-through-the-ui)
3. `cp telegraf/telegraf.env.example telegraf/telegraf.env`
