
Traffic blackhole
====
Atribute|Details
---:|:---
**KPI Name**    | Traffic blackhole
**KPI ID**      | `pulse_traffic_blackhole`
**Category**    | Layer2-Traffic
**Summary**     | Monitors input and output data rates for black hole behavior
**Details**     | Checks the ratio of output data rate to input data rate and verifies that the ratio is within acceptable ranges, otherwise black hole
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-infra-statsd-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface/latest/data-rate
**Cadence(min)** | 5 (default), 1 (min), 15 (max) , 1 (incr)
**Keys**         | `'Producer'`
**Sensors**      |
                            input-data-rate
                            input-packet-rate
                            output-data-rate
                            output-packet-rate
                            output-load
                            input-load
                            bandwidth
     
Alerting
---

* ### `pulse_traffic_blackhole`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_traffic_blackhole```
**Data Filter Logic**    | ```lambda: "interface-name" =~ /^(FastEthernet|GigabitEthernet|TenGigE|FortyGigE|HundredGigE)\d{1,2}?(\/\d{1,2}?){2,4}$/```
**KPI Expression Logic** | ```none```
**Grouping**             | ```['Producer']```
**Alerting template**    | black_hole_detector-master-template
---

