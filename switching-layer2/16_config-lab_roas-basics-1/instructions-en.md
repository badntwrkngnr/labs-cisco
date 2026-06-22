# Router on a Stick Basics

## Objectives

Configure inter-VLAN routing using a single router interface with subinterfaces (Router-on-a-Stick).

## Instructions

1. Configure the switch port connected to the router as an 802.1Q trunk.
2. On the router, create subinterfaces for each VLAN.
3. Assign the correct encapsulation dot1Q VLAN ID and IP address to each subinterface.
4. Ensure hosts in each VLAN use the corresponding subinterface IP as their default gateway.

## Verification

- Use `show vlans` on the router to verify subinterfaces.
- Use `show ip interface brief`.
- Test inter-VLAN communication with `ping`.
