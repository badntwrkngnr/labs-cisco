# VLAN and VTP Configuration

## Objectives

Configure VLANs and VLAN Trunking Protocol (VTP) to manage VLAN distribution across multiple switches.

## Instructions

1. Configure VTP domain, mode, and password on each switch.
2. Create VLANs on the VTP server switch.
3. Verify VLANs are propagated to VTP client switches.
4. Configure trunk links between switches.

## Verification

- Use `show vtp status` to verify VTP operating mode.
- Use `show vlan brief` to verify VLAN database.
- Use `show interfaces trunk` to check trunk status.
