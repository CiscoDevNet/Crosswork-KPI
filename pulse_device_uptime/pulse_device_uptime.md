
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
**Cadence(sec)** | 600 (default), 600 (min), 1800 (max) , 60 (incr)
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

