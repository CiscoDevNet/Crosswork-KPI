
SNMP interface packet error counters
====
Atribute|Details
---:|:---
**KPI Name**    | SNMP interface packet error counters
**KPI ID**      | `pulse_snmp_interface_error_counters`
**Category**    | Layer2-Traffic
**Summary**     | Monitors interface transmit and receive error counters
**Details**     | Monitors interface transmit and receive error counters; generates an alert when unusual error rates occur
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
                            ifInUnknownProtos
                            ifInErrors
                            ifInDiscards
                            ifOutDiscards
                            ifOutErrors
     
Alerting
---

* ### `pulse_snmp_interface_error_counters_rx`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_snmp_interface_error_counters_rx```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("ifInDiscards") + int("ifInErrors") + int("ifInUnknownProtos")```
**Grouping**             | ```['Producer', 'ifIndex', 'ifDescr']```
**Alerting template**    | two_level_rate_threshold-master-template
---

* ### `pulse_snmp_interface_error_counters_tx`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_snmp_interface_error_counters_tx```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("ifOutDiscards") + int("ifOutErrors")```
**Grouping**             | ```['Producer', 'ifIndex', 'ifDescr']```
**Alerting template**    | two_level_rate_threshold-master-template
---

