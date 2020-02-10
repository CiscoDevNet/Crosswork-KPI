
Interface QoS (ingress)
====
Atribute|Details
---:|:---
**KPI Name**    | Interface QoS (ingress)
**KPI ID**      | `pulse_interface_qos_ingress`
**Category**    | QoS
**Summary**     | Monitors interface QoS on the ingress direction for queue statistics, queue depth
**Details**     | Monitors interface QoS on the ingress direction for queue statistics, queue depth
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-qos-ma-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-qos-ma-oper:qos/nodes/node/policy-map/interface-table/interface/input/service-policy-names/service-policy-instance/statistics
**Cadence(sec)** | 300 (default), 10 (min), 900 (max) , 10 (incr)
**Keys**         | `*`
**Sensors**      |
                            class-stats/general-stats/transmit-packets
                            class-stats/general-stats/transmit-bytes
                            class-stats/general-stats/total-drop-packets
                            class-stats/general-stats/total-drop-bytes
                            class-stats/general-stats/total-drop-rate
                            class-stats/general-stats/match-data-rate
                            class-stats/general-stats/total-transmit-rate
                            class-stats/general-stats/pre-policy-matched-packets
                            class-stats/general-stats/pre-policy-matched-bytes
                            class-stats/police-stats-array/drop-packets
                            class-stats/police-stats-array/drop-bytes
                            class-stats/police-stats-array/conform-packets
                            class-stats/police-stats-array/conform-bytes
                            class-stats/police-stats-array/exceed-packets
                            class-stats/police-stats-array/exceed-bytes
                            class-stats/police-stats-array/violate-packets
                            class-stats/police-stats-array/violate-bytes
                            class-stats/police-stats-array/parent-drop-packets
                            class-stats/police-stats-array/parent-drop-bytes
                            class-stats/police-stats-array/conform-rate
                            class-stats/police-stats-array/exceed-rate
                            class-stats/police-stats-array/violate-rate
                            class-stats/wred-stats-array/profile-title
                            class-stats/wred-stats-array/red-transmit-packets
                            class-stats/wred-stats-array/red-transmit-bytes
                            class-stats/wred-stats-array/random-drop-packets
                            class-stats/wred-stats-array/random-drop-bytes
                            class-stats/wred-stats-array/max-threshold-packets
                            class-stats/wred-stats-array/max-threshold-bytes
                            class-stats/wred-stats-array/red-ecn-marked-packets
                            class-stats/wred-stats-array/red-ecn-marked-bytes
     
Alerting
---

* ### `none`
Atribute|Details
---:|:---
**Alert ID**             | ```none```
**Data Filter Logic**    | ```lambda: FALSE```
**KPI Expression Logic** | ```none```
**Grouping**             | ```[*]```
**Alerting template**    | noop_master-template
---

