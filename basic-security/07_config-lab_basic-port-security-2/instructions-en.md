# Basic Port Security

## Objectives

Implement port security on switch interfaces to restrict access based on MAC addresses and prevent unauthorized devices from connecting to the network.

## Instructions

1. Identify the access switch ports that connect to end devices.
2. Configure each access port with the appropriate port security mode:
   - Restrict mode
   - Protect mode
   - Shutdown mode
3. Set the maximum number of allowed MAC addresses per port.
4. Configure the MAC address learning method (static or sticky).
5. Verify port security is active and violations are logged.

## Verification

- Use `show port-security` to view port security status.
- Use `show port-security interface` to check specific interfaces.
- Test by connecting an unauthorized device and observing the violation action.
