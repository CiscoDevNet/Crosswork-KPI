
LLDP neighbors
====
Atribute|Details
---:|:---
**KPI Name**    | LLDP neighbors
**KPI ID**      | `pulse_layer2_lldp_summary`
**Category**    | LLDP
**Summary**     | Monitors LLDP neighbors; generates an alert when any sudden changes are detected
**Details**     | Monitors LLDP neighbors; generates an alert when any sudden changes are detected
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-ethernet-lldp-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-ethernet-lldp-oper:lldp/nodes/node/neighbors/summaries/summary
**Cadence(min)** | 2 (default), 2 (min), 15 (max) , 1 (incr)
**Keys**         | `'Producer'`
**Sensors**      |
                            lldp-neighbor/device-id
                            lldp-neighbor/chassis-id
                            lldp-neighbor/port-id-detail
                            lldp-neighbor/header-version
                            lldp-neighbor/hold-time
                            lldp-neighbor/enabled-capabilities
     
Alerting
---

* ### `pulse_layer2_lldp_summary`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_layer2_lldp_summary```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: "lldp-neighbor__device-id"```
**Grouping**             | ```['Producer']```
**Alerting template**    | stream-stddev-dist-count-alert-master-template
---

