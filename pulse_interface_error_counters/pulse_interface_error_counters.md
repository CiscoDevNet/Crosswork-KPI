
Interface packet error counters
====
Atribute|Details
---:|:---
**KPI Name**    | Interface packet error counters
**KPI ID**      | `pulse_interface_error_counters`
**Category**    | Layer2-Traffic
**Summary**     | Monitors interface transmit and receive error counters
**Details**     | Monitors interface transmit and receive error counters; generates an alert when unusual error rates occur
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-infra-statsd-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface/latest/generic-counters
**Cadence(min)** | 5 (default), 1 (min), 15 (max) , 1 (incr)
**Keys**         | `'Producer', 'interface-name'`
**Sensors**      |
                            output-drops
                            output-queue-drops
                            input-drops
                            input-queue-drops
                            runt-packets-received
                            giant-packets-received
                            throttled-packets-received
                            parity-packets-received
                            unknown-protocol-packets-received
                            input-errors
                            crc-errors
                            input-overruns
                            framing-errors-received
                            input-ignored-packets
                            input-aborts
                            output-errors
                            output-underruns
                            output-buffer-failures
                            output-buffers-swapped-out
                            carrier-transitions
     
Alerting
---

* ### `pulse_interface_error_counters`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_interface_error_counters```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("crc-errors") + int("framing-errors-received") + int("giant-packets-received") + int("input-aborts") + int("input-drops") + int("input-errors") + int("input-ignored-packets") + int("input-queue-drops") + int("parity-packets-received") + int("runt-packets-received") + int("unknown-protocol-packets-received") + int("input-overruns")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | two_level_rate_threshold-master-template
---

* ### `pulse_interface_error_counters`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_interface_error_counters```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("output-buffer-failures") + int("output-buffers-swapped-out") + int("output-drops") + int("output-errors") + int("output-queue-drops") + int("output-underruns")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | two_level_rate_threshold-master-template
---

