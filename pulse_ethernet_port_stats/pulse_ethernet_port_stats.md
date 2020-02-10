
Ethernet port packet statistics
====
Atribute|Details
---:|:---
**KPI Name**    | Ethernet port packet statistics
**KPI ID**      | `pulse_ethernet_port_stats`
**Category**    | Layer1-Traffic
**Summary**     | Monitors port transmit and receive packet statistics
**Details**     | Monitors port transmit and receive packet statistics
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
**Cadence(sec)** | 300 (default), 10 (min), 900 (max) , 10 (incr)
**Keys**         | `'Producer', 'interface-name'`
**Sensors**      |
                            received-total-bytes
                            received-good-bytes
                            received-total-frames
                            received8021q-frames
                            received-pause-frames
                            received-unknown-opcodes
                            received-good-frames
                            received-unicast-frames
                            received-multicast-frames
                            received-broadcast-frames
                            total-bytes-transmitted
                            total-good-bytes-transmitted
                            total-frames-transmitted
                            transmitted8021q-frames
                            transmitted-total-pause-frames
                            transmitted-good-frames
                            transmitted-unicast-frames
                            transmitted-multicast-frames
                            transmitted-broadcast-frames
     
Alerting
---

* ### `pulse_ethernet_port_stats_rxrate`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_ethernet_port_stats_rxrate```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("received-good-bytes")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | stream-derivative-stddev-alert-master-template
---

* ### `pulse_ethernet_port_stats_txrate`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_ethernet_port_stats_txrate```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("total-good-bytes-transmitted")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | stream-derivative-stddev-alert-master-template
---

