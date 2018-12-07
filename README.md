# ejabberd-influxdb

Quick and dirty approach to get stats of ejabberctl into InfluxDB for visualizing using Grafana.

## Usage
`./ejabberstats`

## Utilization
Use this script call within InfluxData's Telegraf

e.g.:
```toml
[[inputs.exec]]
	commands = ["sudo -u jabber /opt/ejabberd-influxdb/ejabberstats"]
	timeout = "5s"
	data_format = "influx"

