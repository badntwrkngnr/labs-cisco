# Layer 2 EtherChannel

## Objectives

Bundle multiple physical switch links into a single logical Layer 2 EtherChannel for increased bandwidth and redundancy.

## Instructions

1. Configure the physical interfaces as trunk ports.
2. Create the EtherChannel bundle using PAgP or LACP.
3. Assign the port-channel interface to the appropriate VLAN mode.
4. Verify the EtherChannel is operational.

## Verification

- Use `show etherchannel summary` to view bundle status.
- Use `show interfaces port-channel`.
- Test failover by shutting down one physical link.
