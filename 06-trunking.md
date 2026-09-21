# Trunking Configuration

## Overview

802.1Q trunking was configured to allow multiple VLANs to traverse the same physical links between network devices.

Trunking is used to transport VLAN traffic between the switching infrastructure and other network devices where required.

## Trunk Configuration

The confirmed trunk configuration includes the following VLANs:

- VLAN 10 — HR
- VLAN 20 — RECEPTIONISTS
- VLAN 30 — IT
- VLAN 99 — SERVERS

The allowed VLAN list was configured as:

```text
10,20,30,99

       Trunking Configuration Commands:

The switch interfaces were configured with trunking using commands including:

"switchport mode trunk
switchport trunk allowed vlan 10,20,30,99"

802.1Q encapsulation was also confirmed on interfaces where the configuration explicitly showed:
switchport trunk encapsulation dot1q

             Purpose of Trunking
The trunk links allow traffic from multiple VLANs to travel across a single physical connection while maintaining VLAN separation through 802.1Q tagging.
This is necessary for carrying VLAN traffic between the switching infrastructure and the Layer 3 routing environment.
Verification
The trunk configuration was verified from the switch configuration.
The documented configuration confirms that VLANs 10, 20, 30, and 99 are permitted across the configured trunk links.

                    Evidence
The trunk configuration screenshots are retained as evidence of the implementation in SCREENSHOT FOLDER
�
