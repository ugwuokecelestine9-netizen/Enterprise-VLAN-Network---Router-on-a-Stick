# IP Addressing Plan

## Overview

The Lab 2 network uses IPv4 addressing to provide connectivity between the router, VLANs, multilayer switch, and firewall.

The addressing plan is divided into internal VLAN networks and point-to-point infrastructure links.

## VLAN Addressing

| VLAN | Name | Network | Default Gateway |
|------|------|---------|-----------------|
| 10 | HR | 192.168.10.0/24 | 192.168.10.1 |
| 20 | RECEPTIONISTS | 192.168.20.0/24 | 192.168.20.1 |
| 30 | IT | 192.168.30.0/24 | 192.168.30.1 |
| 99 | SERVERS | 192.168.99.0/24 | 192.168.99.1 |

## Router Addressing

Router0 has the following confirmed addresses:

| Interface | IP Address |
|-----------|------------|
| GigabitEthernet0/0/0 | 10.10.10.1 |
| GigabitEthernet0/0/1.10 | 192.168.10.1 |
| GigabitEthernet0/0/1.20 | 192.168.20.1 |
| GigabitEthernet0/0/1.30 | 192.168.30.1 |
| GigabitEthernet0/0/1.99 | 192.168.99.1 |

The router subinterfaces provide Layer 3 gateway addresses for the configured VLANs.

## Router-to-ASA Link

The point-to-point network between Router0 and ASA2 is:

- Network: 10.10.10.0/30
- Router0: 10.10.10.1
- ASA2: 10.10.10.2

This provides the Layer 3 connection between Router0 and the ASA.

## Multilayer Switch Addressing

The multilayer switch has the following confirmed Layer 3 address:

| Interface | IP Address |
|-----------|------------|
| VLAN 99 | 192.168.99.2/24 |

The VLAN 99 interface provides the multilayer switch with Layer 3 connectivity on the server/infrastructure network.

## ASA Addressing

The confirmed ASA interface addresses are:

| Interface | IP Address |
|-----------|------------|
| GigabitEthernet1/1 | 10.10.10.2 |
| GigabitEthernet1/2 | 10.10.20.2 |

The address of the device connected to ASA GigabitEthernet1/2 has not yet been confirmed and is therefore not included in this addressing table.

## Routing Information

The router routing table confirms the following directly connected networks:

- 10.10.10.0/30
- 192.168.10.0/24
- 192.168.20.0/24
- 192.168.30.0/24
- 192.168.99.0/24

A default route is also configured through:

10.10.10.2

## Addressing Verification

The IP addressing information was verified using Cisco IOS interface and routing commands, including:

```text
show ip interface brief
show ip route

