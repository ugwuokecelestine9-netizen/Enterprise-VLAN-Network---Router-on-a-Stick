# Spanning Tree Protocol

## Overview

Spanning Tree Protocol (STP) was implemented to help prevent Layer 2 switching loops within the Lab 2 network.

The switches were configured to use Per-VLAN Spanning Tree (PVST).

## STP Mode

The confirmed switch configuration includes:

```text
spanning-tree mode pvst
spanning-tree extend system-id

           PortFast

PortFast was configured on designated end-device access ports.

     The confirmed configuration includes:
spanning-tree portfast
PortFast allows an access port connected to an end device to transition to the forwarding state without going through the normal STP listening and learning process.

              Purpose

The STP configuration provides Layer 2 loop prevention within the switched network.
PortFast is used on appropriate end-device access ports to improve the speed at which those devices obtain network connectivity.

STP Troubleshooting

During the implementation of the network, an STP inconsistency was observed on FastEthernet0/6.

The switch reported:

%SPANTREE-2-RECV_PVID_ERR: Received 802.1Q BPDU on non trunk FastEthernet0/6 VLAN1.

%SPANTREE-2-BLOCK_PVID_LOCAL: Blocking FastEthernet0/6 on VLAN0001.

Inconsistent port type.

          Observed Problem

The switch received an 802.1Q BPDU on FastEthernet0/6 while the port was operating as a non-trunk interface.

STP detected an inconsistent port type and blocked the affected port for VLAN 1.

Troubleshooting Evidence

The error messages were captured directly from the Cisco Packet Tracer CLI during the implementation.

This provides evidence of an actual Layer 2 troubleshooting event encountered during the lab.

Resolution

The exact configuration change used to resolve the STP inconsistency is not documented in this section until it is confirmed from the lab configuration.

            Verification

The STP configuration was verified from the switch configuration.

The lab confirms the use of:

PVST
PortFast
STP loop prevent
STP inconsistency detection

            Evidence

The following screenshots provide evidence of the STP implementation and troubleshooting event:
