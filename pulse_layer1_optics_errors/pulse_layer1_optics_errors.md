
Layer 1 optical errors
====
Atribute|Details
---:|:---
**KPI Name**    | Layer 1 optical errors
**KPI ID**      | `pulse_layer1_optics_errors`
**Category**    | Layer1-Optics
**Summary**     | Monitors per-port Layer 1 errors
**Details**     | Monitors per-port Layer 1 errors; generates alert when error rates exceeds the configured threshold
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-drivers-media-eth-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-drivers-media-eth-oper:ethernet-interface/interfaces/interface
**Cadence(min)** | 5 (default), 5 (min), 15 (max) , 1 (incr)
**Keys**         | `'Producer', 'node-name'`
**Sensors**      |
                            admin-state
                            oper-state-up
                            layer1-info/link-state
                            layer1-info/error-counts/sync-header-errors
                            layer1-info/error-counts/pcsbip-errors
     
Alerting
---

* ### `pulse_layer1_optics_errors`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_layer1_optics_errors```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("sync-header-errors") + int("pcsbip-errors")```
**Grouping**             | ```['Producer', 'node-name']```
**Alerting template**    | two_level_rate_threshold-master-template
---

