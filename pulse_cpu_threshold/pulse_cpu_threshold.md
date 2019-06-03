
CPU threshold
====
Atribute|Details
---:|:---
**KPI Name**    | CPU threshold
**KPI ID**      | `pulse_cpu_threshold`
**Category**    | CPU
**Summary**     | Monitors CPU usage across route processor and line cards on routers
**Details**     | Monitors CPU usage across route processor and line cards on routers; generates an alert when CPU utilization exceeds the configured threshold
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-wdsysmon-fd-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-wdsysmon-fd-oper:system-monitoring/cpu-utilization
**Cadence(min)** | 1 (default), 1 (min), 15 (max) , 1 (incr)
**Keys**         | `'Producer', 'node-name'`
**Sensors**      |
                            total-cpu-one-minute
                            total-cpu-five-minute
                            total-cpu-fifteen-minute
     
Alerting
---

* ### `pulse_cpu_threshold`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_cpu_threshold```
**Data Filter Logic**    | ```lambda: "total-cpu-five-minute" > 0```
**KPI Expression Logic** | ```lambda: float("total-cpu-five-minute")```
**Grouping**             | ```['Producer', 'node-name']```
**Alerting template**    | two_level_threshold-master-template
---

