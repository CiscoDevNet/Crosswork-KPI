
Device uptime
====
Atribute|Details
---:|:---
**KPI Name**    | Device uptime
**KPI ID**      | `pulse_device_uptime`
**Category**    | BASICS
**Summary**     | Monitors device uptime
**Details**     | Monitors device uptime
**Collection Type** | SNMP polling
**YANG module/MIB** | SNMPv2-MIB
**Requirements**    |
                  Software Platform : Unknown
                  Hardware Platform : Unknown
Sensors
---
Atribute|Details
---:|:---
**Subscription** | SNMPv2-MIB:SNMPv2-MIB/system
**Cadence(min)** | 10 (default), 10 (min), 30 (max) , 1 (incr)
**Keys**         | `*`
**Sensors**      |
                            sysObjectID
                            sysUpTime
                            sysContact
                            sysName
                            sysLocation
                            sysServices
                            sysORLastChange
     
Alerting
---

* ### `pulse_device_uptime`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_device_uptime```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("sysUpTime")/100.0```
**Grouping**             | ```[*]```
**Alerting template**    | stream-simple-threshold-below-master-template
---

