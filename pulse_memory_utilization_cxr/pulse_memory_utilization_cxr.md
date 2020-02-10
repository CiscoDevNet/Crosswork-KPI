
Memory utilization (cXR)
====
Atribute|Details
---:|:---
**KPI Name**    | Memory utilization (cXR)
**KPI ID**      | `pulse_memory_utilization_cxr`
**Category**    | Memory
**Summary**     | Monitors memory usage across route processor and line cards on routers on classic XR devices
**Details**     | Monitors memory usage across route processor and line cards on routers on classic XR devices; generates an alert when memory usage is unusual
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-nto-misc-shmem-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-nto-misc-shmem-oper:memory-summary/nodes/node/summary
**Cadence(sec)** | 120 (default), 10 (min), 900 (max) , 10 (incr)
**Keys**         | `'Producer', 'node-name'`
**Sensors**      |
                            ram-memory
                            free-physical-memory
                            system-ram-memory
                            free-application-memory
     
Alerting
---

* ### `pulse_memory_utilization_cxr`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_memory_utilization_cxr```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: (1.0 - "free-application-memory"/"system-ram-memory") * 100.0```
**Grouping**             | ```['Producer', 'node-name']```
**Alerting template**    | stream-stddev-activate-master-template
---

