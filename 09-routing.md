# Routing Configuration

## Overview

Routing was configured to provide Layer 3 connectivity between the internal VLAN networks and the external network through the Cisco ASA firewall.

The router's routing table was used to verify the networks directly connected to Router0 and the configured default route.

## Directly Connected Networks

The routing table confirms the following directly connected networks:

| Network | Description |
|---------|-------------|
| 10.10.10.0/30 | Router-to-ASA network |
| 192.168.10.0/24 | VLAN 10 — HR |
| 192.168.20.0/24 | VLAN 20 — RECEPTIONISTS |
| 192.168.30.0/24 | VLAN 30 — IT |
| 192.168.99.0/24 | VLAN 99 — SERVERS |

## Default Route

Router0 has a default route pointing to the ASA interface at:

```text
10.10.10.2

The routing table displays the default route as:
0.0.0.0/0 via 10.10.10.2
This provides a route of last resort for destinations that are not present in the router's routing table.
Routing Table Verification
The routing table was verified using:
show ip route
The output confirmed the directly connected VLAN networks and the configured default route.
Routing Structure
The confirmed routing relationship between Router0 and the ASA is:
Internal Networks
       |
    Router0
10.10.10.1
       |
       |
10.10.10.2
      ASA2
       |
   External Side
Verification
The routing configuration was verified using the router's routing table.
The verification confirmed:
10.10.10.0/30 is directly connected.
192.168.10.0/24 is directly connected.
192.168.20.0/24 is directly connected.
192.168.30.0/24 is directly connected.
192.168.99.0/24 is directly connected.
A default route points to 10.10.10.2.
Evidence
The routing table screenshot is retained as evidence of the configured routes.


### Evidence file

```text
screenshots/
└── routing/
    └── router-routing-table.png
