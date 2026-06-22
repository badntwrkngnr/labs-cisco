# Data and Voice VLAN

## Objectives

Configure a switch port to support both data and voice VLANs for an IP phone and PC setup.

## Instructions

1. Create the data VLAN and voice VLAN.
2. Configure the switchport as an access port for the data VLAN.
3. Configure the voice VLAN on the same port.
4. Enable QoS trust if applicable.
5. Verify the port correctly handles both device types.

## Verification

- Use `show interfaces switchport` to verify data and voice VLAN settings.
- Check that the IP phone and PC receive correct addressing.
