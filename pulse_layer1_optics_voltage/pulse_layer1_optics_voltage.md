
Layer 1 optical voltage
====
Atribute|Details
---:|:---
**KPI Name**    | Layer 1 optical voltage
**KPI ID**      | `pulse_layer1_optics_voltage`
**Category**    | Layer1-Optics
**Summary**     | Monitors per-port optical voltage
**Details**     | Monitors per-port optical voltage; generates alert when voltages exceeds the configured threshold
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
                            phy-info/phy-details/transceiver-voltage
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/transceiver-voltage-alarm-low
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/transceiver-voltage-alarm-high
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/transceiver-voltage-warning-low
                            phy-info/phy-details/dig-opt-mon-alarm-thresholds/transceiver-voltage-warning-high
                            phy-info/phy-details/dig-opt-mon-alarms/transceiver-voltage
                            layer1-info/link-state
                            layer1-info/led-state
                            layer1-info/speed
                            layer1-info/duplex
                            layer1-info/flowcontrol
     
Alerting
---

* ### `pulse_layer1_optics_voltage`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_layer1_optics_voltage```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: "phy-info__phy-details__dig-opt-mon-alarms__transceiver-voltage"```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | five_state_alert-master-template
---

