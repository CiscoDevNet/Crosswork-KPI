
SNMP traffic blackhole
====
Atribute|Details
---:|:---
**KPI Name**    | SNMP traffic blackhole
**KPI ID**      | `pulse_snmp_traffic_blackhole`
**Category**    | Layer2-Traffic
**Summary**     | Monitors input and output data rates for black hole behavior
**Details**     | Checks the ratio of output data rate to input data rate and verifies that the ratio is within acceptable ranges, otherwise black hole
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
**Keys**         | `'Producer', 'ifDescr'`
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

* ### `pulse_snmp_traffic_blackhole`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_snmp_traffic_blackhole```
**Data Filter Logic**    | ```lambda: "ifDescr" =~ /^(FastEthernet|GigabitEthernet|TenGigE|FortyGigE|HundredGigE)\d{1,2}?(\/\d{1,2}?){2,4}$/```
**KPI Expression Logic** | ```none```
**Grouping**             | ```['Producer', 'ifDescr']```
**Alerting template**    | stream_derivative_blackhole_detector-master-template
---

