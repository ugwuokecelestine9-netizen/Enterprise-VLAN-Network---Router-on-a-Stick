# Inter-VLAN Routing

## Overview

Inter-VLAN routing was configured to provide Layer 3 connectivity between the VLANs within the Lab 2 network.

Router0 uses subinterfaces on GigabitEthernet0/0/1 to provide gateway addresses for the configured VLANs.

This approach allows multiple VLANs to use a single physical router interface while maintaining separate Layer 2 broadcast domains.

## Router Subinterfaces

The following router subinterfaces were confirmed:

| Subinterface | VLAN | IP Address |
|--------------|------|------------|
| G0/0/1.10 | 10 | 192.168.10.1 |
| G0/0/1.20 | 20 | 192.168.20.1 |
| G0/0/1.30 | 30 | 192.168.30.1 |
| G0/0/1.99 | 99 | 192.168.99.1 |

## VLAN 10

VLAN 10 uses the following gateway:

```text
192.168.10.1

         Gateway Verification
The router interface configuration was verified using:
show ip interface brief
The output confirmed the configured VLAN subinterfaces and their IP addresses.
               Result
This Lab router is configured with Layer 3 gateway interfaces for VLANs 10, 20, 30, and 99.
This configuration provides the Layer 3 foundation required for communication between the different VLAN networks.
