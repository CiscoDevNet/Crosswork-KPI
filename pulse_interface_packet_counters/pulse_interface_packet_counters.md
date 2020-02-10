
Interface packet counters
====
Atribute|Details
---:|:---
**KPI Name**    | Interface packet counters
**KPI ID**      | `pulse_interface_packet_counters`
**Category**    | Layer2-Traffic
**Summary**     | Monitors interface transmit and receive counters
**Details**     | Monitors interface transmit and receive counters; generates an alert when unusual traffic rates occur
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-infra-statsd-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface/latest/generic-counters
**Cadence(sec)** | 60 (default), 10 (min), 900 (max) , 10 (incr)
**Keys**         | `*`
**Sensors**      |
                            packets-received
                            bytes-received
                            multicast-packets-received
                            broadcast-packets-received
                            packets-sent
                            bytes-sent
                            multicast-packets-sent
                            broadcast-packets-sent
     
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

