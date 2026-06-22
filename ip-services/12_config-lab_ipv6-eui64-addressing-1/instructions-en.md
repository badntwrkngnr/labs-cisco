# IPv6 EUI-64 Addressing

## Objectives

Configure IPv6 global unicast addresses using EUI-64 (Extended Unique Identifier) automatic interface identifier generation.

## Instructions

1. Enable IPv6 unicast routing on the router.
2. Configure an IPv6 address with the `eui-64` option on interfaces.
3. Verify that the interface identifier was derived from the MAC address.
4. Verify IPv6 connectivity.

## Verification

- Use `show ipv6 interface brief` to check IPv6 addresses.
- Use `ping ipv6` to test connectivity.
