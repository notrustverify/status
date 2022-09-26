# Status for mixnode

## Pre-requistes
- Telegraf
- InfluxDB v2
- Grafana datasource must be `Flux`

To authenticate from Grafana to InfluxDB a token is mandatory. [https://docs.influxdata.com/influxdb/cloud/security/tokens/create-token/](https://docs.influxdata.com/influxdb/cloud/security/tokens/create-token/)

Grafana dashboard: [grafana.com/grafana/dashboards/16460-ntv-mixnode](https://grafana.com/grafana/dashboards/16460-ntv-mixnode)


Demo: [No Trust Verify mixnode](https://status.notrustverify.ch/)

## Docker install

1. `cp telegraf/telegraf.env.example telegraf/telegraf.env`
2. `docker-compose up -d`
3. Configure [influxdb](https://docs.influxdata.com/influxdb/v2.2/install/#set-up-influxdb-through-the-ui)
4. Set the values in `telegraf/telegraf.env` from influxdb install
5. Set your mixnodes and gateway identity key in `telegraf/telegraf.conf`
6. Import grafana dashboard by id [16460](https://grafana.com/grafana/dashboards/16460-ntv-mixnode) or copy the JSON in the instance 

7. docker-compose restart telegraf
