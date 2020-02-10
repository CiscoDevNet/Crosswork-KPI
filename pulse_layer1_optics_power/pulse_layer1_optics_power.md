
Layer 1 optical power
====
Atribute|Details
---:|:---
**KPI Name**    | Layer 1 optical power
**KPI ID**      | `pulse_layer1_optics_power`
**Category**    | Layer1-Optics
**Summary**     | Monitors per-port optical power
**Details**     | Monitors per-port optical power; generates alert when power levels exceeds the configured threshold
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
                            phy-info/media-type
                            phy-info/phy-present
                            phy-info/loopback
                            phy-info/phy-details/vendor
                            phy-info/phy-details/optics-wavelength
                            phy-info/phy-details/vendor-part-number
                            phy-info/phy-details/vendor-serial-number
                            phy-info/phy-details/transceiver-tx-power
                            phy-info/phy-details/transceiver-tx-bias
                            phy-info/phy-details/transceiver-rx-power
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/laser-bias-warning-high
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/optical-transmit-power-alarm-low
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/optical-receive-power-alarm-high
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/optical-receive-power-warning-high
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/optical-transmit-power-alarm-high
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/optical-transmit-power-warning-high
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/optical-transmit-power-warning-low
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/laser-bias-alarm-high
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/laser-bias-warning-low
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/laser-bias-alarm-low
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/optical-receive-power-warning-low
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/optical-receive-power-alarm-low
                            phy-info/phy-details/dig-opt-mon-alarms/transmit-laser-power
                            phy-info/phy-details/dig-opt-mon-alarms/received-laser-power
                            phy-info/phy-details/dig-opt-mon-alarms/laser-bias-current
                            layer1-info/link-state
                            layer1-info/led-state
                            layer1-info/speed
                            layer1-info/duplex
                            layer1-info/flowcontrol
     
Alerting
---

* ### `pulse_layer1_optics_power_received`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_layer1_optics_power_received```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: "phy-info__phy-details__dig-opt-mon-alarms__received-laser-power"```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | five_state_alert-master-template
---

* ### `pulse_layer1_optics_power_transmit`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_layer1_optics_power_transmit```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: "phy-info__phy-details__dig-opt-mon-alarms__transmit-laser-power"```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | five_state_alert-master-template
---

