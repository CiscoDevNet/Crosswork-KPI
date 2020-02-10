
Layer 1 optical alarms
====
Atribute|Details
---:|:---
**KPI Name**    | Layer 1 optical alarms
**KPI ID**      | `pulse_layer1_optics_alarms`
**Category**    | Layer1-Optics
**Summary**     | Monitors per-port optical alarms, current and past
**Details**     | Monitors per-port optical alarms, current and past
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-drivers-media-eth-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-drivers-media-eth-oper:ethernet-interface/interfaces/interface
**Cadence(sec)** | 300 (default), 10 (min), 900 (max) , 10 (incr)
**Keys**         | `'Producer', 'interface-name'`
**Sensors**      |
                            admin-state
                            oper-state-up
                            layer1-info/link-state
                            layer1-info/flowcontrol
                            layer1-info/bandwidth-utilization
                            layer1-info/bandwidth
                            layer1-info/current-alarms/pcs-loss-of-block-lock-alarm
                            layer1-info/current-alarms/local-fault-alarm
                            layer1-info/current-alarms/remote-fault-alarm
                            layer1-info/current-alarms/sd-ber-alarm
                            layer1-info/current-alarms/squelch-alarm
                            layer1-info/current-alarms/rx-opd-alarm
                            layer1-info/current-alarms/received-loss-of-signal-alarm
                            layer1-info/current-alarms/loss-of-synchronization-data-alarm
                            layer1-info/current-alarms/hi-ber-alarm
                            layer1-info/current-alarms/sf-ber-alarm
                            layer1-info/led-state
                            layer1-info/speed
                            layer1-info/duplex
                            layer1-info/ipg
                            layer1-info/previous-alarms/squelch-alarm
                            layer1-info/previous-alarms/pcs-loss-of-block-lock-alarm
                            layer1-info/previous-alarms/sf-ber-alarm
                            layer1-info/previous-alarms/loss-of-synchronization-data-alarm
                            layer1-info/previous-alarms/sd-ber-alarm
                            layer1-info/previous-alarms/hi-ber-alarm
                            layer1-info/previous-alarms/rx-opd-alarm
                            layer1-info/previous-alarms/received-loss-of-signal-alarm
                            layer1-info/previous-alarms/local-fault-alarm
                            layer1-info/previous-alarms/remote-fault-alarm
     
Alerting
---

* ### `pulse_layer1_optics_alarms`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_layer1_optics_alarms```
**Data Filter Logic**    | ```lambda: isPresent("layer1-info__current-alarms__hi-ber-alarm") AND isPresent("layer1-info__current-alarms__local-fault-alarm") AND isPresent("layer1-info__current-alarms__loss-of-synchronization-data-alarm") AND isPresent("layer1-info__current-alarms__pcs-loss-of-block-lock-alarm") AND isPresent("layer1-info__current-alarms__received-loss-of-signal-alarm") AND isPresent("layer1-info__current-alarms__remote-fault-alarm") AND isPresent("layer1-info__current-alarms__rx-opd-alarm") AND isPresent("layer1-info__current-alarms__sd-ber-alarm") AND isPresent("layer1-info__current-alarms__squelch-alarm")```
**KPI Expression Logic** | ```none```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | layer1_optics_alarms-master-template
---

