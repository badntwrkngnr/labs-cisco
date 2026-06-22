# Layer 3 Switching

## Objectives

Configure a Layer 3 switch to perform inter-VLAN routing without an external router.

## Instructions

1. Enable IP routing on the Layer 3 switch.
2. Create SVIs (Switched Virtual Interfaces) for each VLAN.
3. Assign IP addresses to each SVI to serve as default gateways.
4. Verify hosts in different VLANs can communicate.

## Verification

- Use `show ip route` on the switch.
- Use `show ip interface brief`.
- Test inter-VLAN routing with `ping`.
