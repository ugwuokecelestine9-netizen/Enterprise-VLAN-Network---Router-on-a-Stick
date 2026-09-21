# VLAN Configuration

## Overview

VLANs were configured to logically separate different departments and the server infrastructure within the Lab 2 network.

Four VLANs were confirmed in the switch configuration.

## Configured VLANs

| VLAN ID | VLAN Name | Purpose |
|---------|-----------|---------|
| 10 | HR | Human Resources |
| 20 | RECEPTIONISTS | Reception users |
| 30 | IT | IT department |
| 99 | SERVERS | Server and infrastructure network |

## VLAN 10 — HR

VLAN 10 is assigned to the HR department.

Network:

192.168.10.0/24

Default gateway:

192.168.10.1

## VLAN 20 — RECEPTIONISTS

VLAN 20 is assigned to reception users.

Network:

192.168.20.0/24

Default gateway:

192.168.20.1

Several access ports were configured as access ports for VLAN 20.

## VLAN 30 — IT

VLAN 30 is assigned to the IT department.

Network:

192.168.30.0/24

Default gateway:

192.168.30.1

## VLAN 99 — SERVERS

VLAN 99 is used for servers and infrastructure services.

Network:

192.168.99.0/24

The confirmed Layer 3 addresses include:

- Router gateway: 192.168.99.1
- Multilayer switch: 192.168.99.2

## VLAN Verification

The configured VLANs were verified using:

```text
show vlan brief


The command confirmed the presence of VLANs 10, 20, 30, and 99.
VLAN Segmentation
VLAN segmentation separates the network into logical broadcast domains.
This provides a structured network design where devices belonging to different departments can be separated at Layer 2 while Layer 3 routing can be used where communication between VLANs is required.
Evidence
The VLAN configuration and port assignments are documented using screenshots captured from the Cisco Packet Tracer switch CLI.


### Evidence file

screenshot folder 
```text
screenshots/vlan/vlan-configuration.png 
