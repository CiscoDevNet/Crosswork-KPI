
Interface counters by protocol
====
Atribute|Details
---:|:---
**KPI Name**    | Interface counters by protocol
**KPI ID**      | `pulse_intf_stat_protocol`
**Category**    | Layer3-Traffic
**Summary**     | Monitors interface statistics by protocol
**Details**     | Monitors interface statistics (such as incoming and outgoing packets or byte counters) organized by protocol
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-infra-statsd-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface/latest/protocols/protocol
**Cadence(min)** | 5 (default), 1 (min), 15 (max) , 1 (incr)
**Keys**         | `*`
**Sensors**      |
                            bytes-received
                            bytes-sent
                            packets-received
                            packets-sent
                            protocol
                            input-data-rate
                            input-packet-rate
                            output-data-rate
                            output-packet-rate
     
Alerting
---

* ### `pulse_intf_stat_protocol_counters_rxrate`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_intf_stat_protocol_counters_rxrate```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("input-data-rate")```
**Grouping**             | ```[*]```
**Alerting template**    | stream-stddev-aggregate-alert-master-template
---

* ### `pulse_intf_stat_protocol_counters_txrate`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_intf_stat_protocol_counters_txrate```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("output-data-rate")```
**Grouping**             | ```[*]```
**Alerting template**    | stream-stddev-aggregate-alert-master-template
---

