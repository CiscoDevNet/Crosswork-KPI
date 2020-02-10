
Interface bandwidth monitor
====
Atribute|Details
---:|:---
**KPI Name**    | Interface bandwidth monitor
**KPI ID**      | `pulse_interface_bandwidth_utilization`
**Category**    | Layer2-Traffic
**Summary**     | Monitors bandwidth utilization across all interfaces on a router
**Details**     | Monitors bandwidth utilization across all interfaces on a router; generates an alert when bandwidth exceeds the configured threshold
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-infra-statsd-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface/latest/data-rate
**Cadence(sec)** | 60 (default), 10 (min), 900 (max) , 10 (incr)
**Keys**         | `'Producer', 'interface-name'`
**Sensors**      |
                            input-data-rate
                            input-packet-rate
                            input-load
                            output-data-rate
                            output-packet-rate
                            output-load
                            bandwidth
     
Alerting
---

* ### `pulse_interface_bandwidth_utilization_rx`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_interface_bandwidth_utilization_rx```
**Data Filter Logic**    | ```lambda: "input-data-rate" > 0.0```
**KPI Expression Logic** | ```lambda: "input-data-rate"/float("bandwidth")*100.0```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | two_level_threshold-master-template
---

* ### `pulse_interface_bandwidth_utilization_rx`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_interface_bandwidth_utilization_rx```
**Data Filter Logic**    | ```lambda: "input-data-rate" > 0.0```
**KPI Expression Logic** | ```lambda: "input-data-rate"/float("bandwidth")*100.0```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | two_level_threshold-master-template
---

