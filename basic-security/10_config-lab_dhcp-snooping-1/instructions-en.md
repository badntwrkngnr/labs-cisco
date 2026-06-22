# DHCP Snooping

## Objectives

Configure DHCP snooping to protect the network against rogue DHCP servers and DHCP-based attacks such as starvation and spoofing.

## Instructions

1. Enable DHCP snooping globally on the switch.
2. Define the trusted interfaces (interfaces connected to the legitimate DHCP server).
3. Define the untrusted interfaces (interfaces connected to end devices).
4. Optionally configure DHCP snooping binding database options.
5. Verify DHCP snooping is operational and legitimate DHCP leases are obtained.

## Verification

- Use `show ip dhcp snooping` to verify global settings.
- Use `show ip dhcp snooping binding` to view the binding table.
- Use `show ip dhcp snooping interface` to check trust status per interface.
