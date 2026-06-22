# Configuring Serial Links

## Objectives

Configure and verify WAN serial links between routers, including clock rate, encapsulation, and interface activation.

## Instructions

1. Identify the DCE and DTE sides of the serial connection.
2. Configure the clock rate on the DCE interface.
3. Configure IP addresses on both ends of the serial link.
4. Enable both serial interfaces.
5. Verify Layer 1 and Layer 2 status.

## Verification

- Use `show ip interface brief` to check interface status.
- Use `show controllers serial` to identify DCE/DTE.
- Use `show interfaces serial` to verify encapsulation.
- Ping across the serial link.
