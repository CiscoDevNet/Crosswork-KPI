
Layer 1 optical FEC errors
====
Atribute|Details
---:|:---
**KPI Name**    | Layer 1 optical FEC errors
**KPI ID**      | `pulse_layer1_optics_fecerrors`
**Category**    | Layer1-Optics
**Summary**     | Monitors per-port optical FEC errors
**Details**     | Monitors per-port optical FEC errors; generates an alert when FEC errors exceeds the configured threshold
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
                            phy-info/phy-present
                            phy-info/loopback
                            phy-info/phy-details/vendor-serial-number
                            phy-info/phy-details/optics-wavelength
                            phy-info/phy-details/vendor
                            phy-info/fec-details/fec
                            phy-info/fec-details/corrected-codeword-count
                            phy-info/fec-details/uncorrected-codeword-count
                            phy-info/media-type
                            layer1-info/link-state
                            layer1-info/speed
                            layer1-info/duplex
                            layer1-info/flowcontrol
                            layer1-info/ipg
                            layer1-info/laser-squelch-enabled
                            layer1-info/bandwidth-utilization
                            layer1-info/bandwidth
                            layer1-info/autoneg/duplex
                            layer1-info/autoneg/flowcontrol
                            layer1-info/autoneg/config-override
                            layer1-info/autoneg/fec
                            layer1-info/autoneg/autoneg-enabled
                            layer1-info/autoneg/mask
                            layer1-info/autoneg/speed
                            layer1-info/led-state
     
Alerting
---

* ### `pulse_layer1_optics_fecerrors`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_layer1_optics_fecerrors```
**Data Filter Logic**    | ```lambda: "phy-info__fec-details__fec" == 'standard```
**KPI Expression Logic** | ```lambda: int("phy-info__fec-details__corrected-codeword-count") + int("phy-info__fec-details__uncorrected-codeword-count")```
**Grouping**             | ```['Producer', 'interface-name']```
**Alerting template**    | two_level_rate_threshold-master-template
---

