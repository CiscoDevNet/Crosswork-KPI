
SNMP interface packet counters
====
Atribute|Details
---:|:---
**KPI Name**    | SNMP interface packet counters
**KPI ID**      | `pulse_snmp_interface_packet_counters`
**Category**    | Layer2-Traffic
**Summary**     | Monitors interface transmit and receive counters
**Details**     | Monitors interface transmit and receive counters; generates an alert when unusual traffic rates occur
**Collection Type** | SNMP polling
**YANG module/MIB** | IF-MIB
**Requirements**    |
                  Software Platform : Unknown
                  Hardware Platform : Unknown
Sensors
---
Atribute|Details
---:|:---
**Subscription** | IF-MIB:IF-MIB/ifTable/ifEntry
**Cadence(sec)** | 300 (default), 60 (min), 900 (max) , 60 (incr)
**Keys**         | `*`
**Sensors**      |
                            ifName
                            ifDescr
                            ifAlias
                            ifType
                            ifMtu
                            ifSpeed
                            ifAdminStatus
                            ifOperStatus
                            ifHCInOctets
                            ifHCOutOctets
                            ifHCInUcastPkts
                            ifHCInMulticastPkts
                            ifHCInBroadcastPkts
                            ifHCOutUcastPkts
                            ifHCOutMulticastPkts
                            ifHCOutBroadcastPkts
     
Alerting
---

* ### `none`
Atribute|Details
---:|:---
**Alert ID**             | ```none```
**Data Filter Logic**    | ```lambda: FALSE```
**KPI Expression Logic** | ```none```
**Grouping**             | ```[*]```
**Alerting template**    | noop_master-template
---

