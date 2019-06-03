
IP SLA UDP jitter monitoring
====
Atribute|Details
---:|:---
**KPI Name**    | IP SLA UDP jitter monitoring
**KPI ID**      | `pulse_ipsla_udp_jitter`
**Category**    | IPSLA
**Summary**     | Monitors IP SLA UDP jitter; generates an alert when an abnormal UDP jitter occurs
**Details**     | Monitors IP SLA UDP jitter; generates an alert when an abnormal UDP jitter occurs
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-man-ipsla-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-man-ipsla-oper:ipsla/operation-data/operations/operation/statistics/latest/target
**Cadence(min)** | 1 (default), 1 (min), 15 (max) , 1 (incr)
**Keys**         | `'Producer', 'operation-id'`
**Sensors**      |
                            specific-stats/udp-jitter-stats/jitter-in
                            specific-stats/udp-jitter-stats/jitter-out
     
Alerting
---

* ### `pulse_ipsla_udp_jitter_in`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_ipsla_udp_jitter_in```
**Data Filter Logic**    | ```lambda: "specific-stats__udp-jitter-stats__jitter-in" > 0```
**KPI Expression Logic** | ```lambda: float("specific-stats__udp-jitter-stats__jitter-in")```
**Grouping**             | ```['Producer', 'operation-id']```
**Alerting template**    | stream-stddev-activate-master-template
---

* ### `pulse_ipsla_udp_jitter_out`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_ipsla_udp_jitter_out```
**Data Filter Logic**    | ```lambda: "specific-stats__udp-jitter-stats__jitter-out" > 0```
**KPI Expression Logic** | ```lambda: float("specific-stats__udp-jitter-stats__jitter-out")```
**Grouping**             | ```['Producer', 'operation-id']```
**Alerting template**    | stream-stddev-activate-master-template
---

