
ISIS neighbor summary
====
Atribute|Details
---:|:---
**KPI Name**    | ISIS neighbor summary
**KPI ID**      | `pulse_routing_isis_neighbor_summary`
**Category**    | Protocol-ISIS
**Summary**     | Monitors IS-IS neighbor summaries for changes in neighbor status
**Details**     | Monitors IS-IS neighbor summaries for changes in neighbor status; generates an alert when an anomaly is detected (such as neighbors down or flapping)
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-clns-isis-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-clns-isis-oper:isis/instances/instance/neighbor-summaries/neighbor-summary
**Cadence(sec)** | 60 (default), 10 (min), 300 (max) , 10 (incr)
**Keys**         | `'Producer'`
**Sensors**      |
                            level12-neigbors/neighbor-up-count
                            level12-neigbors/neighbor-init-count
                            level12-neigbors/neighbor-down-count
                            level1-neighbors/neighbor-up-count
                            level1-neighbors/neighbor-init-count
                            level1-neighbors/neighbor-down-count
                            level2-neighbors/neighbor-init-count
                            level2-neighbors/neighbor-down-count
                            level2-neighbors/neighbor-up-count
     
Alerting
---

* ### `pulse_routing_isis_neighbor_summary`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_routing_isis_neighbor_summary```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("level2-neighbors__neighbor-up-count" + "level1-neighbors__neighbor-up-count" + "level12-neighbors__neighbor-up-count")```
**Grouping**             | ```['Producer']```
**Alerting template**    | stream-stddev-aggregate-alert-master-template
---

