
Layer 1 optical temperature
====
Atribute|Details
---:|:---
**KPI Name**    | Layer 1 optical temperature
**KPI ID**      | `pulse_layer1_optics_temperature`
**Category**    | Layer1-Optics
**Summary**     | Monitors per-port optical temperature
**Details**     | Monitors per-port optical temperature; generates alert when temperature exceeds the configured threshold
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
**Cadence(min)** | 5 (default), 5 (min), 15 (max) , 1 (incr)
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
                            phy-info/phy-details/transceiver-temperature
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/transceiver-temperature-alarm-low
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/transceiver-temperature-warning-low
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/transceiver-temperature-alarm-high
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/transceiver-temperature-warning-high
                            phy-info/phy-details/dig-opt-mon-alarms/transceiver-temperature
                            layer1-info/link-state
                            layer1-info/led-state
                            layer1-info/speed
                            layer1-info/duplex
                            layer1-info/flowcontrol
     
Alerting
---

* ### `pulse_layer1_optics_temperature`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_layer1_optics_temperature```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: "phy-info__phy-details__dig-opt-mon-alarms__transceiver-temperature"```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | five_state_alert-master-template
---

