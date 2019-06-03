
Line state
====
Atribute|Details
---:|:---
**KPI Name**    | Line state
**KPI ID**      | `pulse_interface_state_info`
**Category**    | Layer2-Interface
**Summary**     | Monitors interface line states; generates an alert when link states change
**Details**     | Monitors interface line states; generates an alert when links states change
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-pfi-im-cmd-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-pfi-im-cmd-oper:interfaces/interface-briefs/interface-brief
**Cadence(min)** | 5 (default), 1 (min), 15 (max) , 1 (incr)
**Keys**         | `'Producer', 'interface-name'`
**Sensors**      |
                            type
                            state
                            actual-state
                            line-state
                            actual-line-state
                            encapsulation
                            encapsulation-type-string
                            mtu
                            l2-transport
                            bandwidth
     
Alerting
---

* ### `none`
Atribute|Details
---:|:---
**Alert ID**             | ```none```
**Data Filter Logic**    | ```lambda: isPresent("actual-state") AND isPresent("actual-line-state") AND "state" != 'im-state-admindown```
**KPI Expression Logic** | ```none```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | line_state-master-template
---

