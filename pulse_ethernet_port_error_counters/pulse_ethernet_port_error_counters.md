
Ethernet port error counters
====
Atribute|Details
---:|:---
**KPI Name**    | Ethernet port error counters
**KPI ID**      | `pulse_ethernet_port_error_counters`
**Category**    | Layer1-Traffic
**Summary**     | Monitors port transmit and receive error counters
**Details**     | Monitors port transmit and receive error counters
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
                            received-good-frames
                            number-of-buffer-overrun-packets-dropped
                            number-of-aborted-packets-dropped
                            numberof-invalid-vlan-id-packets-dropped
                            invalid-dest-mac-drop-packets
                            invalid-encap-drop-packets
                            number-of-miscellaneous-packets-dropped
                            dropped-giant-packets-greaterthan-mru
                            dropped-ether-stats-undersize-pkts
                            dropped-jabbers-packets-greaterthan-mru
                            dropped-ether-stats-fragments
                            dropped-packets-with-crc-align-errors
                            ether-stats-collisions
                            symbol-errors
                            dropped-miscellaneous-error-packets
                            rfc2819-ether-stats-oversized-pkts
                            rfc2819-ether-stats-jabbers
                            rfc2819-ether-stats-crc-align-errors
                            rfc3635dot3-stats-alignment-errors
                            total-bytes-transmitted
                            total-good-bytes-transmitted
                            total-frames-transmitted
                            transmitted-good-frames
                            buffer-underrun-packet-drops
                            aborted-packet-drops
                            uncounted-dropped-frames
                            miscellaneous-output-errors
     
Alerting
---

* ### `pulse_ethernet_port_error_counters_mru`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_ethernet_port_error_counters_mru```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("dropped-giant-packets-greaterthan-mru") + int("dropped-ether-stats-undersize-pkts") + int("dropped-jabbers-packets-greaterthan-mru") + int("dropped-ether-stats-fragments") + int("dropped-packets-with-crc-align-errors") + int("ether-stats-collisions") + int("symbol-errors") + int("dropped-miscellaneous-error-packets")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | two_level_rate_threshold-master-template
---

* ### `pulse_ethernet_port_error_counters_dropped_packets`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_ethernet_port_error_counters_dropped_packets```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("number-of-buffer-overrun-packets-dropped") + int("number-of-aborted-packets-dropped") + int("numberof-invalid-vlan-id-packets-dropped") + int("invalid-dest-mac-drop-packets") + int("invalid-encap-drop-packets") + int("number-of-miscellaneous-packets-dropped")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | two_level_rate_threshold-master-template
---

* ### `pulse_ethernet_port_error_counters_rfc`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_ethernet_port_error_counters_rfc```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("rfc2819-ether-stats-oversized-pkts") + int("rfc2819-ether-stats-jabbers") + int("rfc2819-ether-stats-crc-align-errors")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | two_level_rate_threshold-master-template
---

* ### `pulse_ethernet_port_error_counters_misc`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_ethernet_port_error_counters_misc```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("miscellaneous-output-errors")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | two_level_rate_threshold-master-template
---

* ### `pulse_ethernet_port_error_counters_underruns`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_ethernet_port_error_counters_underruns```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("buffer-underrun-packet-drops") + int("aborted-packet-drops") + int("uncounted-dropped-frames")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | two_level_rate_threshold-master-template
---

