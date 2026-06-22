# VLAN Basics

## Objectives

Create and assign VLANs on a Cisco switch to segment a LAN into multiple broadcast domains.

## Instructions

1. Create the required VLANs with names.
2. Assign access ports to the correct VLANs.
3. Verify VLAN assignments on each switch.
4. Test that hosts in different VLANs cannot communicate without a router.

## Verification

- Use `show vlan brief` to view VLANs.
- Use `show interfaces switchport` to check port assignments.
- Use `ping` to test inter-VLAN connectivity.
