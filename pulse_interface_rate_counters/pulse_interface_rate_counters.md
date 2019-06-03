
Interface rate counters
====
Atribute|Details
---:|:---
**KPI Name**    | Interface rate counters
**KPI ID**      | `pulse_interface_rate_counters`
**Category**    | Layer2-Traffic
**Summary**     | Monitors interface statistics as rate counters
**Details**     | Monitors interface statistics as rate counters; generates an alert when unusual traffic rates occur
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
**Cadence(min)** | 5 (default), 1 (min), 15 (max) , 1 (incr)
**Keys**         | `'Producer', 'interface-name'`
**Sensors**      |
                            input-data-rate
                            input-packet-rate
                            output-data-rate
                            output-packet-rate
                            output-load
                            input-load
                            bandwidth
     
Alerting
---

* ### `pulse_interface_rate_counters_rxrate`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_interface_rate_counters_rxrate```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("input-data-rate")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | stream-stddev-activate-master-template
---

* ### `pulse_interface_rate_counters_txrate`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_interface_rate_counters_txrate```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("output-data-rate")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | stream-stddev-activate-master-template
---

