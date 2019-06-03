
SNMP interface rate counters
====
Atribute|Details
---:|:---
**KPI Name**    | SNMP interface rate counters
**KPI ID**      | `pulse_snmp_interface_rate_counters`
**Category**    | Layer2-Traffic
**Summary**     | Monitors interface statistics as rate counters
**Details**     | Monitors interface statistics as rate counters; generates an alert when unusual traffic rates occur
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
**Cadence(min)** | 5 (default), 1 (min), 15 (max) , 1 (incr)
**Keys**         | `'Producer', 'ifIndex', 'ifDescr'`
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

* ### `pulse_snmp_interface_rate_counters_rxrate`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_snmp_interface_rate_counters_rxrate```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("ifHCInOctets")*8.0```
**Grouping**             | ```['Producer', 'ifIndex', 'ifDescr']```
**Alerting template**    | stream-derivative-stddev-alert-master-template
---

* ### `pulse_snmp_interface_rate_counters_txrate`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_snmp_interface_rate_counters_txrate```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("ifHCOutOctets")*8.0```
**Grouping**             | ```['Producer', 'ifIndex', 'ifDescr']```
**Alerting template**    | stream-derivative-stddev-alert-master-template
---

