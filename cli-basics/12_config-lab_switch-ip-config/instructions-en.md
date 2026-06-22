# Switch IP Configuration

## Objectives

Configure switch management IP addressing and default gateway settings to enable remote management across different subnets.

## Instructions

1. Configure the Switch Virtual Interface (SVI) with the correct IP address and subnet mask.
2. Ensure the SVI VLAN exists and is active.
3. Configure the default gateway so the switch can communicate with remote networks.
4. Verify Layer 3 connectivity from and to the switch.

## Verification

- Use `show ip interface brief` to check the SVI status.
- Use `show vlan brief` to verify VLAN configuration.
- Ping the default gateway and remote hosts.
