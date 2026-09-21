# Port Security

## Overview

Port security was implemented on designated access ports to provide an additional Layer 2 security control.

The configuration restricts access ports by using sticky MAC address learning.

## Port Security Configuration

The confirmed access-port configuration includes:

```text
switchport mode access
switchport access vlan 20
switchport port-security
switchport port-security mac-address sticky

This configuration was applied to designated access ports assigned to VLAN 20 (RECEPTIONISTS).
Sticky MAC Address Learning
Sticky MAC address learning allows the switch to dynamically learn the MAC address connected to a secured access port.
The learned MAC address is then retained as a secure MAC address in the switch configuration.
This helps prevent unauthorized devices from being connected to the protected access ports.

A confirmed example from the lab is:

"interface FastEthernet0/2
 switchport access vlan 20
 switchport mode access
 switchport port-security
 switchport port-security mac-address sticky"
Similar port-security configuration was also observed on additional access ports.


           Security Purpose
Port security provides an additional layer of protection at the access layer by controlling which devices are permitted to use designated switch ports.
The configuration used in this lab combines:
Access mode
VLAN assignment
Port security
Sticky MAC address learning

           Verification
The port-security configuration was verified from the switch configuration output.
The configuration confirms that port security and sticky MAC address learning are enabled on the designated access ports.
Evidence
The port-security configuration screenshot is retained as evidence of the implementation.
