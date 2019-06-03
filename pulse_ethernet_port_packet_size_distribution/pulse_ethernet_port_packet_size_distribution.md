
Ethernet port packet size distribution
====
Atribute|Details
---:|:---
**KPI Name**    | Ethernet port packet size distribution
**KPI ID**      | `pulse_ethernet_port_packet_size_distribution`
**Category**    | Layer1-Traffic
**Summary**     | Monitors port transmit and receive packet size distributions
**Details**     | Monitors port transmit and receive packet size distributions
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-drivers-media-eth-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-drivers-media-eth-oper:ethernet-interface/statistics/statistic
**Cadence(min)** | 5 (default), 1 (min), 15 (max) , 1 (incr)
**Keys**         | `*`
**Sensors**      |
                            received-total64-octet-frames
                            received-total-octet-frames-from65-to127
                            received-total-octet-frames-from128-to255
                            received-total-octet-frames-from256-to511
                            received-total-octet-frames-from512-to1023
                            received-total-octet-frames-from1024-to1518
                            received-total-octet-frames-from1519-to-max
                            transmitted-total64-octet-frames
                            transmitted-total-octet-frames-from65-to127
                            transmitted-total-octet-frames-from128-to255
                            transmitted-total-octet-frames-from256-to511
                            transmitted-total-octet-frames-from512-to1023
                            transmitted-total-octet-frames-from1024-to1518
                            transmitted-total-octet-frames-from1518-to-max
     
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

