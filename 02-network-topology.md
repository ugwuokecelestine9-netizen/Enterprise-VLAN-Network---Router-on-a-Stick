# Network Topology

## Overview

Lab 2 uses a hierarchical enterprise network topology consisting of a Cisco router, Cisco ASA firewall, multilayer switch, access switches, a DHCP server, and multiple end-user devices.

The topology was implemented in Cisco Packet Tracer.

## Network Devices

The topology contains the following devices:

- Router0 — Cisco 4331 Router
- ASA2 — Cisco ASA 5506-X Firewall
- Multilayer Switch — Cisco 3560-24PS
- Switch1 — Cisco 2960
- Switch2 — Cisco 2960
- Switch4 — Cisco 2960
- DHCP Server
- Multiple Laptop-PT end devices

## Topology Structure

The internal network is centered around the multilayer switch.

The access switches provide connectivity to end-user devices, while the DHCP server is connected to the internal switching infrastructure.

The multilayer switch is connected to the ASA firewall, which provides the connection toward Router0.

The general topology is:

Router0
   |
ASA2
   |
Multilayer Switch
   |
   +--- Switch1 --- End Devices
   |
   +--- Switch2 --- End Devices
   |
   +--- Switch4 --- End Devices
   |
   +--- DHCP Server

## Network Components

### Router0

Router0 is a Cisco 4331 router used as part of the external routing environment.

The router has a connection toward the ASA firewall and contains Layer 3 interfaces associated with the configured VLAN networks.

### ASA2

ASA2 is a Cisco ASA 5506-X firewall positioned between the internal network and Router0.

The confirmed ASA interfaces include:

- GigabitEthernet1/1 — 10.10.10.2
- GigabitEthernet1/2 — 10.10.20.2

### Multilayer Switch

The Cisco 3560-24PS multilayer switch acts as the central switching device within the internal network.

It provides connectivity to the access switches, DHCP server, and ASA.

The switch has a confirmed VLAN 99 interface:

- VLAN 99 — 192.168.99.2/24

### Access Switches

The topology contains multiple Cisco 2960 access switches.

These switches provide Layer 2 connectivity for end-user devices and contain access and trunk interfaces.

### DHCP Server

A dedicated Server-PT device is included in the topology for DHCP services.

The server is connected to the multilayer switch.

## Topology Diagram

The original Packet Tracer topology screenshot is retained as the primary visual reference for this lab.

![Lab 2 Network Topology](../screenshots/topology/lab2-topology.png)

## Topology Evidence

The topology screenshot provides visual evidence of:

- Router0
- ASA2
- Multilayer switch
- Access switches
- DHCP server
- End-user devices
- Physical network connections
