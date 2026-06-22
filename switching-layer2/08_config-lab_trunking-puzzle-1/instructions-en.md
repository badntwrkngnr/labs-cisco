# Trunking Puzzle

## Objectives

Analyze and fix VLAN trunking misconfigurations to restore connectivity between switches.

## Instructions

1. Examine the current trunk configurations.
2. Identify any mismatches in encapsulation, allowed VLANs, or native VLAN.
3. Correct the trunk configurations to match requirements.
4. Verify all required VLANs are passing over trunks.

## Verification

- Use `show interfaces trunk`.
- Use `show interfaces switchport`.
- Test connectivity across switches for each VLAN.
