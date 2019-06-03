
IPv6 RIB BGP route count
====
Atribute|Details
---:|:---
**KPI Name**    | IPv6 RIB BGP route count
**KPI ID**      | `pulse_routing_ipv6_rib_bgp`
**Category**    | Layer3-Routing
**Summary**     | Monitors IPv6 RIB for route count and memory used by BGP
**Details**     | Monitors IPv6 RIB for route count and memory used by BGP; generates an alert when an anomaly is detected (such as significant increase or decrease in route counts)
**Collection Type** | Model driven telemetry (MDT)
**YANG module/MIB** | Cisco-IOS-XR-ip-rib-ipv6-oper
**Requirements**    |
                  Software Platform : IOS-XR
                  Hardware Platform : ASR9K, CRS, NCS6K, NCS550x
Sensors
---
Atribute|Details
---:|:---
**Subscription** | Cisco-IOS-XR-ip-rib-ipv6-oper:ipv6-rib/vrfs/vrf/afs/af/safs/saf/ip-rib-route-table-names/ip-rib-route-table-name/protocol/bgp/as/information
**Cadence(min)** | 1 (default), 1 (min), 5 (max) , 1 (incr)
**Keys**         | `*`
**Sensors**      |
                            routes-counts
                            active-routes-count
                            deleted-routes-count
                            protocol-route-memory
                            paths-count
     
Alerting
---

* ### `pulse_routing_ipv6_rib_bgp_routememory`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_routing_ipv6_rib_bgp_routememory```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("protocol-route-memory")```
**Grouping**             | ```[*]```
**Alerting template**    | stream-stddev-activate-master-template
---

* ### `pulse_routing_ipv6_rib_bgp_routecount`
Atribute|Details
---:|:---
**Alert ID**             | ```pulse_routing_ipv6_rib_bgp_routecount```
**Data Filter Logic**    | ```lambda: TRUE```
**KPI Expression Logic** | ```lambda: float("routes-counts")```
**Grouping**             | ```[*]```
**Alerting template**    | stream-stddev-activate-master-template
---

