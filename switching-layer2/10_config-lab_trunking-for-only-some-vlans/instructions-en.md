# Trunking for Only Some VLANs

## Objectives

Configure VLAN trunking with restrictions so only specific VLANs are allowed across the trunk.

## Instructions

1. Configure the trunk link between switches.
2. Use the `switchport trunk allowed vlan` command to restrict VLANs.
3. Verify that only the specified VLANs traverse the trunk.
4. Confirm that excluded VLANs cannot communicate across the trunk.

## Verification

- Use `show interfaces trunk` to check allowed VLANs.
- Test connectivity for allowed and excluded VLANs.
