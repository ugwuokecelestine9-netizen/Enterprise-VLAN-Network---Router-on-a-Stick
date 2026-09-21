# Lab 2 — Enterprise Network Infrastructure

## Project Overview

This project demonstrates the design and implementation of a segmented enterprise network using Cisco networking technologies.

The network was built in Cisco Packet Tracer and consists of a Cisco 4331 router, Cisco ASA 5506-X firewall, multilayer switch, multiple Cisco 2960 access switches, a DHCP server, and multiple end-user devices.

The network uses VLAN segmentation to separate different departments and infrastructure services. Inter-VLAN communication is provided through Layer 3 gateway interfaces, while 802.1Q trunking is used to transport multiple VLANs across trunk links.

Layer 2 security mechanisms, including port security and sticky MAC address learning, were also implemented on designated access ports. Spanning Tree Protocol (PVST) and PortFast were configured to provide Layer 2 loop prevention and faster convergence on appropriate access ports.

The project also includes a Cisco ASA firewall connecting the internal network to the external routing environment.

## Technologies Implemented

- VLAN segmentation
- Inter-VLAN routing
- 802.1Q trunking
- Router subinterfaces
- DHCP infrastructure
- Cisco ASA firewall
- Port security
- Sticky MAC address learning
- Spanning Tree Protocol (PVST)
- PortFast
- IP routing
- Network troubleshooting

## Network Segmentation

The following VLANs were configured:

| VLAN ID | Name | Purpose |
|----------|------|---------|
| 10 | HR | Human Resources |
| 20 | RECEPTIONISTS | Reception users |
| 30 | IT | IT department |
| 99 | SERVERS | Server and infrastructure network |

## Lab Objectives

The main objectives of this lab were to:

- Build a segmented enterprise network.
- Configure VLANs on Cisco switches.
- Configure trunk links using 802.1Q.
- Configure Layer 3 gateway interfaces for the VLANs.
- Implement basic Layer 2 security.
- Configure Spanning Tree and PortFast.
- Integrate a DHCP server into the network.
- Connect the internal network through a Cisco ASA firewall.
- Configure routing between the internal and external network segments.
- Identify and troubleshoot network connectivity and Layer 2 issues.

## Platform

**Cisco Packet Tracer**

The configurations and verification results documented in this repository are based on the actual Lab 2 Packet Tracer implementation.
