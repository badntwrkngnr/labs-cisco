# Port Security

## Objectives

Implement and verify switch port security features to control device access to the network.

## Instructions

1. Identify switch access ports that should have port security enabled.
2. Set the port security violation mode (shutdown, restrict, or protect).
3. Configure the maximum number of MAC addresses.
4. Use sticky MAC learning for dynamic secure address configuration.
5. Verify and test violation behavior.

## Verification

- Use `show port-security` to verify global settings.
- Use `show port-security interface` to check individual ports.
- Use `show mac address-table secure` to view secure MAC addresses.
