
IP SLA UDP Echo RTT
====
Atribute|Details
---:|:---
**KPI Name**    | IP SLA UDP Echo RTT
**KPI ID**      | `pulse_ipsla_udp_echo_rtt`
**Category**    | IPSLA
**Summary**     | Monitors IP SLA UDP echo RTT; generates an alert when unusual RTT values occur
**Details**     | Monitors IP SLA UDP echo RTT; generates an alert when unusual RTT values occur
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
                            common-stats/response-time
     
Alerting
---

* ### `pulse_ipsla_udp_echo_rtt`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_ipsla_udp_echo_rtt```
**Data Filter Logic**    | ```lambda: "common-stats__response-time" > 0```
**KPI Expression Logic** | ```lambda: float("common-stats__response-time")```
**Grouping**             | ```['Producer', 'operation-id']```
**Alerting template**    | stream-stddev-activate-master-template
---

