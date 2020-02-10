
Interface flap detection
====
Atribute|Details
---:|:---
**KPI Name**    | Interface flap detection
**KPI ID**      | `pulse_interface_flap_detector`
**Category**    | Layer2-Interface
**Summary**     | Monitors interface flaps
**Details**     | Monitors interface flaps and alerts when flap count reaches set threshold
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-pfi-im-cmd-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-pfi-im-cmd-oper:interfaces/interface-xr/interface
**Cadence(sec)** | 300 (default), 10 (min), 900 (max) , 10 (incr)
**Keys**         | `'Producer', 'interface-name'`
**Sensors**      |
                            interface-type
                            state
                            line-state
                            encapsulation
                            encapsulation-type-string
                            mtu
                            is-l2-transport-enabled
                            state-transition-count
     
Alerting
---

* ### `pulse_interface_flap_detector`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_interface_flap_detector```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("state-transition-count")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | two_level_rate_threshold-master-template
---

