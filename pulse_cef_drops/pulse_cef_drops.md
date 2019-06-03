
CEF drops
====
Atribute|Details
---:|:---
**KPI Name**    | CEF drops
**KPI ID**      | `pulse_cef_drops`
**Category**    | Dataplane-Counters
**Summary**     | Monitors CEF drop counters
**Details**     | Monitors CEF drop counters and baseline; generates an alert when an unusual amount of drops occur
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-fib-common-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-fib-common-oper:fib-statistics/nodes/node/drops
**Cadence(min)** | 1 (default), 1 (min), 15 (max) , 1 (incr)
**Keys**         | `'Producer', 'node-name'`
**Sensors**      |
                            no-route-packets
                            punt-unreachable-packets
                            df-unreachable-packets
                            encapsulation-failure-packets
                            incomplete-adjacency-packets
                            unresolved-prefix-packets
                            unsupported-feature-packets
                            discard-packets
                            checksum-error-packets
                            fragmenation-consumed-packets
                            fragmenation-failure-packets
                            null-packets
                            rpf-check-failure-packets
                            acl-in-rpf-packets
                            rp-destination-drop-packets
                            total-number-of-drop-packets
                            mpls-disabled-interface
                            gre-lookup-failed-drop
                            gre-error-drop
                            lisp-punt-drops
                            lisp-encap-error-drops
                            lisp-decap-error-drops
                            multi-label-drops
     
Alerting
---

* ### `pulse_cef_drops`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_cef_drops```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: int("acl-in-rpf-packets") + int("checksum-error-packets") + int("df-unreachable-packets") + int("discard-packets") + int("encapsulation-failure-packets") + int("fragmenation-consumed-packets") + int("fragmenation-failure-packets") + int("gre-error-drop") + int("gre-lookup-failed-drop") + int("incomplete-adjacency-packets") + int("lisp-decap-error-drops") + int("lisp-encap-error-drops") + int("lisp-punt-drops") + int("mpls-disabled-interface") + int("multi-label-drops") + int("no-route-packets")+ int("null-packets") + int("punt-unreachable-packets") + int("rp-destination-drop-packets") + int("rpf-check-failure-packets") + int("unresolved-prefix-packets") + int("unsupported-feature-packets")```
**Grouping**             | ```['Producer', 'node-name']```
**Alerting template**    | two_level_rate_threshold-master-template
---

