# Crosswork Alert Forwarding

Crosswork can be configured to forward alerts generated from KPIs.
Alerts can be forwarded to services outside of Crosswork for further processing,
e.g.  Splunk, Webex Teams, Sitman, and ServiceNow.Crosswork

# Alert Message Format

Alert messages are data points in time series database. Some of the fields in the messages are common across all KPIs,
some may vary from KPI to KPI. In the example below "node-name" is applicable to KPI "pulse_cpu_utilization",
while "interface-name" is applicable to KPI "pulse_interface_rate_counters". The variable fields are sensor keys
as documented on [DevNet Crosswork KPI](https://github.com/CiscoDevNet/Crosswork-KPI). For example,
[pulse_cpu_utilization](https://github.com/CiscoDevNet/Crosswork-KPI/blob/master/pulse_cpu_utilization/pulse_cpu_utilization.md)
[pulse_interface_rate_counters](https://github.com/CiscoDevNet/Crosswork-KPI/blob/master/pulse_interface_rate_counters/pulse_interface_rate_counters.md).

Example
[{
		"series": [{
			"columns": [
				"time",
				"activation_threshold",
				"alert_src",
				"clear_threshold",
				"crit_threshold",
				"id",
				"kpi_stream",
				"msg",
				"sigma",
				"warn_threshold"
			],
			"name": "alerts",
			"tags": {
				"CollectorId": "mdt-robot-collector-13a3958e-63d5-47e5-9e0f-31e846b89f2e",
				"EncodingPath": "Cisco-IOS-XR-wdsysmon-fd-oper:system-monitoring/cpu-utilization",
				"Producer": "spnac-a9k-s079",
				"UUID": "5108e98e-aea0-49a5-ba32-88db39b777c3",
				"kpi_id": "pulse_cpu_utilization",
				"level": "INFO",
				"node-name": "0/RP0/CPU0",
				"state": "clear"
			},
			"values": [
				[
					"2019-09-05T22:02:57.412Z",
					-1,
					"TICK",
					2,
					2,
					"pulse_cpu_utilization",
					2,
					"INFO : 0/RP0/CPU0  5min CPU Utilization: 2.00 % has returned to Usual range, Threshold: 2.00 SD. It is 0.45 std. dev away from Average.",
					0.45390323755854023,
					2
				]
			]
		}]
	},
	{
		"series": [{
			"columns": [
				"time",
				"activation_threshold",
				"alert_src",
				"clear_threshold",
				"crit_threshold",
				"id",
				"kpi_stream",
				"msg",
				"sigma",
				"warn_threshold"
			],
			"name": "alerts",
			"tags": {
				"CollectorId": "mdt-robot-collector-13a3958e-63d5-47e5-9e0f-31e846b89f2e",
				"EncodingPath": "Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface/latest/data-rate",
				"Producer": "spnac-a9k-s078",
				"UUID": "16df73dc-0614-44bd-885a-1cad09a68689",
				"interface-name": "GigabitEthernet0/0/0/0",
				"kpi_id": "pulse_interface_rate_counters",
				"level": "INFO",
				"state": "clear"
			},
			"values": [
				[
					"2019-09-05T22:03:03.496Z",
					-1,
					"TICK",
					2,
					2,
					"pulse_interface_rate_counters_rxrate",
					0,
					"INFO : GigabitEthernet0/0/0/0 Rx Rate: 0.00 pkts/sec has returned to Usual range, Threshold: 2.00 SD. It is 0.00 std.dev away from Average.",
					0,
					2
				]
			]
		}]
	}
]

