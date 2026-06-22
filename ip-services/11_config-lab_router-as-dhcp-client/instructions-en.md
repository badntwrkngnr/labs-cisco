# Router as DHCP Client

## Objectives

Configure a router interface to obtain its IP address dynamically from a DHCP server.

## Instructions

1. Configure the router interface with `ip address dhcp`.
2. Ensure the DHCP server has an appropriate pool for the segment.
3. Verify the router receives an IP address, subnet mask, and default gateway.

## Verification

- Use `show ip interface brief` to verify the dynamically assigned address.
- Use `show dhcp lease` to view lease details.
